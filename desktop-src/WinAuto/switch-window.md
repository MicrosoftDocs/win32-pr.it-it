---
title: Finestra Switch (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)
description: La finestra switch viene visualizzata ogni volta che un utente preme ALT+TAB per passare a un'applicazione diversa. La finestra switch contiene un'icona per ogni applicazione attualmente in esecuzione.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa12b5fa3bfb9e6207ddaff4133b030e6c233c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443982"
---
# <a name="switch-window-msaa-ui-element-reference"></a>Finestra Switch (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)

La finestra switch viene visualizzata ogni volta che un utente preme ALT+TAB per passare a un'applicazione diversa. La finestra switch contiene un'icona per ogni applicazione attualmente in esecuzione.

Il nome della classe della finestra per la finestra switch è \# "32771".

## <a name="iaccessible-methods"></a>Metodi IAccessible

La finestra switch supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Metodo                                                                    | Commenti                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | L'oggetto finestra del commutatore stesso non ha una **proprietà DefaultAction.** Il [**metodo accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) per ogni elemento nella finestra switch attiva l'elemento specificato. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

La finestra switch supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



|      Proprietà                                                                          |      Descrizione                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | La **proprietà ChildCount** è zero.                                                                                                                                                                                           |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | L'oggetto finestra del commutatore stesso non ha una **proprietà DefaultAction.** La **proprietà DefaultAction** per ogni elemento nella finestra switch è "Switch".                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | L'oggetto padre della finestra di commutazione non può ricevere lo stato attivo. solo i singoli elementi figlio possono ricevere lo stato attivo.                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | L'oggetto finestra del commutatore non ha una **proprietà** Name. La **proprietà Name** per ogni icona dell'applicazione nella finestra switch corrisponde al nome dell'applicazione visualizzato.                                         |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | L'oggetto finestra del commutatore stesso ha una **proprietà Role** "window \[ 32771". \] Inoltre, ogni icona dell'applicazione nella finestra switch ha la **proprietà Role** [**ROLE SYSTEM \_ \_ LISTITEM**](object-roles.md). |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | L'oggetto finestra del commutatore non supporta la **proprietà** State. Il **valore State** per gli elementi della visualizzazione elenco è STATE SYSTEM [**\_ \_ FOCUSABLE.**](object-state-constants.md)                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




