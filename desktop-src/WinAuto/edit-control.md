---
title: Controllo di modifica (riferimento all'elemento MSAA UI)
description: I controlli di modifica consentono a un utente di visualizzare e modificare il testo.
ms.assetid: a42c73f2-4005-4db9-84bc-637c9c4310f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dde6e562b651b91376bc7d675b2b71ac999cf48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516099"
---
# <a name="edit-control-msaa-ui-element-reference"></a>Controllo di modifica (riferimento all'elemento MSAA UI)

> [!Note]  
> In questo argomento vengono descritti gli oggetti di **controllo di modifica** per scopi di riferimento all'elemento dell'interfaccia utente MSAA. La procedura per la creazione di oggetti **controllo di modifica** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

I controlli di modifica consentono a un utente di visualizzare e modificare il testo. I controlli di modifica vengono creati con molti stili diversi, ad esempio ES \_ Multiline. Con questo stile viene creato un controllo di modifica su più righe, ad esempio l'area client del blocco note e l'ES \_ ReadOnly, che crea un controllo di modifica di sola lettura.

Microsoft Active Accessibility non fa distinzione tra i controlli di modifica creati con il nome della classe di finestra "EDIT" e i controlli Rich Edit creati con il nome della classe della finestra "RichEdit" o "RichEdit20A".

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli di modifica supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli di modifica supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ottenere \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La proprietà **KeyboardShortcut** è la chiave di accesso del controllo di modifica, che è un carattere sottolineato nel testo dell'etichetta del controllo di modifica. Ad esempio, in una finestra di dialogo Apri file standard, ad esempio in WordPad, il **KeyboardShortcut** per il controllo di modifica con etichetta "nomefile:" è "Alt + n".                                                                                                                                                                                                                                                                                                                                        |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** è il testo di un controllo testo statico che etichetta il controllo di modifica. Ad esempio, in una finestra di dialogo Apri file standard, ad esempio in WordPad, la proprietà **nome** per il controllo di modifica è "nome file:".                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è [**il \_ \_ testo del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ottenere \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti:[**stato sistema \_ \_ invisibile**](object-state-constants.md) stato sistema stato stato attivo sistema stato stato \| [**\_ \_ attivo**](object-state-constants.md) sistema \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |
| [**ottenere \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La proprietà **value** è una singola stringa che contiene il testo nel controllo di modifica. Tuttavia, se il controllo è protetto da password, la proprietà **value** restituisce E \_ AccessDenied. Per i controlli di modifica su più righe, la stringa contiene un ritorno a capo e un carattere di nuova riga alla fine di ogni riga.                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Note

-   Microsoft Active Accessibility non supporta la selezione del testo contenuto nei controlli Edit e Rich Edit perché il testo viene esposto come stringa nella proprietà **value** dell'oggetto.
-   Il controllo Rich Edit fornito da Riched20.dll (usato negli editor di testo, ad esempio WordPad in Windows 98), non invia WinEvents quando la posizione del punto di inserimento viene modificata durante la selezione del testo. Quando gli utenti preme MAIUSC e tasti di direzione per selezionare il testo, l'oggetto del cursore non attiva l' [**\_ oggetto evento \_ posizioneCambia**](event-constants.md) WinEvent. Quando la selezione viene impostata a livello di programmazione tramite messaggi Rich Edit, l'oggetto cursore non invia alcun evento per indicare la nuova posizione.

    Tutte le applicazioni che utilizzano Riched20.dll presentano questo problema. Le applicazioni che usano versioni precedenti del controllo Rich Edit inviano correttamente gli eventi in base alla selezione.

-   Il valore di **stato** per i controlli di modifica della password include sempre il sistema di stato del flag di bit [**\_ \_ protetto**](object-state-constants.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





