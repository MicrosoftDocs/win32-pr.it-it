---
description: Le Windows, le tabelle e le proprietà elencate in questa pagina non sono supportate dal programma di installazione di Windows&\# 160;4.5 e versioni precedenti.
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: Non supportato in Windows Installer 4.5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a285094610f0a00a39a26bb2d0683cb41afdfa3ed126ac27f7655c3cd56df17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979351"
---
# <a name="not-supported-in-windows-installer-45"></a>Non supportato in Windows Installer 4.5

Le Windows, le tabelle e le proprietà elencate in questa pagina non sono supportate da Windows Installer 4.5 e versioni precedenti. L'assenza di una funzionalità da questo elenco non garantisce che la funzionalità sia supportata. Vedere la documentazione principale per determinare quale Windows del programma di installazione è necessaria per una particolare funzionalità. Per informazioni su altre Windows del programma di installazione, vedere Novità [di Windows Installer](what-s-new-in-windows-installer.md).

Windows Il programma di installazione 4.5 è disponibile come ridistribuibile per Windows Server 2008, Windows Vista con Service Pack 1 (SP1), Windows XP con Service Pack 2 (SP2) e versioni successive e Windows Server 2003 con Service Pack 1 (SP1) e versioni successive. Per un elenco completo di tutte le Windows e ridistribuibili del programma di installazione, vedere Versioni rilasciate di [Windows Installer](released-versions-of-windows-installer.md).

Le funzionalità seguenti non sono supportate in Windows Installer 4.5 e versioni precedenti.

[Azioni standard](standard-actions.md)

-   [MsiConfigureServices](msiconfigureservices-action.md)

[Funzioni del programma di installazione](installer-functions.md)

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

[Eventi di controllo](control-events.md)

-   [MsiPrint ControlEvent](msiprint-controlevent.md)
-   [MsiLaunchApp ControlEvent](msilaunchapp-controlevent.md)

[Controlli](controls.md)

-   [Controllo Collegamento ipertestuale](hyperlink-control.md)
-   [Supporto del controllo](bitmap-control.md) bitmap dei formati di file di immagine WIC

[Analizzatori di coerenza interna - ICE](internal-consistency-evaluators-ices.md)

-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interfaccia di automazione](automation-interface.md)

-   Proprietà [ **dell'oggetto Installer**](installer-object.md)

    -   [**Installer.ClientsEx**](installer-clientsex.md)
    -   [**Installer.ComponentsEx**](installer-componentsex.md)
    -   [**Installer.ComponentPathEx**](installer-componentpathex.md)

-   Proprietà [ **dell'oggetto Component**](components.md)

    -   [**Component.ComponentCode**](component-componentcode.md)
    -   [**Component.UserSID**](component-usersid.md)
    -   [**Component.Context**](component-context.md)

-   Proprietà [ **dell'oggetto client**](client.md)

    -   [**Client.ProductCode**](client-productcode.md)
    -   [**Client.ComponentCode**](client-componentcode.md)
    -   [**Client.UserSID**](client-usersid.md)
    -   [**Client.Context**](client-context.md)

-   Proprietà [**dell'oggetto ComponentInfo**](componentinfo.md)

    -   [**ComponentInfo.ComponentCode**](componentinfo-componentcode.md)
    -   [**ComponentInfo.Path**](componentinfo-path.md)
    -   [**ComponentInfo.State**](componentinfo-state.md)

## <a name="notes"></a>Note

Windows Il programma di installazione 4.5 non supporta alcune funzionalità che consentono l'installazione di un singolo pacchetto di installazione nel contesto di installazione per computer o per utente. Per altre informazioni, vedere [Creazione di pacchetti singoli](single-package-authoring.md).

Windows Il programma di installazione 4.5 non supporta alcune opzioni di configurazione dei servizi che consentono a un pacchetto di personalizzare i [servizi](../services/services.md) in un computer. Per altre informazioni, vedere [Uso della configurazione dei servizi](using-services-configuration.md).

Windows Il programma di installazione 4.5 non supporta alcune funzionalità che consentono al programma di installazione di Windows di proteggere nuovi account, servizi [Windows,](../services/services.md)file, cartelle e chiavi del Registro di sistema. Per informazioni, vedere [Protezione delle risorse](securing-resources-.md).

Windows Il programma di installazione 4.5 non supporta alcune funzionalità che consentono all'installazione di enumerare tutti i componenti installati nel computer e ottenere il percorso della chiave per il componente. Per altre informazioni, vedere [Enumerazione dei componenti](enumerating-components-.md).

 

 
