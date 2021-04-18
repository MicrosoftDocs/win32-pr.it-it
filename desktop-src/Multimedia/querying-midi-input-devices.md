---
title: Esecuzione di query sui dispositivi di input MIDI
description: Esecuzione di query sui dispositivi di input MIDI
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- MIDI (Musical Instrument Digital Interface), dispositivi di input
- MIDI (Musical Instrument Digital Interface), dispositivi di input
- registrazione audio MIDI, dispositivi di input
- Dispositivi di input MIDI
- MIDI (Musical Instrument Digital Interface), esecuzione di query sui dispositivi di input
- MIDI (Musical Instrument Digital Interface), esecuzione di query sui dispositivi di input
- registrazione dell'audio MIDI, esecuzione di query sui dispositivi di input
- esecuzione di query sui dispositivi di input MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a92bec8733887e20c25f37d1de3dd493e555c8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299714"
---
# <a name="querying-midi-input-devices"></a><span data-ttu-id="9db93-111">Esecuzione di query sui dispositivi di input MIDI</span><span class="sxs-lookup"><span data-stu-id="9db93-111">Querying MIDI Input Devices</span></span>

<span data-ttu-id="9db93-112">Prima di registrare l'audio MIDI, è necessario usare la funzione [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) per determinare le funzionalità del dispositivo di input MIDI presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="9db93-112">Before recording MIDI audio, you should use the [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) function to determine the capabilities of the MIDI input device that is present in the system.</span></span> <span data-ttu-id="9db93-113">Questa funzione accetta un indirizzo di una struttura [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) , che compila con informazioni sulle funzionalità del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="9db93-113">This function takes an address of a [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure, which it fills with information about the capabilities of the given device.</span></span> <span data-ttu-id="9db93-114">Queste informazioni includono gli identificatori del produttore e del prodotto, il nome del prodotto per il dispositivo e il numero di versione del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9db93-114">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9db93-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9db93-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9db93-116">Registrazione audio MIDI</span><span class="sxs-lookup"><span data-stu-id="9db93-116">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 