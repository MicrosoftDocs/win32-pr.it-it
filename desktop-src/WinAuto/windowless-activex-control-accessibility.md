---
title: Accessibilità controllo ActiveX senza finestra
description: In questa sezione viene descritto come utilizzare l'API di accessibilità di Windows per assicurarsi che i controlli ActiveX di Microsoft ActiveX siano accessibili.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399414"
---
# <a name="windowless-activex-control-accessibility"></a>Accessibilità controllo ActiveX senza finestra

In questa sezione viene descritto come utilizzare l'API di accessibilità di Windows per assicurarsi che i controlli ActiveX di Microsoft ActiveX siano accessibili.

Windows 8 include nuove interfacce API per l'accessibilità di Windows che semplificano l'implementazione dell'accessibilità per i controlli ActiveX senza finestra. L'API include interfacce implementate in un controllo senza finestra e nel contenitore di controlli, consentendo al controllo senza finestra e al relativo contenitore di interagire per fornire informazioni sull'accessibilità sul controllo senza finestra. L'API supporta gli scenari seguenti:

-   Microsoft Active Accessibility controlli senza finestra ospitati in un contenitore di controlli Active Accessibility Microsoft.
-   Microsoft Active Accessibility controlli senza finestra ospitati in un contenitore di controlli di automazione interfaccia utente Microsoft.
-   Controlli senza finestra di automazione interfaccia utente ospitati in un contenitore di controlli di Microsoft Active Accessibility.
-   Controlli senza finestra di automazione interfaccia utente ospitati in un contenitore di controlli di automazione interfaccia utente.

La tabella seguente elenca le interfacce che supportano i controlli ActiveX senza finestra e identifica gli oggetti che implementano le interfacce.



| Oggetto              | MSAA                                                                             | automazione interfaccia utente                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Oggetto Control      | [**IAccessibleHandler**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Sito di controllo        | [**IAccessibleWindowlessSite**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Radice della finestra host | [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>Contenuto della sezione

-   [Come usare l'automazione dell'interfaccia utente per rendere accessibile un controllo ActiveX senza finestra](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [Come utilizzare MSAA per rendere accessibile un controllo ActiveX senza finestra](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [Come ospitare un controllo ActiveX senza finestra di automazione interfaccia utente](host-a-ui-automation-windowless-activex-control.md)
-   [Come ospitare un controllo ActiveX senza finestra MSAA](host-an-msaa-windowless-activex-control.md)

 

 