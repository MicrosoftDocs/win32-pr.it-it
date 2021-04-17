---
title: Gestione degli errori con le funzioni MIDI
description: Gestione degli errori con le funzioni MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- MIDI (Musical Instrument Digital Interface), errori
- MIDI (Musical Instrument Digital Interface), errori
- Servizi MIDI, errori
- Errori MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299812"
---
# <a name="handling-errors-with-midi-functions"></a><span data-ttu-id="48469-107">Gestione degli errori con le funzioni MIDI</span><span class="sxs-lookup"><span data-stu-id="48469-107">Handling Errors with MIDI Functions</span></span>

<span data-ttu-id="48469-108">Le funzioni audio MIDI restituiscono un codice di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="48469-108">MIDI audio functions return a nonzero error code.</span></span> <span data-ttu-id="48469-109">Per gli errori associati a MIDI, le funzioni [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) e [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) recuperano le descrizioni testuali per i codici di errore.</span><span class="sxs-lookup"><span data-stu-id="48469-109">For MIDI-associated errors, the [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) and [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) functions retrieve textual descriptions for the error codes.</span></span> <span data-ttu-id="48469-110">L'applicazione deve comunque esaminare il valore di errore stesso per determinare il modo in cui procedere, ma può utilizzare le descrizioni degli errori nelle finestre di dialogo per informare gli utenti delle condizioni di errore.</span><span class="sxs-lookup"><span data-stu-id="48469-110">The application must still look at the error value itself to determine how to proceed, but it can use the error descriptions in dialog boxes to inform users of the error conditions.</span></span>

<span data-ttu-id="48469-111">Le uniche funzioni MIDI che non restituiscono codici di errore sono le funzioni [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) e [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="48469-111">The only MIDI functions that do not return error codes are the [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) and [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) functions.</span></span> <span data-ttu-id="48469-112">Queste funzioni restituiscono un valore pari a zero se non sono presenti dispositivi in un sistema o se vengono rilevati errori dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="48469-112">These functions return a value of zero if no devices are present in a system or if any errors are encountered by the function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48469-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48469-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48469-114">Servizi MIDI</span><span class="sxs-lookup"><span data-stu-id="48469-114">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 