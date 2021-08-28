---
title: Accesso ai Microsoft Active Accessibility server
description: L Microsoft Active Accessibility per Automazione interfaccia utente proxy è un componente software che consente ai client Microsoft Automazione interfaccia utente di interagire con i server Microsoft Active Accessibility che implementano l'interfaccia IAccessible in modo nativo.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Automazione interfaccia utente,accesso Active Accessibility
- Automazione interfaccia utente,Active Accessibility
- proxy Automazione interfaccia utente
- Automazione interfaccia utente,Automazione interfaccia utente Proxy
- Pattern di controllo LegacyIAccessible
- Automazione interfaccia utente,Pattern di controllo LegacyIAccessible
- Microsoft Active Accessibility
- Active Accessibility
- client, accesso Active Accessibility server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6f6ccbc29695b7ca5d1413025a50a7bcf4a9cf679dbcd6a0b8f3160ff0b399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030771"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a>Accesso ai Microsoft Active Accessibility server

Il Microsoft Active Accessibility per Automazione interfaccia utente proxy è un componente software che consente ai client Microsoft Automazione interfaccia utente di interagire con i server Microsoft Active Accessibility che implementano [**l'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in modo nativo. Il proxy supporta il pattern di controllo [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) e fornisce un'istanza [**dell'interfaccia IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) per ogni Microsoft Active Accessibility server rilevato. Automazione interfaccia utente client usano i metodi esposti da **IUIAutomationLegacyIAccessiblePattern** per accedere alle proprietà Microsoft Active Accessibility e agli oggetti supportati dal server.

Se un elemento Automazione interfaccia utente ha un'implementazione Microsoft Active Accessibility sottostante, un client può ottenere un puntatore a interfaccia [**IUIAutomationLegacyIAccessiblePattern per**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) l'elemento passando l'ID del pattern di controllo [**\_ UIA LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) a uno dei metodi [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) seguenti:

-   [**GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [**GetCachedPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [**Getcurrentpattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [**GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

[**L'interfaccia IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) non è disponibile per i controlli basati su Automazione interfaccia utente.

[**L'interfaccia IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) consente Automazione interfaccia utente client di accedere all'implementazione [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sottostante di un Microsoft Active Accessibility elemento . Tuttavia, l'interfaccia non supporta metodi obsoleti o ridondanti con Automazione interfaccia utente funzionalità. Ad esempio, **IUIAutomationLegacyIAccessiblePattern** non ha un metodo equivalente a [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) perché la posizione corrente di un elemento dell'interfaccia utente è disponibile dalla proprietà boundingRectangle di Automazione interfaccia utente.

Il [**metodo IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) consente a un client di recuperare un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) da un Automazione interfaccia utente elemento. Il contrario è possibile anche usando i metodi [**IUIAutomation::ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) e [**IUIAutomation::ElementFromIAccessibleBuildCache.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache)

[**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) restituisce **NULL** se l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento viene fornita da un oggetto proxy da OLEACC.dll o dal Automazione interfaccia utente a Microsoft Active Accessibility Bridge.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Automazione interfaccia utente e Active Accessibility](uiauto-msaa.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




