---
description: Gli eventi di Windows forniscono un metodo standard e centralizzato per le applicazioni (e il sistema operativo) per registrare eventi software e hardware importanti.
ms.assetid: 1f28cbce-b759-4293-8af2-15f86f23228c
title: Registrazione eventi (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7fdaf29ec0c638d3c85b82c74cca2bbede63c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755631"
---
# <a name="event-logging-windows-installer"></a>Registrazione eventi (Windows Installer)

[Gli eventi di Windows](../events/windows-events.md) forniscono un metodo standard e centralizzato per le applicazioni (e il sistema operativo) per registrare eventi software e hardware importanti. Il servizio di registrazione eventi archivia gli eventi da diverse origini in una singola raccolta denominata *log eventi*. Prima di Windows Vista, è possibile utilizzare [Event Tracing for Windows](../etw/event-tracing-portal.md) (ETW) o la [registrazione](../eventlog/event-logging.md) degli eventi per registrare gli eventi. In Windows Vista è stato introdotto un nuovo modello di eventi che unifica sia ETW che l'API [registro eventi di Windows](../wes/windows-event-log.md) .

Il programma di installazione scrive anche le voci nel registro eventi. Questi eventi registrano gli eventi seguenti:

-   Esito positivo o negativo dell'installazione; rimozione o ripristino di un prodotto.
-   Errori che si verificano durante la configurazione del prodotto.
-   Rilevamento dei dati di configurazione danneggiati.

Se viene scritta una grande quantità di informazioni, il file di registro eventi può essere pieno e il programma di installazione visualizzerà il messaggio "il file di registro dell'applicazione è pieno".

Il programma di installazione può scrivere le voci seguenti nel registro eventi. Tutti i messaggi del registro eventi hanno un ID evento univoco. Tutti gli errori generali creati nella [tabella degli errori](error-table.md) restituiti per un'installazione che non riesce vengono registrati nel registro eventi dell'applicazione con un ID messaggio uguale all'errore + 10.000. Ad esempio, il numero di errore nella tabella degli errori per un'installazione completata è 1707. L'installazione riuscita viene registrata nel registro eventi dell'applicazione con ID messaggio 11707 (1707 + 10.000).

Per informazioni su come abilitare la registrazione dettagliata nel computer di un utente durante la risoluzione dei problemi di distribuzione, vedere [Windows Installer procedure consigliate](windows-installer-best-practices.md).



<table>
<thead>
<tr class="header">
<th>ID evento</th>
<th>Message</th>
<th>Commenti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1001</td>
<td>Rilevamento del prodotto ' %1', funzionalità' %2' non riuscita durante la richiesta del componente ' %3'</td>
<td>Messaggio di avviso. Per informazioni dettagliate, vedere <a href="searching-for-a-broken-feature-or-component.md">ricerca di una funzionalità o di un componente danneggiato</a>.</td>
</tr>
<tr class="even">
<td>1002</td>
<td>Valore imprevisto o mancante (nome:' %1', valore:' %2') nella chiave ' %3'</td>
<td>Messaggio di errore relativo a un valore imprevisto o mancante.</td>
</tr>
<tr class="odd">
<td>1003</td>
<td>Sottochiave ' %1' non prevista o mancante nella chiave ' %2'</td>
<td>Messaggio di errore che contiene una sottochiave imprevista o mancante.</td>
</tr>
<tr class="even">
<td>1004</td>
<td>Rilevamento del prodotto ' %1', funzionalità' %2', componente ' %3' non riuscita. <strong>Nota:</strong> a partire da Windows Installer versione 2,0, questo messaggio è: rilevamento del prodotto ' %1', funzionalità' %2', componente ' %3' non riuscita. La risorsa ' %4' non esiste.<br/></td>
<td>Messaggio di avviso. Vedere anche <a href="searching-for-a-broken-feature-or-component.md">ricerca di una funzionalità o di un componente danneggiato</a>.</td>
</tr>
<tr class="odd">
<td>1005</td>
<td>Operazione di installazione avviata un riavvio</td>
<td>Messaggio informativo che l'installazione ha avviato un riavvio del sistema.</td>
</tr>
<tr class="even">
<td>1006</td>
<td>Impossibile eseguire la verifica della firma digitale per il file CAB ' %1'. WinVerifyTrust non è disponibile nel computer.</td>
<td>Messaggio di avviso. È stato creato un file CAB nella <a href="msidigitalsignature-table.md">tabella MsiDigitalSignature</a> per eseguire un controllo <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust"><strong>WinVerifyTrust</strong></a> . Non è stato possibile eseguire l'azione perché nel computer non sono installate le DLL di crittografia appropriate.</td>
</tr>
<tr class="odd">
<td>1007</td>
<td>L'installazione di %1 non è consentita dai criteri di restrizione software. Il Windows Installer consente solo l'esecuzione di elementi senza restrizioni. Il livello di autorizzazione restituito dai criteri di restrizione software era %2.</td>
<td>Messaggio di errore che indica che l'amministratore ha configurato i criteri di restrizione software per impedire questa installazione.</td>
</tr>
<tr class="even">
<td>1008</td>
<td>L'installazione di %1 non è consentita a causa di un errore nell'elaborazione dei criteri di restrizione software. L'oggetto non può essere considerato attendibile.</td>
<td>Messaggio di errore che indica che si sono verificati problemi durante il tentativo di verificare il pacchetto in base ai criteri di restrizione software.</td>
</tr>
<tr class="odd">
<td>1012</td>
<td>Questa versione di Windows non supporta la distribuzione di pacchetti a 64 bit. Lo script ' %1' è per un pacchetto a 64 bit.</td>
<td>Messaggio di errore che indica che gli script per i pacchetti a 64 bit possono essere eseguiti solo in un computer a 64 bit.</td>
</tr>
<tr class="even">
<td>1013</td>
<td>{Report eccezioni non gestite}</td>
<td>Messaggio di errore per un'eccezione non gestita. si tratta del report.</td>
</tr>
<tr class="odd">
<td>1014</td>
<td>Windows Installer le informazioni sul proxy non sono registrate correttamente</td>
<td>Messaggio di errore che segnala che le informazioni sul proxy non sono state registrate correttamente.</td>
</tr>
<tr class="even">
<td>1015</td>
<td>Non è stato possibile connettersi al server. Errore:% d</td>
<td>Messaggio informativo che l'installazione non è riuscita a connettersi al server.</td>
</tr>
<tr class="odd">
<td>1016</td>
<td>Rilevamento del prodotto ' %1', funzionalità' %2', componente ' %3' non riuscito. Impossibile individuare la risorsa ' %4' in un componente run-from-source perché non è stata trovata alcuna origine valida e accessibile.</td>
<td>Messaggio di avviso. Per ulteriori informazioni, vedere <a href="searching-for-a-broken-feature-or-component.md">ricerca di una funzionalità o di un componente danneggiato</a>.</td>
</tr>
<tr class="even">
<td>1017</td>
<td>Il SID utente è stato modificato da' %1' a' %2', ma non è possibile aggiornare l'app gestita e le chiavi di dati utente. Errore =' %3'.</td>
<td>Messaggio di errore che indica che si è verificato un errore durante il tentativo di aggiornare la registrazione dell'utente dopo la modifica del SID dell'utente.</td>
</tr>
<tr class="odd">
<td>1018</td>
<td>Impossibile installare l'applicazione ' %1' perché non è compatibile con questa versione di Windows.</td>
<td>Messaggio di errore che indica che l'installazione non è compatibile con la versione di Windows attualmente in esecuzione. Contattare il produttore del software da installare per un aggiornamento.</td>
</tr>
<tr class="even">
<td>1019</td>
<td>Prodotto: %1-l'aggiornamento ' %2' è stato rimosso.</td>
<td>Messaggio informativo che l'aggiornamento è stato rimosso dal programma di installazione. <strong>Windows Installer 2,0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1020</td>
<td>Prodotto: %1-Impossibile rimuovere l'aggiornamento ' %2'. Codice errore %3. Nel file di log %4 sono disponibili informazioni aggiuntive.</td>
<td>Messaggio di errore che indica che il programma di installazione non è stato in grado di rimuovere l'aggiornamento. Nel file di log sono disponibili informazioni aggiuntive. <strong>Windows Installer 2,0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1021</td>
<td>Prodotto: %1-Impossibile rimuovere l'aggiornamento ' %2'. Codice errore %3.</td>
<td>Messaggio di errore che indica che il programma di installazione non è stato in grado di rimuovere l'aggiornamento. Per informazioni su come attivare la registrazione, vedere <a href="windows-installer-best-practices.md">abilitare la registrazione dettagliata nel computer dell'utente durante la risoluzione dei problemi di distribuzione.</a> <strong>Windows Installer 2,0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1022</td>
<td>Prodotto: %1-aggiornamento di ' %2' completato.</td>
<td>Messaggio informativo in cui l'aggiornamento è stato installato correttamente dal programma di installazione. <strong>Windows Installer 2,0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1023</td>
<td>Prodotto: %1-Impossibile installare l'aggiornamento ' %2'. Codice errore %3. Nel file di log %4 sono disponibili informazioni aggiuntive.</td>
<td>Messaggio di errore che indica che il programma di installazione non è riuscito a installare l'aggiornamento. Nel file di log sono disponibili informazioni aggiuntive. <strong>Windows Installer 2,0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1024</td>
<td>Prodotto: %1-Impossibile installare l'aggiornamento ' %2'. Codice errore %3.</td>
<td>Messaggio di errore che indica che il programma di installazione non è riuscito a installare l'aggiornamento. Per informazioni su come attivare la registrazione, vedere <a href="windows-installer-best-practices.md">abilitare la registrazione dettagliata nel computer dell'utente durante la risoluzione dei problemi di distribuzione.</a> <strong>Windows Installer 2,0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1025</td>
<td>Prodotto: %1. Il file %2 è usato dal processo seguente: Nome: %3, ID %4.</td>
<td><strong>Windows Installer 2,0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1026</td>
<td>Windows Installer ha determinato che la chiave del registro di sistema dei dati di configurazione non è stata protetta correttamente. Il proprietario della chiave deve essere Local System o Builtin\Administrators. La chiave esistente verrà eliminata e ricreata con le impostazioni di sicurezza appropriate.</td>
<td>Messaggio di avviso. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e versioni precedenti</a>:</strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1027</td>
<td>Windows Installer ha determinato che una chiave secondaria del registro di sistema %1 all'interno dei relativi dati di configurazione non è stata protetta correttamente. Il proprietario della chiave deve essere Local System o Builtin\Administrators. La chiave secondaria esistente e tutto il relativo contenuto verranno eliminati.</td>
<td>Messaggio di avviso. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e versioni precedenti</a>:</strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1028</td>
<td>Windows Installer ha determinato che la cartella della cache dei dati di configurazione non è stata protetta correttamente. Il proprietario della chiave deve essere Local System o Builtin\Administrators. La cartella esistente verrà eliminata e ricreata con le impostazioni di sicurezza appropriate.</td>
<td>Messaggio<strong><a href="not-supported-in-windows-installer-version-3-1.md">di avviso Windows Installer 3,1 e versioni precedenti</a>:</strong> non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1029</td>
<td>Prodotto: %1. Riavvio obbligatorio.</td>
<td>Messaggio di avviso indicatiing che è necessario riavviare il sistema per completare l'installazione e il riavvio è stato posticipato a un momento successivo. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e versioni precedenti</a>:</strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1030</td>
<td>Prodotto: %1. L'applicazione ha tentato di installare una versione più recente del file di Windows protetto %2. Per il corretto funzionamento di questa applicazione, potrebbe essere necessario aggiornare il sistema operativo. (Versione pacchetto: %3, versione protetta del sistema operativo: %4).</td>
<td>Messaggio di avviso che indica che l'installazione ha tentato di sostituire un file critico protetto da <a href="windows-resource-protection-on-windows-vista.md">Protezione risorse di Windows</a>. Per utilizzare questa applicazione, potrebbe essere necessario un aggiornamento del sistema operativo. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e versioni precedenti</a>:</strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1031</td>
<td>Prodotto: %1. L'assembly ' %2' per il componente ' %3' è in uso.</td>
<td>Messaggio di avviso che indica che l'installazione ha tentato di aggiornare un assembly attualmente in uso. Il sistema deve essere riavviato per completare l'aggiornamento di questo assembly. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e versioni precedenti</a>:</strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1032</td>
<td>Si è verificato un errore durante l'aggiornamento delle variabili di ambiente aggiornate durante l'installazione di ' %1'.</td>
<td>Messaggio di avviso che indica che alcuni utenti che sono connessi al computer potrebbero dover disconnettersi e tornare indietro per completare l'aggiornamento delle variabili di ambiente. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e versioni precedenti</a>:</strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1033</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. L'installazione è stata completata con stato: %4. Produttore: %5.</td>
<td>Campo 1-campo <a href="productname.md"><strong>ProductName</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e versioni precedenti</a>:</strong> Non disponibile.<br/> Campo 5- <a href="manufacturer.md"> <strong>produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 e versioni precedenti</a>:</strong> Il campo 5 non è disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1034</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. Rimozione completata con stato: %4. Produttore: %5.</td>
<td>Campo 1-campo <a href="productname.md"><strong>ProductName</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e versioni precedenti</a>:</strong> Non disponibile.<br/> Campo 5- <a href="manufacturer.md"> <strong>produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 e versioni precedenti</a>:</strong> Il campo 5 non è disponibile.<br/></td>
</tr>
<tr class="even">
<td>1035</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. Modifica della configurazione completata con stato: %4. Produttore: %5.</td>
<td>Campo 1-campo <a href="productname.md"><strong>ProductName</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 5- <a href="manufacturer.md"> <strong>produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 e versioni precedenti</a>:</strong> Il campo 5 non è disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1036</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. Aggiornamento: %4. L'installazione dell'aggiornamento è stata completata con stato: %5. Produttore: %6.</td>
<td>Campo 1-campo <a href="productname.md"><strong>ProductName</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Field 4: nome descrittivo dell'utente se la <a href="msipatchmetadata-table.md">tabella MsiPatchMetadata</a> è presente nel pacchetto di patch. In caso contrario, si tratta del GUID del codice patch della patch.<br/> Field 5: stato dell'installazione dell'aggiornamento.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e versioni precedenti</a>:</strong> Non disponibile.<br/> Campo 6- <a href="manufacturer.md"> <strong>produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 e versioni precedenti</a>:</strong> Il campo 6 non è disponibile.<br/></td>
</tr>
<tr class="even">
<td>1037</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. Aggiornamento: %4. La rimozione dell'aggiornamento è stata completata con stato: %5. Produttore: %6.</td>
<td>Campo 1-campo <a href="productname.md"><strong>ProductName</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Field 4: nome descrittivo dell'utente se la <a href="msipatchmetadata-table.md">tabella MsiPatchMetadata</a> è presente nel pacchetto di patch. In caso contrario, si tratta del GUID del codice patch della patch.<br/> Field 5-stato della rimozione degli aggiornamenti.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e versioni precedenti</a>:</strong> Non disponibile.<br/> Campo 6- <a href="manufacturer.md"> <strong>produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 e versioni precedenti</a>:</strong> Il campo 6 non è disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1038</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. Riavvio richiesto. Tipo di riavvio: %4. Motivo riavvio: %5. Produttore: %6.</td>
<td>Campo 1-campo <a href="productname.md"><strong>ProductName</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <dl> Field 4-una costante che indica il tipo di riavvio: <br/> <dl> <strong>msirbRebootImmediate</strong> (1)-si è verificato un riavvio immediato del computer.<br />
<strong>msirbRebootDeferred</strong> (2): un utente o un amministratore ha rinviato un riavvio necessario del computer usando l'interfaccia utente o il <a href="reboot.md"><strong>riavvio</strong></a>= ReallySuppress.<br />
</dl> </dd> Field 5 - A constant indicating the reason for the restart:<br/> <dl> <strong>msirbRebootUndeterminedReason</strong> (0): il riavvio è necessario per un motivo non specificato.<br />
<strong>msirbRebootInUseFilesReason</strong> (1): è stato richiesto un riavvio per sostituire i file in uso.<br />
<strong>msirbRebootScheduleRebootReason</strong> (2): il pacchetto contiene un'azione <a href="schedulereboot-action.md">ScheduleReboot</a> .<br />
<strong>msirbRebootForceRebootReason</strong> (3): il pacchetto contiene un'azione <a href="forcereboot-action.md">ForceReboot</a> .<br />
<strong>msirbRebootCustomActionReason</strong> (4): azione personalizzata chiamata funzione <a href="/windows/desktop/api/Msiquery/nf-msiquery-msisetmode"><strong>MsiSetMode</strong></a> .<br />
</dl> </dd> </dl> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 e versioni precedenti</a>:</strong> Non disponibile.<br/> Campo 6- <a href="manufacturer.md"> <strong>produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 e versioni precedenti</a>:</strong> Il campo 6 non è disponibile.<br/></td>
</tr>
<tr class="even">
<td>10005</td>
<td>Si è verificato un errore imprevisto durante l'installazione del pacchetto. L'errore può essere dovuto a problemi del pacchetto. Il codice di errore è [1]. {{Gli argomenti sono: [2], [3], [4]}}</td>
<td>Messaggio di errore che indica che si è verificato un errore interno. Il testo di questo messaggio si basa sul testo creato per l'errore 5 nella tabella degli errori.</td>
</tr>
<tr class="odd">
<td>11707</td>
<td>Prodotto [2]: l'operazione di installazione è stata completata</td>
<td>Messaggio informativo che l'installazione del prodotto ha avuto esito positivo.</td>
</tr>
<tr class="even">
<td>11708</td>
<td>Prodotto [2] – operazione di installazione non riuscita</td>
<td>Messaggio di errore che segnala che l'installazione del prodotto non è riuscita.</td>
</tr>
<tr class="odd">
<td>11728</td>
<td>Prodotto [2]--configurazione completata correttamente.</td>
<td>Messaggio informativo che la configurazione del prodotto ha avuto esito positivo.</td>
</tr>
</tbody>
</table>



 

È possibile importare le stringhe degli errori localizzati per gli eventi nel database usando Msidb.exe o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). L'SDK include stringhe di risorse localizzate per ogni lingua elencata nella sezione [localizzazione dell'errore e delle tabelle ActionText](localizing-the-error-and-actiontext-tables.md) . Se le stringhe di errore corrispondenti agli eventi non vengono popolate, il programma di installazione carica le stringhe localizzate per la lingua specificata dalla proprietà [**ProductLanguage**](productlanguage.md) .

 

 
