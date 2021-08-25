---
description: 'Questa sezione elenca le proprietà definite dal programma di Windows installer:'
ms.assetid: c91119b9-59d5-4a33-91cd-d3ba63659d12
title: Informazioni di riferimento sulla proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e38f952632609090c69b85786c6aef64243d420b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481567"
---
# <a name="property-reference"></a>Informazioni di riferimento sulla proprietà

Questa sezione elenca le proprietà definite dal programma di Windows installer:

-   [Proprietà della posizione dei componenti](#component-location-properties)
-   [Proprietà di configurazione](#configuration-properties)
-   [Proprietà di data e ora](#date-time-properties)
-   [Proprietà delle opzioni di installazione delle funzionalità](#feature-installation-options-properties)
-   [Proprietà hardware](#hardware-properties)
-   [Proprietà dello stato dell'installazione](#installation-status-properties)
-   [Proprietà del sistema operativo](#operating-system-properties)
-   [Proprietà delle informazioni sul prodotto](#product-information-properties)
-   [Proprietà di aggiornamento delle informazioni di riepilogo](#summary-information-update-properties)
-   [Proprietà cartella di sistema](#system-folder-properties)
-   [Proprietà delle informazioni utente](#user-information-properties)

Le proprietà aggiuntive possono essere specificate dai dati creati o dalle azioni personalizzate. Le proprietà con nomi che non contengono lettere minuscole sono proprietà pubbliche e possono essere specificate nella riga di comando.

Per informazioni sui valori della chiave del Registro di sistema **Uninstall** forniti dalle proprietà del programma di installazione, vedere [Disinstallare la chiave del Registro di sistema](uninstall-registry-key.md).

## <a name="component-location-properties"></a>Proprietà della posizione dei componenti

Nell'elenco seguente vengono forniti collegamenti a altre informazioni sulle proprietà della posizione del componente.



| Proprietà                                                            | Descrizione                                                                                                                                                                                                        |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OriginalDatabase**](originaldatabase.md)<br/>             | Il programma di installazione imposta questa proprietà sul database avviato, sul database di origine o sul database memorizzato nella cache.<br/>                                                                                     |
| [**ParentOriginalDatabase**](parentoriginaldatabase.md)<br/> | Il programma di installazione imposta questa proprietà per le installazioni eseguite da [un'azione Di installazione](concurrent-installations.md) simultanea.<br/>                                                                             |
| [**SourceDir**](sourcedir.md)<br/>                           | Directory radice che contiene i file di origine.<br/>                                                                                                                                                          |
| [**TARGETDIR**](targetdir.md)<br/>                           | Specifica la directory di destinazione radice per l'installazione. Durante [un'installazione amministrativa](administrative-installation.md) questa proprietà è il percorso in cui copiare il pacchetto di installazione.<br/> |



 

## <a name="configuration-properties"></a>Configuration Properties

Nell'elenco seguente sono disponibili collegamenti ad altre informazioni su altre proprietà configurabili.



| Proprietà                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AZIONE**](action.md)<br/>                                                     | Azione iniziale chiamata dopo l'inizializzazione del programma di installazione.<br/>                                                                                                                                                                                                                                                                                                                          |
| [**ALLUSERS**](allusers.md)<br/>                                                 | Determina dove vengono archiviate le informazioni di configurazione.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)<br/>                     | URL del canale di aggiornamento per un'applicazione.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**ARPCOMMENTS**](arpcomments.md)<br/>                                           | Fornisce commenti per Installazione **applicazioni** **in** Pannello di controllo .<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPCONTACT**](arpcontact.md)<br/>                                             | Fornisce il contatto per **Installazione applicazioni** in **Pannello di controllo**.<br/>                                                                                                                                                                                                                                                                                                          |
| [**ARPINSTALLLOCATION**](arpinstalllocation.md)<br/>                             | Percorso completo della cartella primaria di un'applicazione.<br/>                                                                                                                                                                                                                                                                                                                      |
| [**ARPNOMODIFY**](arpnomodify.md)<br/>                                           | Disabilita la funzionalità che modifica un prodotto.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**ARPNOREMOVE**](arpnoremove.md)<br/>                                           | Disabilita la funzionalità che rimuove un prodotto.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPNOREPAIR**](arpnorepair.md)<br/>                                           | Disabilita il pulsante **Ripristina** nella procedura guidata Programmi.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**ARPPRODUCTICON**](arpproducticon.md)<br/>                                     | Specifica l'icona primaria per il pacchetto di installazione.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ARPREADME**](arpreadme.md)<br/>                                               | Fornisce un **file Leggimi** per **Installazione applicazioni** in **Pannello di controllo**.<br/>                                                                                                                                                                                                                                                                                                     |
| [**ARPSIZE**](arpsize.md)<br/>                                                   | Dimensioni stimate di un'applicazione in kilobyte.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPSYSTEMCOMPONENT**](arpsystemcomponent.md)<br/>                             | Impedisce la visualizzazione di un'applicazione **nell'elenco Installazione applicazioni.**<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPURLINFOABOUT**](arpurlinfoabout.md)<br/>                                   | URL per la home page di un'applicazione.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)<br/>                                 | URL per le informazioni sull'aggiornamento dell'applicazione.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**AVAILABLEFREEREG**](availablefreereg.md)<br/>                                 | Spazio del Registro di sistema (in kilobyte) richiesto da un'applicazione. Utilizzato [dall'azione AllocateRegistrySpace](allocateregistryspace-action.md).<br/>                                                                                                                                                                                                                                              |
| [**UNITÀ \_ CCP**](ccp-drive.md)<br/>                                              | Percorso radice per i prodotti idonei per CCP.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**DefaultUIFont**](defaultuifont.md)<br/>                                       | Stile del carattere predefinito usato per i controlli.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md)<br/>                         | Impostare per disabilitare la generazione dei collegamenti specifici che [supportano l'installazione su richiesta.](installation-on-demand.md)<br/>                                                                                                                                                                                                                                                            |
| [**DISABLEMEDIA**](-disablemedia.md)<br/>                                        | Impedisce al programma di installazione di registrare origini multimediali, ad esempio CD-ROM, come origini valide per il prodotto.<br/>                                                                                                                                                                                                                                                                        |
| [**DISABLEROLLBACK**](-disablerollback.md)<br/>                                  | Disabilita il rollback per la configurazione corrente.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**EXECUTEACTION**](executeaction.md)<br/>                                       | Azione di primo livello avviata da ExecuteAction.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**EXECUTEMODE**](executemode.md)<br/>                                           | Modalità di esecuzione eseguita dal programma di installazione.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**FASTOEM**](fastoem.md)<br/>                                                   | Migliora le prestazioni di installazione in scenari OEM specifici.<br/>                                                                                                                                                                                                                                                                                                                    |
| [**INSTALLLEVEL**](installlevel.md)<br/>                                         | Livello iniziale in cui vengono installate le funzionalità.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**LIMITUI**](limitui.md)<br/>                                                   | Il livello dell'interfaccia utente è limitato a Basic.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**LOGACTION**](logaction.md)<br/>                                               | Elenco di nomi di azioni da registrato.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**MEDIAPACKAGEPATH**](mediapackagepath.md)<br/>                                 | Questa proprietà deve essere impostata sul percorso relativo se il pacchetto di installazione non si trova nella radice del CD-ROM.<br/>                                                                                                                                                                                                                                                               |
| [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)<br/>                 | Questa proprietà facoltativa contiene un elenco delimitato da punto e virgola dei percorsi del Registro di sistema in cui l'applicazione archivia le impostazioni e le preferenze di un utente. Disponibile con Windows Installer 4.0.<br/>                                                                                                                                                                                        |
| [**MSIDISABLEEEUI**](msidisableeeui.md)<br/>                                     | Disabilitare l'interfaccia utente incorporata per l'installazione.<br/> **[Windows Installer 4.0 e versioni precedenti:](not-supported-in-windows-installer-4-0.md)** Non supportato.<br/>                                                                                                                                                                                                           |
| [**MSIFASTINSTALL**](msifastinstall.md)<br/>                                     | Ridurre il tempo necessario per installare un pacchetto di installazione Windows di grandi dimensioni.<br/> **[Windows Installer 4.5 e versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato.<br/>                                                                                                                                                                                              |
| [**MSIINSTALLPERUSER**](msiinstallperuser.md)<br/>                               | Richiede che il Windows installi il pacchetto solo per l'utente corrente.<br/> **[Windows Installer 4.5 e versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato.<br/>                                                                                                                                                                                  |
| [**MSINODISABLEMEDIA**](msinodisablemedia.md)<br/>                               | Impostare questa proprietà per impedire al programma di installazione di impostare la [**proprietà DISABLEMEDIA.**](-disablemedia.md)<br/>                                                                                                                                                                                                                                                                        |
| [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)<br/>   | Impostare questa proprietà su 1 (uno) nella [](property-table.md) riga di comando o [](small-updates.md) nella tabella delle proprietà per applicare le regole del componente di aggiornamento durante piccoli aggiornamenti e aggiornamenti secondari [di](minor-upgrades.md) un prodotto specifico. Disponibile a partire da Windows Installer 3.0.<br/>                                                                                     |
| [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)<br/> | Quando questa proprietà è stata impostata su 1, il programma di installazione può annullare la registrazione e disinstallare i componenti ridondanti per evitare di lasciare i componenti orfani nel computer.<br/> **[Windows Installer 4.0 e versioni precedenti:](not-supported-in-windows-installer-4-0.md)** Non supportato.<br/>                                                                                                  |
| [**PRIMARYFOLDER**](primaryfolder.md)<br/>                                       | Consente all'autore di designare una cartella primaria per un'installazione. Usato per determinare i valori per [**le proprietà PrimaryVolumePath**](primaryvolumepath.md), [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md), [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)e [**PrimaryVolumeSpaceRemaining.**](primaryvolumespaceremaining.md)<br/> |
| [**Privilegiata**](privileged.md)<br/>                                             | Esegue un'installazione con privilegi elevati.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md)<br/>                             | Azione se lo spazio su disco per l'installazione è insufficiente.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**RIAVVIARE**](reboot.md)<br/>                                                     | Forza o elimina un riavvio.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**REBOOTPROMPT**](rebootprompt.md)<br/>                                         | Elimina la visualizzazione delle richieste di riavvio all'utente. Eventuali riavvii necessari vengono evasi automaticamente.<br/>                                                                                                                                                                                                                                                                     |
| [**ROOTDRIVE**](rootdrive.md)<br/>                                               | Unità predefinita per un'installazione.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SEQUENCE**](sequence.md)<br/>                                                 | Tabella con lo schema della tabella di sequenza.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**SHORTFILENAMES**](shortfilenames.md)<br/>                                     | Determina l'uso di nomi di file brevi.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**TRASFORMA**](transforms.md)<br/>                                             | Elenco di trasformazioni da applicare a un database.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**TRANSFORMSATSOURCE**](transformsatsource.md)<br/>                             | Informa il programma di installazione che le trasformazioni per un prodotto risiedono nell'origine.<br/>                                                                                                                                                                                                                                                                                                      |
| [**TRANSFORMSSECURE**](transformssecure.md)<br/>                                 | L'impostazione della proprietà [**TRANSFORMSECURE**](transformssecure.md) su 1 (uno) informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache locale nel computer utente in un percorso in cui l'utente non ha accesso in scrittura.<br/>                                                                                                                                                           |
| [**MsiLogFileLocation**](msilogfilelocation.md)<br/>                             | Il programma di installazione imposta il valore di questa proprietà sul percorso completo del file di log, quando la registrazione è stata abilitata. Questa proprietà è disponibile a partire da Windows Installer 4.0.<br/>                                                                                                                                                                                                     |
| [**MsiLogging**](msilogging.md)<br/>                                             | Imposta la modalità di registrazione predefinita per il pacchetto Windows Installer. Questa proprietà è disponibile a partire da Windows Installer 4.0.<br/>                                                                                                                                                                                                                                                   |
| [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)<br/>                 | Impostare questa proprietà su 1 per richiedere che il programma di installazione usi le informazioni utente effettive durante l'impostazione [**della proprietà AdminUser.**](adminuser.md) Questa proprietà è disponibile a partire da Windows Installer 4.0.<br/>                                                                                                                                                                         |



 

## <a name="date-time-properties"></a>Proprietà di data e ora

Le [**proprietà Data**](date.md) e [**Ora**](time.md) sono proprietà in tempo reale impostate dal programma di installazione quando vengono estratti i dati.



| Proprietà                        | Descrizione                  |
|---------------------------------|------------------------------|
| [**Date**](date.md)<br/> | Data corrente.<br/> |
| [**Ora**](time.md)<br/> | Ora corrente.<br/> |



 

## <a name="feature-installation-options-properties"></a>Proprietà delle opzioni di installazione delle funzionalità

Nell'elenco seguente sono disponibili collegamenti a altre informazioni sulle proprietà delle opzioni di installazione delle funzionalità.



| Proprietà                                                                | Descrizione                                                                                                                                                                       |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADDDEFAULT**](adddefault.md)<br/>                             | Elenco di funzionalità da installare nella configurazione predefinita.<br/>                                                                                                         |
| [**ADDLOCAL**](addlocal.md)<br/>                                 | Elenco di funzionalità da installare in locale.<br/>                                                                                                                              |
| [**ADDSOURCE**](addsource.md)<br/>                               | Elenco di funzionalità da eseguire dall'origine.<br/>                                                                                                                                |
| [**PUBBLICIZZARE**](advertise.md)<br/>                               | Elenco di funzionalità da annunciare.<br/>                                                                                                                                     |
| [**COMPADDDEFAULT**](compadddefault.md)<br/>                     | Elenco dei componenti da installare nella configurazione predefinita.<br/>                                                                                                       |
| [**COMPADDLOCAL**](compaddlocal.md)<br/>                         | Elenco di ID componente da installare in locale.<br/>                                                                                                                         |
| [**COMPADDSOURCE**](compaddsource.md)<br/>                       | Elenco di ID componente da eseguire dal supporto di origine.<br/>                                                                                                                        |
| [**FILEADDDEFAULT**](fileadddefault.md)<br/>                     | Elenco di chiavi di file per i file da installare nella configurazione predefinita.<br/>                                                                                              |
| [**FILEADDLOCAL**](fileaddlocal.md)<br/>                         | Elenco di chiavi di file per i file da eseguire in locale.<br/>                                                                                                                         |
| [**FILEADDSOURCE**](fileaddsource.md)<br/>                       | Elenco di chiavi di file da eseguire dal supporto di origine.<br/>                                                                                                                     |
| [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)<br/>       | L'impostazione di questa proprietà impedisce l'applicazione di patch all'utente con privilegi minimi di un'applicazione.<br/>                                                                                 |
| [**MsiPatchRemovalList**](msipatchremovallist.md)<br/>           | Elenco di patch da rimuovere durante l'installazione.<br/>                                                                                                                 |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)<br/> | Specifica se il pacchetto usa la [funzionalità Gestione riavvio](../rstmgr/restart-manager-portal.md) [o FilesInUse.](filesinuse-dialog.md)<br/>                                          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)<br/>           | Specifica in che modo le applicazioni o i servizi che attualmente usano i file interessati da un aggiornamento devono essere arrestati e riavviati per abilitare l'installazione dell'aggiornamento.<br/> |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)<br/>                       | Specifica la modalità di arresto delle applicazioni o dei servizi che attualmente usano i file interessati da un aggiornamento per abilitare l'installazione dell'aggiornamento.<br/>               |
| [**MSIPATCHREMOVE**](msipatchremove.md)<br/>                     | L'impostazione di questa proprietà rimuove le patch.<br/>                                                                                                                                 |
| [**BENDA**](patch.md)<br/>                                       | L'impostazione di questa proprietà applica una patch.<br/>                                                                                                                                 |
| [**REINSTALL**](reinstall.md)<br/>                               | Elenco di funzionalità da reinstallare.<br/>                                                                                                                                    |
| [**REINSTALLMODE**](reinstallmode.md)<br/>                       | Stringa contenente lettere che specificano il tipo di reinstallazione da eseguire.<br/>                                                                                          |
| [**RIMUOVERE**](remove.md)<br/>                                     | Elenco di funzionalità da rimuovere.<br/>                                                                                                                                        |



 

## <a name="hardware-properties"></a>Proprietà hardware

L'elenco seguente identifica le proprietà hardware impostate dal Windows installer all'avvio.




| Proprietà | Descrizione | 
|----------|-------------|
| <a href="alpha.md"><strong>Alfa</strong></a><br /> | Livello del processore numerico durante l'esecuzione in un processore Alpha.<br /><blockquote>[!Note]<br />Questa proprietà è obsoleta, la piattaforma Alpha non è supportata Windows Installer.</blockquote><br /> | 
| <a href="borderside.md"><strong>Bordo bordo</strong></a><br /> | Larghezza dei bordi della finestra, in pixel.<br /> | 
| <a href="bordertop.md"><strong>BorderTop</strong></a><br /> | Altezza dei bordi della finestra, in pixel.<br /> | 
| <a href="captionheight.md"><strong>CaptionHeight</strong></a><br /> | Altezza dell'area del sottotitolo normale, in pixel.<br /> | 
| <a href="colorbits.md"><strong>ColorBits</strong></a><br /> | Numero di bit di colore adiacenti per ogni pixel.<br /> | 
| <a href="intel.md"><strong>Intel</strong></a><br /> | Livello del processore numerico durante l'esecuzione in un processore Intel.<br /> | 
| <a href="intel64.md"><strong>Intel64</strong></a><br /> | Livello del processore numerico durante l'esecuzione in un processore Itanium.<br /> | 
| <a href="msix64.md"><strong>Msix64</strong></a><br /> | Livello del processore numerico in esecuzione in un processore x64.<br /> | 
| <a href="physicalmemory.md"><strong>PhysicalMemory</strong></a><br /> | Dimensioni della RAM installata, in megabyte.<br /> | 
| <a href="screenx.md"><strong>ScreenX</strong></a><br /> | Larghezza dello schermo, in pixel.<br /> | 
| <a href="screeny.md"><strong>ScreenY</strong></a><br /> | Altezza dello schermo, in pixel.<br /> | 
| <a href="textheight.md"><strong>TextHeight</strong></a><br /> | Altezza dei caratteri, in unità logiche.<br /> | 
| <a href="virtualmemory.md"><strong>VirtualMemory</strong></a><br /> | Quantità di spazio disponibile in megabyte per il file di pagina.<br /> | 




 

## <a name="installation-status-properties"></a>Proprietà dello stato dell'installazione

Nell'elenco seguente vengono forniti collegamenti a altre informazioni sulle proprietà di stato aggiornate dal programma di installazione durante l'installazione.



| Proprietà                                                                      | Descrizione                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AFTERREBOOT**](afterreboot.md)<br/>                                 | Indica che l'installazione corrente segue un riavvio richiamato [dall'azione ForceReboot.](forcereboot-action.md)<br/>                                                                                                                                                |
| [**CostingComplete**](costingcomplete.md)<br/>                         | Indica se la determinazione dei costi dello spazio su disco è completa.<br/>                                                                                                                                                                                                             |
| [**Installato**](installed.md)<br/>                                     | Indica che un prodotto è già installato.<br/>                                                                                                                                                                                                                |
| [**MSICHECKCRCS**](msicheckcrcs.md)<br/>                               | Il programma di installazione esegue un CRC sui file solo se è impostata la [**proprietà MSICHECKCRCS.**](msicheckcrcs.md)<br/>                                                                                                                                                           |
| [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)<br/> | Il programma di installazione imposta questa proprietà sulla chiave di sessione per la [sessione di Gestione riavvio.](../rstmgr/restart-manager-portal.md)<br/>                                                                                                                                                         |
| [**MsiRunningElevated**](msirunningelevated-.md)<br/>                  | Il programma di installazione imposta il valore di questa proprietà su 1 quando il programma di installazione è in esecuzione con [*privilegi*](e-gly.md) elevati.<br/>                                                                                                                   |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)<br/>           | Il programma di installazione imposta questa proprietà su 1 se il riavvio del sistema operativo è attualmente in sospeso.<br/>                                                                                                                                                              |
| [**MsiUIHideCancel**](msiuihidecancel.md)<br/>                         | Il programma di [**installazione imposta MsiUIHideCancel**](msiuihidecancel.md) su 1 quando il livello di installazione interno include **INSTALLUILEVEL \_ HIDECANCEL**.<br/>                                                                                                                   |
| [**MsiUIProgressOnly**](msiuiprogressonly.md)<br/>                     | Il programma di installazione [**imposta MsiUIProgressOnly**](msiuiprogressonly.md) su 1 quando il livello di installazione interno include **INSTALLUILEVEL \_ PROGRESSONLY**.<br/>                                                                                                             |
| [**MsiUISourceResOnly**](msiuisourceresonly.md)<br/>                   | [**MsiUISourceResOnly su**](msiuisourceresonly.md) 1 (uno) quando il livello di installazione interno include **INSTALLUILEVEL \_ SOURCERESONLY**.<br/>                                                                                                                       |
| [**NOCOMPANYNAME**](nocompanyname.md)<br/>                             | Elimina l'impostazione automatica della [**proprietà COMPANYNAME.**](companyname.md)<br/>                                                                                                                                                                          |
| [**NOUSERNAME**](nousername.md)<br/>                                   | Elimina l'impostazione automatica della proprietà [**USERNAME.**](username.md)<br/>                                                                                                                                                                                |
| [**OutOfDiskSpace**](outofdiskspace.md)<br/>                           | Spazio su disco insufficiente per supportare l'installazione.<br/>                                                                                                                                                                                                      |
| [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)<br/>                   | Spazio su disco insufficiente con rollback disattivato.<br/>                                                                                                                                                                                                             |
| [**Preselezionato**](preselected.md)<br/>                                 | Le funzionalità sono già selezionate.<br/>                                                                                                                                                                                                                                |
| [**PrimaryVolumePath**](primaryvolumepath.md)<br/>                     | Il programma di installazione imposta il valore di questa proprietà sul percorso del volume designato [**dalla proprietà PRIMARYFOLDER.**](primaryfolder.md)<br/>                                                                                                                  |
| [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md)<br/> | Il programma di installazione imposta il valore di questa proprietà su una stringa che rappresenta il numero totale di byte disponibili nel volume a cui fa riferimento la [**proprietà PrimaryVolumePath.**](primaryvolumepath.md)<br/>                                                      |
| [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md)<br/> | Il programma di installazione imposta il valore di questa proprietà su una stringa che rappresenta il numero totale di byte rimanenti nel volume a cui fa riferimento la proprietà [**PrimaryVolumePath**](primaryvolumepath.md) se sono installate tutte le funzionalità attualmente selezionate.<br/> |
| [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)<br/>   | Il programma di installazione imposta il valore di questa proprietà su una stringa che rappresenta il numero totale di byte richiesti da tutte le funzionalità attualmente selezionate nel volume a cui fa riferimento la [**proprietà PrimaryVolumePath.**](primaryvolumepath.md)<br/>                    |
| [**ProductLanguage**](productlanguage.md)<br/>                         | Identificatore di lingua numerico (LANGID) per il database. (OBBLIGATORIO)<br/>                                                                                                                                                                                             |
| [**ReplacedInUseFiles**](replacedinusefiles.md)<br/>                   | Impostare se il programma di installazione viene installato su un file in uso.<br/>                                                                                                                                                                                          |
| [**RIASSUMERE**](resume.md)<br/>                                           | Ripresa dell'installazione.<br/>                                                                                                                                                                                                                                         |
| [**RollbackDisabled**](rollbackdisabled.md)<br/>                       | Il programma di installazione imposta questa proprietà quando il rollback è disabilitato.<br/>                                                                                                                                                                                                   |
| [**UILevel**](uilevel.md)<br/>                                         | Indica il livello dell'interfaccia utente.<br/>                                                                                                                                                                                                                           |
| [**UpdateStarted**](updatestarted.md)<br/>                             | Impostare quando sono state avviate le modifiche al sistema per questa installazione.<br/>                                                                                                                                                                                              |
| [**AGGIORNAMENTO DIPRODUCTCODE**](upgradingproductcode.md)<br/>               | Impostata dal programma di installazione quando un aggiornamento rimuove un'applicazione.<br/>                                                                                                                                                                                                  |
| [**VersionMsi**](versionmsi.md)<br/>                                   | Il programma di installazione imposta questa proprietà sulla versione del Windows che viene eseguita durante l'installazione.<br/>                                                                                                                                                     |



 

## <a name="operating-system-properties"></a>Proprietà del sistema operativo

Nell'elenco seguente vengono forniti collegamenti a altre informazioni sulle proprietà del sistema operativo impostate dal programma di installazione all'avvio.



| Nome della proprietà                                                                             | Breve descrizione                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdminUser**](adminuser.md)<br/>                                                 | Impostare su Windows 2000 se l'utente ha privilegi di amministratore.<br/>                                                                                                                                                                                                                        |
| [**Nomecomputer**](computername.md)<br/>                                           | Nome computer del sistema corrente.<br/>                                                                                                                                                                                                                                                 |
| [**MsiNetAssemblySupport**](msinetassemblysupport.md)<br/>                         | Nei sistemi che supportano assembly Common Language Runtime, il programma di installazione imposta il valore di questa proprietà sulla versione del file fusion.dll. Il programma di installazione non imposta questa proprietà se il sistema operativo non supporta assembly Common Language Runtime.<br/>                   |
| [**MsiNTProductType**](msintproducttype.md)<br/>                                   | Indica il tipo Windows prodotto.<br/>                                                                                                                                                                                                                                                  |
| [**MsiNTSuiteBackOffice**](msintsuitebackoffice.md)<br/>                           | Nei Windows 2000 e versioni successive, il programma di installazione imposta questa proprietà su 1 (uno) solo se sono installati i componenti di Microsoft BackOffice.<br/>                                                                                                                                      |
| [**MsiNTSuiteDataCenter**](msintsuitedatacenter.md)<br/>                           | Nei Windows 2000 e versioni successive, il programma di installazione imposta questa proprietà su 1 (uno) solo se è installato Windows 2000 Datacenter Server.<br/>                                                                                                                                        |
| [**MsiNTSuiteEnterprise**](msintsuiteenterprise.md)<br/>                           | Nei Windows 2000 e versioni successive, il programma di installazione imposta questa proprietà su 1 (uno) solo se è installato Windows 2000 Advanced Server.<br/>                                                                                                                                          |
| [**MsiNTSuitePersonal**](msintsuitepersonal.md)<br/>                               | In Windows XP e versioni successive, il programma di installazione imposta questa proprietà su 1 (uno) solo se il sistema operativo è Home (non Professional).<br/>                                                                                                                                      |
| [**MsiNTSuiteSmallBusiness**](msintsuitesmallbusiness.md)<br/>                     | Nei Windows 2000 e versioni successive, il programma di installazione imposta questa proprietà su 1 (uno) solo se è installato Microsoft Small Business Server.<br/>                                                                                                                                       |
| [**MsiNTSuiteSmallBusinessRestricted**](msintsuitesmallbusinessrestricted.md)<br/> | Nei Windows 2000 e versioni successive, il programma di installazione imposta questa proprietà su 1 (uno) solo se Microsoft Small Business Server è installato con la licenza client restrittiva.<br/>                                                                                                   |
| [**MsiNTSuiteWebServer**](msintsuitewebserver.md)<br/>                             | Nei sistemi operativi Windows 2000 e versioni successive, il programma di installazione imposta la proprietà [**MsiNTSuiteWebServer**](msintsuitewebserver.md) su 1 (uno) se è installata l'edizione Web di Windows Server 2003. Disponibile solo con la versione Windows Server 2003 del programma di Windows installazione.<br/> |
| [**MsiTabletPC**](msitabletpc.md)<br/>                                             | Il programma di installazione imposta questa proprietà su un valore diverso da zero se il sistema operativo corrente è Windows XP Tablet PC Edition.<br/>                                                                                                                                                                 |
| [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md)<br/>                     | Nei sistemi che supportano assembly Win32, il programma di installazione imposta il valore di questa proprietà sulla versione del file di sxs.dll. Il programma di installazione non imposta questa proprietà se il sistema operativo non supporta gli assembly Win32.<br/>                                                          |
| [**OLEAdvtSupport**](oleadvtsupport.md)<br/>                                       | Impostare se OLE supporta il programma Windows programma di installazione.<br/>                                                                                                                                                                                                                                           |
| [**RedirectedDllSupport**](redirecteddllsupport.md)<br/>                           | Il programma di installazione imposta la [**proprietà RedirectedDllSupport**](redirecteddllsupport.md) se il sistema che esegue l'installazione supporta [Componenti isolati](isolated-components.md).<br/>                                                                                              |
| [**RemoteAdminTS**](remoteadmints.md)<br/>                                         | Il programma di installazione imposta [**la proprietà RemoteAdminTS**](remoteadmints.md) quando il sistema è un server di amministrazione remota che esegue il servizio ruolo Terminal Server.<br/>                                                                                                                   |
| [**ServicePackLevel**](servicepacklevel.md)<br/>                                   | Numero di versione del Service Pack del sistema operativo.<br/>                                                                                                                                                                                                                             |
| [**ServicePackLevelMinor**](servicepacklevelminor.md)<br/>                         | Numero di versione secondaria del Service Pack del sistema operativo.<br/>                                                                                                                                                                                                                       |
| [**SharedWindows**](sharedwindows.md)<br/>                                         | Impostare quando il sistema funziona come Windows.<br/>                                                                                                                                                                                                                                  |
| [**ShellAdvtSupport**](shelladvtsupport.md)<br/>                                   | Impostare se la shell supporta la funzionalità pubblicitaria.<br/>                                                                                                                                                                                                                                       |
| [**SystemLanguageID**](systemlanguageid.md)<br/>                                   | Identificatore di lingua predefinito per il sistema.<br/>                                                                                                                                                                                                                                          |
| [**TerminalServer**](terminalserver.md)<br/>                                       | Impostare quando il sistema è un server che esegue il servizio ruolo Terminal Server.<br/>                                                                                                                                                                                                            |
| [**TTCSupport**](ttcsupport.md)<br/>                                               | Indica se il sistema operativo supporta l'uso di file con estensione ttc (raccolte di tipi di carattere true).<br/>                                                                                                                                                                                            |
| [**Versione9X**](version9x.md)<br/>                                                 | Numero di versione per il Windows operativo.<br/>                                                                                                                                                                                                                                     |
| [**VersionDatabase**](versiondatabase.md)<br/>                                     | Versione numerica del database dell'installazione corrente.<br/>                                                                                                                                                                                                                                |
| [**VersionNT**](versionnt.md)<br/>                                                 | Numero di versione per il sistema operativo.<br/>                                                                                                                                                                                                                                             |
| [**VersionNT64**](versionnt64.md)<br/>                                             | Numero di versione del sistema operativo se il sistema è in esecuzione in un computer a 64 bit.<br/>                                                                                                                                                                                               |
| [**Windows compilazione**](windowsbuild.md)<br/>                                          | Numero di build del sistema operativo.<br/>                                                                                                                                                                                                                                                |



 

## <a name="product-information-properties"></a>Proprietà delle informazioni sul prodotto

Nell'elenco seguente vengono forniti collegamenti a ulteriori informazioni sulle proprietà specifiche del prodotto specificate nella [tabella delle proprietà](property-table.md).



| Nome della proprietà                                                  | Breve descrizione                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)<br/>                  | Indirizzo Internet o URL per il supporto tecnico.<br/>                                                                                 |
| [**ARPHELPTELEPHONE**](arphelptelephone.md)<br/>        | Numeri di telefono del supporto tecnico.<br/>                                                                                               |
| [**DiskPrompt**](diskprompt.md)<br/>                    | Stringa visualizzata da una finestra di messaggio che richiede un disco.<br/>                                                                     |
| [**IsAdminPackage**](isadminpackage.md)<br/>            | Impostare su 1 (uno) se l'installazione corrente è in esecuzione da un pacchetto creato tramite un'installazione amministrativa.<br/>           |
| [**LeftUnit**](leftunit.md)<br/>                        | Posiziona le unità a sinistra del numero.<br/>                                                                                        |
| [**Produttore**](manufacturer.md)<br/>                | Nome del produttore dell'applicazione. (Obbligatorio)<br/>                                                                               |
| [**MediaSourceDir**](mediasourcedir.md)<br/>            | Il programma di installazione imposta questa proprietà su 1 (uno) quando l'installazione usa un'origine supporto, ad esempio un CD-ROM.<br/>                       |
| [**MSIINSTANCEGUID**](msiinstanceguid.md)<br/>          | La presenza di questa proprietà indica che una trasformazione di modifica del codice prodotto è registrata nel prodotto.<br/>                   |
| [**MSINEWINSTANCE**](msinewinstance.md)<br/>            | Questa proprietà indica l'installazione di una nuova istanza di un prodotto con trasformazioni di istanza.<br/>                              |
| [**ParentProductCode**](parentoriginaldatabase.md)<br/> | Il programma di installazione imposta questa proprietà per le installazioni eseguite da [un'azione di](concurrent-installations.md) installazione simultanea.<br/> |
| [**PIDTemplate**](pidtemplate.md)<br/>                  | Stringa utilizzata come modello per la [**proprietà PIDKEY.**](pidkey.md)<br/>                                                           |
| [**ProductCode**](productcode.md)<br/>                  | Identificatore univoco per una versione specifica del prodotto. (Obbligatorio)<br/>                                                                 |
| [**ProductName**](productname.md)<br/>                  | Nome leggibile di un'applicazione. (Obbligatorio)<br/>                                                                              |
| [**ProductState**](productstate.md)<br/>                | Impostare sullo stato installato di un prodotto.<br/>                                                                                       |
| [**ProductVersion**](productversion.md)<br/>            | Formato stringa della versione del prodotto come valore numerico. (Obbligatorio)<br/>                                                            |
| [**Codice di aggiornamento**](upgradecode.md)<br/>                  | GUID che rappresenta un set correlato di prodotti.<br/>                                                                              |



 

## <a name="summary-information-update-properties"></a>Proprietà di aggiornamento delle informazioni di riepilogo

Le proprietà seguenti vengono impostate solo dalle trasformazioni nei file msp utilizzati per aggiornare il flusso di informazioni di riepilogo di un'immagine amministrativa.



| Proprietà                                                              | Descrizione                                                                                                                  |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md)<br/>         | Il valore di questa proprietà viene scritto nella proprietà [**Riepilogo numero revisione.**](revision-number-summary.md)<br/> |
| [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)<br/> | Il valore di questa proprietà viene scritto nella [**proprietà Riepilogo**](comments-summary.md) commenti.<br/>               |
| [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)<br/>   | Il valore di questa proprietà viene scritto nella proprietà [**Riepilogo**](subject-summary.md) oggetto.<br/>                 |



 

## <a name="system-folder-properties"></a>Proprietà cartella di sistema

Nell'elenco seguente vengono forniti collegamenti a altre informazioni sulle cartelle di sistema impostate dal programma di installazione al momento dell'installazione.



| Proprietà                                                        | Descrizione                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**AdminToolsFolder**](admintoolsfolder.md)<br/>         | Percorso completo della directory che contiene gli strumenti di amministrazione.<br/>         |
| [**AppDataFolder**](appdatafolder.md)<br/>               | Percorso completo della cartella **Roaming** per l'utente corrente.<br/>              |
| [**CommonAppDataFolder**](commonappdatafolder.md)<br/>   | Percorso completo dei dati dell'applicazione per tutti gli utenti.<br/>                           |
| [**CommonFiles64Folder**](commonfiles64folder.md)<br/>   | Percorso completo della cartella file **comuni a 64 bit** predefinita.<br/>            |
| [**CommonFilesFolder**](commonfilesfolder.md)<br/>       | Percorso completo della cartella **File comuni** per l'utente corrente.<br/>         |
| [**DesktopFolder**](desktopfolder.md)<br/>               | Percorso completo della **cartella Desktop.**<br/>                                   |
| [**Cartella Preferiti**](favoritesfolder.md)<br/>           | Percorso completo della cartella **Preferiti** per l'utente corrente.<br/>            |
| [**FontsFolder**](fontsfolder.md)<br/>                   | Percorso completo della cartella **Fonts.**<br/>                                     |
| [**LocalAppDataFolder**](localappdatafolder.md)<br/>     | Percorso completo della cartella che contiene applicazioni locali (non in roaming).<br/> |
| [**Cartella MyPictures**](mypicturesfolder.md)<br/>         | Percorso completo della **cartella** Immagini.<br/>                                  |
| [**NetHoodFolder**](nethoodfolder.md)<br/>               | Percorso completo della cartella **NetHood.**<br/>                                   |
| [**PersonalFolder**](personalfolder.md)<br/>             | Percorso completo della cartella **Documenti** per l'utente corrente.<br/>            |
| [**PrintHoodFolder**](printhoodfolder.md)<br/>           | Percorso completo della **cartella PrintHood.**<br/>                                 |
| [**ProgramFiles64Folder**](programfiles64folder.md)<br/> | Percorso completo della cartella predefinita **Programmi a 64 bit.**<br/>           |
| [**Cartella ProgramFilesFolder**](programfilesfolder.md)<br/>     | Percorso completo della cartella predefinita **Programmi a 32 bit.**<br/>           |
| [**Cartella ProgramMenuFolder**](programmenufolder.md)<br/>       | Percorso completo della **cartella Menu di** programma.<br/>                              |
| [**RecentFolder**](recentfolder.md)<br/>                 | Percorso completo della **cartella** Recenti.<br/>                                    |
| [**SendToFolder**](sendtofolder.md)<br/>                 | Percorso completo della cartella **SendTo** per l'utente corrente.<br/>               |
| [**StartMenuFolder**](startmenufolder.md)<br/>           | Percorso completo della cartella **menu Start.**<br/>                                |
| [**StartupFolder**](startupfolder.md)<br/>               | Percorso completo della **cartella Startup.**<br/>                                   |
| [**System16Folder**](system16folder.md)<br/>             | Percorso completo della cartella per le DLL di sistema a 16 bit.<br/>                            |
| [**System64Folder**](system64folder.md)<br/>             | Percorso completo della cartella **System64** predefinita.<br/>                       |
| [**Cartella di sistema**](systemfolder.md)<br/>                 | Percorso completo della cartella **System** per l'utente corrente.<br/>               |
| [**TempFolder**](tempfolder.md)<br/>                     | Percorso completo della **cartella** Temp.<br/>                                      |
| [**TemplateFolder**](templatefolder.md)<br/>             | Percorso completo della cartella **Modello** per l'utente corrente.<br/>             |
| [**Cartella Windows**](windowsfolder.md)<br/>               | Percorso completo della cartella **Windows.**<br/>                                   |
| [**WindowsVolume**](windowsvolume.md)<br/>               | Volume della cartella **Windows** locale.<br/>                                      |



 

## <a name="user-information-properties"></a>Proprietà delle informazioni utente

Nell'elenco seguente vengono forniti collegamenti a altre informazioni sulle informazioni fornite dall'utente.



| Proprietà                                                      | Descrizione                                                                             |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AdminProperties**](adminproperties.md)<br/>         | Elenco di proprietà impostate durante un'installazione di amministrazione.<br/>       |
| [**COMPANYNAME**](companyname.md)<br/>                 | Nome dell'organizzazione dell'utente che esegue l'installazione.<br/>            |
| [**Logonuser**](logonuser.md)<br/>                     | Nome utente per l'utente attualmente connesso.<br/>                           |
| [**MsiHiddenProperties**](msihiddenproperties.md)<br/> | Elenco di proprietà che non possono essere scritte nel log.<br/>       |
| [**PIDKEY**](pidkey.md)<br/>                           | Parte dell'ID prodotto immesso dall'utente.<br/>                                 |
| [**Productid**](productid.md)<br/>                     | ID prodotto completo dopo una convalida riuscita.<br/>                               |
| [**UserLanguageID**](userlanguageid.md)<br/>           | Identificatore di lingua predefinito dell'utente corrente.<br/>                             |
| [**NOME UTENTE**](username.md)<br/>                       | Utente che esegue l'installazione.<br/>                                     |
| [**UserSID - proprietà**](usersid.md)<br/>                | Impostata dal programma di installazione in base all'identificatore di sicurezza (SID) dell'utente.<br/> |



 

 

 
