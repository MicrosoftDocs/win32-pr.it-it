---
description: Le informazioni contenute in questo argomento identificano le aggiunte e le modifiche disponibili in Windows Installer&\# 160; 5.0.
ms.assetid: c088c15b-0eef-4a92-bb65-e7fe871afbfe
title: Novità di Windows Installer 5,0
ms.topic: article
ms.date: 11/08/2019
ms.openlocfilehash: ae7986cec60341127ab00ad08a3032aad80209bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878534"
---
# <a name="whats-new-in-windows-installer-50"></a>Novità di Windows Installer 5,0

Le informazioni contenute in questo argomento identificano le aggiunte e le modifiche disponibili in Windows Installer 5,0.

Windows Installer 5,0 è incluso nelle seguenti versioni di Windows:

* Client: Windows 7 e tutte le versioni successive.
* Server: Windows Server 2008 R2 e tutte le versioni successive.

> [!NOTE]
> Non è disponibile alcun componente ridistribuibile per Windows Installer 5,0. Per un elenco dei ridistribuibili disponibili per le versioni precedenti di Windows Installer, vedere [Windows Installer ridistribuibili](windows-installer-redistributables.md). Per un elenco completo delle versioni di Windows Installer, vedere [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).

Questa pagina viene fornita come guida alla documentazione. Per determinare i requisiti effettivi del sistema operativo, fare riferimento alla sezione requisiti nelle pagine principali di riferimento. Parti del Windows Installer che non sono collegate da questa pagina possono essere disponibili in un'altra versione del Windows Installer. Per informazioni su altre versioni di Windows Installer, vedere Novità [di Windows Installer](what-s-new-in-windows-installer.md).

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

[Proprietà informazioni di riepilogo](summary-information-stream-reference.md)

-   Il [**Riepilogo del modello**](template-summary.md) presenta nuovi valori per indicare che il database è compatibile con Windows RT o con la piattaforma Arm64.

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

[Analizzatori di coerenza interni-CIEM](internal-consistency-evaluators-ices.md)

-   [ICE101](ice-101.md)
-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interfaccia di automazione](automation-interface.md)

-   Proprietà dell' [ **oggetto del programma di installazione**](installer-object.md)

    -   [**Programma di installazione. ClientsEx**](installer-clientsex.md)
    -   [**Programma di installazione. ComponentsEx**](installer-componentsex.md)
    -   [**Programma di installazione. ComponentPathEx**](installer-componentpathex.md)

-   Proprietà dell' [ **oggetto Components**](components.md)

    -   [**Components. ComponentCode**](component-componentcode.md)
    -   [**Components. UserSID**](component-usersid.md)
    -   [**Components. Context**](component-context.md)

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

Gli sviluppatori del programma di installazione possono utilizzare Windows Installer 5,0 per creare un singolo pacchetto di installazione in grado di installare l'applicazione per computer o per utente. Per ulteriori informazioni, vedere [creazione di singoli pacchetti](single-package-authoring.md). L'analizzatore di coerenza interno [ICE105](ice-105.md) verifica che il pacchetto sia stato creato per essere installato in un contesto per utente. Un'applicazione in grado di essere installata, aggiornata, eseguita e rimossa da un utente standard senza elevazione dei privilegi è detta applicazione Per-User (PUA). Un PUA può offrire un'esperienza utente migliore, ridurre al minimo gli effetti sul sistema e altri utenti del computer e riserva la richiesta di controllo dell'account utente a situazioni che richiedono effettivamente l'elevazione dei privilegi dell'utente. Le funzionalità di creazione di singoli pacchetti di Windows Installer 5,0 consentono di semplificare lo sviluppo di applicazioni Per-User.

Le opzioni di configurazione dei servizi consentono a un pacchetto di Windows Installer di personalizzare i [Servizi](../services/services.md) in un computer. Per ulteriori informazioni, vedere [utilizzo della configurazione dei servizi](using-services-configuration.md).

A partire da Windows Installer 5,0, un pacchetto di Windows Installer è in grado di proteggere nuovi account, [Servizi](../services/services.md)Windows, file, cartelle e chiavi del registro di sistema. La tabella [MsiLockPermissionsEx](msilockpermissionsex-table.md) può specificare un descrittore di sicurezza che nega le autorizzazioni, specifica l'ereditarietà delle autorizzazioni da una risorsa padre o specifica le autorizzazioni di un nuovo account. Per informazioni, vedere [protezione delle risorse](securing-resources-.md).

Windows Installer 5,0 è in grado di enumerare tutti i componenti installati nel computer e di ottenere il percorso della chiave per il componente. Per ulteriori informazioni, vedere [enumerazione dei componenti](enumerating-components-.md).

Windows Installer 5,0 in esecuzione in Windows Server 2012 o Windows 8 supporta l'installazione di app approvate in Windows RT. Non è possibile installare un pacchetto di Windows Installer, una patch o una trasformazione che non è stata firmata da Microsoft in Windows RT. La proprietà [**Riepilogo modello**](template-summary.md) indica la piattaforma compatibile con il database di installazione e deve includere il valore per Windows RT.

Windows Installer 5,0 in esecuzione su Windows 10 nei processori Arm64 supporta l'installazione di applicazioni compilate in modo specifico per la piattaforma Arm64.  La proprietà di [**Riepilogo del modello**](template-summary.md) di questi pacchetti deve includere il valore Arm64. 

 
