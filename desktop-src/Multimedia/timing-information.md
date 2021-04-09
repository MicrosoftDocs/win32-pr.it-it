---
title: Informazioni sull'intervallo
description: Informazioni sull'intervallo
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- MIDI (Musical Instrument Digital Interface), informazioni sugli intervalli
- MIDI (Musical Instrument Digital Interface), informazioni sugli intervalli
- buffer di flusso, informazioni sugli intervalli
- Struttura MIDIEVENT
- buffer di flusso, formato SMPTE
- buffer di flusso, ora della nota trimestre
- buffer di flusso, cicli
- Formato SMPTE
- ora della nota trimestre
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117599"
---
# <a name="timing-information"></a><span data-ttu-id="d4192-113">Informazioni sull'intervallo</span><span class="sxs-lookup"><span data-stu-id="d4192-113">Timing Information</span></span>

<span data-ttu-id="d4192-114">Le informazioni di temporizzazione per un evento MIDI vengono archiviate nel membro **dwDeltaTime** della struttura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="d4192-114">Timing information for a MIDI event is stored in the **dwDeltaTime** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="d4192-115">Il tempo è espresso in cicli, come definito nella specifica dei *file MIDI Standard 1,0* .</span><span class="sxs-lookup"><span data-stu-id="d4192-115">Time is given in ticks, as defined in the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="d4192-116">La lunghezza di un segno di selezione è definita dal formato dell'ora e possibilmente dal tempo associato al flusso.</span><span class="sxs-lookup"><span data-stu-id="d4192-116">The length of a tick is defined by the time format and possibly the tempo associated with the stream.</span></span> <span data-ttu-id="d4192-117">Per altre informazioni sui flussi, vedere [flussi MIDI](midi-streams.md).</span><span class="sxs-lookup"><span data-stu-id="d4192-117">For more information about streams, see [MIDI Streams](midi-streams.md).</span></span>

<span data-ttu-id="d4192-118">Un segno di ingrandimento è espresso in microsecondi per ogni trimestre o come segni di cadenza del periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="d4192-118">A tick is expressed either as microseconds per quarter note or as ticks of SMPTE (Society of Motion Picture and Television Engineers) time.</span></span> <span data-ttu-id="d4192-119">Le applicazioni che inviano messaggi MIDI singolarmente o usano messaggi MIDI non elaborati usano le informazioni relative a tempo e tempo per la nota del trimestre per determinare la durata di un segno di cadenza.</span><span class="sxs-lookup"><span data-stu-id="d4192-119">Applications that send MIDI messages individually or use unprocessed MIDI messages use quarter note time and tempo information to determine the duration of a tick.</span></span> <span data-ttu-id="d4192-120">Le applicazioni che preelaborano i messaggi MIDI possono archiviare il tempo trascorso come un conteggio delle unità SMPTE utilizzate.</span><span class="sxs-lookup"><span data-stu-id="d4192-120">Applications that preprocess MIDI messages can store the elapsed time as a count of the SMPTE units being used.</span></span>

<span data-ttu-id="d4192-121">La durata della nota di trimestre è indicata da uno zero nel bit a parola alta (bit 15) della parola di divisione temporale.</span><span class="sxs-lookup"><span data-stu-id="d4192-121">Quarter note time is indicated with a zero in the high-word bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="d4192-122">Il resto della parola contiene la nota relativa ai cicli per trimestre.</span><span class="sxs-lookup"><span data-stu-id="d4192-122">The remainder of the word contains the ticks per quarter note.</span></span> <span data-ttu-id="d4192-123">Un tempo associato a un flusso di dati MIDI viene mantenuto in unità (in microsecondi per ogni trimestre) coerente con la specifica dei *file MIDI Standard 1,0* .</span><span class="sxs-lookup"><span data-stu-id="d4192-123">A tempo associated with a stream of MIDI data is kept in units (microseconds per quarter note) consistent with the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="d4192-124">Ad esempio, una nota di trimestre in 4/4 di tempo che usa un tempo di 500.000 microsecondi per ogni trimestre viene riprodotta alla velocità di 120 battute al minuto.</span><span class="sxs-lookup"><span data-stu-id="d4192-124">For example, a quarter note in 4/4 time that uses a tempo of 500,000 microseconds per quarter note plays at the rate of 120 beats per minute.</span></span>

<span data-ttu-id="d4192-125">I formati della divisione temporale SMPTE specificano completamente la lunghezza di un segno di incirca senza la necessità di informazioni sul tempo.</span><span class="sxs-lookup"><span data-stu-id="d4192-125">SMPTE time division formats completely specify the length of a tick without the need for tempo information.</span></span> <span data-ttu-id="d4192-126">Quando si usano i formati di ora SMPTE, le sequenze MIDI possono essere sincronizzate con altri eventi SMPTE, ad esempio video o audio con striping.</span><span class="sxs-lookup"><span data-stu-id="d4192-126">In using SMPTE time formats, MIDI sequences can be synchronized with other SMPTE events, such as video or striped audio.</span></span> <span data-ttu-id="d4192-127">Il tempo SMPTE è indicato con un valore 1 nel bit più significativo (bit 15) della parola di divisione temporale.</span><span class="sxs-lookup"><span data-stu-id="d4192-127">SMPTE time is indicated with a 1 in the high-order bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="d4192-128">Il resto del byte più significativo specifica il formato SMPTE in uso come valore negativo.</span><span class="sxs-lookup"><span data-stu-id="d4192-128">The rest of the most-significant byte specifies the SMPTE format in use as negative values.</span></span> <span data-ttu-id="d4192-129">I formati SMPTE supportati e i valori corrispondenti (tra parentesi) sono 24 (-24), 25 (-25), 30 (-30) e 30 drop (-29).</span><span class="sxs-lookup"><span data-stu-id="d4192-129">The supported SMPTE formats and their corresponding values (in parentheses) are 24 (-24), 25 (-25), 30 (-30), and 30 drop (-29).</span></span> <span data-ttu-id="d4192-130">Il byte inferiore della parola di divisione temporale specifica il numero di cicli per fotogramma SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d4192-130">The low byte of the time-division word specifies the number of ticks per SMPTE frame.</span></span>

 

 