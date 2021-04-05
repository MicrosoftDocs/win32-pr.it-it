---
title: Finestra switch (riferimento all'elemento dell'interfaccia utente MSAA)
description: La finestra di commutazione viene visualizzata ogni volta che un utente preme ALT + TAB per passare a un'altra applicazione. La finestra switch contiene un'icona per ogni applicazione attualmente in esecuzione.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eead618e23f8a56c90b37eae2386f16a90f6dd67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714128"
---
# <a name="switch-window-msaa-ui-element-reference"></a>Finestra switch (riferimento all'elemento dell'interfaccia utente MSAA)

La finestra di commutazione viene visualizzata ogni volta che un utente preme ALT + TAB per passare a un'altra applicazione. La finestra switch contiene un'icona per ogni applicazione attualmente in esecuzione.

Il nome della classe di finestra per la finestra switch è " \# 32771".

## <a name="iaccessible-methods"></a>Metodi IAccessible

La finestra switch supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Metodo                                                                    | Commenti                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | L'oggetto finestra switch non dispone di una proprietà **DefaultAction** . Il metodo [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) per ogni elemento nella finestra switch attiva l'elemento specificato. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

La finestra switch supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



|                                                                                |                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | La proprietà **childCount** è zero.                                                                                                                                                                                           |
| [**ottenere \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | L'oggetto finestra switch non dispone di una proprietà **DefaultAction** . La proprietà **DefaultAction** per ogni elemento nella finestra switch è "switch".                                                                     |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | L'oggetto padre della finestra switch non può ricevere lo stato attivo; solo i singoli figli possono ricevere lo stato attivo.                                                                                                                          |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | L'oggetto finestra switch non dispone di una proprietà **Name** . La proprietà **Name** per ogni icona dell'applicazione nella finestra switch corrisponde al nome dell'applicazione visualizzato.                                         |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | L'oggetto finestra switch ha una proprietà **Role** di "window \[ 32771 \] ". Inoltre, ogni icona dell'applicazione nella finestra del commutire presenta il ruolo proprietà del ruolo proprietà **del ruolo.** [**\_ \_**](object-roles.md) |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | L'oggetto finestra switch non supporta la proprietà **state** . Il valore **dello stato** per gli elementi della visualizzazione elenco è [**stato \_ \_ attivabile dal sistema di stato**](object-state-constants.md).                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




