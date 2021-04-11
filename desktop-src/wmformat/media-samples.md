---
title: Esempi di supporto (Windows Media Format 11 SDK)
description: Esempi di supporti
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media Format SDK, esempi di supporti
- Windows Media Format SDK, esempi
- Advanced Systems Format (ASF), esempi di supporti
- ASF (Advanced Systems Format), esempi di supporti
- ASF (Advanced Systems Format), esempi
- ASF (formato avanzato dei sistemi), esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d46a933775877f4566115ba3936c0f9f8bd7b3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103963702"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="cb008-109">Esempi di supporto (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="cb008-109">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="cb008-110">Un esempio multimediale, o esempio, è un blocco di dati multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="cb008-110">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="cb008-111">Un esempio è l'unità di base che viene modificata dagli oggetti di lettura e scrittura di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="cb008-111">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="cb008-112">Il contenuto di un singolo campione è determinato dal tipo di supporto associato all'esempio.</span><span class="sxs-lookup"><span data-stu-id="cb008-112">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="cb008-113">Per video, ogni esempio rappresenta un singolo frame.</span><span class="sxs-lookup"><span data-stu-id="cb008-113">For video, each sample represents a single frame.</span></span> <span data-ttu-id="cb008-114">Per l'audio, la quantità di dati in un singolo campione viene impostata nel profilo utilizzato per creare il file ASF.</span><span class="sxs-lookup"><span data-stu-id="cb008-114">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="cb008-115">Gli esempi possono contenere dati non compressi oppure possono contenere dati compressi, nel qual caso vengono chiamati esempi di *flusso*.</span><span class="sxs-lookup"><span data-stu-id="cb008-115">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="cb008-116">Quando si crea un file ASF, gli esempi vengono passati al writer.</span><span class="sxs-lookup"><span data-stu-id="cb008-116">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="cb008-117">Il writer coordina la compressione degli esempi con il codec appropriato e dispone i dati compressi nella sezione dati del file ASF.</span><span class="sxs-lookup"><span data-stu-id="cb008-117">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="cb008-118">Durante la riproduzione, il lettore legge i dati compressi, li decomprime e fornisce i dati non compressi ricostruiti come esempi di output.</span><span class="sxs-lookup"><span data-stu-id="cb008-118">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="cb008-119">Tutti gli esempi usati da Windows Media Format SDK vengono incapsulati in un oggetto buffer la cui memoria viene allocata automaticamente dai componenti di runtime dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="cb008-119">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="cb008-120">Se necessario, è anche possibile allocare i propri buffer, usando le funzionalità avanzate del writer e del lettore.</span><span class="sxs-lookup"><span data-stu-id="cb008-120">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="cb008-121">**Nota** Il termine esempio viene usato in questo SDK per fare riferimento a un esempio di supporto, non a un esempio di audio.</span><span class="sxs-lookup"><span data-stu-id="cb008-121">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="cb008-122">Nella codifica audio un esempio si riferisce a un singolo valore audio codificato.</span><span class="sxs-lookup"><span data-stu-id="cb008-122">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="cb008-123">In genere, la qualità dell'audio codificato viene specificata da un numero di campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="cb008-123">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="cb008-124">Ad esempio, il suono di qualità CD viene registrato a 44.100 campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="cb008-124">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="cb008-125">Questo valore viene comunemente abbreviato con la notazione Hz, quindi 44.100 campioni al secondo saranno 44.100 Hz o 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="cb008-125">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb008-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb008-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb008-127">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="cb008-127">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="cb008-128">**Interfaccia INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="cb008-128">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="cb008-129">**Input, flussi e output**</span><span class="sxs-lookup"><span data-stu-id="cb008-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




