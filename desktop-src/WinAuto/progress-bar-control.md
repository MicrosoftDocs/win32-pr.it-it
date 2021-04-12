---
title: Controllo indicatore di stato (riferimento all'elemento MSAA UI)
description: I controlli indicatore di stato indicano lo stato di avanzamento di un'operazione di lunga durata, ad esempio il download di un file da Internet. In genere lo stato di avanzamento è espresso come percentuale da zero (0) a 100 (100).
ms.assetid: 9165d00e-b3f3-41cd-812c-cd39313460fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9bbd9a648ee1c4d4f112577c8e41a5983f69038
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221799"
---
# <a name="progress-bar-control-msaa-ui-element-reference"></a>Controllo indicatore di stato (riferimento all'elemento MSAA UI)

> [!Note]  
> In questo argomento vengono descritti gli oggetti **controllo indicatore di stato** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La procedura per la creazione di oggetti **controllo indicatore di stato** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

I controlli indicatore di stato indicano lo stato di avanzamento di un'operazione di lunga durata, ad esempio il download di un file da Internet. In genere lo stato di avanzamento è espresso come percentuale da zero (0) a 100 (100).

Il nome della classe della finestra per un controllo indicatore di stato è la \_ classe Progress, definita come "msctls \_ Progress" in commctrl. h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli indicatore di stato supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli indicatore di stato supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La proprietà **childCount** è zero.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La proprietà **KeyboardShortcut** è la chiave di accesso dell'indicatore di stato, che è un carattere sottolineato nel testo dell'etichetta per l'indicatore di stato. La stringa restituita contiene il carattere di chiave di accesso aggiunto alla stringa "Alt +".                                                                                                                                                                                                                                 |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** è il testo di un controllo testo statico che etichetta l'indicatore di stato.                                                                                                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.                                                                                                                                                                                                                                                              |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è [**\_ \_ PROGRESSBAR del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                      |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile<br/> |
| [**ottenere \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La proprietà **value** è una stringa da "0%" a "100%" che descrive lo stato di avanzamento.                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





