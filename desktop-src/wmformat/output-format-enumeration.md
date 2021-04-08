---
title: Enumerazione del formato di output
description: Enumerazione del formato di output
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows Media Format SDK, enumerazioni del formato di output
- Advanced Systems Format (ASF), enumerazioni del formato di output
- ASF (formato avanzato dei sistemi), enumerazioni del formato di output
- Windows Media Format SDK, interfaccia IWMReaderTypeNegotiation
- Advanced Systems Format (ASF), interfaccia IWMReaderTypeNegotiation
- ASF (formato avanzato dei sistemi), interfaccia IWMReaderTypeNegotiation
- enumerazioni del formato di output
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046262"
---
# <a name="output-format-enumeration"></a><span data-ttu-id="83b0c-111">Enumerazione del formato di output</span><span class="sxs-lookup"><span data-stu-id="83b0c-111">Output Format Enumeration</span></span>

<span data-ttu-id="83b0c-112">Sia l'oggetto Reader che l'oggetto Reader sincrono comunicano con i codec per enumerare i formati di output possibili per i flussi compressi.</span><span class="sxs-lookup"><span data-stu-id="83b0c-112">Both the reader object and the synchronous reader object communicate with the codecs to enumerate the possible output formats for compressed streams.</span></span> <span data-ttu-id="83b0c-113">Quando si legge un file contenente contenuti compressi con uno o più codec Windows Media, è possibile esaminare i possibili formati di output per scegliere quello più adatto alle proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="83b0c-113">When you read a file containing content compressed with one or more of the Windows Media codecs, you can examine the possible output formats to choose the one that best suits your needs.</span></span> <span data-ttu-id="83b0c-114">Per praticità, ogni codec ha un formato di output predefinito impostato sul formato usato più di frequente.</span><span class="sxs-lookup"><span data-stu-id="83b0c-114">For convenience, each codec has a default output format which is set to the most commonly used format.</span></span> <span data-ttu-id="83b0c-115">Per ulteriori informazioni sull'enumerazione di output, vedere [utilizzo degli output](working-with-outputs.md).</span><span class="sxs-lookup"><span data-stu-id="83b0c-115">For more information about output enumeration, see [Working with Outputs](working-with-outputs.md).</span></span>

<span data-ttu-id="83b0c-116">È possibile apportare alcune modifiche a un formato di output a seconda del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="83b0c-116">You can make certain changes to an output format depending upon the media type.</span></span> <span data-ttu-id="83b0c-117">Per i flussi video, ad esempio, è possibile modificare le dimensioni del frame e la profondità del colore.</span><span class="sxs-lookup"><span data-stu-id="83b0c-117">For video streams, for example, you can change the frame size and color depth.</span></span> <span data-ttu-id="83b0c-118">Gli oggetti di lettura supportano entrambi un'interfaccia per testare le modifiche apportate al formato di output, denominato [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span><span class="sxs-lookup"><span data-stu-id="83b0c-118">The reading objects both support an interface to test changes you make to the output format, called [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="83b0c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83b0c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83b0c-120">**Funzionalità di lettura file**</span><span class="sxs-lookup"><span data-stu-id="83b0c-120">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




