---
title: comando Delete
description: Il comando Delete Elimina un segmento di dati da un file. Digital-video e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- Elimina il comando Windows Multimedia
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874458"
---
# <a name="delete-command"></a><span data-ttu-id="0f807-105">comando Delete</span><span class="sxs-lookup"><span data-stu-id="0f807-105">delete command</span></span>

<span data-ttu-id="0f807-106">Il comando Delete Elimina un segmento di dati da un file.</span><span class="sxs-lookup"><span data-stu-id="0f807-106">The delete command deletes a data segment from a file.</span></span> <span data-ttu-id="0f807-107">Digital-video e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="0f807-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="0f807-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0f807-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0f807-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f807-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f807-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0f807-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0f807-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="0f807-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0f807-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="0f807-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0f807-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span><span class="sxs-lookup"><span data-stu-id="0f807-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span></span>
</dt> <dd>

<span data-ttu-id="0f807-114">Flag che identifica un segmento di dati da eliminare.</span><span class="sxs-lookup"><span data-stu-id="0f807-114">Flag that identifies a data segment to delete.</span></span> <span data-ttu-id="0f807-115">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Delete** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="0f807-115">The following table lists device types that recognize the **delete** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0f807-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0f807-116">Value</span></span></th>
<th><span data-ttu-id="0f807-117">Significato</span><span class="sxs-lookup"><span data-stu-id="0f807-117">Meaning</span></span></th>
<th><span data-ttu-id="0f807-118">Significato</span><span class="sxs-lookup"><span data-stu-id="0f807-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f807-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="0f807-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="0f807-120">al <em>rettangolo</em></span><span class="sxs-lookup"><span data-stu-id="0f807-120">at <em>rectangle</em></span></span></li>
<li><span data-ttu-id="0f807-121"><em>flusso</em> del flusso audio</span><span class="sxs-lookup"><span data-stu-id="0f807-121">audio stream <em>stream</em></span></span></li>
<li><span data-ttu-id="0f807-122">dalla <em>posizione</em></span><span class="sxs-lookup"><span data-stu-id="0f807-122">from <em>position</em></span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0f807-123"><em>posizione</em></span><span class="sxs-lookup"><span data-stu-id="0f807-123">to <em>position</em></span></span></li>
<li><span data-ttu-id="0f807-124"><em>flusso</em> del flusso video</span><span class="sxs-lookup"><span data-stu-id="0f807-124">video stream <em>stream</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f807-125">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="0f807-125">waveaudio</span></span></td>
<td><span data-ttu-id="0f807-126">dalla <em>posizione</em></span><span class="sxs-lookup"><span data-stu-id="0f807-126">from <em>position</em></span></span></td>
<td><span data-ttu-id="0f807-127"><em>posizione</em></span><span class="sxs-lookup"><span data-stu-id="0f807-127">to <em>position</em></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0f807-128">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro *lpszPosition* e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="0f807-128">The following table lists the flags that can be specified in the *lpszPosition* parameter and their meanings.</span></span>



| <span data-ttu-id="0f807-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0f807-129">Value</span></span>                 | <span data-ttu-id="0f807-130">Significato</span><span class="sxs-lookup"><span data-stu-id="0f807-130">Meaning</span></span>                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f807-131">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="0f807-131">at *rectangle*</span></span>        | <span data-ttu-id="0f807-132">Specifica la parte di ogni frame eliminata.</span><span class="sxs-lookup"><span data-stu-id="0f807-132">Specifies the portion of each frame deleted.</span></span> <span data-ttu-id="0f807-133">Se omesso, il valore predefinito è l'intero frame.</span><span class="sxs-lookup"><span data-stu-id="0f807-133">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="0f807-134">Quando si specifica questo elemento, i frame non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="0f807-134">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="0f807-135">L'area all'interno del rettangolo diventa invece nero.</span><span class="sxs-lookup"><span data-stu-id="0f807-135">Instead the area inside the rectangle becomes black.</span></span>                                          |
| <span data-ttu-id="0f807-136">*flusso* del flusso audio</span><span class="sxs-lookup"><span data-stu-id="0f807-136">audio stream *stream*</span></span> | <span data-ttu-id="0f807-137">Specifica il flusso audio nell'area di lavoro interessata dal comando.</span><span class="sxs-lookup"><span data-stu-id="0f807-137">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="0f807-138">Se si usa questo flag e si vuole anche eliminare il video, è necessario usare anche il flag "flusso video".</span><span class="sxs-lookup"><span data-stu-id="0f807-138">If you use this flag and also want to delete video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="0f807-139">Se non viene specificato alcun flag, vengono eliminati tutti i flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="0f807-139">(If neither flag is specified, all audio and video streams are deleted.)</span></span> |
| <span data-ttu-id="0f807-140">dalla *posizione*</span><span class="sxs-lookup"><span data-stu-id="0f807-140">from *position*</span></span>       | <span data-ttu-id="0f807-141">Specifica la posizione di inizio dell'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="0f807-141">Specifies the position at which deletion begins.</span></span> <span data-ttu-id="0f807-142">Se questo flag viene omesso, l'eliminazione inizia in corrispondenza della posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="0f807-142">If this flag is omitted, the deletion begins at the current position.</span></span>                                                                                                                       |
| <span data-ttu-id="0f807-143">*posizione*</span><span class="sxs-lookup"><span data-stu-id="0f807-143">to *position*</span></span>         | <span data-ttu-id="0f807-144">Specifica la posizione in cui termina l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="0f807-144">Specifies the position at which deletion ends.</span></span> <span data-ttu-id="0f807-145">Se questo flag viene omesso, l'eliminazione continua fino alla fine del contenuto o dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0f807-145">If this flag is omitted, the deletion continues to the end of the content or workspace.</span></span>                                                                                                       |
| <span data-ttu-id="0f807-146">*flusso* del flusso video</span><span class="sxs-lookup"><span data-stu-id="0f807-146">video stream *stream*</span></span> | <span data-ttu-id="0f807-147">Specifica il flusso video nell'area di lavoro interessata dal comando.</span><span class="sxs-lookup"><span data-stu-id="0f807-147">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="0f807-148">Se si utilizza questo flag e si desidera eliminare anche audio, è necessario utilizzare anche il flag "flusso audio".</span><span class="sxs-lookup"><span data-stu-id="0f807-148">If you use this flag and also want to delete audio, you must also use "audio stream" flag.</span></span> <span data-ttu-id="0f807-149">Se non viene specificato alcun flag, vengono eliminati tutti i flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="0f807-149">(If neither flag is specified, all audio and video streams are deleted.)</span></span>     |



 

</dd> <dt>

<span data-ttu-id="0f807-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="0f807-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0f807-151">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="0f807-151">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="0f807-152">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="0f807-152">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="0f807-153">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0f807-153">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f807-154">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f807-154">Return Value</span></span>

<span data-ttu-id="0f807-155">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="0f807-155">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f807-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f807-156">Remarks</span></span>

<span data-ttu-id="0f807-157">Prima di emettere i comandi che usano i valori di posizione, è necessario impostare il formato di ora desiderato usando il comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="0f807-157">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="0f807-158">Esempio</span><span class="sxs-lookup"><span data-stu-id="0f807-158">Examples</span></span>

<span data-ttu-id="0f807-159">Il comando seguente elimina i dati audio della forma d'onda da 1 millisecondo a 900 millisecondi (presupponendo che il formato dell'ora sia impostato su millisecondi).</span><span class="sxs-lookup"><span data-stu-id="0f807-159">The following command deletes the waveform-audio data from 1 millisecond through 900 milliseconds (assuming the time format is set to milliseconds).</span></span>

``` syntax
delete mysound from 1 to 900
```

## <a name="requirements"></a><span data-ttu-id="0f807-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f807-160">Requirements</span></span>



| <span data-ttu-id="0f807-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f807-161">Requirement</span></span> | <span data-ttu-id="0f807-162">Valore</span><span class="sxs-lookup"><span data-stu-id="0f807-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0f807-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f807-163">Minimum supported client</span></span><br/> | <span data-ttu-id="0f807-164">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f807-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0f807-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f807-165">Minimum supported server</span></span><br/> | <span data-ttu-id="0f807-166">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f807-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0f807-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f807-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f807-168">MCI</span><span class="sxs-lookup"><span data-stu-id="0f807-168">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0f807-169">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="0f807-169">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="0f807-170">set</span><span class="sxs-lookup"><span data-stu-id="0f807-170">set</span></span>](set.md)
</dt> </dl>

 

