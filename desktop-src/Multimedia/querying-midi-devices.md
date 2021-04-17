---
title: Esecuzione di query sui dispositivi MIDI
description: Esecuzione di query sui dispositivi MIDI
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- MIDI (Musical Instrument Digital Interface), esecuzione di query sui dispositivi
- MIDI (Musical Instrument Digital Interface), esecuzione di query sui dispositivi
- Servizi MIDI, esecuzione di query sui dispositivi
- esecuzione di query sui dispositivi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398891"
---
# <a name="querying-midi-devices"></a><span data-ttu-id="c7871-107">Esecuzione di query sui dispositivi MIDI</span><span class="sxs-lookup"><span data-stu-id="c7871-107">Querying MIDI Devices</span></span>

<span data-ttu-id="c7871-108">Prima di riprodurre o registrare i dati MIDI, è necessario determinare le funzionalità dell'hardware MIDI presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c7871-108">Before playing or recording MIDI data, you must determine the capabilities of the MIDI hardware present in the system.</span></span> <span data-ttu-id="c7871-109">La funzionalità MIDI può variare da un computer multimediale a quello successivo. le applicazioni non devono creare presupposti sull'hardware presente in un sistema specifico.</span><span class="sxs-lookup"><span data-stu-id="c7871-109">MIDI capability can vary from one multimedia computer to the next; applications should not make assumptions about the hardware present in a given system.</span></span>

<span data-ttu-id="c7871-110">Windows fornisce le funzioni seguenti per determinare il numero di dispositivi MIDI disponibili per l'input o l'output in un determinato sistema.</span><span class="sxs-lookup"><span data-stu-id="c7871-110">Windows provides the following functions to determine how many MIDI devices are available for input or output in a given system.</span></span>



| <span data-ttu-id="c7871-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c7871-111">Value</span></span>                                          | <span data-ttu-id="c7871-112">Significato</span><span class="sxs-lookup"><span data-stu-id="c7871-112">Meaning</span></span>                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="c7871-113">**midiInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="c7871-113">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | <span data-ttu-id="c7871-114">Recupera il numero di dispositivi di input MIDI presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c7871-114">Retrieves the number of MIDI input devices present in the system.</span></span>  |
| [<span data-ttu-id="c7871-115">**midiOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="c7871-115">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | <span data-ttu-id="c7871-116">Recupera il numero di dispositivi di output MIDI presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c7871-116">Retrieves the number of MIDI output devices present in the system.</span></span> |



 

<span data-ttu-id="c7871-117">Analogamente ad altri dispositivi audio, i dispositivi MIDI sono identificati da un identificatore di dispositivo, determinato in modo implicito dal numero di dispositivi presenti in un determinato sistema.</span><span class="sxs-lookup"><span data-stu-id="c7871-117">Like other audio devices, MIDI devices are identified by a device identifier, which is determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="c7871-118">Gli identificatori di dispositivo sono compresi tra zero e il numero di dispositivi presenti, meno uno.</span><span class="sxs-lookup"><span data-stu-id="c7871-118">Device identifiers range from zero to the number of devices present, minus one.</span></span> <span data-ttu-id="c7871-119">Se ad esempio sono presenti due dispositivi di output MIDI in un sistema, gli identificatori di dispositivo validi sono 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="c7871-119">For example, if there are two MIDI output devices in a system, valid device identifiers are 0 and 1.</span></span>

<span data-ttu-id="c7871-120">Dopo aver determinato il numero di dispositivi di input o output MIDI presenti in un sistema, è possibile richiedere informazioni sulle funzionalità di ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7871-120">After you determine how many MIDI input or output devices are present in a system, you can inquire about the capabilities of each device.</span></span> <span data-ttu-id="c7871-121">Windows fornisce le funzioni seguenti per determinare le funzionalità dei dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="c7871-121">Windows provides the following functions to determine the capabilities of audio devices.</span></span>



| <span data-ttu-id="c7871-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c7871-122">Value</span></span>                                          | <span data-ttu-id="c7871-123">Significato</span><span class="sxs-lookup"><span data-stu-id="c7871-123">Meaning</span></span>                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7871-124">**midiInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="c7871-124">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | <span data-ttu-id="c7871-125">Recupera le funzionalità di un determinato dispositivo di input MIDI e inserisce queste informazioni nella struttura [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) .</span><span class="sxs-lookup"><span data-stu-id="c7871-125">Retrieves the capabilities of a given MIDI input device and places this information in the [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure.</span></span>    |
| [<span data-ttu-id="c7871-126">**midiOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="c7871-126">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | <span data-ttu-id="c7871-127">Recupera le funzionalità di un dispositivo di output MIDI specificato e inserisce queste informazioni nella struttura [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) .</span><span class="sxs-lookup"><span data-stu-id="c7871-127">Retrieves the capabilities of a given MIDI output device and places this information in the [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) structure.</span></span> |



 

<span data-ttu-id="c7871-128">Ognuna di queste funzioni include un parametro che specifica l'indirizzo di una struttura che la funzione compila con informazioni sulle funzionalità di un dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="c7871-128">Each of these functions has a parameter specifying the address of a structure that the function fills with information about the capabilities of a specified device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7871-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7871-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7871-130">Servizi MIDI</span><span class="sxs-lookup"><span data-stu-id="c7871-130">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 