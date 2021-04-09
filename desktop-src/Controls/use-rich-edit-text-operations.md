---
title: Come usare le operazioni Rich Edit Text
description: Un'applicazione può inviare messaggi per recuperare o trovare testo in un controllo Rich Edit. È possibile recuperare il testo selezionato o un intervallo di testo specificato.
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b54619e1ce5952b7c0d06527c6aca2402a4e714
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963504"
---
# <a name="how-to-use-rich-edit-text-operations"></a>Come usare le operazioni Rich Edit Text

Un'applicazione può inviare messaggi per recuperare o trovare testo in un controllo Rich Edit. È possibile recuperare il testo selezionato o un intervallo di testo specificato.

Per ottenere il testo selezionato in un controllo Rich Edit, usare il [**messaggio \_ GETSELTEXT em**](em-getseltext.md) . Il testo viene copiato nella matrice di caratteri specificata. È necessario assicurarsi che la matrice sia sufficientemente grande da conservare il testo selezionato più un carattere di terminazione null.

Per recuperare un intervallo di testo specificato, utilizzare il [**messaggio \_ GETTEXTRANGE em**](em-gettextrange.md) . La struttura [**TextRange**](/windows/win32/api/richedit/ns-richedit-textrangea) utilizzata con questo messaggio specifica l'intervallo di testo da recuperare e punta a una matrice di caratteri che riceve il testo. Anche in questo caso, l'applicazione deve garantire che la matrice sia sufficientemente grande per il testo specificato più un carattere di terminazione null.

È possibile cercare una stringa in un controllo Rich Edit usando i messaggi [**em \_ FindText**](em-findtext.md) o [**em \_ FINDTEXTEX**](em-findtextex.md) o i rispettivi equivalenti Unicode [**em \_ FINDTEXTW**](em-findtextw.md) e [**em \_ FINDTEXTEXW**](em-findtextexw.md). La struttura [**FindText**](/windows/win32/api/richedit/ns-richedit-findtexta) usata con le versioni non estese specifica l'intervallo di testo da cercare e la stringa da cercare. Le versioni estese usano una struttura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , che specifica le stesse informazioni e riceve anche i punti di inizio e di fine dell'intervallo di caratteri del testo trovato. È anche possibile specificare tali opzioni, ad esempio se la ricerca fa distinzione tra maiuscole e minuscole.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-a-rich-edit-text-operation"></a>Usa un'operazione Rich Edit Text

La funzione di esempio seguente consente di trovare il testo specificato all'interno del testo selezionato in un controllo Rich Edit che supporta Unicode. Se la destinazione viene trovata, diventa la nuova selezione.


```C++
BOOL FindTextInSelection(HWND hRich, WCHAR* target)
{
    CHARRANGE selectionRange;
    
    SendMessage(hRich, EM_EXGETSEL, 0, (LPARAM)&selectionRange);
    
    FINDTEXTEX ftex;
    
    ftex.lpstrText  = target;
    ftex.chrg.cpMin = selectionRange.cpMin;
    ftex.chrg.cpMax = selectionRange.cpMax;
    
    LRESULT lr = SendMessage(hRich, EM_FINDTEXTEXW, (WPARAM)FR_DOWN, (LPARAM) &ftex);
    
    if (lr >= 0)
    {
        LRESULT lr1 = SendMessage(hRich, EM_EXSETSEL, 0, (LPARAM)&ftex.chrgText);
        
        SendMessage(hRich, EM_HIDESELECTION, (LPARAM)FALSE, 0);
        
        return TRUE;
    }
    
    return FALSE;
    
}
```



## <a name="remarks"></a>Commenti

Microsoft Rich Edit 3,0 supporta anche la funzione IME (Input Method Editor) HexToUnicode, che consente a un utente di eseguire la conversione tra esadecimali e Unicode usando i tasti di scelta rapida. Per ulteriori informazioni, vedere [HEXTOUNICODE IME](/windows/desktop/Intl/hextounicode-ime).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 