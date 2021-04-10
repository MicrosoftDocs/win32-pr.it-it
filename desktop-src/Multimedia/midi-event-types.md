---
title: Tipi di evento MIDI
description: Tipi di evento MIDI
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- MIDI (Musical Instrument Digital Interface), tipi di evento
- MIDI (Musical Instrument Digital Interface), tipi di evento
- Struttura MIDIEVENT
- buffer di flusso, tipi di evento MIDI
- Tipi di evento MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046723"
---
# <a name="midi-event-types"></a><span data-ttu-id="bdff2-108">Tipi di evento MIDI</span><span class="sxs-lookup"><span data-stu-id="bdff2-108">MIDI Event Types</span></span>

<span data-ttu-id="bdff2-109">Il membro **dwEvent** della struttura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) descrive l'evento MIDI che deve essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="bdff2-109">The **dwEvent** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure describes the MIDI event that is to take place.</span></span> <span data-ttu-id="bdff2-110">Gli eventi brevi si adattano interamente a questo membro.</span><span class="sxs-lookup"><span data-stu-id="bdff2-110">Short events fit entirely into this member.</span></span> <span data-ttu-id="bdff2-111">Per gli eventi Long sono necessari uno o più valori parola doppia oltre al membro **dwEvent** per archiviare le descrizioni degli eventi.</span><span class="sxs-lookup"><span data-stu-id="bdff2-111">Long events require one or more doubleword values in addition to the **dwEvent** member to store the event descriptions.</span></span>

<span data-ttu-id="bdff2-112">Il byte elevato del membro **dwEvent** contiene informazioni sul fatto che l'evento sia lungo o breve e che venga generato un callback insieme all'evento.</span><span class="sxs-lookup"><span data-stu-id="bdff2-112">The high byte of the **dwEvent** member contains information about whether the event is long or short and about whether a callback is generated along with the event.</span></span> <span data-ttu-id="bdff2-113">Questo byte viene inoltre usato per descrivere il tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="bdff2-113">In addition, this byte is used to describe the event type.</span></span> <span data-ttu-id="bdff2-114">I restanti 24 bit del membro **dwEvent** vengono utilizzati per contenere i parametri evento (per i messaggi brevi) o per contenere la lunghezza dei parametri evento (per i messaggi lunghi).</span><span class="sxs-lookup"><span data-stu-id="bdff2-114">The remaining 24 bits of the **dwEvent** member are used either to contain the event parameters (for short messages) or to contain the length of the event parameters (for long messages).</span></span> <span data-ttu-id="bdff2-115">Per estrarre informazioni dal membro **dwEvent** , usare le macro [**MEVT \_ eventType**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) e [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) .</span><span class="sxs-lookup"><span data-stu-id="bdff2-115">To extract information from the **dwEvent** member, use the [**MEVT\_EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) and [**MEVT\_EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) macros.</span></span>

<span data-ttu-id="bdff2-116">Per una descrizione dei tipi di evento predefiniti, vedere il materiale di riferimento per la struttura **MIDIEVENT** .</span><span class="sxs-lookup"><span data-stu-id="bdff2-116">For a description of the predefined event types, see the reference material for the **MIDIEVENT** structure.</span></span>

 

 