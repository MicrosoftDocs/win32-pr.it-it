---
title: Controllo Barra di stato (riferimento all'elemento MSAA dell'interfaccia utente)
description: Le barre di stato visualizzano le informazioni sullo stato in una finestra orizzontale nella parte inferiore di una finestra dell'applicazione.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6c4955bfe10bc7eb224213a8e2e262179d2b122ca4eae210d0d1e72e4635b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998061"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a>Controllo Barra di stato (riferimento all'elemento MSAA dell'interfaccia utente)

> [!Note]  
> Questo argomento descrive gli oggetti **Controllo barra di stato** ai fini delle informazioni di riferimento sugli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti controllo barra di** stato in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento dell'API per il framework dell'interfaccia utente in uso.

 

Le barre di stato visualizzano le informazioni sullo stato in una finestra orizzontale nella parte inferiore di una finestra dell'applicazione. Le barre di stato sono spesso suddivise in parti, denominate riquadri, e ogni riquadro visualizza informazioni sullo stato diverse. Inoltre, le barre di stato possono contenere oggetti di tipi diversi, inclusi pulsanti e barre di stato. Il nome della classe della finestra per un controllo barra di stato è STATUSCLASSNAME, definito come "msctls \_ statusbar32" in Commctrl.h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Le barre di stato supportano i [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Le barre di stato supportano le [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La **proprietà ChildCount** è il numero di riquadri nella barra di stato.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | L'oggetto barra di stato stesso non ha una **proprietà** Name. La **proprietà Name** di ogni riquadro nella barra di stato corrisponde al testo visualizzato.                                                                                                                                                                                                                                                                                                                   |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La **proprietà Parent** dell'oggetto barra di stato è una finestra ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) che racchiude il controllo e ha lo stesso nome della classe della finestra del controllo. La **proprietà Parent** dei riquadri nella barra di stato è l'oggetto barra di stato.                                                                                                                                                                           |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La **proprietà Role** per l'oggetto barra di stato è ROLE SYSTEM [**\_ \_ STATUSBAR**](object-roles.md). Il testo visualizzato in una barra di stato ha [**ROLE \_ SYSTEM \_ STATICTEXT**](object-roles.md) come **proprietà Role.**                                                                                                                                                                                                 |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Note

Poiché i tasti di scelta rapida non sono supportati per i controlli barra di stato o le aree di testo nelle barre di stato, [**il metodo \_ get accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) non è supportato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





