---
description: Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer&\# 160; 3.1 e versioni precedenti.
ms.assetid: fbf75dbe-3fa1-424b-83bb-cfd0b179107c
title: Non supportato in Windows Installer 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a221d80f56c5737cc5ae92a040a005ae42449e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318654"
---
# <a name="not-supported-in-windows-installer-31"></a>Non supportato in Windows Installer 3,1

Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer 3,1 e versioni precedenti. L'assenza di una funzionalità da questo elenco non garantisce che la funzionalità sia supportata. Vedere la documentazione principale per determinare quale versione di Windows Installer è necessaria per una determinata funzionalità. Per informazioni sulle altre versioni di Windows Installer, vedere Novità [di Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 3,1 è disponibile per Windows Server 2003, Windows XP o Windows 2000. Per un elenco di tutte le versioni Windows Installer e i ridistribuibili, vedere [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).

Le funzionalità seguenti non sono supportate in Windows Installer 3,1 e versioni precedenti.

[Funzioni di installazione](installer-functions.md)

-   [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)

[Proprietà](properties.md)

-   [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)
-   [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md)
-   [**MSIDISABLERMRESTART**](msidisablermrestart.md)
-   [**MsiLogFileLocation**](msilogfilelocation.md)
-   [**MsiLogging**](msilogging.md)
-   [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
-   [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)
-   [**MSIRMSHUTDOWN**](msirmshutdown.md)
-   [**MsiRunningElevated**](msirunningelevated-.md)
-   [**MsiSystemRebootPending**](msisystemrebootpending.md)
-   [**MsiTabletPC**](msitabletpc.md)
-   [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)

[Proprietà informazioni di riepilogo](summary-information-stream-reference.md)

-   La [**proprietà di riepilogo di Word Count**](word-count-summary.md) include nuovi bit di flag per specificare se l'installazione del pacchetto richiede privilegi elevati.

[Criteri di sistema](system-policy.md)

-   [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
-   [DisableLoggingFromPackage](disableloggingfrompackage.md)

[Tabelle di database](database-tables.md)

-   [Tabella di collegamento](shortcut-table.md)

    Nuove colonne: DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL e DescriptionResourceId

[Finestre di dialogo](dialog-boxes.md)

-   [Finestra di dialogo MsiRMFilesInUse](msirmfilesinuse-dialog.md)

[Attributi del controllo](control-attributes.md)

-   [ElevationShield](elevationshield-attribute.md)

[ControlEvents](control-events.md)

-   [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)

[Tipi di messaggi dell'interfaccia utente esterni](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)

-   \_RMFILESINUSE INSTALLLOGMODE

[Windows Installer su sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md)

-   attributo **msidbComponentAttributesDisableRegistryReflection** nella [tabella Component](component-table.md)

[Interfaccia di automazione](automation-interface.md)

-   Metodi dell' [ **oggetto Installer**](installer-object.md)

    -   [**Programma di installazione. AdvertiseProduct**](installer-advertiseproduct.md)
    -   [**Programma di installazione. AdvertiseScript**](installer-advertisescript.md)
    -   [**Programma di installazione. CreateAdvertiseScript**](installer-createadvertisescript.md)
    -   [**Programma di installazione. ProvideAssembly**](installer-provideassembly.md)

-   Proprietà dell' [ **oggetto Installer**](installer-object.md)

    -   [**Programma di installazione. PatchFiles**](installer-patchfiles.md)
    -   [**Programma di installazione. ProductElevated**](installer-productelevated.md)
    -   [**Programma di installazione. ProductInfoFromScript**](installer-productinfofromscript.md)

## <a name="notes"></a>Note

Il servizio di Windows Installer deve essere eseguito in Windows Vista per consentire l'uso di [Gestione riavvio](../rstmgr/restart-manager-portal.md), [*controllo dell'account utente*](u-gly.md)e applicazione di [patch di controllo dell'account utente (UAC)](user-account-control--uac--patching.md). Per informazioni, vedere [uso di Windows Installer con Gestione riavvio](using-windows-installer-with-restart-manager.md) e [uso di Windows Installer con l'applicazione di patch a UAC](using-windows-installer-with-uac.md) e [controllo dell'account utente (UAC)](user-account-control--uac--patching.md).

Windows Installer 3,1 supporta la protezione file di Windows (WFP) e non supporta Protezione risorse di Windows (WRP). WRP in Windows Server 2008 e Windows Vista sostituisce WFP in Windows Server 2003, Windows XP e Windows 2000. Per informazioni su Windows Installer e WFP, vedere [uso di Windows Installer e protezione risorse di Windows](windows-resource-protection-on-windows-vista.md).

 

 
