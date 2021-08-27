---
title: Come implementare descrizioni comando su più righe
description: Le descrizioni comando su più righe consentono la visualizzazione del testo su più righe.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0d9f4172b256d2e6b72fb59ace4dc377fa3a0061e3ee0e6c0f234a74aad06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085627"
---
# <a name="how-to-implement-multiline-tooltips"></a>Come implementare descrizioni comando su più righe

Le descrizioni comando su più righe consentono la visualizzazione del testo su più righe.

Sono supportati dalla [versione 4.70](common-control-versions.md) e successive dei controlli comuni. L'applicazione crea una descrizione comando su più righe inviando un [**messaggio \_ TTM SETMAXTIPWIDTH,**](ttm-setmaxtipwidth.md) specificando la larghezza del rettangolo di visualizzazione. Il testo che supera questa larghezza va a capo alla riga successiva invece di ampliare l'area di visualizzazione. L'altezza del rettangolo viene aumentata in base alle esigenze per contenere le linee aggiuntive. Il controllo descrizione comando esegue automaticamente il wrapping delle righe oppure è possibile usare una combinazione di ritorno a capo/avanzamento riga, r n, per forzare le interruzioni di riga \\ \\ in posizioni specifiche.

La visualizzazione risultante è illustrata nella figura seguente.

![Screenshot di una finestra di dialogo con una descrizione comando che contiene testo disposte come un paragrafo su più righe](images/tt-multiline.png)

> [!Note]  
> Il buffer di testo specificato dal **membro szText** della [**struttura NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) può contenere solo 80 caratteri. Se è necessario usare una stringa più lunga, puntare il membro **lpszText** di **NMTTDISPINFO** a un buffer contenente il testo desiderato.

 

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="implement-multiline-tooltips"></a>Implementare descrizioni comando su più righe

Il frammento di codice seguente è un esempio di un semplice gestore di notifica [ \_ GETDISPINFO TTN.](ttn-getdispinfo.md) Abilita una descrizione comando su più righe impostando il rettangolo di visualizzazione su 150 pixel. Un'interruzione di riga manuale viene inserita dopo la prima parola per mostrare che le interruzioni di riga possono essere dure e soft.


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

[Uso dei controlli descrizione comando](using-tooltip-contro.md)
</dt> </dl>

 

 




