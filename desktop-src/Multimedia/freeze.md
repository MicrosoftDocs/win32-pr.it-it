---
title: blocca comando
description: Il comando Freeze consente di bloccare l'input video o l'output video in un VCR o di disabilitare l'acquisizione di video nel buffer del frame. I dispositivi Digital-video, video-overlay e VCR riconoscono questo comando.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- blocca il comando Windows Multimedia
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047836"
---
# <a name="freeze-command"></a><span data-ttu-id="3460a-105">blocca comando</span><span class="sxs-lookup"><span data-stu-id="3460a-105">freeze command</span></span>

<span data-ttu-id="3460a-106">Il comando Freeze consente di bloccare l'input video o l'output video in un VCR o di disabilitare l'acquisizione di video nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="3460a-106">The freeze command freezes video input or video output on a VCR or disables video acquisition to the frame buffer.</span></span> <span data-ttu-id="3460a-107">I dispositivi Digital-video, video-overlay e VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="3460a-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="3460a-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="3460a-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="3460a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3460a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3460a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3460a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3460a-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="3460a-111">Identifier of an MCI device.</span></span> <span data-ttu-id="3460a-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="3460a-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="3460a-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span><span class="sxs-lookup"><span data-stu-id="3460a-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3460a-114">Flag che identifica gli elementi da bloccare.</span><span class="sxs-lookup"><span data-stu-id="3460a-114">Flag that identifies what to freeze.</span></span> <span data-ttu-id="3460a-115">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Freeze** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="3460a-115">The following table lists device types that recognize the **freeze** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3460a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3460a-116">Value</span></span></th>
<th><span data-ttu-id="3460a-117">Significato</span><span class="sxs-lookup"><span data-stu-id="3460a-117">Meaning</span></span></th>
<th><span data-ttu-id="3460a-118">Significato</span><span class="sxs-lookup"><span data-stu-id="3460a-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3460a-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="3460a-119">digitalvideo</span></span></td>
<td><span data-ttu-id="3460a-120">al <em>rettangolo</em></span><span class="sxs-lookup"><span data-stu-id="3460a-120">at <em>rectangle</em></span></span></td>
<td><span data-ttu-id="3460a-121">fuori</span><span class="sxs-lookup"><span data-stu-id="3460a-121">outside</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3460a-122">overlay</span><span class="sxs-lookup"><span data-stu-id="3460a-122">overlay</span></span></td>
<td><span data-ttu-id="3460a-123">al <em>rettangolo</em></span><span class="sxs-lookup"><span data-stu-id="3460a-123">at <em>rectangle</em></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3460a-124">VCR</span><span class="sxs-lookup"><span data-stu-id="3460a-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="3460a-125">campo</span><span class="sxs-lookup"><span data-stu-id="3460a-125">field</span></span></li>
<li><span data-ttu-id="3460a-126">frame</span><span class="sxs-lookup"><span data-stu-id="3460a-126">frame</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3460a-127">input</span><span class="sxs-lookup"><span data-stu-id="3460a-127">input</span></span></li>
<li><span data-ttu-id="3460a-128">output</span><span class="sxs-lookup"><span data-stu-id="3460a-128">output</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3460a-129">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro *lpszFreezeFlags* e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="3460a-129">The following table lists the flags that can be specified in the *lpszFreezeFlags* parameter and their meanings.</span></span>



| <span data-ttu-id="3460a-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3460a-130">Value</span></span>          | <span data-ttu-id="3460a-131">Significato</span><span class="sxs-lookup"><span data-stu-id="3460a-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3460a-132">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="3460a-132">at *rectangle*</span></span> | <span data-ttu-id="3460a-133">Specifica l'area che verrà bloccata.</span><span class="sxs-lookup"><span data-stu-id="3460a-133">Specifies the region that will be frozen.</span></span> <span data-ttu-id="3460a-134">Per i dispositivi con sovrimpressione video, in questa area l'acquisizione video è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="3460a-134">For video-overlay devices, this region will have video acquisition disabled.</span></span> <span data-ttu-id="3460a-135">Per i dispositivi video digitali, i pixel all'interno del rettangolo avranno il relativo bit di maschera di blocco acceso (a meno che non sia specificato il flag "esterno").</span><span class="sxs-lookup"><span data-stu-id="3460a-135">For digital-video devices, the pixels within the rectangle will have their lock mask bit turned on (unless the "outside" flag is specified).</span></span> <span data-ttu-id="3460a-136">Il rettangolo è relativo all'origine del buffer video ed è specificato come *X1 Y1 Y1 2*.</span><span class="sxs-lookup"><span data-stu-id="3460a-136">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="3460a-137">Le coordinate *X1 Y1* specificano l'angolo superiore sinistro del rettangolo e le coordinate *X2 Y2* specificano la larghezza e l'altezza.</span><span class="sxs-lookup"><span data-stu-id="3460a-137">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="3460a-138">campo</span><span class="sxs-lookup"><span data-stu-id="3460a-138">field</span></span>          | <span data-ttu-id="3460a-139">Blocca il primo campo.</span><span class="sxs-lookup"><span data-stu-id="3460a-139">Freezes the first field.</span></span> <span data-ttu-id="3460a-140">Per impostazione predefinita, viene utilizzato il campo (se non viene specificato né frame né campo).</span><span class="sxs-lookup"><span data-stu-id="3460a-140">Field is assumed by default (if neither frame nor field is specified).</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3460a-141">frame</span><span class="sxs-lookup"><span data-stu-id="3460a-141">frame</span></span>          | <span data-ttu-id="3460a-142">Blocca l'intero frame, visualizzando entrambi i campi.</span><span class="sxs-lookup"><span data-stu-id="3460a-142">Freezes the entire frame, displaying both fields.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3460a-143">input</span><span class="sxs-lookup"><span data-stu-id="3460a-143">input</span></span>          | <span data-ttu-id="3460a-144">Blocca il frame corrente dell'immagine di input, se è in pausa o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3460a-144">Freezes the current frame of the input image, whether it is paused or running.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3460a-145">output</span><span class="sxs-lookup"><span data-stu-id="3460a-145">output</span></span>         | <span data-ttu-id="3460a-146">Blocca il frame corrente dell'output dal VCR.</span><span class="sxs-lookup"><span data-stu-id="3460a-146">Freezes the current frame of the output from the VCR.</span></span> <span data-ttu-id="3460a-147">Se il videoregistratore viene riprodotto quando viene eseguito il blocco, il frame corrente viene bloccato e il videoregistratore viene sospeso.</span><span class="sxs-lookup"><span data-stu-id="3460a-147">If the VCR is playing when freeze is issued, the current frame is frozen and the VCR is paused.</span></span> <span data-ttu-id="3460a-148">Se il videoregistratore viene sospeso quando viene emesso questo comando, il frame corrente è bloccato.</span><span class="sxs-lookup"><span data-stu-id="3460a-148">If the VCR is paused when this command is issued, the current frame is frozen.</span></span> <span data-ttu-id="3460a-149">L'immagine bloccata rimane sul dispositivo di output fino a quando non viene emesso un comando di [Unfreeze](unfreeze.md) .</span><span class="sxs-lookup"><span data-stu-id="3460a-149">The frozen image remains on the output device until an [unfreeze](unfreeze.md) command is issued.</span></span> <span data-ttu-id="3460a-150">Se non viene specificato né "input" né "output", viene utilizzato "output".</span><span class="sxs-lookup"><span data-stu-id="3460a-150">If neither "input" nor "output" is specified, "output" is assumed.</span></span>                                                                                    |
| <span data-ttu-id="3460a-151">fuori</span><span class="sxs-lookup"><span data-stu-id="3460a-151">outside</span></span>        | <span data-ttu-id="3460a-152">Indica che l'area esterna all'area specificata utilizzando il flag "at" è bloccata.</span><span class="sxs-lookup"><span data-stu-id="3460a-152">Indicates that the area outside the region specified using the "at" flag is frozen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="3460a-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="3460a-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3460a-154">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="3460a-154">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="3460a-155">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="3460a-155">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="3460a-156">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3460a-156">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3460a-157">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3460a-157">Return Value</span></span>

<span data-ttu-id="3460a-158">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="3460a-158">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3460a-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="3460a-159">Remarks</span></span>

<span data-ttu-id="3460a-160">Se usato con i dispositivi VCR, questo comando è destinato alle schede di acquisizione dei frame.</span><span class="sxs-lookup"><span data-stu-id="3460a-160">When used with VCR devices, this command is intended for frame-grabbing cards.</span></span>

<span data-ttu-id="3460a-161">Per specificare le aree di acquisizione irregolari con il flag "at", usare una serie di comandi Freeze e [Unfreeze](unfreeze.md) .</span><span class="sxs-lookup"><span data-stu-id="3460a-161">To specify irregular acquisition regions with the "at" flag, use a series of freeze and [unfreeze](unfreeze.md) commands.</span></span> <span data-ttu-id="3460a-162">Alcuni dispositivi con sovrimpressione video limitano la complessità dell'area di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3460a-162">Some video-overlay devices limit the complexity of the acquisition region.</span></span>

<span data-ttu-id="3460a-163">Questo comando è supportato solo se una chiamata al comando [Capability](capability.md) con il flag "Can Freeze" restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="3460a-163">This command is supported only if a call to the [capability](capability.md) command with the "can freeze" flag returns **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="3460a-164">Esempio</span><span class="sxs-lookup"><span data-stu-id="3460a-164">Examples</span></span>

<span data-ttu-id="3460a-165">Il comando che segue Disabilita l'acquisizione di video in un quadrato di 100 pixel nell'angolo superiore sinistro del buffer video.</span><span class="sxs-lookup"><span data-stu-id="3460a-165">The following command disables video acquisition in a 100-pixel square at the upper left corner of the video buffer.</span></span>

``` syntax
freeze vboard at 0 0 100 100
```

## <a name="requirements"></a><span data-ttu-id="3460a-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3460a-166">Requirements</span></span>



| <span data-ttu-id="3460a-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="3460a-167">Requirement</span></span> | <span data-ttu-id="3460a-168">Valore</span><span class="sxs-lookup"><span data-stu-id="3460a-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3460a-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3460a-169">Minimum supported client</span></span><br/> | <span data-ttu-id="3460a-170">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3460a-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3460a-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3460a-171">Minimum supported server</span></span><br/> | <span data-ttu-id="3460a-172">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3460a-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3460a-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3460a-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3460a-174">MCI</span><span class="sxs-lookup"><span data-stu-id="3460a-174">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3460a-175">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="3460a-175">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="3460a-176">capability</span><span class="sxs-lookup"><span data-stu-id="3460a-176">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="3460a-177">Sblocca</span><span class="sxs-lookup"><span data-stu-id="3460a-177">unfreeze</span></span>](unfreeze.md)
</dt> </dl>

 

