---
title: Sospendi comando
description: Il comando Sospendi sospende la riproduzione o la registrazione.
ms.assetid: 8fa1a40d-fdb1-4c9f-a8db-9dd6a0d83b87
keywords:
- Sospendi comando Windows Multimedia
topic_type:
- apiref
api_name:
- pause
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25957defa4db514ce84f2e013dcc3751e21779b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874622"
---
# <a name="pause-command"></a><span data-ttu-id="87aea-104">Sospendi comando</span><span class="sxs-lookup"><span data-stu-id="87aea-104">pause command</span></span>

<span data-ttu-id="87aea-105">Il comando Sospendi sospende la riproduzione o la registrazione.</span><span class="sxs-lookup"><span data-stu-id="87aea-105">The pause command pauses playing or recording.</span></span> <span data-ttu-id="87aea-106">La maggior parte dei driver mantiene la posizione corrente e, infine, riprende la riproduzione o la registrazione in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="87aea-106">Most drivers retain the current position and eventually resume playback or recording at this position.</span></span> <span data-ttu-id="87aea-107">CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="87aea-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="87aea-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="87aea-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("pause %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="87aea-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="87aea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87aea-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="87aea-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="87aea-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="87aea-111">Identifier of an MCI device.</span></span> <span data-ttu-id="87aea-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="87aea-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="87aea-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="87aea-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="87aea-114">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="87aea-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="87aea-115">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="87aea-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="87aea-116">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="87aea-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87aea-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87aea-117">Return Value</span></span>

<span data-ttu-id="87aea-118">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="87aea-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="87aea-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="87aea-119">Remarks</span></span>

<span data-ttu-id="87aea-120">Con i driver MCICDA, MCISEQ e MCIPIONR, il comando pause funziona allo stesso modo del comando [Stop](stop.md) .</span><span class="sxs-lookup"><span data-stu-id="87aea-120">With the MCICDA, MCISEQ, and MCIPIONR drivers, the pause command works the same as the [stop](stop.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="87aea-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="87aea-121">Examples</span></span>

<span data-ttu-id="87aea-122">Il comando che segue sospende il dispositivo "audio".</span><span class="sxs-lookup"><span data-stu-id="87aea-122">The following command pauses the "mysound" device.</span></span>

``` syntax
pause mysound
```

## <a name="requirements"></a><span data-ttu-id="87aea-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87aea-123">Requirements</span></span>



| <span data-ttu-id="87aea-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="87aea-124">Requirement</span></span> | <span data-ttu-id="87aea-125">Valore</span><span class="sxs-lookup"><span data-stu-id="87aea-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="87aea-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87aea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="87aea-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87aea-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="87aea-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87aea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="87aea-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87aea-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="87aea-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87aea-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87aea-131">MCI</span><span class="sxs-lookup"><span data-stu-id="87aea-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="87aea-132">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="87aea-132">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="87aea-133">stop</span><span class="sxs-lookup"><span data-stu-id="87aea-133">stop</span></span>](stop.md)
</dt> </dl>

 

