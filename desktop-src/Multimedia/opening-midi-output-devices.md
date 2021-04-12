---
title: Apertura di dispositivi di output MIDI
description: Apertura di dispositivi di output MIDI
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- MIDI (Musical Instrument Digital Interface), dispositivi di output
- MIDI (Musical Instrument Digital Interface), dispositivi di output
- riproduzione di file MIDI, dispositivi di output
- Dispositivi di output MIDI
- MIDI (Musical Instrument Digital Interface), apertura di dispositivi di output
- MIDI (Musical Instrument Digital Interface), apertura di dispositivi di output
- riproduzione di file MIDI, apertura di dispositivi di output
- apertura di dispositivi di output MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca7a7e1db461b29700ec7c7c61ee140073bc345
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472963"
---
# <a name="opening-midi-output-devices"></a><span data-ttu-id="c2263-111">Apertura di dispositivi di output MIDI</span><span class="sxs-lookup"><span data-stu-id="c2263-111">Opening MIDI Output Devices</span></span>

<span data-ttu-id="c2263-112">Per aprire un dispositivo di output MIDI per la riproduzione, usare la funzione [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="c2263-112">To open a MIDI output device for playback, use the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="c2263-113">Questa funzione apre il dispositivo associato all'identificatore di dispositivo specificato e restituisce un handle del dispositivo aperto scrivendo l'handle in una posizione di memoria specificata.</span><span class="sxs-lookup"><span data-stu-id="c2263-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="c2263-114">Uno dei parametri di **midiOutOpen** è un valore parola doppia.</span><span class="sxs-lookup"><span data-stu-id="c2263-114">One of the parameters of **midiOutOpen** is a doubleword value.</span></span> <span data-ttu-id="c2263-115">Questo valore specifica un handle di finestra o di thread, un handle di evento o l'indirizzo di una funzione di callback utilizzata per monitorare lo stato di avanzamento della riproduzione dei dati esclusivi del sistema MIDI e dei buffer di flusso.</span><span class="sxs-lookup"><span data-stu-id="c2263-115">This value specifies a window or thread handle, an event handle, or the address of a callback function that is used to monitor the progress of the playback of MIDI system-exclusive data and stream buffers.</span></span> <span data-ttu-id="c2263-116">Il monitoraggio consente all'applicazione di determinare quando inviare blocchi di dati aggiuntivi e quando liberare i blocchi di dati che sono stati inviati.</span><span class="sxs-lookup"><span data-stu-id="c2263-116">Monitoring enables the application to determine when to send additional data blocks and when to free data blocks that have been sent.</span></span> <span data-ttu-id="c2263-117">Per altre informazioni su questi metodi, vedere [Managing MIDI Data blocks](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="c2263-117">For more information about these methods, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 