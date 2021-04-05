---
title: Come usare i metodi di tabulazione in TOM
description: Nell'esempio seguente vengono fornite le funzioni C che illustrano l'utilizzo dei metodi di tabulazione nel modello a oggetti di testo (TOM).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9851b30fdf58c0d4200600c0c4c83c7f9a00a555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103872227"
---
# <a name="how-to-use-tab-methods-in-tom"></a><span data-ttu-id="38151-103">Come usare i metodi di tabulazione in TOM</span><span class="sxs-lookup"><span data-stu-id="38151-103">How to Use Tab Methods in TOM</span></span>

<span data-ttu-id="38151-104">Nell'esempio seguente vengono fornite le funzioni C che illustrano l'utilizzo dei metodi di tabulazione nel modello a oggetti di testo (TOM).</span><span class="sxs-lookup"><span data-stu-id="38151-104">The following example provides C functions that illustrate the use of the tab methods in the Text Object Model (TOM).</span></span> <span data-ttu-id="38151-105">Si presuppone che la maggior parte delle applicazioni includa una barra degli strumenti che mostra la posizione corrente e il tipo delle schede per il paragrafo attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="38151-105">It is assumed that most applications include a toolbar that shows the current position and type of the tabs for the currently selected paragraph.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="38151-106">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="38151-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="38151-107">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="38151-107">Technologies</span></span>

-   [<span data-ttu-id="38151-108">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="38151-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="38151-109">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="38151-109">Prerequisites</span></span>

-   <span data-ttu-id="38151-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="38151-110">C/C++</span></span>
-   <span data-ttu-id="38151-111">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="38151-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="38151-112">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="38151-112">Instructions</span></span>

### <a name="use-a-tab-method"></a><span data-ttu-id="38151-113">Usare un metodo Tab</span><span class="sxs-lookup"><span data-stu-id="38151-113">Use a Tab Method</span></span>

<span data-ttu-id="38151-114">Nell'esempio di codice riportato di seguito viene illustrato come aggiornare una barra degli strumenti con i dettagli della scheda corrente.</span><span class="sxs-lookup"><span data-stu-id="38151-114">The following code example demonstrates how to update a toolbar with the current tab details.</span></span>


```C++
HRESULT UpdateToolbar(ITextSelection *pSel)
{
    HRESULT hr       = S_OK;        
    ITextPara *pPara = 0;
    
    float f;
    long tbt;            // tab type
    long tbp;

    hr = pSel->GetPara(&pPara);
    
    if (FAILED(hr))
        goto cleanup;    // Paragraph properties are not supported
    
    f = (float) -1.0;    // Start at beginning
    
    while (pPara->GetTab(tbgoNext, &f, &tbt, NULL) == S_OK)
    {
            // Do something like draw tab icon on toolbar here
            // DrawTabPicture(f, tbt);
    }
    
cleanup:

    if (pPara)
        pPara->Release();
        
    return hr;
    
}
```



### <a name="copy-tab-information"></a><span data-ttu-id="38151-115">Copia informazioni scheda</span><span class="sxs-lookup"><span data-stu-id="38151-115">Copy Tab Information</span></span>

<span data-ttu-id="38151-116">Nell'esempio seguente viene illustrato come copiare solo le informazioni di tabulazione da un'interfaccia [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) a un'altra.</span><span class="sxs-lookup"><span data-stu-id="38151-116">The following example shows how to copy only the tab information from one [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) interface to another.</span></span> <span data-ttu-id="38151-117">Accetta due parametri: **ITextPara** \* *pParaFrom* (il paragrafo da cui copiare le schede) e **ITextPara** \* *pParaFrom* (il paragrafo in cui copiare le schede).</span><span class="sxs-lookup"><span data-stu-id="38151-117">It takes two parameters: **ITextPara** \* *pParaFrom* (the paragraph from which to copy tabs) and **ITextPara** \* *pParaFrom* (the paragraph to which to copy tabs).</span></span>


```C++
HRESULT CopyOnlyTabs(ITextPara *pParaFrom, ITextPara *pParaTo)
{
    float f;
    short tbt;
    short style;
     
    pParaTo->ClearAllTabs();
    
    f = (float) -1.0;
    
    while (pParaFrom->GetTab(tbgoNext, &f, &tbt, &style) == S_OK)
        pParaTo->AddTab(f, tbt, style);
        
    return S_OK;                
    
}
```



## <a name="related-topics"></a><span data-ttu-id="38151-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38151-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38151-119">Uso del modello a oggetti di testo</span><span class="sxs-lookup"><span data-stu-id="38151-119">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="38151-120">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="38151-120">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="38151-121">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="38151-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




