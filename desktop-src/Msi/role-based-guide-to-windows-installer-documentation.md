---
description: Windows Installer è la soluzione consigliata per l'installazione e la configurazione delle applicazioni in Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Guida basata sui ruoli per la documentazione di Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8a2138e963b6d29bd161df5e09144cf0cfd36b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049700"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a>Guida basata sui ruoli per la documentazione di Windows Installer

Windows Installer è la soluzione consigliata per l'installazione e la configurazione delle applicazioni in Windows. Pertanto, alcune delle informazioni contenute in questo SDK saranno di interesse per un'ampia gamma di sviluppatori di software e professionisti IT. Questa sezione è costituita da una guida ai lettori che preferiscono visualizzare collegamenti ad argomenti organizzati in base al ruolo professionale e agli scenari di attività comuni. Poiché i ruoli possono differire molto tra le organizzazioni, il raggruppamento seguente dovrebbe essere considerato solo come una guida a una posizione per iniziare a cercare le informazioni necessarie.

-   [Sviluppatori di applicazioni](#application-developers)
-   [Autori installazione](#setup-authors)
-   [Professionisti IT](#it-professionals)
-   [Sviluppatori di infrastrutture](#infrastructure-developers)

Questa documentazione è destinata agli sviluppatori di software che desiderano creare applicazioni che utilizzano Windows Installer. Come origine principale del materiale di riferimento per il programma di installazione, l'SDK fornisce informazioni sui pacchetti di installazione e il servizio del programma di installazione. Contiene descrizioni complete del Application Programming Interface (API) e degli elementi del database del programma di installazione.

Per ulteriori informazioni, vedere [altre origini di Windows Installer informazioni](other-sources-of-windows-installer-information.md).

## <a name="application-developers"></a>Sviluppatori di applicazioni

Gli sviluppatori di applicazioni creano applicazioni che chiamano il Windows Installer Application Programming Interface e installano i pacchetti di Windows Installer in fase di esecuzione. Il Windows Installer può funzionare in un'applicazione, ad esempio la riparazione automatica e l'installazione su richiesta. In genere, gli sviluppatori di applicazioni eseguono le operazioni seguenti:

-   Consente l'installazione su richiesta di applicazioni in fase di esecuzione da un'altra applicazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Uso delle funzioni del programma di installazione](using-installer-functions.md)
    -   [Riferimento alla funzione Installer](installer-function-reference.md)
    -   [Installazione su richiesta](installation-on-demand.md)
    -   [Gestione dei componenti](component-management.md)
    -   [Modifica dei collegamenti del programma di installazione](editing-installer-shortcuts.md)
    -   [**Proprietà OLEAdvtSupport**](oleadvtsupport.md)
    -   [Supporto della piattaforma per gli annunci](platform-support-of-advertisement.md)

-   Abilitare la riparazione automatica delle applicazioni reinstallando i componenti in base alle esigenze in fase di esecuzione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Uso delle funzioni del programma di installazione](using-installer-functions.md)
    -   [Riferimento alla funzione Installer](installer-function-reference.md)
    -   [Resilienza](resiliency.md)
    -   [Resilienza di origine](source-resiliency.md)
    -   [Ricerca di una funzionalità o di un componente danneggiato](searching-for-a-broken-feature-or-component.md)
    -   [Sostituzione dei file esistenti](replacing-existing-files.md)

-   Consente di visualizzare un'interfaccia utente per raccogliere informazioni sull'utente e preferenze di configurazione la prima volta che un'applicazione viene installata o eseguita. L'interfaccia utente deve essere aggiunta dall'autore del programma di installazione del pacchetto di Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Uso delle funzioni del programma di installazione](using-installer-functions.md)
    -   [Inizializzazione di un'applicazione](initializing-an-application.md)
    -   [Finestra di dialogo FirstRun](firstrun-dialog.md)
    -   [Informazioni sull'interfaccia utente](about-the-user-interface.md)

-   Creare applicazioni che utilizzano un modello di riferimento indiretto per fare riferimento ai componenti con funzionalità parallele. Le categorie di componenti qualificate devono essere aggiunte dall'autore del programma di installazione del pacchetto Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Componenti qualificati](qualified-components.md)
    -   [Utilizzo di componenti qualificati](using-qualified-components.md)

-   Usare gli assembly privati e affiancati per isolare le applicazioni e ridurre i conflitti di DLL.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Assembly](assemblies.md)
    -   [Chiavi del registro di sistema dell'assembly scritte da Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Installazione degli assembly Win32 per la condivisione side-by-side in Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [Installazione di assembly Win32 per l'utilizzo privato di un'applicazione in Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [Tabella MsiAssembly](msiassembly-table.md)
    -   [Tabella MsiAssemblyName](msiassemblyname-table.md)
    -   [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [**Proprietà MsiWin32AssemblySupport**](msiwin32assemblysupport.md)
    -   [**Proprietà MsiNetAssemblySupport**](msinetassemblysupport.md)
    -   [**Componenti isolati**](isolated-components.md)

-   Preparare l'applicazione per l'installazione degli aggiornamenti principali completi.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Applicazione di patch e aggiornamenti](patching-and-upgrades.md)
    -   [Aggiornamenti principali](major-upgrades.md)
    -   [**Proprietà UpgradeCode**](upgradecode.md)
    -   [**Uso di un UpgradeCode**](using-an-upgradecode.md)
    -   [Impedire l'installazione di un pacchetto obsoleto in una versione più recente](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   Preparare l'applicazione per l'installazione di aggiornamenti secondari, piccoli aggiornamenti o correzioni.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Applicazione di patch e aggiornamenti](patching-and-upgrades.md)
    -   [Aggiornamenti di piccole dimensioni](small-updates.md)
    -   [Aggiornamenti secondari](minor-upgrades.md)

-   Organizzare le risorse dell'applicazione in componenti che possono funzionare con la Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Componenti Windows Installer](windows-installer-components.md)
    -   [Utilizzo delle funzionalità e dei componenti](working-with-features-and-components.md)
    -   [Utilizzo di componenti transitivi](using-transitive-components.md)
    -   [Cosa accade se le regole dei componenti sono interrotte?](what-happens-if-the-component-rules-are-broken.md)
    -   [Organizzazione di applicazioni in componenti](organizing-applications-into-components.md)
    -   [Componenti isolati](isolated-components.md)
    -   [Componenti qualificati](qualified-components.md)

## <a name="setup-authors"></a>Autori installazione

Gli autori del programma di installazione creano pacchetti di Windows Installer (file con estensione msi) che contengono la logica di installazione e le informazioni necessarie per installare un'applicazione. In genere usano strumenti di creazione, ad esempio [Orca.exe](orca-exe.md) per popolare il database Windows Installer con le informazioni e la logica di installazione. In genere, gli autori del programma di installazione eseguono le operazioni seguenti:

-   Determinare le funzionalità disponibili con diverse versioni di Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Determinazione della versione di Windows Installer](determining-the-windows-installer-version.md)
    -   [Versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md)
    -   [Novità di Windows Installer](what-s-new-in-windows-installer.md)

-   Organizzare le risorse dell'applicazione in componenti Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Componenti Windows Installer](windows-installer-components.md)
    -   [Organizzazione di applicazioni in componenti](organizing-applications-into-components.md)
    -   [Modifica del codice componente](changing-the-component-code.md)
    -   [Cosa accade se le regole dei componenti sono interrotte?](what-happens-if-the-component-rules-are-broken.md)
    -   [Esempi di Windows Installer](windows-installer-examples.md)

-   Utilizzare strumenti di creazione di pacchetti Windows Installer o strumenti SDK di terze parti, ad esempio [Orca.exe](orca-exe.md) per popolare un database di installazione e creare un pacchetto di Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
    -   [Pacchetto di installazione, informazioni sul database del programma di installazione](installation-package.md)
    -   [Estensioni di file Windows Installer](windows-installer-file-extensions.md)
    -   [Tabelle di database](database-tables.md)
    -   [Codici del pacchetto](package-codes.md)
    -   [Creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md)
    -   [Windows Installer su sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md)
    -   [Denominazione di tabelle, proprietà e azioni personalizzate](naming-custom-tables-properties-and-actions.md)
    -   [Limitazioni OLE sui flussi](ole-limitations-on-streams.md)
    -   [Formato della definizione di colonna](column-definition-format.md)
    -   [Riduzione delle dimensioni di un file con estensione msi](reducing-the-size-of-an--msi-file.md)

-   Creare il database di Windows Installer per installare i file.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Gruppo di tabelle Core](core-tables-group.md)
    -   [Gruppo di tabelle file](file-tables-group.md)
    -   [Tabella file](file-table.md)
    -   [Ricerca file](file-searching.md)
    -   [Costo file](file-costing.md)
    -   [Installazione file](file-installation.md)
    -   [File complementari](companion-files.md)
    -   [Regole di controllo delle versioni dei file](file-versioning-rules.md)
    -   [Controllo delle versioni dei file predefinito](default-file-versioning.md)
    -   [Sostituzione dei file esistenti](replacing-existing-files.md)
    -   [Uso di cabinet e origini compresse](using-cabinets-and-compressed-sources.md)
    -   [Rimozione di file bloccati](removing-stranded-files.md)
    -   [Installazione di componenti permanenti, file, tipi di carattere, chiavi del registro di sistema](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Tabella FileSFPCatalog](filesfpcatalog-table.md)
    -   [Ricerca di un file e creazione di una proprietà che contiene il percorso del file](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [Ricerca di una directory e di un file nella directory](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [Esempi di Windows Installer](windows-installer-examples.md)

-   Creare un database di Windows Installer che installa una struttura di directory e le cartelle.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Gruppo di tabelle Core](core-tables-group.md)
    -   [Gruppo di tabelle file](file-tables-group.md)
    -   [Tabella componenti](component-table.md)
    -   [Tabella directory](directory-table.md)
    -   [Uso della tabella di directory](using-the-directory-table.md)
    -   [Utilizzo di una proprietà di directory in un percorso](using-a-directory-property-in-a-path.md)
    -   [Proprietà cartella di sistema](property-reference.md)
    -   [Tabella CreateFolder](createfolder-table.md)
    -   [Tabella LockPermissions](lockpermissions-table.md)
    -   [Tabella MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [Modifica del percorso di destinazione per una directory](changing-the-target-location-for-a-directory.md)
    -   [Esempi di Windows Installer](windows-installer-examples.md)

-   Creare un database di Windows Installer che installa le chiavi del registro di sistema.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Gruppo di tabelle Core](core-tables-group.md)
    -   [Gruppo di tabelle del registro di sistema](registry-tables-group.md)
    -   [Tabella del registro di sistema](registry-table.md)
    -   [Modifica del registro di sistema](modifying-the-registry.md)
    -   [Aggiunta o rimozione di chiavi del registro di sistema durante l'installazione o la rimozione di componenti](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [Aggiunta e rimozione di un'applicazione senza traccia nel registro di sistema](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Installazione di componenti permanenti, file, tipi di carattere, chiavi del registro di sistema](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [Ricerca di una voce del registro di sistema e creazione di una proprietà contenente il valore del registro di sistema](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [Chiavi del registro di sistema dell'assembly scritte dal Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Disinstalla chiave del registro di sistema](uninstall-registry-key.md)
    -   [Tabella SelfReg](selfreg-table.md)
    -   [Specifica dell'ordine di registrazione automatica](specifying-the-order-of-self-registration.md)
    -   [Esempi di Windows Installer](windows-installer-examples.md)

-   Creare un database di Windows Installer che installa i servizi.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella ServiceInstall](serviceinstall-table.md)
    -   [Tabella ServiceControl](servicecontrol-table.md)
    -   [Tabella componenti](component-table.md)

-   Creare un database di Windows Installer che installa componenti isolati o componenti COM.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Gruppo di tabelle del registro di sistema](registry-tables-group.md)
    -   [Tabella classi](class-table.md)
    -   [Tabella ComPlus](complus-table.md)
    -   [Componenti isolati](isolated-components.md)
    -   [Utilizzo di componenti isolati](using-isolated-components.md)
    -   [Installazione di componenti isolati](installation-of-isolated-components.md)
    -   [Reinstallazione dei componenti isolati](reinstallation-of-isolated-components.md)
    -   [Rimozione di componenti isolati](removal-of-isolated-components.md)
    -   [Installazione di un componente COM in un percorso privato](installing-a-com-component-to-a-private-location.md)
    -   [Rendere privato un componente COM in un pacchetto esistente](make-a-com-component-in-an-existing-package-private.md)
    -   [Installazione di un'applicazione COM+ con la Windows Installer](installing-a-com--application-with-the-windows-installer.md)
    -   [Installazione di un componente non COM in una posizione privata](installing-a-non-com-component-to-a-private-location.md)
    -   [Creare un componente non COM in un pacchetto esistente privato](make-a-non-com-component-in-an-existing-package-private.md)

-   Consente di creare un database Windows Installer per l'installazione degli assembly.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella MsiAssembly](msiassembly-table.md)
    -   [Tabella MsiAssemblyName](msiassemblyname-table.md)
    -   [Assembly](assemblies.md)
    -   [Chiavi del registro di sistema dell'assembly scritte dal Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Installazione degli assembly Win32](installation-of-win32-assemblies.md)

-   Creazione di un database di Windows Installer che consente di installare driver e convertitori ODBC.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella ODBCAttribute](odbcattribute-table.md)
    -   [Tabella ODBCDriver](odbcdriver-table.md)
    -   [Tabella ODBCTranslator](odbctranslator-table.md)
    -   [Tabella ODBCDataSource](odbcdatasource-table.md)
    -   [Tabella ODBCSourceAttribute](odbcsourceattribute-table.md)

-   Creare un database di Windows Installer che installa MIME.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella MIME](mime-table.md)
    -   [Tabella di estensione](extension-table.md)
    -   [Modifica del registro di sistema](modifying-the-registry.md)

-   Creazione di un database di Windows Installer per l'installazione delle variabili di ambiente.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella ambiente](environment-table.md)

-   Creare un database di Windows Installer che installa i collegamenti.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella di collegamento](shortcut-table.md)
    -   [Tabella MsiShortcutProperty](msishortcutproperty-table.md)
    -   [Modifica dei collegamenti del programma di installazione](editing-installer-shortcuts.md)
    -   [Esempi di Windows Installer](windows-installer-examples.md)

-   Creare un database di Windows Installer che installa più istanze di applicazioni.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md)
    -   [Creazione di più istanze con le trasformazioni dell'istanza](authoring-multiple-instances-with-instance-transforms.md)
    -   [Installazione di più istanze con le trasformazioni dell'istanza](installing-multiple-instances-with-instance-transforms.md)

-   Specificare gli Stati e le opzioni di selezione delle funzionalità predefinite.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Gruppo di tabelle Core](core-tables-group.md)
    -   [Tabella componenti](component-table.md)
    -   [Tabella delle funzionalità](feature-table.md)
    -   [Tabella FeatureComponents](featurecomponents-table.md)
    -   [Controllo degli Stati di selezione delle funzionalità](controlling-feature-selection-states.md)
    -   [Proprietà opzioni di installazione funzionalità](property-reference.md)

-   Specificare le condizioni che devono essere soddisfatte per installare un'applicazione o i componenti selezionati.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Tabella Condition](condition-table.md)
    -   [Tabella LaunchCondition](launchcondition-table.md)
    -   [Tabella componenti](component-table.md)
    -   [Uso delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md)
    -   [Sintassi dell'istruzione condizionale](conditional-statement-syntax.md)
    -   [Esecuzione delle azioni di condizionamento durante la rimozione](conditioning-actions-to-run-during-removal.md)
    -   [Esempi di sintassi di istruzioni condizionali](examples-of-conditional-statement-syntax.md)

-   Consente di creare la sequenza di azioni utilizzata per installare l'applicazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Utilizzo di una tabella di sequenza](using-a-sequence-table.md)
    -   [Gruppo tabelle procedure di installazione](installation-procedure-tables-group.md)
    -   [Esempio dettagliato della tabella Sequence](sequence-table-detailed-example.md)
    -   [Azioni con restrizioni di sequenziazione](actions-with-sequencing-restrictions.md)
    -   [Azioni senza restrizioni di sequenziazione](actions-without-sequencing-restrictions.md)
    -   [Uso delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md)
    -   [Sintassi dell'istruzione condizionale](conditional-statement-syntax.md)
    -   [Esempi di sintassi di istruzioni condizionali](examples-of-conditional-statement-syntax.md)
    -   [Esecuzione delle azioni di condizionamento durante la rimozione](conditioning-actions-to-run-during-removal.md)
    -   [Azioni standard](standard-actions.md)
    -   [Esempi di Windows Installer](windows-installer-examples.md)

-   Preparare il pacchetto di installazione dell'applicazione per gli aggiornamenti futuri dell'applicazione da parte del servizio Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Applicazione di patch e aggiornamenti](patching-and-upgrades.md)
    -   [Preparazione di un'applicazione per aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md)
    -   [Uso di un UpgradeCode](using-an-upgradecode.md)
    -   [Aggiorna tabella](upgrade-table.md)
    -   [**Proprietà UpgradeCode**](upgradecode.md)
    -   [Impedire l'installazione di un pacchetto obsoleto in una versione più recente](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [Modifica del codice del prodotto](changing-the-product-code.md)
    -   [Aggiornamento degli assembly](updating-assemblies.md)
    -   [Esempi di Windows Installer](windows-installer-examples.md)

-   Risolvere i problemi relativi ai pacchetti Windows Installer in fase di sviluppo.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Convalida del pacchetto](package-validation.md)
    -   [Analizzatori di coerenza interni-CIEM](internal-consistency-evaluators-ices.md)
    -   [Registrazione Windows Installer](windows-installer-logging.md)
    -   [Verifica dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md)
    -   [Creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
    -   [Convalida di moduli merge](validating-merge-modules.md)
    -   [Convalida di un database di installazione](validating-an-installation-database.md)
    -   [Convalida di un aggiornamento dell'installazione](validating-an-installation-upgrade.md)
    -   [Ricerca di una funzionalità o di un componente danneggiato](searching-for-a-broken-feature-or-component.md)
    -   [Messaggi di errore Windows Installer](windows-installer-error-messages.md)
    -   [Registrazione delle richieste di riavvio](logging-of-reboot-requests.md)

-   Verificare la configurazione e l'installazione sicure dell'applicazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Linee guida per la creazione di installazioni sicure](guidelines-for-authoring-secure-installations.md)
    -   [Linee guida per la protezione di azioni personalizzate](guidelines-for-securing-custom-actions.md)
    -   [Sicurezza azione personalizzata](custom-action-security.md)
    -   [Linee guida per la protezione dei pacchetti nei computer bloccati](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [Creazione di un'installazione firmata completamente verificata tramite l'automazione](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [Esempio di installazione di Windows Installer basata su Windows](a-url-based-windows-installer-installation-example.md)
    -   [Creazione dell'interfaccia utente per l'input della password](authoring-the-user-interface-for-password-input.md)
    -   [Firme digitali e Windows Installer](digital-signatures-and-windows-installer.md)
    -   [Uso di Windows Installer con UAC](using-windows-installer-with-uac.md)
    -   [Applicazione di patch al controllo dell'account utente (UAC)](user-account-control--uac--patching.md)
    -   [Msicert.exe](msicert-exe.md)
    -   [**Proprietà AdminUser**](adminuser.md)
    -   [**Proprietà Privileged**](privileged.md)
    -   [**Proprietà SecureCustomProperties**](securecustomproperties.md)

-   Creare un'interfaccia utente per presentare le opzioni per configurare l'installazione e ottenere informazioni dall'utente sul processo di installazione in sospeso.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Informazioni sull'interfaccia utente](about-the-user-interface.md)
    -   [Aggiunta di controlli e testo](adding-controls-and-text.md)
    -   [Creazione di un controllo ProgressBar](authoring-a-progressbar-control.md)
    -   [Creazione di messaggi di richiesta del disco](authoring-disk-prompt-messages.md)
    -   [Creazione di un condizionale "attendere..." MessageBox](authoring-a-conditional-please-wait-------message-box.md)
    -   [Visualizzazione in anteprima dell'interfaccia utente](previewing-the-user-interface.md)
    -   [Aggiunta di testo archiviato in una proprietà](adding-text-stored-in-a-property.md)
    -   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   Creare un'interfaccia utente esterna per presentare un'interfaccia utente personalizzata per configurare l'installazione e ottenere informazioni dall'utente sul processo di installazione in sospeso.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [Monitoraggio di un'installazione mediante MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [Analisi di messaggi di Windows Installer](parsing-windows-installer-messages.md)
    -   [Restituzione di valori da un gestore di interfaccia utente esterno](returning-values-from-an-external-user-interface-handler.md)
    -   [\_gestore INSTALLUI](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [Gestione dei messaggi di stato tramite MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md)
    -   [Monitoraggio di un'installazione mediante MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md)

-   Impostare le informazioni per l'applicazione in **installazione** applicazioni (ARP.)

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Configurazione di installazione applicazioni con Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
    -   [Aggiunta e rimozione di un'applicazione senza traccia nel registro di sistema](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Disinstalla chiave del registro di sistema](uninstall-registry-key.md)

-   Scrivere azioni personalizzate per gestire la logica di installazione che non è supportata in modo nativo da Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Azioni personalizzate](custom-actions.md)
    -   [Elenco riepilogativo di tutti i tipi di azione personalizzati](summary-list-of-all-custom-action-types.md)
    -   [Linee guida per la protezione di azioni personalizzate](guidelines-for-securing-custom-actions.md)
    -   [Riferimento all'azione personalizzata](custom-action-reference.md)
    -   [Uso di un'azione personalizzata per creare account utente in un computer locale](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [Uso di un'azione personalizzata per avviare un file installato al termine dell'installazione](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [Accesso a un database o a una sessione dall'interno di un'azione personalizzata](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [Accesso alla sessione corrente del programma di installazione dall'interno di un'azione personalizzata](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [Modifica dello stato del sistema mediante un'azione personalizzata](changing-the-system-state-using-a-custom-action.md)

-   Bootstrap del Windows Installer nel computer di un utente.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Bootstrap](bootstrapping.md)
    -   [Instmsi.exe](instmsi-exe.md)
    -   [Bootstrap di download Internet](internet-download-bootstrapping.md)
    -   [Msistuff.exe](msistuff-exe.md)
    -   [Esempio di installazione di Windows Installer basata su Windows](a-url-based-windows-installer-installation-example.md)
    -   [Configurazione delle risorse Setup.exe](configuring-the-setup-exe-resources.md)
    -   [Download di un'installazione da Internet](downloading-an-installation-from-the-internet.md)

-   Rispettare Active Accessibility linee guida per la scrittura di pacchetti Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Accessibilità](accessibility.md)

-   Preparare l'internazionalizzazione della configurazione di un'applicazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Preparazione di un pacchetto di Windows Installer per la localizzazione](preparing-a-windows-installer-package-for-localization.md),
    -   [Localizzazione di un pacchetto di Windows Installer](localizing-a-windows-installer-package.md)
    -   [Gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md)
    -   [Aggiunta di risorse localizzate](adding-localized-resources.md)
    -   [Esempio di localizzazione](a-localization-example.md)
    -   [Localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md)
    -   [Localizzazione di colonne di database](localizing-database-columns.md)
    -   [Creazione di un database con una tabella codici neutra](creating-a-database-with-a-neutral-code-page.md)
    -   [Gestione delle tabelle codici per le tabelle importate ed esportate](code-page-handling-of-imported-and-exported-tables.md)
    -   [Localizzazione della lingua visualizzata dalle finestre di dialogo](localizing-the-language-displayed-by-dialogs.md)
    -   [Importazione delle tabelle ActionText e degli errori localizzati](importing-localized-error-and-actiontext-tables.md)
    -   [Aggiornamento delle proprietà ProductLanguage e ProductCode](updating-productlanguage-and-productcode-properties.md)
    -   [Aggiornamento di un flusso di informazioni di riepilogo](updating-a-summary-information-stream.md)
    -   [Componenti qualificati](qualified-components.md)
    -   [Tabella UIText](uitext-table.md)
    -   [Gestisci lingua e tabella codici](manage-language-and-codepage.md)
    -   [Controllo della tabella codici del database di installazione](checking-the-installation-database-code-page.md)

-   Creare pacchetti di Windows Installer per piattaforme a 32 bit e a 64 bit.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Windows Installer su sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md)
    -   [Azioni personalizzate a 64 bit](64-bit-custom-actions.md)
    -   [Uso di azioni personalizzate a 64 bit](using-64-bit-custom-actions.md)
    -   [Uso di moduli unione a 64 bit](using-64-bit-merge-modules.md)

-   Ridistribuire i componenti di Windows Installer condivisi e la logica di installazione come moduli unione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Unisci moduli](merge-modules.md)
    -   [Creazione di una trasformazione lingua per un modulo merge a più lingue](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [Applicazione di un modulo merge configurabile con personalizzazioni](applying-a-configurable-merge-module-with-customizations.md)

-   Pianificare o disattivare il riavvio durante un'installazione di Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Riavvio del sistema](system-reboots.md)
    -   [Registrazione delle richieste di riavvio](logging-of-reboot-requests.md)

-   Creare aggiornamenti o correzioni per un'applicazione esistente creando una patch.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Creazione di una patch di aggiornamento di piccole dimensioni](creating-a-small-update-patch.md)
    -   [Un piccolo esempio di patch di aggiornamento](a-small-update-patching-example.md)

-   Creare un pacchetto a doppio scopo in grado di installare un'applicazione solo per l'utente corrente o per tutti gli utenti del computer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Contesto di installazione](installation-context.md)
    -   [Creazione di pacchetti singoli](single-package-authoring.md)
    -   [Esempio di creazione di pacchetti singoli](single-package-authoring-example.md)

-   Personalizzare i servizi nel computer usando il Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Uso della configurazione dei servizi](using-services-configuration.md)

-   Proteggere le risorse del computer utilizzando il Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Linee guida per la creazione di installazioni sicure](guidelines-for-authoring-secure-installations.md)
    -   [Protezione delle risorse](securing-resources-.md)

-   Enumerare tutti i componenti installati nel computer e ottenere il percorso della chiave per il componente.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Enumerazione dei componenti](enumerating-components-.md)

-   Installare più pacchetti usando l' [*elaborazione delle transazioni*](t-gly.md).

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Installazioni con più pacchetti](multiple-package-installations.md)

-   Incorporare un'interfaccia utente personalizzata nel pacchetto di Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Utilizzo dell'interfaccia utente](using-the-user-interface.md)
    -   [Uso di un'interfaccia utente incorporata](using-an-embedded-ui.md)

## <a name="it-professionals"></a>Professionisti IT

I professionisti IT e gli amministratori possono personalizzare e distribuire i pacchetti di Windows Installer esistenti. Questi utenti riassemblano le configurazioni per le applicazioni esistenti in pacchetti di installazione Windows Installer e installano e gestiscono immagini amministrative di Windows Installer installazioni sulle reti.

-   Personalizzare le applicazioni e il programma di installazione tramite la generazione e l'applicazione di trasformazioni Windows Installer

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Personalizzazione](customization.md)
    -   [Trasformazioni di database](database-transforms.md)
    -   [Esempio di trasformazione della personalizzazione](a-customization-transform-example.md)
    -   [Unioni e trasformazioni](merges-and-transforms.md)
    -   [Uso delle trasformazioni per aggiungere risorse](using-transforms-to-add-resources.md)
    -   [Genera una trasformazione](generate-a-transform.md)
    -   [Opzioni della riga di comando](command-line-options.md)
    -   [Msitran.exe](msitran-exe.md)
    -   [Applicare una trasformazione](apply-a-transform.md)
    -   [Visualizzazione di una trasformazione](view-a-transform.md)
    -   [Visualizzare le differenze tra due database](view-differences-between-two-databases.md)
    -   [Applicazione di patch a applicazioni personalizzate](patching-customized-applications.md)

-   Distribuire un pacchetto di installazione di Windows Installer, aggiornamento o patch.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Installazione di un'applicazione](installing-an-application.md)
    -   [Applicazione di patch e aggiornamenti](patching-and-upgrades.md)
    -   [Trasformazioni](transforms.md)
    -   [Installazione di un pacchetto con privilegi elevati per un amministratore non](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Applicazione degli aggiornamenti principali mediante l'applicazione di patch all'installazione locale del prodotto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [Applicazione degli aggiornamenti principali tramite l'installazione del prodotto](applying-major-upgrades-by-installing-the-product.md)
    -   [Applicazione di piccoli aggiornamenti con l'applicazione di patch all'installazione locale del prodotto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Applicazione di piccoli aggiornamenti con la reinstallazione del prodotto](applying-small-updates-by-reinstalling-the-product.md)
    -   [Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Applicazione di patch alle installazioni iniziali](patching-initial-installations.md)
    -   [Opzioni della riga di comando](command-line-options.md)

-   Risolvere i problemi relativi ai pacchetti Windows Installer.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Registrazione Windows Installer](windows-installer-logging.md)
    -   [Verifica dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Ricerca di una funzionalità o di un componente danneggiato](searching-for-a-broken-feature-or-component.md)
    -   [Messaggi di errore Windows Installer](windows-installer-error-messages.md)
    -   [Msicert.exe](msicert-exe.md)

-   Utilizzare gli script per eseguire query Windows Installer pacchetti per ottenere informazioni su un prodotto e modificarne l'installazione.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Interfaccia di automazione](automation-interface.md)
    -   [Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
    -   [Utilizzo di Windows Installer con WMI](using-windows-installer-with-wmi.md)

-   Creare e gestire le installazioni amministrative.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Installazione amministrativa](administrative-installation.md)
    -   [Opzioni della riga di comando](command-line-options.md)
    -   [**Proprietà AdminProperties**](adminproperties.md)
    -   [Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Applicazione di un pacchetto di patch a un'installazione amministrativa](applying-a-patch-package-to-an-administrative-installation.md)
    -   [Ordine di esecuzione delle azioni](action-execution-order.md)
    -   [**Proprietà IsAdminPackage**](isadminpackage.md)
    -   [Ordine di precedenza delle proprietà](order-of-property-precedence.md)
    -   [**Proprietà AdminProperties**](adminproperties.md)

-   Rendere disponibile un'applicazione per tutti gli utenti di un computer o solo per un utente specifico.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Contesto di installazione](installation-context.md)
    -   [**Proprietà ALLUSERS**](allusers.md)

-   Interpretare i pacchetti, installare i prodotti e configurare le opzioni delle funzionalità tramite una riga di comando.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Opzioni della riga di comando](command-line-options.md)
    -   [Impostazione dei valori delle proprietà pubbliche nella riga di comando](setting-public-property-values-on-the-command-line.md)
    -   [Recupero e impostazione delle proprietà](getting-and-setting-properties.md)
    -   [Reinstallazione di una funzionalità o di un'applicazione](reinstalling-a-feature-or-application.md)
    -   [Applicazione di piccoli aggiornamenti con l'applicazione di patch all'installazione locale del prodotto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Applicazione di piccoli aggiornamenti con la reinstallazione del prodotto](applying-small-updates-by-reinstalling-the-product.md)
    -   [Modifica del percorso di destinazione per una directory](changing-the-target-location-for-a-directory.md)
    -   [Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Applicazione degli aggiornamenti principali tramite l'installazione del prodotto](applying-major-upgrades-by-installing-the-product.md)
    -   [Proprietà di configurazione](property-reference.md)
    -   [Proprietà opzioni di installazione funzionalità](property-reference.md)

-   Usare i criteri per gestire i diritti e le autorizzazioni di accesso.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Criteri del computer](machine-policies.md),
    -   [Criteri utente](user-policies.md),
    -   [Installazione di un pacchetto con privilegi elevati per un amministratore non](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Annuncio di un'applicazione Per-User da installare con privilegi elevati](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Uso di un'azione personalizzata per creare account utente in un computer locale](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**Proprietà AdminUser**](adminuser.md)
    -   [**Proprietà Privileged**](privileged.md)
    -   [**Proprietà EnableUserControl**](enableusercontrol.md)
    -   [**Proprietà UserSID**](usersid.md)
    -   [**Proprietà SecureCustomProperties**](securecustomproperties.md)

-   Installare più pacchetti usando l' [*elaborazione delle transazioni*](t-gly.md).

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Installazioni con più pacchetti](multiple-package-installations.md)

-   Incorporare un'interfaccia utente personalizzata all'interno di un pacchetto di Windows Installer..

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Utilizzo dell'interfaccia utente](using-the-user-interface.md)
    -   [Uso di un'interfaccia utente incorporata](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a>Sviluppatori di infrastrutture

Gli sviluppatori di infrastrutture possono creare piattaforme unificate per la distribuzione e la gestione del software che usa il servizio Windows Installer. Possono utilizzare l'interfaccia di programmazione Windows Installer per eseguire query, gestire e distribuire applicazioni, patch e origini in un sistema.

-   Individuazione, inventario ed esecuzione di query per lo stato, le informazioni e i client dei componenti.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Funzioni specifiche del componente](installer-function-reference.md)
    -   [Funzioni di stato del sistema](installer-function-reference.md)
    -   [Oggetto Installer](installer-object.md)
    -   [Oggetto Product](product-object.md)
    -   [Patch (oggetto)](patch-object.md)

-   Inventario ed esecuzione di query per informazioni e lo stato di prodotti e funzionalità.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Inventario di prodotti e patch](inventory-products-and-patches-.md)
    -   [Funzioni di stato del sistema](installer-function-reference.md)
    -   [Funzioni di query sul prodotto](installer-function-reference.md)
    -   [Oggetto Installer](installer-object.md)
    -   [Oggetto Product](product-object.md)
    -   [Patch (oggetto)](patch-object.md)

-   Migliorare la resilienza dell'origine usando il Windows Installer per eseguire l'inventario, eseguire query e modificare l'elenco di origine di applicazioni, aggiornamenti e patch.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [**SOURCEs (proprietà)**](sourcelist.md)
    -   [**Resilienza di origine**](source-resiliency.md)
    -   [Funzioni di installazione e configurazione](installer-function-reference.md)
    -   [Oggetto Installer](installer-object.md)
    -   [Oggetto Product](product-object.md)
    -   [Patch (oggetto)](patch-object.md)

-   Migliorare la resilienza dell'origine usando il Windows Installer per l'inventario, la query e la modifica delle origini multimediali.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [**SOURCEs (proprietà)**](sourcelist.md)
    -   [Resilienza di origine](source-resiliency.md)
    -   [Funzioni di installazione e configurazione](installer-function-reference.md)
    -   [Oggetto Product](product-object.md)
    -   [Patch (oggetto)](patch-object.md)

-   Inventario ed esecuzione di query per le informazioni e lo stato delle patch.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Inventario di prodotti e patch](inventory-products-and-patches-.md)
    -   [Riferimento alla funzione Installer](installer-function-reference.md)
    -   [Patch (oggetto)](patch-object.md)

-   Usare i criteri per gestire i diritti e le autorizzazioni di accesso.

    Per altre informazioni, vedere gli argomenti seguenti:

    -   [Criteri del computer](machine-policies.md)
    -   [Criteri utente](user-policies.md)
    -   [Installazione di un pacchetto con privilegi elevati per un amministratore non](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Annuncio di un'applicazione Per-User da installare con privilegi elevati](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Uso di un'azione personalizzata per creare account utente in un computer locale](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**Proprietà AdminUser**](adminuser.md)
    -   [**Proprietà Privileged**](privileged.md)
    -   [**Proprietà EnableUserControl**](enableusercontrol.md)
    -   [**Proprietà UserSID**](usersid.md)
    -   [**Proprietà SecureCustomProperties**](securecustomproperties.md)

 

 



