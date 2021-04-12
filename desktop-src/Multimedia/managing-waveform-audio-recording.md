---
title: Gestione della registrazione di Waveform-Audio
description: Gestione della registrazione di Waveform-Audio
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- audio Waveform, registrazione
- waveform-interfaccia audio, registrazione
- registrazione dell'audio della forma d'onda, informazioni
- Struttura WAVEHDR
- waveInAddBuffer (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336991"
---
# <a name="managing-waveform-audio-recording"></a><span data-ttu-id="e33c4-108">Gestione della registrazione di Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="e33c4-108">Managing Waveform-Audio Recording</span></span>

<span data-ttu-id="e33c4-109">Dopo aver aperto un dispositivo di input audio e di forma d'onda, è possibile iniziare la registrazione dei dati audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="e33c4-109">After you open a waveform-audio input device, you can begin recording waveform-audio data.</span></span> <span data-ttu-id="e33c4-110">Forma d'onda: i dati audio vengono registrati nei buffer forniti dall'applicazione specificati da una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) .</span><span class="sxs-lookup"><span data-stu-id="e33c4-110">Waveform-audio data is recorded into application-supplied buffers specified by a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure.</span></span> <span data-ttu-id="e33c4-111">È necessario preparare questi blocchi di dati prima di utilizzarli; Per ulteriori informazioni, vedere la pagina relativa ai [blocchi di dati audio](audio-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="e33c4-111">These data blocks must be prepared before they are used; for more information, see [Audio Data Blocks](audio-data-blocks.md).</span></span>

<span data-ttu-id="e33c4-112">Windows fornisce le funzioni seguenti per gestire la registrazione audio e la forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="e33c4-112">Windows provides the following functions to manage waveform-audio recording.</span></span>



| <span data-ttu-id="e33c4-113">Funzione</span><span class="sxs-lookup"><span data-stu-id="e33c4-113">Function</span></span>                                   | <span data-ttu-id="e33c4-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e33c4-114">Description</span></span>                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e33c4-115">**waveInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="e33c4-115">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | <span data-ttu-id="e33c4-116">Invia un buffer al driver di dispositivo in modo che possa essere riempito con i dati audio della forma d'onda registrati.</span><span class="sxs-lookup"><span data-stu-id="e33c4-116">Sends a buffer to the device driver so it can be filled with recorded waveform-audio data.</span></span> |
| [<span data-ttu-id="e33c4-117">**waveInReset**</span><span class="sxs-lookup"><span data-stu-id="e33c4-117">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | <span data-ttu-id="e33c4-118">Arresta la registrazione audio e di forma d'onda e contrassegna tutti i buffer in sospeso come completato.</span><span class="sxs-lookup"><span data-stu-id="e33c4-118">Stops waveform-audio recording and marks all pending buffers as done.</span></span>                      |
| [<span data-ttu-id="e33c4-119">**waveInStart**</span><span class="sxs-lookup"><span data-stu-id="e33c4-119">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | <span data-ttu-id="e33c4-120">Avvia la registrazione audio e la forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="e33c4-120">Starts waveform-audio recording.</span></span>                                                           |
| [<span data-ttu-id="e33c4-121">**waveInStop**</span><span class="sxs-lookup"><span data-stu-id="e33c4-121">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | <span data-ttu-id="e33c4-122">Arresta la registrazione audio e la forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="e33c4-122">Stops waveform-audio recording.</span></span>                                                            |



 

<span data-ttu-id="e33c4-123">Usare la funzione [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) per inviare i buffer al driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e33c4-123">Use the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function to send buffers to the device driver.</span></span> <span data-ttu-id="e33c4-124">Quando i buffer sono riempiti con dati audio e di forma d'onda registrati, l'applicazione riceve una notifica con un messaggio di finestra, un messaggio di callback, un messaggio di thread o un evento, a seconda del flag specificato quando il dispositivo è stato aperto.</span><span class="sxs-lookup"><span data-stu-id="e33c4-124">As the buffers are filled with recorded waveform-audio data, the application is notified with a window message, callback message, thread message, or event, depending on the flag specified when the device was opened.</span></span>

<span data-ttu-id="e33c4-125">Prima di iniziare la registrazione tramite [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), è necessario inviare almeno un buffer al driver oppure i dati in arrivo potrebbero andare persi.</span><span class="sxs-lookup"><span data-stu-id="e33c4-125">Before you begin recording by using [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), you should send at least one buffer to the driver, or incoming data could be lost.</span></span>

<span data-ttu-id="e33c4-126">Prima di chiudere il dispositivo usando [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), chiamare [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) per contrassegnare eventuali blocchi di dati in sospeso come eseguiti.</span><span class="sxs-lookup"><span data-stu-id="e33c4-126">Before closing the device using [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), call [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) to mark any pending data blocks as being done.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e33c4-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e33c4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e33c4-128">Registrazione dell'audio della forma d'onda</span><span class="sxs-lookup"><span data-stu-id="e33c4-128">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 