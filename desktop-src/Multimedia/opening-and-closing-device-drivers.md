---
title: Apertura e chiusura di driver di dispositivo
description: Apertura e chiusura di driver di dispositivo
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- MIDI (Musical Instrument Digital Interface), apertura di dispositivi
- MIDI (Musical Instrument Digital Interface), apertura di dispositivi
- Servizi MIDI, apertura di dispositivi
- apertura di dispositivi MIDI
- MIDI (Musical Instrument Digital Interface), chiusura di dispositivi
- MIDI (Musical Instrument Digital Interface), chiusura di dispositivi
- Servizi MIDI, chiusura di dispositivi
- chiusura di dispositivi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725079"
---
# <a name="opening-and-closing-device-drivers"></a><span data-ttu-id="390e1-111">Apertura e chiusura di driver di dispositivo</span><span class="sxs-lookup"><span data-stu-id="390e1-111">Opening and Closing Device Drivers</span></span>

<span data-ttu-id="390e1-112">È necessario aprire un dispositivo MIDI prima di usarlo ed è necessario chiudere il dispositivo non appena si termina di usarlo.</span><span class="sxs-lookup"><span data-stu-id="390e1-112">You must open a MIDI device before using it, and you should close the device as soon as you finish using it.</span></span> <span data-ttu-id="390e1-113">Windows fornisce le funzioni seguenti per aprire e chiudere tipi diversi di dispositivi MIDI.</span><span class="sxs-lookup"><span data-stu-id="390e1-113">Windows provides the following functions to open and close different types of MIDI devices.</span></span>



| <span data-ttu-id="390e1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="390e1-114">Value</span></span>                                | <span data-ttu-id="390e1-115">Significato</span><span class="sxs-lookup"><span data-stu-id="390e1-115">Meaning</span></span>                                            |
|--------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="390e1-116">**midiInClose**</span><span class="sxs-lookup"><span data-stu-id="390e1-116">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | <span data-ttu-id="390e1-117">Chiude un dispositivo di input MIDI specificato.</span><span class="sxs-lookup"><span data-stu-id="390e1-117">Closes a specified MIDI input device.</span></span>              |
| [<span data-ttu-id="390e1-118">**midiInOpen**</span><span class="sxs-lookup"><span data-stu-id="390e1-118">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | <span data-ttu-id="390e1-119">Apre un dispositivo di input MIDI specificato per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="390e1-119">Opens a specified MIDI input device for recording.</span></span> |
| [<span data-ttu-id="390e1-120">**midiOutClose**</span><span class="sxs-lookup"><span data-stu-id="390e1-120">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | <span data-ttu-id="390e1-121">Chiude un dispositivo di output MIDI specificato.</span><span class="sxs-lookup"><span data-stu-id="390e1-121">Closes a specified MIDI output device.</span></span>             |
| [<span data-ttu-id="390e1-122">**midiOutOpen**</span><span class="sxs-lookup"><span data-stu-id="390e1-122">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | <span data-ttu-id="390e1-123">Apre un dispositivo di output MIDI per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="390e1-123">Opens a MIDI output device for playback.</span></span>           |



 

<span data-ttu-id="390e1-124">Ogni funzione che apre un dispositivo MIDI accetta come parametri un identificatore di dispositivo, un indirizzo di una posizione di memoria e alcuni parametri univoci per i dispositivi MIDI.</span><span class="sxs-lookup"><span data-stu-id="390e1-124">Each function that opens a MIDI device takes as parameters a device identifier, an address of a memory location, and some parameters unique to MIDI devices.</span></span> <span data-ttu-id="390e1-125">La posizione di memoria viene riempita con un handle di dispositivo, che viene usato per identificare il dispositivo audio aperto nelle chiamate ad altre funzioni audio.</span><span class="sxs-lookup"><span data-stu-id="390e1-125">The memory location is filled with a device handle, which is used to identify the open audio device in calls to other audio functions.</span></span>

<span data-ttu-id="390e1-126">Molte funzioni MIDI possono accettare un handle di dispositivo o un identificatore di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="390e1-126">Many MIDI functions can accept either a device handle or a device identifier.</span></span> <span data-ttu-id="390e1-127">Sebbene sia possibile usare un handle di dispositivo ovunque venga usato un identificatore di dispositivo, non è sempre possibile usare un identificatore di dispositivo quando viene chiamato un handle per.</span><span class="sxs-lookup"><span data-stu-id="390e1-127">Although you can use a device handle wherever you would use a device identifier, you cannot always use a device identifier when a handle is called for.</span></span>

> [!Note]  
> <span data-ttu-id="390e1-128">I dispositivi MIDI non sono necessariamente condivisibili, pertanto è possibile che un determinato dispositivo non sia disponibile quando richiesto da un utente.</span><span class="sxs-lookup"><span data-stu-id="390e1-128">MIDI devices are not necessarily sharable, so a particular device may not be available when a user requests it.</span></span> <span data-ttu-id="390e1-129">In questo caso, l'applicazione deve notificare all'utente e consentire all'utente di provare ad aprire nuovamente il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="390e1-129">If this happens, the application should notify the user and allow the user to try to open the device again.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="390e1-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="390e1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="390e1-131">Servizi MIDI</span><span class="sxs-lookup"><span data-stu-id="390e1-131">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 