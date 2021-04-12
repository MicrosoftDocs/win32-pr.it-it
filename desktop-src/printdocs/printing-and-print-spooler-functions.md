---
description: L'API spooler di stampa contiene le funzioni e le strutture dei dati utilizzate dalle applicazioni per gestire lo spooler di stampa di Windows e le stampanti e i processi di stampa che controlla.
ms.assetid: d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39
title: Funzioni dell'API spooler di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df751b11206ebf26d2d0e8fd88f61ede8447dad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233609"
---
# <a name="print-spooler-api-functions"></a>Funzioni dell'API spooler di stampa

L'API spooler di stampa contiene le funzioni e le strutture dei dati utilizzate dalle applicazioni per gestire lo spooler di stampa di Windows e le stampanti e i processi di stampa che controlla.

Le funzioni dell'API spooler di stampa sono divise nei gruppi seguenti:

-   [Funzioni del processo di stampa](#print-job-functions)
-   [Funzioni dell'interfaccia utente della stampante](#printer-user-interface-functions)
-   [Funzioni stampante](#printer-functions)
-   [Funzioni di notifica della modifica della stampante](#printer-change-notification-functions)
-   [Funzioni modulo stampante](#printer-form-functions)
-   [Funzioni spooler di stampa](#print-spooler-api-functions)

## <a name="print-job-functions"></a>Funzioni del processo di stampa

Queste funzioni inviano processi di stampa a una stampante e tengono traccia e controllano i processi di stampa nello spooler di stampa.



| Funzione                                                                      | Descrizione                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddJob**](addjob.md)<br/>                                           | La funzione [**AddJob**](/windows/desktop/printdocs/addjob) aggiunge un processo di stampa all'elenco dei processi di stampa che possono essere pianificati dallo spooler di stampa. La funzione recupera il nome del file che è possibile usare per archiviare il processo. <br/>                                      |
| [**ClosePrinter**](closeprinter.md)<br/>                               | La funzione [**ClosePrinter**](/windows/desktop/printdocs/closeprinter) chiude l'oggetto stampante specificato. <br/>                                                                                                                                                      |
| [**DocumentEvent**](documentevent.md)<br/>                             | La funzione [**DocumentEvent**](/windows/desktop/printdocs/documentevent) è un gestore eventi per gli eventi associati alla stampa di un documento. <br/>                                                                                                                     |
| [**DocumentProperties**](documentproperties.md)<br/>                   | La funzione [**DocumentProperties**](/windows/desktop/printdocs/documentproperties) Recupera o modifica le informazioni di inizializzazione della stampante o Visualizza una finestra delle proprietà di configurazione della stampante per la stampante specificata. <br/>                                        |
| [**EndDocPrinter**](enddocprinter.md)<br/>                             | La funzione [**EndDocPrinter**](/windows/desktop/printdocs/enddocprinter) termina un processo di stampa per la stampante specificata. <br/>                                                                                                                                             |
| [**EndPagePrinter**](endpageprinter.md)<br/>                           | La funzione [**EndPagePrinter**](/windows/desktop/printdocs/endpageprinter) notifica allo spooler di stampa che l'applicazione si trova alla fine di una pagina in un processo di stampa. <br/>                                                                                               |
| [**EnumJobs**](enumjobs.md)<br/>                                       | La funzione [**EnumJobs**](/windows/desktop/printdocs/enumjobs) recupera le informazioni su un set specificato di processi di stampa per una stampante specificata. <br/>                                                                                                                |
| [**GetJob**](getjob.md)<br/>                                           | La funzione [**GetJob**](/windows/desktop/printdocs/getjob) recupera le informazioni su un processo di stampa specificato. <br/>                                                                                                                                                    |
| [**OpenPrinter**](openprinter.md)<br/>                                 | La funzione [**OpenPrinter**](/windows/desktop/printdocs/openprinter) recupera un handle per la stampante o il server di stampa specificato o per altri tipi di handle nel sottosistema di stampa. <br/>                                                                               |
| [**OpenPrinter2**](openprinter2.md)<br/>                               | Recupera un handle per la stampante, il server di stampa o altri tipi di handle specificati nel sottosistema di stampa, durante l'impostazione di alcune opzioni della stampante.<br/>                                                                                      |
| [**ReportJobProcessingProgress**](reportjobprocessingprogress.md)<br/> | Segnala al servizio spooler di stampa se un processo di stampa XPS si trova nella fase di spooling o di rendering e quale parte dell'elaborazione è attualmente in corso.<br/>                                                                               |
| [**ScheduleJob**](schedulejob.md)<br/>                                 | La funzione [**ScheduleJob**](/windows/desktop/printdocs/schedulejob) richiede che lo spooler di stampa pianifichi un processo di stampa specificato per la stampa. <br/>                                                                                                                |
| [**SetJob**](setjob.md)<br/>                                           | La funzione [**SetJob**](/windows/desktop/printdocs/setjob) sospende, riprende, Annulla o riavvia un processo di stampa su una stampante specificata. È inoltre possibile utilizzare la funzione **SetJob** per impostare i parametri del processo di stampa, ad esempio la priorità del processo di stampa e il nome del documento. <br/> |
| [**StartDocPrinter**](startdocprinter.md)<br/>                         | La funzione [**StartDocPrinter**](/windows/desktop/printdocs/startdocprinter) notifica allo spooler di stampa che è necessario eseguire lo spooling di un documento per la stampa. <br/>                                                                                                           |
| [**StartPagePrinter**](startpageprinter.md)<br/>                       | La funzione [**StartPagePrinter**](/windows/desktop/printdocs/startpageprinter) notifica allo spooler che una pagina sta per essere stampata sulla stampante specificata. <br/>                                                                                                 |



 

## <a name="printer-user-interface-functions"></a>Funzioni dell'interfaccia utente della stampante

Queste funzioni visualizzano un'interfaccia utente che consente all'utente di selezionare o configurare una stampante.



| Funzione                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedDocumentProperties**](advanceddocumentproperties.md)<br/> | La funzione [**AdvancedDocumentProperties**](/windows/desktop/printdocs/advanceddocumentproperties) Visualizza una finestra di dialogo di configurazione della stampante per la stampante specificata, consentendo all'utente di configurare la stampante. <br/>                                                                                                                                                      |
| [**ConfigurePort**](configureport.md)<br/>                           | La funzione [**ConfigurePort**](/windows/desktop/printdocs/configureport) Visualizza la finestra di dialogo configurazione porta per una porta nel server specificato. <br/>                                                                                                                                                                                                                     |
| [**ConnectToPrinterDlg**](connecttoprinterdlg.md)<br/>               | La funzione [**ConnectToPrinterDlg**](/windows/desktop/printdocs/connecttoprinterdlg) Visualizza una finestra di dialogo che consente agli utenti di esplorare e connettersi alle stampanti in una rete. Se l'utente seleziona una stampante, la funzione tenta di crearvi una connessione. Se nel server non è installato un driver idoneo, all'utente viene offerta la possibilità di creare una stampante localmente. <br/> |
| [**PrinterProperties**](printerproperties.md)<br/>                   | La funzione [**PrinterProperties**](/windows/desktop/printdocs/printerproperties) Visualizza una finestra delle proprietà Printer-Properties per la stampante specificata. <br/>                                                                                                                                                                                                                    |



 

## <a name="printer-functions"></a>Funzioni stampante

Queste funzioni aggiungono e configurano le stampanti utilizzate dallo spooler di stampa.



| Funzione                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPrinter**](abortprinter.md)<br/>                       | La funzione [**AbortPrinter**](/windows/desktop/printdocs/abortprinter) Elimina il file di spool della stampante se la stampante è configurata per lo spooling. <br/>                                                                                                                                                                                                                                                                  |
| [**AddPrinter**](addprinter.md)<br/>                           | La funzione [**AddPrinter**](/windows/desktop/printdocs/addprinter) aggiunge una stampante all'elenco delle stampanti supportate per un server specificato. <br/>                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection**](addprinterconnection.md)<br/>       | La funzione **AddPrinterConnection** aggiunge una connessione alla stampante specificata per l'utente corrente. <br/>                                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection2**](addprinterconnection2.md)<br/>     | Aggiunge una connessione alla stampante specificata per l'utente corrente e specifica i dettagli della connessione.<br/>                                                                                                                                                                                                                                                                                             |
| [**DeletePrinter**](deleteprinter.md)<br/>                     | La funzione [**DeletePrinter**](/windows/desktop/printdocs/deleteprinter) Elimina l'oggetto stampante specificato. <br/>                                                                                                                                                                                                                                                                                                    |
| [**DeletePrinterConnection**](deleteprinterconnection.md)<br/> | La funzione [**DeletePrinterConnection**](/windows/desktop/printdocs/deleteprinterconnection) Elimina una connessione a una stampante stabilita da una chiamata a [**AddPrinterConnection**](addprinterconnection.md) o [**ConnectToPrinterDlg**](connecttoprinterdlg.md). <br/>                                                                                                                                      |
| [**DeletePrinterData**](deleteprinterdata.md)<br/>             | La funzione [**DeletePrinterData**](/windows/desktop/printdocs/deleteprinterdata) Elimina i dati di configurazione specificati per una stampante. I dati di configurazione di una stampante sono costituiti da un set di valori denominati e tipizzati. La funzione **DeletePrinterData** Elimina uno di questi valori, specificato in base al nome del relativo valore. <br/>                                                                                                     |
| [**DeletePrinterDataEx**](deleteprinterdataex.md)<br/>         | La funzione [**DeletePrinterDataEx**](/windows/desktop/printdocs/deleteprinterdataex) Elimina un valore specificato dai dati di configurazione di una stampante. I dati di configurazione di una stampante sono costituiti da un set di valori denominati e tipizzati archiviati in una gerarchia di chiavi del registro di sistema. La funzione Elimina un valore specificato in una chiave specificata. <br/>                                                                        |
| [**DeletePrinterKey**](deleteprinterkey.md)<br/>               | La funzione [**DeletePrinterKey**](/windows/desktop/printdocs/deleteprinterkey) Elimina una chiave specificata e tutte le relative sottochiavi per una stampante specificata. <br/>                                                                                                                                                                                                                                                               |
| [**EnumPrinterData**](enumprinterdata.md)<br/>                 | La funzione [**EnumPrinterData**](/windows/desktop/printdocs/enumprinterdata) enumera i dati di configurazione per una stampante specificata. <br/>                                                                                                                                                                                                                                                                               |
| [**EnumPrinterDataEx**](enumprinterdataex.md)<br/>             | La funzione [**EnumPrinterDataEx**](/windows/desktop/printdocs/enumprinterdataex) enumera tutti i nomi e i dati dei valori per una stampante e una chiave specificate. <br/>                                                                                                                                                                                                                                                             |
| [**EnumPrinterKey**](enumprinterkey.md)<br/>                   | La funzione [**EnumPrinterKey**](/windows/desktop/printdocs/enumprinterkey) enumera le sottochiavi di una chiave specificata per una stampante specificata. <br/>                                                                                                                                                                                                                                                                     |
| [**EnumPrinters**](enumprinters.md)<br/>                       | La funzione [**EnumPrinters**](/windows/desktop/printdocs/enumprinters) enumera le stampanti disponibili, i server di stampa, i domini o i provider di stampa. <br/>                                                                                                                                                                                                                                                                 |
| [**FlushPrinter**](flushprinter.md)<br/>                       | La funzione [**FlushPrinter**](/windows/desktop/printdocs/flushprinter) Invia un buffer alla stampante per cancellarla da uno stato temporaneo. <br/>                                                                                                                                                                                                                                                                 |
| [**GetDefaultPrinter**](getdefaultprinter.md)<br/>             | La funzione [**GetDefaultPrinter**](/windows/desktop/printdocs/getdefaultprinter) Recupera il nome della stampante predefinita per l'utente corrente nel computer locale. <br/>                                                                                                                                                                                                                                    |
| [**GetPrinter**](getprinter.md)<br/>                           | La funzione [**GetPrinter**](/windows/desktop/printdocs/getprinter) recupera le informazioni su una stampante specificata. <br/>                                                                                                                                                                                                                                                                                               |
| [**GetPrinterData**](getprinterdata.md)<br/>                   | La funzione [**GetPrinterData**](/windows/desktop/printdocs/getprinterdata) recupera i dati di configurazione per la stampante o il server di stampa specificato. <br/>                                                                                                                                                                                                                                                                |
| [**GetPrinterDataEx**](getprinterdataex.md)<br/>               | La funzione [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) recupera i dati di configurazione per la stampante o il server di stampa specificato. **GetPrinterDataEx** è in grado di recuperare i valori archiviati dalla funzione [**SetPrinterData**](setprinterdata.md) . Inoltre, **GetPrinterDataEx** può recuperare i valori archiviati con una chiave specificata dalla funzione [**SetPrinterDataEx**](setprinterdataex.md) . <br/> |
| [**IsValidDevmode**](isvaliddevmode.md)<br/>                   | La funzione [**IsValidDevmode**](isvaliddevmode.md) verifica che il contenuto di una struttura DEVMODE sia valido. <br/>                                                                                                                                                                                                                                                                           |
| [**ReadPrinter**](readprinter.md)<br/>                         | La funzione [**ReadPrinter**](/windows/desktop/printdocs/readprinter) recupera i dati dalla stampante specificata. <br/>                                                                                                                                                                                                                                                                                                   |
| [**ResetPrinter**](resetprinter.md)<br/>                       | La funzione [**ResetPrinter**](/windows/desktop/printdocs/resetprinter) specifica il tipo di dati e i valori della modalità dispositivo da usare per la stampa dei documenti inviati dalla funzione [**StartDocPrinter**](startdocprinter.md) . È possibile eseguire l'override di questi valori utilizzando la funzione [**SetJob**](setjob.md) dopo l'avvio della stampa del documento. <br/>                                                                  |
| [**SetDefaultPrinter**](setdefaultprinter.md)<br/>             | La funzione [**SetDefaultPrinter**](/windows/desktop/printdocs/setdefaultprinter) imposta il nome della stampante predefinita per l'utente corrente nel computer locale. <br/>                                                                                                                                                                                                                                         |
| [**Porta**](setport.md)<br/>                                 | La funzione [**seport**](/windows/desktop/printdocs/setport) imposta lo stato associato a una porta stampante. <br/>                                                                                                                                                                                                                                                                                                      |
| [**SetPrinter**](setprinter.md)<br/>                           | La funzione [**Seprinter**](/windows/desktop/printdocs/setprinter) imposta i dati per una stampante specificata o imposta lo stato della stampante specificata sospendendo la stampa, riprendendo la stampa o cancellando tutti i processi di stampa. <br/>                                                                                                                                                                                           |
| [**SetPrinterData**](setprinterdata.md)<br/>                   | La funzione [**SetPrinterData**](/windows/desktop/printdocs/setprinterdata) imposta i dati di configurazione per una stampante o un server di stampa. <br/>                                                                                                                                                                                                                                                                             |
| [**SetPrinterDataEx**](setprinterdataex.md)<br/>               | La funzione [**SetPrinterDataEx**](/windows/desktop/printdocs/setprinterdataex) imposta i dati di configurazione per una stampante o un server di stampa. La funzione archivia i dati di configurazione sotto la chiave del registro di sistema della stampante. <br/>                                                                                                                                                                                            |
| [**WritePrinter**](writeprinter.md)<br/>                       | La funzione [**WritePrinter**](writeprinter.md) notifica allo spooler di stampa che i dati devono essere scritti nella stampante specificata. <br/>                                                                                                                                                                                                                                                           |



 

## <a name="printer-change-notification-functions"></a>Funzioni di notifica della modifica della stampante

Queste funzioni consentono a un'applicazione di ricevere notifiche relative alle modifiche apportate allo stato di una stampante.



| Funzione                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)<br/> | La funzione [**FindClosePrinterChangeNotification**](/windows/desktop/printdocs/findcloseprinterchangenotification) chiude un oggetto notifica di modifica creato chiamando la funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . La stampante o il server di stampa associato all'oggetto notifica delle modifiche non verrà più monitorato da tale oggetto. <br/> |
| [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)<br/> | La funzione [**FindFirstPrinterChangeNotification**](/windows/desktop/printdocs/findfirstprinterchangenotification) crea un oggetto notifica di modifica e restituisce un handle per l'oggetto. È quindi possibile usare questo handle in una chiamata a una delle funzioni wait per monitorare le modifiche apportate alla stampante o al server di stampa. <br/>                                                                              |
| [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)<br/>   | La funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) recupera le informazioni sulla notifica di modifica più recente per un oggetto notifica di modifica associato a una stampante o a un server di stampa. Chiamare questa funzione quando viene soddisfatta un'operazione di attesa sull'oggetto notifica di modifica. <br/>                                           |
| [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md)<br/>                           | La funzione [**FreePrinterNotifyInfo**](/windows/desktop/printdocs/freeprinternotifyinfo) libera un buffer allocato dal sistema creato dalla funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) . <br/>                                                                                                                                                                |



 

## <a name="printer-form-functions"></a>Funzioni modulo stampante

Queste funzioni gestiscono i moduli utilizzati da una stampante.



| Funzione                                    | Descrizione                                                                                                                                    |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddForm**](addform.md)<br/>       | La funzione [**AddForm**](/windows/desktop/printdocs/addform) aggiunge un modulo all'elenco dei moduli disponibili che è possibile selezionare per la stampante specificata. <br/> |
| [**DeleteForm**](deleteform.md)<br/> | La funzione [**DeleteForm**](/windows/desktop/printdocs/deleteform) rimuove un nome di modulo dall'elenco dei form supportati. <br/>                                |
| [**EnumForms**](enumforms.md)<br/>   | La funzione [**EnumForms**](/windows/desktop/printdocs/enumforms) enumera i form supportati dalla stampante specificata. <br/>                               |
| [**GetForm**](getform.md)<br/>       | La funzione [**GetForm**](/windows/desktop/printdocs/getform) recupera le informazioni relative a un modulo specificato. <br/>                                              |
| [**Diformi**](setform.md)<br/>       | La funzione [**seform**](/windows/desktop/printdocs/setform) imposta le informazioni sul form per la stampante specificata. <br/>                                       |



 

## <a name="print-spooler-functions"></a>Funzioni spooler di stampa

Queste funzioni interagiscono con lo spooler di stampa a un livello basso.



| Funzione                                                          | Descrizione                                                                                                                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseSpoolFileHandle**](closespoolfilehandle.md)<br/>   | La funzione [**CloseSpoolFileHandle**](/windows/desktop/printdocs/closespoolfilehandle) chiude un handle a un file di spooling associato al processo di stampa attualmente inviato dall'applicazione. <br/>                    |
| [**CommitSpoolData**](commitspooldata.md)<br/>             | La funzione [**CommitSpoolData**](/windows/desktop/printdocs/commitspooldata) notifica allo spooler di stampa che una quantità specificata di dati è stata scritta in un file di spool specificato ed è pronta per essere sottoposta a rendering. <br/> |
| [**GetPrintExecutionData**](getprintexecutiondata.md)<br/> | [**GetPrintExecutionData**](getprintexecutiondata.md) Recupera il contesto di stampa corrente.<br/>                                                                                             |
| [**GetSpoolFileHandle**](getspoolfilehandle.md)<br/>       | La funzione [**GetSpoolFileHandle**](/windows/desktop/printdocs/getspoolfilehandle) recupera un handle per il file di spooling associato al processo attualmente inviato dall'applicazione. <br/>                        |



 

 

