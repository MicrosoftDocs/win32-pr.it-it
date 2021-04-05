---
title: Dati di input e di output
description: Dati di input e di output
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Plug-in di Windows Media Player, input e output dei dati
- plug-in, input e output dei dati
- plug-in per l'elaborazione di segnali digitali, input e output dei dati
- Plug-in DSP, input e output dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116837"
---
# <a name="data-input-and-output"></a><span data-ttu-id="fcebe-107">Dati di input e di output</span><span class="sxs-lookup"><span data-stu-id="fcebe-107">Data Input and Output</span></span>

<span data-ttu-id="fcebe-108">Windows Media Player fornisce dati audio o video a plug-in DSP tramite un buffer di input allocato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fcebe-108">Windows Media Player provides audio or video data to DSP plug-ins through an input buffer allocated by Windows Media Player.</span></span> <span data-ttu-id="fcebe-109">I plug-in DSP restituiscono i dati elaborati a Windows Media Player tramite un buffer di output anch ' esso allocato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fcebe-109">DSP plug-ins return processed data to Windows Media Player through an output buffer that is also allocated by Windows Media Player.</span></span> <span data-ttu-id="fcebe-110">Windows Media Player gestisce il processo di passaggio dei dati tra se stesso e il plug-in DSP chiamando i metodi implementati dal plug-in.</span><span class="sxs-lookup"><span data-stu-id="fcebe-110">Windows Media Player manages the process of passing data between itself and the DSP plug-in by calling methods implemented by the plug-in.</span></span> <span data-ttu-id="fcebe-111">Per un plug-in che agisce come DMO (DirectX Media Object), il processo funziona nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="fcebe-111">For a plug-in acting as a DirectX Media Object (DMO), the process works as follows:</span></span>

1.  <span data-ttu-id="fcebe-112">Windows Media Player chiama **IMediaObject::P rocessinput**, passando un puntatore a un oggetto **IMediaBuffer** al plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="fcebe-112">Windows Media Player calls **IMediaObject::ProcessInput**, passing a pointer to an **IMediaBuffer** object to the DSP plug-in.</span></span>
2.  <span data-ttu-id="fcebe-113">Il plug-in DSP mantiene un conteggio dei riferimenti nell'oggetto buffer di input.</span><span class="sxs-lookup"><span data-stu-id="fcebe-113">The DSP plug-in keeps a reference count on the input buffer object.</span></span> <span data-ttu-id="fcebe-114">Il plug-in DSP restituisce un **HRESULT** di esito positivo o negativo appropriato.</span><span class="sxs-lookup"><span data-stu-id="fcebe-114">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
3.  <span data-ttu-id="fcebe-115">Windows Media Player chiama **IMediaObject::P rocessoutput**, passando un puntatore a una matrice di strutture del **\_ \_ \_ buffer dei dati di output DMO** , che contengono buffer di output, al plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="fcebe-115">Windows Media Player calls **IMediaObject::ProcessOutput**, passing a pointer to an array of **DMO\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
4.  <span data-ttu-id="fcebe-116">Il plug-in DSP elabora i dati nel buffer di input e quindi copia i dati nel buffer di output appropriato.</span><span class="sxs-lookup"><span data-stu-id="fcebe-116">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="fcebe-117">Il plug-in DSP rilascia il conteggio dei riferimenti nell'oggetto buffer di input quando tutti i dati nel buffer sono stati elaborati.</span><span class="sxs-lookup"><span data-stu-id="fcebe-117">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="fcebe-118">Il plug-in DSP restituisce quindi un **HRESULT** di esito positivo o negativo appropriato.</span><span class="sxs-lookup"><span data-stu-id="fcebe-118">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
5.  <span data-ttu-id="fcebe-119">Windows Media Player esegue il rendering del contenuto nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="fcebe-119">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="fcebe-120">Per un plug-in che agisce come una trasformazione Media Foundation (MFT), il processo funziona nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="fcebe-120">For a plug-in acting as a Media Foundation Transform (MFT), the process works as follows:</span></span>

-   <span data-ttu-id="fcebe-121">Windows Media Player chiama **IMFTransform::P rocessinput**, passando un puntatore a un oggetto di interfaccia **IMFSample** al plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="fcebe-121">Windows Media Player calls **IMFTransform::ProcessInput**, passing a pointer to an **IMFSample** interface object to the DSP plug-in.</span></span>
    1.  <span data-ttu-id="fcebe-122">Il plug-in DSP mantiene un conteggio dei riferimenti nell'interfaccia **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="fcebe-122">The DSP plug-in keeps a reference count on the **IMFSample** interface.</span></span> <span data-ttu-id="fcebe-123">Il plug-in DSP restituisce un **HRESULT** di esito positivo o negativo appropriato.</span><span class="sxs-lookup"><span data-stu-id="fcebe-123">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
    2.  <span data-ttu-id="fcebe-124">Windows Media Player chiama **IMFTransform::P rocessoutput**, passando un puntatore a una matrice di strutture del **\_ \_ \_ buffer dei dati di output di MFT** (che contengono buffer di output) al plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="fcebe-124">Windows Media Player calls **IMFTransform::ProcessOutput**, passing a pointer to an array of **MFT\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
    3.  <span data-ttu-id="fcebe-125">Il plug-in DSP elabora i dati nel buffer di input e quindi copia i dati nel buffer di output appropriato.</span><span class="sxs-lookup"><span data-stu-id="fcebe-125">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="fcebe-126">Il plug-in DSP rilascia il conteggio dei riferimenti nell'oggetto buffer di input quando tutti i dati nel buffer sono stati elaborati.</span><span class="sxs-lookup"><span data-stu-id="fcebe-126">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="fcebe-127">Il plug-in DSP restituisce quindi un **HRESULT** di esito positivo o negativo appropriato.</span><span class="sxs-lookup"><span data-stu-id="fcebe-127">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
    4.  <span data-ttu-id="fcebe-128">Windows Media Player esegue il rendering del contenuto nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="fcebe-128">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="fcebe-129">Questo processo si ripete continuamente quando il plug-in è abilitato e Windows Media Player dispone di contenuto di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="fcebe-129">This process repeats continuously while the plug-in is enabled and Windows Media Player has content to render.</span></span>

> [!Note]  
> <span data-ttu-id="fcebe-130">Non scrivere codice che scrive i dati nel buffer di input o legge i dati dal buffer di output.</span><span class="sxs-lookup"><span data-stu-id="fcebe-130">Do not write code that writes data to the input buffer or reads data from the output buffer.</span></span> <span data-ttu-id="fcebe-131">L'accesso non corretto ai buffer dei dati può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="fcebe-131">Incorrectly accessing data buffers may yield unexpected results.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fcebe-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fcebe-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcebe-133">**Panoramica per gli sviluppatori di plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="fcebe-133">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




