---
title: Velocità in bit
description: Velocità in bit
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows Media Format SDK, velocità in bit
- ASF (Advanced Systems Format), velocità in bit
- ASF (formato avanzato dei sistemi), velocità in bit
- velocità in bit, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d793be8fe04746a61eea48bcf066d95d641221a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713711"
---
# <a name="bit-rate"></a><span data-ttu-id="25795-107">Velocità in bit</span><span class="sxs-lookup"><span data-stu-id="25795-107">Bit Rate</span></span>

<span data-ttu-id="25795-108">La velocità in bit si riferisce alla quantità di dati al secondo recapitati da un file ASF.</span><span class="sxs-lookup"><span data-stu-id="25795-108">Bit rate refers to the amount of data per second that is delivered from an ASF file.</span></span> <span data-ttu-id="25795-109">Le misurazioni della velocità in bit sono in bit al secondo (BPS) o kilobit al secondo (Kbps).</span><span class="sxs-lookup"><span data-stu-id="25795-109">Bit rate measurements are in bits per second (bps) or kilobits per second (Kbps).</span></span> <span data-ttu-id="25795-110">La velocità in bit è spesso confusa con la larghezza di banda, ovvero una misurazione della capacità di trasferimento dei dati di una rete.</span><span class="sxs-lookup"><span data-stu-id="25795-110">Bit rate is often confused with bandwidth, which is a measurement of the data transfer capacity of a network.</span></span> <span data-ttu-id="25795-111">La larghezza di banda viene misurata anche in bps e kbps.</span><span class="sxs-lookup"><span data-stu-id="25795-111">Bandwidth is also measured in bps and Kbps.</span></span>

<span data-ttu-id="25795-112">Windows Media Format SDK può essere usato per creare applicazioni che forniscono contenuti basati su Windows Media in streaming da percorsi Internet o Intranet.</span><span class="sxs-lookup"><span data-stu-id="25795-112">The Windows Media Format SDK can be used to create applications that deliver streaming Windows Media-based content from Internet or intranet locations.</span></span> <span data-ttu-id="25795-113">Quando si esegue il flusso di dati in una rete o in Internet, la velocità in bit è di importanza fondamentale per l'esperienza dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="25795-113">When you are streaming data across a network or the Internet, the bit rate is of vital importance to the end-user experience.</span></span> <span data-ttu-id="25795-114">Se la larghezza di banda disponibile per la rete è inferiore alla velocità in bit del file ASF, la riproduzione del file verrà interrotta in qualche modo.</span><span class="sxs-lookup"><span data-stu-id="25795-114">If the bandwidth available to the network is less than the bit rate of the ASF file, the playback of the file will be interrupted in some way.</span></span> <span data-ttu-id="25795-115">In genere, la larghezza di banda insufficiente comporta l'omissione degli esempi o la sospensione della riproduzione mentre vengono memorizzati nel buffer più dati.</span><span class="sxs-lookup"><span data-stu-id="25795-115">Usually, insufficient bandwidth will result in either samples being skipped, or a pause in playback while more data is buffered.</span></span>

<span data-ttu-id="25795-116">A ogni file ASF viene assegnato un valore di velocità in bit al momento della creazione, in base al tipo e al numero di flussi inclusi nel profilo utilizzato.</span><span class="sxs-lookup"><span data-stu-id="25795-116">Every ASF file is assigned a bit rate value at the time of creation, based upon the type and number of streams that are included in the profile used.</span></span> <span data-ttu-id="25795-117">I singoli flussi hanno una propria velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="25795-117">Individual streams have their own bit rates.</span></span> <span data-ttu-id="25795-118">Le velocità in bit possono essere costanti (i dati originali vengono compressi in modo da mantenere un flusso costante di dati alla stessa velocità) o variabile (i dati originali vengono compressi in modo da mantenere la stessa qualità in tutto, anche se questo potrebbe significare un flusso di dati non uniforme).</span><span class="sxs-lookup"><span data-stu-id="25795-118">Bit rates can be constant (the original data is compressed in such a way as to maintain a constant flow of data at approximately the same rate) or variable (the original data is compressed in such a way as to maintain the same quality throughout, even though this may mean uneven data flow).</span></span> <span data-ttu-id="25795-119">È possibile applicare tipi di velocità in bit diversi a flussi diversi all'interno dello stesso file.</span><span class="sxs-lookup"><span data-stu-id="25795-119">Different bit rate types can be applied to different streams within the same file.</span></span>

<span data-ttu-id="25795-120">È possibile codificare lo stesso contenuto in più flussi diversi, ognuno con una velocità in bit diversa.</span><span class="sxs-lookup"><span data-stu-id="25795-120">You can encode the same content to several different streams, each with a different bit rate.</span></span> <span data-ttu-id="25795-121">È quindi possibile configurare i flussi in modo che si escludano a vicenda.</span><span class="sxs-lookup"><span data-stu-id="25795-121">Then you can configure the streams so that they are mutually exclusive.</span></span> <span data-ttu-id="25795-122">Questo consente di creare un singolo file che può essere trasmesso a utenti con larghezze di banda diverse.</span><span class="sxs-lookup"><span data-stu-id="25795-122">This enables you to create a single file that can be streamed to users with different bandwidths.</span></span> <span data-ttu-id="25795-123">Questa funzionalità è denominata velocità in bit multipla o MBR.</span><span class="sxs-lookup"><span data-stu-id="25795-123">This feature is called multiple bit rate, or MBR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25795-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25795-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25795-125">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="25795-125">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="25795-126">**Codifica della velocità in bit costante (CBR)**</span><span class="sxs-lookup"><span data-stu-id="25795-126">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="25795-127">**Input, flussi e output**</span><span class="sxs-lookup"><span data-stu-id="25795-127">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="25795-128">**Profili**</span><span class="sxs-lookup"><span data-stu-id="25795-128">**Profiles**</span></span>](profiles.md)
</dt> <dt>

[<span data-ttu-id="25795-129">**Codifica della velocità in bit variabile (VBR)**</span><span class="sxs-lookup"><span data-stu-id="25795-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




