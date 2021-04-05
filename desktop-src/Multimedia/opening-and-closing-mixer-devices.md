---
title: Apertura e chiusura di dispositivi mixer
description: Apertura e chiusura di dispositivi mixer
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- audio multimediale, apertura di dispositivi mixer
- audio, apertura di dispositivi mixer
- mixer audio, apertura
- mixer, apertura
- audio multimediale, chiusura di dispositivi mixer
- audio, chiusura di dispositivi mixer
- mixer audio, chiusura
- mixer, chiusura
- apertura di dispositivi mixer
- chiusura di dispositivi mixer
- identificatori di dispositivo e handle del dispositivo
- mixer audio, identificatori di dispositivo e handle del dispositivo
- mixer, identificatori di dispositivo e handle del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046592"
---
# <a name="opening-and-closing-mixer-devices"></a><span data-ttu-id="398f4-116">Apertura e chiusura di dispositivi mixer</span><span class="sxs-lookup"><span data-stu-id="398f4-116">Opening and Closing Mixer Devices</span></span>

<span data-ttu-id="398f4-117">Quando si vuole usare un dispositivo mixer, è sufficiente iniziare a usarlo oppure è possibile aprire il dispositivo in modo esplicito prima di usarlo.</span><span class="sxs-lookup"><span data-stu-id="398f4-117">When you want to use a mixer device, you can either simply begin using it or you can explicitly open the device before using it.</span></span> <span data-ttu-id="398f4-118">L'apertura esplicita di un dispositivo mixer offre due vantaggi principali:</span><span class="sxs-lookup"><span data-stu-id="398f4-118">Explicitly opening a mixer device offers two main benefits:</span></span>

-   <span data-ttu-id="398f4-119">Garantisce la continua esistenza del dispositivo mixer.</span><span class="sxs-lookup"><span data-stu-id="398f4-119">It guarantees the continued existence of that mixer device.</span></span>
-   <span data-ttu-id="398f4-120">Consente di ricevere la notifica delle modifiche della riga audio e del controllo.</span><span class="sxs-lookup"><span data-stu-id="398f4-120">It lets you receive notification of audio line and control changes.</span></span>

<span data-ttu-id="398f4-121">È possibile usare la funzione [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) per aprire in modo esplicito un dispositivo mixer.</span><span class="sxs-lookup"><span data-stu-id="398f4-121">You can use the [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) function to explicitly open a mixer device.</span></span> <span data-ttu-id="398f4-122">Questa funzione accetta come parametri un identificatore di dispositivo, un puntatore a una posizione di memoria e altri valori univoci per ogni tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="398f4-122">This function takes as parameters a device identifier, a pointer to a memory location, and other values unique to each type of device.</span></span> <span data-ttu-id="398f4-123">La posizione di memoria viene riempita con un handle di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="398f4-123">The memory location is filled with a device handle.</span></span> <span data-ttu-id="398f4-124">Usare questo handle di dispositivo per identificare il dispositivo mixer aperto quando si chiamano altre funzioni del mixer audio.</span><span class="sxs-lookup"><span data-stu-id="398f4-124">Use this device handle to identify the open mixer device when calling other audio mixer functions.</span></span> <span data-ttu-id="398f4-125">Fino a quando un handle di un dispositivo mixer esiste, il dispositivo continua a esistere nel sistema.</span><span class="sxs-lookup"><span data-stu-id="398f4-125">As long as a handle of a mixer device exists, the device continues to exist in the system.</span></span> <span data-ttu-id="398f4-126">Se viene apportata una modifica alla configurazione del dispositivo mixer e non è stata aperta in modo esplicito, l'applicazione potrebbe non essere in grado di accedervi improvvisamente.</span><span class="sxs-lookup"><span data-stu-id="398f4-126">If a configuration change occurs to the mixer device and it hasn't been explicitly opened, your application might suddenly be unable to access it.</span></span>

> [!Note]  
> <span data-ttu-id="398f4-127">La differenza tra gli identificatori di dispositivo e gli handle del dispositivo è importante.</span><span class="sxs-lookup"><span data-stu-id="398f4-127">The difference between device identifiers and device handles is important.</span></span> <span data-ttu-id="398f4-128">Gli handle di dispositivo vengono restituiti quando si apre un driver di dispositivo usando **mixerOpen**.</span><span class="sxs-lookup"><span data-stu-id="398f4-128">Device handles are returned when you open a device driver by using **mixerOpen**.</span></span> <span data-ttu-id="398f4-129">Gli identificatori di dispositivo sono determinati in modo implicito dal numero di dispositivi presenti in un sistema; Questo numero viene ottenuto tramite la funzione [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="398f4-129">Device identifiers are determined implicitly from the number of devices present in a system; this number is obtained by using the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function.</span></span>

 

<span data-ttu-id="398f4-130">Per chiudere un dispositivo mixer, è possibile usare la funzione [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) .</span><span class="sxs-lookup"><span data-stu-id="398f4-130">You can use the [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) function to close a mixer device.</span></span> <span data-ttu-id="398f4-131">Dopo aver completato l'uso, è necessario chiudere il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="398f4-131">You should close the device after you finish using it.</span></span>

 

 