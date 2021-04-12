---
title: Conversione di dati da un formato a un altro
description: Conversione di dati da un formato a un altro
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Gestione compressione audio (ACM), conversione dei dati
- ACM (Gestione compressione audio), conversione dei dati
- Esempi di ACM, conversione di dati
- conversione dei dati
- acmStreamOpen (funzione)
- acmStreamSize (funzione)
- acmStreamPrepareHeader (funzione)
- acmStreamConvert (funzione)
- acmStreamUnprepareHeader (funzione)
- acmStreamClose (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329756"
---
# <a name="converting-data-from-one-format-to-another"></a><span data-ttu-id="418c3-113">Conversione di dati da un formato a un altro</span><span class="sxs-lookup"><span data-stu-id="418c3-113">Converting Data from One Format to Another</span></span>

<span data-ttu-id="418c3-114">L'ACM usa le funzioni di flusso per supportare la conversione del formato dati.</span><span class="sxs-lookup"><span data-stu-id="418c3-114">The ACM uses stream functions to support data format conversion.</span></span> <span data-ttu-id="418c3-115">I convertitori nell'ACM cambiano il formato, ma non il tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="418c3-115">Converters in the ACM change the format, but not the data type.</span></span> <span data-ttu-id="418c3-116">Un modulo Converter, ad esempio, può modificare 44-kHz, dati a 16 bit in dati a 8 bit a 44-kHz.</span><span class="sxs-lookup"><span data-stu-id="418c3-116">For example, a converter module can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span>

<span data-ttu-id="418c3-117">Le funzioni ACM seguenti supportano la conversione del formato dati.</span><span class="sxs-lookup"><span data-stu-id="418c3-117">The following ACM functions support data format conversion.</span></span> <span data-ttu-id="418c3-118">Sono elencate nell'ordine in cui vengono in genere usate.</span><span class="sxs-lookup"><span data-stu-id="418c3-118">They are listed in the order in which you would typically use them.</span></span>

-   <span data-ttu-id="418c3-119">La funzione [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) apre un flusso di conversione.</span><span class="sxs-lookup"><span data-stu-id="418c3-119">The [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) function opens a conversion stream.</span></span>
-   <span data-ttu-id="418c3-120">La funzione [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) calcola la dimensione appropriata del buffer di origine o di destinazione.</span><span class="sxs-lookup"><span data-stu-id="418c3-120">The [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function calculates the appropriate size of the source or destination buffer.</span></span>
-   <span data-ttu-id="418c3-121">La funzione [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) prepara i buffer di origine e di destinazione da utilizzare in una conversione.</span><span class="sxs-lookup"><span data-stu-id="418c3-121">The [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) function prepares source and destination buffers to be used in a conversion.</span></span>
-   <span data-ttu-id="418c3-122">La funzione [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) converte i dati in un buffer di origine nel formato di destinazione, scrivendo i dati convertiti nel buffer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="418c3-122">The [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) function converts data in a source buffer into the destination format, writing the converted data into the destination buffer.</span></span>
-   <span data-ttu-id="418c3-123">La funzione [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) pulisce i buffer di origine e di destinazione preparati da **acmStreamPrepareHeader**.</span><span class="sxs-lookup"><span data-stu-id="418c3-123">The [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) function cleans up the source and destination buffers prepared by **acmStreamPrepareHeader**.</span></span> <span data-ttu-id="418c3-124">È necessario chiamare questa funzione prima di liberare i buffer di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="418c3-124">You must call this function before freeing the source and destination buffers.</span></span>
-   <span data-ttu-id="418c3-125">La funzione [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) chiude un flusso di conversione.</span><span class="sxs-lookup"><span data-stu-id="418c3-125">The [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) function closes a conversion stream.</span></span>

<span data-ttu-id="418c3-126">Quando si convertono i dati, identificare prima il formato di origine, quindi scegliere il formato di destinazione.</span><span class="sxs-lookup"><span data-stu-id="418c3-126">When converting data, first identify the source format, then choose the destination format.</span></span> <span data-ttu-id="418c3-127">Il modo più semplice per eseguire questa operazione consiste nell'usare la funzione [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , che visualizza una finestra di dialogo di selezione del formato e restituisce la scelta del formato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="418c3-127">The easiest way to do this is by using the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, which displays a format-selection dialog box and returns the user's format choice.</span></span>

<span data-ttu-id="418c3-128">Quando si conoscono i formati di origine e di destinazione, è possibile usare [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) per aprire un flusso di conversione.</span><span class="sxs-lookup"><span data-stu-id="418c3-128">When you know the source and destination formats, you can use [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) to open a conversion stream.</span></span> <span data-ttu-id="418c3-129">È quindi possibile usare la funzione [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) per determinare le dimensioni del buffer appropriate.</span><span class="sxs-lookup"><span data-stu-id="418c3-129">Then you can use the [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function to determine the appropriate buffer sizes.</span></span>

<span data-ttu-id="418c3-130">Il passaggio successivo consiste nel preparare i buffer da usare nella conversione usando [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span><span class="sxs-lookup"><span data-stu-id="418c3-130">The next step is to prepare the buffers to be used in the conversion by using [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span></span>

<span data-ttu-id="418c3-131">Per eseguire la conversione, utilizzare [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) fino a quando non vengono elaborati tutti i buffer.</span><span class="sxs-lookup"><span data-stu-id="418c3-131">To perform the conversion, use [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) until all the buffers have been processed.</span></span> <span data-ttu-id="418c3-132">Al termine della conversione, usare [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) per pulire i buffer e quindi usare [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) per chiudere il flusso di conversione.</span><span class="sxs-lookup"><span data-stu-id="418c3-132">When the conversion is complete, use [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) to clean up the buffers and then use [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) to close the conversion stream.</span></span>

 

 




