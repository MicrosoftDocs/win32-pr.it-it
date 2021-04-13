---
title: Ricezione di Time-Stamped messaggi MIDI
description: Ricezione di Time-Stamped messaggi MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- MIDI (Musical Instrument Digital Interface), messaggi con timestamp
- MIDI (Musical Instrument Digital Interface), messaggi con timestamp
- registrazione audio MIDI, messaggi con timestamp
- messaggi MIDI con timestamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337111"
---
# <a name="receiving-time-stamped-midi-messages"></a><span data-ttu-id="401e5-107">Ricezione di Time-Stamped messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="401e5-107">Receiving Time-Stamped MIDI Messages</span></span>

<span data-ttu-id="401e5-108">A causa del ritardo che intercorre tra la ricezione di un messaggio MIDI da parte del driver di dispositivo e il momento in cui l'applicazione riceve il messaggio, i driver del dispositivo di input MIDI contrassegnano il messaggio MIDI con l'ora in cui il messaggio è stato ricevuto.</span><span class="sxs-lookup"><span data-stu-id="401e5-108">Because of the delay between when the device driver receives a MIDI message and the time the application receives the message, MIDI input device drivers time stamp the MIDI message with the time that the message was received.</span></span> <span data-ttu-id="401e5-109">I timestamp MIDI, definiti come l'ora in cui è stato ricevuto il primo byte del messaggio, vengono specificati in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="401e5-109">MIDI time stamps, which are defined as the time the first byte of the message was received, are specified in milliseconds.</span></span> <span data-ttu-id="401e5-110">La funzione [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) Reimposta il timestamp di un dispositivo su zero.</span><span class="sxs-lookup"><span data-stu-id="401e5-110">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function resets the time stamps for a device to zero.</span></span>

<span data-ttu-id="401e5-111">Come indicato in precedenza, per ricevere timestamp con input MIDI, è necessario usare una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="401e5-111">As stated previously, to receive time stamps with MIDI input, you must use a callback function.</span></span> <span data-ttu-id="401e5-112">Il parametro *dwParam2* della funzione di callback specifica il timestamp per i dati associati ai [**\_ dati MIM**](mim-data.md) e ai messaggi [**\_ LONGDATA MIM**](mim-longdata.md) .</span><span class="sxs-lookup"><span data-stu-id="401e5-112">The *dwParam2* parameter of the callback function specifies the time stamp for data associated with the [**MIM\_DATA**](mim-data.md) and [**MIM\_LONGDATA**](mim-longdata.md) messages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="401e5-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="401e5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="401e5-114">Registrazione audio MIDI</span><span class="sxs-lookup"><span data-stu-id="401e5-114">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 