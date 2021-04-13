---
title: Scrittura di esempi compressi
description: Scrittura di esempi compressi
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- Formato di sistemi avanzati (ASF), scrittura di esempi compressi
- ASF (Advanced Systems Format), scrittura di esempi compressi
- ASF (Advanced Systems Format), passaggio di esempi compressi
- ASF (Advanced Systems Format), passaggio di esempi compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104472251"
---
# <a name="writing-compressed-samples"></a><span data-ttu-id="5facd-107">Scrittura di esempi compressi</span><span class="sxs-lookup"><span data-stu-id="5facd-107">Writing Compressed Samples</span></span>

<span data-ttu-id="5facd-108">Per alcuni flussi audio o video, potrebbe essere necessario passare esempi già compressi anziché passare dati non elaborati.</span><span class="sxs-lookup"><span data-stu-id="5facd-108">For some audio or video streams, you may want to pass samples that are already compressed instead of passing raw data.</span></span> <span data-ttu-id="5facd-109">Questa funzionalità viene usata per copiare un flusso esistente o per scrivere esempi compressi con un codec di terze parti.</span><span class="sxs-lookup"><span data-stu-id="5facd-109">This feature is used to copy an existing stream or to write samples compressed with a third-party codec.</span></span> <span data-ttu-id="5facd-110">Il processo di scrittura di un campione compresso è identico alla scrittura di un campione non compresso, con la differenza che si usa [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) anziché [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span><span class="sxs-lookup"><span data-stu-id="5facd-110">The process of writing a compressed sample is identical to writing an uncompressed sample, except that you use [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) instead of [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span> <span data-ttu-id="5facd-111">Per ulteriori informazioni sulla scrittura di esempi non compressi, vedere [per scrivere esempi](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="5facd-111">For more information about writing uncompressed samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="5facd-112">Quando si scrivono esempi compressi, per i profili CBR, il writer eliminerà alcuni esempi, se necessario, per preservare il contenuto entro i valori specificati per la velocità in bit e la finestra del buffer.</span><span class="sxs-lookup"><span data-stu-id="5facd-112">When you write compressed samples, for CBR profiles, the writer will drop some samples, if necessary, to keep the content within the specified bit rate and buffer window values.</span></span> <span data-ttu-id="5facd-113">Per VBR, il writer non eliminerà gli esempi, ma non esiste alcun modo per assicurarsi che i valori della velocità in bit e della finestra del buffer siano corretti.</span><span class="sxs-lookup"><span data-stu-id="5facd-113">For VBR, the writer will not drop samples, but there is no way to be sure that the bit rate and buffer window values will be correct.</span></span>

<span data-ttu-id="5facd-114">Se si copia un flusso da un file a un altro, è necessario copiare sempre l'oggetto di configurazione del flusso dal profilo del file originale nel profilo del nuovo file.</span><span class="sxs-lookup"><span data-stu-id="5facd-114">If you are copying a stream from one file to another, you should always copy the stream configuration object from the profile of the original file to the profile of the new file.</span></span> <span data-ttu-id="5facd-115">Ciò garantisce che siano disponibili le informazioni corrette sulla velocità in bit e sulla finestra del buffer.</span><span class="sxs-lookup"><span data-stu-id="5facd-115">This ensures that you have the correct bit rate and buffer window information.</span></span> <span data-ttu-id="5facd-116">Se si copia un flusso compresso in un flusso con una finestra buffer inferiore impostata, gli esempi verranno eliminati durante la scrittura di file.</span><span class="sxs-lookup"><span data-stu-id="5facd-116">If you copy a compressed stream to a stream that has a lower buffer window set, samples will be dropped during file writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5facd-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5facd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5facd-118">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="5facd-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




