---
title: Contenuto del buffer
description: Contenuto del buffer
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Media Format SDK, contenuto del buffer
- contenuto del buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297744"
---
# <a name="buffering-content"></a><span data-ttu-id="5e9f5-105">Contenuto del buffer</span><span class="sxs-lookup"><span data-stu-id="5e9f5-105">Buffering Content</span></span>

<span data-ttu-id="5e9f5-106">Quando l'oggetto Reader apre un file di flusso, determina le dimensioni del buffer in base alle impostazioni nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-106">When the reader object opens a streaming file, it determines the size of the buffer based upon settings in the header of the file.</span></span> <span data-ttu-id="5e9f5-107">È possibile considerare il buffer come un bucket con un foro nella parte inferiore che perde a una velocità costante.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-107">You can think of the buffer as a bucket with a hole in the bottom that leaks at a constant rate.</span></span> <span data-ttu-id="5e9f5-108">Fino a quando la velocità con cui viene riempito il bucket non è, in media, maggiore della frequenza con cui si verificano perdite, il bucket non verrà mai overflow.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-108">As long as the rate at which the bucket is filled is not, on average, greater than the rate at which it is leaking, the bucket will never overflow.</span></span>

<span data-ttu-id="5e9f5-109">La velocità con cui si verifica la perdita del bucket immaginaria è la velocità in bit del flusso.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-109">The rate at which the imaginary bucket leaks is the bit rate of the stream.</span></span> <span data-ttu-id="5e9f5-110">La velocità di riempimento del bucket è la velocità effettiva in bit del flusso.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-110">The rate at which the bucket fills is the actual streaming bit rate.</span></span> <span data-ttu-id="5e9f5-111">I dati in un flusso compresso variano a seconda della quantità di compressione conseguita, da campione a campione.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-111">The data in a compressed stream varies in size from sample to sample depending on the amount of compression that was achieved.</span></span> <span data-ttu-id="5e9f5-112">Pertanto, anche se la velocità in bit del flusso è impostata nel profilo, rappresenta la velocità in bit media, non una costante.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-112">Thus, even though the bit rate of the stream is set in the profile, it represents the average bit rate, not a constant.</span></span>

<span data-ttu-id="5e9f5-113">L'altra impostazione di flusso importante per il processo di buffering è la finestra buffer.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-113">The other stream setting important to the buffering process is the buffer window.</span></span> <span data-ttu-id="5e9f5-114">La finestra buffer viene misurata nel tempo e specifica la quantità di contenuto che può essere memorizzato nel buffer.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-114">The buffer window is measured in time and specifies how much content can be buffered.</span></span> <span data-ttu-id="5e9f5-115">È possibile trovare la capacità del bucket immaginario usando la finestra buffer.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-115">The capacity of the imaginary bucket can be found using the buffer window.</span></span> <span data-ttu-id="5e9f5-116">Se, ad esempio, si dispone di un flusso con una velocità in bit di 32 kbps e una finestra del buffer di 3 secondi, il buffer viene ridimensionato in modo da contenere 3 secondi di contenuto di 32 kbps o 12.000 byte (32.000 bit al secondo x 3 secondi/8 bit per byte).</span><span class="sxs-lookup"><span data-stu-id="5e9f5-116">For example, if you have a stream with a bit rate of 32 Kbps and a buffer window of 3 seconds, the buffer is sized to hold 3 seconds of 32 Kbps content, or 12,000 bytes (32,000 bits per second x 3 seconds / 8 bits per byte).</span></span> <span data-ttu-id="5e9f5-117">Il codec limita la variazione tra la velocità effettiva in bit di streaming dei campioni codificati, in modo che, in un periodo di tempo uguale alla finestra del buffer, la velocità in bit media non sia maggiore della velocità in bit del flusso.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-117">The codec limits the variation between the actual streaming bit rate of encoded samples so that over a period of time equal to the buffer window, the average bit rate is no greater than the bit rate of the stream.</span></span>

<span data-ttu-id="5e9f5-118">In genere, è possibile impostare la velocità in bit e la finestra del buffer per un flusso in un profilo e il writer gestisce il resto.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-118">Normally, you set the bit rate and buffer window for a stream in a profile, and the writer handles the rest.</span></span> <span data-ttu-id="5e9f5-119">Quando si passano esempi compressi al lettore, tuttavia, è necessario assicurarsi che i valori corretti vengano trasferiti nel nuovo file impostando la velocità in bit e la finestra del buffer per il flusso nel profilo di destinazione sui valori del flusso compresso.</span><span class="sxs-lookup"><span data-stu-id="5e9f5-119">When passing compressed samples to the reader, however, you must ensure that the correct values are transferred to the new file by setting the bit rate and buffer window for the stream in the destination profile to the values from the compressed stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e9f5-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5e9f5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e9f5-121">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="5e9f5-121">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="5e9f5-122">**Esempi di supporti**</span><span class="sxs-lookup"><span data-stu-id="5e9f5-122">**Media Samples**</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="5e9f5-123">**Input, flussi e output**</span><span class="sxs-lookup"><span data-stu-id="5e9f5-123">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




