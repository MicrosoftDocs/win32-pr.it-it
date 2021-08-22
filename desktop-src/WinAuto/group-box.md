---
title: Casella di gruppo (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)
description: Una casella di gruppo è un rettangolo che racchiude un set di controlli, ad esempio caselle di controllo o pulsanti di opzione, e contiene un testo definito dall'applicazione (etichetta).
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06675a1ffa88e83bc3c5e36f5d8410682e797169b83e98aa1680b0f0c50d28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860321"
---
# <a name="group-box-msaa-ui-element-reference"></a>Casella di gruppo (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **Group Box** ai fini del riferimento agli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti Casella di gruppo** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il framework dell'interfaccia utente in uso.

 

Una casella di gruppo è un rettangolo che racchiude un set di controlli, ad esempio caselle di controllo o pulsanti di opzione, e contiene un testo definito dall'applicazione (etichetta).

L'unico scopo di una casella di gruppo è organizzare i controlli correlati in base a uno scopo comune, indicato dall'etichetta.

Il nome della classe della finestra per una casella di gruppo è "BUTTON".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Una casella di gruppo supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Una casella di gruppo supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **proprietà ChildCount** è sempre zero.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Le caselle di gruppo non dispongono di tasti di scelta rapida. Tuttavia, se il testo della finestra per la casella di gruppo contiene un carattere e commerciale (&), Microsoft Active Accessibility restituisce una stringa non Null come **proprietà KeyboardShortcut.**                                                                                                                                                                                                                                            |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** viene ottenuta dal testo (o didascalia) della finestra del controllo, visualizzato con la casella di gruppo.                                                                                                                                                                                                                                                                                                                                                    |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà Parent è una finestra ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md)  ) che racchiude il controllo e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra del controllo.                                                                                                                                                                                                                                                              |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ GROUPING.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md)[**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





