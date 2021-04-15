---
title: comando Step
description: Il comando Step esegue la riproduzione di uno o più frame avanti o indietro. L'azione predefinita prevede l'esecuzione del passaggio avanti di un frame. I dispositivi videodisco Digital-video, VCR e CAV-Format riconoscono questo comando.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- comando passaggio Windows Multimedia
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6203d0b2d5dea401e8197e1261946955cd28618a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476583"
---
# <a name="step-command"></a><span data-ttu-id="13f27-106">comando Step</span><span class="sxs-lookup"><span data-stu-id="13f27-106">step command</span></span>

<span data-ttu-id="13f27-107">Il comando Step esegue la riproduzione di uno o più frame avanti o indietro.</span><span class="sxs-lookup"><span data-stu-id="13f27-107">The step command steps the play one or more frames forward or reverse.</span></span> <span data-ttu-id="13f27-108">L'azione predefinita prevede l'esecuzione del passaggio avanti di un frame.</span><span class="sxs-lookup"><span data-stu-id="13f27-108">The default action is to step forward one frame.</span></span> <span data-ttu-id="13f27-109">I dispositivi videodisco Digital-video, VCR e CAV-Format riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="13f27-109">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="13f27-110">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="13f27-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="13f27-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="13f27-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13f27-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="13f27-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="13f27-113">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="13f27-113">Identifier of an MCI device.</span></span> <span data-ttu-id="13f27-114">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="13f27-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="13f27-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span><span class="sxs-lookup"><span data-stu-id="13f27-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span></span>
</dt> <dd>

<span data-ttu-id="13f27-116">Uno o entrambi i flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="13f27-116">One or both of the following flags.</span></span>



| <span data-ttu-id="13f27-117">Valore</span><span class="sxs-lookup"><span data-stu-id="13f27-117">Value</span></span>       | <span data-ttu-id="13f27-118">Significato</span><span class="sxs-lookup"><span data-stu-id="13f27-118">Meaning</span></span>                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f27-119">per *frame*</span><span class="sxs-lookup"><span data-stu-id="13f27-119">by *frames*</span></span> | <span data-ttu-id="13f27-120">Indica il numero di frame da scorrere.</span><span class="sxs-lookup"><span data-stu-id="13f27-120">Indicates the number of frames to step.</span></span> <span data-ttu-id="13f27-121">Se si specifica un valore di *frame* negativi, non è possibile specificare il flag "Reverse".</span><span class="sxs-lookup"><span data-stu-id="13f27-121">If you specify a negative *frames* value, you cannot specify the "reverse" flag.</span></span> |
| <span data-ttu-id="13f27-122">reverse</span><span class="sxs-lookup"><span data-stu-id="13f27-122">reverse</span></span>     | <span data-ttu-id="13f27-123">Eseguire il passaggio dei frame in senso inverso.</span><span class="sxs-lookup"><span data-stu-id="13f27-123">Step the frames in reverse.</span></span>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="13f27-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="13f27-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="13f27-125">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="13f27-125">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="13f27-126">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="13f27-126">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="13f27-127">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="13f27-127">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13f27-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13f27-128">Return Value</span></span>

<span data-ttu-id="13f27-129">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="13f27-129">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="13f27-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13f27-130">Requirements</span></span>



| <span data-ttu-id="13f27-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="13f27-131">Requirement</span></span> | <span data-ttu-id="13f27-132">Valore</span><span class="sxs-lookup"><span data-stu-id="13f27-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="13f27-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13f27-133">Minimum supported client</span></span><br/> | <span data-ttu-id="13f27-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13f27-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="13f27-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13f27-135">Minimum supported server</span></span><br/> | <span data-ttu-id="13f27-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13f27-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="13f27-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13f27-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f27-138">MCI</span><span class="sxs-lookup"><span data-stu-id="13f27-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="13f27-139">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="13f27-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

