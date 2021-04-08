---
title: Per identificare gli input in base al numero
description: Per identificare gli input in base al numero
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- ASF (Advanced Systems Format), identificazione degli input per numero
- ASF (Advanced Systems Format), identificazione degli input per numero
- profili, identificazione degli input per numero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0629776eaaff4252a690c0e31cd6002f5de42b31
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046297"
---
# <a name="to-identify-inputs-by-number"></a><span data-ttu-id="4eda2-106">Per identificare gli input in base al numero</span><span class="sxs-lookup"><span data-stu-id="4eda2-106">To Identify Inputs By Number</span></span>

<span data-ttu-id="4eda2-107">Ogni esempio passato al writer deve essere associato a un numero di input.</span><span class="sxs-lookup"><span data-stu-id="4eda2-107">Every sample you pass to the writer must be associated with an input number.</span></span> <span data-ttu-id="4eda2-108">Ogni numero di input corrisponde a uno o più flussi nel profilo utilizzato dal writer per scrivere il file.</span><span class="sxs-lookup"><span data-stu-id="4eda2-108">Each input number corresponds to one or more streams in the profile that the writer is using to write the file.</span></span> <span data-ttu-id="4eda2-109">In un profilo, le origini multimediali sono identificate da un nome di connessione.</span><span class="sxs-lookup"><span data-stu-id="4eda2-109">In a profile, media sources are identified by a connection name.</span></span> <span data-ttu-id="4eda2-110">Quando si imposta il profilo per il writer, il writer associa un numero di input a ogni nome di connessione.</span><span class="sxs-lookup"><span data-stu-id="4eda2-110">The writer associates an input number with each connection name when you set the profile for the writer.</span></span> <span data-ttu-id="4eda2-111">Prima di poter passare i campioni al writer, è necessario determinare i dati previsti per ogni input.</span><span class="sxs-lookup"><span data-stu-id="4eda2-111">Before you can pass samples to the writer, you must determine what data each input is expecting.</span></span> <span data-ttu-id="4eda2-112">Non è possibile presupporre che gli input si trovino nello stesso ordine dei flussi in un profilo, anche se si tratta spesso del caso.</span><span class="sxs-lookup"><span data-stu-id="4eda2-112">You cannot assume that the inputs will be in the same order as the streams in a profile, even if this is often the case.</span></span> <span data-ttu-id="4eda2-113">Pertanto, l'unico modo affidabile per trovare la corrispondenza con gli input con i flussi consiste nel confrontare il nome della connessione dell'input con il nome della connessione del flusso.</span><span class="sxs-lookup"><span data-stu-id="4eda2-113">Therefore, the only reliable way to match inputs with streams is to compare the connection name of the input with the connection name of the stream.</span></span>

<span data-ttu-id="4eda2-114">Per identificare i nomi di connessione e i numeri di input corrispondenti per un profilo caricato, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="4eda2-114">To identify the connection names and corresponding input numbers for a loaded profile, perform the following steps:</span></span>

1.  <span data-ttu-id="4eda2-115">Creare un oggetto writer e impostare un profilo da usare.</span><span class="sxs-lookup"><span data-stu-id="4eda2-115">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="4eda2-116">Per ulteriori informazioni sull'impostazione dei profili nel writer, vedere [per utilizzare i profili con il writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="4eda2-116">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="4eda2-117">Si noteranno i nomi di connessione usati per i flussi nel profilo.</span><span class="sxs-lookup"><span data-stu-id="4eda2-117">You should know the connection names used for the streams in the profile.</span></span> <span data-ttu-id="4eda2-118">È possibile ottenere il nome della connessione dall'interno del profilo ottenendo l'oggetto di configurazione del flusso per ogni flusso e chiamando [**IWMStreamConfig:: Getconnectname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span><span class="sxs-lookup"><span data-stu-id="4eda2-118">You can get the connection name from within the profile by getting the stream configuration object for each stream and calling [**IWMStreamConfig::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span></span> <span data-ttu-id="4eda2-119">Per ulteriori informazioni sui profili e sugli oggetti di configurazione di flusso, vedere [utilizzo dei profili](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="4eda2-119">For more information about profiles and stream configuration objects, see [Working with Profiles](working-with-profiles.md).</span></span>
2.  <span data-ttu-id="4eda2-120">Recuperare il numero totale di input chiamando [**IWMWriter:: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span><span class="sxs-lookup"><span data-stu-id="4eda2-120">Retrieve the total number of inputs by calling [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span></span>
3.  <span data-ttu-id="4eda2-121">Scorrere tutti gli input, eseguendo i passaggi seguenti per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="4eda2-121">Loop through all of the inputs, performing the following steps for each.</span></span>
    -   <span data-ttu-id="4eda2-122">Recuperare l'interfaccia [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) per l'input chiamando [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="4eda2-122">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
    -   <span data-ttu-id="4eda2-123">Recuperare il nome della connessione che corrisponde al numero di input chiamando [**IWMInputMediaProps:: Getconnectname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span><span class="sxs-lookup"><span data-stu-id="4eda2-123">Retrieve the connection name that corresponds to the input number by calling [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span></span> <span data-ttu-id="4eda2-124">Dopo aver impostato il nome della connessione, si conoscono i flussi associati ai numeri di input assegnati dal writer.</span><span class="sxs-lookup"><span data-stu-id="4eda2-124">After you have the connection name, you know the streams that are associated with the input numbers assigned by the writer.</span></span>

<span data-ttu-id="4eda2-125">Nell'esempio di codice seguente viene visualizzato il nome della connessione per ogni input.</span><span class="sxs-lookup"><span data-stu-id="4eda2-125">The following example code displays the connection name for each input.</span></span> <span data-ttu-id="4eda2-126">Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="4eda2-126">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="4eda2-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4eda2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eda2-128">**Interfaccia IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="4eda2-128">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="4eda2-129">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="4eda2-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




