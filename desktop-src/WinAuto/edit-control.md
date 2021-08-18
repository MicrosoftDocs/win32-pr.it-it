---
title: Controllo Edit (Riferimento all'elemento DELL'interfaccia utente MSAA)
description: I controlli di modifica consentono a un utente di visualizzare e modificare il testo.
ms.assetid: a42c73f2-4005-4db9-84bc-637c9c4310f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3844dcdf99f925813765ae46494b0ff70345c086f3845304fff0e53d70f07d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829845"
---
# <a name="edit-control-msaa-ui-element-reference"></a>Controllo Edit (Riferimento all'elemento DELL'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **Edit Control** ai fini delle informazioni di riferimento sugli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti di controllo** di modifica in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento dell'API per il framework dell'interfaccia utente in uso.

 

I controlli di modifica consentono a un utente di visualizzare e modificare il testo. I controlli di modifica vengono creati con molti stili diversi, ad esempio ES \_ MULTILINE. Questo stile crea un controllo di modifica su più righe, ad esempio l'area client di Blocco note ed ES READONLY, che crea un controllo \_ di modifica di sola lettura.

Microsoft Active Accessibility non fa distinzione tra i controlli di modifica creati con il nome della classe della finestra "EDIT" e i controlli Rich Edit creati con il nome di classe della finestra "RichEdit" o "RichEdit20A".

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli di modifica supportano i [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli di modifica supportano le [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **proprietà KeyboardShortcut** è il tasto di scelta del controllo di modifica, ovvero un carattere sottolineato nel testo dell'etichetta del controllo di modifica. Ad esempio, in una finestra di dialogo apri file standard, ad esempio in WordPad, **KeyboardShortcut** per il controllo di modifica con etichetta "Filename:" è "ALT+n".                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** è il testo di un controllo di testo statico che etichetta il controllo di modifica. Ad esempio, in una finestra di dialogo apri file standard, ad esempio in WordPad, la proprietà **Nome** per il controllo di modifica è "Nome file:".                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **proprietà Parent** è una finestra ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra del controllo.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ TEXT.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md)[**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM FOCUSABLE STATE SYSTEM \_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**FOCUSABLE STATE SYSTEM \_ \_ READONLY**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ PROTECTED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ NORMAL**](object-state-constants.md)<br/> |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La **proprietà Value** è una singola stringa che contiene il testo nel controllo di modifica. Tuttavia, se il controllo è protetto da password, la **proprietà Value** restituisce E \_ ACCESSDENIED. Per i controlli di modifica su più righe, la stringa contiene un ritorno a capo e un carattere di nuova riga alla fine di ogni riga.                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Note

-   Microsoft Active Accessibility non supporta la selezione del testo contenuto nei controlli di modifica e rich edit perché il testo viene esposto come stringa nella proprietà **Value dell'oggetto.**
-   Il controllo Rich Edit fornito da Riched20.dll (usato in editor di testo come WordPad in Windows 98) non invia alcun WinEvent quando la posizione del cursore viene modificata durante la selezione del testo. Quando gli utenti premono MAIUSC e i tasti di direzione per selezionare il testo, l'oggetto cursore non attiva [**EVENT \_ OBJECT \_ LOCATIONCHANGE**](event-constants.md) WinEvent. Quando la selezione viene impostata a livello di codice tramite messaggi rich edit, l'oggetto cursore non invia alcun evento per indicare la nuova posizione.

    Tutte le applicazioni che usano Riched20.dll presentano questo problema. Le applicazioni che usano versioni precedenti del controllo Rich Edit inviano correttamente gli eventi in base alla selezione.

-   Il **valore State** per i controlli di modifica della password include sempre il flag di bit STATE SYSTEM [**\_ \_ PROTECTED.**](object-state-constants.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





