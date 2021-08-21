---
title: Up-Down (riferimento all'elemento DELL'interfaccia utente MSAA)
description: Un controllo di scorrimento, noto anche come controllo di selezione, combina una coppia di pulsanti visualizzati come frecce con un controllo di modifica. Facendo clic sulle frecce viene incrementato o decrementato il valore nel controllo di modifica.
ms.assetid: 45e56c0f-4ac6-4731-b9a6-be4613bf40ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b9475d8bbca24d2bf536a4eb9a9decf078297e788a37aa4d8560029a67e50e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114626"
---
# <a name="up-down-control-msaa-ui-element-reference"></a>Up-Down (riferimento all'elemento DELL'interfaccia utente MSAA)

> [!Note]  
> In questo argomento vengono descritti **gli oggetti controllo up-down** ai fini delle informazioni di riferimento sugli elementi dell'interfaccia utente MSAA. La procedura per la **creazione di oggetti controllo up-down** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento dell'API per il framework dell'interfaccia utente in uso.

 

Un controllo di scorrimento, noto anche come controllo di selezione, combina una coppia di pulsanti visualizzati come frecce con un controllo di modifica. Facendo clic sulle frecce viene incrementato o decrementato il valore nel controllo di modifica.

Il nome della classe della finestra per un controllo di tipo up-down è UPDOWN CLASS, definito \_ come "msctls \_ updown32" in Commctrl.h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un controllo di tipo up-down supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un controllo di tipo up-down supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La **proprietà ChildCount** è "2" (i pulsanti freccia su e giù).                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La **proprietà Name** per l'oggetto controllo verso l'alto viene ottenuta dal testo della finestra (o didascalia) del controllo. Questo testo non viene visualizzato con il controllo di riepilogo, quindi gli sviluppatori del server devono fornire testo significativo nell'istruzione di definizione delle risorse del controllo per consentire agli utenti delle utilità client di identificare il controllo. La **proprietà Name** per il pulsante freccia superiore nel controllo verso l'alto è "More" e la proprietà **Name** per il pulsante freccia inferiore è "Less". |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La **proprietà Parent** del controllo verso l'alto è una finestra ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra del controllo. La **proprietà Parent** dei pulsanti freccia SU e FRECCIA GIÙ è l'oggetto controllo verso il basso.                                                                                                                                                    |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La **proprietà Role** per l'oggetto controllo verso l'alto è ROLE SYSTEM [**\_ \_ SPINBUTTON.**](object-roles.md) La **proprietà Role** per i pulsanti freccia è ROLE SYSTEM [**\_ \_ PUSHBUTTON**](object-roles.md).                                                                                                                                                                                                                          |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La proprietà State per l'oggetto controllo di livello superiore è uno dei valori [seguenti:](object-state-constants.md)[**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/>                                                                                                                                                                                      |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Note

Microsoft Active Accessibility espone il controllo di modifica del controllo come oggetto separato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





