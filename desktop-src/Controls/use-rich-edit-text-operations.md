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
# <a name="how-to-use-rich-edit-text-operations"></a><span data-ttu-id="f0b9a-104">Come usare le operazioni Rich Edit Text</span><span class="sxs-lookup"><span data-stu-id="f0b9a-104">How to Use Rich Edit Text Operations</span></span>

<span data-ttu-id="f0b9a-105">Un'applicazione può inviare messaggi per recuperare o trovare testo in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-105">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="f0b9a-106">È possibile recuperare il testo selezionato o un intervallo di testo specificato.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-106">You can retrieve either the selected text or a specified range of text.</span></span>

<span data-ttu-id="f0b9a-107">Per ottenere il testo selezionato in un controllo Rich Edit, usare il [**messaggio \_ GETSELTEXT em**](em-getseltext.md) .</span><span class="sxs-lookup"><span data-stu-id="f0b9a-107">To get the selected text in a rich edit control, use the [**EM\_GETSELTEXT**](em-getseltext.md) message.</span></span> <span data-ttu-id="f0b9a-108">Il testo viene copiato nella matrice di caratteri specificata.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-108">The text is copied to the specified character array.</span></span> <span data-ttu-id="f0b9a-109">È necessario assicurarsi che la matrice sia sufficientemente grande da conservare il testo selezionato più un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-109">You must ensure that the array is large enough to hold the selected text plus a terminating null character.</span></span>

<span data-ttu-id="f0b9a-110">Per recuperare un intervallo di testo specificato, utilizzare il [**messaggio \_ GETTEXTRANGE em**](em-gettextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="f0b9a-110">To retrieve a specified range of text, use the [**EM\_GETTEXTRANGE**](em-gettextrange.md) message.</span></span> <span data-ttu-id="f0b9a-111">La struttura [**TextRange**](/windows/win32/api/richedit/ns-richedit-textrangea) utilizzata con questo messaggio specifica l'intervallo di testo da recuperare e punta a una matrice di caratteri che riceve il testo.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-111">The [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure used with this message specifies the text range to retrieve and points to a character array that receives the text.</span></span> <span data-ttu-id="f0b9a-112">Anche in questo caso, l'applicazione deve garantire che la matrice sia sufficientemente grande per il testo specificato più un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-112">Here again, the application must ensure that the array is large enough for the specified text plus a terminating null character.</span></span>

<span data-ttu-id="f0b9a-113">È possibile cercare una stringa in un controllo Rich Edit usando i messaggi [**em \_ FindText**](em-findtext.md) o [**em \_ FINDTEXTEX**](em-findtextex.md) o i rispettivi equivalenti Unicode [**em \_ FINDTEXTW**](em-findtextw.md) e [**em \_ FINDTEXTEXW**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="f0b9a-113">You can search for a string in a rich edit control by using the [**EM\_FINDTEXT**](em-findtext.md) or [**EM\_FINDTEXTEX**](em-findtextex.md) messages, or their Unicode equivalents, [**EM\_FINDTEXTW**](em-findtextw.md) and [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span> <span data-ttu-id="f0b9a-114">La struttura [**FindText**](/windows/win32/api/richedit/ns-richedit-findtexta) usata con le versioni non estese specifica l'intervallo di testo da cercare e la stringa da cercare.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-114">The [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure that is used with the nonextended versions specifies the text range to search and the string to search for.</span></span> <span data-ttu-id="f0b9a-115">Le versioni estese usano una struttura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , che specifica le stesse informazioni e riceve anche i punti di inizio e di fine dell'intervallo di caratteri del testo trovato.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-115">The extended versions use a [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, which specifies the same information and also receives the start and end points of the character range of the found text.</span></span> <span data-ttu-id="f0b9a-116">È anche possibile specificare tali opzioni, ad esempio se la ricerca fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-116">You can also specify such options as whether the search is case sensitive.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f0b9a-117">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="f0b9a-117">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f0b9a-118">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="f0b9a-118">Technologies</span></span>

-   [<span data-ttu-id="f0b9a-119">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="f0b9a-119">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f0b9a-120">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="f0b9a-120">Prerequisites</span></span>

-   <span data-ttu-id="f0b9a-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="f0b9a-121">C/C++</span></span>
-   <span data-ttu-id="f0b9a-122">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="f0b9a-122">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f0b9a-123">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="f0b9a-123">Instructions</span></span>

### <a name="use-a-rich-edit-text-operation"></a><span data-ttu-id="f0b9a-124">Usa un'operazione Rich Edit Text</span><span class="sxs-lookup"><span data-stu-id="f0b9a-124">Use a Rich Edit Text Operation</span></span>

<span data-ttu-id="f0b9a-125">La funzione di esempio seguente consente di trovare il testo specificato all'interno del testo selezionato in un controllo Rich Edit che supporta Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-125">The following example function finds the specified text within the selected text in a rich edit control that supports Unicode.</span></span> <span data-ttu-id="f0b9a-126">Se la destinazione viene trovata, diventa la nuova selezione.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-126">If the target is found, it becomes the new selection.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="f0b9a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0b9a-127">Remarks</span></span>

<span data-ttu-id="f0b9a-128">Microsoft Rich Edit 3,0 supporta anche la funzione IME (Input Method Editor) HexToUnicode, che consente a un utente di eseguire la conversione tra esadecimali e Unicode usando i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="f0b9a-128">Microsoft Rich Edit 3.0 also supports the HexToUnicode Input Method Editor (IME) function, which allows a user to convert between hexadecimal and Unicode by using hot keys.</span></span> <span data-ttu-id="f0b9a-129">Per ulteriori informazioni, vedere [HEXTOUNICODE IME](/windows/desktop/Intl/hextounicode-ime).</span><span class="sxs-lookup"><span data-stu-id="f0b9a-129">For more information, see [HexToUnicode IME](/windows/desktop/Intl/hextounicode-ime).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0b9a-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0b9a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0b9a-131">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="f0b9a-131">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="f0b9a-132">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="f0b9a-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 