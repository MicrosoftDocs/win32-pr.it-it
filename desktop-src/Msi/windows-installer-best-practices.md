---
description: "Questa sezione enumera un elenco di suggerimenti, collegati alla documentazione principale di Windows Installer SDK, per consentire agli sviluppatori di applicazioni, agli autori del programma di installazione, ai professionisti IT e agli sviluppatori di infrastruttura di individuare le procedure consigliate per l'uso del programma di installazione di Windows:"
ms.assetid: ff48d995-fe6f-4d1b-898d-67574ed3c5b7
title: Windows Procedure consigliate per il programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e430cf8871279e18107b3ab1deb1f347e9d4779b619ab6cf8133d30cdfa4ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808961"
---
# <a name="windows-installer-best-practices"></a>Windows Procedure consigliate per il programma di installazione

Questa sezione enumera un elenco di suggerimenti, collegati alla documentazione principale di Windows Installer SDK, per consentire agli sviluppatori di applicazioni, agli autori del programma di installazione, ai professionisti IT e agli sviluppatori di infrastruttura di individuare le procedure consigliate per l'uso del programma di installazione di Windows:

-   [Aggiornare la versione Windows Installer.](#update-the-windows-installer-version)
-   [Soddisfare i requisiti Windows di certificazione del logo.](#meet-the-windows-logo-certification-requirements)
-   [Preparare il pacchetto per la localizzazione.](#prepare-the-package-for-localization)
-   [Aggiornare gli strumenti Windows di sviluppo del programma di installazione e la documentazione.](#update-your-windows-installer-development-tools-and-documentation)
-   [Se si decide di creare un nuovo pacchetto di un'applicazione di configurazione legacy, seguire le procedure consigliate per la riacchettamento.](#if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices)
-   [Non provare a sostituire le risorse protette.](#do-not-try-to-replace-protected-resources)
-   [Non dipendere da risorse non critiche.](#do-not-depend-upon-non-critical-resources)
-   [Usare l'API per recuperare Windows di configurazione del programma di installazione.](#use-the-api-to-retrieve-windows-installer-configuration-information)
-   [Organizzare l'installazione dell'applicazione in base ai componenti.](#organize-the-installation-of-your-application-around-components)
-   [Ridurre le dimensioni dei pacchetti di installazione Windows di grandi dimensioni.](#reduce-the-size-of-large-windows-installer-packages)
-   [Se si usano azioni personalizzate, seguire le procedure consigliate per le azioni personalizzate.](#if-you-use-custom-actions-follow-good-custom-action-practices)
-   [Se si usano assembly, seguire le procedure consigliate per gli assembly](#if-you-use-assemblies-follow-good-assembly-practices)
-   [Non spedire installazioni simultanee.](#do-not-ship-concurrent-installations)
-   [Mantenere coerenti i nomi e i codici dei pacchetti.](#keep-package-names-and-package-codes-consistent)
-   [Non usare le tabelle SelfReg e TypeLib.](#do-not-use-the-selfreg-and-typelib-tables)
-   [Specificare l'opzione per l'installazione senza un'interfaccia utente.](#provide-the-option-to-install-without-a-user-interface)
-   [Evitare di usare i criteri AlwaysInstallElevated.](#avoid-using-the-alwaysinstallelevated-policy)
-   [Abilitare il criterio DisableMedia per limitare l'installazione non autorizzata.](#enable-the-disablemedia-policy-to-limit-unauthorized-installation)
-   [Mantenere i file di origine del pacchetto originale protetti e disponibili per gli utenti.](#keep-the-original-package-source-files-secure-and-available-to-users)
-   [Abilitare la registrazione dettagliata nel computer dell'utente durante la risoluzione dei problemi di distribuzione.](#enable-verbose-logging-on-users-computer-when-troubleshooting-deployment)
-   [La disinstallazione lascia il computer dell'utente in uno stato pulito.](#uninstallation-leaves-the-users-computer-in-a-clean-state)
-   [Testare i pacchetti per la distribuzione dell'installazione per utente e per computer.](#test-packages-for-both-per-user-and-per-machine-installation-deployment)
-   [Pianificare e testare una strategia di manutenzione prima di spedire l'applicazione.](#plan-and-test-a-servicing-strategy-before-shipping-the-application)
-   [Ridurre la dipendenza degli aggiornamenti dalle origini originali.](#reduce-the-dependency-of-updates-upon-the-original-sources)
-   [Non distribuire moduli unione inutilizzabili.](#do-not-distribute-unserviceable-merge-modules)
-   [Evitare di applicare patch alle installazioni amministrative.](#avoid-patching-administrative-installations)
-   [Registrare gli aggiornamenti per l'esecuzione con privilegi elevati.](#register-updates-to-run-with-elevated-privilege)
-   [Usare la tabella MsiPatchSequence per sequenziare le patch.](#use-the-msipatchsequence-table-to-sequence-patches)
-   [Testare accuratamente il pacchetto di installazione.](#test-the-installation-package-thoroughly)
-   [Correggere tutti gli errori di convalida prima di distribuire un pacchetto di installazione nuovo o modificato.](#fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package)
-   [Creare un'installazione sicura.](#author-a-secure-installation)
-   [Usare PMSIHANDLE anziché HANDLE](#use-pmsihandle-instead-of-handle)

## <a name="update-the-windows-installer-version"></a>Aggiornare la versione Windows Installer.

-   Usare Windows Installer 5.0 in Windows Server 2008 R2 e Windows 7. Questa è la Windows del programma di installazione fornita con il sistema operativo.
-   Usare Windows Installer 4.5 in Windows Server 2008, Windows Server 2003 con Service Pack 1 (SP1), Windows Vista con Service Pack 1 (SP1) o Windows XP con Service Pack 2 (SP2). Per informazioni su come ottenere la versione più recente Windows Installer, vedere [Windows Installer Redistributables.](windows-installer-redistributables.md)
-   Usare Windows Installer 3.1 in Windows 2000 con Service Pack 3 (SP3). Windows Nella versione 3.1 del programma di installazione sono disponibili funzionalità che semplificano la manutenzione e l'applicazione di [patch alle applicazioni.](patching.md)
-   Molte funzionalità importanti sono state introdotte con la versione 3.0 e sono elencate nella sezione Non supportato [in Windows Installer versione 2.0.](not-supported-in-windows-installer-version-2-0.md) I pacchetti di installazione e gli aggiornamenti creati per Windows Installer 2.0 possono essere installati usando Windows Installer 3.0 e versioni successive. I pacchetti patch che contengono le nuove tabelle usate da Windows Installer 3.0 possono comunque essere applicati usando le versioni precedenti del programma di installazione di Windows ma senza la funzionalità di applicazione di patch di Windows Installer 3.0. È anche possibile creare patch che richiedono in modo esplicito Windows Installer 3.0 che non può essere applicato dalle versioni precedenti di Windows Installer. Se un utente non è in grado di aggiornare la versione del programma di installazione, assicurarsi che l'applicazione o l'aggiornamento sia compatibile con un aggiornamento futuro del programma di Windows installazione.
-   Per un elenco delle funzionalità di Windows Installer non supportate dalle versioni precedenti del programma di installazione di Windows, vedere Novità del programma [di Windows.](what-s-new-in-windows-installer.md)

## <a name="meet-the-windows-logo-certification-requirements"></a>Soddisfare i requisiti Windows di certificazione del logo.

-   Anche se non si intende inviare l'applicazione al programma di logo, seguire le linee guida per la certificazione del logo può contribuire a migliorare il Windows programma di installazione. Per una panoramica dei requisiti del logo e per i collegamenti a programmi di certificazione del logo specifici, Windows requisiti del programma di installazione [e del logo.](windows-installer-and-logo-requirements.md)

## <a name="prepare-the-package-for-localization"></a>Preparare il pacchetto per la localizzazione.

-   È consigliabile prepararsi per la localizzazione futura durante la creazione del pacchetto di installazione originale. È possibile seguire la procedura di localizzazione dei pacchetti suggerita in [Localizzazione di un pacchetto Windows installer](localizing-a-windows-installer-package.md).

## <a name="update-your-windows-installer-development-tools-and-documentation"></a>Aggiornare gli strumenti Windows di sviluppo e la documentazione del programma di installazione.

-   Gli [Windows di sviluppo del](windows-installer-development-tools.md) programma di installazione non sono ridistribuibili ed è consigliabile usare solo le versioni di questi strumenti disponibili in Microsoft. Questi componenti sono disponibili in [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) in Microsoft Windows Software Development Kit (SDK).
-   Diversi fornitori di software indipendenti offrono strumenti per creare o modificare Windows di installazione. Questi strumenti possono fornire un ambiente di creazione di pacchetti che può essere più facile da usare rispetto agli strumenti forniti in Windows Installer SDK. Per altre informazioni su questi strumenti, vedere le risorse di informazioni illustrate in Altre origini di Windows [informazioni sul programma di installazione.](other-sources-of-windows-installer-information.md)
-   La possibilità di compilare un pacchetto da file di testo può essere più intuitiva per alcuni sviluppatori. Il set Windows di strumenti WiX (Installer [](https://sourceforge.net/projects/wix) XML) disponibile in Sourceforge.net compila Windows pacchetti di installazione dal codice sorgente XML.
-   La documentazione [nell'SDK Windows Installer](./windows-installer-portal.md) rilasciato in MSDN Online Library viene aggiornata con maggiore frequenza.
-   Usare la versione recente di [Msizap.exe](msizap-exe.md) (versione 3.1.4000.2726 o successiva) disponibile in [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) for Windows Vista o versione successiva. Le versioni più Msizap.exe possono rimuovere informazioni su tutti gli aggiornamenti applicati ad altre applicazioni nel computer dell'utente. Se queste informazioni vengono rimosse, potrebbe essere necessario rimuovere e reinstallare queste altre applicazioni per ricevere aggiornamenti aggiuntivi.
-   L'editor di tabelle [Orca.exe](orca-exe.md) database è un editor di tabelle di database per la creazione e la modifica di Windows di installazione e di moduli unione. Ha un'interfaccia GUI di base, ma supporta la modifica avanzata dei Windows installer. Anche se si usa un'altra applicazione come strumento di sviluppo principale, l'uso di Orca.exe risulta utile durante la risoluzione dei problemi e il test di un pacchetto.
-   Per [informazioni](other-sources-of-windows-installer-information.md) aggiornate sul programma di installazione di Windows, vedere Altre fonti di informazioni sul programma di installazione di Windows disponibili in blog, chat tecniche, newsgroup, articoli tecnici e siti Web.

## <a name="if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices"></a>Se si decide di creare un nuovo pacchetto di un'applicazione di configurazione legacy, seguire le procedure consigliate per la riacchettamento.

Molti fornitori di applicazioni forniscono pacchetti Windows installer nativi per l'installazione o i relativi prodotti. Il software che converte un'applicazione di installazione legacy esistente in un pacchetto Windows Installer è detto strumento di repackaging. Il white paper [Step-by-Step Guide to Creating Windows Installer Packages and Repackaging Software for the Windows Installer](https://www.microsoft.com/technet/prodtechnol/windows2000serv/howto/winstall.mspx) (Guida dettagliata alla creazione di pacchetti del programma di installazione di Windows e alla riacchettazione del software per il programma di installazione di Windows) descrive uno strumento di repackaging disponibile in commercio. La ricompressione di un'applicazione di installazione esistente non è la procedura consigliata per lo sviluppo. Le applicazioni progettate fin dall'inizio per sfruttare i vantaggi delle Windows Installer possono essere più semplici da installare e da usare per gli utenti. Se si decide di usare un software di repackaging, le procedure seguenti consentono di produrre un pacchetto di Windows installer migliore.

-   La decompressione degli strumenti converte le installazioni legacy in un pacchetto di Windows Installer, prendendo un'immagine di un sistema di gestione temporanea prima e dopo l'installazione. Tutte le modifiche del Registro di sistema, le modifiche ai file o le impostazioni di sistema che si verificano durante il processo di acquisizione vengono incluse nell'installazione. Configurare l'hardware e il software del computer usato per ri-creare il pacchetto dell'installazione il più vicino possibile al sistema dell'utente previsto. Creare un pacchetto separato per ogni configurazione hardware diversa. Creare un nuovo pacchetto usando un computer di gestione temporanea pulito. Rimuovere tutte le applicazioni non necessarie. Arrestare tutti i processi non necessari. Chiudere tutti i servizi di sistema non essenziali.
-   Creare sempre una copia dell'installazione originale prima di iniziare a lavorare su di essa. Usare sempre la copia. Non arrestare mai un repackager prima di terminare la compilazione del pacchetto. Se il repackager danneggia il pacchetto, sarà ancora l'originale.
-   Non creare un nuovo pacchetto di aggiornamenti software Microsoft in un pacchetto Windows Installer. Microsoft rilascia gli aggiornamenti software, ad esempio i Service Pack, come file autoestrativi che eseggono automaticamente l'installazione. Questi aggiornamenti usano programmi di installazione diversi rispetto a Windows Installer per sostituire le risorse Windows protette e non possono essere convertiti in un pacchetto Windows Installer. Per informazioni su come distribuire Windows Service Pack, vedere la guida alla distribuzione del Service Pack in [Microsoft TechNet.](https://technet.microsoft.com/)
-   Non usare uno strumento di repackaging per convertire un pacchetto Windows Installer in un nuovo pacchetto. Il Windows di installazione aggiunge informazioni di configurazione al sistema e alle risorse dell'applicazione. Quando uno strumento di repackaging confronta il sistema prima e dopo l'installazione, il repackager interpretate erroneamente le informazioni di configurazione come parte dell'applicazione. Questo danneggia in genere l'applicazione riacchetto. Usare invece [le trasformazioni di personalizzazione](a-customization-transform-example.md) per modificare un pacchetto Windows Installer esistente o creare un nuovo pacchetto. È possibile creare trasformazioni di personalizzazione usando [ loMsitran.exe](msitran-exe.md) personalizzato.
-   Non usare uno strumento di repackaging per consolidare Windows pacchetti del programma di installazione in un singolo pacchetto. È invece possibile usare lo strumento [Msistuff.exe](msistuff-exe.md) per configurare il Setup.exe bootstrap per installare i pacchetti uno dopo l'altro.
-   Creare il Windows installer in modo che possa essere facilmente personalizzato dal cliente. Le variabili globali usate dal programma di Windows durante un'installazione possono essere impostate usando proprietà [pubbliche](properties.md) o [trasformazioni di personalizzazione.](a-customization-transform-example.md) Fornire la documentazione per l'uso di tali proprietà e dei valori predefiniti pratici per tutti i valori personalizzabili. Per informazioni su come ottenere e impostare le proprietà, vedere [Uso delle proprietà](using-properties.md). Per un esempio di trasformazione di personalizzazione, vedere [A Customization Transform Example](a-customization-transform-example.md).

## <a name="do-not-try-to-replace-protected-resources"></a>Non provare a sostituire le risorse protette.

Windows I pacchetti del programma di installazione non devono tentare di sostituire le risorse protette durante l'installazione o l'aggiornamento. Il Windows installer non rimuove o sostituisce queste risorse perché Windows la sostituzione di file di sistema, cartelle e chiavi del Registro di sistema essenziali. La protezione di queste risorse impedisce errori dell'applicazione e del sistema operativo.

-   Quando viene eseguito in Windows Server 2008 o Windows Vista, il programma di installazione di Windows ignora l'installazione di qualsiasi file o chiave del Registro di sistema protetta da [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) (WRP), il programma di installazione immette un avviso nel file di log e continua con il resto dell'installazione senza errori. Per informazioni, vedere [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).
-   WRP è il nuovo nome per Windows Protezione file (WFP). WRP protegge le chiavi e le cartelle del Registro di sistema, nonché i file di sistema essenziali. In Windows Server 2003, Windows XP e Windows 2000, quando il programma di installazione di Windows rilevava un file protetto da WFP, il programma di installazione richiedeva l'installazione del file da parte del PROGRAMMA DI WINDOWS. Per informazioni, vedere [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).

## <a name="do-not-depend-upon-non-critical-resources"></a>Non dipendere da risorse non critiche.

L'installazione o l'aggiornamento non deve dipendere dall'installazione di risorse non critiche per i motivi seguenti.

-   Le azioni personalizzate possono non riuscire se dipendono da un componente appartenente a una funzionalità annunciata dall'utente anziché dall'installazione.
-   Le azioni personalizzate sequenziate prima [dell'azione InstallFinalize](installfinalize-action.md) possono avere esito negativo se dipendono da un componente contenente un assembly installato. Il Windows installer non esegue il commit degli assembly nella Global Assembly Cache (GAC) fino al completamento dell'azione InstallFinalize.

## <a name="use-the-api-to-retrieve-windows-installer-configuration-information"></a>Usare l'API per recuperare le Windows di configurazione del programma di installazione.

L'installazione dell'applicazione o dell'aggiornamento non deve dipendere dall'accesso diretto Windows informazioni di configurazione del programma di installazione salvate nel computer. Usare invece l'Windows di programmazione dell'applicazione del programma di installazione per recuperare le informazioni di configurazione. Il percorso e il formato delle informazioni di configurazione vengono gestiti dal Windows installer e possono cambiare.

-   Le funzioni di installazione e configurazione dell'API Windows Installer sono descritte in Informazioni di riferimento sulle funzioni [del programma di installazione](installer-function-reference.md).
-   Le [proprietà di configurazione](property-reference.md) sono descritte in Informazioni di riferimento sulla proprietà.
-   I metodi e le proprietà di automazione sono descritti in Informazioni di riferimento [sull'interfaccia di automazione](automation-interface-reference.md). Lo script di esempio WiLstPrd.vbs si connette a un oggetto Installer ed enumera i prodotti registrati e le informazioni sul prodotto. Per informazioni, vedere [Elencare prodotti, proprietà, funzionalità e componenti](list-products-properties-features-and-components.md).

## <a name="organize-the-installation-of-your-application-around-components"></a>Organizzare l'installazione dell'applicazione intorno ai componenti.

Il Windows installer installa o rimuove raccolte di risorse denominate [componenti](windows-installer-components.md). Poiché i componenti sono comunemente condivisi, l'autore di un pacchetto di installazione deve seguire le regole quando si specificano i componenti di una funzionalità o di un'applicazione.

-   Rispettare le regole [](organizing-applications-into-components.md) dei componenti quando si organizzano le applicazioni in componenti per garantire che i nuovi componenti o le nuove versioni dei componenti possano essere installati e rimossi senza danneggiare altre applicazioni. È possibile seguire la procedura descritta in [Definizione dei componenti del programma di installazione](defining-installer-components.md).
-   Il programma di installazione tiene traccia di ogni componente in base al RISPETTIVO GUID ID componente specificato nella [tabella Componente](component-table.md). Per il funzionamento del meccanismo di conteggio dei Windows installer è essenziale che il GUID dell'ID componente sia corretto. Seguire le linee guida in [Modifica del codice del componente](changing-the-component-code.md).
-   Se il pacchetto deve interrompere le regole dei componenti, tenere presenti le possibili conseguenze e assicurarsi che l'installazione non installi mai questi componenti in cui potrebbero danneggiare i componenti nel sistema dell'utente. Per informazioni, [vedere Cosa accade se le regole del componente vengono interrotte?](what-happens-if-the-component-rules-are-broken.md).
-   Tenere presente in che modo il Windows installer applica le regole [di controllo delle versioni dei file](file-versioning-rules.md) quando si [sostituiscono i file esistenti.](replacing-existing-files.md) Il Windows installer determina innanzitutto se il file di chiave del componente è già installato prima di provare a installare uno dei file del componente. Se il programma di installazione trova un file con lo stesso nome del file di chiave del componente installato nel percorso di destinazione, confronta la versione, la data e la lingua dei due file chiave e usa le regole di controllo delle versioni dei file per determinare se installare il componente fornito dal pacchetto. Se il programma di installazione determina che deve sostituire la base del componente sul file di chiave, usa le regole di controllo delle versioni dei file in ogni file installato per determinare se sostituire il file.

## <a name="reduce-the-size-of-large-windows-installer-packages"></a>Ridurre le dimensioni dei pacchetti di installazione Windows di grandi dimensioni.

I pacchetti Windows molto grandi accettano le risorse di sistema e possono essere difficili da installare per gli utenti. È consigliabile ridurre le dimensioni dei pacchetti di installazione Windows pacchetti del programma di installazione con i metodi seguenti.

-   Comprimere i file nell'installazione e archiviarli in un file cab (.cab). Il programma di installazione consente .cab file da archiviare come file esterno separato o come flusso di dati nel pacchetto MSI stesso. Per informazioni, vedere [Uso di archivi e origini compresse.](using-cabinets-and-compressed-sources.md)
-   Rimuovere lo spazio di archiviazione sprecato nel file .msi usando una delle opzioni descritte in Riduzione delle dimensioni di un .msi [file](reducing-the-size-of-an--msi-file.md).
-   Se il Windows installer contiene più di 32767 file, è necessario modificare lo schema del database. Per informazioni, vedere [Creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md).

## <a name="if-you-use-custom-actions-follow-good-custom-action-practices"></a>Se si usano azioni personalizzate, seguire le procedure consigliate per le azioni personalizzate.

Il Windows installer include molte azioni [standard incorporate](standard-actions-reference.md) per l'installazione e la manutenzione delle applicazioni. Gli sviluppatori devono tentare di basarsi sulle azioni standard tanto quanto pratiche, anziché creare [azioni personalizzate.](custom-actions.md) Esistono tuttavia situazioni in cui lo sviluppatore di un pacchetto di installazione trova la necessità di scrivere un'azione personalizzata.

-   Seguire le linee guida per [l'uso di azioni personalizzate.](using-custom-actions.md)
-   Seguire le [linee guida per la protezione delle azioni personalizzate.](guidelines-for-securing-custom-actions.md) Le azioni personalizzate che usano informazioni riservate non devono scrivere queste informazioni nel log. Per informazioni, vedere [Sicurezza delle azioni personalizzate.](custom-action-security.md)
-   Le azioni personalizzate non devono tentare di impostare un punto Ripristino configurazione di sistema di ingresso dall'interno di un'azione personalizzata. Per informazioni, vedere [Impostazione di un punto di ripristino da un'azione personalizzata.](setting-a-restore-point-from-a-custom-action.md)
-   Restituire messaggi di errore da azioni personalizzate e scriverli nel log per facilitare la risoluzione dei problemi relativi alle azioni personalizzate. Per informazioni, vedere [Azioni personalizzate del messaggio di errore](error-message-custom-actions.md) e Restituzione di messaggi di errore da azioni [personalizzate](returning-error-messages-from-custom-actions.md).
-   Non modificare lo stato del sistema da un'azione personalizzata immediata. Le azioni personalizzate che modificano direttamente il sistema o chiamano un altro servizio di sistema devono essere rinviate all'ora in cui viene eseguito lo script di installazione. Ogni [azione personalizzata di esecuzione posticipata](deferred-execution-custom-actions.md) che modifica lo stato del sistema deve essere preceduta da un'azione personalizzata di [rollback](rollback-custom-actions.md) per annullare la modifica dello stato del sistema in un rollback dell'installazione. Per informazioni, vedere [Modifica dello stato del sistema tramite un'azione personalizzata.](changing-the-system-state-using-a-custom-action.md)
-   Le azioni personalizzate che eseguono operazioni di installazione complesse devono essere un [file eseguibile](executable-files.md) o [una libreria a collegamento dinamico.](dynamic-link-libraries.md) Limitare l'uso di azioni personalizzate basate su [script a](scripts.md) semplici operazioni di installazione.
-   Rendere facilmente individuabili per gli amministratori di sistema i dettagli delle azioni personalizzate apportate al sistema. Inserire i dettagli delle voci del Registro di sistema e dei file usati dall'azione personalizzata in una tabella personalizzata e fare in modo che l'azione personalizzata sia letta da questa tabella. Questo è dimostrato dall'esempio in [Uso di un'azione personalizzata per creare account utente in un computer locale.](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md) Per informazioni sull'aggiunta di tabelle personalizzate a un database, vedere [Uso](working-with-queries.md) di query ed esempi di query di [database SQL e script](examples-of-database-queries-using-sql-and-script.md).
-   Le azioni personalizzate non devono visualizzare una finestra di dialogo. Le azioni personalizzate che richiedono un'interfaccia utente possono invece [**usare la funzione MsiProcessMessage.**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) Vedere [Invio di messaggi a Windows programma di installazione tramite MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).
-   Le azioni personalizzate non devono usare alcuna delle funzioni elencate nella pagina Funzioni non da [usare nelle azioni personalizzate](functions-not-for-use-in-custom-actions.md).
-   Se l'installazione deve essere eseguita in un server terminal, verificare che tutte le azioni personalizzate siano in grado di essere eseguite in un server terminal. Per altre informazioni, vedere [**La proprietà TerminalServer.**](terminalserver.md)
-   Per eseguire un'azione personalizzata quando viene disinstallata una determinata patch, l'azione personalizzata deve essere presente nell'applicazione originale o essere in una patch per il prodotto che viene sempre applicata. Per altre informazioni, vedere [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).
-   Le azioni personalizzate non devono usare il livello dell'interfaccia utente come condizione per l'invio di messaggi di errore al programma di installazione perché ciò può interferire con la registrazione e i messaggi esterni. Per informazioni, vedere [Determinazione del livello dell'interfaccia utente da un'azione personalizzata.](determining-ui-level-from-a-custom-action.md)
-   Usare le istruzioni [](conditional-statement-syntax.md) condizionali e la sintassi delle istruzioni condizionali per assicurarsi che il pacchetto eserciti correttamente azioni personalizzate, non eserciti azioni personalizzate o eserciti un'azione personalizzata alternativa quando il pacchetto viene disinstallato. Verificare che il pacchetto funzioni come previsto durante [la disinstallazione di azioni personalizzate.](uninstalling-custom-actions.md) Per informazioni, vedere [Condizionamento delle azioni da eseguire durante la rimozione](conditioning-actions-to-run-during-removal.md)
-   Se l'installazione deve essere eseguita da utenti che non dispongono di privilegi di amministratore, verificare che tutte le azioni personalizzate possano essere eseguite con privilegi non di amministratore. Le azioni personalizzate richiedono privilegi elevati per modificare parti del sistema non specifiche dell'utente. Il programma di installazione può eseguire azioni personalizzate con privilegi elevati se è in corso l'installazione di un'applicazione gestita o se sono stati specificati i criteri di sistema per privilegi elevati. Tutte le azioni personalizzate che richiedono privilegi elevati devono includere msidbCustomActionTypeInScript e msidbCustomActionTypeNoImpersonate [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md) nel tipo di azione personalizzata. Questo è dimostrato dall'esempio in [Uso di un'azione personalizzata per creare account utente in un computer locale.](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)

## <a name="if-you-use-assemblies-follow-good-assembly-practices"></a>Se si usano assembly, seguire le procedure consigliate per gli assembly

Se il pacchetto usa [assembly](assemblies.md)software, seguire le linee guida per l'aggiunta di assembly [a](adding-assemblies-to-a-package.md)un pacchetto [,](updating-assemblies.md)l'aggiornamento degli assembly e l'installazione e la rimozione [di assembly](installing-and-removing-assemblies.md).

## <a name="do-not-ship-concurrent-installations"></a>Non spedire installazioni simultanee.

[Le installazioni simultanee,](concurrent-installations.md)denominate anche installazioni annidate, installano un altro pacchetto Windows installer durante un'installazione attualmente in esecuzione. L'uso di installazioni simultanee non è una buona pratica perché sono difficili da usare per i clienti. L'applicazione di patch e l'aggiornamento potrebbero non funzionare con le installazioni simultanee. L'alternativa consigliata all'uso di installazioni simultanee consiste nell'usare invece un'applicazione di installazione e un gestore dell'interfaccia utente esterno per installare Windows pacchetti del programma di installazione in sequenza.

Per altre informazioni sull'uso di un gestore dell'interfaccia utente esterno, vedere [Monitoraggio di un'installazione tramite MsiSetExternalUI.](monitoring-an-installation-using-msisetexternalui.md) Per altre informazioni sull'uso di un gestore esterno basato su record, vedere Monitoraggio di un'installazione [tramite MsiSetExternalUIRecord.](monitoring-an-installation-using-msisetexternaluirecord.md)

Le installazioni simultanee vengono talvolta usate in ambienti aziendali controllati per installare applicazioni non destinate al pubblico. Se si decide di usare installazioni simultanee, seguire queste linee guida.

-   Non usare installazioni simultanee per installare o aggiornare un prodotto di spedizione.
-   Le installazioni simultanee non devono condividere componenti.
-   Un'installazione amministrativa non deve contenere un'installazione simultanea.
-   Le barre di stato integrate non devono essere usate con installazioni simultanee.
-   Le risorse da annunciare non devono essere installate da un'installazione simultanea.
-   Un pacchetto che esegue un'installazione simultanea di un'applicazione deve anche disinstallare l'applicazione simultanea quando viene disinstallato il prodotto padre. Un'installazione annidata esiste nel contesto del prodotto padre in Installazione applicazioni in Pannello di controllo.

## <a name="keep-package-names-and-package-codes-consistent"></a>Mantenere coerenti i nomi e i codici dei pacchetti.

Al file .msi può essere assegnato qualsiasi nome che consente agli utenti di identificare il pacchetto, ma il nome non deve essere modificato senza modificare anche il codice del prodotto.

-   Assegnare al file .msi un nome descrittivo che consenta all'utente di identificare il contenuto del pacchetto Windows Installer.
-   Il [codice prodotto è](product-codes.md) l'identificazione principale di un'applicazione e deve cambiare ogni volta che è disponibile un aggiornamento completo dell'applicazione. Per informazioni, vedere [**ProductCode**](productcode.md) e [Modifica del codice prodotto.](changing-the-product-code.md) La modifica del nome del file .msi dell'applicazione è considerata una modifica completa e richiede sempre una modifica corrispondente del codice prodotto per mantenere la coerenza.
-   Il [codice del pacchetto](package-codes.md) è l'identificatore principale usato dal programma di installazione per cercare e convalidare il pacchetto corretto per una determinata installazione. Due file non .msi non devono mai avere lo stesso codice del pacchetto. Se un pacchetto viene modificato senza modificare il codice del pacchetto, il programma di installazione potrebbe non usare il pacchetto più recente se entrambi sono ancora accessibili al programma di installazione. Il codice del pacchetto viene archiviato nella proprietà [**Riepilogo numero revisione**](revision-number-summary.md) del flusso di informazioni di [riepilogo](summary-information-stream.md).
-   Si noti che le lettere nei GUID del codice prodotto e [del](guid.md) pacchetto devono essere tutte maiuscole.

## <a name="do-not-use-the-selfreg-and-typelib-tables"></a>Non usare le tabelle SelfReg e TypeLib.

-   Gli autori di pacchetti di installazione sono fortemente sconsigliati di usare la registrazione automatica e [la tabella SelfReg.](selfreg-table.md) Devono invece registrare i moduli mediante la creazione di una o più tabelle nel gruppo [Registry Tables.](registry-tables-group.md) Molti dei vantaggi del programma di installazione Windows vengono persi con la registrazione automatica perché le routine di registrazione automatica tendono a nascondere le informazioni di configurazione critiche. Per un elenco dei motivi per evitare la registrazione automatica, vedere [la tabella SelfReg](selfreg-table.md).
-   Gli autori dei pacchetti di installazione sono fortemente sconsigliati di usare la [tabella TypeLib.](typelib-table.md) Anziché usare la tabella TypeLib, registrare le librerie dei tipi usando la [tabella Registry.](registry-table.md) Se un'installazione che usa la tabella TypeLib ha esito negativo e deve essere eseguito il rollback, è possibile che il rollback non ripristini il computer allo stesso stato esistente prima del rollback.

## <a name="provide-the-option-to-install-without-a-user-interface"></a>Specificare l'opzione per l'installazione senza un'interfaccia utente.

Gli amministratori spesso preferiscono distribuire applicazioni all'interno di un'azienda senza richiedere l'interazione dell'utente. È consigliabile consentire all'applicazione di offrire l'opzione di installazione con il [livello dell'interfaccia utente](user-interface-levels.md) Nessuno.

-   Usare [le proprietà pubbliche per](public-properties.md) le informazioni di configurazione. Gli amministratori possono fornire queste informazioni dalla riga di comando.
-   Non è necessario che l'installazione di dipersi dalle informazioni raccolte dall'interazione dell'utente con le finestre di dialogo. Queste informazioni non sono disponibili durante un'installazione invisibile all'utente.
-   Non riavviare automaticamente il computer dell'utente durante un'installazione invisibile all'utente.
-   Gli amministratori possono impostare il [livello dell'interfaccia](user-interface-levels.md) utente durante l'installazione usando l'opzione della [riga di comando](command-line-options.md) "/q". Il livello dell'interfaccia utente può essere impostato anche a livello di codice con una chiamata a [**MsiSetInternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="avoid-using-the-alwaysinstallelevated-policy"></a>Evitare di usare i criteri AlwaysInstallElevated.

Se il [criterio AlwaysInstallElevated](alwaysinstallelevated.md) non è impostato, le applicazioni non distribuite dall'amministratore vengono installate usando i privilegi dell'utente e solo le applicazioni gestite ottengono privilegi elevati. L'impostazione di questo criterio Windows programma di installazione di usare le autorizzazioni di sistema quando installa l'applicazione nel sistema. Questo metodo può aprire un computer a un rischio per la sicurezza, perché quando [](e-gly.md) questo criterio è impostato, un utente non amministratore può eseguire installazioni con privilegi elevati e accedere a percorsi sicuri nel computer. È consigliabile usare un altro metodo rispetto ai criteri [](installing-a-package-with-elevated-privileges-for-a-non-admin.md) AlwaysInstallElevated durante l'installazione di un pacchetto con privilegi elevati per un utente non amministratore o l'applicazione di patch Per-User [applicazioni gestite](patching-per-user-managed-applications.md).

## <a name="enable-the-disablemedia-policy-to-limit-unauthorized-installation"></a>Abilitare il criterio DisableMedia per limitare l'installazione non autorizzata.

Il [criterio DisableMedia](disablemedia.md) può impedire l'installazione non autorizzata delle applicazioni. Quando questo criterio è abilitato, gli utenti e gli amministratori che eseguono un'installazione di manutenzione di un prodotto non possono usare la finestra di dialogo Sfoglia per esplorare le origini dei supporti, ad esempio CD-ROM, per le origini di altri prodotti installabili. L'esplorazione di altri prodotti non è consentita indipendentemente dal fatto che l'installazione sia stata eseguita con privilegi elevati. È comunque possibile che l'utente reinstalli il prodotto dai supporti se l'utente dispone di un'origine multimediale etichettata correttamente.

## <a name="keep-the-original-package-source-files-secure-and-available-to-users"></a>Mantenere i file di origine del pacchetto originale protetti e disponibili per gli utenti.

In alcuni casi può essere necessaria l'origine originale del pacchetto Windows Installer per installare, ripristinare o aggiornare un'applicazione su richiesta. Se il programma di installazione non riesce a individuare un'origine disponibile, all'utente viene richiesto di fornire supporti o di passare a un percorso di rete contenente le origini necessarie. È consigliabile assicurarsi che il programma di installazione abbia le origini necessarie senza dover chiedere conferma all'utente.

-   Usare [firme digitali e file CAB esterni](digital-signatures-and-external-cabinet-files.md) per assicurarsi che le origini oriziali usate dal programma di installazione siano sicure. Un'immagine di origine non compressa archiviata in un percorso pubblico non è sicura.
-   Includere un elenco completo dei percorsi di origine url o di rete del pacchetto di installazione dell'applicazione nella [**proprietà SOURCELIST.**](sourcelist.md)
-   Usare una file system distribuito (DFS) per il percorso di origine.
-   Usare l'API Windows Installer per recuperare e modificare le informazioni dell'elenco di origine per Windows e le patch del programma di installazione. Per informazioni, vedere [Gestione delle origini di installazione.](managing-installation-sources.md)
-   Usare i metodi e le proprietà dell'oggetto [**Installer**](installer-object.md), [**dell'oggetto Product**](product-object.md)e dell'oggetto [**Patch**](patch-object.md) per recuperare e modificare le informazioni dell'elenco di origine per Windows e le patch del programma di installazione.
-   Attenersi ai punti elencati in [Impedire a](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md) una patch di richiedere l'accesso ai punti di origine dell'installazione originale per ridurre al minimo la possibilità che la patch richieda l'accesso alle origini originali.
-   Archiviare i file di origine del pacchetto in un percorso diverso dalla cartella temporanea del sistema. Windows I file di origine del programma di installazione archiviati nella cartella temporanea possono diventare non disponibili per gli utenti.

## <a name="enable-verbose-logging-on-users-computer-when-troubleshooting-deployment"></a>Abilitare la registrazione dettagliata nel computer dell'utente durante la risoluzione dei problemi di distribuzione.

[Windows registrazione del programma di](windows-installer-logging.md) installazione include un'opzione di registrazione dettagliata che può essere abilitata nel computer di un utente. Le informazioni contenute in un log dettagliato possono essere utili quando si tenta di risolvere i Windows distribuzione del pacchetto del programma di installazione.

-   È possibile abilitare la registrazione dettagliata nel computer dell'utente usando le opzioni della riga di comando [,](command-line-options.md)la proprietà [**MsiLogging,**](msilogging.md) i criteri di [registrazione,](logging.md) [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)e [**il metodo EnableLog.**](installer-enablelog.md)
-   Una risorsa molto utile per interpretare i Windows di log del programma di installazione [èWilogutl.exe](wilogutl-exe.md). Questo strumento consente di analizzare i file di log e di visualizzare le soluzioni suggerite per gli errori rilevati in un file di log.
-   Per altre informazioni sull'interpretazione dei file di log Windows Installer, vedere il white paper disponibile nel sito TechNet: [Windows Installer: Benefits and Implementation for System Administrators](https://www.microsoft.com/technet/prodtechnol/windows2000serv/maintain/featusability/winmsi.mspx).
-   L'opzione di registrazione dettagliata deve essere usata solo per la risoluzione dei problemi e non deve essere lasciata attiva perché può avere effetti negativi sulle prestazioni del sistema e sullo spazio su disco. Ogni volta che si usa lo strumento Installazione applicazioni in Pannello di controllo, viene creato un nuovo file.

## <a name="uninstallation-leaves-the-users-computer-in-a-clean-state"></a>La disinstallazione lascia il computer dell'utente in uno stato pulito.

La rimozione delle applicazioni è importante quanto l'installazione. Quando un Windows di installazione viene disinstallato, non deve lasciare alcuna parte inutile di se stesso nel computer dell'utente.

-   Se un file che deve essere stato rimosso dal computer dell'utente rimane installato dopo l'esecuzione di una disinstallazione, è possibile che il programma di installazione non rimova il componente contenente il file per uno o più dei motivi descritti in [Rimozione](removing-stranded-files.md)di file non installati .
-   Se è necessario registrare un'applicazione, creare il pacchetto per rimuovere le informazioni del Registro di sistema quando l'applicazione viene disinstallata. Per informazioni, vedere [Aggiunta o rimozione di chiavi del Registro di sistema nell'installazione o nella rimozione di componenti](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). Se un'applicazione non è registrata, non è elencata nella funzionalità Installazione applicazioni di Pannello di controllo e non può essere gestita tramite il programma di installazione Windows.
-   Per nascondere un'applicazione dalla funzionalità Installazione applicazioni di Pannello di controllo ed essere comunque in grado di usare il programma di installazione di Windows per gestire l'applicazione, seguire le linee guida descritte in Aggiunta e rimozione di un'applicazione e Nessuna traccia nel Registro di [sistema.](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
-   Le azioni personalizzate devono essere condizionate per l'esecuzione o meno in base alle esigenze al momento della disinstallazione. Potrebbe essere necessario eseguire azioni personalizzate diverse durante l'installazione e la disinstallazione.
-   Le informazioni di personalizzazione specifiche dell'utente possono essere archiviate in un file di testo nel computer. Questo ha il vantaggio che il file può essere rimosso quando l'applicazione viene disinstallata, anche se l'utente di questa personalizzazione non è attualmente connesso.

## <a name="test-packages-for-both-per-user-and-per-machine-installation-deployment"></a>Testare i pacchetti per la distribuzione dell'installazione per utente e per computer.

È consigliabile consentire ai clienti di decidere se distribuire un pacchetto per l'installazione nel contesto di installazione per computer o per [utente.](installation-context.md)

-   Valutare se l'applicazione deve essere disponibile solo per determinati utenti o per tutti gli utenti del computer durante il processo di sviluppo.
-   Verificare che il pacchetto funzioni correttamente sia per i contesti di installazione per utente che per computer.
-   Rendere il pacchetto facilmente personalizzabile e consentire ai clienti di decidere se distribuirlo per utente o per computer.

## <a name="plan-and-test-a-servicing-strategy-before-shipping-the-application"></a>Pianificare e testare una strategia di manutenzione prima di spedire l'applicazione.

È necessario decidere come si intende eseguire la gestione dell'applicazione prima di distribuirlo per la prima volta.

-   Prendere in considerazione i tipi di aggiornamenti che si prevede di usare per la gestione dell'applicazione in futuro. Il Windows di installazione offre tre tipi di aggiornamenti: [Small Update,](small-updates.md) [Minor Upgrade](minor-upgrades.md)e [Major Upgrades.](major-upgrades.md) Le differenze sono descritte [nell'argomento Applicazione di patch e](patching-and-upgrades.md) aggiornamenti.
-   Prima di spedire l'applicazione, verificare che funzioni come previsto dopo la manutenzione con ogni tipo di aggiornamento.

## <a name="reduce-the-dependency-of-updates-upon-the-original-sources"></a>Ridurre la dipendenza degli aggiornamenti dalle origini originali.

Se i file di origine originali sono necessari per aggiornare l'applicazione, ciò può rendere più difficile la manutenzione dell'applicazione. I metodi seguenti consentono di ridurre la dipendenza degli aggiornamenti dalle origini originali.

-   Usare una [*patch delta per*](d-gly.md) aggiornare le versioni di base dell'applicazione, ad esempio la versione RTM e le versioni del Service Pack. Seguire le linee guida per l'uso delle patch delta descritte nell'argomento Riduzione [delle dimensioni delle patch.](reducing-patch-size.md)
-   Seguire le raccomandazioni elencate nell'argomento: [Impedisci a una patch di richiedere l'accesso all'origine di installazione originale](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

## <a name="do-not-distribute-unserviceable-merge-modules"></a>Non distribuire moduli unione inutilizzabili.

Le applicazioni non devono dipendere [da moduli unione](merge-modules.md) per l'installazione del componente se il proprietario del modulo unione e il proprietario dell'applicazione sono diversi. Ciò può rendere difficile la gestione dell'applicazione perché entrambi i proprietari devono coordinarsi per aggiornare l'applicazione o il modulo. Senza conoscere tutte le applicazioni che hanno usato il modulo unione, il proprietario dell'applicazione non è in grado di aggiornare il modulo di merge senza rischiare che l'aggiornamento potrebbe essere incompatibile con un'altra applicazione. Il proprietario del modulo unione non dispone di un metodo diretto per l'aggiornamento Windows di installazione che hanno già installato il modulo di merge.

-   È consigliabile fornire i componenti necessari agli utenti come un'altra Windows programma di installazione.

## <a name="avoid-patching-administrative-installations"></a>Evitare di applicare patch alle installazioni amministrative.

Fornire in rete [un'installazione](administrative-installation.md) amministrativa del pacchetto del programma di installazione Windows originale dell'applicazione per consentire ai membri di un gruppo di lavoro di installare l'applicazione. Gli utenti di questa immagine amministrativa devono quindi applicare gli aggiornamenti all'istanza locale dell'applicazione che si trova nel computer. In questo modo gli utenti vengono sempre in sincronizzazione con l'immagine amministrativa. L'applicazione di aggiornamenti all'installazione amministrativa non è consigliata per i motivi seguenti.

-   Le dimensioni e la latenza del download necessarie agli utenti per ottenere un aggiornamento vengono aumentate rispetto al download di una patch. L'intero pacchetto Windows Installer aggiornato e i file di origine devono essere scaricati, memorizzati nuovamente nella cache e reinstallati.
-   Gli utenti non possono eseguire [l'installazione su richiesta](installation-on-demand.md) e ripristinare le applicazioni da un'installazione amministrativa aggiornata fino a quando non vengono memorizzate nuovamente nella cache e reinstallate l'applicazione.
-   L'applicazione di una patch a un'installazione amministrativa rimuove la firma digitale dal pacchetto. Un amministratore deve eseguire la firma del pacchetto. Per altre informazioni sull'uso delle firme digitali, vedere [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).
-   Molte patch binarie hanno come destinazione l'immagine RTM dell'applicazione e richiedono una versione precedente del file. L'istanza locale di un'applicazione installata da un'installazione amministrativa aggiornata potrebbe non funzionare con altri aggiornamenti. Molte applicazioni di patch binarie possono avere esito negativo.
-   L'applicazione di una patch a un'installazione amministrativa aggiorna i file di origine e il file .msi, ma non contrassegna l'immagine di rete con le informazioni sull'aggiornamento. Gli utenti non possono determinare quali aggiornamenti hanno ricevuto dall'installazione amministrativa. Ciò rende impossibile sequenziare gli aggiornamenti applicati sul lato utente con quelli già applicati sul lato dell'immagine amministrativa.
-   Le patch applicate a un'installazione amministrativa non sono [patch disinstallabili.](uninstallable-patches.md) Ciò può impedire che il codice del pacchetto memorizzato nella cache del computer dell'utente diventi diverso dal codice del pacchetto nell'installazione amministrativa. Se il codice del pacchetto memorizzato nella cache del computer dell'utente diventa diverso da quello nell'installazione amministrativa, reinstallare l'applicazione dall'installazione amministrativa e quindi applicare patch al computer client.
-   Se si decide di applicare piccoli aggiornamenti applicando patch a un'immagine amministrativa, seguire le linee guida descritte nell'argomento: Applicazione di piccoli aggiornamenti tramite l'applicazione di patch a [un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md).

## <a name="register-updates-to-run-with-elevated-privilege"></a>Registrare gli aggiornamenti per l'esecuzione con privilegi elevati.

A partire da Windows Installer 3.0, è possibile applicare patch a un'applicazione installata in un contesto gestito per utente, dopo che la patch è stata registrata con privilegi elevati. Non è possibile applicare patch alle applicazioni installate in un contesto gestito per utente usando versioni di Windows Installer precedenti alla versione 3.0.

-   Usare il [**metodo SourceListAddSource**](patch-sourcelistaddsource.md) o la [**funzione MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) per registrare un pacchetto patch con privilegi elevati. Seguire le linee guida e gli esempi forniti in [Applicazione di patch Per-User applicazioni gestite.](patching-per-user-managed-applications.md)
-   Quando si esegue il programma di installazione di Windows versione 4.0 in Windows Vista, è anche possibile usare l'applicazione di patch di Controllo dell'account utente per consentire agli autori delle installazioni del programma di installazione di Windows di identificare le patch con firma digitale che possono essere applicate in futuro da utenti non amministratori. [](user-account-control--uac--patching.md) Questa opzione è disponibile solo con l'installazione di pacchetti nel contesto di installazione per computer [](installation-context.md) (ALLUSERS=1).
-   Assicurarsi che l'applicazione di patch con privilegi minimi non sia stata disabilitata impostando la proprietà [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) o il [criterio DisableLUAPatching.](disableluapatching.md)

## <a name="use-the-msipatchsequence-table-to-sequence-patches"></a>Usare la tabella MsiPatchSequence per sequenziare le patch.

Includere una [tabella MsiPatchSequence nel](msipatchsequence-table.md) pacchetto e aggiungere informazioni di sequenziazione delle patch. A partire da Windows Installer versione 3.0, il programma di installazione può usare la tabella MsiPatchSequence quando si installano più [patch](installing-multiple-patches.md) per determinare la sequenza di applicazione patch migliore. Usare le linee guida descritte in [Sequenza di patch in Windows Installer versione 3.0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3) white paper per la definizione delle famiglie di patch.

-   Se possibile, specificare tutte le patch come appartenenti a un'unica famiglia di patch. In molti casi, una singola famiglia di patch offre una flessibilità sufficiente per sequenziare le patch. La complessità della creazione aumenta quando vengono usate più famiglie di patch. Assegnare un nome significativo alla famiglia di patch e assegnare i valori di sequenza in tale famiglia di patch che aumentano nel tempo. Seguire [l'esempio di applicazione di più](multiple-patching-example.md) patch per applicare le patch nell'ordine in cui sono state rilasciate.
-   Usare la [tabella PatchSequence](patchsequence-table--patchwiz-dll-.md) [Patchwiz.dll](patchwiz-dll.md) generare le informazioni nella tabella [MsiPatchSequence](msipatchsequence-table.md). La versione di PATCHWIZ.DLL rilasciata con Windows Installer 3.0 può generare automaticamente informazioni di sequenziazione delle patch. Per altre informazioni su come aggiungere una nuova patch, vedere [Generating Patch Sequence Information](generating-patch-sequence-information---patchwiz-dll-.md). Per altre informazioni sugli scenari di sequenziazione delle patch, vedere il white paper: [Patch Sequencing in Windows Installer versione 3.0.](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3)

## <a name="test-the-installation-package-thoroughly"></a>Testare accuratamente il pacchetto di installazione.

Testare l'installazione, il ripristino e la rimozione corretti del pacchetto Windows Installer. È possibile dividere il processo di test nelle parti seguenti.

-   Test di installazione: testare l'installazione con tutte le possibili combinazioni di funzionalità dell'applicazione. Testare tutti i tipi di installazione, tra [cui Installazione amministrativa,](administrative-installation.md) [Installazione con rollback](rollback-installation.md)e Installazione su [richiesta.](installation-on-demand.md) Provare tutti i metodi di installazione possibili, tra cui fare clic sul file [.msi,](command-line-options.md)sulle opzioni della riga di comando e sull'installazione dal Pannello di controllo. Verificare che il pacchetto possa essere installato dagli utenti in tutti i contesti di privilegi possibili. Provare a installare il pacchetto dopo che è stato distribuito con tutti i metodi possibili. Abilitare [Windows registrazione del programma di](windows-installer-logging.md) installazione per ogni test e risolvere tutti gli errori rilevati nel log del programma di installazione e nel registro eventi.
-   Interfaccia utente test: testare il pacchetto quando viene installato con tutti i possibili [livelli di interfaccia utente](user-interface-levels.md). Testare il pacchetto installato senza interfaccia utente e con tutte le informazioni fornite tramite l'interfaccia utente. Verificare [l'accessibilità](accessibility.md) dell'interfaccia utente e che l'interfaccia utente funzioni come previsto per diverse risoluzioni dello schermo e dimensioni dei caratteri.
-   Test di manutenzione e ripristino: verificare che il pacchetto sia in grado [](minor-upgrades.md)di gestire l'applicazione di [patch](patching-and-upgrades.md) e gli aggiornamenti recapitati da un aggiornamento di piccole [dimensioni,](small-updates.md)da un aggiornamento secondario e da [aggiornamenti principali.](major-upgrades.md) Prima di distribuire il pacchetto, scrivere un aggiornamento di valutazione di ogni tipo e provare ad applicarlo al pacchetto originale.
-   Test di disinstallazione: verificare che quando il pacchetto viene rimosso non lasci parti inutili di se stesso nel computer dell'utente e che siano state rimosse solo le informazioni appartenenti al pacchetto. Riavviare il computer di test dopo aver disinstallato il pacchetto e verificare l'integrità degli strumenti di sistema comuni e di altre applicazioni standard. Verificare che il pacchetto possa essere rimosso dagli utenti in tutti i contesti di privilegi possibili. Testare tutti i metodi per rimuovere il pacchetto, [](command-line-options.md)fare clic sul file .msi, provare le opzioni della riga di comando e provare a rimuovere il pacchetto dal Pannello di controllo. Abilitare [Windows registrazione del programma di](windows-installer-logging.md) installazione per ogni test e risolvere tutti gli errori rilevati nel log del programma di installazione e nel registro eventi.
-   Test delle funzionalità del prodotto: assicurarsi che l'applicazione funzioni come previsto dopo l'installazione, il ripristino o la rimozione del pacchetto.

## <a name="fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package"></a>Correggere tutti gli errori di convalida prima di distribuire un pacchetto di installazione nuovo o modificato.

Eseguire [la convalida del](package-validation.md) pacchetto in un pacchetto Windows installer nuovo o modificato prima di provare a installarlo per la prima volta. La convalida controlla la presenza Windows errori di creazione nel database del programma di installazione. Il tentativo di installare un pacchetto che non supera la convalida può danneggiare il sistema dell'utente.

-   È possibile convalidare il pacchetto [ usandoOrca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md). Entrambi gli strumenti vengono forniti con Windows SDK. I fornitori di terze parti possono anche incorporare il sistema di convalida ICE nell'ambiente di creazione.
-   È possibile usare il set standard di analizzatori di coerenza interna [,](internal-consistency-evaluators-ices.md) inclusi nei file con [](building-an-ice.md) estensione cub forniti con l'SDK, oppure personalizzare la convalida creando un ice e aggiungendolo al file con estensione cub.
-   È possibile usare il Evalcom2.dll per implementare l'automazione [della convalida](validation-automation.md) per i pacchetti di installazione e i moduli unione.

## <a name="author-a-secure-installation"></a>Creare un'installazione sicura.

Seguire queste linee guida quando si sviluppa il pacchetto per mantenere un ambiente sicuro durante l'installazione.

-   [Linee guida per la creazione di installazioni sicure](guidelines-for-authoring-secure-installations.md)
-   [Linee guida per la protezione dei pacchetti nei computer bloccati](guidelines-for-securing-packages-on-locked-down-computers.md)
-   [Linee guida per la protezione delle azioni personalizzate](guidelines-for-securing-custom-actions.md)

## <a name="use-pmsihandle-instead-of-handle"></a>Usare PMSIHANDLE anziché HANDLE

Le variabili di tipo **PMSIHANDLE** sono definite in msi.h. È consigliabile che l'applicazione usi il tipo **PMSIHANDLE** perché il programma di installazione chiude gli oggetti **PMSIHANDLE** non appena es uscita dall'ambito, mentre l'applicazione deve chiudere gli oggetti **MSIHANDLE** chiamando [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).

Ad esempio, se si usa codice simile al seguente:

``` syntax
MSIHANDLE hRec = MsiCreateRecord(3);
```

Modificarlo in:

``` syntax
PMSIHANDLE hRec = MsiCreateRecord(3);
```

 

 
