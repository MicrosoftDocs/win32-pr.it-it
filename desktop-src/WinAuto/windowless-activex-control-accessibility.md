---
title: Accessibilità dei controlli ActiveX finestra
description: Questa sezione descrive come usare l'Windows API Accessibilità per garantire che i controlli ActiveX Microsoft senza finestra siano accessibili.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3842dd6b9ec18b745e043841936dd811afd1580779d276290057c2fe6d2194cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563456"
---
# <a name="windowless-activex-control-accessibility"></a>Accessibilità dei controlli ActiveX finestra

Questa sezione descrive come usare l'Windows API Accessibilità per garantire che i controlli ActiveX Microsoft senza finestra siano accessibili.

Windows 8 include nuove interfacce Windows API Accessibilità che semplificano l'attività di implementazione dell'accessibilità per i controlli ActiveX finestra. L'API include interfacce implementate in un controllo senza finestra e nel contenitore di controlli, consentendo al controllo senza finestra e al relativo contenitore di lavorare insieme per fornire informazioni sull'accessibilità sul controllo senza finestra. L'API supporta gli scenari seguenti:

-   Microsoft Active Accessibility controlli senza finestra ospitati in un Microsoft Active Accessibility contenitore di controlli.
-   Microsoft Active Accessibility controlli senza finestra ospitati in un contenitore di controlli Automazione interfaccia utente Microsoft.
-   Automazione interfaccia utente controlli senza finestra ospitati in un Microsoft Active Accessibility contenitore di controlli.
-   Automazione interfaccia utente controlli senza finestra ospitati in un Automazione interfaccia utente contenitore di controlli.

Nella tabella seguente sono elencate le interfacce che supportano ActiveX e identificano gli oggetti che implementano le interfacce.



| Oggetto              | MSAA                                                                             | automazione interfaccia utente                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Oggetto Control      | [**IAccessibleHandler**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Sito di controllo        | [**IAccessibleWindowlessSite**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Radice della finestra host | [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>Contenuto della sezione

-   [Come usare le Automazione interfaccia utente rendere accessibile un controllo ActiveX finestra](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [Come usare MSAA per rendere accessibile un controllo ActiveX finestra](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [Come ospitare un controllo Automazione interfaccia utente senza ActiveX finestra](host-a-ui-automation-windowless-activex-control.md)
-   [Come ospitare un controllo ActiveX msaa](host-an-msaa-windowless-activex-control.md)

 

 