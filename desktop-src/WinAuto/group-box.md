---
title: Casella di gruppo (riferimento all'elemento MSAA UI)
description: Una casella di gruppo è un rettangolo che racchiude un set di controlli, ad esempio caselle di controllo o pulsanti di opzione, e contiene un testo definito dall'applicazione (etichetta).
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712571"
---
# <a name="group-box-msaa-ui-element-reference"></a>Casella di gruppo (riferimento all'elemento MSAA UI)

> [!Note]  
> Questo argomento descrive gli oggetti **casella di gruppo** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La creazione di oggetti **casella di gruppo** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Una casella di gruppo è un rettangolo che racchiude un set di controlli, ad esempio caselle di controllo o pulsanti di opzione, e contiene un testo definito dall'applicazione (etichetta).

L'unico scopo di una casella di gruppo è organizzare i controlli correlati da uno scopo comune, indicato dall'etichetta.

Il nome della classe della finestra per una casella di gruppo è "BUTTON".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Una casella di gruppo supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Una casella di gruppo supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La proprietà **childCount** è sempre zero.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Le caselle di gruppo non dispongono di tasti di scelta rapida. Tuttavia, se il testo della finestra per la casella di gruppo contiene un carattere e commerciale (&), Microsoft Active Accessibility restituisce una stringa non null come proprietà **KeyboardShortcut** .                                                                                                                                                                                                                                            |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** viene ottenuta dal testo della finestra del controllo (o didascalia), visualizzata con la casella di gruppo.                                                                                                                                                                                                                                                                                                                                                    |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.                                                                                                                                                                                                                                                              |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è [**il \_ \_ raggruppamento del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                            |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





