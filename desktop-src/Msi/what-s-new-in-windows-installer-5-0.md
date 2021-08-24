---
description: Le informazioni contenute in questo argomento identificano le aggiunte e le modifiche disponibili in Windows Installer&\# 160;5.0.
ms.assetid: c088c15b-0eef-4a92-bb65-e7fe871afbfe
title: Novità del programma di installazione Windows 5.0
ms.topic: article
ms.date: 11/08/2019
ms.openlocfilehash: 82c6ae3bf5c6781ba84d18b366998c74deedd4ca0fa4c61ac452b1d0ec409850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145224"
---
# <a name="whats-new-in-windows-installer-50"></a>Novità del programma di installazione Windows 5.0

Le informazioni contenute in questo argomento identificano le aggiunte e le modifiche disponibili in Windows Installer 5.0.

Windows Installer 5.0 è incluso nelle versioni seguenti di Windows:

* Client: Windows 7 e tutte le versioni successive.
* Server: Windows Server 2008 R2 e tutte le versioni successive.

> [!NOTE]
> Non è possibile ridistribuire Windows Installer 5.0. Per un elenco dei componenti ridistribuibili disponibili per le versioni precedenti di Windows Installer, vedere Windows [Installer Redistributables](windows-installer-redistributables.md). Per un elenco completo delle Windows del programma di installazione, vedere [Versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).

Questa pagina viene fornita come guida alla documentazione. Per determinare i requisiti effettivi del sistema operativo, vedere la sezione Requisiti nelle pagine di riferimento principali. Le parti del Windows non collegate a questa pagina potrebbero essere disponibili in un'altra versione del Windows installer. Per informazioni su altre Windows del programma di installazione, vedere Novità [di Windows Installer](what-s-new-in-windows-installer.md).

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

[Proprietà delle informazioni di riepilogo](summary-information-stream-reference.md)

-   Il [**riepilogo dei**](template-summary.md) modelli include nuovi valori per indicare che il database è compatibile con Windows RT o con la piattaforma Arm64.

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

[Analizzatori di coerenza interna - ICE](internal-consistency-evaluators-ices.md)

-   [ICE101](ice-101.md)
-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interfaccia di automazione](automation-interface.md)

-   Proprietà [ **dell'oggetto Installer**](installer-object.md)

    -   [**Installer.ClientsEx**](installer-clientsex.md)
    -   [**Installer.ComponentsEx**](installer-componentsex.md)
    -   [**Installer.ComponentPathEx**](installer-componentpathex.md)

-   Proprietà [ **dell'oggetto Components**](components.md)

    -   [**Components.ComponentCode**](component-componentcode.md)
    -   [**Components.UserSID**](component-usersid.md)
    -   [**Components.Context**](component-context.md)

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

Gli sviluppatori del programma di installazione possono usare Windows Installer 5.0 per creare un singolo pacchetto di installazione in grado di eseguire l'installazione per computer o per utente dell'applicazione. Per altre informazioni, vedere [Creazione di pacchetti singoli](single-package-authoring.md). L'analizzatore di coerenza [interno ICE105](ice-105.md) verifica che il pacchetto sia stato creato per essere installato in un contesto per utente. Un'applicazione in grado di essere installata, aggiornata, eseguita e rimossa da un utente standard senza elevazione dei privilegi è denominata applicazione Per-User (PUA). Un puA può offrire un'esperienza utente migliore, ridurre al minimo gli effetti sul sistema e su altri utenti del computer e riserva il controllo dell'account utente che richiede a situazioni che richiedono effettivamente l'elevazione dei privilegi dell'utente. Le funzionalità di creazione di pacchetti singoli di Windows Installer 5.0 possono facilitare lo sviluppo di Per-User applicazioni.

Le opzioni di configurazione dei servizi Windows un pacchetto del programma di installazione per personalizzare [i servizi](../services/services.md) in un computer. Per altre informazioni, vedere [Uso della configurazione dei servizi](using-services-configuration.md).

A partire da Windows Installer 5.0, un pacchetto del programma di installazione di Windows è in grado di proteggere nuovi account, servizi [Windows,](../services/services.md)file, cartelle e chiavi del Registro di sistema. La [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md) può specificare un descrittore di sicurezza che nega le autorizzazioni, specifica l'ereditarietà delle autorizzazioni da una risorsa padre o specifica le autorizzazioni di un nuovo account. Per informazioni, vedere [Protezione delle risorse](securing-resources-.md).

Windows Il programma di installazione 5.0 può enumerare tutti i componenti installati nel computer e ottenere il percorso della chiave per il componente. Per altre informazioni, vedere [Enumerazione dei componenti](enumerating-components-.md).

Windows Il programma di installazione 5.0 in Windows Server 2012 o Windows 8 supporta l'installazione di app approvate Windows RT. Un Windows, una patch o una trasformazione del programma di installazione non firmata da Microsoft non può essere installata Windows RT. La [**proprietà Riepilogo**](template-summary.md) modello indica la piattaforma compatibile con il database di installazione e deve includere il valore per Windows RT.

Windows Il programma di installazione 5.0 in Windows 10 nei processori Arm64 supporta l'installazione di applicazioni compilate in modo specifico per la piattaforma Arm64.  La [**proprietà Riepilogo**](template-summary.md) modello di questi pacchetti deve includere il valore Arm64. 

 
