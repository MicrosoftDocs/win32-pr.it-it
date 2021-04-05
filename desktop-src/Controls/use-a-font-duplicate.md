---
title: Come usare un duplicato del tipo di carattere
description: In questa sezione viene illustrato come utilizzare un duplicato del tipo di carattere per applicare una serie di modifiche a un intervallo di testo, in una sola volta.
ms.assetid: CF0123E5-313F-4583-872F-6FE954F1C9E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dce0481b59fe9955b93a00b2c0d703c5c695ef
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103956288"
---
# <a name="how-to-use-a-font-duplicate"></a><span data-ttu-id="26152-103">Come usare un duplicato del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="26152-103">How to Use a Font Duplicate</span></span>

<span data-ttu-id="26152-104">In questa sezione viene illustrato come utilizzare un duplicato del tipo di carattere per applicare una serie di modifiche a un intervallo di testo, in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="26152-104">This section explains how to use a font duplicate to apply a number of changes to a text range, all at once.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="26152-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="26152-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="26152-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="26152-106">Technologies</span></span>

-   [<span data-ttu-id="26152-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="26152-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="26152-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="26152-108">Prerequisites</span></span>

-   <span data-ttu-id="26152-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="26152-109">C/C++</span></span>
-   <span data-ttu-id="26152-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="26152-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="26152-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="26152-111">Instructions</span></span>

### <a name="use-a-font-duplicate"></a><span data-ttu-id="26152-112">Usa un duplicato del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="26152-112">Use a Font Duplicate</span></span>

<span data-ttu-id="26152-113">Nell'esempio seguente viene illustrato come è possibile utilizzare un duplicato del tipo di carattere per applicare una serie di modifiche a un intervallo in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="26152-113">The following example shows how a font duplicate can be used to apply a number of changes to a range at once.</span></span>


```C++
void ChangeFontNameSizeBold(ITextSelection *pSel)
{
    ITextFont *pFontSel      = NULL
    ITextFont *FontDuplicate = NULL;
    
    // Get ITextFont version of non-duplicated font.
    if (FAILED(pSel->GetFont( &pFontSel))
        return;

    // Duplicate the font.
    pFontSel->GetValue(&pFontDuplicate);
    pFontSel->Release();
    
    if(!pFontDuplicate)
        return;

   // Changes here happen only to the underlying data structure, 
   // such as a CHARFORMAT, in the duplicate - NOT to the actual story text.

    BSTR bstrTemp = UnicodeBstrFromAnsi("Times New Roman");   // Font name
    
    pFontDuplicate->SetName(bstrTemp);
    SysFreeString(bstrTemp);
    
    pFontDuplicate->SetBold(tomTrue);                        // Bold
    pFontDuplicate->SetSize(10.5);                           // 10.5 point font.
    pFontDuplicate->SetAnimation(tomBlackMarchingAnts);

    // Apply the change to text as one change: one screen update, one undo. 
    // You can also apply the font object to different ranges before you free it.
    
    pSel->SetFont(pFontDuplicate);
    
    pFontDuplicate->Release();
    
}
```



## <a name="related-topics"></a><span data-ttu-id="26152-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26152-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26152-115">Uso del modello a oggetti di testo</span><span class="sxs-lookup"><span data-stu-id="26152-115">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="26152-116">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="26152-116">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="26152-117">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="26152-117">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




