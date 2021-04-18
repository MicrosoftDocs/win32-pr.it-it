---
title: Resume (comando)
description: Il comando Resume continua la riproduzione o la registrazione in un dispositivo che è stato sospeso usando il comando pause.
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- riprendere il comando Windows Multimedia
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f01fd96e2b25e191608c7c6abf70bfd842158d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301013"
---
# <a name="resume-command"></a><span data-ttu-id="c1793-104">Resume (comando)</span><span class="sxs-lookup"><span data-stu-id="c1793-104">resume command</span></span>

<span data-ttu-id="c1793-105">Il comando Resume continua la riproduzione o la registrazione in un dispositivo che è stato sospeso usando il comando [pause](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="c1793-105">The resume command continues playing or recording on a device that has been paused using the [pause](pause.md) command.</span></span> <span data-ttu-id="c1793-106">Digital-video, VCR e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="c1793-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="c1793-107">Anche se i dispositivi CD audio, MIDI sequencer e videodisco riconoscono questo comando, i driver di dispositivo MCICDA, MCISEQ e MCIPIONR non lo supportano.</span><span class="sxs-lookup"><span data-stu-id="c1793-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="c1793-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c1793-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("resume %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c1793-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1793-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1793-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c1793-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c1793-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c1793-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c1793-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="c1793-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c1793-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c1793-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c1793-114">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="c1793-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c1793-115">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="c1793-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="c1793-116">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c1793-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1793-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1793-117">Return Value</span></span>

<span data-ttu-id="c1793-118">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="c1793-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="c1793-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="c1793-119">Examples</span></span>

<span data-ttu-id="c1793-120">Il seguente comando continua la riproduzione o la registrazione del dispositivo "Newsound".</span><span class="sxs-lookup"><span data-stu-id="c1793-120">The following command continues playing or recording the "newsound" device.</span></span>

``` syntax
resume newsound
```

## <a name="requirements"></a><span data-ttu-id="c1793-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1793-121">Requirements</span></span>



| <span data-ttu-id="c1793-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1793-122">Requirement</span></span> | <span data-ttu-id="c1793-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c1793-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c1793-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1793-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c1793-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1793-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c1793-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1793-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c1793-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1793-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c1793-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1793-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1793-129">MCI</span><span class="sxs-lookup"><span data-stu-id="c1793-129">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c1793-130">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="c1793-130">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c1793-131">pause</span><span class="sxs-lookup"><span data-stu-id="c1793-131">pause</span></span>](pause.md)
</dt> </dl>

 

