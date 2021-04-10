---
title: Mappe chiave
description: Mappe chiave
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, mappe chiave
- Mappe chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955321"
---
# <a name="key-maps"></a><span data-ttu-id="48e21-107">Mappe chiave</span><span class="sxs-lookup"><span data-stu-id="48e21-107">Key Maps</span></span>

<span data-ttu-id="48e21-108">Ogni voce nella tabella di traduzione della mappa patch può avere una mappa delle chiavi associata.</span><span class="sxs-lookup"><span data-stu-id="48e21-108">Each entry in the patch-map translation table can have an associated key map.</span></span> <span data-ttu-id="48e21-109">Le mappe chiave influiscono sui messaggi note-on, note-off e polifoniche-Key-aftertouch.</span><span class="sxs-lookup"><span data-stu-id="48e21-109">Key maps affect note-on, note-off, and polyphonic-key-aftertouch messages.</span></span> <span data-ttu-id="48e21-110">Una mappa delle chiavi include una tabella di traduzione con una voce per ogni valore di chiave MIDI 128.</span><span class="sxs-lookup"><span data-stu-id="48e21-110">A key map has a translation table with an entry for each of the 128 MIDI key values.</span></span> <span data-ttu-id="48e21-111">Se, ad esempio, la voce relativa al valore della chiave 60 è 72, il mapper MIDI modifica i messaggi di note MIDI su, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="48e21-111">For example, if the entry for key value 60 is 72, the MIDI Mapper modifies MIDI note-on messages as shown in the following illustration.</span></span>

![immagine del mapper MIDI](images/mmap-a06.gif)

<span data-ttu-id="48e21-113">Le mappe chiave sono utili con i sintetizzatori che hanno strumenti di percussione basati su chiavi con un suono di percussione particolare assegnato a ogni chiave.</span><span class="sxs-lookup"><span data-stu-id="48e21-113">Key maps are useful with synthesizers that have key-based percussion instruments with a particular percussion sound assigned to each key.</span></span> <span data-ttu-id="48e21-114">Le mappe chiave vengono in genere assegnate alla prima patch nelle mappe delle patch nei canali di percussione (10 e 16).</span><span class="sxs-lookup"><span data-stu-id="48e21-114">Key maps are usually assigned to the first patch in the patch maps on the percussion channels (10 and 16).</span></span>

 

 




