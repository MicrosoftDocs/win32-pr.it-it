---
title: Controllo barra di stato (riferimento all'elemento MSAA UI)
description: Le barre di stato visualizzano le informazioni sullo stato in una finestra orizzontale nella parte inferiore di una finestra dell'applicazione.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81bddf2898b9b7eca5385d86d6dabc6a50d3d4df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332231"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a>Controllo barra di stato (riferimento all'elemento MSAA UI)

> [!Note]  
> Questo argomento descrive gli oggetti **controllo barra di stato** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La creazione di oggetti **controllo barra di stato** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Le barre di stato visualizzano le informazioni sullo stato in una finestra orizzontale nella parte inferiore di una finestra dell'applicazione. Le barre di stato sono spesso divise in parti, denominate riquadri e ogni riquadro Visualizza informazioni sullo stato diverse. Inoltre, le barre di stato possono contenere oggetti di tipi diversi, inclusi pulsanti e barre di stato. Il nome della classe della finestra per un controllo barra di stato è STATUSCLASSNAME, definito come "msctls \_ statusbar32" in commctrl. h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Le barre di stato supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Le barre di stato supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La proprietà **childCount** è il numero di riquadri nella barra di stato.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | L'oggetto barra di stato non dispone di una proprietà **Name** . La proprietà **Name** di ogni riquadro nella barra di stato corrisponde al testo visualizzato.                                                                                                                                                                                                                                                                                                                   |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La proprietà **Parent** dell'oggetto barra di stato è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha lo stesso nome della classe della finestra del controllo. La proprietà **Parent** dei riquadri della barra di stato è l'oggetto della barra di stato.                                                                                                                                                                           |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La proprietà **Role** per l'oggetto barra di stato stesso è il [**sistema del ruolo \_ \_ StatusBar**](object-roles.md). Il testo visualizzato in una barra di stato [**ha \_ \_ STATICTEXT del sistema ruolo**](object-roles.md) come proprietà del **ruolo** .                                                                                                                                                                                                 |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile<br/> |



 

## <a name="notes"></a>Note

Poiché i tasti di scelta rapida non sono supportati per i controlli barra di stato o le aree di testo nelle barre di stato, [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) non è supportato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





