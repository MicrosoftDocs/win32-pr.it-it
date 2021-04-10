---
description: In che modo un flusso video codificato con VBR basato sulla qualità dispone di un numero di frame inferiore rispetto al flusso originale?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: In che modo un flusso video codificato con VBR basato sulla qualità dispone di un numero di frame inferiore rispetto al flusso originale?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227067"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a><span data-ttu-id="38d6e-103">In che modo un flusso video codificato con VBR basato sulla qualità dispone di un numero di frame inferiore rispetto al flusso originale?</span><span class="sxs-lookup"><span data-stu-id="38d6e-103">How can a video stream encoded using quality-based VBR have fewer frames than the original stream?</span></span>

<span data-ttu-id="38d6e-104">Il numero di frame di un flusso codificato può essere inferiore al numero di frame dell'originale per uno dei due motivi seguenti: frame duplicati e frame eliminati.</span><span class="sxs-lookup"><span data-stu-id="38d6e-104">The frame count of an encoded stream can be lower than the frame count of the original for one of two reasons: duplicate frames and dropped frames.</span></span>

<span data-ttu-id="38d6e-105">Il codificatore non produce in genere frame che sono duplicati esatti del frame precedente.</span><span class="sxs-lookup"><span data-stu-id="38d6e-105">The encoder does not normally produce frames that are exact duplicates of the previous frame.</span></span> <span data-ttu-id="38d6e-106">Se è necessario disporre di un campione per ogni frame (ad esempio, è necessario per alcuni contenitori), è possibile configurare il codificatore per produrre frame "fittizi" impostando la proprietà [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="38d6e-106">If you need to have a sample for every frame (this is required by some containers, for example), you can configure the encoder to produce "dummy" frames by setting the [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="38d6e-107">Il codificatore rilascia frame quando non è in grado di codificare tutti i frame senza overflow del buffer.</span><span class="sxs-lookup"><span data-stu-id="38d6e-107">The encoder drops frames when it cannot encode all of the frames without overflowing the buffer.</span></span> <span data-ttu-id="38d6e-108">I frame eliminati influiscono sulla qualità del flusso. i frame duplicati non lo fanno.</span><span class="sxs-lookup"><span data-stu-id="38d6e-108">Dropped frames affect the quality of the stream, duplicate frames do not.</span></span>

<span data-ttu-id="38d6e-109">È possibile ottenere le statistiche del frame dal codificatore per determinare se i frame sono stati eliminati.</span><span class="sxs-lookup"><span data-stu-id="38d6e-109">You can get frame statistics from the encoder to determine whether frames have been dropped.</span></span> <span data-ttu-id="38d6e-110">Per ulteriori informazioni, vedere [recupero delle statistiche di codifica](gettingencodingstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="38d6e-110">For more information, see [Getting Encoding Statistics](gettingencodingstatistics.md).</span></span>

<span data-ttu-id="38d6e-111">In genere, i flussi VBR basati sulla qualità avranno un numero di frame inferiore rispetto a quello originale se sono presenti frame duplicati (poiché la velocità in bit non è vincolata).</span><span class="sxs-lookup"><span data-stu-id="38d6e-111">Typically, quality-based VBR streams will only have fewer frames than the original if there are duplicate frames (because the bit rate is not constrained).</span></span>

## <a name="related-topics"></a><span data-ttu-id="38d6e-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38d6e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38d6e-113">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="38d6e-113">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



