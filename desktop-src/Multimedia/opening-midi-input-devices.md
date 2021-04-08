---
title: Apertura di dispositivi di input MIDI
description: Apertura di dispositivi di input MIDI
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- MIDI (Musical Instrument Digital Interface), dispositivi di input
- MIDI (Musical Instrument Digital Interface), dispositivi di input
- registrazione audio MIDI, dispositivi di input
- Dispositivi di input MIDI
- MIDI (Musical Instrument Digital Interface), apertura di dispositivi di input
- MIDI (Musical Instrument Digital Interface), apertura di dispositivi di input
- registrazione audio MIDI, apertura di dispositivi di input
- apertura di dispositivi di input MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726319"
---
# <a name="opening-midi-input-devices"></a><span data-ttu-id="f0dff-111">Apertura di dispositivi di input MIDI</span><span class="sxs-lookup"><span data-stu-id="f0dff-111">Opening MIDI Input Devices</span></span>

<span data-ttu-id="f0dff-112">Per aprire un dispositivo di input MIDI per la registrazione, usare la funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="f0dff-112">To open a MIDI input device for recording, use the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span> <span data-ttu-id="f0dff-113">Questa funzione apre il dispositivo associato all'identificatore di dispositivo specificato e restituisce un handle del dispositivo aperto scrivendo l'handle in una posizione di memoria specificata.</span><span class="sxs-lookup"><span data-stu-id="f0dff-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="f0dff-114">Se si usa il flag di stato i/ \_ \_ o MIDI con **midiInOpen**, il sistema usa il messaggio [**\_ MOREDATA MIM**](mim-moredata.md) per avvisare la funzione di callback dell'applicazione quando non elabora i dati MIDI in modo sufficientemente veloce da restare al passo con il driver di dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="f0dff-114">If you use the MIDI\_IO\_STATUS flag with **midiInOpen**, the system uses the [**MIM\_MOREDATA**](mim-moredata.md) message to alert your application's callback function when it is not processing MIDI data fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="f0dff-115">Il messaggio [**\_ \_ MOREDATA in mm MIM**](mm-mim-moredata.md) esegue lo stesso processo con callback di finestra.</span><span class="sxs-lookup"><span data-stu-id="f0dff-115">(The [**MM\_MIM\_MOREDATA**](mm-mim-moredata.md) message does the same job with window callbacks.</span></span> <span data-ttu-id="f0dff-116">Tuttavia, per motivi di prestazioni, la maggior parte delle applicazioni utilizzerà funzioni di callback anziché callback di finestra. Se l'applicazione elabora i dati MIDI in un thread separato, l'aumento della priorità del thread può avere un impatto significativo sulla capacità dell'applicazione di rimanere al passo con il flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="f0dff-116">However, for performance reasons, most applications will use callback functions instead of window callbacks.) If your application processes MIDI data in a separate thread, boosting the thread's priority can have a significant impact on the application's ability to keep up with the data flow.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0dff-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0dff-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0dff-118">Registrazione audio MIDI</span><span class="sxs-lookup"><span data-stu-id="f0dff-118">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 