---
description: Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer&\# 160, 4.5 e versioni precedenti.
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: Non supportato in Windows Installer 4,5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d1d1b3039c4e51c7233f98ee2e41afb308a822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754218"
---
# <a name="not-supported-in-windows-installer-45"></a>Non supportato in Windows Installer 4,5

Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer 4,5 e versioni precedenti. L'assenza di una funzionalità da questo elenco non garantisce che la funzionalità sia supportata. Vedere la documentazione principale per determinare quale versione di Windows Installer è necessaria per una determinata funzionalità. Per informazioni sulle altre versioni di Windows Installer, vedere Novità [di Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 4,5 è disponibile come ridistribuibile per Windows Server 2008, Windows Vista con Service Pack 1 (SP1), Windows XP con Service Pack 2 (SP2) e versioni successive e Windows Server 2003 con Service Pack 1 (SP1) e versioni successive. Per un elenco completo di tutte le versioni di Windows Installer e dei ridistribuibili, vedere [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).

Le funzionalità seguenti non sono supportate in Windows Installer 4,5 e versioni precedenti.

[Azioni standard](standard-actions.md)

-   [MsiConfigureServices](msiconfigureservices-action.md)

[Funzioni di installazione](installer-functions.md)

-   [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
-   [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
-   [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

[Tipi di dati delle colonne](column-data-types.md)

-   [**FormattedSDDLText**](formattedsddltext.md)

[Proprietà](properties.md)

-   [**MSIFASTINSTALL**](msifastinstall.md)
-   [**MSIINSTALLPERUSER**](msiinstallperuser.md)

[Tabelle di database](database-tables.md)

-   [Tabella MsiServiceConfig](msiserviceconfig-table.md)
-   [Tabella MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md)
-   [Tabella MsiShortcutProperty](msishortcutproperty-table.md)
-   [Tabella MsiLockPermissionsEx](msilockpermissionsex-table.md)

[ControlEvents](control-events.md)

-   [ControlEvent MsiPrint](msiprint-controlevent.md)
-   [ControlEvent MsiLaunchApp](msilaunchapp-controlevent.md)

[Controlli](controls.md)

-   [Controllo collegamento ipertestuale](hyperlink-control.md)
-   Supporto del [controllo bitmap](bitmap-control.md) dei formati di file di immagine WIC

[Analizzatori di coerenza interni-CIEM](internal-consistency-evaluators-ices.md)

-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interfaccia di automazione](automation-interface.md)

-   Proprietà dell' [ **oggetto del programma di installazione**](installer-object.md)

    -   [**Programma di installazione. ClientsEx**](installer-clientsex.md)
    -   [**Programma di installazione. ComponentsEx**](installer-componentsex.md)
    -   [**Programma di installazione. ComponentPathEx**](installer-componentpathex.md)

-   Proprietà dell' [ **oggetto Component**](components.md)

    -   [**Componente. ComponentCode**](component-componentcode.md)
    -   [**Componente. UserSID**](component-usersid.md)
    -   [**Component. Context**](component-context.md)

-   Proprietà dell' [ **oggetto client**](client.md)

    -   [**Client. ProductCode**](client-productcode.md)
    -   [**Client. ComponentCode**](client-componentcode.md)
    -   [**Client. UserSID**](client-usersid.md)
    -   [**Client. Context**](client-context.md)

-   Proprietà dell'oggetto [**ComponentInfo**](componentinfo.md)

    -   [**ComponentInfo. ComponentCode**](componentinfo-componentcode.md)
    -   [**ComponentInfo. Path**](componentinfo-path.md)
    -   [**ComponentInfo. state**](componentinfo-state.md)

## <a name="notes"></a>Note

Windows Installer 4,5 non supporta alcune funzionalità che consentono di installare un singolo pacchetto di installazione nel contesto di installazione per computer o per utente. Per ulteriori informazioni, vedere [creazione di singoli pacchetti](single-package-authoring.md).

Windows Installer 4,5 non supporta alcune opzioni di configurazione dei servizi che consentono a un pacchetto di personalizzare i [Servizi](../services/services.md) in un computer. Per ulteriori informazioni, vedere [utilizzo della configurazione dei servizi](using-services-configuration.md).

Windows Installer 4,5 non supporta alcune funzionalità che consentono al Windows Installer di proteggere nuovi account, [Servizi](../services/services.md)Windows, file, cartelle e chiavi del registro di sistema. Per informazioni, vedere [protezione delle risorse](securing-resources-.md).

Windows Installer 4,5 non supporta alcune funzionalità che consentono all'installazione di enumerare tutti i componenti installati nel computer e di ottenere il percorso della chiave per il componente. Per ulteriori informazioni, vedere [enumerazione dei componenti](enumerating-components-.md).

 

 
