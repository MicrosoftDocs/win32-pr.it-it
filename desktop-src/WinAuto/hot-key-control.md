---
title: Controllo tasto di scelta rapida (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)
description: I controlli tasto di scelta rapida consentono agli utenti di immettere una combinazione di sequenze di tasti usate come tasto di scelta rapida, che consente di eseguire rapidamente un'azione. Un controllo tasto di scelta rapida visualizza le sequenze di tasti immesse dall'utente e garantisce che l'utente seleziona una combinazione di tasti valida.
ms.assetid: 56c9fee4-f3d3-4f61-8587-bf80186aa5b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53829b371ea026c92388e8ed0dac11ee0303514ff930ad1a64ada4b5583bfa60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734441"
---
# <a name="hot-key-control-msaa-ui-element-reference"></a>Controllo tasto di scelta rapida (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)

I controlli tasto di scelta rapida consentono agli utenti di immettere una combinazione di sequenze di tasti usate come tasto di scelta rapida, che consente di eseguire rapidamente un'azione. Un controllo tasto di scelta rapida visualizza le sequenze di tasti immesse dall'utente e garantisce che l'utente seleziona una combinazione di tasti valida.

Il nome della classe della finestra per un controllo tasto di scelta rapida è HOTKEY CLASS, definito \_ come "msctls \_ hotkey32" in Commctrl.h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli tasto di scelta rapida supportano i [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli tasto di scelta rapida supportano le [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **proprietà ChildCount** è sempre zero.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **proprietà KeyboardShortcut** è il tasto di scelta del controllo tasto di scelta, ovvero un carattere sottolineato nel testo dell'etichetta del controllo tasto di scelta rapida. La stringa restituita contiene il carattere del tasto di scelta aggiunto alla stringa "ALT+".                                                                                                                                                                                                                                 |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** è il testo di un controllo testo statico che etichetta il controllo tasto di scelta rapida.                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà Parent è una finestra ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md)  ) che racchiude il controllo e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra del controllo.                                                                                                                                                                                                                                                              |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ HOTKEYFIELD.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md)[**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La **proprietà Value** è una stringa che contiene il testo nel campo del tasto di scelta rapida.                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





