---
title: Mappe patch
description: Mappe patch
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, mappe patch
- Mappe patch
- Programmi MIDI-modificare i messaggi
- Messaggi del controller del volume MIDI
- messaggi di modifica programma
- messaggi del controller del volume
- Mapper MIDI, messaggi di modifica del programma
- Mapper MIDI, messaggi del controller del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329620"
---
# <a name="patch-maps"></a><span data-ttu-id="a6026-113">Mappe patch</span><span class="sxs-lookup"><span data-stu-id="a6026-113">Patch Maps</span></span>

<span data-ttu-id="a6026-114">A ogni voce della mappa del canale può essere associata una mappa patch.</span><span class="sxs-lookup"><span data-stu-id="a6026-114">Each channel map entry can have an associated patch map.</span></span> <span data-ttu-id="a6026-115">Le mappe delle patch influiscono sul programma MIDI, sulla modifica e sui messaggi del controller del volume.</span><span class="sxs-lookup"><span data-stu-id="a6026-115">Patch maps affect MIDI program-change and volume-controller messages.</span></span> <span data-ttu-id="a6026-116">Messaggi di modifica del programma indicano a un sintetizzatore di modificare il suono dello strumento (patch) per un canale specificato.</span><span class="sxs-lookup"><span data-stu-id="a6026-116">Program-change messages tell a synthesizer to change the instrument sound (patch) for a specified channel.</span></span> <span data-ttu-id="a6026-117">I messaggi del controller del volume impostano il volume per un canale.</span><span class="sxs-lookup"><span data-stu-id="a6026-117">Volume-controller messages set the volume for a channel.</span></span>

<span data-ttu-id="a6026-118">Una mappa di patch include una tabella di traduzione con una voce per ogni valore di modifica del programma 128.</span><span class="sxs-lookup"><span data-stu-id="a6026-118">A patch map has a translation table with an entry for each of the 128 program-change values.</span></span> <span data-ttu-id="a6026-119">Ogni mappa di patch specifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a6026-119">Each patch map specifies the following:</span></span>

-   <span data-ttu-id="a6026-120">Valore di modifica di un programma di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a6026-120">A destination program-change value.</span></span>
-   <span data-ttu-id="a6026-121">Volume scalare.</span><span class="sxs-lookup"><span data-stu-id="a6026-121">A volume scalar.</span></span> <span data-ttu-id="a6026-122">Per ulteriori informazioni, vedere [volume Scalar](the-volume-scalar.md).</span><span class="sxs-lookup"><span data-stu-id="a6026-122">(For more information, see [The Volume Scalar](the-volume-scalar.md).)</span></span>
-   <span data-ttu-id="a6026-123">Mappa delle chiavi facoltativa.</span><span class="sxs-lookup"><span data-stu-id="a6026-123">An optional key map.</span></span> <span data-ttu-id="a6026-124">Per ulteriori informazioni, vedere la pagina relativa ai [mapping delle chiavi](key-maps.md).</span><span class="sxs-lookup"><span data-stu-id="a6026-124">(For more information, see [Key Maps](key-maps.md).)</span></span>

<span data-ttu-id="a6026-125">Quando i messaggi di modifica del programma vengono ricevuti dal mapper MIDI, il valore di modifica del programma di destinazione viene sostituito con il valore di modifica del programma nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="a6026-125">When program-change messages are received by the MIDI Mapper, the destination program-change value is substituted for the program-change value in the message.</span></span> <span data-ttu-id="a6026-126">Ad esempio, se il valore del programma di destinazione-modifica valore per programma-modifica 16 è 18, il mapper del MIDI modifica il messaggio di modifica del programma MIDI, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="a6026-126">For example, if the destination program-change value for program-change 16 is 18, the MIDI Mapper modifies the MIDI program-change message as shown in the following illustration.</span></span>

![immagine del mapper MIDI](images/mmap-a03.gif)

 

 




