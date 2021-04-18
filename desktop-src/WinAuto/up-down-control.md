---
title: Controllo Up-Down (riferimento all'elemento MSAA UI)
description: Un controllo di scorrimento, noto anche come controllo di selezione, combina una coppia di pulsanti visualizzati come frecce con un controllo di modifica dell'amico. Facendo clic sulle frecce si incrementa o decrementa il valore nel controllo di modifica.
ms.assetid: 45e56c0f-4ac6-4731-b9a6-be4613bf40ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd2d28acc4c14a89ec73f5994ed0af47202145a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298235"
---
# <a name="up-down-control-msaa-ui-element-reference"></a>Controllo Up-Down (riferimento all'elemento MSAA UI)

> [!Note]  
> Questo argomento descrive gli oggetti **controllo di scorrimento** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La creazione di oggetti **controllo di scorrimento** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Un controllo di scorrimento, noto anche come controllo di selezione, combina una coppia di pulsanti visualizzati come frecce con un controllo di modifica dell'amico. Facendo clic sulle frecce si incrementa o decrementa il valore nel controllo di modifica.

Il nome della classe della finestra per un controllo di scorrimento è UpDown \_ Class, definito come "msctls \_ updown32" in commctrl. h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un controllo di scorrimento supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un controllo di scorrimento supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La proprietà **childCount** è "2", ovvero i pulsanti freccia su e freccia giù.                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La proprietà **Name** per l'oggetto controllo di scorrimento è ottenuta dal testo della finestra del controllo (o didascalia). Questo testo non viene visualizzato con il controllo di scorrimento, quindi gli sviluppatori del server devono fornire testo significativo nell'istruzione di definizione della risorsa del controllo per consentire agli utenti delle utilità client di identificare il controllo. La proprietà **Name** del pulsante freccia in alto nel controllo di scorrimento è "more" e la proprietà **Name** per il pulsante freccia in basso è "less". |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La proprietà **Parent** del controllo di scorrimento è una finestra (finestra del [**\_ sistema di \_ ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo. La proprietà **Parent** dei pulsanti freccia su e freccia giù è l'oggetto controllo di scorrimento.                                                                                                                                                    |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La proprietà **Role** per l'oggetto controllo di scorrimento è [**\_ \_ SPINBUTTON del sistema Role**](object-roles.md). La proprietà **Role** per i pulsanti freccia è [**il \_ \_ pulsante sistema ruolo**](object-roles.md).                                                                                                                                                                                                                          |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La proprietà state per l'oggetto controllo di scorrimento è uno dei [valori](object-state-constants.md)[**seguenti: stato attivo \_ del \_ sistema di stato stato**](object-state-constants.md) \| [**\_ \_ attivo**](object-state-constants.md)<br/>                                                                                                                                                                                      |
| [**ottenere \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Note

Microsoft Active Accessibility espone il controllo di modifica di Buddy come oggetto separato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





