---
title: Accesso ai server Microsoft Active Accessibility
description: Microsoft Active Accessibility al proxy di automazione interfaccia utente è un componente software che consente ai client di automazione interfaccia utente Microsoft di interagire con i server Microsoft Active Accessibility che implementano l'interfaccia IAccessible in modo nativo.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Automazione interfaccia utente, accesso Active Accessibility
- Automazione interfaccia utente, Active Accessibility
- Proxy di automazione interfaccia utente
- Automazione interfaccia utente, proxy di automazione interfaccia utente
- Pattern di controllo LegacyIAccessible
- Automazione interfaccia utente, pattern di controllo LegacyIAccessible
- Microsoft Active Accessibility
- Active Accessibility
- client, accesso a server Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97319028203351cd9f45b39d133fa38727d6861e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044413"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a>Accesso ai server Microsoft Active Accessibility

Microsoft Active Accessibility al proxy di automazione interfaccia utente è un componente software che consente ai client di automazione interfaccia utente Microsoft di interagire con i server Microsoft Active Accessibility che implementano l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in modo nativo. Il proxy supporta il pattern di controllo [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) e fornisce un'istanza dell'interfaccia [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) per ogni server Active Accessibility Microsoft rilevato. I client di automazione interfaccia utente usano i metodi esposti da **IUIAutomationLegacyIAccessiblePattern** per accedere alle proprietà e agli oggetti di Microsoft Active Accessibility supportati dal server.

Se un elemento di automazione interfaccia utente dispone di un'implementazione di Microsoft Active Accessibility sottostante, un client può ottenere un puntatore di interfaccia [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) per l'elemento passando l'ID del pattern di controllo [**\_ LegacyIAccessiblePatternId di UIA**](uiauto-controlpattern-ids.md) a uno dei seguenti metodi [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) :

-   [**GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [**GetCachedPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [**GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [**GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

L'interfaccia [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) non è disponibile per i controlli basati sull'automazione dell'interfaccia utente.

L'interfaccia [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) consente ai client di automazione interfaccia utente di accedere all'implementazione [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sottostante di un elemento Active Accessibility Microsoft. Tuttavia, l'interfaccia non supporta i metodi obsoleti o ridondanti con le funzionalità di automazione interfaccia utente. Ad esempio, **IUIAutomationLegacyIAccessiblePattern** non dispone di un metodo equivalente a [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) perché la posizione corrente di un elemento dell'interfaccia utente è disponibile dalla proprietà BoundingRectangle di automazione interfaccia utente.

Il metodo [**IUIAutomationLegacyIAccessiblePattern:: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) consente a un client di recuperare un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) da un elemento di automazione interfaccia utente. Il contrario è possibile anche usando i metodi [**IUIAutomation:: ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) e [**IUIAutomation:: ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) .

[**IUIAutomationLegacyIAccessiblePattern:: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) restituisce **null** se l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento viene fornita da un oggetto proxy da OLEACC.dll o dall'automazione interfaccia utente a Microsoft Active Accessibility Bridge.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Automazione interfaccia utente e Active Accessibility](uiauto-msaa.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




