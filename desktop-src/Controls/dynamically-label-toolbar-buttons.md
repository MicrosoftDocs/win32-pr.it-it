---
title: Come etichettare dinamicamente i pulsanti della barra degli strumenti
description: È possibile assegnare testo a un pulsante esistente usando il messaggio TB \_ SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "104472427"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a><span data-ttu-id="794da-103">Come etichettare dinamicamente i pulsanti della barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="794da-103">How to Dynamically Label Toolbar Buttons</span></span>

<span data-ttu-id="794da-104">È possibile assegnare testo a un pulsante esistente usando il messaggio [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="794da-104">You can assign text to an existing button by using the [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="794da-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="794da-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="794da-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="794da-106">Technologies</span></span>

-   [<span data-ttu-id="794da-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="794da-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="794da-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="794da-108">Prerequisites</span></span>

-   <span data-ttu-id="794da-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="794da-109">C/C++</span></span>
-   <span data-ttu-id="794da-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="794da-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="794da-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="794da-111">Instructions</span></span>

### <a name="dynamically-label-a-toolbar-button"></a><span data-ttu-id="794da-112">Etichetta dinamicamente un pulsante della barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="794da-112">Dynamically Label a Toolbar Button</span></span>

<span data-ttu-id="794da-113">Nell'esempio seguente viene illustrato come modificare il testo del terzo pulsante degli esempi precedenti da **Save** in Salva con **nome**.</span><span class="sxs-lookup"><span data-stu-id="794da-113">The following example demonstrates how to change the text of the third button in the previous examples from **Save** to **Save As**.</span></span>


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a><span data-ttu-id="794da-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="794da-114">Remarks</span></span>

<span data-ttu-id="794da-115">La modifica del testo di un pulsante con [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) non influisce sulla stringa assegnata a tale pulsante nell'elenco di stringhe interno.</span><span class="sxs-lookup"><span data-stu-id="794da-115">Changing a button's text by using [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) does not affect the string that is assigned to that button in the internal string list.</span></span>

<span data-ttu-id="794da-116">Se si aggiunge una stringa del pulsante della barra degli strumenti all'elenco di testo interno, non è possibile recuperare l'indice di tale stringa chiamando [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md): è necessario usare invece il messaggio [**TB \_ GetButton**](tb-getbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="794da-116">If you add a toolbar button string to the internal text list, you cannot retrieve the index of that string by calling [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md)—you must use the [**TB\_GETBUTTON**](tb-getbutton.md) message instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="794da-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="794da-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="794da-118">Utilizzo di controlli Toolbar</span><span class="sxs-lookup"><span data-stu-id="794da-118">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="794da-119">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="794da-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




