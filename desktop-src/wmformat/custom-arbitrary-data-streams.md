---
title: Flussi di dati arbitrari personalizzati
description: Flussi di dati arbitrari personalizzati
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows Media Format SDK, flussi di dati arbitrari personalizzati
- Formati di sistemi avanzati (ASF), flussi di dati arbitrari personalizzati
- ASF (Advanced Systems Format), flussi di dati arbitrari personalizzati
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- flussi di dati arbitrari personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298919"
---
# <a name="custom-arbitrary-data-streams"></a><span data-ttu-id="b4322-110">Flussi di dati arbitrari personalizzati</span><span class="sxs-lookup"><span data-stu-id="b4322-110">Custom Arbitrary Data Streams</span></span>

<span data-ttu-id="b4322-111">È possibile creare un flusso in un file ASF per contenere qualsiasi tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="b4322-111">You can create a stream in an ASF file to contain any sort of data.</span></span> <span data-ttu-id="b4322-112">Se nessuno dei tipi di flusso supportati è adatto alle proprie esigenze, è necessario usare un flusso di dati arbitrari.</span><span class="sxs-lookup"><span data-stu-id="b4322-112">If none of the supported stream types suits your needs, you must use an arbitrary data stream.</span></span> <span data-ttu-id="b4322-113">L'oggetto writer gestisce un flusso di dati arbitrari Analogamente a qualsiasi flusso non compresso. gli esempi sono disponibili in pacchetti e combinati con gli esempi di altri flussi nella sezione dati del file.</span><span class="sxs-lookup"><span data-stu-id="b4322-113">The writer object handles an arbitrary data stream just as it does any uncompressed stream; the samples are packetized and combined with the samples from other streams in the data section of the file.</span></span> <span data-ttu-id="b4322-114">Naturalmente, solo un'applicazione di lettura che è stata programmata in modo specifico per gestire il tipo arbitrario sarà in grado di gestire i dati dopo che sono stati recapitati dall'oggetto di lettura.</span><span class="sxs-lookup"><span data-stu-id="b4322-114">Of course, only a reading application that has been specifically programmed to deal with your arbitrary type will be able to handle the data after it is delivered by the reading object.</span></span>

<span data-ttu-id="b4322-115">Un uso comune di flussi di dati arbitrari è per i dati multimediali codificati usando un codec di terze parti.</span><span class="sxs-lookup"><span data-stu-id="b4322-115">One common use of arbitrary data streams is for media data encoded by using a third-party codec.</span></span> <span data-ttu-id="b4322-116">Poiché gli oggetti di questo SDK non interagiscono direttamente con i codec di terze parti, l'applicazione di scrittura deve elaborare gli esempi con la parte di codifica del codec e passare gli esempi compressi al writer.</span><span class="sxs-lookup"><span data-stu-id="b4322-116">Because the objects of this SDK do not interact directly with third-party codecs, your writing application must process the samples with the encoding portion of the codec and pass the compressed samples to the writer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4322-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b4322-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4322-118">**Flussi arbitrari**</span><span class="sxs-lookup"><span data-stu-id="b4322-118">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="b4322-119">**Configurazione di flussi arbitrari personalizzati**</span><span class="sxs-lookup"><span data-stu-id="b4322-119">**Configuring Custom Arbitrary Streams**</span></span>](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




