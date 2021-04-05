---
title: Come implementare descrizioni comandi su più righe
description: Le descrizioni comando su più righe consentono di visualizzare il testo su più di una riga.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d6f32d638b2d33ea6270aa5f8ce2c09f0f4174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708662"
---
# <a name="how-to-implement-multiline-tooltips"></a>Come implementare descrizioni comandi su più righe

Le descrizioni comando su più righe consentono di visualizzare il testo su più di una riga.

Sono supportati dalla [versione 4,70](common-control-versions.md) e successive dei controlli comuni. L'applicazione crea una descrizione comando su più righe inviando un messaggio [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) , specificando la larghezza del rettangolo di visualizzazione. Il testo che supera questa larghezza va a capo alla riga successiva anziché ampliare l'area di visualizzazione. L'altezza del rettangolo viene aumentata in base alle esigenze per contenere le righe aggiuntive. Il controllo ToolTip esegue automaticamente il wrapping delle righe, oppure è possibile usare una combinazione di ritorno a capo/avanzamento riga, \\ r \\ n, per forzare le interruzioni di riga in posizioni particolari.

La visualizzazione risultante è illustrata nella figura seguente.

![Screenshot di una finestra di dialogo con una descrizione comando contenente testo disposto come un paragrafo a più righe](images/tt-multiline.png)

> [!Note]  
> Il buffer di testo specificato dal membro **szText** della struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) può contenere solo 80 caratteri. Se è necessario usare una stringa più lunga, puntare il membro **lpszText** di **NMTTDISPINFO** a un buffer contenente il testo desiderato.

 

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="implement-multiline-tooltips"></a>Implementare descrizioni comandi su più righe

Il frammento di codice seguente è un esempio di un semplice gestore di notifiche [ \_ GETDISPINFO TTN](ttn-getdispinfo.md) . Abilita una descrizione comando su più righe impostando il rettangolo di visualizzazione su 150 pixel. Viene inserita un'interruzione di riga manuale dopo la prima parola per mostrare che le interruzioni di riga possono essere rigide e morbide.


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 




