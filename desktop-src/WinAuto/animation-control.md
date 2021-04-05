---
title: Controllo Animation (riferimento all'elemento MSAA UI)
description: I controlli animazione visualizzano automaticamente un clip audio video con interfoliazione (AVI). I controlli di animazione vengono in genere visualizzati durante la copia dei file o quando viene eseguita un'altra attività che richiede molto tempo.
ms.assetid: 2a31d4ba-a1bd-478b-86a9-726fa93ab714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ca7cf7e4b8a2174dae81b1770b2d877f749502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710693"
---
# <a name="animation-control-msaa-ui-element-reference"></a>Controllo Animation (riferimento all'elemento MSAA UI)

I controlli animazione visualizzano automaticamente un clip audio video con interfoliazione (AVI). I controlli di animazione vengono in genere visualizzati durante la copia dei file o quando viene eseguita un'altra attività che richiede molto tempo.

Il nome della classe della finestra per un controllo animazione è ANIMAte \_ Class, definito come "SysAnimate32" in commctrl. h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli di animazione supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli animazione supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La proprietà **childCount** è zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | I controlli di animazione non dispongono di tasti di scelta rapida. Tuttavia, se l'etichetta per il controllo contiene un tasto di accesso, ovvero un carattere sottolineato nel testo dell'etichetta del controllo, [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) restituisce una stringa non null. Questa stringa contiene il carattere di chiave di accesso aggiunto alla stringa "Alt +". Ad esempio, se l'etichetta è "download dei file", **KeyboardShortcut** è "Alt + d".                                                                                        |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** è ottenuta dal controllo testo statico che etichetta il controllo Animation. Quando si creano i controlli, gli sviluppatori di server devono garantire che un controllo testo statico preceda immediatamente il controllo che etichetta all'interno dell'ordine di tabulazione.                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è [**un' \_ \_ animazione del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è una combinazione di una o più delle seguenti costanti di stato dell'oggetto: stato del sistema di stato [**\_ \_ invisibile**](object-state-constants.md) al sistema dello stato non \| [**\_ \_ disponibile**](object-state-constants.md) sistema stato \| [**\_ \_ attivo**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> Per altre informazioni, vedere [costanti di stato dell'oggetto](object-state-constants.md).<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





