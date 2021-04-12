---
title: Reimpostazione dell'output MIDI
description: Reimpostazione dell'output MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- MIDI (Musical Instrument Digital Interface), reimpostazione dei dispositivi di output
- MIDI (Musical Instrument Digital Interface), reimpostazione dei dispositivi di output
- riproduzione di file MIDI, reimpostazione dei dispositivi di output
- reimpostazione dei dispositivi di output
- MIDI (Musical Instrument Digital Interface), dispositivi di output
- MIDI (Musical Instrument Digital Interface), dispositivi di output
- riproduzione di file MIDI, dispositivi di output
- Dispositivi di output MIDI
- EOX (End-of-Exclusive)
- End-of-Exclusive (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336878"
---
# <a name="resetting-midi-output"></a><span data-ttu-id="58af3-113">Reimpostazione dell'output MIDI</span><span class="sxs-lookup"><span data-stu-id="58af3-113">Resetting MIDI Output</span></span>

<span data-ttu-id="58af3-114">La funzione [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) disattiva tutte le note in tutti i canali MIDI per un dispositivo MIDI specificato.</span><span class="sxs-lookup"><span data-stu-id="58af3-114">The [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) function turns off all notes on all MIDI channels for a specified MIDI device.</span></span> <span data-ttu-id="58af3-115">Quindi, la funzione contrassegna i buffer esclusivi del sistema in sospeso come completato e li restituisce all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="58af3-115">Then, the function marks any pending system-exclusive buffers as done and returns them to the application.</span></span> <span data-ttu-id="58af3-116">Questa funzione può essere utile in un'applicazione che usa l'output MIDI per fornire all'utente la possibilità di reimpostare l'output MIDI.</span><span class="sxs-lookup"><span data-stu-id="58af3-116">This function can be useful in an application that uses MIDI output to provide the user with the ability to reset MIDI output.</span></span>

> [!Note]  
> <span data-ttu-id="58af3-117">La chiusura di un messaggio esclusivo del sistema senza inviare un byte EOX (End of Exclusive) può causare problemi per il dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="58af3-117">Terminating a system-exclusive message without sending an EOX (end-of-exclusive) byte can cause problems for the receiving device.</span></span> <span data-ttu-id="58af3-118">La funzione **midiOutReset** non invia un byte EOX quando termina un messaggio esclusivo del sistema, perché le applicazioni sono responsabili di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="58af3-118">The **midiOutReset** function does not send an EOX byte when it terminates a system-exclusive message, because applications are responsible for doing this.</span></span>

 

 

 