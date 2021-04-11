---
title: Recupero della posizione di riproduzione corrente
description: Recupero della posizione di riproduzione corrente
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- audio Waveform, posizione corrente di riproduzione
- waveform-interfaccia audio, posizione corrente di riproduzione
- riproduzione di file audio Waveform, posizione corrente di riproduzione
- waveOutGetPosition (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28737cfc292dc8779b21756f38813642b82e452
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336862"
---
# <a name="retrieving-the-current-playback-position"></a><span data-ttu-id="8046d-107">Recupero della posizione di riproduzione corrente</span><span class="sxs-lookup"><span data-stu-id="8046d-107">Retrieving the Current Playback Position</span></span>

<span data-ttu-id="8046d-108">È possibile monitorare la posizione di riproduzione corrente all'interno del file durante la riproduzione dell'audio della forma d'onda usando la funzione [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) .</span><span class="sxs-lookup"><span data-stu-id="8046d-108">You can monitor the current playback position within the file while waveform audio is playing by using the [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) function.</span></span>

<span data-ttu-id="8046d-109">Per i dispositivi Waveform-Audio, gli esempi rappresentano il formato ora preferito in cui rappresentare la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="8046d-109">For waveform-audio devices, samples are the preferred time format in which to represent the current position.</span></span> <span data-ttu-id="8046d-110">In questo modo, la posizione corrente di un dispositivo di forma d'onda-audio viene specificata come numero di campioni per un canale a partire dall'inizio del file audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="8046d-110">Thus, the current position of a waveform-audio device is specified as the number of samples for one channel from the beginning of the waveform-audio file.</span></span> <span data-ttu-id="8046d-111">Per eseguire una query sulla posizione corrente di un dispositivo audio Waveform, impostare il membro **wType** della struttura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) su \_ Samples Time e passare la struttura a **waveOutGetPosition**.</span><span class="sxs-lookup"><span data-stu-id="8046d-111">To query the current position of a waveform-audio device, set the **wType** member of the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to TIME\_SAMPLES and pass this structure to **waveOutGetPosition**.</span></span>

<span data-ttu-id="8046d-112">La struttura **MMTIME** può rappresentare il tempo in uno o più formati diversi, tra cui millisecondi, esempi, SMPTE (società di Motion Picture e ingegneri televisivi) e formati di puntatore del brano MIDI.</span><span class="sxs-lookup"><span data-stu-id="8046d-112">The **MMTIME** structure can represent time in one or more different formats, including milliseconds, samples, SMPTE (Society of Motion Picture and Television Engineers), and MIDI song pointer formats.</span></span> <span data-ttu-id="8046d-113">Il membro **wType** specifica il formato utilizzato per rappresentare l'ora.</span><span class="sxs-lookup"><span data-stu-id="8046d-113">The **wType** member specifies the format used to represent time.</span></span> <span data-ttu-id="8046d-114">Prima di chiamare una funzione che usa la struttura **MMTIME** , è necessario impostare **wType** per indicare il formato di ora richiesto.</span><span class="sxs-lookup"><span data-stu-id="8046d-114">Before calling a function that uses the **MMTIME** structure, you must set **wType** to indicate your requested time format.</span></span> <span data-ttu-id="8046d-115">Assicurarsi di controllare **wType** dopo la chiamata per verificare se il formato ora richiesto è supportato.</span><span class="sxs-lookup"><span data-stu-id="8046d-115">Be sure to check **wType** after the call to see whether the requested time format is supported.</span></span> <span data-ttu-id="8046d-116">Se il formato tempo richiesto non è supportato, il driver di dispositivo specifica l'ora in un formato di ora alternativo e modifica il membro **wType** nel formato di ora selezionato.</span><span class="sxs-lookup"><span data-stu-id="8046d-116">If the requested time format is not supported, the device driver specifies the time in an alternate time format and changes the **wType** member to the selected time format.</span></span>

<span data-ttu-id="8046d-117">Per ulteriori informazioni sulla struttura **MMTIME** , vedere la pagina relativa ai [timer multimediali](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="8046d-117">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

 

 