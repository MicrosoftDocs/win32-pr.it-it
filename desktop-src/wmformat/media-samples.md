---
title: Esempi di supporti (Windows Media Format 11 SDK)
description: Informazioni sugli esempi multimediali in Windows Media Format 11 SDK. Un esempio di supporto è un oggetto che contiene un elenco ordinato di zero o più buffer.
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media Format SDK, esempi multimediali
- Windows Media Format SDK,esempi
- Advanced Systems Format (ASF), esempi di supporti
- ASF (Advanced Systems Format), esempi multimediali
- Advanced Systems Format (ASF), esempi
- ASF (Advanced Systems Format), esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8d264aa23e80f1e692f28789c2f2e631ef3ed8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989076"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="33164-110">Esempi di supporti (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="33164-110">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="33164-111">Un campione multimediale, o campione, è un blocco di dati multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="33164-111">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="33164-112">Un esempio è l'unità di base che viene manipolata dagli oggetti di lettura e scrittura di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="33164-112">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="33164-113">Il contenuto di un singolo campione è determinato dal tipo di supporto associato all'esempio.</span><span class="sxs-lookup"><span data-stu-id="33164-113">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="33164-114">Per i video, ogni esempio rappresenta un singolo fotogramma.</span><span class="sxs-lookup"><span data-stu-id="33164-114">For video, each sample represents a single frame.</span></span> <span data-ttu-id="33164-115">Per l'audio, la quantità di dati in un singolo campione viene impostata nel profilo usato per creare il file ASF.</span><span class="sxs-lookup"><span data-stu-id="33164-115">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="33164-116">Gli esempi possono contenere dati non compressi o possono contenere dati compressi, nel qual caso sono detti *esempi di flusso.*</span><span class="sxs-lookup"><span data-stu-id="33164-116">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="33164-117">Quando si crea un file ASF, si passano esempi al writer.</span><span class="sxs-lookup"><span data-stu-id="33164-117">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="33164-118">Il writer coordina la compressione degli esempi con il codec appropriato e dispone i dati compressi nella sezione dei dati del file ASF.</span><span class="sxs-lookup"><span data-stu-id="33164-118">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="33164-119">Durante la riproduzione, il lettore legge i dati compressi, decomprime i dati e fornisce i dati non compressi ricostruiti come campioni di output.</span><span class="sxs-lookup"><span data-stu-id="33164-119">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="33164-120">Tutti gli esempi usati da Windows Media Format SDK vengono incapsulati nell'oggetto buffer la cui memoria viene allocata automaticamente dai componenti di run-time dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="33164-120">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="33164-121">È anche possibile allocare buffer personalizzati, se necessario, usando le funzionalità avanzate del writer e del lettore.</span><span class="sxs-lookup"><span data-stu-id="33164-121">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="33164-122">**Nota:** Il termine esempio viene usato in questo SDK per fare riferimento a un campione multimediale, non a un esempio audio.</span><span class="sxs-lookup"><span data-stu-id="33164-122">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="33164-123">Nella codifica audio, un esempio fa riferimento a un singolo valore audio codificato.</span><span class="sxs-lookup"><span data-stu-id="33164-123">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="33164-124">In genere, la qualità dell'audio codificato viene specificata da un numero di campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="33164-124">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="33164-125">Ad esempio, l'audio di qualità CD viene registrato a 44.100 campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="33164-125">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="33164-126">Questo valore è comunemente abbreviato con la notazione Hz, quindi 44.100 campioni al secondo sarebbero 44.100 Hz o 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="33164-126">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33164-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33164-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33164-128">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="33164-128">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="33164-129">**Interfaccia INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="33164-129">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="33164-130">**Input, flussi e output**</span><span class="sxs-lookup"><span data-stu-id="33164-130">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




