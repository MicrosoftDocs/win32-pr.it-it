---
title: Controllo Calendar (riferimento all'elemento DELL'interfaccia utente MSAA)
description: I controlli calendario offrono un modo semplice e intuitivo per consentire a un utente di selezionare una data da un'interfaccia familiare.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f41daf9e86f178f4b22a7908e4d9d10d1dab1a2f867ca2d09c62d111cbc806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899556"
---
# <a name="calendar-control-msaa-ui-element-reference"></a>Controllo Calendar (riferimento all'elemento DELL'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **Calendar Control** ai fini delle informazioni di riferimento sugli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti controllo Calendar** in vari framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il framework dell'interfaccia utente in uso.

 

I controlli calendario offrono un modo semplice e intuitivo per consentire a un utente di selezionare una data da un'interfaccia familiare.

Il nome della classe della finestra per un controllo calendario mensile è MONTHCAL CLASS, definito \_ come "SysMonthCal32" in Commctrl.h. Le informazioni contenute in questo argomento si applicano al controllo calendario mensile nella versione 5 di Commctrl.h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli Calendar supportano i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli Calendar supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La **proprietà ChildCount** è zero.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La **proprietà Name** viene ottenuta dal controllo testo statico che etichetta il controllo calendario. Quando creano controlli, gli sviluppatori del server devono assicurarsi che un controllo testo statico preceda immediatamente il controllo etichettato all'interno dell'ordine di tabulazione.                                                                                                                                                                                                                 |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La proprietà Parent è una finestra ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md)  ) che racchiude il controllo e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra del controllo.                                                                                                                                                                                                                                                             |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La **proprietà Role** è ROLE SYSTEM [**\_ \_ CLIENT**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La **proprietà State** è una combinazione di uno o più dei valori [SEGUENTI](object-state-constants.md)[**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





