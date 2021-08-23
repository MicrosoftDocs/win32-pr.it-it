---
title: Controllo Indicatore di stato (riferimenti a elementi dell'interfaccia utente MSAA)
description: I controlli indicatore di stato indicano lo stato di avanzamento di un'operazione di lunga durata, ad esempio il download di un file da Internet. In genere lo stato di avanzamento è espresso come percentuale da zero (0) a 100 (100).
ms.assetid: 9165d00e-b3f3-41cd-812c-cd39313460fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a96b692de7b4c3992bab82eaa2461ce2826e5117498c24be7d8e40913d8a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052559"
---
# <a name="progress-bar-control-msaa-ui-element-reference"></a>Controllo Indicatore di stato (riferimenti a elementi dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **Controllo indicatore di stato** ai fini delle informazioni di riferimento sugli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti controllo Indicatore di** stato in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento dell'API per il framework dell'interfaccia utente in uso.

 

I controlli indicatore di stato indicano lo stato di avanzamento di un'operazione di lunga durata, ad esempio il download di un file da Internet. In genere lo stato di avanzamento è espresso come percentuale da zero (0) a 100 (100).

Il nome della classe della finestra per un controllo indicatore di stato è PROGRESS CLASS, definito \_ come "msctls \_ progress" in Commctrl.h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli indicatore di stato supportano i [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli indicatore di stato supportano le [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **proprietà ChildCount** è zero.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **proprietà KeyboardShortcut** è il tasto di scelta dell'indicatore di stato, ovvero un carattere sottolineato nel testo dell'etichetta per l'indicatore di stato. La stringa restituita contiene il carattere del tasto di scelta aggiunto alla stringa "Alt+".                                                                                                                                                                                                                                 |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** è il testo di un controllo testo statico che etichetta l'indicatore di stato.                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **proprietà Parent** è una finestra ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra del controllo.                                                                                                                                                                                                                                                              |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ PROGRESSBAR.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md)[**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La **proprietà Value** è una stringa da "0%" a "100%" che descrive lo stato di avanzamento.                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





