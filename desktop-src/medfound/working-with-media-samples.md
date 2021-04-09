---
description: Utilizzo degli esempi di supporti
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: Utilizzo degli esempi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968856"
---
# <a name="working-with-media-samples"></a><span data-ttu-id="db95a-103">Utilizzo degli esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="db95a-103">Working with Media Samples</span></span>

<span data-ttu-id="db95a-104">In questo argomento viene descritto come utilizzare l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) per modificare gli oggetti di esempio multimediali.</span><span class="sxs-lookup"><span data-stu-id="db95a-104">This topic describes how to use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to manipulate media sample objects.</span></span> <span data-ttu-id="db95a-105">Per una panoramica generale degli esempi di supporti, vedere [esempi di supporti](media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="db95a-105">For a general overview of media samples, see [Media Samples](media-samples.md).</span></span>

<span data-ttu-id="db95a-106">Per creare un nuovo esempio di supporto, chiamare la funzione [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) .</span><span class="sxs-lookup"><span data-stu-id="db95a-106">To create a new media sample, call the [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) function.</span></span> <span data-ttu-id="db95a-107">Inizialmente, l'elenco di buffer dell'esempio è vuoto.</span><span class="sxs-lookup"><span data-stu-id="db95a-107">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="db95a-108">Per aggiungere un buffer alla fine dell'elenco, chiamare [**IMFSample:: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span><span class="sxs-lookup"><span data-stu-id="db95a-108">To add a buffer to the end of the list, call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="db95a-109">Il codice seguente illustra come creare un esempio e aggiungervi un buffer.</span><span class="sxs-lookup"><span data-stu-id="db95a-109">The following code shows how to create a sample and add a buffer to it.</span></span>


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="db95a-110">Il metodo consigliato per ottenere i buffer dall'esempio consiste nel chiamare [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span><span class="sxs-lookup"><span data-stu-id="db95a-110">The recommended way to get the buffers from the sample is to call [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span></span> <span data-ttu-id="db95a-111">Questo metodo restituisce un singolo buffer Continguous.</span><span class="sxs-lookup"><span data-stu-id="db95a-111">This method returns a single continguous buffer.</span></span>

<span data-ttu-id="db95a-112">Per scorrere i buffer nell'elenco, iniziare chiamando [**IMFSample:: GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span><span class="sxs-lookup"><span data-stu-id="db95a-112">To iterate through the buffers in the list, start by calling [**IMFSample::GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span></span> <span data-ttu-id="db95a-113">Questo metodo restituisce il numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="db95a-113">This method returns the number of buffers.</span></span> <span data-ttu-id="db95a-114">Chiamare quindi [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) e specificare l'indice del buffer da recuperare.</span><span class="sxs-lookup"><span data-stu-id="db95a-114">Then call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) and specify the index of the buffer to retrieve.</span></span> <span data-ttu-id="db95a-115">I buffer sono indicizzati da zero.</span><span class="sxs-lookup"><span data-stu-id="db95a-115">Buffers are indexed from zero.</span></span>

<span data-ttu-id="db95a-116">Nel codice seguente viene illustrato come scorrere i buffer in un esempio.</span><span class="sxs-lookup"><span data-stu-id="db95a-116">The following code shows how to iterate through the buffers in a sample.</span></span>


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



<span data-ttu-id="db95a-117">Gli esempi hanno un timestamp e una durata.</span><span class="sxs-lookup"><span data-stu-id="db95a-117">Samples have a time stamp and a duration.</span></span> <span data-ttu-id="db95a-118">Il timestamp indica quando deve essere eseguito il rendering dei dati nell'esempio rispetto al clock di presentazione.</span><span class="sxs-lookup"><span data-stu-id="db95a-118">The time stamp indicates when the data in the sample should be rendered, relative to the presentation clock.</span></span> <span data-ttu-id="db95a-119">La durata è l'intervallo di tempo per cui è necessario eseguire il rendering dei dati.</span><span class="sxs-lookup"><span data-stu-id="db95a-119">The duration is the length of time for which the data should be rendered.</span></span> <span data-ttu-id="db95a-120">In genere, il componente che genera i dati imposta il timestamp e la durata iniziali.</span><span class="sxs-lookup"><span data-stu-id="db95a-120">Typically the component that generates the data sets the initial time stamp and duration.</span></span> <span data-ttu-id="db95a-121">Questi valori potrebbero essere modificati dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="db95a-121">These values might get modified by the Media Session.</span></span> <span data-ttu-id="db95a-122">Per impostare il timestamp, chiamare [**IMFSample:: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span><span class="sxs-lookup"><span data-stu-id="db95a-122">To set the time stamp, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="db95a-123">Per impostare la durata, chiamare [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span><span class="sxs-lookup"><span data-stu-id="db95a-123">To set the duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="db95a-124">Gli esempi possono includere anche attributi, che contengono informazioni aggiuntive sull'esempio.</span><span class="sxs-lookup"><span data-stu-id="db95a-124">Samples can also have attributes, which contain additional information about the sample.</span></span> <span data-ttu-id="db95a-125">Per un elenco di attributi di esempio, vedere [esempi di attributi](sample-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="db95a-125">For a list of sample attributes, see [Sample Attributes](sample-attributes.md).</span></span> <span data-ttu-id="db95a-126">Per impostare e recuperare gli attributi, usare l' [**interfaccia IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), che eredita da [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="db95a-126">To set and retrieve attributes, use the [**IMFAttributes Interface**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) inherits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db95a-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db95a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db95a-128">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="db95a-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="db95a-129">Buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="db95a-129">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



