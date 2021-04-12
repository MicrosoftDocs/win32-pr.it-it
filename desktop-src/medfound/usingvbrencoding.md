---
description: In questa sezione viene descritto come configurare i flussi VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Uso della codifica VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226496"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a><span data-ttu-id="61163-103">Uso della codifica VBR (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="61163-103">Using VBR Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="61163-104">Come descritto in dettaglio nell'argomento [metodi di codifica](encodingmethods.md) , viene usata la codifica con velocità in bit variabile (VBR) per migliorare la coerenza della qualità del contenuto.</span><span class="sxs-lookup"><span data-stu-id="61163-104">As detailed in the [Encoding Methods](encodingmethods.md) topic, variable bit rate (VBR) encoding is used to improve the consistency of content quality.</span></span> <span data-ttu-id="61163-105">Si configurano i flussi VBR nello stesso modo in cui si codificano i flussi di velocità in bit costante (CBR), ad eccezione dei parametri del buffer (velocità in bit e finestra del buffer).</span><span class="sxs-lookup"><span data-stu-id="61163-105">You configure VBR streams in the same way that you encode constant bit rate (CBR) streams, except for the buffer parameters (bit rate and buffer window).</span></span> <span data-ttu-id="61163-106">In questa sezione viene descritto come configurare i flussi VBR.</span><span class="sxs-lookup"><span data-stu-id="61163-106">This section describes how to configure VBR streams.</span></span>

## <a name="configuring-quality-based-vbr"></a><span data-ttu-id="61163-107">Configurazione di VBR basato sulla qualità</span><span class="sxs-lookup"><span data-stu-id="61163-107">Configuring Quality Based VBR</span></span>

<span data-ttu-id="61163-108">La codifica tramite il metodo VBR basato sulla qualità non richiede parametri del buffer predefiniti.</span><span class="sxs-lookup"><span data-stu-id="61163-108">Encoding using the quality based VBR method does not require any predefined buffer parameters.</span></span> <span data-ttu-id="61163-109">Si specifica invece un livello di qualità (da 0 a 100) che il codificatore utilizza per determinare dinamicamente i parametri del buffer appropriati.</span><span class="sxs-lookup"><span data-stu-id="61163-109">Instead, you specify a quality level (from 0 to 100) which the encoder uses to determine the appropriate buffer parameters dynamically.</span></span> <span data-ttu-id="61163-110">Questa modalità di codifica utilizza un solo passaggio di codifica.</span><span class="sxs-lookup"><span data-stu-id="61163-110">This encoding mode uses only one encoding pass.</span></span>

<span data-ttu-id="61163-111">È possibile enumerare i tipi di output VBR basati sulla qualità supportati per i codec audio.</span><span class="sxs-lookup"><span data-stu-id="61163-111">You can enumerate the supported quality-based VBR output types for the audio codecs.</span></span> <span data-ttu-id="61163-112">È necessario utilizzare uno dei tipi restituiti da DMO quando si imposta il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="61163-112">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="61163-113">Per altre informazioni, vedere [enumerazione di tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="61163-113">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="61163-114">Per configurare un flusso video VBR basato sulla qualità, è necessario impostare le proprietà elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="61163-114">To configure a quality-based VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="61163-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="61163-115">Property</span></span>                                            | <span data-ttu-id="61163-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61163-116">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61163-117">\_VBRENABLED MFPKEY</span><span class="sxs-lookup"><span data-stu-id="61163-117">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="61163-118">Impostare su VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="61163-118">Set to VARIANT\_TRUE.</span></span>                                                                                                                                   |
| [<span data-ttu-id="61163-119">\_VBRQUALITY MFPKEY</span><span class="sxs-lookup"><span data-stu-id="61163-119">MFPKEY\_VBRQUALITY</span></span>](mfpkey-vbrqualityproperty.md) | <span data-ttu-id="61163-120">Impostare sul valore di qualità desiderato, da 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="61163-120">Set to the desired quality value, from 0 to 100.</span></span> <span data-ttu-id="61163-121">Non tutti i valori di qualità rappresentano impostazioni discrete.</span><span class="sxs-lookup"><span data-stu-id="61163-121">Not all quality values represent discrete settings.</span></span> <span data-ttu-id="61163-122">Per ulteriori informazioni, vedere la descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="61163-122">See the property description for more information.</span></span> |



 

## <a name="configuring-unconstrained-vbr"></a><span data-ttu-id="61163-123">Configurazione di un VBR non vincolato</span><span class="sxs-lookup"><span data-stu-id="61163-123">Configuring Unconstrained VBR</span></span>

<span data-ttu-id="61163-124">La codifica VBR non vincolata consente al codificatore di variare le dimensioni dei singoli campioni senza limiti di buffer espliciti.</span><span class="sxs-lookup"><span data-stu-id="61163-124">Unconstrained VBR encoding enables the encoder to vary the size of individual samples without any explicit buffer limits.</span></span> <span data-ttu-id="61163-125">Tuttavia, la velocità in bit media per la durata del contenuto risultante deve essere minore o uguale al valore specificato.</span><span class="sxs-lookup"><span data-stu-id="61163-125">However, the average bit rate over the duration of the resulting content must be less than or equal to the specified value.</span></span> <span data-ttu-id="61163-126">Il VBR non vincolato richiede due sessioni di codifica.</span><span class="sxs-lookup"><span data-stu-id="61163-126">Unconstrained VBR requires two encoding passes.</span></span>

<span data-ttu-id="61163-127">È possibile enumerare i tipi di output di VBR a due passaggi supportati per i codec audio.</span><span class="sxs-lookup"><span data-stu-id="61163-127">You can enumerate the supported two-pass VBR output types for the audio codecs.</span></span> <span data-ttu-id="61163-128">È necessario utilizzare uno dei tipi restituiti da DMO quando si imposta il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="61163-128">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="61163-129">Per altre informazioni, vedere [enumerazione di tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="61163-129">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="61163-130">Per configurare un flusso video VBR non vincolato, è necessario impostare le proprietà elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="61163-130">To configure an unconstrained VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="61163-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="61163-131">Property</span></span>                                            | <span data-ttu-id="61163-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61163-132">Description</span></span>                          |
|-----------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="61163-133">\_VBRENABLED MFPKEY</span><span class="sxs-lookup"><span data-stu-id="61163-133">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="61163-134">Impostare su VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="61163-134">Set to VARIANT\_TRUE.</span></span>                |
| [<span data-ttu-id="61163-135">\_PASSESUSED MFPKEY</span><span class="sxs-lookup"><span data-stu-id="61163-135">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="61163-136">Impostare su 2.</span><span class="sxs-lookup"><span data-stu-id="61163-136">Set to 2.</span></span>                            |
| [<span data-ttu-id="61163-137">\_RAVG MFPKEY</span><span class="sxs-lookup"><span data-stu-id="61163-137">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="61163-138">Impostare sulla velocità in bit media desiderata.</span><span class="sxs-lookup"><span data-stu-id="61163-138">Set to the desired average bit rate.</span></span> |



 

## <a name="configuring-peak-constrained-vbr"></a><span data-ttu-id="61163-139">Configurazione di Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="61163-139">Configuring Peak-Constrained VBR</span></span>

<span data-ttu-id="61163-140">Il numero di VBR con vincoli di picco è simile a quello di VBR non vincolato, perché è limitato a una velocità in bit media per la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="61163-140">Peak-constrained VBR is like unconstrained VBR in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="61163-141">Inoltre, la funzionalità VBR con vincoli di picco è conforme a un buffer di picco.</span><span class="sxs-lookup"><span data-stu-id="61163-141">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="61163-142">Questo buffer viene descritto usando una velocità in bit massima e una finestra del buffer di picco, così come un buffer CBR viene descritto da una velocità in bit media e da una finestra del buffer.</span><span class="sxs-lookup"><span data-stu-id="61163-142">This buffer is described using a peak bit rate and a peak buffer window, just as a CBR buffer is described by an average bit rate and a buffer window.</span></span> <span data-ttu-id="61163-143">Questa modalità offre alla flessibilità del codificatore la modalità di codifica dei singoli campioni rispettando al massimo le limitazioni.</span><span class="sxs-lookup"><span data-stu-id="61163-143">This mode gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span> <span data-ttu-id="61163-144">Questa operazione è particolarmente utile quando la decodifica viene eseguita da un chip in un dispositivo, ad esempio un lettore DVD, in cui sono presenti limitazioni hardware che devono essere prese in considerazione.</span><span class="sxs-lookup"><span data-stu-id="61163-144">This is particularly useful when decoding is performed by a chip in a device, like a DVD player, where there are hardware limitations that must be considered.</span></span>

<span data-ttu-id="61163-145">I tipi di output supportati del codificatore audio VBR con vincoli di picco sono gli stessi tipi enumerati per VBR non vincolato.</span><span class="sxs-lookup"><span data-stu-id="61163-145">The supported peak-constrained, VBR audio encoder output types are the same types enumerated for unconstrained VBR.</span></span> <span data-ttu-id="61163-146">Impostare i valori di picco su DMO e utilizzare il tipo recapitato.</span><span class="sxs-lookup"><span data-stu-id="61163-146">Set the peak values on the DMO and use the delivered type.</span></span> <span data-ttu-id="61163-147">Per altre informazioni, vedere [enumerazione di tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="61163-147">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="61163-148">Per configurare un flusso video VBR con vincoli di picco, è necessario impostare le proprietà elencate nella tabella seguente usando il metodo **IPropertyBag:: Write** .</span><span class="sxs-lookup"><span data-stu-id="61163-148">To configure a peak-constrained VBR video stream, you must set the properties that are listed in the following table using the **IPropertyBag::Write** method.</span></span>



| <span data-ttu-id="61163-149">Proprietà</span><span class="sxs-lookup"><span data-stu-id="61163-149">Property</span></span>                                            | <span data-ttu-id="61163-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61163-150">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="61163-151">\_VBRENABLED MFPKEY</span><span class="sxs-lookup"><span data-stu-id="61163-151">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="61163-152">Impostare su VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="61163-152">Set to VARIANT\_TRUE.</span></span>                                           |
| [<span data-ttu-id="61163-153">\_PASSESUSED MFPKEY</span><span class="sxs-lookup"><span data-stu-id="61163-153">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="61163-154">Impostare su 2.</span><span class="sxs-lookup"><span data-stu-id="61163-154">Set to 2.</span></span>                                                       |
| [<span data-ttu-id="61163-155">\_RAVG MFPKEY</span><span class="sxs-lookup"><span data-stu-id="61163-155">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="61163-156">Impostare sulla velocità in bit media desiderata.</span><span class="sxs-lookup"><span data-stu-id="61163-156">Set to the desired average bit rate.</span></span>                            |
| [<span data-ttu-id="61163-157">\_Rmax MFPKEY</span><span class="sxs-lookup"><span data-stu-id="61163-157">MFPKEY\_RMAX</span></span>](mfpkey-rmaxproperty.md)             | <span data-ttu-id="61163-158">Impostare sulla velocità in bit massima desiderata.</span><span class="sxs-lookup"><span data-stu-id="61163-158">Set to the desired peak bit rate.</span></span>                               |
| [<span data-ttu-id="61163-159">\_BMAX MFPKEY</span><span class="sxs-lookup"><span data-stu-id="61163-159">MFPKEY\_BMAX</span></span>](mfpkey-bmaxproperty.md)             | <span data-ttu-id="61163-160">Impostare sulla finestra del buffer che corrisponde alla velocità in bit del picco.</span><span class="sxs-lookup"><span data-stu-id="61163-160">Set to the buffer window that corresponds to the peak bit rate.</span></span> |



 

> [!Note]  
> <span data-ttu-id="61163-161">È consigliabile impostare la velocità in bit massima su almeno il doppio della velocità in bit media.</span><span class="sxs-lookup"><span data-stu-id="61163-161">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="61163-162">Impostando la velocità di picco su un valore inferiore, il codec può codificare il contenuto come CBR a due passaggi invece che con il picco di VBR.</span><span class="sxs-lookup"><span data-stu-id="61163-162">Setting the peak rate to a lower value may cause the codec to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="61163-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61163-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61163-164">Codec Windows Media</span><span class="sxs-lookup"><span data-stu-id="61163-164">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> <dt>

[<span data-ttu-id="61163-165">Uso della codifica Two-Pass</span><span class="sxs-lookup"><span data-stu-id="61163-165">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="61163-166">Utilizzo di audio</span><span class="sxs-lookup"><span data-stu-id="61163-166">Working with Audio</span></span>](workingwithaudio.md)
</dt> <dt>

[<span data-ttu-id="61163-167">Uso dei video</span><span class="sxs-lookup"><span data-stu-id="61163-167">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



