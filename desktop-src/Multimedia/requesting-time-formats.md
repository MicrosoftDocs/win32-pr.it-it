---
title: Formati di ora richieste
description: Formati di ora richieste
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- MIDI (Musical Instrument Digital Interface), formati di ora
- MIDI (Musical Instrument Digital Interface), formati di ora
- Servizi MIDI, formati di ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724807"
---
# <a name="requesting-time-formats"></a><span data-ttu-id="02587-106">Formati di ora richieste</span><span class="sxs-lookup"><span data-stu-id="02587-106">Requesting Time Formats</span></span>

<span data-ttu-id="02587-107">Windows utilizza la struttura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) per rappresentare l'ora in uno o più formati diversi, tra cui i formati di millisecondi, Samples, SMPTE e Midi song pointer.</span><span class="sxs-lookup"><span data-stu-id="02587-107">Windows uses the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to represent time in one or more different formats, including milliseconds, samples, SMPTE, and MIDI song pointer formats.</span></span> <span data-ttu-id="02587-108">Il membro **wType** specifica il formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="02587-108">The **wType** member specifies the time format.</span></span>

<span data-ttu-id="02587-109">La funzione [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) usa la struttura **MMTIME** .</span><span class="sxs-lookup"><span data-stu-id="02587-109">The [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) function uses the **MMTIME** structure.</span></span> <span data-ttu-id="02587-110">Prima di chiamare questa funzione, è necessario impostare il membro **wType** per indicare il formato di tempo richiesto.</span><span class="sxs-lookup"><span data-stu-id="02587-110">Before calling this function, you must set the **wType** member to indicate your requested time format.</span></span> <span data-ttu-id="02587-111">Per verificare se il formato ora richiesto è supportato, controllare **wType** dopo la chiamata.</span><span class="sxs-lookup"><span data-stu-id="02587-111">To see if the requested time format is supported, check **wType** after the call.</span></span> <span data-ttu-id="02587-112">Se il formato tempo richiesto non è supportato, l'ora viene specificata in un formato di ora alternativo selezionato dal driver di dispositivo e il membro **wType** viene modificato per indicare il formato di ora selezionato.</span><span class="sxs-lookup"><span data-stu-id="02587-112">If the requested time format is not supported, the time is specified in an alternate time format selected by the device driver and the **wType** member is changed to indicate the selected time format.</span></span>

<span data-ttu-id="02587-113">Per ulteriori informazioni sulla struttura **MMTIME** , vedere la pagina relativa ai [timer multimediali](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="02587-113">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02587-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02587-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02587-115">Servizi MIDI</span><span class="sxs-lookup"><span data-stu-id="02587-115">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 