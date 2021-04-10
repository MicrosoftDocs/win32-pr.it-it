---
title: Come fornire controlli Rich Edit senza finestra con la funzionalità finestra
description: La funzionalità finestra include la possibilità di ricevere messaggi e la proprietà di un contesto di dispositivo in cui eseguire il progetto. I controlli Rich Edit senza finestra ricevono questa funzionalità per mezzo di una coppia di interfacce ITextServices e ITextHost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce987630c21b1e15a2237066b39dd264125a857
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103956283"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a><span data-ttu-id="436f0-104">Come fornire controlli Rich Edit senza finestra con la funzionalità finestra</span><span class="sxs-lookup"><span data-stu-id="436f0-104">How to Provide Windowless Rich Edit Controls with Window Functionality</span></span>

<span data-ttu-id="436f0-105">La funzionalità finestra include la possibilità di ricevere messaggi e la proprietà di un contesto di dispositivo in cui eseguire il progetto.</span><span class="sxs-lookup"><span data-stu-id="436f0-105">Window functionality includes the ability to receive messages and the ownership of a device context into which to draw.</span></span> <span data-ttu-id="436f0-106">I controlli Rich Edit senza finestra ricevono questa funzionalità per mezzo di una coppia di interfacce: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="436f0-106">Windowless rich edit controls receive this functionality by way of a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="436f0-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="436f0-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="436f0-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="436f0-108">Technologies</span></span>

-   [<span data-ttu-id="436f0-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="436f0-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="436f0-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="436f0-110">Prerequisites</span></span>

-   <span data-ttu-id="436f0-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="436f0-111">C/C++</span></span>
-   <span data-ttu-id="436f0-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="436f0-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="436f0-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="436f0-113">Instructions</span></span>

### <a name="establish-the-window-functionality"></a><span data-ttu-id="436f0-114">Definire la funzionalità della finestra</span><span class="sxs-lookup"><span data-stu-id="436f0-114">Establish the Window Functionality</span></span>

<span data-ttu-id="436f0-115">Nell'esempio di codice seguente viene illustrato come creare l'host di testo e i servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="436f0-115">The following example code demonstrates how to create the text host and text services.</span></span>


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a><span data-ttu-id="436f0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="436f0-116">Remarks</span></span>

<span data-ttu-id="436f0-117">Il parametro *hmodRichEdit* nell'esempio di codice è un handle per il modulo Msftedit.dll e si presuppone che questo handle sia già stato recuperato da una chiamata alla funzione **GetModuleHandle** .</span><span class="sxs-lookup"><span data-stu-id="436f0-117">The *hmodRichEdit* parameter in the code example is a handle to the Msftedit.dll module, and it is assumed that this handle has already been retrieved by a call to the **GetModuleHandle** function.</span></span>

## <a name="complete-example"></a><span data-ttu-id="436f0-118">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="436f0-118">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="436f0-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="436f0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="436f0-120">Uso di controlli Rich Edit senza finestra</span><span class="sxs-lookup"><span data-stu-id="436f0-120">Using Windowless Rich Edit Controls</span></span>](using-windowless-rich-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="436f0-121">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="436f0-121">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="436f0-122">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="436f0-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




