---
title: Blocchi di dati audio
description: Blocchi di dati audio
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- audio multimediale, blocchi di dati
- audio, blocchi di dati
- audio Waveform, blocchi di dati
- blocchi di dati audio, informazioni
- Struttura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956383"
---
# <a name="audio-data-blocks"></a><span data-ttu-id="59182-108">Blocchi di dati audio</span><span class="sxs-lookup"><span data-stu-id="59182-108">Audio Data Blocks</span></span>

<span data-ttu-id="59182-109">Per le funzioni [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) e [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) è necessario che le applicazioni allochino i blocchi di dati da passare ai driver di dispositivo a scopo di registrazione o riproduzione.</span><span class="sxs-lookup"><span data-stu-id="59182-109">The [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) and [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) functions require applications to allocate data blocks to pass to the device drivers for recording or playback purposes.</span></span> <span data-ttu-id="59182-110">Entrambe queste funzioni usano la struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) per descrivere il relativo blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="59182-110">Both of these functions use the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to describe its data block.</span></span>

<span data-ttu-id="59182-111">Prima di usare una di queste funzioni per passare un blocco di dati a un driver di dispositivo, è necessario allocare memoria per il blocco di dati e la struttura di intestazione che descrive il blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="59182-111">Before using one of these functions to pass a data block to a device driver, you must allocate memory for the data block and the header structure that describes the data block.</span></span> <span data-ttu-id="59182-112">È possibile preparare e non preparare le intestazioni usando le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="59182-112">The headers can be prepared and unprepared by using the following functions.</span></span>



| <span data-ttu-id="59182-113">Funzione</span><span class="sxs-lookup"><span data-stu-id="59182-113">Function</span></span>                                                 | <span data-ttu-id="59182-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59182-114">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="59182-115">**waveInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="59182-115">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | <span data-ttu-id="59182-116">Prepara un blocco di dati di input audio e di forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="59182-116">Prepares a waveform-audio input data block.</span></span>                      |
| [<span data-ttu-id="59182-117">**waveInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="59182-117">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | <span data-ttu-id="59182-118">Pulisce la preparazione in un blocco di dati di input audio e di forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="59182-118">Cleans up the preparation on a waveform-audio input data block.</span></span>  |
| [<span data-ttu-id="59182-119">**waveOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="59182-119">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | <span data-ttu-id="59182-120">Prepara un blocco di dati di output dell'audio e della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="59182-120">Prepares a waveform-audio output data block.</span></span>                     |
| [<span data-ttu-id="59182-121">**waveOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="59182-121">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | <span data-ttu-id="59182-122">Pulisce la preparazione in un blocco di dati di output dell'audio e della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="59182-122">Cleans up the preparation on a waveform-audio output data block.</span></span> |



 

<span data-ttu-id="59182-123">Prima di passare un blocco di dati audio a un driver di dispositivo, è necessario preparare il blocco di dati passandolo a [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) o [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span><span class="sxs-lookup"><span data-stu-id="59182-123">Before you pass an audio data block to a device driver, you must prepare the data block by passing it to either [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) or [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span></span> <span data-ttu-id="59182-124">Quando il driver di dispositivo è terminato con il blocco di dati e lo restituisce, è necessario pulire la preparazione passando il blocco di dati a [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) o [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) prima di poter liberare la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="59182-124">When the device driver is finished with the data block and returns it, you must clean up this preparation by passing the data block to either [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) or [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) before any allocated memory can be freed.</span></span>

<span data-ttu-id="59182-125">A meno che i dati di input e di output della forma d'onda non siano sufficientemente piccoli da essere contenuti in un singolo blocco di dati, le applicazioni devono fornire continuamente al driver di dispositivo i blocchi di dati fino al completamento della riproduzione o della registrazione.</span><span class="sxs-lookup"><span data-stu-id="59182-125">Unless the waveform-audio input and output data is small enough to be contained in a single data block, applications must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="59182-126">Anche se viene utilizzato un singolo blocco di dati, un'applicazione deve essere in grado di determinare quando un driver di dispositivo è terminato con il blocco di dati, in modo che l'applicazione possa liberare la memoria associata al blocco di dati e alla struttura dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="59182-126">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so the application can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="59182-127">Esistono diversi modi per determinare quando un driver di dispositivo è terminato con un blocco di dati:</span><span class="sxs-lookup"><span data-stu-id="59182-127">There are several ways to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="59182-128">Specificando una funzione di callback per ricevere un messaggio inviato dal driver al termine di un blocco di dati</span><span class="sxs-lookup"><span data-stu-id="59182-128">By specifying a callback function to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="59182-129">Utilizzando un callback di evento</span><span class="sxs-lookup"><span data-stu-id="59182-129">By using an event callback</span></span>
-   <span data-ttu-id="59182-130">Specificando una finestra o un thread per ricevere un messaggio inviato dal driver al termine di un blocco di dati</span><span class="sxs-lookup"><span data-stu-id="59182-130">By specifying a window or thread to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="59182-131">Eseguendo il polling del \_ bit WHDR eseguito nel membro **dwFlags** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) inviata con ogni blocco di dati</span><span class="sxs-lookup"><span data-stu-id="59182-131">By polling the WHDR\_DONE bit in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure sent with each data block</span></span>

<span data-ttu-id="59182-132">Se un'applicazione non ottiene un blocco di dati al driver di dispositivo quando necessario, potrebbe verificarsi una lacuna udibile nella riproduzione o una perdita di informazioni registrate in entrata.</span><span class="sxs-lookup"><span data-stu-id="59182-132">If an application does not get a data block to the device driver when needed, there can be an audible gap in playback or a loss of incoming recorded information.</span></span> <span data-ttu-id="59182-133">Questa operazione richiede almeno uno schema a doppio buffer, rimanendo almeno un blocco di dati prima del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59182-133">This requires at least a double-buffering scheme — staying at least one data block ahead of the device driver.</span></span>

<span data-ttu-id="59182-134">Negli argomenti seguenti vengono descritti i modi per determinare quando un driver di dispositivo è terminato con un blocco di dati:</span><span class="sxs-lookup"><span data-stu-id="59182-134">The following topics describe ways to determine when a device driver is finished with a data block:</span></span>

<span data-ttu-id="59182-135">Utilizzo di una funzione di callback per elaborare i messaggi del driver</span><span class="sxs-lookup"><span data-stu-id="59182-135">Using a Callback Function to Process Driver Messages</span></span>

-   [<span data-ttu-id="59182-136">Utilizzo di una funzione di callback per elaborare i messaggi del driver</span><span class="sxs-lookup"><span data-stu-id="59182-136">Using a Callback Function to Process Driver Messages</span></span>](using-a-callback-function-to-process-driver-messages.md)
-   [<span data-ttu-id="59182-137">Utilizzo di un callback di evento per elaborare i messaggi del driver</span><span class="sxs-lookup"><span data-stu-id="59182-137">Using an Event Callback to Process Driver Messages</span></span>](using-an-callback-to-process-driver-messages.md)
-   [<span data-ttu-id="59182-138">Uso di una finestra o di un thread per elaborare i messaggi dei driver</span><span class="sxs-lookup"><span data-stu-id="59182-138">Using a Window or Thread to Process Driver Messages</span></span>](using-a-window-or-thread-to-process-driver-messages.md)
-   [<span data-ttu-id="59182-139">Gestione dei blocchi di dati tramite polling</span><span class="sxs-lookup"><span data-stu-id="59182-139">Managing Data Blocks by Polling</span></span>](managing-data-blocks-by-polling.md)

 

 