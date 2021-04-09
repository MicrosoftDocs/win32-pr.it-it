---
title: Flussi MIDI
description: Flussi MIDI
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- MIDI (Musical Instrument Digital Interface), flussi
- MIDI (Musical Instrument Digital Interface), flussi
- buffer di flusso, flussi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117706"
---
# <a name="midi-streams"></a><span data-ttu-id="6f168-106">Flussi MIDI</span><span class="sxs-lookup"><span data-stu-id="6f168-106">MIDI Streams</span></span>

<span data-ttu-id="6f168-107">Gli eventi MIDI si verificano nel contesto di un flusso di dati MIDI.</span><span class="sxs-lookup"><span data-stu-id="6f168-107">MIDI events occur in the context of a stream of MIDI data.</span></span> <span data-ttu-id="6f168-108">Sebbene un'applicazione possa usare diversi flussi per definire i dati musicali, il mapper MIDI non riconosce più flussi.</span><span class="sxs-lookup"><span data-stu-id="6f168-108">Although an application can use several streams to define musical data, the MIDI mapper does not recognize multiple streams.</span></span> <span data-ttu-id="6f168-109">Per la maggior parte delle applicazioni che usano flussi viene usato un solo flusso MIDI.</span><span class="sxs-lookup"><span data-stu-id="6f168-109">Most applications that use streams use a single MIDI stream.</span></span>

<span data-ttu-id="6f168-110">Le funzioni seguenti funzionano con i flussi.</span><span class="sxs-lookup"><span data-stu-id="6f168-110">The following functions work with streams.</span></span>



| <span data-ttu-id="6f168-111">Valore</span><span class="sxs-lookup"><span data-stu-id="6f168-111">Value</span></span>                                            | <span data-ttu-id="6f168-112">Significato</span><span class="sxs-lookup"><span data-stu-id="6f168-112">Meaning</span></span>                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="6f168-113">**midiStreamClose**</span><span class="sxs-lookup"><span data-stu-id="6f168-113">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | <span data-ttu-id="6f168-114">Chiude un flusso MIDI.</span><span class="sxs-lookup"><span data-stu-id="6f168-114">Closes a MIDI stream.</span></span>                                                   |
| [<span data-ttu-id="6f168-115">**midiStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="6f168-115">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | <span data-ttu-id="6f168-116">Apre un flusso MIDI e recupera un handle.</span><span class="sxs-lookup"><span data-stu-id="6f168-116">Opens a MIDI stream and retrieves a handle.</span></span>                             |
| [<span data-ttu-id="6f168-117">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="6f168-117">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | <span data-ttu-id="6f168-118">Riproduce o Accoda un flusso (buffer) di dati MIDI a un dispositivo di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="6f168-118">Plays or queues a stream (buffer) of MIDI data to a MIDI output device.</span></span> |
| [<span data-ttu-id="6f168-119">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="6f168-119">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | <span data-ttu-id="6f168-120">Sospende la riproduzione di un flusso MIDI specificato.</span><span class="sxs-lookup"><span data-stu-id="6f168-120">Pauses playback of a specified MIDI stream.</span></span>                             |
| [<span data-ttu-id="6f168-121">**midiStreamPosition**</span><span class="sxs-lookup"><span data-stu-id="6f168-121">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | <span data-ttu-id="6f168-122">Recupera la posizione corrente in un flusso MIDI.</span><span class="sxs-lookup"><span data-stu-id="6f168-122">Retrieves the current position in a MIDI stream.</span></span>                        |
| [<span data-ttu-id="6f168-123">**midiStreamProperty**</span><span class="sxs-lookup"><span data-stu-id="6f168-123">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | <span data-ttu-id="6f168-124">Imposta e recupera le proprietà del flusso.</span><span class="sxs-lookup"><span data-stu-id="6f168-124">Sets and retrieves stream properties.</span></span>                                   |
| [<span data-ttu-id="6f168-125">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="6f168-125">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | <span data-ttu-id="6f168-126">Riavvia la riproduzione di un flusso MIDI sospeso.</span><span class="sxs-lookup"><span data-stu-id="6f168-126">Restarts playback of a paused MIDI stream.</span></span>                              |
| [<span data-ttu-id="6f168-127">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="6f168-127">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | <span data-ttu-id="6f168-128">Disattiva tutte le note in tutti i canali MIDI per il flusso MIDI specificato.</span><span class="sxs-lookup"><span data-stu-id="6f168-128">Turns off all notes on all MIDI channels for the specified MIDI stream.</span></span> |



 

 

 