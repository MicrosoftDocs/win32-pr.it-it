---
title: Tipi di dispositivi
description: Tipi di dispositivi
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712967"
---
# <a name="device-types"></a><span data-ttu-id="01b9f-103">Tipi di dispositivi</span><span class="sxs-lookup"><span data-stu-id="01b9f-103">Device Types</span></span>

<span data-ttu-id="01b9f-104">MCI riconosce un set di base di *tipi di dispositivi*.</span><span class="sxs-lookup"><span data-stu-id="01b9f-104">MCI recognizes a basic set of *device types*.</span></span> <span data-ttu-id="01b9f-105">Un tipo di dispositivo è un set di driver MCI che condividono un set di comandi comune e vengono usati per controllare dispositivi multimediali o file di dati simili.</span><span class="sxs-lookup"><span data-stu-id="01b9f-105">A device type is a set of MCI drivers that share a common command set and are used to control similar multimedia devices or data files.</span></span> <span data-ttu-id="01b9f-106">Molti comandi MCI, ad esempio [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)), richiedono di specificare un tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01b9f-106">Many MCI commands, such as [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)), require you to specify a device type.</span></span>

<span data-ttu-id="01b9f-107">Nella tabella seguente sono elencati i tipi di dispositivi definiti.</span><span class="sxs-lookup"><span data-stu-id="01b9f-107">The following table lists the defined device types.</span></span> <span data-ttu-id="01b9f-108">L'implementazione corrente di MCI include i set di comandi per un subset di questi dispositivi.</span><span class="sxs-lookup"><span data-stu-id="01b9f-108">The current implementation of MCI includes command sets for a subset of these devices.</span></span>



| <span data-ttu-id="01b9f-109">Tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="01b9f-109">Device type</span></span>      | <span data-ttu-id="01b9f-110">Costante</span><span class="sxs-lookup"><span data-stu-id="01b9f-110">Constant</span></span>                      | <span data-ttu-id="01b9f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01b9f-111">Description</span></span>                                      |
|------------------|-------------------------------|--------------------------------------------------|
| <span data-ttu-id="01b9f-112">**cdaudio**</span><span class="sxs-lookup"><span data-stu-id="01b9f-112">**cdaudio**</span></span>      | <span data-ttu-id="01b9f-113">\_ \_ audio CD DEVTYPE \_ MCI</span><span class="sxs-lookup"><span data-stu-id="01b9f-113">MCI\_DEVTYPE\_CD\_AUDIO</span></span>       | <span data-ttu-id="01b9f-114">Lettore audio CD</span><span class="sxs-lookup"><span data-stu-id="01b9f-114">CD audio player</span></span>                                  |
| <span data-ttu-id="01b9f-115">**dat**</span><span class="sxs-lookup"><span data-stu-id="01b9f-115">**dat**</span></span>          | <span data-ttu-id="01b9f-116">DEVTYPE di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="01b9f-116">MCI\_DEVTYPE\_DAT</span></span>             | <span data-ttu-id="01b9f-117">Lettore nastro digitale audio</span><span class="sxs-lookup"><span data-stu-id="01b9f-117">Digital-audio tape player</span></span>                        |
| <span data-ttu-id="01b9f-118">**digitalvideo**</span><span class="sxs-lookup"><span data-stu-id="01b9f-118">**digitalvideo**</span></span> | <span data-ttu-id="01b9f-119">\_ \_ video digitale MCI \_ DEVTYPE</span><span class="sxs-lookup"><span data-stu-id="01b9f-119">MCI\_DEVTYPE\_DIGITAL\_VIDEO</span></span>  | <span data-ttu-id="01b9f-120">Video digitale in una finestra (non basato su GDI)</span><span class="sxs-lookup"><span data-stu-id="01b9f-120">Digital video in a window (not GDI-based)</span></span>        |
| <span data-ttu-id="01b9f-121">**altri**</span><span class="sxs-lookup"><span data-stu-id="01b9f-121">**other**</span></span>        | <span data-ttu-id="01b9f-122">\_altri DEVTYPE \_ MCI</span><span class="sxs-lookup"><span data-stu-id="01b9f-122">MCI\_DEVTYPE\_OTHER</span></span>           | <span data-ttu-id="01b9f-123">Dispositivo MCI non definito</span><span class="sxs-lookup"><span data-stu-id="01b9f-123">Undefined MCI device</span></span>                             |
| <span data-ttu-id="01b9f-124">**sovrapposizione**</span><span class="sxs-lookup"><span data-stu-id="01b9f-124">**overlay**</span></span>      | <span data-ttu-id="01b9f-125">\_ \_ sovrimpressione DEVTYPE MCI</span><span class="sxs-lookup"><span data-stu-id="01b9f-125">MCI\_DEVTYPE\_OVERLAY</span></span>         | <span data-ttu-id="01b9f-126">Dispositivo overlay (video analogico in una finestra)</span><span class="sxs-lookup"><span data-stu-id="01b9f-126">Overlay device (analog video in a window)</span></span>        |
| <span data-ttu-id="01b9f-127">**scanner**</span><span class="sxs-lookup"><span data-stu-id="01b9f-127">**scanner**</span></span>      | <span data-ttu-id="01b9f-128">\_scanner DEVTYPE \_ MCI</span><span class="sxs-lookup"><span data-stu-id="01b9f-128">MCI\_DEVTYPE\_SCANNER</span></span>         | <span data-ttu-id="01b9f-129">Scanner immagini</span><span class="sxs-lookup"><span data-stu-id="01b9f-129">Image scanner</span></span>                                    |
| <span data-ttu-id="01b9f-130">**sequencer**</span><span class="sxs-lookup"><span data-stu-id="01b9f-130">**sequencer**</span></span>    | <span data-ttu-id="01b9f-131">\_ \_ sequencer DEVTYPE MCI</span><span class="sxs-lookup"><span data-stu-id="01b9f-131">MCI\_DEVTYPE\_SEQUENCER</span></span>       | <span data-ttu-id="01b9f-132">Sequencer MIDI</span><span class="sxs-lookup"><span data-stu-id="01b9f-132">MIDI sequencer</span></span>                                   |
| <span data-ttu-id="01b9f-133">**VCR**</span><span class="sxs-lookup"><span data-stu-id="01b9f-133">**vcr**</span></span>          | <span data-ttu-id="01b9f-134">\_VCR DEVTYPE \_ MCI</span><span class="sxs-lookup"><span data-stu-id="01b9f-134">MCI\_DEVTYPE\_VCR</span></span>             | <span data-ttu-id="01b9f-135">Registratore di cassette video o lettore</span><span class="sxs-lookup"><span data-stu-id="01b9f-135">Video-cassette recorder or player</span></span>                |
| <span data-ttu-id="01b9f-136">**videodisco**</span><span class="sxs-lookup"><span data-stu-id="01b9f-136">**videodisc**</span></span>    | <span data-ttu-id="01b9f-137">\_videodisco DEVTYPE \_ MCI</span><span class="sxs-lookup"><span data-stu-id="01b9f-137">MCI\_DEVTYPE\_VIDEODISC</span></span>       | <span data-ttu-id="01b9f-138">Videodisco Player</span><span class="sxs-lookup"><span data-stu-id="01b9f-138">Videodisc player</span></span>                                 |
| <span data-ttu-id="01b9f-139">**WaveAudio**</span><span class="sxs-lookup"><span data-stu-id="01b9f-139">**waveaudio**</span></span>    | <span data-ttu-id="01b9f-140">\_audio della \_ waveform \_ DEVTYPE MCI</span><span class="sxs-lookup"><span data-stu-id="01b9f-140">MCI\_DEVTYPE\_WAVEFORM\_AUDIO</span></span> | <span data-ttu-id="01b9f-141">Dispositivo audio che riproduce file di forma d'onda digitalizzati</span><span class="sxs-lookup"><span data-stu-id="01b9f-141">Audio device that plays digitized waveform files</span></span> |



 

<span data-ttu-id="01b9f-142">In questo documento i nomi dei tipi di dispositivo sono in grassetto.</span><span class="sxs-lookup"><span data-stu-id="01b9f-142">In this document, the names of device types are bold.</span></span> <span data-ttu-id="01b9f-143">I nomi dei tipi di dispositivo vengono usati con l'interfaccia della stringa di comando.</span><span class="sxs-lookup"><span data-stu-id="01b9f-143">Device-type names are used with the command-string interface.</span></span> <span data-ttu-id="01b9f-144">Le costanti di tipo dispositivo vengono usate con l'interfaccia del messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="01b9f-144">Device-type constants are used with the command-message interface.</span></span>

 

 




