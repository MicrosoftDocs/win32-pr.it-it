---
title: Ricezione di messaggi di Running-Status
description: Ricezione di messaggi di Running-Status
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- MIDI (Musical Instrument Digital Interface), stato di esecuzione
- MIDI (Musical Instrument Digital Interface), stato di esecuzione
- registrazione audio MIDI, stato di esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4d12a19f525a6fa673747063774bf4507d65b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395382"
---
# <a name="receiving-running-status-messages"></a><span data-ttu-id="f8dd2-106">Ricezione di messaggi di Running-Status</span><span class="sxs-lookup"><span data-stu-id="f8dd2-106">Receiving Running-Status Messages</span></span>

<span data-ttu-id="f8dd2-107">La specifica dei *file MIDI Standard 1,0* consente di utilizzare *lo stato di esecuzione* quando un messaggio ha lo stesso byte di stato del messaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="f8dd2-107">The *Standard MIDI Files 1.0* specification allows the use of *running status* when a message has the same status byte as the previous message.</span></span> <span data-ttu-id="f8dd2-108">Quando si utilizza lo stato di esecuzione, il byte di stato dei messaggi successivi può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="f8dd2-108">When running status is used, the status byte of subsequent messages can be omitted.</span></span> <span data-ttu-id="f8dd2-109">Tutti i driver di dispositivo di input MIDI sono necessari per espandere i messaggi utilizzando lo stato di esecuzione in messaggi completi, in modo da ricevere sempre messaggi MIDI completi da un driver di dispositivo di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="f8dd2-109">All MIDI input device drivers are required to expand messages using running status into complete messages, so that you always receive complete MIDI messages from a MIDI input device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8dd2-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8dd2-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8dd2-111">Registrazione audio MIDI</span><span class="sxs-lookup"><span data-stu-id="f8dd2-111">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 




