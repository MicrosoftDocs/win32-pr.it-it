---
title: Window (riferimento all'elemento MSAA UI)
description: Microsoft Active Accessibility crea un oggetto finestra generico come contenitore per un altro oggetto. Gli sviluppatori client non trasmettono le informazioni dagli oggetti finestra agli utenti finali, perché questi oggetti non contengono informazioni utili.
ms.assetid: cc32528f-c454-4522-91b9-06f87cff8bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87c8601ecd6344dc82bbdb416055c694687e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709271"
---
# <a name="window-msaa-ui-element-reference"></a>Window (riferimento all'elemento MSAA UI)

> [!Note]  
> Questo argomento descrive gli oggetti **Window** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La creazione di oggetti **finestra** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Microsoft Active Accessibility crea un oggetto finestra generico come contenitore per un altro oggetto. Gli sviluppatori client non trasmettono le informazioni dagli oggetti finestra agli utenti finali, perché questi oggetti non contengono informazioni utili.

Se un'applicazione server crea un controllo personalizzato, Microsoft Active Accessibility crea un oggetto finestra che contiene il controllo personalizzato, ma il server crea un oggetto accessibile per fornire informazioni sul contenuto del controllo. Il sistema genera eventi a livello di oggetto per l'oggetto finestra, ma il server deve inviare eventi per l'oggetto accessibile che fornisce informazioni sul controllo.

## <a name="iaccessible-methods"></a>Metodi IAccessible

L'oggetto finestra supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

L'oggetto finestra supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera l'interfaccia [IDispatch](idispatch-interface.md) dell'elemento figlio specificato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La proprietà **childCount** è 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | L'oggetto finestra non dispone di una proprietà **Description** . La proprietà **Description** per l'oggetto figlio può essere recuperata tramite l'oggetto Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | L'oggetto finestra non dispone di una proprietà **KeyboardShortcut** . La proprietà **KeyboardShortcut** per l'oggetto figlio viene recuperata tramite l'oggetto finestra.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** dell'oggetto Window è uguale a quella dell'oggetto figlio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è [**la \_ \_ finestra del sistema Role**](object-roles.md). Il **ruolo** dell'oggetto figlio viene recuperato tramite l'oggetto finestra.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato [**\_ sistema \_ invisibile**](object-state-constants.md) allo stato sistema stato non \| [**\_ \_ disponibile**](object-state-constants.md) sistema stato stato attivo sistema stato stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ attivo**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Note

Gli eventi [**\_ sistema \_ DRAGDROPSTART**](event-constants.md), [**\_ \_ DRAGDROPEND**](event-constants.md)eventi, [**\_ \_ Nascondi oggetti evento**](event-constants.md)e [**\_ \_ PARENTCHANGE oggetto evento**](event-constants.md) non vengono inviati dall'oggetto finestra. Si tratta di un problema noto che viene risolto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





