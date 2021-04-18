---
title: Copia di flussi con esempi decompressi
description: Copia di flussi con esempi decompressi
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows Media Format SDK, copia di flussi
- Formato di sistemi avanzati (ASF), copia dei flussi
- ASF (formato avanzato dei sistemi), copia dei flussi
- flussi, copia con dati decompressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298785"
---
# <a name="copying-streams-using-decompressed-samples"></a><span data-ttu-id="4b8c3-107">Copia di flussi con esempi decompressi</span><span class="sxs-lookup"><span data-stu-id="4b8c3-107">Copying Streams Using Decompressed Samples</span></span>

<span data-ttu-id="4b8c3-108">Si consiglia vivamente di non copiare i flussi da un file a un altro usando campioni decompressi.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-108">It is strongly recommended that you not copy streams from one file to another using decompressed samples.</span></span> <span data-ttu-id="4b8c3-109">Il processo di decompressione e ricompressione degli esempi ridurrà la qualità dell'output.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-109">The process of decompressing and recompressing samples will degrade the quality of the output.</span></span> <span data-ttu-id="4b8c3-110">Se è necessario decomprimere gli esempi e quindi copiarli in un altro flusso, è possibile che si verifichino alcune difficoltà con i flussi codificati della velocità in bit (VBR) basati sulla qualità.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-110">If you do need to decompress your samples and then copy them to another stream, you may encounter some difficulty with quality-based variable bit rate (VBR) encoded streams.</span></span>

<span data-ttu-id="4b8c3-111">Quando il codec termina la compressione di un flusso VBR basato sulla qualità, registra la velocità in bit e la finestra del buffer del contenuto risultante.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-111">When the codec finishes compressing a quality-based VBR stream, it records the bit rate and buffer window of the resulting content.</span></span> <span data-ttu-id="4b8c3-112">Quando si legge un file contenente un flusso codificato con VBR basato sulla qualità, il profilo ottenuto dal lettore annoterà la velocità in bit e la finestra del buffer, nonché la velocità in bit massima e la finestra massima del buffer.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-112">When you read a file containing a stream encoded with quality-based VBR, the profile obtained from the reader will note the bit rate and buffer window as well as the maximum bit rate and maximum buffer window.</span></span> <span data-ttu-id="4b8c3-113">Questa configurazione nel profilo indica normalmente un flusso di velocità in bit limitato a una velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-113">This configuration in the profile normally signifies a bit-rate constrained variable bit rate stream.</span></span> <span data-ttu-id="4b8c3-114">Di conseguenza, quando si imposta il profilo sul writer, è previsto un passaggio di pre-elaborazione per il flusso, perché i flussi VBR vincolati a velocità in bit richiedono la codifica in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-114">As a result, when you set the profile on the writer, it will expect a preprocessing pass for the stream, because bit-rate constrained VBR streams require two-pass encoding.</span></span> <span data-ttu-id="4b8c3-115">È consigliabile considerare il flusso come se fosse un flusso VBR vincolato a velocità in bit e recapitare gli esempi per la pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-115">You should treat the stream as if it were a bit-rate constrained VBR stream and deliver the samples for preprocessing.</span></span> <span data-ttu-id="4b8c3-116">Poiché si utilizzano i valori restituiti dopo la codifica del contenuto a un particolare livello di qualità, tali valori rappresentano il livello di qualità desiderato.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-116">Because you are using the values returned after encoding the content at a particular quality level, those values represent the desired quality level.</span></span> <span data-ttu-id="4b8c3-117">Naturalmente, la qualità dell'output di cui è stato ricodificato sarà leggermente ridotta, in seguito alla nuova codifica.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-117">Of course, the quality of the re-encoded output will be somewhat degraded anyway, as a result of the re-encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b8c3-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b8c3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b8c3-119">**Copia di dati da un file a un altro**</span><span class="sxs-lookup"><span data-stu-id="4b8c3-119">**Copying Data from One File to Another**</span></span>](copying-data-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="4b8c3-120">**Copia dei flussi senza decomprimere i dati**</span><span class="sxs-lookup"><span data-stu-id="4b8c3-120">**Copying Streams Without Decompressing the Data**</span></span>](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




