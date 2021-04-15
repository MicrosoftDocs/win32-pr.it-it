---
title: Interrompi comando
description: Il comando Stop interrompe la riproduzione o la registrazione. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- Interrompi comando Windows Multimedia
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d70aa150c01bd4c0ceab10332b4eca8b15d041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400615"
---
# <a name="stop-command"></a><span data-ttu-id="0a843-105">Interrompi comando</span><span class="sxs-lookup"><span data-stu-id="0a843-105">stop command</span></span>

<span data-ttu-id="0a843-106">Il comando Stop interrompe la riproduzione o la registrazione.</span><span class="sxs-lookup"><span data-stu-id="0a843-106">The stop command stops playback or recording.</span></span> <span data-ttu-id="0a843-107">CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="0a843-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="0a843-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0a843-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("stop %s %s %s"), 
  lpszDeviceID, 
  lpszStopFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0a843-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a843-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a843-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0a843-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0a843-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="0a843-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0a843-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="0a843-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0a843-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span><span class="sxs-lookup"><span data-stu-id="0a843-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0a843-114">Per i dispositivi digitali video, il flag può essere il seguente.</span><span class="sxs-lookup"><span data-stu-id="0a843-114">For digital-video devices, it can be the following flag.</span></span>



| <span data-ttu-id="0a843-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0a843-115">Value</span></span> | <span data-ttu-id="0a843-116">Significato</span><span class="sxs-lookup"><span data-stu-id="0a843-116">Meaning</span></span>                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a843-117">contenere</span><span class="sxs-lookup"><span data-stu-id="0a843-117">hold</span></span>  | <span data-ttu-id="0a843-118">Impedisce il rilascio di risorse necessarie per ricreare un'immagine ancora sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="0a843-118">Prevents the release of resources required to redraw a still image on the screen.</span></span> <span data-ttu-id="0a843-119">Il buffer del frame rimane disponibile per l'aggiornamento della visualizzazione quando, ad esempio, la finestra viene spostata.</span><span class="sxs-lookup"><span data-stu-id="0a843-119">The frame buffer remains available for use in updating the display when, for example, the window is moved.</span></span> |



 

</dd> <dt>

<span data-ttu-id="0a843-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="0a843-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0a843-121">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="0a843-121">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="0a843-122">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="0a843-122">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="0a843-123">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0a843-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a843-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a843-124">Return Value</span></span>

<span data-ttu-id="0a843-125">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="0a843-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a843-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a843-126">Remarks</span></span>

<span data-ttu-id="0a843-127">Per i dispositivi audio CD, il comando Interrompi arresta la riproduzione e reimposta la posizione corrente del rilevamento su zero.</span><span class="sxs-lookup"><span data-stu-id="0a843-127">For CD audio devices, the stop command stops playback and resets the current track position to zero.</span></span>

## <a name="examples"></a><span data-ttu-id="0a843-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="0a843-128">Examples</span></span>

<span data-ttu-id="0a843-129">Il comando seguente interrompe la riproduzione o la registrazione sul dispositivo "audio".</span><span class="sxs-lookup"><span data-stu-id="0a843-129">The following command stops playback or recording on the "mysound" device.</span></span>

``` syntax
stop mysound
```

## <a name="requirements"></a><span data-ttu-id="0a843-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a843-130">Requirements</span></span>



| <span data-ttu-id="0a843-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a843-131">Requirement</span></span> | <span data-ttu-id="0a843-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0a843-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0a843-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a843-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0a843-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a843-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0a843-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a843-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0a843-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a843-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0a843-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a843-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a843-138">MCI</span><span class="sxs-lookup"><span data-stu-id="0a843-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0a843-139">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="0a843-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

