---
description: Windows Gli eventi consentono alle applicazioni e al sistema operativo di registrare eventi software e hardware importanti in modo centralizzato.
ms.assetid: 1f28cbce-b759-4293-8af2-15f86f23228c
title: Registrazione eventi (Windows programma di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c1aa4808727a220ec104cb3e7bfdff2741dcb2366ca1468288a082baab813b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636925"
---
# <a name="event-logging-windows-installer"></a>Registrazione eventi (Windows programma di installazione)

[Windows eventi offre](../events/windows-events.md) una modalità standard e centralizzata per le applicazioni (e il sistema operativo) per registrare eventi software e hardware importanti. Il servizio di registrazione eventi archivia gli eventi provenienti da diverse origini in un'unica raccolta denominata *registro eventi*. Prima di Windows Vista, è necessario usare [Event Tracing for Windows](../etw/event-tracing-portal.md) (ETW) o Registrazione [eventi](../eventlog/event-logging.md) per registrare gli eventi. Windows Vista ha introdotto un nuovo modello di gestione degli eventi che unifica sia ETW che [l Windows aPI del registro](../wes/windows-event-log.md) eventi.

Il programma di installazione scrive anche le voci nel registro eventi. Questi registrano eventi come i seguenti:

-   Esito positivo o negativo dell'installazione; rimozione o riparazione di un prodotto.
-   Errori che si verificano durante la configurazione del prodotto.
-   Rilevamento di dati di configurazione danneggiati.

Se viene scritta una grande quantità di informazioni, il file di registro eventi può diventare pieno e il programma di installazione visualizza il messaggio "Il file di log dell'applicazione è pieno".

Il programma di installazione può scrivere le voci seguenti nel registro eventi. Tutti i messaggi del registro eventi hanno un ID evento univoco. Tutti gli errori generali [](error-table.md) creati nella tabella Degli errori restituiti per un'installazione non riuscita vengono registrati nel registro eventi dell'applicazione con un ID messaggio uguale a Errore + 10.000. Ad esempio, il numero di errore nella tabella Errori per un'installazione completata correttamente è 1707. La corretta installazione viene registrata nel registro eventi dell'applicazione con ID messaggio 11707 (1707 + 10.000).

Per informazioni su come abilitare la registrazione dettagliata nel computer di un utente durante la risoluzione dei problemi di distribuzione, vedere Windows procedure consigliate per il programma [di installazione](windows-installer-best-practices.md)di .



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
<td>Rilevamento del prodotto '%1', funzionalità '%2' non riuscita durante la richiesta del componente '%3'</td>
<td>Messaggio di avviso. Per informazioni dettagliate, <a href="searching-for-a-broken-feature-or-component.md">vedere Ricerca di una funzionalità o di un componente interrotto.</a></td>
</tr>
<tr class="even">
<td>1002</td>
<td>Valore imprevisto o mancante (nome: '%1', valore: '%2') nella chiave '%3'</td>
<td>Messaggio di errore che indica che si è verificato un valore imprevisto o mancante.</td>
</tr>
<tr class="odd">
<td>1003</td>
<td>Sottochiave '%1' imprevista o mancante nella chiave '%2'</td>
<td>Messaggio di errore che indica che si è verificata una sottochiave imprevista o mancante.</td>
</tr>
<tr class="even">
<td>1004</td>
<td>Rilevamento del prodotto '%1', funzionalità '%2', componente '%3' non <strong>riuscito Nota:</strong> a partire da Windows Installer versione 2.0, questo messaggio è: Rilevamento del prodotto '%1', funzionalità '%2', componente '%3' non riuscito. La risorsa '%4' non esiste.<br/></td>
<td>Messaggio di avviso. Vedere anche <a href="searching-for-a-broken-feature-or-component.md">Ricerca di una funzionalità o di un componente interrotto.</a></td>
</tr>
<tr class="odd">
<td>1005</td>
<td>L'operazione di installazione ha avviato un riavvio</td>
<td>Messaggio informativo che indica che l'installazione ha avviato un riavvio del sistema.</td>
</tr>
<tr class="even">
<td>1006</td>
<td>Impossibile verificare la firma digitale per l'archivio '%1'. WinVerifyTrust non è disponibile nel computer.</td>
<td>Messaggio di avviso. Nella tabella <a href="msidigitalsignature-table.md">MsiDigitalSignature</a> è stato creato un file CAB per eseguire un controllo <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust"><strong>WinVerifyTrust.</strong></a> Non è stato possibile eseguire questa azione perché nel computer non sono installate le DLL di crittografia appropriate.</td>
</tr>
<tr class="odd">
<td>1007</td>
<td>L'installazione di %1 non è consentita dai criteri di restrizione software. Il Windows installer consente solo l'esecuzione di elementi senza restrizioni. Il livello di autorizzazione restituito dai criteri di restrizione software era %2.</td>
<td>Messaggio di errore che indica che l'amministratore ha configurato criteri di restrizione software per non consentire l'installazione.</td>
</tr>
<tr class="even">
<td>1008</td>
<td>L'installazione di %1 non è consentita a causa di un errore nell'elaborazione dei criteri di restrizione software. L'oggetto non può essere considerato attendibile.</td>
<td>Messaggio di errore che indica che si sono verificato problemi durante il tentativo di verificare il pacchetto in base ai criteri di restrizione software.</td>
</tr>
<tr class="odd">
<td>1012</td>
<td>Questa versione di Windows non supporta la distribuzione di pacchetti a 64 bit. Lo script '%1' è per un pacchetto a 64 bit.</td>
<td>Messaggio di errore che indica che gli script per i pacchetti a 64 bit possono essere eseguiti solo in un computer a 64 bit.</td>
</tr>
<tr class="even">
<td>1013</td>
<td>{Report eccezioni non gestite}</td>
<td>Messaggio di errore per un'eccezione non gestita. Questo è il report.</td>
</tr>
<tr class="odd">
<td>1014</td>
<td>Windows Le informazioni sul proxy del programma di installazione non sono registrate correttamente</td>
<td>Messaggio di errore che indica che le informazioni sul proxy non sono registrate correttamente.</td>
</tr>
<tr class="even">
<td>1015</td>
<td>Impossibile connettersi al server. Errore: %d</td>
<td>Messaggio informativo che indica che l'installazione non è riuscita a connettersi al server.</td>
</tr>
<tr class="odd">
<td>1016</td>
<td>Rilevamento del prodotto '%1', funzionalità '%2', componente '%3' non riuscito. Impossibile trovare la risorsa '%4' in un componente di esecuzione dall'origine perché non è stata trovata alcuna origine valida e accessibile.</td>
<td>Messaggio di avviso. Per altre informazioni, vedere <a href="searching-for-a-broken-feature-or-component.md">Ricerca di una funzionalità o di un componente interrotto.</a></td>
</tr>
<tr class="even">
<td>1017</td>
<td>Il SID dell'utente è stato modificato da '%1' a '%2', ma non è possibile aggiornare l'app gestita e le chiavi dati utente. Errore = '%3'.</td>
<td>Messaggio di errore che indica che si è verificato un errore durante il tentativo di aggiornare la registrazione dell'utente dopo la modifica del SID dell'utente.</td>
</tr>
<tr class="odd">
<td>1018</td>
<td>Impossibile installare l'applicazione '%1' perché non è compatibile con questa versione di Windows.</td>
<td>Messaggio di errore che indica che l'installazione non è compatibile con la versione attualmente in esecuzione di Windows. Per un aggiornamento, contattare il produttore del software installato.</td>
</tr>
<tr class="even">
<td>1019</td>
<td>Prodotto: %1 - L'aggiornamento '%2' è stato rimosso correttamente.</td>
<td>Messaggio informativo che indica che l'aggiornamento è stato rimosso dal programma di installazione. <strong>Windows Installer 2.0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1020</td>
<td>Prodotto: %1 - Impossibile rimuovere l'aggiornamento '%2'. Codice di errore %3. Informazioni aggiuntive sono disponibili nel file di log %4.</td>
<td>Messaggio di errore che indica che il programma di installazione non è riuscito a rimuovere l'aggiornamento. Altre informazioni sono disponibili nel file di log. <strong>Windows Installer 2.0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1021</td>
<td>Prodotto: %1 - Impossibile rimuovere l'aggiornamento '%2'. Codice di errore %3.</td>
<td>Messaggio di errore che indica che il programma di installazione non è riuscito a rimuovere l'aggiornamento. Per informazioni su come attivare la registrazione, vedere Abilitare la registrazione dettagliata nel <a href="windows-installer-best-practices.md">computer dell'utente</a> durante la risoluzione dei problemi di distribuzione. <strong>Windows Installer 2.0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1022</td>
<td>Prodotto: %1 - L'aggiornamento '%2' è stato installato correttamente.</td>
<td>Messaggio informativo che indica che l'aggiornamento è stato installato correttamente dal programma di installazione. <strong>Windows Installer 2.0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1023</td>
<td>Prodotto: %1 : impossibile installare l'aggiornamento '%2'. Codice errore %3. Altre informazioni sono disponibili nel file di log %4.</td>
<td>Messaggio di errore che indica che il programma di installazione non è stato in grado di installare l'aggiornamento. Altre informazioni sono disponibili nel file di log. <strong>Windows Installer 2.0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1024</td>
<td>Prodotto: %1 : impossibile installare l'aggiornamento '%2'. Codice errore %3.</td>
<td>Messaggio di errore che indica che il programma di installazione non è stato in grado di installare l'aggiornamento. Per informazioni su come attivare l'accesso, vedere Abilitare la registrazione dettagliata nel <a href="windows-installer-best-practices.md">computer dell'utente</a> durante la risoluzione dei problemi relativi alla distribuzione. <strong>Windows Installer 2.0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1025</td>
<td>Prodotto: %1. Il file %2 viene usato dal processo seguente: Nome: %3, ID %4.</td>
<td><strong>Windows Installer 2.0:</strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1026</td>
<td>Windows Il programma di installazione ha determinato che la chiave del Registro di sistema relativa ai dati di configurazione non è stata protetta correttamente. Il proprietario della chiave deve essere Sistema locale o Builtin\Administrators. La chiave esistente verrà eliminata e ri-creata con le impostazioni di sicurezza appropriate.</td>
<td>Messaggio di avviso. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1027</td>
<td>Windows Il programma di installazione ha determinato che una chiave secondaria del Registro di sistema %1 all'interno dei dati di configurazione non è stata protetta correttamente. Il proprietario della chiave deve essere Sistema locale o Builtin\Administrators. La chiave secondaria esistente e tutto il relativo contenuto verranno eliminati.</td>
<td>Messaggio di avviso. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1028</td>
<td>Windows Il programma di installazione ha determinato che la cartella della cache dei dati di configurazione non è stata protetta correttamente. Il proprietario della chiave deve essere Sistema locale o Builtin\Administrators. La cartella esistente verrà eliminata e ri-creata con le impostazioni di sicurezza appropriate.</td>
<td>Messaggio di<strong><a href="not-supported-in-windows-installer-version-3-1.md">avviso Windows installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1029</td>
<td>Prodotto: %1. Riavvio necessario.</td>
<td>Messaggio di avviso che indica che è necessario un riavvio del sistema per completare l'installazione e che il riavvio è stato posticipato in un secondo momento. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1030</td>
<td>Prodotto: %1. L'applicazione ha provato a installare una versione più recente del file Windows protetto %2. Potrebbe essere necessario aggiornare il sistema operativo per il corretto funzionamento dell'applicazione. (Versione pacchetto: %3, Versione protetta del sistema operativo: %4).</td>
<td>Messaggio di avviso che indica che l'installazione ha tentato di sostituire un file critico protetto da Windows <a href="windows-resource-protection-on-windows-vista.md">Resource Protection.</a> Per usare questa applicazione potrebbe essere necessario un aggiornamento del sistema operativo. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1031</td>
<td>Prodotto: %1. L'assembly '%2' per il componente '%3' è in uso.</td>
<td>Messaggio di avviso che indica che l'installazione ha tentato di aggiornare un assembly attualmente in uso. Il sistema deve essere riavviato per completare l'aggiornamento di questo assembly. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1032</td>
<td>Si è verificato un errore durante l'aggiornamento delle variabili di ambiente aggiornate durante l'installazione di '%1'.</td>
<td>Messaggio di avviso che indica che alcuni utenti connessi al computer potrebbero dover disconnettersi e accedere di nuovo per completare l'aggiornamento delle variabili di ambiente. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1033</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. Installazione completata con stato: %4. Produttore: %5.</td>
<td>Campo 1 - <a href="productname.md"><strong>Campo ProductName</strong></a> 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3 - <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/> Campo 5 - <a href="manufacturer.md"> <strong>Produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 e versioni precedenti:</a></strong> Campo 5 non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1034</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. Rimozione completata con stato: %4. Produttore: %5.</td>
<td>Campo 1 - <a href="productname.md"><strong>Campo ProductName</strong></a> 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3 - <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/> Campo 5 - <a href="manufacturer.md"> <strong>Produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 e versioni precedenti:</a></strong> Campo 5 non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1035</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. Modifica della configurazione completata con stato: %4. Produttore: %5.</td>
<td>Campo 1 - <a href="productname.md"><strong>Campo ProductName</strong></a> 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3 - <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 5 - <a href="manufacturer.md"> <strong>Produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 e versioni precedenti:</a></strong> Campo 5 non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1036</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. Aggiornamento: %4. Installazione dell'aggiornamento completata con stato: %5. Produttore: %6.</td>
<td>Campo 1 - <a href="productname.md"><strong>Campo ProductName</strong></a> 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3 - <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 4: nome descrittivo se la tabella <a href="msipatchmetadata-table.md">MsiPatchMetadata</a> è presente nel pacchetto di patch. In caso contrario, si tratta del GUID del codice patch della patch.<br/> Campo 5: stato dell'installazione dell'aggiornamento.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/> Campo 6 - <a href="manufacturer.md"> <strong>Produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 e versioni precedenti:</a></strong> Campo 6 non disponibile.<br/></td>
</tr>
<tr class="even">
<td>1037</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. Aggiornamento: %4. Rimozione dell'aggiornamento completata con stato: %5. Produttore: %6.</td>
<td>Campo 1 - <a href="productname.md"><strong>Campo ProductName</strong></a> 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3 - <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 4: nome descrittivo se la tabella <a href="msipatchmetadata-table.md">MsiPatchMetadata</a> è presente nel pacchetto di patch. In caso contrario, si tratta del GUID del codice patch della patch.<br/> Campo 5: stato della rimozione degli aggiornamenti.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/> Campo 6 - <a href="manufacturer.md"> <strong>Produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 e versioni precedenti:</a></strong> Campo 6 non disponibile.<br/></td>
</tr>
<tr class="odd">
<td>1038</td>
<td>Prodotto: %1. Versione: %2. Lingua: %3. Riavvio richiesto. Tipo di riavvio: %4. Motivo riavvio: %5. Produttore: %6.</td>
<td>Campo 1 - <a href="productname.md"><strong>Campo ProductName</strong></a> 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3 - <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <dl> Campo 4: costante che indica il tipo di riavvio: <br/> <dl> <strong>msirbRebootImmediate</strong> (1): è stato subito riavviato il computer.<br />
<strong>msirbRebootDeferred</strong> (2): un utente o un amministratore ha posticipato un riavvio necessario del computer usando l'interfaccia utente o <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress.<br />
</dl> </dd> Field 5 - A constant indicating the reason for the restart:<br/> <dl> <strong>msirbRebootUndeterminedReason</strong> (0): riavvio necessario per un motivo non specificato.<br />
<strong>msirbRebootInUseFilesReason</strong> (1): è stato necessario un riavvio per sostituire i file in uso.<br />
<strong>msirbRebootScheduleRebootReason</strong> (2): il pacchetto contiene <a href="schedulereboot-action.md">un'azione ScheduleReboot.</a><br />
<strong>msirbRebootForceRebootReason</strong> (3) - Il pacchetto contiene <a href="forcereboot-action.md">un'azione ForceReboot.</a><br />
<strong>msirbRebootCustomActionReason</strong> (4): azione personalizzata denominata <a href="/windows/desktop/api/Msiquery/nf-msiquery-msisetmode"><strong>funzione MsiSetMode.</strong></a><br />
</dl> </dd> </dl> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 e versioni precedenti:</a></strong> Non disponibile.<br/> Campo 6 - <a href="manufacturer.md"> <strong>Produttore</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 e versioni precedenti:</a></strong> Campo 6 non disponibile.<br/></td>
</tr>
<tr class="even">
<td>10005</td>
<td>Il programma di installazione ha rilevato un errore imprevisto durante l'installazione del pacchetto. L'errore può essere dovuto a problemi del pacchetto. Il codice di errore è [1]. {{Gli argomenti sono: [2], [3], [4]}}</td>
<td>Messaggio di errore che indica che si è verificato un errore interno. Il testo di questo messaggio è basato sul testo creato per l'errore 5 nella tabella Errore.</td>
</tr>
<tr class="odd">
<td>11707</td>
<td>Prodotto [2] - L'operazione di installazione è stata completata correttamente</td>
<td>Messaggio informativo che indica che l'installazione del prodotto è stata completata correttamente.</td>
</tr>
<tr class="even">
<td>11708</td>
<td>Prodotto [2] - Operazione di installazione non riuscita</td>
<td>Messaggio di errore che indica che l'installazione del prodotto non è riuscita.</td>
</tr>
<tr class="odd">
<td>11728</td>
<td>Prodotto [2] -- Configurazione completata.</td>
<td>Messaggio informativo che indica che la configurazione del prodotto è riuscita.</td>
</tr>
</tbody>
</table>



 

È possibile importare stringhe di errori localizzate per gli eventi nel database usando Msidb.exe [**o MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). L'SDK include stringhe di risorse localizzate per ognuna delle lingue elencate nella sezione Localizzazione delle tabelle [Error e ActionText.](localizing-the-error-and-actiontext-tables.md) Se le stringhe di errore corrispondenti agli eventi non vengono popolate, il programma di installazione carica le stringhe localizzate per la lingua specificata dalla [**proprietà ProductLanguage.**](productlanguage.md)

 

 
