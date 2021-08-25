---
title: Controllo Animation (riferimento all'elemento DELL'interfaccia utente MSAA)
description: I controlli di animazione visualizzano automaticamente un clip AVI (Audio Video Interleaved). I controlli di animazione vengono in genere visualizzati quando i file vengono copiati o quando viene eseguita un'altra attività dispendiosa in termini di tempo.
ms.assetid: 2a31d4ba-a1bd-478b-86a9-726fa93ab714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c7f134d5acdd3496f76e3399e5aafd1fcb2664aed37e042bb7c2cfca60f922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326855"
---
# <a name="animation-control-msaa-ui-element-reference"></a>Controllo Animation (riferimento all'elemento DELL'interfaccia utente MSAA)

I controlli di animazione visualizzano automaticamente un clip AVI (Audio Video Interleaved). I controlli di animazione vengono in genere visualizzati quando i file vengono copiati o quando viene eseguita un'altra attività dispendiosa in termini di tempo.

Il nome della classe della finestra per un controllo di animazione è ANIMATE CLASS, definito \_ come "SysAnimate32" in Commctrl.h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli di animazione supportano i [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli di animazione supportano le [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **proprietà ChildCount** è zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | I controlli di animazione non dispongono di tasti di scelta rapida. Tuttavia, se l'etichetta per il controllo contiene un tasto di scelta (un carattere sottolineato nel testo dell'etichetta del controllo), [**il metodo \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) restituisce una stringa non NULL. Questa stringa contiene il carattere del tasto di scelta aggiunto alla stringa "ALT+". Ad esempio, se l'etichetta è "Download di file", **KeyboardShortcut** è "ALT+d".                                                                                        |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** viene ottenuta dal controllo di testo statico che etichetta il controllo di animazione. Quando creano controlli, gli sviluppatori del server devono assicurarsi che un controllo di testo statico preceda immediatamente il controllo etichettato all'interno dell'ordine di tabulazione.                                                                                                                                                                                                                                                                                             |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà Parent è una finestra ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md)  ) che racchiude il controllo e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra del controllo.                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ ANIMATION.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di una o più delle costanti di stato dell'oggetto seguenti: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ ANIMATED**](object-state-constants.md)<br/> Per altre informazioni, vedere [Costanti dello stato dell'oggetto](object-state-constants.md).<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





