---
description: Per ottenere un controllo più dettagliato sul comportamento di completamento automatico o per aggiungere un'origine personalizzata di stringhe di completamento automatico, è necessario gestire manualmente l'oggetto di completamento automatico.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Come abilitare il completamento automatico manualmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979570"
---
# <a name="how-to-enable-autocomplete-manually"></a><span data-ttu-id="6b409-103">Come abilitare il completamento automatico manualmente</span><span class="sxs-lookup"><span data-stu-id="6b409-103">How to Enable Autocomplete Manually</span></span>

<span data-ttu-id="6b409-104">Per ottenere un controllo più dettagliato sul comportamento di completamento automatico o per aggiungere un'origine personalizzata di stringhe di completamento automatico, è necessario gestire manualmente l'oggetto di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-104">To gain more detailed control over the autocomplete behavior, or to add a custom source of autocomplete strings, you must manage the autocomplete object yourself.</span></span> <span data-ttu-id="6b409-105">È possibile abilitare il completamento automatico manualmente nei modi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6b409-105">You can enable autocomplete manually in the following ways.</span></span>

## <a name="instructions"></a><span data-ttu-id="6b409-106">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="6b409-106">Instructions</span></span>

### <a name="creating-a-simple-autocomplete-object"></a><span data-ttu-id="6b409-107">Creazione di un oggetto di completamento automatico semplice</span><span class="sxs-lookup"><span data-stu-id="6b409-107">Creating a Simple Autocomplete Object</span></span>

<span data-ttu-id="6b409-108">Nei passaggi seguenti viene illustrato come creare e inizializzare un semplice oggetto di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-108">The following steps show how to create and initialize a simple autocomplete object.</span></span> <span data-ttu-id="6b409-109">Un oggetto di completamento automatico semplice completa le stringhe da un'unica origine.</span><span class="sxs-lookup"><span data-stu-id="6b409-109">A simple autocomplete object completes strings from a single source.</span></span> <span data-ttu-id="6b409-110">Il controllo degli errori è stato intenzionalmente omesso in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="6b409-110">Error checking has been intentionally omitted in this example.</span></span>

1.  <span data-ttu-id="6b409-111">Creare l'oggetto di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-111">Create the autocomplete object.</span></span>

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  <span data-ttu-id="6b409-112">Creare l'origine di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-112">Create the autocomplete source.</span></span> <span data-ttu-id="6b409-113">È possibile usare un' [origine di completamento automatico predefinita](ac-ovw.md) oppure è possibile scrivere un'origine personalizzata.</span><span class="sxs-lookup"><span data-stu-id="6b409-113">You can use a [predefined autocomplete source](ac-ovw.md) or you can write your own custom source.</span></span>

    <span data-ttu-id="6b409-114">Nel codice seguente viene utilizzata una delle origini di completamento automatico predefinite.</span><span class="sxs-lookup"><span data-stu-id="6b409-114">The following code uses one of the predefined autocomplete sources.</span></span>

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    <span data-ttu-id="6b409-115">Il codice seguente usa un'origine di completamento automatico personalizzata.</span><span class="sxs-lookup"><span data-stu-id="6b409-115">The following code uses a custom autocomplete source.</span></span> <span data-ttu-id="6b409-116">È possibile scrivere un'origine di completamento automatico personalizzata implementando un oggetto che espone l'interfaccia [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) .</span><span class="sxs-lookup"><span data-stu-id="6b409-116">You can write your own autocomplete source by implementing an object that exposes the [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) interface.</span></span> <span data-ttu-id="6b409-117">L'oggetto può inoltre implementare facoltativamente le interfacce [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) e [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .</span><span class="sxs-lookup"><span data-stu-id="6b409-117">The object can also optionally implement the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) and [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interfaces.</span></span>

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  <span data-ttu-id="6b409-118">Impostare le opzioni nell'origine completamento automatico (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="6b409-118">Set the options on the autocomplete source (optional).</span></span>

    <span data-ttu-id="6b409-119">È possibile personalizzare il comportamento dell'origine AutoComplete impostando le opzioni se l'origine espone l'interfaccia [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .</span><span class="sxs-lookup"><span data-stu-id="6b409-119">You can customize the behavior of the autocomplete source by setting its options if the source exposes the [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interface.</span></span> <span data-ttu-id="6b409-120">Quando si usano le origini di completamento automatico predefinite, solo CLSID \_ ACListISF Esporta **IACList2**.</span><span class="sxs-lookup"><span data-stu-id="6b409-120">When using the predefined autocomplete sources, only CLSID\_ACListISF exports **IACList2**.</span></span> <span data-ttu-id="6b409-121">Per un elenco completo delle opzioni e dei relativi valori, vedere [**IACList2:: SetOption**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="6b409-121">For a complete list of options and their values, see [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  <span data-ttu-id="6b409-122">Inizializzare l'oggetto di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-122">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="6b409-123">In questo esempio, **hwndEdit** è l'handle della finestra di controllo di modifica per la quale è necessario abilitare la funzionalità di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-123">In this example, **hwndEdit** is the handle of the edit control window for which autocomplete is to be enabled.</span></span> <span data-ttu-id="6b409-124">Per una descrizione degli ultimi due parametri inutilizzati, vedere [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) .</span><span class="sxs-lookup"><span data-stu-id="6b409-124">See [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) for a description of the final two unused parameters.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  <span data-ttu-id="6b409-125">Impostare le opzioni dell'oggetto di completamento automatico (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="6b409-125">Set the options of the autocomplete object (optional).</span></span>

    <span data-ttu-id="6b409-126">È possibile personalizzare il comportamento dell'oggetto di completamento automatico impostando le relative opzioni.</span><span class="sxs-lookup"><span data-stu-id="6b409-126">You can customize the behavior of the autocomplete object by setting its options.</span></span> <span data-ttu-id="6b409-127">Per un elenco completo delle opzioni e dei relativi valori, vedere la documentazione di [**IACList2:: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="6b409-127">For a complete list of options and their values, see the documentation for [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  <span data-ttu-id="6b409-128">Rilasciare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="6b409-128">Release the objects.</span></span>

    > [!Note]  
    > <span data-ttu-id="6b409-129">L'oggetto di completamento automatico rimane collegato al controllo di modifica anche dopo che è stato rilasciato.</span><span class="sxs-lookup"><span data-stu-id="6b409-129">The autocomplete object remains attached to the edit control even after you release it.</span></span> <span data-ttu-id="6b409-130">Se si prevede di dover accedere successivamente a questi oggetti, se si desidera modificare le opzioni di completamento automatico in un secondo momento, ad esempio, non è necessario rilasciarle a questo punto.</span><span class="sxs-lookup"><span data-stu-id="6b409-130">If you foresee a need to access these objects later—if you want to change the autocomplete options at a later time, for example—it is not required that you release them at this point.</span></span>

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a><span data-ttu-id="6b409-131">Creazione di un oggetto di completamento automatico composto</span><span class="sxs-lookup"><span data-stu-id="6b409-131">Creating a Compound Autocomplete Object</span></span>

<span data-ttu-id="6b409-132">Un oggetto di completamento automatico composto corrisponde a stringhe da più origini.</span><span class="sxs-lookup"><span data-stu-id="6b409-132">A compound autocomplete object matches against strings from multiple sources.</span></span> <span data-ttu-id="6b409-133">La barra degli indirizzi di Windows Internet Explorer, ad esempio, utilizza un oggetto di completamento automatico composto perché l'utente potrebbe iniziare a digitare il nome di un file o un URL.</span><span class="sxs-lookup"><span data-stu-id="6b409-133">For example, the Windows Internet Explorer Address bar uses a compound autocomplete object because the user might begin typing the name of a file or a URL.</span></span> <span data-ttu-id="6b409-134">La maggior parte dei passaggi necessari per la creazione di un oggetto di completamento automatico composto è identica a quella descritta in "creazione di un oggetto di completamento automatico semplice".</span><span class="sxs-lookup"><span data-stu-id="6b409-134">Most of the steps involved in creating a compound autocomplete object are identical to the steps in "Creating a Simple Autocomplete Object."</span></span> <span data-ttu-id="6b409-135">Questi passaggi sono indicati come tali.</span><span class="sxs-lookup"><span data-stu-id="6b409-135">Those steps are indicated as such.</span></span>

1.  <span data-ttu-id="6b409-136">Creare l'oggetto di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-136">Create the autocomplete object.</span></span> <span data-ttu-id="6b409-137">Corrisponde al passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="6b409-137">This is the same as step 1 above.</span></span>

2.  <span data-ttu-id="6b409-138">Creare il gestore dell'oggetto di origine composto di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-138">Create the autocomplete compound source object manager.</span></span>

    <span data-ttu-id="6b409-139">L'oggetto di origine composto di completamento automatico consente di combinare più origini di completamento automatico in un'unica origine di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-139">The autocomplete compound source object allows multiple autocomplete sources to be combined into a single autocomplete source.</span></span>

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  <span data-ttu-id="6b409-140">Creare e impostare le opzioni per ognuna delle origini di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-140">Create and set options for each of the autocomplete sources.</span></span> <span data-ttu-id="6b409-141">Ripetere i passaggi 2 e 3 sopra per ogni origine.</span><span class="sxs-lookup"><span data-stu-id="6b409-141">Repeat steps 2 and 3 above for each source.</span></span>

4.  <span data-ttu-id="6b409-142">Alleghi ogni origine di completamento automatico a gestione oggetti di origine.</span><span class="sxs-lookup"><span data-stu-id="6b409-142">Attach each autocomplete source to the source object manager.</span></span>

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  <span data-ttu-id="6b409-143">Inizializzare l'oggetto di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-143">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="6b409-144">Questo è lo stesso del passaggio 4 precedente, ad eccezione del fatto che anziché passare la semplice origine di completamento automatico a [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), si passa il gestore oggetti di origine composto.</span><span class="sxs-lookup"><span data-stu-id="6b409-144">This is the same as step 4 above, except that instead of passing the simple autocomplete source to [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), you pass the compound source object manager.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  <span data-ttu-id="6b409-145">Impostare le opzioni dell'oggetto di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="6b409-145">Set the options of the autocomplete object.</span></span> <span data-ttu-id="6b409-146">Questo è lo stesso del passaggio 5 riportato sopra.</span><span class="sxs-lookup"><span data-stu-id="6b409-146">This is the same as step 5 above.</span></span>

7.  <span data-ttu-id="6b409-147">Rilasciare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="6b409-147">Release the objects.</span></span>

    <span data-ttu-id="6b409-148">Come nel caso più semplice, è possibile rilasciare gli oggetti non appena ne è stata completata l'uso, ma è possibile conservarli anche per modificare le opzioni in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="6b409-148">As in the simple case, you can release the objects as soon as you are finished using them, but you can also retain them to change options later.</span></span>

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
