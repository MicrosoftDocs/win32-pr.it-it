---
title: Il mapper MIDI e Windows
description: Il mapper MIDI e Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad3cee4fb37de6ecbfdc4f81860afcb9f589d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046677"
---
# <a name="the-midi-mapper-and-windows"></a><span data-ttu-id="95167-106">Il mapper MIDI e Windows</span><span class="sxs-lookup"><span data-stu-id="95167-106">The MIDI Mapper and Windows</span></span>

<span data-ttu-id="95167-107">Il mapper MIDI è parte del software di sistema.</span><span class="sxs-lookup"><span data-stu-id="95167-107">The MIDI Mapper is part of the system software.</span></span> <span data-ttu-id="95167-108">Nella figura seguente viene illustrato il modo in cui il mapper MIDI si riferisce ad altri elementi dei servizi audio.</span><span class="sxs-lookup"><span data-stu-id="95167-108">The following illustration shows how the MIDI Mapper relates to other elements of the audio services.</span></span>

![relazione tra il mapper MIDI e altri elementi dell'immagine dei servizi audio](images/mmap-a01.gif)

<span data-ttu-id="95167-110">Dal punto di vista di un'applicazione, il mapper MIDI si presenta come un altro dispositivo di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="95167-110">From the viewpoint of an application, the MIDI Mapper looks like another MIDI output device.</span></span> <span data-ttu-id="95167-111">Il mapper MIDI riceve i messaggi inviati dalle funzioni di output MIDI di basso livello [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) e [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span><span class="sxs-lookup"><span data-stu-id="95167-111">The MIDI Mapper receives messages sent to it by the low-level MIDI output functions [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) and [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span></span> <span data-ttu-id="95167-112">Il mapper MIDI modifica questi messaggi e li reindirizza a un dispositivo di output MIDI in base alla mappa di configurazione MIDI corrente.</span><span class="sxs-lookup"><span data-stu-id="95167-112">The MIDI Mapper modifies these messages and redirects them to a MIDI output device according to the current MIDI setup map.</span></span> <span data-ttu-id="95167-113">La mappa di installazione MIDI corrente viene selezionata dall'utente tramite l'opzione pannello di controllo MIDI.</span><span class="sxs-lookup"><span data-stu-id="95167-113">The current MIDI setup map is selected by the user by means of the MIDI Control Panel option.</span></span> <span data-ttu-id="95167-114">Solo l'utente può selezionare la mappa di installazione corrente. le applicazioni non possono modificare la mappa di installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="95167-114">Only the user can select the current setup map; applications cannot change the current setup map.</span></span>

 

 