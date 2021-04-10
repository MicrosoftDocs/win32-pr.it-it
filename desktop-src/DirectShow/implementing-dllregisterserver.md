---
description: Implementazione di DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implementazione di DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b994e80a181b69efffbe6123382957e7a38f8278
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125037"
---
# <a name="implementing-dllregisterserver"></a><span data-ttu-id="85078-103">Implementazione di DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="85078-103">Implementing DllRegisterServer</span></span>

<span data-ttu-id="85078-104">Il passaggio finale consiste nell'implementare la funzione **DllRegisterServer** .</span><span class="sxs-lookup"><span data-stu-id="85078-104">The final step is to implement the **DllRegisterServer** function.</span></span> <span data-ttu-id="85078-105">La DLL che contiene il componente deve esportare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="85078-105">The DLL that contains the component must export this function.</span></span> <span data-ttu-id="85078-106">La funzione verrà chiamata da un'applicazione di configurazione o quando l'utente esegue lo strumento Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="85078-106">The function will be called by a set-up application, or when the user runs the Regsvr32.exe tool.</span></span>

<span data-ttu-id="85078-107">Nell'esempio seguente viene illustrata un'implementazione minima di **DlLRegisterServer**:</span><span class="sxs-lookup"><span data-stu-id="85078-107">The following example shows a minimal implementation of **DlLRegisterServer**:</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



<span data-ttu-id="85078-108">La funzione [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) crea voci del registro di sistema per ogni componente nel</span><span class="sxs-lookup"><span data-stu-id="85078-108">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function creates registry entries for every component in the</span></span>


```
g_Templates
```



<span data-ttu-id="85078-109">matrice.</span><span class="sxs-lookup"><span data-stu-id="85078-109">array.</span></span> <span data-ttu-id="85078-110">Questa funzione presenta tuttavia alcune limitazioni.</span><span class="sxs-lookup"><span data-stu-id="85078-110">However, this function has some limitations.</span></span> <span data-ttu-id="85078-111">Innanzitutto, assegna tutti i filtri alla categoria "DirectShow Filters" (CLSID \_ LegacyAmFilterCategory), ma non tutti i filtri appartengono a questa categoria.</span><span class="sxs-lookup"><span data-stu-id="85078-111">First, it assigns every filter to the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory), but not every filter belongs in this category.</span></span> <span data-ttu-id="85078-112">I filtri di acquisizione e di compressione, ad esempio, hanno categorie personalizzate.</span><span class="sxs-lookup"><span data-stu-id="85078-112">Capture filters and compression filters, for example, have their own categories.</span></span> <span data-ttu-id="85078-113">In secondo luogo, se il filtro supporta un dispositivo hardware, potrebbe essere necessario registrare due informazioni aggiuntive non gestite da **AMovieDLLRegisterServer2** , ovvero la categoria *media* e *pin*.</span><span class="sxs-lookup"><span data-stu-id="85078-113">Second, if your filter supports a hardware device, you might need to register two additional pieces of information that **AMovieDLLRegisterServer2** does not handle: the *medium* and the *pin category*.</span></span> <span data-ttu-id="85078-114">Un supporto definisce un metodo di comunicazione in un dispositivo hardware, ad esempio un bus.</span><span class="sxs-lookup"><span data-stu-id="85078-114">A medium defines a method of communication in a hardware device, such as a bus.</span></span> <span data-ttu-id="85078-115">La categoria pin definisce la funzione di un PIN.</span><span class="sxs-lookup"><span data-stu-id="85078-115">The pin category defines the function of a pin.</span></span> <span data-ttu-id="85078-116">Per informazioni sui supporti, vedere "KSPIN \_ medium" in Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="85078-116">For information on mediums, see "KSPIN\_MEDIUM" in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="85078-117">Per un elenco di categorie di pin, vedere [impostare la proprietà pin](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="85078-117">For a list of pin categories, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="85078-118">Se si desidera specificare una categoria di filtro, un supporto o una categoria di pin, chiamare il metodo [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) dall'interno di **DllRegisterServer**.</span><span class="sxs-lookup"><span data-stu-id="85078-118">If you want to specify a filter category, a medium, or a pin category, call the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method from within **DllRegisterServer**.</span></span> <span data-ttu-id="85078-119">Questo metodo accetta un puntatore a una struttura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , che specifica le informazioni sul filtro.</span><span class="sxs-lookup"><span data-stu-id="85078-119">This method takes a pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure, which specifies information about the filter.</span></span>

<span data-ttu-id="85078-120">Per complicare un po' le cose, la struttura **REGFILTER2** supporta due formati diversi per la registrazione dei pin.</span><span class="sxs-lookup"><span data-stu-id="85078-120">To complicate matters somewhat, the **REGFILTER2** structure supports two different formats for registering pins.</span></span> <span data-ttu-id="85078-121">Il membro **dwVersion** specifica il formato:</span><span class="sxs-lookup"><span data-stu-id="85078-121">The **dwVersion** member specifies the format:</span></span>

-   <span data-ttu-id="85078-122">Se **dwVersion** è 1, il formato del PIN è **AMOVIESETUP \_ pin** (descritto in precedenza).</span><span class="sxs-lookup"><span data-stu-id="85078-122">If **dwVersion** is 1, the pin format is **AMOVIESETUP\_PIN** (described previously).</span></span>
-   <span data-ttu-id="85078-123">Se **dwVersion** è 2, il formato del PIN è [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span><span class="sxs-lookup"><span data-stu-id="85078-123">If **dwVersion** is 2, the pin format is [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span></span>

<span data-ttu-id="85078-124">La struttura **REGFILTERPINS2** include voci per supporti pin e categorie pin.</span><span class="sxs-lookup"><span data-stu-id="85078-124">The **REGFILTERPINS2** structure includes entries for pin mediums and pin categories.</span></span> <span data-ttu-id="85078-125">USA anche i flag di bit per alcuni elementi che **AMOVIESETUP \_ pin** dichiara come valori booleani.</span><span class="sxs-lookup"><span data-stu-id="85078-125">Also, it uses bit flags for some items that **AMOVIESETUP\_PIN** declares as Boolean values.</span></span>

<span data-ttu-id="85078-126">Nell'esempio seguente viene illustrato come chiamare **IFilterMapper2:: RegisterFilter** dall'interno di **DllRegisterServer**:</span><span class="sxs-lookup"><span data-stu-id="85078-126">The following example shows how to call **IFilterMapper2::RegisterFilter** from inside **DllRegisterServer**:</span></span>


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 



