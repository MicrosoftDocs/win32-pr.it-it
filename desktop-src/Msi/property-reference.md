---
description: 'In questa sezione sono elencate le proprietà definite da Windows Installer:'
ms.assetid: c91119b9-59d5-4a33-91cd-d3ba63659d12
title: Riferimento alla proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2ae30800d3c718549ecc887e3438d743881f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756485"
---
# <a name="property-reference"></a>Riferimento alla proprietà

In questa sezione sono elencate le proprietà definite da Windows Installer:

-   [Proprietà percorso componente](#component-location-properties)
-   [Proprietà di configurazione](#configuration-properties)
-   [Proprietà data, ora](#date-time-properties)
-   [Proprietà opzioni di installazione funzionalità](#feature-installation-options-properties)
-   [Proprietà hardware](#hardware-properties)
-   [Proprietà stato installazione](#installation-status-properties)
-   [Proprietà del sistema operativo](#operating-system-properties)
-   [Proprietà informazioni sul prodotto](#product-information-properties)
-   [Proprietà aggiornamento informazioni di riepilogo](#summary-information-update-properties)
-   [Proprietà cartella di sistema](#system-folder-properties)
-   [Proprietà informazioni utente](#user-information-properties)

È possibile specificare proprietà aggiuntive mediante dati creati o azioni personalizzate. Le proprietà con nomi che non contengono lettere minuscole sono proprietà pubbliche e possono essere specificate nella riga di comando.

Per informazioni sui valori della chiave del registro di sistema **Disinstalla** fornita dalle proprietà del programma di installazione, vedere [Disinstalla chiave del registro di sistema](uninstall-registry-key.md).

## <a name="component-location-properties"></a>Proprietà percorso componente

Nell'elenco seguente vengono forniti i collegamenti a ulteriori informazioni sulle proprietà del percorso dei componenti.



| Proprietà                                                            | Descrizione                                                                                                                                                                                                        |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OriginalDatabase**](originaldatabase.md)<br/>             | Il programma di installazione imposta questa proprietà sul database avviato, ovvero sul database nell'origine o sul database memorizzato nella cache.<br/>                                                                                     |
| [**ParentOriginalDatabase**](parentoriginaldatabase.md)<br/> | Il programma di installazione imposta questa proprietà per le installazioni eseguite da un'azione di [installazione simultanea](concurrent-installations.md) .<br/>                                                                             |
| [**SourceDir**](sourcedir.md)<br/>                           | Directory radice che contiene i file di origine.<br/>                                                                                                                                                          |
| [**TARGETDIR**](targetdir.md)<br/>                           | Specifica la directory di destinazione radice per l'installazione. Durante un' [installazione amministrativa](administrative-installation.md) questa proprietà è il percorso in cui copiare il pacchetto di installazione.<br/> |



 

## <a name="configuration-properties"></a>Configuration Properties

Nell'elenco seguente vengono forniti i collegamenti ad altre informazioni sulle altre proprietà configurabili.



| Proprietà                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AZIONE**](action.md)<br/>                                                     | Azione iniziale chiamata dopo l'inizializzazione del programma di installazione.<br/>                                                                                                                                                                                                                                                                                                                          |
| [**ALLUSERS**](allusers.md)<br/>                                                 | Determina la posizione di archiviazione delle informazioni di configurazione.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)<br/>                     | URL del canale di aggiornamento per un'applicazione.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**ARPCOMMENTS**](arpcomments.md)<br/>                                           | Fornisce commenti per **Installazione applicazioni** nel **Pannello di controllo**.<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPCONTACT**](arpcontact.md)<br/>                                             | Fornisce il contatto per **Installazione applicazioni** nel pannello di **controllo**.<br/>                                                                                                                                                                                                                                                                                                          |
| [**ARPINSTALLLOCATION**](arpinstalllocation.md)<br/>                             | Percorso completo della cartella principale di un'applicazione.<br/>                                                                                                                                                                                                                                                                                                                      |
| [**ARPNOMODIFY**](arpnomodify.md)<br/>                                           | Disabilita la funzionalità di modifica di un prodotto.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**ARPNOREMOVE**](arpnoremove.md)<br/>                                           | Disabilita la funzionalità che rimuove un prodotto.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPNOREPAIR**](arpnorepair.md)<br/>                                           | Disabilita il pulsante **Ripristina** nella creazione guidata programmi.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**ARPPRODUCTICON**](arpproducticon.md)<br/>                                     | Specifica l'icona primaria per il pacchetto di installazione.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ARPREADME**](arpreadme.md)<br/>                                               | Fornisce un **file Leggimi** per **Installazione applicazioni** nel pannello di **controllo**.<br/>                                                                                                                                                                                                                                                                                                     |
| [**ARPSIZE**](arpsize.md)<br/>                                                   | Dimensioni stimate di un'applicazione, espressa in kilobyte.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPSYSTEMCOMPONENT**](arpsystemcomponent.md)<br/>                             | Impedisce la visualizzazione di un'applicazione nell'elenco **Installazione applicazioni** .<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPURLINFOABOUT**](arpurlinfoabout.md)<br/>                                   | URL per il home page di un'applicazione.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)<br/>                                 | URL per le informazioni di aggiornamento dell'applicazione.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**AVAILABLEFREEREG**](availablefreereg.md)<br/>                                 | Spazio del registro di sistema (in kilobyte) richiesto da un'applicazione. Utilizzato dall' [azione AllocateRegistrySpace](allocateregistryspace-action.md).<br/>                                                                                                                                                                                                                                              |
| [**\_unità CCP**](ccp-drive.md)<br/>                                              | Percorso radice per i prodotti idonei per CCP.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**DefaultUIFont**](defaultuifont.md)<br/>                                       | Stile del carattere predefinito usato per i controlli.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md)<br/>                         | Impostare questa impostazione per disabilitare la generazione di collegamenti specifici che supportano l' [installazione su richiesta](installation-on-demand.md).<br/>                                                                                                                                                                                                                                                            |
| [**DISABLEMEDIA**](-disablemedia.md)<br/>                                        | Impedisce al programma di installazione di registrare origini multimediali, ad esempio CD-ROM, come origini valide per il prodotto.<br/>                                                                                                                                                                                                                                                                        |
| [**DISABLEROLLBACK**](-disablerollback.md)<br/>                                  | Disabilita il rollback per la configurazione corrente.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**EXECUTEACTION**](executeaction.md)<br/>                                       | Azione di primo livello avviata da ExecuteAction.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**EXECUTEMODE**](executemode.md)<br/>                                           | Modalità di esecuzione eseguita dal programma di installazione.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**FASTOEM**](fastoem.md)<br/>                                                   | Migliora le prestazioni di installazione in scenari OEM specifici.<br/>                                                                                                                                                                                                                                                                                                                    |
| [**INSTALLLEVEL**](installlevel.md)<br/>                                         | Livello iniziale di installazione delle funzionalità.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**LIMITUI**](limitui.md)<br/>                                                   | Livello dell'interfaccia utente limitato come di base.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**LOGACTION**](logaction.md)<br/>                                               | Elenco dei nomi di azione da registrare.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**MEDIAPACKAGEPATH**](mediapackagepath.md)<br/>                                 | Questa proprietà deve essere impostata sul percorso relativo se il pacchetto di installazione non si trova nella directory principale del CD-ROM.<br/>                                                                                                                                                                                                                                                               |
| [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)<br/>                 | Questa proprietà facoltativa contiene un elenco delimitato da punti e virgola dei percorsi del registro di sistema in cui l'applicazione archivia le impostazioni e le preferenze di un utente. Disponibile con Windows Installer 4,0.<br/>                                                                                                                                                                                        |
| [**MSIDISABLEEEUI**](msidisableeeui.md)<br/>                                     | Disabilitare l'interfaccia utente incorporata per l'installazione.<br/> **[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato.<br/>                                                                                                                                                                                                           |
| [**MSIFASTINSTALL**](msifastinstall.md)<br/>                                     | Ridurre il tempo necessario per installare un pacchetto di Windows Installer di grandi dimensioni.<br/> **[Windows Installer 4,5 e versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.<br/>                                                                                                                                                                                              |
| [**MSIINSTALLPERUSER**](msiinstallperuser.md)<br/>                               | Richiede che il Windows Installer installare il pacchetto solo per l'utente corrente.<br/> **[Windows Installer 4,5 e versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.<br/>                                                                                                                                                                                  |
| [**MSINODISABLEMEDIA**](msinodisablemedia.md)<br/>                               | Impostare questa proprietà per impedire al programma di installazione di impostare la proprietà [**DISABLEMEDIA**](-disablemedia.md) .<br/>                                                                                                                                                                                                                                                                        |
| [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)<br/>   | Impostare questa proprietà su 1 (uno) nella riga di comando o nella [tabella delle proprietà](property-table.md) per applicare le regole del componente di aggiornamento durante [piccoli aggiornamenti](small-updates.md) e [aggiornamenti secondari](minor-upgrades.md) di un prodotto specifico. Disponibile a partire da Windows Installer 3,0.<br/>                                                                                     |
| [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)<br/> | Quando questa proprietà è stata impostata su 1, il programma di installazione può annullare la registrazione e disinstallare i componenti ridondanti per evitare di lasciare i componenti orfani nel computer.<br/> **[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato.<br/>                                                                                                  |
| [**PRIMARYFOLDER**](primaryfolder.md)<br/>                                       | Consente all'autore di designare una cartella primaria per un'installazione. Usato per determinare i valori per le proprietà [**PrimaryVolumePath**](primaryvolumepath.md), [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md), [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)e [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) .<br/> |
| [**Con privilegi**](privileged.md)<br/>                                             | Esegue un'installazione con privilegi elevati.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md)<br/>                             | Azione se lo spazio su disco è insufficiente per l'installazione.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**RIAVVIO**](reboot.md)<br/>                                                     | Forza o disattiva un riavvio.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**REBOOTPROMPT**](rebootprompt.md)<br/>                                         | Evita la visualizzazione di richieste di riavvio per l'utente. Tutti i riavvii necessari avvengono automaticamente.<br/>                                                                                                                                                                                                                                                                     |
| [**ROOTDRIVE**](rootdrive.md)<br/>                                               | Unità predefinita per un'installazione.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SEQUENCE**](sequence.md)<br/>                                                 | Tabella con lo schema della tabella di sequenza.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**SHORTFILENAMES**](shortfilenames.md)<br/>                                     | Causa l'utilizzo di nomi di file brevi.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**TRASFORMA**](transforms.md)<br/>                                             | Elenco di trasformazioni da applicare a un database.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**TRANSFORMSATSOURCE**](transformsatsource.md)<br/>                             | Informa il programma di installazione che le trasformazioni per un prodotto si trovano nell'origine.<br/>                                                                                                                                                                                                                                                                                                      |
| [**TRANSFORMSSECURE**](transformssecure.md)<br/>                                 | L'impostazione della proprietà [**TRANSFORMSECURE**](transformssecure.md) su 1 (uno) informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache localmente nel computer utente in una posizione in cui l'utente non dispone dell'accesso in scrittura.<br/>                                                                                                                                                           |
| [**MsiLogFileLocation**](msilogfilelocation.md)<br/>                             | Il programma di installazione imposta il valore di questa proprietà sul percorso completo del file di log quando è stata abilitata la registrazione. Questa proprietà è disponibile a partire da Windows Installer 4,0.<br/>                                                                                                                                                                                                     |
| [**MsiLogging**](msilogging.md)<br/>                                             | Imposta la modalità di registrazione predefinita per il pacchetto di Windows Installer. Questa proprietà è disponibile a partire da Windows Installer 4,0.<br/>                                                                                                                                                                                                                                                   |
| [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)<br/>                 | Impostare questa proprietà su 1 per richiedere al programma di installazione di utilizzare le informazioni utente effettive quando si imposta la proprietà [**AdminUser**](adminuser.md) . Questa proprietà è disponibile a partire da Windows Installer 4,0.<br/>                                                                                                                                                                         |



 

## <a name="date-time-properties"></a>Proprietà data, ora

Le proprietà di [**Data**](date.md) e [**ora**](time.md) sono proprietà attive impostate dal programma di installazione quando vengono estratti i dati.



| Proprietà                        | Descrizione                  |
|---------------------------------|------------------------------|
| [**Date**](date.md)<br/> | Data corrente.<br/> |
| [**Tempo**](time.md)<br/> | Ora corrente.<br/> |



 

## <a name="feature-installation-options-properties"></a>Proprietà opzioni di installazione funzionalità

Nell'elenco seguente vengono forniti i collegamenti a ulteriori informazioni sulle proprietà delle opzioni di installazione delle funzionalità.



| Proprietà                                                                | Descrizione                                                                                                                                                                       |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADDDEFAULT**](adddefault.md)<br/>                             | Elenco di funzionalità da installare nella configurazione predefinita.<br/>                                                                                                         |
| [**ADDLOCAL**](addlocal.md)<br/>                                 | Elenco di funzionalità da installare localmente.<br/>                                                                                                                              |
| [**ADDSOURCE**](addsource.md)<br/>                               | Elenco di funzionalità da eseguire dall'origine.<br/>                                                                                                                                |
| [**PUBBLICIZZARE**](advertise.md)<br/>                               | Elenco di funzionalità da annunciare.<br/>                                                                                                                                     |
| [**COMPADDDEFAULT**](compadddefault.md)<br/>                     | Elenco di componenti da installare nella configurazione predefinita.<br/>                                                                                                       |
| [**COMPADDLOCAL**](compaddlocal.md)<br/>                         | Elenco di ID di componenti da installare localmente.<br/>                                                                                                                         |
| [**COMPADDSOURCE**](compaddsource.md)<br/>                       | Elenco di ID di componenti da eseguire dal supporto di origine.<br/>                                                                                                                        |
| [**FILEADDDEFAULT**](fileadddefault.md)<br/>                     | Elenco di chiavi file per i file da installare nella configurazione predefinita.<br/>                                                                                              |
| [**FILEADDLOCAL**](fileaddlocal.md)<br/>                         | Elenco di chiavi file per i file da eseguire localmente.<br/>                                                                                                                         |
| [**FILEADDSOURCE**](fileaddsource.md)<br/>                       | Elenco di chiavi del file da eseguire dal supporto di origine.<br/>                                                                                                                     |
| [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)<br/>       | L'impostazione di questa proprietà impedisce l'applicazione di patch con privilegi minimi (LUA) per un'applicazione.<br/>                                                                                 |
| [**MsiPatchRemovalList**](msipatchremovallist.md)<br/>           | Elenco delle patch da rimuovere durante l'installazione.<br/>                                                                                                                 |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)<br/> | Specifica se il pacchetto utilizza la funzionalità [Gestione riavvio](../rstmgr/restart-manager-portal.md) o [filesinus](filesinuse-dialog.md) .<br/>                                          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)<br/>           | Specifica il modo in cui le applicazioni o i servizi che attualmente utilizzano i file interessati da un aggiornamento devono essere arrestati e riavviati per consentire l'installazione dell'aggiornamento.<br/> |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)<br/>                       | Specifica il modo in cui le applicazioni o i servizi che attualmente utilizzano i file interessati da un aggiornamento devono essere arrestati per consentire l'installazione dell'aggiornamento.<br/>               |
| [**MSIPATCHREMOVE**](msipatchremove.md)<br/>                     | Se si imposta questa proprietà, verranno rimosse le patch.<br/>                                                                                                                                 |
| [**PATCH**](patch.md)<br/>                                       | L'impostazione di questa proprietà applica una patch.<br/>                                                                                                                                 |
| [**REINSTALL**](reinstall.md)<br/>                               | Elenco di funzionalità da reinstallare.<br/>                                                                                                                                    |
| [**REINSTALLMODE**](reinstallmode.md)<br/>                       | Stringa che contiene lettere che specificano il tipo di reinstallazione da eseguire.<br/>                                                                                          |
| [**RIMUOVERE**](remove.md)<br/>                                     | Elenco di funzionalità da rimuovere.<br/>                                                                                                                                        |



 

## <a name="hardware-properties"></a>Proprietà hardware

Nell'elenco seguente vengono identificate le proprietà hardware impostate dall'Windows Installer all'avvio.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="alpha.md"><strong>Alfa</strong></a><br/></td>
<td>Livello di processore numerico durante l'esecuzione in un processore Alpha.<br/>
<blockquote>
[!Note]<br />
Questa proprietà è obsoleta, la piattaforma Alpha non è supportata da Windows Installer.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="borderside.md"><strong>BorderSide</strong></a><br/></td>
<td>Larghezza dei bordi della finestra, in pixel.<br/></td>
</tr>
<tr class="odd">
<td><a href="bordertop.md"><strong>BorderTop</strong></a><br/></td>
<td>Altezza dei bordi della finestra, in pixel.<br/></td>
</tr>
<tr class="even">
<td><a href="captionheight.md"><strong>CaptionHeight</strong></a><br/></td>
<td>Altezza della normale area della didascalia, in pixel.<br/></td>
</tr>
<tr class="odd">
<td><a href="colorbits.md"><strong>ColorBits</strong></a><br/></td>
<td>Numero di bit di colore adiacenti per ogni pixel.<br/></td>
</tr>
<tr class="even">
<td><a href="intel.md"><strong>Intel</strong></a><br/></td>
<td>Livello di processore numerico durante l'esecuzione in un processore Intel.<br/></td>
</tr>
<tr class="odd">
<td><a href="intel64.md"><strong>Intel64</strong></a><br/></td>
<td>Livello di processore numerico durante l'esecuzione in un processore Itanium.<br/></td>
</tr>
<tr class="even">
<td><a href="msix64.md"><strong>Msix64</strong></a><br/></td>
<td>Livello di processore numerico durante l'esecuzione in un processore x64.<br/></td>
</tr>
<tr class="odd">
<td><a href="physicalmemory.md"><strong>PhysicalMemory</strong></a><br/></td>
<td>Dimensioni della RAM installata, in megabyte.<br/></td>
</tr>
<tr class="even">
<td><a href="screenx.md"><strong>ScreenX</strong></a><br/></td>
<td>Larghezza dello schermo, in pixel.<br/></td>
</tr>
<tr class="odd">
<td><a href="screeny.md"><strong>ScreenY</strong></a><br/></td>
<td>Altezza dello schermo, in pixel.<br/></td>
</tr>
<tr class="even">
<td><a href="textheight.md"><strong>TextHeight</strong></a><br/></td>
<td>Altezza dei caratteri, in unità logiche.<br/></td>
</tr>
<tr class="odd">
<td><a href="virtualmemory.md"><strong>VirtualMemory</strong></a><br/></td>
<td>Quantità di spazio disponibile per i file di paging, in megabyte.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="installation-status-properties"></a>Proprietà stato installazione

Nell'elenco seguente vengono forniti i collegamenti a ulteriori informazioni sulle proprietà di stato aggiornate dal programma di installazione durante l'installazione.



| Proprietà                                                                      | Descrizione                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AFTERREBOOT**](afterreboot.md)<br/>                                 | Indica che l'installazione corrente segue un riavvio richiamato dall' [azione ForceReboot](forcereboot-action.md) .<br/>                                                                                                                                                |
| [**CostingComplete**](costingcomplete.md)<br/>                         | Indica se il costo dello spazio su disco è completo.<br/>                                                                                                                                                                                                             |
| [**Installato**](installed.md)<br/>                                     | Indica che un prodotto è già installato.<br/>                                                                                                                                                                                                                |
| [**MSICHECKCRCS**](msicheckcrcs.md)<br/>                               | Il programma di installazione esegue un CRC sui file solo se la proprietà [**MSICHECKCRCS**](msicheckcrcs.md) è impostata.<br/>                                                                                                                                                           |
| [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)<br/> | Il programma di installazione imposta questa proprietà sulla chiave di sessione per la sessione di [Gestione riavvio](../rstmgr/restart-manager-portal.md) .<br/>                                                                                                                                                         |
| [**MsiRunningElevated**](msirunningelevated-.md)<br/>                  | Il programma di installazione imposta il valore di questa proprietà su 1 quando il programma di installazione è in esecuzione con privilegi [*elevati*](e-gly.md) .<br/>                                                                                                                   |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)<br/>           | Il programma di installazione imposta questa proprietà su 1 se è attualmente in sospeso un riavvio del sistema operativo.<br/>                                                                                                                                                              |
| [**MsiUIHideCancel**](msiuihidecancel.md)<br/>                         | Il programma di installazione imposta [**MsiUIHideCancel**](msiuihidecancel.md) su 1 quando il livello di installazione interno include **INSTALLUILEVEL \_ HIDECANCEL**.<br/>                                                                                                                   |
| [**MsiUIProgressOnly**](msiuiprogressonly.md)<br/>                     | Il programma di installazione imposta [**MsiUIProgressOnly**](msiuiprogressonly.md) su 1 quando il livello di installazione interno include **INSTALLUILEVEL \_ PROGRESSONLY**.<br/>                                                                                                             |
| [**MsiUISourceResOnly**](msiuisourceresonly.md)<br/>                   | [**MsiUISourceResOnly**](msiuisourceresonly.md) su 1 (uno) quando il livello di installazione interno include **INSTALLUILEVEL \_ SOURCERESONLY**.<br/>                                                                                                                       |
| [**NoCompanyName**](nocompanyname.md)<br/>                             | Disattiva l'impostazione automatica della proprietà [**CompanyName**](companyname.md) .<br/>                                                                                                                                                                          |
| [**NOUSERNAME**](nousername.md)<br/>                                   | Disattiva l'impostazione automatica della proprietà [**username**](username.md) .<br/>                                                                                                                                                                                |
| [**OutOfDiskSpace**](outofdiskspace.md)<br/>                           | Spazio su disco insufficiente per ospitare l'installazione.<br/>                                                                                                                                                                                                      |
| [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)<br/>                   | Spazio su disco insufficiente con rollback disattivato.<br/>                                                                                                                                                                                                             |
| [**Preselezionate**](preselected.md)<br/>                                 | Le funzionalità sono già selezionate.<br/>                                                                                                                                                                                                                                |
| [**PrimaryVolumePath**](primaryvolumepath.md)<br/>                     | Il programma di installazione imposta il valore di questa proprietà sul percorso del volume designato dalla proprietà [**PRIMARYFOLDER**](primaryfolder.md) .<br/>                                                                                                                  |
| [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md)<br/> | Il programma di installazione imposta il valore di questa proprietà su una stringa che rappresenta il numero totale di byte disponibili sul volume a cui fa riferimento la proprietà [**PrimaryVolumePath**](primaryvolumepath.md) .<br/>                                                      |
| [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md)<br/> | Il programma di installazione imposta il valore di questa proprietà su una stringa che rappresenta il numero totale di byte rimanenti nel volume a cui fa riferimento la proprietà [**PrimaryVolumePath**](primaryvolumepath.md) se tutte le funzionalità attualmente selezionate sono installate.<br/> |
| [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)<br/>   | Il programma di installazione imposta il valore di questa proprietà su una stringa che rappresenta il numero totale di byte necessari per tutte le funzionalità attualmente selezionate nel volume a cui fa riferimento la proprietà [**PrimaryVolumePath**](primaryvolumepath.md) .<br/>                    |
| [**ProductLanguage**](productlanguage.md)<br/>                         | Identificatore del linguaggio numerico (LANGID) per il database. NECESSARIA<br/>                                                                                                                                                                                             |
| [**ReplacedInUseFiles**](replacedinusefiles.md)<br/>                   | Impostare se il programma di installazione viene installato su un file che viene mantenuto in uso.<br/>                                                                                                                                                                                          |
| [**RIPRENDERE**](resume.md)<br/>                                           | Ripresa dell'installazione.<br/>                                                                                                                                                                                                                                         |
| [**RollbackDisabled**](rollbackdisabled.md)<br/>                       | Il programma di installazione imposta questa proprietà quando il rollback è disabilitato.<br/>                                                                                                                                                                                                   |
| [**UILevel**](uilevel.md)<br/>                                         | Indica il livello dell'interfaccia utente.<br/>                                                                                                                                                                                                                           |
| [**UpdateStarted**](updatestarted.md)<br/>                             | Impostare quando le modifiche apportate al sistema sono state avviate per questa installazione.<br/>                                                                                                                                                                                              |
| [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)<br/>               | Impostato dal programma di installazione quando un aggiornamento rimuove un'applicazione.<br/>                                                                                                                                                                                                  |
| [**VersionMsi**](versionmsi.md)<br/>                                   | Il programma di installazione imposta questa proprietà sulla versione di Windows Installer eseguita durante l'installazione.<br/>                                                                                                                                                     |



 

## <a name="operating-system-properties"></a>Proprietà del sistema operativo

Nell'elenco seguente vengono forniti i collegamenti a ulteriori informazioni sulle proprietà del sistema operativo impostate dal programma di installazione all'avvio.



| Nome della proprietà                                                                             | Breve descrizione                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdminUser**](adminuser.md)<br/>                                                 | Impostare su Windows 2000 se l'utente dispone di privilegi di amministratore.<br/>                                                                                                                                                                                                                        |
| [**ComputerName**](computername.md)<br/>                                           | Nome del computer del sistema corrente.<br/>                                                                                                                                                                                                                                                 |
| [**MsiNetAssemblySupport**](msinetassemblysupport.md)<br/>                         | Nei sistemi che supportano Common Language Runtime assembly, il programma di installazione imposta il valore di questa proprietà sulla versione del file di fusion.dll. Il programma di installazione non imposta questa proprietà se il sistema operativo non supporta assembly Common Language Runtime.<br/>                   |
| [**MsiNTProductType**](msintproducttype.md)<br/>                                   | Indica il tipo di prodotto Windows.<br/>                                                                                                                                                                                                                                                  |
| [**MsiNTSuiteBackOffice**](msintsuitebackoffice.md)<br/>                           | In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta questa proprietà su 1 (uno) solo se sono installati i componenti di Microsoft BackOffice.<br/>                                                                                                                                      |
| [**MsiNTSuiteDataCenter**](msintsuitedatacenter.md)<br/>                           | In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta questa proprietà su 1 (uno) solo se è installato Windows 2000 Datacenter Server.<br/>                                                                                                                                        |
| [**MsiNTSuiteEnterprise**](msintsuiteenterprise.md)<br/>                           | In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta questa proprietà su 1 (uno) solo se è installato Windows 2000 Advanced Server.<br/>                                                                                                                                          |
| [**MsiNTSuitePersonal**](msintsuitepersonal.md)<br/>                               | In Windows XP e nei sistemi operativi successivi il programma di installazione imposta questa proprietà su 1 (uno) solo se il sistema operativo è Home (non professionale).<br/>                                                                                                                                      |
| [**MsiNTSuiteSmallBusiness**](msintsuitesmallbusiness.md)<br/>                     | In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta questa proprietà su 1 (uno) solo se è installato Microsoft Small Business Server.<br/>                                                                                                                                       |
| [**MsiNTSuiteSmallBusinessRestricted**](msintsuitesmallbusinessrestricted.md)<br/> | In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta questa proprietà su 1 (uno) solo se Microsoft Small Business Server è installato con la licenza client restrittiva.<br/>                                                                                                   |
| [**MsiNTSuiteWebServer**](msintsuitewebserver.md)<br/>                             | In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà [**MsiNTSuiteWebServer**](msintsuitewebserver.md) su 1 (uno) se è installata l'edizione Web di windows Server 2003. Disponibile solo con la versione di Windows Server 2003 della Windows Installer.<br/> |
| [**MsiTabletPC**](msitabletpc.md)<br/>                                             | Il programma di installazione imposta questa proprietà su un valore diverso da zero se il sistema operativo corrente è Windows XP Tablet PC Edition.<br/>                                                                                                                                                                 |
| [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md)<br/>                     | Nei sistemi che supportano gli assembly Win32, il programma di installazione imposta il valore di questa proprietà sulla versione del file di sxs.dll. Il programma di installazione non imposta questa proprietà se il sistema operativo non supporta gli assembly Win32.<br/>                                                          |
| [**OLEAdvtSupport**](oleadvtsupport.md)<br/>                                       | Impostare se OLE supporta il Windows Installer.<br/>                                                                                                                                                                                                                                           |
| [**RedirectedDllSupport**](redirecteddllsupport.md)<br/>                           | Il programma di installazione imposta la proprietà [**RedirectedDllSupport**](redirecteddllsupport.md) se il sistema che esegue l'installazione supporta [componenti isolati](isolated-components.md).<br/>                                                                                              |
| [**RemoteAdminTS**](remoteadmints.md)<br/>                                         | Il programma di installazione imposta la proprietà [**RemoteAdminTS**](remoteadmints.md) quando il sistema è un server di amministrazione remoto che esegue il servizio ruolo Terminal Server.<br/>                                                                                                                   |
| [**ServicePackLevel**](servicepacklevel.md)<br/>                                   | Numero di versione del sistema operativo Service Pack.<br/>                                                                                                                                                                                                                             |
| [**ServicePackLevelMinor**](servicepacklevelminor.md)<br/>                         | Numero di versione secondario del Service Pack del sistema operativo.<br/>                                                                                                                                                                                                                       |
| [**SharedWindows**](sharedwindows.md)<br/>                                         | Impostato quando il sistema funziona come finestre condivise.<br/>                                                                                                                                                                                                                                  |
| [**ShellAdvtSupport**](shelladvtsupport.md)<br/>                                   | Impostare se la Shell supporta la funzionalità pubblicitaria.<br/>                                                                                                                                                                                                                                       |
| [**SystemLanguageID**](systemlanguageid.md)<br/>                                   | Identificatore della lingua predefinita per il sistema.<br/>                                                                                                                                                                                                                                          |
| [**TerminalServer**](terminalserver.md)<br/>                                       | Impostare quando il sistema è un server che esegue il servizio ruolo Terminal Server.<br/>                                                                                                                                                                                                            |
| [**TTCSupport**](ttcsupport.md)<br/>                                               | Indica se il sistema operativo supporta l'utilizzo di file con estensione TTC (True Type Font Collections).<br/>                                                                                                                                                                                            |
| [**Version9X**](version9x.md)<br/>                                                 | Numero di versione del sistema operativo Windows.<br/>                                                                                                                                                                                                                                     |
| [**VersionDatabase**](versiondatabase.md)<br/>                                     | Versione del database numerico dell'installazione corrente.<br/>                                                                                                                                                                                                                                |
| [**VersionNT**](versionnt.md)<br/>                                                 | Numero di versione del sistema operativo.<br/>                                                                                                                                                                                                                                             |
| [**VersionNT64**](versionnt64.md)<br/>                                             | Numero di versione del sistema operativo se il sistema è in esecuzione in un computer a 64 bit.<br/>                                                                                                                                                                                               |
| [**Compilazione di Windows**](windowsbuild.md)<br/>                                          | Numero di build del sistema operativo.<br/>                                                                                                                                                                                                                                                |



 

## <a name="product-information-properties"></a>Proprietà informazioni sul prodotto

Nell'elenco seguente vengono forniti i collegamenti a ulteriori informazioni sulle proprietà specifiche del prodotto specificate nella [tabella delle proprietà](property-table.md).



| Nome della proprietà                                                  | Breve descrizione                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)<br/>                  | Indirizzo Internet o URL per il supporto tecnico.<br/>                                                                                 |
| [**ARPHELPTELEPHONE**](arphelptelephone.md)<br/>        | Numeri di telefono del supporto tecnico.<br/>                                                                                               |
| [**DiskPrompt**](diskprompt.md)<br/>                    | Stringa visualizzata da una finestra di messaggio che richiede un disco.<br/>                                                                     |
| [**IsAdminPackage**](isadminpackage.md)<br/>            | Impostare su 1 (uno) se l'installazione corrente viene eseguita da un pacchetto creato tramite un'installazione amministrativa.<br/>           |
| [**LeftUnit**](leftunit.md)<br/>                        | Inserisce le unità a sinistra del numero.<br/>                                                                                        |
| [**Produttore**](manufacturer.md)<br/>                | Nome del produttore dell'applicazione. (Obbligatorio)<br/>                                                                               |
| [**MediaSourceDir**](mediasourcedir.md)<br/>            | Il programma di installazione imposta questa proprietà su 1 (uno) quando l'installazione usa un'origine multimediale, ad esempio un CD-ROM.<br/>                       |
| [**MSIINSTANCEGUID**](msiinstanceguid.md)<br/>          | La presenza di questa proprietà indica che una trasformazione modifica codice prodotto è registrata nel prodotto.<br/>                   |
| [**MSINEWINSTANCE**](msinewinstance.md)<br/>            | Questa proprietà indica l'installazione di una nuova istanza di un prodotto con le trasformazioni dell'istanza.<br/>                              |
| [**ParentProductCode**](parentoriginaldatabase.md)<br/> | Il programma di installazione imposta questa proprietà per le installazioni eseguite da un'azione di [installazione simultanea](concurrent-installations.md) .<br/> |
| [**PIDTemplate**](pidtemplate.md)<br/>                  | Stringa utilizzata come modello per la proprietà [**codice PIDKEY**](pidkey.md) .<br/>                                                           |
| [**ProductCode**](productcode.md)<br/>                  | Identificatore univoco per una versione del prodotto specifica. (Obbligatorio)<br/>                                                                 |
| [**ProductName**](productname.md)<br/>                  | Nome leggibile di un'applicazione. (Obbligatorio)<br/>                                                                              |
| [**ProductState**](productstate.md)<br/>                | Impostare sullo stato di installazione di un prodotto.<br/>                                                                                       |
| [**ProductVersion**](productversion.md)<br/>            | Formato stringa della versione del prodotto come valore numerico. (Obbligatorio)<br/>                                                            |
| [**UpgradeCode**](upgradecode.md)<br/>                  | GUID che rappresenta un set correlato di prodotti.<br/>                                                                              |



 

## <a name="summary-information-update-properties"></a>Proprietà aggiornamento informazioni di riepilogo

Le proprietà seguenti vengono impostate solo da trasformazioni nei file con estensione msp utilizzati per aggiornare il flusso di informazioni di riepilogo di un'immagine amministrativa.



| Proprietà                                                              | Descrizione                                                                                                                  |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md)<br/>         | Il valore di questa proprietà viene scritto nella proprietà di [**Riepilogo dei numeri di revisione**](revision-number-summary.md) .<br/> |
| [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)<br/> | Il valore di questa proprietà viene scritto nella proprietà di [**Riepilogo dei commenti**](comments-summary.md) .<br/>               |
| [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)<br/>   | Il valore di questa proprietà viene scritto nella proprietà di [**Riepilogo dell'oggetto**](subject-summary.md) .<br/>                 |



 

## <a name="system-folder-properties"></a>Proprietà cartella di sistema

Nell'elenco seguente vengono forniti i collegamenti ad altre informazioni sulle cartelle di sistema impostate dal programma di installazione al momento dell'installazione.



| Proprietà                                                        | Descrizione                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**AdminToolsFolder**](admintoolsfolder.md)<br/>         | Percorso completo della directory che contiene gli strumenti di amministrazione.<br/>         |
| [**CartellaDatiApp**](appdatafolder.md)<br/>               | Percorso completo della cartella **roaming** per l'utente corrente.<br/>              |
| [**CommonAppDataFolder**](commonappdatafolder.md)<br/>   | Percorso completo dei dati dell'applicazione per tutti gli utenti.<br/>                           |
| [**CommonFiles64Folder**](commonfiles64folder.md)<br/>   | Percorso completo della cartella di **file comuni a 64 bit** predefinita.<br/>            |
| [**CommonFilesFolder**](commonfilesfolder.md)<br/>       | Percorso completo della cartella dei **file comuni** per l'utente corrente.<br/>         |
| [**Includevano**](desktopfolder.md)<br/>               | Percorso completo della cartella **Desktop** .<br/>                                   |
| [**FavoritesFolder**](favoritesfolder.md)<br/>           | Percorso completo della cartella **Preferiti** per l'utente corrente.<br/>            |
| [**FontsFolder**](fontsfolder.md)<br/>                   | Percorso completo della cartella dei **tipi di carattere** .<br/>                                     |
| [**LocalAppDataFolder**](localappdatafolder.md)<br/>     | Percorso completo della cartella che contiene le applicazioni locali (non in roaming).<br/> |
| [**MyPicturesFolder**](mypicturesfolder.md)<br/>         | Percorso completo della cartella **Immagini** .<br/>                                  |
| [**NetHoodFolder**](nethoodfolder.md)<br/>               | Percorso completo della cartella **NetHood** .<br/>                                   |
| [**PersonalFolder**](personalfolder.md)<br/>             | Percorso completo della cartella **documenti** per l'utente corrente.<br/>            |
| [**PrintHoodFolder**](printhoodfolder.md)<br/>           | Percorso completo della cartella **PrintHood** .<br/>                                 |
| [**ProgramFiles64Folder**](programfiles64folder.md)<br/> | Percorso completo della cartella dei file di **programma a 64 bit** predefinita.<br/>           |
| [**ProgramFilesFolder**](programfilesfolder.md)<br/>     | Percorso completo della cartella dei file di **programma a 32 bit** predefinita.<br/>           |
| [**ProgramMenuFolder**](programmenufolder.md)<br/>       | Percorso completo della cartella del **menu del programma** .<br/>                              |
| [**RecentFolder**](recentfolder.md)<br/>                 | Percorso completo della cartella **recente** .<br/>                                    |
| [**SendToFolder**](sendtofolder.md)<br/>                 | Percorso completo della cartella **SendTo** per l'utente corrente.<br/>               |
| [**Dei**](startmenufolder.md)<br/>           | Percorso completo della cartella del **menu Start** .<br/>                                |
| [**StartupFolder**](startupfolder.md)<br/>               | Percorso completo della cartella di **avvio** .<br/>                                   |
| [**System16Folder**](system16folder.md)<br/>             | Percorso completo della cartella per le DLL di sistema a 16 bit.<br/>                            |
| [**System64Folder**](system64folder.md)<br/>             | Percorso completo della cartella **system64** predefinita.<br/>                       |
| [**SystemFolder**](systemfolder.md)<br/>                 | Percorso completo della cartella di **sistema** per l'utente corrente.<br/>               |
| [**TempFolder**](tempfolder.md)<br/>                     | Percorso completo della cartella **temporanea** .<br/>                                      |
| [**Cartellamodelli**](templatefolder.md)<br/>             | Percorso completo della cartella del **modello** per l'utente corrente.<br/>             |
| [**WindowsFolder**](windowsfolder.md)<br/>               | Percorso completo della cartella di **Windows** .<br/>                                   |
| [**WindowsVolume**](windowsvolume.md)<br/>               | Volume della cartella di **Windows** .<br/>                                      |



 

## <a name="user-information-properties"></a>Proprietà informazioni utente

Nell'elenco seguente vengono forniti i collegamenti a ulteriori informazioni sulle informazioni fornite dall'utente.



| Proprietà                                                      | Descrizione                                                                             |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AdminProperties**](adminproperties.md)<br/>         | Elenco di proprietà impostate durante un'installazione di amministrazione.<br/>       |
| [**COMPANYNAME**](companyname.md)<br/>                 | Nome dell'organizzazione dell'utente che sta eseguendo l'installazione.<br/>            |
| [**LogonUser**](logonuser.md)<br/>                     | Nome utente per l'utente attualmente connesso.<br/>                           |
| [**MsiHiddenProperties**](msihiddenproperties.md)<br/> | Elenco delle proprietà che non possono essere scritte nel log.<br/>       |
| [**CODICE PIDKEY**](pidkey.md)<br/>                           | Parte dell'ID prodotto immesso dall'utente.<br/>                                 |
| [**ProductID**](productid.md)<br/>                     | ID prodotto completo dopo una convalida corretta.<br/>                               |
| [**UserLanguageID**](userlanguageid.md)<br/>           | Identificatore della lingua predefinita dell'utente corrente.<br/>                             |
| [**NOME utente**](username.md)<br/>                       | Utente che sta eseguendo l'installazione.<br/>                                     |
| [**Proprietà UserSID**](usersid.md)<br/>                | Impostato dal programma di installazione in base all'ID di sicurezza (SID) dell'utente.<br/> |



 

 

 
