---
title: Controllo Calendar (riferimento all'elemento MSAA UI)
description: I controlli calendario consentono a un utente di selezionare una data da un'interfaccia familiare in modo semplice e intuitivo.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855781"
---
# <a name="calendar-control-msaa-ui-element-reference"></a>Controllo Calendar (riferimento all'elemento MSAA UI)

> [!Note]  
> In questo argomento vengono descritti gli oggetti **controllo calendario** per gli scopi del riferimento all'elemento dell'interfaccia utente MSAA. La creazione di oggetti **controllo calendario** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

I controlli calendario consentono a un utente di selezionare una data da un'interfaccia familiare in modo semplice e intuitivo.

Il nome della classe della finestra per un controllo calendario mensile è la \_ classe MONTHCAL, definita come "SysMonthCal32" in commctrl. h. Le informazioni contenute in questo argomento si applicano al controllo calendario mensile nella versione 5 di COMmctrl. h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli Calendar supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli Calendar supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La proprietà **childCount** è zero.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La proprietà **Name** è ottenuta dal controllo testo statico che etichetta il controllo Calendar. Quando si creano i controlli, gli sviluppatori di server devono garantire che un controllo testo statico preceda immediatamente il controllo che etichetta all'interno dell'ordine di tabulazione.                                                                                                                                                                                                                 |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.                                                                                                                                                                                                                                                             |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La proprietà **Role** è [**un \_ \_ client del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La proprietà **state** è una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: lo stato del sistema dello stato [**\_ \_ Invisible**](object-state-constants.md) sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





