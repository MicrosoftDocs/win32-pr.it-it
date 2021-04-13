---
title: Controllo tasto di scelta (riferimento all'elemento MSAA UI)
description: I controlli tasto di scelta consentono agli utenti di immettere una combinazione di sequenze di tasti utilizzate come tasto di scelta, che consente loro di eseguire rapidamente un'azione. Un controllo tasto di scelta consente di visualizzare le sequenze di tasti immesse dall'utente e garantisce che l'utente selezioni una combinazione di tasti valida.
ms.assetid: 56c9fee4-f3d3-4f61-8587-bf80186aa5b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aed12ce64fe25c091f6204d9143a0c6ebefb65a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331436"
---
# <a name="hot-key-control-msaa-ui-element-reference"></a>Controllo tasto di scelta (riferimento all'elemento MSAA UI)

I controlli tasto di scelta consentono agli utenti di immettere una combinazione di sequenze di tasti utilizzate come tasto di scelta, che consente loro di eseguire rapidamente un'azione. Un controllo tasto di scelta consente di visualizzare le sequenze di tasti immesse dall'utente e garantisce che l'utente selezioni una combinazione di tasti valida.

Il nome della classe della finestra per un controllo tasto di scelta è la \_ classe hotkey, definita come "msctls \_ hotkey32" in commctrl. h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli tasto di scelta supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli tasto di scelta supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La proprietà **childCount** è sempre zero.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La proprietà **KeyboardShortcut** è la chiave di accesso del controllo tasto di scelta, che è un carattere sottolineato nel testo dell'etichetta del controllo tasto di scelta. La stringa restituita contiene il carattere di chiave di accesso aggiunto alla stringa "Alt +".                                                                                                                                                                                                                                 |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** è il testo di un controllo testo statico che etichetta il controllo tasto di scelta.                                                                                                                                                                                                                                                                                                                                                                            |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.                                                                                                                                                                                                                                                              |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è [**\_ \_ HOTKEYFIELD del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                      |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile<br/> |
| [**ottenere \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La proprietà **value** è una stringa che contiene il testo nel campo del tasto di scelta.                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





