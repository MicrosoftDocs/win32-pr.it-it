---
description: Windows Il programma di installazione è la soluzione consigliata per l'installazione e la configurazione di applicazioni Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Guida basata sui ruoli alla documentazione Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f886050f3bb0256f6f0f993e613be940cee9cd2fe748b2d17b5dc0f0f84a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625863"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a>Guida basata sui ruoli alla documentazione Windows Installer

Windows Il programma di installazione è la soluzione consigliata per l'installazione e la configurazione di applicazioni Windows. Di conseguenza, alcune delle informazioni contenute in questo SDK saranno di interesse per un'ampia gamma di professionisti IT e di sviluppo software. Questa sezione viene fornita come guida ai lettori che preferiscono visualizzare collegamenti ad argomenti organizzati in base al ruolo professionale e agli scenari di attività comuni. Poiché i ruoli possono differire notevolmente tra le organizzazioni, il raggruppamento seguente deve essere considerato solo come guida per una posizione in cui iniziare a cercare le informazioni necessarie.

-   [Sviluppatori di applicazioni](#application-developers)
-   [Autori dell'installazione](#setup-authors)
-   [Professionisti IT](#it-professionals)
-   [Sviluppatori di infrastrutture](#infrastructure-developers)

Questa documentazione è destinata agli sviluppatori di software che vogliono creare applicazioni che usano Windows programma di installazione. Come origine principale del materiale di riferimento per il programma di installazione, l'SDK fornisce informazioni sui pacchetti di installazione e sul servizio di installazione. Contiene descrizioni complete dell'API (Application Programming Interface) e degli elementi del database del programma di installazione.

Per altre informazioni, vedere [Other Sources of Windows Installer Information](other-sources-of-windows-installer-information.md).

## <a name="application-developers"></a>Sviluppatori di applicazioni

Gli sviluppatori di applicazioni creano applicazioni che chiamano l'Windows di programmazione dell'applicazione del programma di installazione di Windows e installano Windows di installazione in fase di esecuzione. Il Windows di installazione può funzionare in un'applicazione, ad esempio la riparazione automatica e l'installazione su richiesta. In genere, gli sviluppatori di applicazioni ese verificano quanto segue:

-   Abilitare l'installazione su richiesta delle applicazioni in fase di esecuzione dall'interno di un'altra applicazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Uso delle funzioni del programma di installazione](using-installer-functions.md)
    -   [Informazioni di riferimento sulla funzione Installer](installer-function-reference.md)
    -   [Installazione su richiesta](installation-on-demand.md)
    -   [Gestione dei componenti](component-management.md)
    -   [Modifica dei tasti di scelta rapida del programma di installazione](editing-installer-shortcuts.md)
    -   [**Proprietà OLEAdvtSupport**](oleadvtsupport.md)
    -   [Supporto della piattaforma di annunci pubblicitari](platform-support-of-advertisement.md)

-   Abilitare il ripristino automatico delle applicazioni reinstallando i componenti in base alle esigenze in fase di esecuzione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Uso delle funzioni del programma di installazione](using-installer-functions.md)
    -   [Informazioni di riferimento sulla funzione Installer](installer-function-reference.md)
    -   [Resilienza](resiliency.md)
    -   [Resilienza di origine](source-resiliency.md)
    -   [Ricerca di una funzionalità o di un componente interrotto](searching-for-a-broken-feature-or-component.md)
    -   [Sostituzione di file esistenti](replacing-existing-files.md)

-   Visualizzare un'interfaccia utente per raccogliere informazioni utente e preferenze di configurazione la prima volta che un'applicazione viene installata o eseguita. L'interfaccia utente deve essere aggiunta dall'autore del programma di installazione Windows programma di installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Uso delle funzioni del programma di installazione](using-installer-functions.md)
    -   [Inizializzazione di un'applicazione](initializing-an-application.md)
    -   [Finestra di dialogo FirstRun](firstrun-dialog.md)
    -   [Informazioni sul Interfaccia utente](about-the-user-interface.md)

-   Creare applicazioni che usano un modello di riferimento indiretto per fare riferimento a componenti con funzionalità parallele. Le categorie di componenti qualificate devono essere aggiunte dall'autore del programma di installazione Windows programma di installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Componenti qualificati](qualified-components.md)
    -   [Uso di componenti qualificati](using-qualified-components.md)

-   Usare assembly privati e side-by-side per isolare le applicazioni e ridurre i conflitti di DLL.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Assembly](assemblies.md)
    -   [Chiavi del Registro di sistema degli assembly scritte Windows programma di installazione](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Installazione di assembly Win32 per la condivisione side-by-side in Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [Installazione di assembly Win32 per l'uso privato di un'applicazione in Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [Tabella MsiAssembly](msiassembly-table.md)
    -   [Tabella MsiAssemblyName](msiassemblyname-table.md)
    -   [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [**Proprietà MsiWin32AssemblySupport**](msiwin32assemblysupport.md)
    -   [**Proprietà MsiNetAssemblySupport**](msinetassemblysupport.md)
    -   [**Componenti isolati**](isolated-components.md)

-   Preparare l'applicazione per installare i propri aggiornamenti principali completi.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Applicazione di patch e aggiornamenti](patching-and-upgrades.md)
    -   [Aggiornamenti principali](major-upgrades.md)
    -   [**Proprietà UpgradeCode**](upgradecode.md)
    -   [**Uso di UpgradeCode**](using-an-upgradecode.md)
    -   [Impedire l'installazione di un pacchetto precedente in una versione più recente](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   Preparare l'applicazione per l'installazione di aggiornamenti secondari, aggiornamenti di piccole dimensioni o correzioni.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Applicazione di patch e aggiornamenti](patching-and-upgrades.md)
    -   [Aggiornamenti di piccole dimensioni](small-updates.md)
    -   [Aggiornamenti secondari](minor-upgrades.md)

-   Organizzare le risorse dell'applicazione in componenti che possono essere Windows programma di installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Windows Componenti del programma di installazione](windows-installer-components.md)
    -   [Uso di funzionalità e componenti](working-with-features-and-components.md)
    -   [Uso di componenti transitivi](using-transitive-components.md)
    -   [Cosa accade se le regole del componente vengono interrotte?](what-happens-if-the-component-rules-are-broken.md)
    -   [Organizzazione delle applicazioni in componenti](organizing-applications-into-components.md)
    -   [Componenti isolati](isolated-components.md)
    -   [Componenti qualificati](qualified-components.md)

## <a name="setup-authors"></a>Autori dell'installazione

Gli autori del programma di Windows creano pacchetti di .msi (file di installazione) che contengono la logica di installazione e le informazioni necessarie per installare un'applicazione. In genere usano strumenti di creazione, ad esempio [Orca.exe](orca-exe.md) per popolare il database Windows Installer con la logica di installazione e le informazioni. In genere, gli autori del programma di installazione ese verificano quanto segue:

-   Determinare la funzionalità disponibile con diverse versioni Windows programma di installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Determinazione della versione Windows installer](determining-the-windows-installer-version.md)
    -   [Versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md)
    -   [Novità del programma di installazione Windows](what-s-new-in-windows-installer.md)

-   Organizzare le risorse dell'applicazione in Windows del programma di installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Windows Componenti del programma di installazione](windows-installer-components.md)
    -   [Organizzazione delle applicazioni in componenti](organizing-applications-into-components.md)
    -   [Modifica del codice del componente](changing-the-component-code.md)
    -   [Cosa accade se le regole del componente vengono interrotte?](what-happens-if-the-component-rules-are-broken.md)
    -   [Windows Esempi di programma di installazione](windows-installer-examples.md)

-   Usare strumenti SDK o strumenti SDK di Windows installer di terze parti, ad esempio [Orca.exe,](orca-exe.md) per popolare un database di installazione e creare un pacchetto Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
    -   [Pacchetto di installazione, Informazioni sul database del programma di installazione](installation-package.md)
    -   [Windows Estensioni di file del programma di installazione](windows-installer-file-extensions.md)
    -   [Tabelle di database](database-tables.md)
    -   [Codici dei pacchetti](package-codes.md)
    -   [Creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md)
    -   [Windows Programma di installazione nei sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md)
    -   [Denominazione di tabelle, proprietà e azioni personalizzate](naming-custom-tables-properties-and-actions.md)
    -   [Limitazioni OLE in Flussi](ole-limitations-on-streams.md)
    -   [Formato definizione colonna](column-definition-format.md)
    -   [Riduzione delle dimensioni di un file .msi](reducing-the-size-of-an--msi-file.md)

-   Creare il database Windows Installer per installare i file.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Gruppo tabelle principali](core-tables-group.md)
    -   [File Tables Group](file-tables-group.md)
    -   [Tabella file](file-table.md)
    -   [Ricerca file](file-searching.md)
    -   [Determinazione dei costi dei file](file-costing.md)
    -   [Installazione di file](file-installation.md)
    -   [File complementari](companion-files.md)
    -   [Regole di controllo delle versioni dei file](file-versioning-rules.md)
    -   [Controllo delle versioni dei file predefinito](default-file-versioning.md)
    -   [Sostituzione di file esistenti](replacing-existing-files.md)
    -   [Uso di file CAB e origini compresse](using-cabinets-and-compressed-sources.md)
    -   [Rimozione di file non crittografati](removing-stranded-files.md)
    -   [Installazione di componenti permanenti, file, tipi di carattere, chiavi del Registro di sistema](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Tabella FileSFPCatalog](filesfpcatalog-table.md)
    -   [Ricerca di un file e creazione di una proprietà contenente il percorso del file](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [Ricerca di una directory e di un file nella directory](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [Windows Esempi di programma di installazione](windows-installer-examples.md)

-   Creare un database Windows Installer che installa una struttura di directory e cartelle.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Gruppo tabelle principali](core-tables-group.md)
    -   [File Tables Group](file-tables-group.md)
    -   [Tabella dei componenti](component-table.md)
    -   [Tabella directory](directory-table.md)
    -   [Uso della tabella directory](using-the-directory-table.md)
    -   [Uso di una proprietà directory in un percorso](using-a-directory-property-in-a-path.md)
    -   [Proprietà cartella di sistema](property-reference.md)
    -   [Tabella CreateFolder](createfolder-table.md)
    -   [Tabella LockPermissions](lockpermissions-table.md)
    -   [Tabella MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [Modifica del percorso di destinazione per una directory](changing-the-target-location-for-a-directory.md)
    -   [Windows Esempi di programma di installazione](windows-installer-examples.md)

-   Creare un database Windows Installer che installa le chiavi del Registro di sistema.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Gruppo tabelle principali](core-tables-group.md)
    -   [Gruppo tabelle del Registro di sistema](registry-tables-group.md)
    -   [Tabella del Registro di sistema](registry-table.md)
    -   [Modifica del Registro di sistema](modifying-the-registry.md)
    -   [Aggiunta o rimozione di chiavi del Registro di sistema durante l'installazione o la rimozione di componenti](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [Aggiunta e rimozione di un'applicazione senza lasciare traccia nel Registro di sistema](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Installazione di componenti permanenti, file, tipi di carattere, chiavi del Registro di sistema](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Ricerca di applicazioni, file, voci del Registro di sistema o .ini file esistenti](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [Ricerca di una voce del Registro di sistema e creazione di una proprietà contenente il valore del Registro di sistema](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [Chiavi del Registro di sistema degli assembly scritte dal programma Windows installazione](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Disinstallare la chiave del Registro di sistema](uninstall-registry-key.md)
    -   [Tabella SelfReg](selfreg-table.md)
    -   [Specifica dell'ordine di registrazione automatica](specifying-the-order-of-self-registration.md)
    -   [Windows Esempi di programma di installazione](windows-installer-examples.md)

-   Creare un database Windows Installer per l'installazione dei servizi.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella ServiceInstall](serviceinstall-table.md)
    -   [Tabella ServiceControl](servicecontrol-table.md)
    -   [Tabella dei componenti](component-table.md)

-   Creare un database Windows Installer che installa componenti isolati o componenti COM.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Gruppo tabelle del Registro di sistema](registry-tables-group.md)
    -   [Tabella delle classi](class-table.md)
    -   [Tabella Complus](complus-table.md)
    -   [Componenti isolati](isolated-components.md)
    -   [Uso di componenti isolati](using-isolated-components.md)
    -   [Installazione di componenti isolati](installation-of-isolated-components.md)
    -   [Reinstallazione di componenti isolati](reinstallation-of-isolated-components.md)
    -   [Rimozione di componenti isolati](removal-of-isolated-components.md)
    -   [Installazione di un componente COM in una posizione privata](installing-a-com-component-to-a-private-location.md)
    -   [Rendere privato un componente COM in un pacchetto esistente](make-a-com-component-in-an-existing-package-private.md)
    -   [Installazione di un'applicazione COM+ con il programma Windows installazione](installing-a-com--application-with-the-windows-installer.md)
    -   [Installazione di un componente non COM in un percorso privato](installing-a-non-com-component-to-a-private-location.md)
    -   [Rendere privato un componente non COM in un pacchetto esistente](make-a-non-com-component-in-an-existing-package-private.md)

-   Creare un database Windows Installer che installa gli assembly.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella MsiAssembly](msiassembly-table.md)
    -   [Tabella MsiAssemblyName](msiassemblyname-table.md)
    -   [Assembly](assemblies.md)
    -   [Chiavi del Registro di sistema degli assembly scritte dal programma Windows installazione](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Installazione di assembly Win32](installation-of-win32-assemblies.md)

-   Creare un database Windows Installer che installa driver e convertitori ODBC.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella ODBCAttribute](odbcattribute-table.md)
    -   [Tabella ODBCDriver](odbcdriver-table.md)
    -   [Tabella ODBCTranslator](odbctranslator-table.md)
    -   [Tabella ODBCDataSource](odbcdatasource-table.md)
    -   [Tabella ODBCSourceAttribute](odbcsourceattribute-table.md)

-   Creare un database Windows Installer che installa MIME.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella MIME](mime-table.md)
    -   [Tabella delle estensioni](extension-table.md)
    -   [Modifica del Registro di sistema](modifying-the-registry.md)

-   Creare un database Windows Installer che installa le variabili di ambiente.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella dell'ambiente](environment-table.md)

-   Creare un database Windows installer che installa i collegamenti.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella dei collegamenti](shortcut-table.md)
    -   [Tabella MsiShortcutProperty](msishortcutproperty-table.md)
    -   [Modifica dei tasti di scelta rapida del programma di installazione](editing-installer-shortcuts.md)
    -   [Windows Esempi di programma di installazione](windows-installer-examples.md)

-   Creare un Windows del programma di installazione che installa più istanze di applicazioni.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md)
    -   [Creazione di più istanze con trasformazioni di istanza](authoring-multiple-instances-with-instance-transforms.md)
    -   [Installazione di più istanze con trasformazioni di istanza](installing-multiple-instances-with-instance-transforms.md)

-   Specificare le opzioni e gli stati di selezione delle funzionalità predefiniti.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Gruppo tabelle principali](core-tables-group.md)
    -   [Tabella dei componenti](component-table.md)
    -   [Tabella delle funzionalità](feature-table.md)
    -   [Tabella FeatureComponents](featurecomponents-table.md)
    -   [Controllo degli stati di selezione delle funzionalità](controlling-feature-selection-states.md)
    -   [Proprietà delle opzioni di installazione delle funzionalità](property-reference.md)

-   Specificare le condizioni che devono essere soddisfatte per installare un'applicazione o componenti selezionati.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella delle condizioni](condition-table.md)
    -   [Tabella LaunchCondition](launchcondition-table.md)
    -   [Tabella dei componenti](component-table.md)
    -   [Uso delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md)
    -   [Sintassi di istruzioni condizionali](conditional-statement-syntax.md)
    -   [Azioni di condizionamento da eseguire durante la rimozione](conditioning-actions-to-run-during-removal.md)
    -   [Esempi di sintassi di istruzioni condizionali](examples-of-conditional-statement-syntax.md)

-   Creare la sequenza di azioni usate per installare l'applicazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Uso di una tabella di sequenza](using-a-sequence-table.md)
    -   [Gruppo tabelle procedura di installazione](installation-procedure-tables-group.md)
    -   [Esempio dettagliato della tabella sequence](sequence-table-detailed-example.md)
    -   [Azioni con restrizioni di sequenziazione](actions-with-sequencing-restrictions.md)
    -   [Azioni senza restrizioni di sequenziazione](actions-without-sequencing-restrictions.md)
    -   [Uso delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md)
    -   [Sintassi di istruzioni condizionali](conditional-statement-syntax.md)
    -   [Esempi di sintassi di istruzioni condizionali](examples-of-conditional-statement-syntax.md)
    -   [Azioni di condizionamento da eseguire durante la rimozione](conditioning-actions-to-run-during-removal.md)
    -   [Azioni standard](standard-actions.md)
    -   [Windows Esempi di programma di installazione](windows-installer-examples.md)

-   Preparare il pacchetto di installazione dell'applicazione per gli aggiornamenti futuri dell'applicazione tramite il Windows installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Applicazione di patch e aggiornamenti](patching-and-upgrades.md)
    -   [Preparazione di un'applicazione per futuri aggiornamenti principali](preparing-an-application-for-future-major-upgrades.md)
    -   [Uso di un codice di aggiornamento](using-an-upgradecode.md)
    -   [Aggiornare la tabella](upgrade-table.md)
    -   [**Proprietà UpgradeCode**](upgradecode.md)
    -   [Impedire l'installazione di un pacchetto precedente in una versione più recente](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [Modifica del codice prodotto](changing-the-product-code.md)
    -   [Aggiornamento degli assembly](updating-assemblies.md)
    -   [Windows Esempi di programma di installazione](windows-installer-examples.md)

-   Risolvere i Windows pacchetti del programma di installazione in fase di sviluppo.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Convalida dei pacchetti](package-validation.md)
    -   [Analizzatori di coerenza interna - ICE](internal-consistency-evaluators-ices.md)
    -   [Windows Registrazione del programma di installazione](windows-installer-logging.md)
    -   [Controllo dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md)
    -   [Creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
    -   [Convalida dei moduli unione](validating-merge-modules.md)
    -   [Convalida di un database di installazione](validating-an-installation-database.md)
    -   [Convalida di un aggiornamento dell'installazione](validating-an-installation-upgrade.md)
    -   [Ricerca di una funzionalità o di un componente interrotto](searching-for-a-broken-feature-or-component.md)
    -   [Windows Messaggi di errore del programma di installazione](windows-installer-error-messages.md)
    -   [Registrazione delle richieste di riavvio](logging-of-reboot-requests.md)

-   Assicurarsi una configurazione e un'installazione sicure dell'applicazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Linee guida per la creazione di installazioni sicure](guidelines-for-authoring-secure-installations.md)
    -   [Linee guida per la protezione delle azioni personalizzate](guidelines-for-securing-custom-actions.md)
    -   [Sicurezza delle azioni personalizzate](custom-action-security.md)
    -   [Linee guida per la protezione dei pacchetti nei computer bloccati](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [Creazione di un'installazione firmata completamente verificata tramite Automazione](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [Esempio di installazione di Windows Installer basata su Windows](a-url-based-windows-installer-installation-example.md)
    -   [Creazione del Interfaccia utente per l'input della password](authoring-the-user-interface-for-password-input.md)
    -   [Firme digitali e programma di Windows di installazione](digital-signatures-and-windows-installer.md)
    -   [Uso del Windows installer con Controllo dell'account utente](using-windows-installer-with-uac.md)
    -   [Applicazione di patch al controllo dell'account utente](user-account-control--uac--patching.md)
    -   [Msicert.exe](msicert-exe.md)
    -   [**AdminUser - proprietà**](adminuser.md)
    -   [**Proprietà con privilegi**](privileged.md)
    -   [**SecureCustomProperties - proprietà**](securecustomproperties.md)

-   Creare un'interfaccia utente per presentare le opzioni per configurare l'installazione e ottenere informazioni dall'utente sul processo di installazione in sospeso.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Informazioni sulla Interfaccia utente](about-the-user-interface.md)
    -   [Aggiunta di controlli e testo](adding-controls-and-text.md)
    -   [Creazione di un controllo ProgressBar](authoring-a-progressbar-control.md)
    -   [Creazione di messaggi di richiesta su disco](authoring-disk-prompt-messages.md)
    -   [Creazione di un'istruzione condizionale "Please Wait . . ". Finestra di messaggio](authoring-a-conditional-please-wait-------message-box.md)
    -   [Anteprima del Interfaccia utente](previewing-the-user-interface.md)
    -   [Aggiunta di testo archiviato in una proprietà](adding-text-stored-in-a-property.md)
    -   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   Creare un'interfaccia utente esterna per presentare un'interfaccia utente personalizzata per configurare l'installazione e ottenere informazioni dall'utente sul processo di installazione in sospeso.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [Monitoraggio di un'installazione tramite MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [Analisi dei Windows del programma di installazione](parsing-windows-installer-messages.md)
    -   [Restituzione di valori da un gestore Interfaccia utente esterno](returning-values-from-an-external-user-interface-handler.md)
    -   [GESTORE \_ INSTALLUI](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [Gestione dei messaggi di stato tramite MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md)
    -   [Monitoraggio di un'installazione tramite MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md)

-   Impostare le informazioni per l'applicazione in **Installazione applicazioni** (ARP).

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Configurazione di Installazione applicazioni con il programma Windows installazione](configuring-add-remove-programs-with-windows-installer.md)
    -   [Aggiunta e rimozione di un'applicazione senza lasciare traccia nel Registro di sistema](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Disinstallare la chiave del Registro di sistema](uninstall-registry-key.md)

-   Scrivere azioni personalizzate per gestire la logica di installazione non supportata in modo nativo da Windows programma di installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Azioni personalizzate](custom-actions.md)
    -   [Elenco di riepilogo di tutti i tipi di azione personalizzati](summary-list-of-all-custom-action-types.md)
    -   [Linee guida per la protezione delle azioni personalizzate](guidelines-for-securing-custom-actions.md)
    -   [Informazioni di riferimento su azioni personalizzate](custom-action-reference.md)
    -   [Uso di un'azione personalizzata per creare account utente in un computer locale](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [Uso di un'azione personalizzata per avviare un file installato al termine dell'installazione](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [Accesso a un database o a una sessione dall'interno di un'azione personalizzata](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [Accesso alla sessione del programma di installazione corrente dall'interno di un'azione personalizzata](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [Modifica dello stato del sistema tramite un'azione personalizzata](changing-the-system-state-using-a-custom-action.md)

-   Avviare il Windows di installazione nel computer di un utente.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Bootstrap](bootstrapping.md)
    -   [Instmsi.exe](instmsi-exe.md)
    -   [Bootstrap di download Internet](internet-download-bootstrapping.md)
    -   [Msistuff.exe](msistuff-exe.md)
    -   [Esempio di installazione di Windows Installer basata su Windows](a-url-based-windows-installer-installation-example.md)
    -   [Configurazione delle risorse Setup.exe](configuring-the-setup-exe-resources.md)
    -   [Download di un'installazione da Internet](downloading-an-installation-from-the-internet.md)

-   Attenersi alle Active Accessibility quando si scrivono Windows di installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Accessibilità](accessibility.md)

-   Prepararsi per l'internazionalizzazione della configurazione di un'applicazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Preparazione di un Windows installer per la localizzazione,](preparing-a-windows-installer-package-for-localization.md)
    -   [Localizzazione di un pacchetto Windows Installer](localizing-a-windows-installer-package.md)
    -   [Gestione della tabella codici (programma Windows di installazione)](code-page-handling-windows-installer-.md)
    -   [Aggiunta di risorse localizzate](adding-localized-resources.md)
    -   [Esempio di localizzazione](a-localization-example.md)
    -   [Localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md)
    -   [Localizzazione di colonne di database](localizing-database-columns.md)
    -   [Creazione di un database con una tabella codici neutra](creating-a-database-with-a-neutral-code-page.md)
    -   [Gestione delle tabelle codici delle tabelle importate ed esportate](code-page-handling-of-imported-and-exported-tables.md)
    -   [Localizzazione della lingua visualizzata dalle finestre di dialogo](localizing-the-language-displayed-by-dialogs.md)
    -   [Importazione di tabelle Error e ActionText localizzate](importing-localized-error-and-actiontext-tables.md)
    -   [Aggiornamento delle proprietà ProductLanguage e ProductCode](updating-productlanguage-and-productcode-properties.md)
    -   [Aggiornamento di un flusso di informazioni di riepilogo](updating-a-summary-information-stream.md)
    -   [Componenti qualificati](qualified-components.md)
    -   [Tabella UIText](uitext-table.md)
    -   [Gestire linguaggio e tabella codici](manage-language-and-codepage.md)
    -   [Controllo della tabella codici del database di installazione](checking-the-installation-database-code-page.md)

-   Creare Windows installer per piattaforme a 32 bit e a 64 bit.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Windows Programma di installazione nei sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md)
    -   [Azioni personalizzate a 64 bit](64-bit-custom-actions.md)
    -   [Uso di azioni personalizzate a 64 bit](using-64-bit-custom-actions.md)
    -   [Uso di moduli unione a 64 bit](using-64-bit-merge-modules.md)

-   Ridistribuire i componenti Windows Installer e la logica di installazione come moduli unione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Unire i moduli](merge-modules.md)
    -   [Creazione di una trasformazione del linguaggio per un modulo unione in più lingue](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [Applicazione di un modulo unione configurabile con personalizzazioni](applying-a-configurable-merge-module-with-customizations.md)

-   Pianificare o eliminare i riavvii durante un Windows installazione del programma di installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Riavvii del sistema](system-reboots.md)
    -   [Registrazione delle richieste di riavvio](logging-of-reboot-requests.md)

-   Creare aggiornamenti o correzioni per un'applicazione esistente creando una patch.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Creazione di una patch di aggiornamento di piccole dimensioni](creating-a-small-update-patch.md)
    -   [Esempio di applicazione di patch per gli aggiornamenti di piccole dimensioni](a-small-update-patching-example.md)

-   Creare un pacchetto per doppio scopo in grado di installare un'applicazione solo per l'utente corrente o per tutti gli utenti del computer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Contesto di installazione](installation-context.md)
    -   [Creazione di singoli pacchetti](single-package-authoring.md)
    -   [Esempio di creazione di pacchetti singoli](single-package-authoring-example.md)

-   Personalizzare i servizi nel computer usando il programma di Windows installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Uso della configurazione dei servizi](using-services-configuration.md)

-   Proteggere le risorse nel computer usando il programma Windows installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Linee guida per la creazione di installazioni sicure](guidelines-for-authoring-secure-installations.md)
    -   [Protezione delle risorse](securing-resources-.md)

-   Enumerare tutti i componenti installati nel computer e ottenere il percorso della chiave per il componente.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Enumerazione dei componenti](enumerating-components-.md)

-   Installare più pacchetti usando [*l'elaborazione delle transazioni*](t-gly.md).

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Installazioni con più pacchetti](multiple-package-installations.md)

-   Incorporare un'interfaccia utente personalizzata nel pacchetto Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Utilizzo dell'interfaccia utente](using-the-user-interface.md)
    -   [Uso di un'interfaccia utente incorporata](using-an-embedded-ui.md)

## <a name="it-professionals"></a>Professionisti IT

I professionisti IT e gli amministratori personalizzano e distribuiscono i Windows installer esistenti. Questi utenti riassecchettono le configurazioni per le applicazioni esistenti Windows pacchetti di installazione del programma di installazione di e installano e gestiscono le immagini amministrative delle installazioni Windows Installer in reti.

-   Personalizzare le applicazioni e la configurazione generando e applicando Windows del programma di installazione

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Personalizzazione](customization.md)
    -   [Trasformazioni di database](database-transforms.md)
    -   [Esempio di trasformazione di personalizzazione](a-customization-transform-example.md)
    -   [Unioni e trasformazioni](merges-and-transforms.md)
    -   [Uso delle trasformazioni per aggiungere risorse](using-transforms-to-add-resources.md)
    -   [Generare una trasformazione](generate-a-transform.md)
    -   [Opzioni della riga di comando](command-line-options.md)
    -   [Msitran.exe](msitran-exe.md)
    -   [Applicare una trasformazione](apply-a-transform.md)
    -   [Visualizzare una trasformazione](view-a-transform.md)
    -   [Visualizzare le differenze tra due database](view-differences-between-two-databases.md)
    -   [Applicazione di patch alle applicazioni personalizzate](patching-customized-applications.md)

-   Distribuire un pacchetto di Windows, un aggiornamento o una patch del programma di installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Installazione di un'applicazione](installing-an-application.md)
    -   [Applicazione di patch e aggiornamenti](patching-and-upgrades.md)
    -   [Trasformazioni](transforms.md)
    -   [Installazione di un pacchetto con privilegi elevati per un utente non amministratore](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Applicazione di aggiornamenti principali applicando patch all'installazione locale del prodotto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [Applicazione di aggiornamenti principali tramite l'installazione del prodotto](applying-major-upgrades-by-installing-the-product.md)
    -   [Applicazione di piccoli aggiornamenti tramite applicazione di patch all'installazione locale del prodotto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Applicazione di piccoli aggiornamenti reinstallando il prodotto](applying-small-updates-by-reinstalling-the-product.md)
    -   [Applicazione di piccoli aggiornamenti tramite applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Applicazione di patch alle installazioni iniziali](patching-initial-installations.md)
    -   [Opzioni della riga di comando](command-line-options.md)

-   Risolvere i Windows pacchetti del programma di installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Windows Registrazione del programma di installazione](windows-installer-logging.md)
    -   [Controllo dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Ricerca di una funzionalità o di un componente interrotto](searching-for-a-broken-feature-or-component.md)
    -   [Windows Messaggi di errore del programma di installazione](windows-installer-error-messages.md)
    -   [Msicert.exe](msicert-exe.md)

-   Usare lo scripting per eseguire Windows pacchetti del programma di installazione per informazioni su un prodotto e modificare l'installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Interfaccia di automazione](automation-interface.md)
    -   [Windows Esempi di scripting del programma di installazione](windows-installer-scripting-examples.md)
    -   [Uso del Windows installer con WMI](using-windows-installer-with-wmi.md)

-   Creare e gestire installazioni amministrative.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Installazione amministrativa](administrative-installation.md)
    -   [Opzioni della riga di comando](command-line-options.md)
    -   [**Proprietà AdminProperties**](adminproperties.md)
    -   [Applicazione di piccoli aggiornamenti tramite applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Applicazione di un pacchetto patch a un'installazione amministrativa](applying-a-patch-package-to-an-administrative-installation.md)
    -   [Ordine di esecuzione dell'azione](action-execution-order.md)
    -   [**Proprietà IsAdminPackage**](isadminpackage.md)
    -   [Ordine di precedenza delle proprietà](order-of-property-precedence.md)
    -   [**Proprietà AdminProperties**](adminproperties.md)

-   Rendere un'applicazione disponibile per tutti gli utenti di un computer o solo per un utente specificato.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Contesto di installazione](installation-context.md)
    -   [**Proprietà ALLUSERS**](allusers.md)

-   Interpretare i pacchetti, installare prodotti e configurare le opzioni delle funzionalità tramite una riga di comando.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Opzioni della riga di comando](command-line-options.md)
    -   [Impostazione dei valori delle proprietà pubbliche nella riga di comando](setting-public-property-values-on-the-command-line.md)
    -   [Recupero e impostazione delle proprietà](getting-and-setting-properties.md)
    -   [Reinstallazione di una funzionalità o di un'applicazione](reinstalling-a-feature-or-application.md)
    -   [Applicazione di piccoli aggiornamenti tramite applicazione di patch all'installazione locale del prodotto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Applicazione di piccoli aggiornamenti reinstallando il prodotto](applying-small-updates-by-reinstalling-the-product.md)
    -   [Modifica del percorso di destinazione per una directory](changing-the-target-location-for-a-directory.md)
    -   [Applicazione di piccoli aggiornamenti tramite applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Applicazione di aggiornamenti principali tramite l'installazione del prodotto](applying-major-upgrades-by-installing-the-product.md)
    -   [Proprietà di configurazione](property-reference.md)
    -   [Proprietà delle opzioni di installazione delle funzionalità](property-reference.md)

-   Usare i criteri per gestire i diritti di accesso e le autorizzazioni.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Criteri computer](machine-policies.md),
    -   [Criteri utente](user-policies.md),
    -   [Installazione di un pacchetto con privilegi elevati per un utente non amministratore](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Annuncio di Per-User'applicazione da installare con privilegi elevati](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Uso di un'azione personalizzata per creare account utente in un computer locale](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**Proprietà AdminUser**](adminuser.md)
    -   [**Proprietà privileged**](privileged.md)
    -   [**Proprietà EnableUserControl**](enableusercontrol.md)
    -   [**Proprietà UserSID**](usersid.md)
    -   [**Proprietà SecureCustomProperties**](securecustomproperties.md)

-   Installare più pacchetti usando [*l'elaborazione delle transazioni*](t-gly.md).

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Installazioni con più pacchetti](multiple-package-installations.md)

-   Incorporare un'interfaccia utente personalizzata all'interno Windows pacchetto del programma di installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Utilizzo dell'interfaccia utente](using-the-user-interface.md)
    -   [Uso di un'interfaccia utente incorporata](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a>Sviluppatori di infrastrutture

Gli sviluppatori dell'infrastruttura possono creare piattaforme unificate per la distribuzione e la gestione del software che usa il Windows installer. Possono usare l'Windows di programmazione di Installer per eseguire query, gestire e distribuire applicazioni, patch e origini in un sistema.

-   Individuare, eseguire l'inventario ed eseguire query per lo stato, le informazioni e i client dei componenti.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Funzioni specifiche dei componenti](installer-function-reference.md)
    -   [Funzioni di stato del sistema](installer-function-reference.md)
    -   [Oggetto Installer](installer-object.md)
    -   [Oggetto Product](product-object.md)
    -   [Oggetto Patch](patch-object.md)

-   Inventario ed esecuzione di query per informazioni sullo stato dei prodotti e delle funzionalità.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Inventario di prodotti e patch](inventory-products-and-patches-.md)
    -   [Funzioni di stato del sistema](installer-function-reference.md)
    -   [Funzioni di query sul prodotto](installer-function-reference.md)
    -   [Oggetto Installer](installer-object.md)
    -   [Oggetto Product](product-object.md)
    -   [Oggetto Patch](patch-object.md)

-   Migliorare la resilienza dell'origine usando Windows installer per eseguire l'inventario, eseguire query e modificare l'elenco di origine di applicazioni, aggiornamenti e patch.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [**Proprietà SOURCELIST**](sourcelist.md)
    -   [**Resilienza di origine**](source-resiliency.md)
    -   [Funzioni di installazione e configurazione](installer-function-reference.md)
    -   [Oggetto Installer](installer-object.md)
    -   [Oggetto Product](product-object.md)
    -   [Oggetto Patch](patch-object.md)

-   Migliorare la resilienza dell'origine usando il programma di Windows per eseguire l'inventario, eseguire query e modificare le origini multimediali.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [**Proprietà SOURCELIST**](sourcelist.md)
    -   [Resilienza di origine](source-resiliency.md)
    -   [Funzioni di installazione e configurazione](installer-function-reference.md)
    -   [Oggetto Product](product-object.md)
    -   [Oggetto Patch](patch-object.md)

-   Inventario ed esecuzione di query per ottenere informazioni e lo stato delle patch.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Inventario di prodotti e patch](inventory-products-and-patches-.md)
    -   [Informazioni di riferimento sulla funzione Installer](installer-function-reference.md)
    -   [Oggetto Patch](patch-object.md)

-   Usare i criteri per gestire i diritti di accesso e le autorizzazioni.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Criteri del computer](machine-policies.md)
    -   [Criteri utente](user-policies.md)
    -   [Installazione di un pacchetto con privilegi elevati per utenti non amministratori](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Annuncio di Per-User'applicazione da installare con privilegi elevati](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Uso di un'azione personalizzata per creare account utente in un computer locale](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**Proprietà AdminUser**](adminuser.md)
    -   [**Proprietà privileged**](privileged.md)
    -   [**Proprietà EnableUserControl**](enableusercontrol.md)
    -   [**Proprietà UserSID**](usersid.md)
    -   [**Proprietà SecureCustomProperties**](securecustomproperties.md)

 

 



