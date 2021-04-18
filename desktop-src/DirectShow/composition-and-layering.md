---
description: Composizione e sovrapposizione
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Composizione e sovrapposizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303823"
---
# <a name="composition-and-layering"></a><span data-ttu-id="9d47c-103">Composizione e sovrapposizione</span><span class="sxs-lookup"><span data-stu-id="9d47c-103">Composition and Layering</span></span>

<span data-ttu-id="9d47c-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="9d47c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9d47c-105">In una raccolta di tracce, la prima traccia ha la priorità più bassa (priorità 0) e ogni traccia successiva ha priorità di un livello superiore.</span><span class="sxs-lookup"><span data-stu-id="9d47c-105">In a collection of tracks, the first track has the lowest priority (priority 0) and each subsequent track has a priority one level higher.</span></span> <span data-ttu-id="9d47c-106">A ogni livello di priorità, le clip di origine in tale traccia nascondono le clip di origine nelle tracce sottostanti, a meno che tale livello non contenga anche una transizione.</span><span class="sxs-lookup"><span data-stu-id="9d47c-106">At each priority level, the source clips in that track hide the source clips in the tracks below it, unless that layer also contains a transition.</span></span> <span data-ttu-id="9d47c-107">In questo modo è possibile immaginare che la creazione di più passaggi quando viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="9d47c-107">Thus you can imagine DES making several passes when it renders.</span></span>

<span data-ttu-id="9d47c-108">Viene innanzitutto eseguito il rendering di Track 0.</span><span class="sxs-lookup"><span data-stu-id="9d47c-108">First, it renders track 0.</span></span> <span data-ttu-id="9d47c-109">Non è presente alcun elemento "in" Track 0, quindi viene eseguito il rendering delle aree vuote come immagine nera a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="9d47c-109">There is nothing "under" Track 0, so empty regions are rendered as a solid black image.</span></span> <span data-ttu-id="9d47c-110">Le transizioni in questo livello si verificano tra l'immagine nera e la traccia 0 o viceversa.</span><span class="sxs-lookup"><span data-stu-id="9d47c-110">Transitions in this layer occur between the black image and track 0 or vice versa.</span></span> <span data-ttu-id="9d47c-111">DES stabilisce la traccia 1 nella parte superiore della traccia 0, generando le transizioni tra le due tracce.</span><span class="sxs-lookup"><span data-stu-id="9d47c-111">DES lays track 1 on top of track 0, generating any transitions between the two tracks.</span></span> <span data-ttu-id="9d47c-112">Il risultato è costituito da un composto di due tracce.</span><span class="sxs-lookup"><span data-stu-id="9d47c-112">The result is the composite of the two tracks.</span></span> <span data-ttu-id="9d47c-113">Quindi posiziona il Track 2 su questo composto.</span><span class="sxs-lookup"><span data-stu-id="9d47c-113">Next, it places track 2 onto this composite.</span></span> <span data-ttu-id="9d47c-114">Le transizioni a questo livello si verificano tra composito e Track 2.</span><span class="sxs-lookup"><span data-stu-id="9d47c-114">Transitions at this layer occur between the composite and track 2.</span></span> <span data-ttu-id="9d47c-115">Il processo continua fino a quando non viene disattivata l'ultima traccia (priorità più alta).</span><span class="sxs-lookup"><span data-stu-id="9d47c-115">The process continues until the last (highest-priority) track is put down.</span></span>

<span data-ttu-id="9d47c-116">Quando più tracce sono composte insieme, si comportano come una singola traccia (denominata traccia virtuale).</span><span class="sxs-lookup"><span data-stu-id="9d47c-116">When several tracks are composited together, they behave like a single track (called a virtual track).</span></span> <span data-ttu-id="9d47c-117">L'oggetto Composition incapsula questo comportamento, rendendo possibili transizioni complesse.</span><span class="sxs-lookup"><span data-stu-id="9d47c-117">The composition object encapsulates this behavior, making complex transitions possible.</span></span> <span data-ttu-id="9d47c-118">Ad esempio, un clip video può essere cancellato da un secondo clip, mentre il composito (entrambi i clip più la cancellazione) si dissolve in una terza clip.</span><span class="sxs-lookup"><span data-stu-id="9d47c-118">For example, one video clip can wipe to a second clip, while the composite (both clips plus the wipe) fades to a third clip.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d47c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d47c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d47c-120">Introduzione con i servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="9d47c-120">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



