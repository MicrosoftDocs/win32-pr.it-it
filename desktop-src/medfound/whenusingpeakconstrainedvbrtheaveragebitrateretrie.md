---
description: Quando si usa il valore VBR con vincoli di picco, la velocità in bit media recuperata dall'oggetto codec è maggiore della velocità in bit massima.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Quando si usa il valore VBR con vincoli di picco, la velocità in bit media recuperata dall'oggetto codec è maggiore della velocità in bit massima. Come è possibile?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344841"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a><span data-ttu-id="b402c-104">Quando si usa il valore VBR con vincoli di picco, la velocità in bit media recuperata dall'oggetto codec è maggiore della velocità in bit massima.</span><span class="sxs-lookup"><span data-stu-id="b402c-104">When I use peak-constrained VBR, the average bit rate retrieved from the codec object is larger than the peak bit rate.</span></span> <span data-ttu-id="b402c-105">Come è possibile?</span><span class="sxs-lookup"><span data-stu-id="b402c-105">How is that possible?</span></span>

<span data-ttu-id="b402c-106">La relazione tra la velocità in bit media e la velocità in bit massima è spesso fraintesa.</span><span class="sxs-lookup"><span data-stu-id="b402c-106">The relationship between the average bit rate and the peak bit rate is often misunderstood.</span></span> <span data-ttu-id="b402c-107">La velocità in bit massima descrive un vincolo di buffer in un periodo di tempo specificato dalla finestra del buffer di picco.</span><span class="sxs-lookup"><span data-stu-id="b402c-107">The peak bit rate describes a buffer constraint over a period of time specified by the peak buffer window.</span></span> <span data-ttu-id="b402c-108">La velocità in bit media per VBR a due passaggi (non vincolata o con picco) corrisponde alla media di bit al secondo per la durata del file.</span><span class="sxs-lookup"><span data-stu-id="b402c-108">The average bit rate for two-pass VBR (unconstrained or peak-constrained) is the average bits per second over the duration of the file.</span></span>

<span data-ttu-id="b402c-109">Come descritto nel [modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md), la velocità in bit effettiva utilizzata in un periodo di tempo uguale alla finestra del buffer può avvicinarsi al doppio della velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="b402c-109">As described in [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md), the actual bit rate used over a period of time equal to the buffer window can approach twice the bit rate.</span></span> <span data-ttu-id="b402c-110">Questo perché il buffer, definito come un numero di bit uguale alla velocità in bit per la finestra del buffer (in secondi), viene svuotato a una velocità costante.</span><span class="sxs-lookup"><span data-stu-id="b402c-110">This is because the buffer, defined as a number of bits equal to the bit rate times the buffer window (in seconds), is being emptied at a constant rate.</span></span>

<span data-ttu-id="b402c-111">Ad esempio, in un secondo di un flusso di 56 Kbps, il codificatore crea esempi totali di 59 KB.</span><span class="sxs-lookup"><span data-stu-id="b402c-111">For example, in one second of a 56 Kbps stream, the encoder creates samples totaling 59 Kb.</span></span> <span data-ttu-id="b402c-112">Quindi, 56 KB di dati vengono rimossi dal buffer in quel secondo, lasciando 3 KB nel buffer.</span><span class="sxs-lookup"><span data-stu-id="b402c-112">So, 56 Kb of data is removed from the buffer in that second, leaving 3 Kb in the buffer.</span></span> <span data-ttu-id="b402c-113">Se il flusso ha una finestra del buffer di tre secondi e pertanto una dimensione del buffer totale di 168 KB, il riempimento del buffer richiederà circa 40 secondi.</span><span class="sxs-lookup"><span data-stu-id="b402c-113">If the stream has a buffer window of three seconds, and thus a total buffer size of 168 Kb, it would take almost 40 seconds to fill the buffer.</span></span> <span data-ttu-id="b402c-114">Velocità in bit media per il flusso (se la durata è inferiore al tempo necessario per riempire il buffer) è 59 kbps, anche se la velocità in bit è impostata su 56 Kbps.</span><span class="sxs-lookup"><span data-stu-id="b402c-114">The average bit rate for the stream (if its duration is less than the time it takes to fill the buffer) is 59 Kbps, even though the bit rate is set to 56 Kbps.</span></span>

<span data-ttu-id="b402c-115">Lo stesso fenomeno si applica ai vincoli di velocità in bit massimi.</span><span class="sxs-lookup"><span data-stu-id="b402c-115">The same phenomenon applies to peak bit rate constraints.</span></span> <span data-ttu-id="b402c-116">Per contenuto breve, la velocità in bit media calcolata dall'oggetto codec dopo il completamento della codifica può essere maggiore della velocità in bit massima.</span><span class="sxs-lookup"><span data-stu-id="b402c-116">For short content, the average bit rate computed by the codec object after encoding is completed can be greater than the peak bit rate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b402c-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b402c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b402c-118">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="b402c-118">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



