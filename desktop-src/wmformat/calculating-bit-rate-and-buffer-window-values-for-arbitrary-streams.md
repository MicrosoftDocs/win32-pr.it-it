---
title: Calcolo dei valori della velocità in bit e della finestra del buffer per flussi arbitrari
description: Calcolo dei valori della velocità in bit e della finestra del buffer per flussi arbitrari
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- flussi, velocità in bit
- codec, calcolo della velocità in bit per flussi arbitrari
- velocità in bit, calcolo per flussi arbitrari
- flussi, calcolo di velocità in bit per flussi arbitrari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044140"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a><span data-ttu-id="3b55a-107">Calcolo dei valori della velocità in bit e della finestra del buffer per flussi arbitrari</span><span class="sxs-lookup"><span data-stu-id="3b55a-107">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>

<span data-ttu-id="3b55a-108">Il calcolo della velocità in bit e della finestra del buffer appropriate per un tipo di flusso arbitrario non è una scienza esatta.</span><span class="sxs-lookup"><span data-stu-id="3b55a-108">Calculating the proper bit rate and buffer window for an arbitrary stream type is not an exact science.</span></span> <span data-ttu-id="3b55a-109">Un approccio semplice consiste nell'impostare la velocità in bit in modo che corrisponda alla dimensione del flusso divisa per la relativa lunghezza, in secondi.</span><span class="sxs-lookup"><span data-stu-id="3b55a-109">One simple approach is to set the bit rate to match the size of the stream divided by its length, in seconds.</span></span> <span data-ttu-id="3b55a-110">Ad esempio, un flusso contenente un totale di 68000 bit che dura 20 secondi potrebbe avere una velocità in bit di 3400 bit al secondo (68000 bit/20 secondi = 3400 bit al secondo).</span><span class="sxs-lookup"><span data-stu-id="3b55a-110">For example, a stream containing a total of 68000 bits lasting 20 seconds might have a bit rate of 3400 bits per second (68000 bits / 20 seconds = 3400 bits per second).</span></span>

<span data-ttu-id="3b55a-111">Il problema di questa semplice tecnica di assegnazione della velocità in bit è che non prende in considerazione la distribuzione dei dati all'interno del flusso.</span><span class="sxs-lookup"><span data-stu-id="3b55a-111">The problem with this simple technique of assigning bit rate is that it does not take into account the distribution of data within the stream.</span></span> <span data-ttu-id="3b55a-112">Molti flussi arbitrari contengono maggiori quantità di dati a intervalli lungo la sequenza temporale del file.</span><span class="sxs-lookup"><span data-stu-id="3b55a-112">Many arbitrary streams contain larger amounts of data at intervals along the timeline of the file.</span></span> <span data-ttu-id="3b55a-113">I flussi di immagini, ad esempio, presentano esempi di dimensioni piuttosto elevate, ma sono in genere separati da pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="3b55a-113">Image streams, for example, have samples that are rather large, but are usually spaced several seconds apart.</span></span> <span data-ttu-id="3b55a-114">È necessario impostare la finestra buffer per verificare che il buffer non venga overflow.</span><span class="sxs-lookup"><span data-stu-id="3b55a-114">The buffer window must be set to ensure that the buffer will not overflow.</span></span>

<span data-ttu-id="3b55a-115">Per controllare la finestra del buffer, moltiplicare la velocità in bit (bit al secondo) con la finestra del buffer (in secondi) e dividere per 1000 per ottenere la dimensione, in bit, del buffer per il flusso.</span><span class="sxs-lookup"><span data-stu-id="3b55a-115">To check the buffer window, multiply the bit rate (bits per second) by the buffer window (in seconds) and divide by 1000 to get the size, in bits, of the buffer for the stream.</span></span> <span data-ttu-id="3b55a-116">Assicurarsi quindi che le dimensioni del buffer siano sufficienti a mantenere una qualsiasi combinazione di campioni nel flusso inferiore alla finestra del buffer in fase di presentazione.</span><span class="sxs-lookup"><span data-stu-id="3b55a-116">Then make sure that the buffer size is large enough to hold any combination of samples in the stream that are less than the buffer window apart in presentation time.</span></span> <span data-ttu-id="3b55a-117">In caso di dubbi, impostare entrambi i valori su un valore leggermente superiore rispetto a quelli necessari.</span><span class="sxs-lookup"><span data-stu-id="3b55a-117">When in doubt, set both values a little higher than you think you need them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b55a-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b55a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b55a-119">**Contenuto del buffer**</span><span class="sxs-lookup"><span data-stu-id="3b55a-119">**Buffering Content**</span></span>](buffering-content.md)
</dt> <dt>

[<span data-ttu-id="3b55a-120">**Configurazione di tipi di flusso arbitrari**</span><span class="sxs-lookup"><span data-stu-id="3b55a-120">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




