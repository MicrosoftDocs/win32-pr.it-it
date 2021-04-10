---
description: "Questa sezione enumera un elenco di suggerimenti, collegati alla documentazione principale di Windows Installer SDK, per aiutare gli sviluppatori di applicazioni, gli autori di installazione, i professionisti IT e gli sviluppatori di infrastrutture a individuare le procedure consigliate per l'uso della Windows Installer:"
ms.assetid: ff48d995-fe6f-4d1b-898d-67574ed3c5b7
title: Procedure consigliate Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffaf6aae83afbe510f2b1eefc447e34754296ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057803"
---
# <a name="windows-installer-best-practices"></a>Procedure consigliate Windows Installer

Questa sezione enumera un elenco di suggerimenti, collegati alla documentazione principale di Windows Installer SDK, per aiutare gli sviluppatori di applicazioni, gli autori di installazione, i professionisti IT e gli sviluppatori di infrastrutture a individuare le procedure consigliate per l'uso della Windows Installer:

-   [Aggiornare la versione del Windows Installer.](#update-the-windows-installer-version)
-   [Soddisfare i requisiti di certificazione del logo Windows.](#meet-the-windows-logo-certification-requirements)
-   [Preparare il pacchetto per la localizzazione.](#prepare-the-package-for-localization)
-   [Aggiornare la documentazione e gli strumenti di sviluppo Windows Installer.](#update-your-windows-installer-development-tools-and-documentation)
-   [Se si decide di ricreare un pacchetto di un'applicazione di installazione legacy, seguire le buone procedure per la creazione di pacchetti.](#if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices)
-   [Non tentare di sostituire le risorse protette.](#do-not-try-to-replace-protected-resources)
-   [Non dipendono da risorse non critiche.](#do-not-depend-upon-non-critical-resources)
-   [Usare l'API per recuperare le informazioni di configurazione Windows Installer.](#use-the-api-to-retrieve-windows-installer-configuration-information)
-   [Organizzare l'installazione dell'applicazione intorno ai componenti.](#organize-the-installation-of-your-application-around-components)
-   [Ridurre le dimensioni dei pacchetti di Windows Installer di grandi dimensioni.](#reduce-the-size-of-large-windows-installer-packages)
-   [Se si usano azioni personalizzate, seguire le buone procedure di azione personalizzate.](#if-you-use-custom-actions-follow-good-custom-action-practices)
-   [Se si usano gli assembly, seguire le buone procedure per gli assembly](#if-you-use-assemblies-follow-good-assembly-practices)
-   [Non vengono fornite installazioni simultanee.](#do-not-ship-concurrent-installations)
-   [Mantieni i nomi dei pacchetti e i codici del pacchetto coerenti.](#keep-package-names-and-package-codes-consistent)
-   [Non usare le tabelle SelfReg e TypeLib.](#do-not-use-the-selfreg-and-typelib-tables)
-   [Consente di specificare l'opzione di installazione senza interfaccia utente.](#provide-the-option-to-install-without-a-user-interface)
-   [Evitare di usare i criteri AlwaysInstallElevated.](#avoid-using-the-alwaysinstallelevated-policy)
-   [Abilitare il criterio DisableMedia per limitare l'installazione non autorizzata.](#enable-the-disablemedia-policy-to-limit-unauthorized-installation)
-   [Mantieni i file di origine del pacchetto originali protetti e disponibili per gli utenti.](#keep-the-original-package-source-files-secure-and-available-to-users)
-   [Abilitare la registrazione dettagliata nel computer dell'utente durante la risoluzione dei problemi di distribuzione.](#enable-verbose-logging-on-users-computer-when-troubleshooting-deployment)
-   [La disinstallazione lascia il computer dell'utente in uno stato pulito.](#uninstallation-leaves-the-users-computer-in-a-clean-state)
-   [Testare i pacchetti per la distribuzione dell'installazione per utente e per computer.](#test-packages-for-both-per-user-and-per-machine-installation-deployment)
-   [Pianificare e testare una strategia di manutenzione prima di distribuire l'applicazione.](#plan-and-test-a-servicing-strategy-before-shipping-the-application)
-   [Ridurre la dipendenza degli aggiornamenti sulle origini originali.](#reduce-the-dependency-of-updates-upon-the-original-sources)
-   [Non distribuire i moduli merge non collegabili.](#do-not-distribute-unserviceable-merge-modules)
-   [Evitare l'applicazione di patch alle installazioni amministrative.](#avoid-patching-administrative-installations)
-   [Registrare gli aggiornamenti da eseguire con privilegi elevati.](#register-updates-to-run-with-elevated-privilege)
-   [Usare la tabella MsiPatchSequence per sequenziare le patch.](#use-the-msipatchsequence-table-to-sequence-patches)
-   [Testare accuratamente il pacchetto di installazione.](#test-the-installation-package-thoroughly)
-   [Correggere tutti gli errori di convalida prima di distribuire un pacchetto di installazione nuovo o modificato.](#fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package)
-   [Creare un'installazione sicura.](#author-a-secure-installation)
-   [USA PMSIHANDLE anziché HANDLE](#use-pmsihandle-instead-of-handle)

## <a name="update-the-windows-installer-version"></a>Aggiornare la versione del Windows Installer.

-   Usare Windows Installer 5,0 in Windows Server 2008 R2 e Windows 7. Si tratta della versione Windows Installer fornita con il sistema operativo.
-   Utilizzare Windows Installer 4,5 in Windows Server 2008, Windows Server 2003 con Service Pack 1 (SP1), Windows Vista con Service Pack 1 (SP1) o Windows XP con Service Pack 2 (SP2). Per informazioni su come ottenere la versione più recente di Windows Installer, vedere [Windows Installer ridistribuibili](windows-installer-redistributables.md).
-   Usare Windows Installer 3,1 in Windows 2000 con Service Pack 3 (SP3). Windows Installer versione 3,1 dispone di funzionalità che facilitano la manutenzione e l'applicazione di [patch](patching.md)migliori.
-   Molte importanti funzionalità sono state introdotte con la versione 3,0 e sono elencate nella sezione [non supportata in Windows Installer versione 2,0](not-supported-in-windows-installer-version-2-0.md). È possibile installare i pacchetti di installazione e gli aggiornamenti creati per Windows Installer 2,0 usando Windows Installer 3,0 e versioni successive. I pacchetti di patch contenenti le nuove tabelle utilizzate da Windows Installer 3,0 possono comunque essere applicati utilizzando versioni precedenti di Windows Installer ma senza la funzionalità di applicazione delle patch Windows Installer 3,0. È anche possibile creare patch che richiedono in modo esplicito il Windows Installer 3,0 che non possono essere applicate da versioni precedenti di Windows Installer. Se un utente non è in grado di aggiornare la versione del programma di installazione, assicurarsi che l'applicazione o l'aggiornamento saranno compatibili con un aggiornamento futuro del Windows Installer.
-   Per un elenco delle funzionalità di Windows Installer non supportate nelle versioni precedenti di Windows Installer, vedere [novità di Windows Installer](what-s-new-in-windows-installer.md).

## <a name="meet-the-windows-logo-certification-requirements"></a>Soddisfare i requisiti di certificazione del logo Windows.

-   Anche se non si prevede di inviare l'applicazione al programma logo, le linee guida per la certificazione del logo possono contribuire a migliorare il pacchetto di Windows Installer. Per una panoramica dei requisiti del logo e per i collegamenti a specifici programmi di certificazione del logo, vedere [Windows Installer e logo requirements](windows-installer-and-logo-requirements.md).

## <a name="prepare-the-package-for-localization"></a>Preparare il pacchetto per la localizzazione.

-   È consigliabile prepararsi per la localizzazione futura durante la creazione del pacchetto di installazione originale. È possibile seguire la procedura di localizzazione dei pacchetti suggerita in [localizzazione di un pacchetto di Windows Installer](localizing-a-windows-installer-package.md).

## <a name="update-your-windows-installer-development-tools-and-documentation"></a>Aggiornare la documentazione e gli strumenti di sviluppo Windows Installer.

-   Gli [strumenti di sviluppo Windows Installer](windows-installer-development-tools.md) non sono ridistribuibili ed è consigliabile utilizzare solo le versioni di questi strumenti disponibili da Microsoft. Questi sono disponibili nella [Windows SDK componenti per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md) in Microsoft Windows Software Development Kit (SDK).
-   Diversi fornitori di software indipendenti offrono strumenti per creare o modificare pacchetti Windows Installer. Questi strumenti possono fornire un ambiente di creazione di pacchetti che può essere più facile da usare rispetto agli strumenti disponibili in Windows Installer SDK. Per ulteriori informazioni su questi strumenti, vedere le risorse di informazioni illustrate in [altre fonti di Windows Installer informazioni](other-sources-of-windows-installer-information.md).
-   La possibilità di creare un pacchetto dai file di testo può essere più intuitiva per alcuni sviluppatori. Il set di strumenti Windows Installer XML (WiX) disponibile in [sourceforge.NET](https://sourceforge.net/projects/wix) compila i pacchetti di installazione di Windows dal codice sorgente XML.
-   La documentazione di [Windows Installer SDK](./windows-installer-portal.md) rilasciata in MSDN Library viene aggiornata più di frequente.
-   Utilizzare la versione recente di [Msizap.exe](msizap-exe.md) (versione 3.1.4000.2726 o successiva) disponibile nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md) per Windows Vista o versione successiva. Versioni minori di Msizap.exe possono rimuovere informazioni su tutti gli aggiornamenti applicati ad altre applicazioni nel computer dell'utente. Se queste informazioni vengono rimosse, potrebbe essere necessario rimuovere e reinstallare le altre applicazioni per ricevere ulteriori aggiornamenti.
-   L'editor di tabelle di database [Orca.exe](orca-exe.md) è un editor di tabelle di database per la creazione e la modifica di Windows Installer pacchetti e i moduli unione. Dispone di un'interfaccia GUI di base che supporta la modifica avanzata dei database Windows Installer. Anche se si usa un'altra applicazione come strumento di sviluppo principale, è possibile trovare l'uso di Orca.exe è utile per la risoluzione dei problemi e il test di un pacchetto.
-   Per informazioni aggiornate sui Windows Installer disponibili in Blog, chat tecniche, newsgroup, articoli tecnici e siti Web, vedere [altre fonti di Windows Installer informazioni](other-sources-of-windows-installer-information.md) .

## <a name="if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices"></a>Se si decide di ricreare un pacchetto di un'applicazione di installazione legacy, seguire le buone procedure per la creazione di pacchetti.

Molti fornitori di applicazioni forniscono pacchetti di Windows Installer nativi per l'installazione o i prodotti. Il software che converte un'applicazione di installazione legacy esistente in un pacchetto di Windows Installer viene definito strumento per la creazione di pacchetti. La [Guida dettagliata al white paper per la creazione di pacchetti di Windows Installer e la ricreazione del pacchetto del software per la Windows Installer](https://www.microsoft.com/technet/prodtechnol/windows2000serv/howto/winstall.mspx) descrive uno strumento di Repackaging disponibile in commercio. Il riassemblaggio di un'applicazione di installazione esistente non è la procedura di sviluppo ottimale. Le applicazioni progettate dall'inizio per sfruttare i vantaggi delle funzionalità di Windows Installer possono essere più facili da installare e servire dagli utenti. Se si decide di usare un software di riconfezionamento, le procedure seguenti consentono di produrre un pacchetto di Windows Installer migliore.

-   La creazione di pacchetti di strumenti consente di convertire le installazioni legacy in un pacchetto di Windows Installer facendo un'immagine di un sistema di gestione temporanea prima e dopo l'installazione. Eventuali modifiche al registro di sistema, modifiche dei file o impostazioni di sistema che si verificano durante il processo di acquisizione sono incluse nell'installazione. Configurare l'hardware e il software del computer utilizzato per riassemblare l'installazione il più vicino possibile al sistema dell'utente desiderato. Creare un pacchetto separato per ogni configurazione hardware differente. Ricreare il pacchetto utilizzando un computer di staging pulito. Rimuovere tutte le applicazioni non necessarie. Arrestare tutti i processi non necessari. Chiudere tutti i servizi di sistema non essenziali.
-   Prima di iniziare a lavorare, creare sempre una copia dell'installazione originale. Usare sempre la copia. Non arrestare mai un riassemblatore prima di completare la compilazione del pacchetto. Se il riassemblatore danneggia il pacchetto, si avrà ancora l'originale.
-   Non riassemblare gli aggiornamenti software Microsoft in un pacchetto di Windows Installer. Microsoft rilascia gli aggiornamenti software, ad esempio i Service Pack, come file autoestraenti che eseguono automaticamente l'installazione. Questi aggiornamenti usano programmi di installazione diversi rispetto al Windows Installer per sostituire le risorse protette di Windows e non possono essere convertiti in un pacchetto di Windows Installer. Per informazioni su come distribuire i Service Pack di Windows, vedere la guida alla distribuzione di Service Pack in [Microsoft TechNet](https://technet.microsoft.com/).
-   Non usare uno strumento di reimballaggio per convertire un pacchetto di Windows Installer in un nuovo pacchetto. Il Windows Installer aggiunge informazioni di configurazione al sistema e alle risorse dell'applicazione. Quando uno strumento di reimballaggio confronta il sistema prima e dopo l'installazione, il reimballatore interpreta erroneamente le informazioni di configurazione come parte dell'applicazione. Questa operazione in genere danneggia l'applicazione riassemblata. Usare invece le [trasformazioni di personalizzazione](a-customization-transform-example.md) per modificare un pacchetto di Windows Installer esistente o creare un nuovo pacchetto. È possibile creare trasformazioni di personalizzazione utilizzando lo strumento [Msitran.exe](msitran-exe.md) .
-   Non usare uno strumento di riconfezionamento per consolidare diversi pacchetti di Windows Installer in un unico pacchetto. È invece possibile usare lo strumento [Msistuff.exe](msistuff-exe.md) per configurare l'eseguibile di bootstrap Setup.exe per installare i pacchetti uno dopo l'altro.
-   Creare il pacchetto di Windows Installer in modo che possa essere facilmente personalizzato dal cliente. Le variabili globali utilizzate dal Windows Installer durante un'installazione possono essere impostate utilizzando le [Proprietà](properties.md) pubbliche o le [trasformazioni di personalizzazione](a-customization-transform-example.md). Fornire la documentazione per l'utilizzo di tali proprietà e i valori predefiniti pratici per tutti i valori personalizzabili. Per informazioni su come ottenere e impostare le proprietà, vedere [using Properties](using-properties.md). Per un esempio di trasformazione della personalizzazione, vedere [un esempio di trasformazione della personalizzazione](a-customization-transform-example.md).

## <a name="do-not-try-to-replace-protected-resources"></a>Non tentare di sostituire le risorse protette.

I pacchetti Windows Installer non devono tentare di sostituire le risorse protette durante l'installazione o l'aggiornamento. Il Windows Installer non rimuove o sostituisce queste risorse perché Windows impedisce la sostituzione di file di sistema, cartelle e chiavi del registro di sistema essenziali. La protezione di queste risorse impedisce gli errori dell'applicazione e del sistema operativo.

-   Quando è in esecuzione in Windows Server 2008 o Windows Vista, il Windows Installer ignora l'installazione di qualsiasi file o chiave del registro di sistema protetta da [Protezione risorse di Windows](../wfp/windows-resource-protection-portal.md) (WRP), il programma di installazione immette un avviso nel file di log e continua con il resto dell'installazione senza errori. Per informazioni, vedere [utilizzo di Windows Installer e protezione risorse di Windows](windows-resource-protection-on-windows-vista.md).
-   WRP è il nuovo nome per la protezione dei file di Windows (WFP). WRP protegge le chiavi del registro di sistema e le cartelle, nonché i file di sistema essenziali. In Windows Server 2003, Windows XP e Windows 2000, quando il Windows Installer ha rilevato un file protetto da WFP, il programma di installazione richiederà l'installazione del file da parte di Pam. Per informazioni, vedere [utilizzo di Windows Installer e protezione risorse di Windows](windows-resource-protection-on-windows-vista.md).

## <a name="do-not-depend-upon-non-critical-resources"></a>Non dipendono da risorse non critiche.

L'installazione o l'aggiornamento non deve dipendere dall'installazione di risorse non critiche per i motivi seguenti.

-   Le azioni personalizzate possono avere esito negativo se dipendono da un componente appartenente a una funzionalità che l'utente annuncia anziché installare.
-   Le azioni personalizzate sequenziate prima dell'azione [InstallFinalize](installfinalize-action.md) possono avere esito negativo se dipendono da un componente contenente un assembly in fase di installazione. Il Windows Installer non esegue il commit degli assembly nella global assembly cache (GAC) finché non viene completata l'azione InstallFinalize.

## <a name="use-the-api-to-retrieve-windows-installer-configuration-information"></a>Usare l'API per recuperare le informazioni di configurazione Windows Installer.

L'installazione dell'applicazione o dell'aggiornamento non deve dipendere dall'accesso diretto alle informazioni di configurazione Windows Installer salvate nel computer. Usare invece il Application Programming Interface Windows Installer per recuperare le informazioni di configurazione. Il percorso e il formato delle informazioni di configurazione sono gestiti dal servizio Windows Installer e possono essere modificati.

-   Le funzioni di installazione e configurazione dell'API Windows Installer sono descritte nella Guida di [riferimento alla funzione del programma](installer-function-reference.md)di installazione.
-   Le [proprietà di configurazione](property-reference.md) sono descritte nel riferimento alla proprietà.
-   I metodi e le proprietà di automazione sono descritti nella Guida di [riferimento all'interfaccia di automazione](automation-interface-reference.md). Lo script di esempio WiLstPrd.vbs si connette a un oggetto del programma di installazione ed enumera i prodotti registrati e le informazioni sul prodotto. Per informazioni, vedere [elencare prodotti, proprietà, funzionalità e componenti](list-products-properties-features-and-components.md).

## <a name="organize-the-installation-of-your-application-around-components"></a>Organizzare l'installazione dell'applicazione intorno ai componenti.

Il servizio Windows Installer installa o rimuove raccolte di risorse definite [componenti](windows-installer-components.md). Poiché i componenti sono comunemente condivisi, l'autore di un pacchetto di installazione deve seguire le regole quando si specificano i componenti di una funzionalità o di un'applicazione.

-   Rispettare le regole dei componenti quando si [organizzano le applicazioni in componenti](organizing-applications-into-components.md) per garantire che i nuovi componenti, o le nuove versioni dei componenti, possano essere installati e rimossi senza danneggiare altre applicazioni. È possibile seguire la procedura descritta in [definizione dei componenti del programma di installazione](defining-installer-components.md).
-   Il programma di installazione tiene traccia di ogni componente per il rispettivo GUID ID componente specificato nella [tabella dei componenti](component-table.md). È essenziale per il funzionamento del Windows Installer meccanismo di conteggio dei riferimenti che il GUID dell'ID componente sia corretto. Seguire le linee guida per la [modifica del codice componente](changing-the-component-code.md).
-   Se il pacchetto deve suddividere le regole dei componenti, tenere presenti le possibili conseguenze e assicurarsi che l'installazione non installi mai questi componenti in modo che possano danneggiare i componenti nel sistema dell'utente. Per informazioni, vedere [cosa accade se le regole del componente sono interrotte?](what-happens-if-the-component-rules-are-broken.md).
-   Tenere presente il modo in cui il Windows Installer applica le [regole di controllo delle versioni dei file](file-versioning-rules.md) durante la sostituzione dei [file esistenti](replacing-existing-files.md). Il Windows Installer determina innanzitutto se il file di chiave del componente è già installato prima di tentare di installare uno dei file del componente. Se il programma di installazione trova un file con lo stesso nome del file di chiave del componente installato nel percorso di destinazione, confronta la versione, la data e la lingua dei due file chiave e usa le regole di controllo delle versioni dei file per determinare se installare il componente fornito dal pacchetto. Se il programma di installazione stabilisce che è necessario sostituire la base del componente sul file di chiave, USA le regole di controllo delle versioni dei file per ogni file installato per determinare se sostituire il file.

## <a name="reduce-the-size-of-large-windows-installer-packages"></a>Ridurre le dimensioni dei pacchetti di Windows Installer di grandi dimensioni.

I pacchetti Windows di grandi dimensioni accettano risorse di sistema e possono essere difficili da installare per gli utenti. È consigliabile ridurre le dimensioni dei pacchetti di Windows Installer molto grandi con i metodi seguenti.

-   Comprimere i file nell'installazione e archiviarli in un file CAB (con estensione cab). Il programma di installazione consente di archiviare il file con estensione cab come file esterno separato o come flusso di dati nel pacchetto MSI stesso. Per informazioni [, vedere uso di cabinet e origini compresse](using-cabinets-and-compressed-sources.md).
-   Rimuovere lo spazio di archiviazione sprecato nel file con estensione MSI usando una delle opzioni descritte in [riduzione delle dimensioni di un file con estensione msi](reducing-the-size-of-an--msi-file.md).
-   Se il pacchetto di Windows Installer contiene più di 32767 file, è necessario modificare lo schema del database. Per informazioni, vedere [creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md).

## <a name="if-you-use-custom-actions-follow-good-custom-action-practices"></a>Se si usano azioni personalizzate, seguire le buone procedure di azione personalizzate.

Il Windows Installer dispone di molte [azioni standard](standard-actions-reference.md) predefinite per l'installazione e la gestione delle applicazioni. Gli sviluppatori devono provare a basarsi sulle azioni standard quanto più pratica, anziché creare [azioni personalizzate](custom-actions.md). Tuttavia, esistono situazioni in cui lo sviluppatore di un pacchetto di installazione rileva che è necessario scrivere un'azione personalizzata.

-   Seguire le linee guida per l' [uso di azioni personalizzate](using-custom-actions.md).
-   Seguire le [linee guida per proteggere le azioni personalizzate](guidelines-for-securing-custom-actions.md). Le azioni personalizzate che usano informazioni riservate non devono scrivere queste informazioni nel log. Per informazioni, vedere [sicurezza dell'azione personalizzata](custom-action-security.md).
-   Le azioni personalizzate non devono tentare di impostare un punto di ingresso di ripristino del sistema dall'interno di un'azione personalizzata. Per informazioni, vedere [impostazione di un punto di ripristino da un'azione personalizzata](setting-a-restore-point-from-a-custom-action.md).
-   Restituisce i messaggi di errore dalle azioni personalizzate e li scrive nel log per facilitare la risoluzione dei problemi relativi alle azioni personalizzate. Per informazioni, vedere [azioni personalizzate del messaggio di errore](error-message-custom-actions.md) e [restituzione di messaggi di errore da azioni personalizzate](returning-error-messages-from-custom-actions.md).
-   Non modificare lo stato del sistema da un'azione personalizzata immediata. Le azioni personalizzate che modificano direttamente il sistema o chiamano un altro servizio di sistema devono essere rinviate al momento in cui viene eseguito lo script di installazione. Ogni [azione personalizzata di esecuzione posticipata](deferred-execution-custom-actions.md) che modifica lo stato del sistema deve essere preceduta da un' [azione personalizzata rollback](rollback-custom-actions.md) per annullare la modifica dello stato del sistema durante il rollback dell'installazione. Per informazioni, vedere [modifica dello stato del sistema mediante un'azione personalizzata](changing-the-system-state-using-a-custom-action.md).
-   Le azioni personalizzate che eseguono operazioni di installazione complesse devono essere un [file eseguibile](executable-files.md) o una [libreria a collegamento dinamico](dynamic-link-libraries.md). Limitare l'uso di azioni personalizzate basate su [script](scripts.md) per semplici operazioni di installazione.
-   Rendere facilmente individuabili gli amministratori di sistema i dettagli relativi all'azione personalizzata eseguita dal sistema. Inserire i dettagli delle voci del registro di sistema e dei file utilizzati dall'azione personalizzata in una tabella personalizzata e fare in modo che l'azione personalizzata legga da questa tabella. Questa operazione viene illustrata nell'esempio di [utilizzo di un'azione personalizzata per creare account utente in un computer locale](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md). Per informazioni sull'aggiunta di tabelle personalizzate a un database, vedere [utilizzo di query](working-with-queries.md) ed [esempi di query di database tramite SQL e script](examples-of-database-queries-using-sql-and-script.md).
-   Le azioni personalizzate non devono visualizzare una finestra di dialogo. Le azioni personalizzate che richiedono un'interfaccia utente possono invece usare la funzione [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) . Vedere [invio di messaggi a Windows Installer con MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).
-   Per le azioni personalizzate non è necessario utilizzare alcuna delle funzioni elencate nella pagina: [funzioni non utilizzabili in azioni personalizzate](functions-not-for-use-in-custom-actions.md).
-   Se l'installazione è progettata per l'esecuzione in un server terminal, verificare che tutte le azioni personalizzate siano in grado di essere eseguite in un server terminal. Per ulteriori informazioni, vedere proprietà [**TerminalServer**](terminalserver.md) .
-   Per eseguire un'azione personalizzata quando una particolare patch viene disinstallata, l'azione personalizzata deve essere presente nell'applicazione originale o essere inclusa in una patch per il prodotto che viene sempre applicato. Per altre informazioni, vedere [patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).
-   Le azioni personalizzate non devono utilizzare il livello di interfaccia utente come condizione per l'invio di messaggi di errore al programma di installazione, in quanto ciò può interferire con la registrazione e i messaggi esterni. Per informazioni, vedere [determinazione del livello dell'interfaccia utente da un'azione personalizzata](determining-ui-level-from-a-custom-action.md).
-   Usare le istruzioni condizionali e la [sintassi dell'istruzione condizionale](conditional-statement-syntax.md) per garantire che il pacchetto esegua correttamente le azioni personalizzate, non esegue azioni personalizzate o esegue un'azione personalizzata alternativa quando il pacchetto viene disinstallato. Verificare che il pacchetto funzioni come previsto durante la [Disinstallazione delle azioni personalizzate](uninstalling-custom-actions.md). Per informazioni, vedere [azioni di condizionamento da eseguire durante la rimozione](conditioning-actions-to-run-during-removal.md)
-   Se l'installazione deve essere in grado di essere eseguita da utenti che non dispongono di privilegi di amministratore, eseguire un test per assicurarsi che tutte le azioni personalizzate possano essere eseguite con privilegi non amministrativi. Per le azioni personalizzate sono necessari privilegi elevati per modificare parti del sistema che non sono specifiche dell'utente. Il programma di installazione può eseguire azioni personalizzate con privilegi elevati se è in corso l'installazione di un'applicazione gestita o se i criteri di sistema sono stati specificati per privilegi elevati. Tutte le azioni personalizzate che richiedono privilegi elevati devono includere l'azione personalizzata msidbCustomActionTypeInScript e msidbCustomActionTypeNoImpersonate [In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md) nel tipo di azione personalizzata. Questa operazione viene illustrata nell'esempio di [utilizzo di un'azione personalizzata per creare account utente in un computer locale](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md).

## <a name="if-you-use-assemblies-follow-good-assembly-practices"></a>Se si usano gli assembly, seguire le buone procedure per gli assembly

Se il pacchetto utilizza [assembly](assemblies.md)software, attenersi alle linee guida per l' [aggiunta di assembly a un pacchetto](adding-assemblies-to-a-package.md), l' [aggiornamento degli assembly](updating-assemblies.md)e [l'installazione e la rimozione di assembly](installing-and-removing-assemblies.md).

## <a name="do-not-ship-concurrent-installations"></a>Non vengono fornite installazioni simultanee.

Le [installazioni simultanee](concurrent-installations.md), denominate anche installazioni annidate, installano un altro pacchetto Windows Installer durante un'installazione attualmente in esecuzione. L'uso di installazioni simultanee non è una procedura consigliata perché è difficile per i clienti. L'applicazione di patch e l'aggiornamento potrebbero non funzionare con le installazioni simultanee. L'alternativa consigliata per l'utilizzo di installazioni simultanee consiste invece nell'utilizzare un'applicazione di installazione e un gestore dell'interfaccia utente esterno per installare più pacchetti Windows Installer in modo sequenziale.

Per ulteriori informazioni sull'utilizzo di un gestore dell'interfaccia utente esterno, vedere [monitoraggio di un'installazione mediante MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md). Per ulteriori informazioni sull'utilizzo di un gestore esterno basato su record, vedere [monitoraggio di un'installazione mediante MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).

Le installazioni simultanee vengono talvolta utilizzate negli ambienti aziendali controllati per installare le applicazioni che non sono destinate al pubblico. Se si decide di utilizzare installazioni simultanee, attenersi a queste linee guida.

-   Non utilizzare installazioni simultanee per installare o aggiornare un prodotto di spedizione.
-   Le installazioni simultanee non devono condividere i componenti.
-   Un'installazione amministrativa non deve contenere un'installazione simultanea.
-   I ProgressBar integrati non devono essere usati con installazioni simultanee.
-   Le risorse da annunciare non devono essere installate da un'installazione simultanea.
-   Un pacchetto che esegue un'installazione simultanea di un'applicazione deve disinstallare anche l'applicazione simultanea quando viene disinstallato il prodotto padre. Un'installazione nidificata è presente nel contesto del prodotto padre in Installazione applicazioni nel pannello di controllo.

## <a name="keep-package-names-and-package-codes-consistent"></a>Mantieni i nomi dei pacchetti e i codici del pacchetto coerenti.

Al file con estensione msi è possibile assegnare qualsiasi nome che consenta agli utenti di identificare il pacchetto, ma il nome non deve essere modificato senza modificare anche il codice del prodotto.

-   Assegnare al file con estensione msi un nome descrittivo che consenta all'utente di identificare il contenuto del pacchetto Windows Installer.
-   Il [codice del prodotto](product-codes.md) è l'identificazione principale di un'applicazione e deve essere modificato ogni volta che viene eseguito un aggiornamento completo dell'applicazione. Per informazioni, vedere [**ProductCode**](productcode.md) e [modifica del codice del prodotto](changing-the-product-code.md). La modifica del nome del file con estensione msi dell'applicazione è considerata una modifica completa e richiede sempre una modifica corrispondente del codice prodotto per garantire la coerenza.
-   Il [codice del pacchetto](package-codes.md) è l'identificatore primario utilizzato dal programma di installazione per cercare e convalidare il pacchetto corretto per una determinata installazione. Due file con estensione msi non identici dovrebbero avere sempre lo stesso codice del pacchetto. Se un pacchetto viene modificato senza modificare il codice del pacchetto, è possibile che il programma di installazione non usi il pacchetto più recente se entrambi sono ancora accessibili al programma di installazione. Il codice del pacchetto viene archiviato nella proprietà [**Riepilogo numero revisione**](revision-number-summary.md) del [flusso di informazioni di riepilogo](summary-information-stream.md).
-   Si noti che le lettere nel codice del prodotto e i [GUID](guid.md) del codice del pacchetto devono essere tutti in maiuscolo.

## <a name="do-not-use-the-selfreg-and-typelib-tables"></a>Non usare le tabelle SelfReg e TypeLib.

-   Gli autori dei pacchetti di installazione si sconsigliano vivamente di usare la registrazione automatica e la tabella [selfreg](selfreg-table.md) . Devono invece registrare i moduli creando una o più tabelle nel [gruppo tabelle del registro di sistema](registry-tables-group.md). Molti dei vantaggi della Windows Installer vengono persi con la registrazione automatica perché le routine di registrazione automatica tendono a nascondere le informazioni di configurazione critiche. Per un elenco dei motivi per evitare la registrazione automatica, vedere [tabella SelfReg](selfreg-table.md).
-   Gli autori dei pacchetti di installazione si sconsigliano vivamente di utilizzare la tabella [typelib](typelib-table.md) . Anziché utilizzare la tabella TypeLib, registrare le librerie dei tipi utilizzando la tabella [del registro di sistema](registry-table.md) . Se un'installazione che utilizza la tabella TypeLib ha esito negativo ed è necessario eseguirne il rollback, è possibile che il rollback non ripristini il computer nello stesso stato esistente prima del rollback.

## <a name="provide-the-option-to-install-without-a-user-interface"></a>Consente di specificare l'opzione di installazione senza interfaccia utente.

Spesso gli amministratori preferiscono distribuire le applicazioni all'interno di un'azienda senza richiedere l'intervento dell'utente. È consigliabile consentire all'applicazione di fornire la possibilità di installare con il [livello di interfaccia utente](user-interface-levels.md) di nessuno.

-   Utilizzare le [proprietà pubbliche](public-properties.md) per le informazioni di configurazione. Gli amministratori possono fornire queste informazioni nella riga di comando.
-   Non richiedere che l'installazione dipenda dalle informazioni raccolte dall'interazione dell'utente con le finestre di dialogo. Queste informazioni non sono disponibili durante un'installazione invisibile all'utente.
-   Non riavviare automaticamente il computer dell'utente durante un'installazione invisibile all'utente.
-   Gli amministratori possono impostare il [livello di interfaccia utente](user-interface-levels.md) durante l'installazione di tramite l' [opzione della riga di comando](command-line-options.md) "/q". Il livello di interfaccia utente può essere impostato anche a livello di codice con una chiamata a [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).

## <a name="avoid-using-the-alwaysinstallelevated-policy"></a>Evitare di usare i criteri AlwaysInstallElevated.

Se il criterio [AlwaysInstallElevated](alwaysinstallelevated.md) non è impostato, le applicazioni non distribuite dall'amministratore vengono installate usando i privilegi dell'utente e solo le applicazioni gestite ottengono privilegi elevati. L'impostazione di questo criterio indica Windows Installer di utilizzare le autorizzazioni di sistema durante l'installazione dell'applicazione nel sistema. Questo metodo può aprire un computer a un rischio per la sicurezza, perché quando questo criterio è impostato, un utente non amministratore può eseguire installazioni con privilegi [*elevati*](e-gly.md) e accedere a posizioni sicure nel computer. È consigliabile usare un altro metodo rispetto ai criteri di AlwaysInstallElevated durante [l'installazione di un pacchetto con privilegi elevati per un non amministratore](installing-a-package-with-elevated-privileges-for-a-non-admin.md) o l' [applicazione di patch Per-User applicazioni gestite](patching-per-user-managed-applications.md).

## <a name="enable-the-disablemedia-policy-to-limit-unauthorized-installation"></a>Abilitare il criterio DisableMedia per limitare l'installazione non autorizzata.

Il criterio [DisableMedia](disablemedia.md) può impedire l'installazione di applicazioni non autorizzate. Quando questo criterio è abilitato, gli utenti e gli amministratori che eseguono un'installazione di manutenzione di un prodotto non possono utilizzare la finestra di dialogo Sfoglia per visualizzare le origini multimediali, ad esempio CD-ROM, per le origini di altri prodotti installabili. L'esplorazione di altri prodotti viene impedita indipendentemente dal fatto che l'installazione venga eseguita con privilegi elevati. È comunque possibile che l'utente reinstalli il prodotto da un supporto se l'utente dispone di un'origine multimediale correttamente etichettata.

## <a name="keep-the-original-package-source-files-secure-and-available-to-users"></a>Mantieni i file di origine del pacchetto originali protetti e disponibili per gli utenti.

In alcuni casi è possibile che l'origine originale del pacchetto di Windows Installer sia necessaria per l'installazione su richiesta, il ripristino o l'aggiornamento di un'applicazione. Se il programma di installazione non è in grado di individuare un'origine disponibile, all'utente viene richiesto di fornire supporti o di accedere a un percorso di rete contenente le origini necessarie. È consigliabile assicurarsi che il programma di installazione disponga delle origini necessarie senza richiedere l'intervento dell'utente.

-   Usare le [firme digitali e i file CAB esterni](digital-signatures-and-external-cabinet-files.md) per assicurarsi che le origini origial usate dal programma di installazione siano sicure. Un'immagine di origine non compressa archiviata in un percorso pubblico non è sicura.
-   Includere un elenco completo dei percorsi di origine della rete o dell'URL per il pacchetto di installazione dell'applicazione nella proprietà dell'elenco di [**origine**](sourcelist.md) .
-   Utilizzare una condivisione file system distribuito (DFS) per il percorso di origine.
-   Usare l'API Windows Installer per recuperare e modificare le informazioni dell'elenco di origine per Windows Installer le applicazioni e le patch. Per informazioni, vedere [gestione delle origini di installazione](managing-installation-sources.md).
-   Usare i metodi e le proprietà dell'oggetto del [**programma di installazione**](installer-object.md), dell'oggetto [**prodotto**](product-object.md)e dell' [**oggetto patch**](patch-object.md) per recuperare e modificare le informazioni dell'elenco di origine per Windows Installer le applicazioni e le patch.
-   Rispettare i punti elencati in [Impedisci a una patch di richiedere l'accesso ai punti di origine dell'installazione originale](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md) per ridurre al minimo la possibilità che la patch richieda l'accesso alle origini originali.
-   Archiviare i file di origine del pacchetto in un percorso che non sia la cartella temporanea del sistema. Windows Installer file di origine archiviati nella cartella temporanea possono risultare non disponibili per gli utenti.

## <a name="enable-verbose-logging-on-users-computer-when-troubleshooting-deployment"></a>Abilitare la registrazione dettagliata nel computer dell'utente durante la risoluzione dei problemi di distribuzione.

[Windows Installer registrazione](windows-installer-logging.md) include un'opzione di registrazione dettagliata che può essere abilitata nel computer di un utente. Le informazioni contenute in un log dettagliato possono risultare utili quando si tenta di risolvere i problemi Windows Installer distribuzione del pacchetto.

-   È possibile abilitare la registrazione dettagliata nel computer dell'utente usando le [Opzioni della riga di comando](command-line-options.md), la proprietà [**MsiLogging**](msilogging.md) , i [criteri di registrazione](logging.md), [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)e il metodo [**EnableLog**](installer-enablelog.md) .
-   Una risorsa molto utile per interpretare i file di log di Windows Installer è [Wilogutl.exe](wilogutl-exe.md). Questo strumento consente di analizzare i file di log e di visualizzare le soluzioni consigliate per gli errori rilevati in un file di log.
-   Per ulteriori informazioni sull'interpretazione dei file di log di Windows Installer, vedere la white paper disponibile sul sito TechNet: [Windows Installer: vantaggi e implementazione per gli amministratori di sistema](https://www.microsoft.com/technet/prodtechnol/windows2000serv/maintain/featusability/winmsi.mspx).
-   L'opzione di registrazione dettagliata deve essere utilizzata solo per finalità di risoluzione dei problemi e non deve essere lasciata in quanto può avere effetti negativi sulle prestazioni del sistema e sullo spazio su disco. Ogni volta che si utilizza lo strumento Installazione applicazioni nel pannello di controllo, viene creato un nuovo file.

## <a name="uninstallation-leaves-the-users-computer-in-a-clean-state"></a>La disinstallazione lascia il computer dell'utente in uno stato pulito.

La rimozione dell'applicazione è importante come l'installazione. Quando viene disinstallato un pacchetto di Windows Installer, non è necessario che nel computer dell'utente rimangano parti superflue.

-   Se un file che dovrebbe essere stato rimosso dal computer dell'utente rimane installato dopo l'esecuzione di una disinstallazione, il programma di installazione potrebbe non rimuovere il componente contenente il file per uno o più dei motivi descritti in [rimuovere i file bloccati](removing-stranded-files.md).
-   Se è necessario registrare un'applicazione, creare il pacchetto per rimuovere le informazioni del registro di sistema quando l'applicazione viene disinstallata. Per informazioni, vedere [aggiunta o rimozione di chiavi del registro di sistema durante l'installazione o la rimozione di componenti](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). Se un'applicazione non è registrata, l'applicazione non viene elencata nella funzionalità Installazione applicazioni nel pannello di controllo e non può essere gestita tramite il Windows Installer.
-   Per nascondere un'applicazione dalla funzionalità Installazione applicazioni nel pannello di controllo e comunque essere in grado di usare la Windows Installer per gestire l'applicazione, seguire le linee guida descritte in [aggiunta e rimozione di un'applicazione e senza lasciare traccia nel registro di sistema](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).
-   Le azioni personalizzate devono essere condizionate per l'esecuzione o non in base alle necessità alla disinstallazione. Potrebbe essere necessario eseguire azioni personalizzate diverse durante l'installazione e la disinstallazione.
-   Le informazioni di personalizzazione specifiche dell'utente possono essere archiviate in un file di testo nel computer. Questo ha il vantaggio di poter rimuovere il file quando viene disinstallata l'applicazione, anche se l'utente di questa personalizzazione non è attualmente connesso.

## <a name="test-packages-for-both-per-user-and-per-machine-installation-deployment"></a>Testare i pacchetti per la distribuzione dell'installazione per utente e per computer.

È consigliabile consentire ai clienti di decidere se distribuire un pacchetto per l'installazione nel [contesto di installazione](installation-context.md)per computer o per utente.

-   Valutare se l'applicazione deve essere disponibile solo per determinati utenti o per tutti gli utenti del computer durante il processo di sviluppo.
-   Verificare che il pacchetto funzioni correttamente sia per l'installazione per utente che per i contesti di installazione per computer.
-   Rendere il pacchetto facilmente personalizzabile e consentire ai clienti di decidere se distribuirlo per utente o per computer.

## <a name="plan-and-test-a-servicing-strategy-before-shipping-the-application"></a>Pianificare e testare una strategia di manutenzione prima di distribuire l'applicazione.

È necessario decidere come si intende eseguire la manutenzione dell'applicazione prima di distribuire l'applicazione per la prima volta.

-   Prendere in considerazione i tipi di aggiornamenti che si prevede di usare per il servizio dell'applicazione in futuro. Il Windows Installer fornisce tre tipi di aggiornamenti: [Small Update](small-updates.md), [aggiornamento secondario](minor-upgrades.md)e [aggiornamenti principali](major-upgrades.md). Le differenze tra questi argomenti sono descritte in applicazione di [patch e aggiornamenti](patching-and-upgrades.md) .
-   Prima di distribuire l'applicazione, verificare che funzioni come previsto dopo la manutenzione di ogni tipo di aggiornamento.

## <a name="reduce-the-dependency-of-updates-upon-the-original-sources"></a>Ridurre la dipendenza degli aggiornamenti sulle origini originali.

Se i file di origine originali sono necessari per aggiornare l'applicazione, questo può rendere più difficile la manutenzione dell'applicazione. I metodi seguenti consentono di ridurre la dipendenza degli aggiornamenti sulle origini originali.

-   Usare una [*patch Delta*](d-gly.md) per aggiornare le versioni di base dell'applicazione, ad esempio la versione RTM e le versioni Service Pack. Seguire le linee guida per l'uso delle patch Delta descritte nell'argomento: [riduzione delle dimensioni delle patch](reducing-patch-size.md).
-   Seguire i consigli elencati nell'argomento: [impedire a una patch di richiedere l'accesso all'origine dell'installazione originale](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

## <a name="do-not-distribute-unserviceable-merge-modules"></a>Non distribuire i moduli merge non collegabili.

Le applicazioni non devono dipendere da [moduli merge](merge-modules.md) per l'installazione del componente se il proprietario del modulo merge e il proprietario dell'applicazione sono diversi. Questo può rendere difficile il servizio dell'applicazione perché entrambi i proprietari devono coordinarsi per aggiornare l'applicazione o il modulo. Senza conoscere tutte le applicazioni che hanno utilizzato il modulo merge, il proprietario dell'applicazione non è in grado di aggiornare il modulo merge senza rischiare che l'aggiornamento potrebbe non essere compatibile con un'altra applicazione. Il proprietario del modulo merge non dispone di un metodo diretto per l'aggiornamento di Windows Installer pacchetti in cui è già installato il modulo merge.

-   È consigliabile fornire i componenti necessari agli utenti come un'altra Windows Installer installazione.

## <a name="avoid-patching-administrative-installations"></a>Evitare l'applicazione di patch alle installazioni amministrative.

Fornire in rete un' [installazione amministrativa](administrative-installation.md) del pacchetto di Windows Installer originale dell'applicazione per consentire ai membri di un gruppo di lavoro di installare l'applicazione. Gli utenti di questa immagine amministrativa dovranno quindi applicare gli aggiornamenti all'istanza locale dell'applicazione presente nel computer. In questo modo gli utenti vengono sincronizzati con l'immagine amministrativa. Non è consigliabile applicare gli aggiornamenti all'installazione amministrativa per i motivi seguenti.

-   Le dimensioni e la latenza del download necessarie per gli utenti per ottenere un aggiornamento vengono aumentate rispetto al download di una patch. L'intero pacchetto di Windows Installer aggiornato e i file di origine devono essere scaricati, rimemorizzati nella cache e reinstallati.
-   Gli utenti non sono in grado di eseguire l' [installazione su richiesta](installation-on-demand.md) e di ripristinare le applicazioni da un'installazione amministrativa aggiornata finché non rimemorizzano nella cache e reinstalla l'applicazione.
-   L'applicazione di una patch a un'installazione amministrativa rimuove la firma digitale dal pacchetto. Un amministratore deve firmare nuovamente il pacchetto. Per altre informazioni sull'uso delle firme digitali, vedere [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md).
-   Molte patch binarie sono destinate all'immagine RTM dell'applicazione e richiedono una versione precedente del file. L'istanza locale di un'applicazione installata da un'installazione amministrativa aggiornata potrebbe non funzionare con altri aggiornamenti. Molte applicazioni di patch binarie possono avere esito negativo.
-   Se si applica una patch a un'installazione amministrativa, i file di origine e il file con estensione msi non vengono contrassegnati con le informazioni sull'aggiornamento. Gli utenti non possono determinare quali aggiornamenti sono stati ricevuti dall'installazione amministrativa. Ciò rende impossibile sequenziare gli aggiornamenti applicati sul lato utente con quelli già applicati sul lato dell'immagine amministrativa.
-   Le patch applicate a un'installazione amministrativa non sono [patch disinstallabili](uninstallable-patches.md). Ciò può impedire che il codice del pacchetto memorizzato nella cache del computer dell'utente diventi diverso dal codice del pacchetto nell'installazione amministrativa. Se il codice del pacchetto memorizzato nella cache nel computer dell'utente è diverso da quello dell'installazione amministrativa, reinstallare l'applicazione dall'installazione amministrativa, quindi applicare una patch al computer client.
-   Se si decide di applicare piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa, attenersi alle linee guida descritte nell'argomento relativo all' [applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md).

## <a name="register-updates-to-run-with-elevated-privilege"></a>Registrare gli aggiornamenti da eseguire con privilegi elevati.

A partire da Windows Installer 3,0, è possibile applicare patch a un'applicazione installata in un contesto gestito per utente, dopo che la patch è stata registrata con privilegi elevati. Non è possibile applicare patch alle applicazioni installate in un contesto gestito per utente usando versioni di Windows Installer precedenti alla versione 3,0.

-   Usare il metodo [**SourceListAddSource**](patch-sourcelistaddsource.md) o la funzione [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) per registrare un pacchetto di patch con privilegi elevati. Seguire le linee guida ed esempi disponibili in [applicazione di patch Per-User applicazioni gestite](patching-per-user-managed-applications.md).
-   Quando si esegue Windows Installer versione 4,0 in Windows Vista, è anche possibile usare l'applicazione di patch per il [controllo dell'account utente](user-account-control--uac--patching.md) per consentire agli autori di Windows Installer installazioni di identificare le patch firmate digitalmente che possono essere applicate in futuro da utenti non amministratori. Questa operazione è disponibile solo con l'installazione dei pacchetti nel [contesto di installazione](installation-context.md) per computer (ALLUSERS = 1).
-   Verificare che l'applicazione di patch con privilegi minimi non sia stata disabilitata impostando la proprietà [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) o il criterio [DisableLUAPatching](disableluapatching.md) .

## <a name="use-the-msipatchsequence-table-to-sequence-patches"></a>Usare la tabella MsiPatchSequence per sequenziare le patch.

Includere una [tabella MsiPatchSequence](msipatchsequence-table.md) nel pacchetto e aggiungere le informazioni di sequenziazione delle patch. A partire da Windows Installer versione 3,0, il programma di installazione può usare la tabella MsiPatchSequence quando si [installano più patch](installing-multiple-patches.md) per determinare la sequenza di applicazione patch migliore. Usare le linee guida descritte in [sequenziazione della patch in Windows Installer versione 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3) white paper per la definizione delle famiglie di patch.

-   Se lo si desidera, specificare tutte le patch come appartenenti a una singola famiglia di patch. In molti casi, una singola famiglia di patch offre una flessibilità sufficiente per la sequenziazione delle patch. La complessità della creazione aumenta quando vengono utilizzate più famiglie di patch. Assegnare un nome significativo alla famiglia di patch e assegnare i valori di sequenza in tale famiglia di patch che aumentano nel tempo. Per applicare le patch nell'ordine in cui sono state rilasciate, seguire l'esempio di applicazione di [patch multipli](multiple-patching-example.md) .
-   Usare la [tabella PatchSequence](patchsequence-table--patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md) per generare le informazioni nella [tabella MsiPatchSequence](msipatchsequence-table.md). La versione di PATCHWIZ.DLL rilasciata con Windows Installer 3,0 può generare automaticamente informazioni di sequenziazione delle patch. Per ulteriori informazioni su come aggiungere una nuova patch, vedere [generazione di informazioni sulla sequenza di patch](generating-patch-sequence-information---patchwiz-dll-.md). Per ulteriori informazioni sugli scenari di sequenziazione delle patch, vedere il white paper sulla [sequenziazione delle patch nella Windows Installer versione 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3).

## <a name="test-the-installation-package-thoroughly"></a>Testare accuratamente il pacchetto di installazione.

Verificare la corretta installazione, ripristino e rimozione del pacchetto di Windows Installer. È possibile dividere il processo di test nelle parti seguenti.

-   Test dell'installazione: testare l'installazione con tutte le possibili combinazioni di funzionalità dell'applicazione. Testare tutti i tipi di installazione, tra cui l'installazione [amministrativa](administrative-installation.md), l' [installazione di rollback](rollback-installation.md)e l' [installazione su richiesta](installation-on-demand.md). Provare tutti i possibili metodi di installazione, incluso il file con estensione msi, le [Opzioni della riga di comando](command-line-options.md)e l'installazione dal pannello di controllo. Verificare che il pacchetto possa essere installato dagli utenti in tutti i possibili contesti dei privilegi. Provare a installare il pacchetto dopo che è stato distribuito con tutti i metodi possibili. Abilitare la [registrazione Windows Installer](windows-installer-logging.md) per ogni test e risolvere tutti gli errori rilevati nel log del programma di installazione e nel registro eventi.
-   Test dell'interfaccia utente: testare il pacchetto quando viene installato con tutti i [livelli di interfaccia utente](user-interface-levels.md)possibili. Testare il pacchetto installato senza interfaccia utente e con tutte le informazioni fornite tramite l'interfaccia utente. Verificare l' [accessibilità](accessibility.md) dell'interfaccia utente e che l'interfaccia utente funzioni come previsto per diverse risoluzioni dello schermo e dimensioni dei tipi di carattere.
-   Test di manutenzione e riparazione: verificare che il pacchetto sia in grado di gestire l'applicazione di [patch e gli aggiornamenti](patching-and-upgrades.md) forniti da un [piccolo aggiornamento](small-updates.md), dall' [aggiornamento secondario](minor-upgrades.md)e dagli [aggiornamenti principali](major-upgrades.md). Prima di distribuire il pacchetto, scrivere un aggiornamento di valutazione di ogni tipo e provare ad applicarlo al pacchetto originale.
-   Test di disinstallazione: verificare che, quando il pacchetto viene rimosso, non rimanga inutile parte del computer dell'utente e che siano state rimosse solo le informazioni appartenenti al pacchetto. Riavviare il computer di test dopo aver disinstallato il pacchetto e verificare l'integrità degli strumenti di sistema comuni e di altre applicazioni standard. Verificare che il pacchetto possa essere rimosso dagli utenti in tutti i possibili contesti dei privilegi. Testare tutti i metodi per rimuovere il pacchetto, fare clic sul file con estensione msi, provare a usare le [Opzioni della riga di comando](command-line-options.md)e provare a rimuovere il pacchetto dal pannello di controllo. Abilitare la [registrazione Windows Installer](windows-installer-logging.md) per ogni test e risolvere tutti gli errori rilevati nel log del programma di installazione e nel registro eventi.
-   Test delle funzionalità del prodotto: assicurarsi che l'applicazione funzioni come previsto dopo l'installazione, il ripristino o la rimozione del pacchetto.

## <a name="fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package"></a>Correggere tutti gli errori di convalida prima di distribuire un pacchetto di installazione nuovo o modificato.

Eseguire la [convalida del pacchetto](package-validation.md) in un pacchetto di Windows Installer nuovo o rivisto prima di provare a installarlo per la prima volta. La convalida controlla il database Windows Installer per la creazione di errori. Il tentativo di installare un pacchetto che non supera la convalida può danneggiare il sistema dell'utente.

-   È possibile convalidare il pacchetto usando [Orca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md). Entrambi gli strumenti sono forniti con il Windows SDK. I fornitori di terze parti possono anche incorporare il sistema di convalida del ghiaccio nell'ambiente di creazione.
-   È possibile usare il set standard di [analizzatori di coerenza interni](internal-consistency-evaluators-ices.md) , ovvero i ghiacci inclusi nei file con estensione cub forniti con l'SDK, oppure personalizzare la convalida compilando [un ghiaccio](building-an-ice.md) e aggiungendolo al file con estensione cub.
-   È possibile utilizzare il Evalcom2.dll per implementare l' [automazione di convalida](validation-automation.md) per i pacchetti di installazione e i moduli unione.

## <a name="author-a-secure-installation"></a>Creare un'installazione sicura.

Seguendo queste linee guida durante lo sviluppo del pacchetto per mantenere un ambiente protetto durante l'installazione.

-   [Linee guida per la creazione di installazioni sicure](guidelines-for-authoring-secure-installations.md)
-   [Linee guida per la protezione dei pacchetti nei computer bloccati](guidelines-for-securing-packages-on-locked-down-computers.md)
-   [Linee guida per la protezione di azioni personalizzate](guidelines-for-securing-custom-actions.md)

## <a name="use-pmsihandle-instead-of-handle"></a>USA PMSIHANDLE anziché HANDLE

Le variabili di tipo **PMSIHANDLE** sono definite in MSI. h. È consigliabile che l'applicazione usi il tipo **PMSIHANDLE** perché il programma di installazione chiude gli oggetti **PMSIHANDLE** quando escono dall'ambito, mentre l'applicazione deve chiudere gli oggetti **MSIHANDLE** chiamando [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).

Ad esempio, se si usa codice simile al seguente:

``` syntax
MSIHANDLE hRec = MsiCreateRecord(3);
```

Modificarla in:

``` syntax
PMSIHANDLE hRec = MsiCreateRecord(3);
```

 

 
