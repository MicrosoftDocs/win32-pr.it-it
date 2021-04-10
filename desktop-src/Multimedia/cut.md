---
title: Taglia comando
description: Il comando taglia rimuove i dati dall'area di lavoro e li copia negli Appunti. I dispositivi digitali video riconoscono questo comando.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- taglia il comando Windows Multimedia
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964727"
---
# <a name="cut-command"></a><span data-ttu-id="0e5a3-105">Taglia comando</span><span class="sxs-lookup"><span data-stu-id="0e5a3-105">cut command</span></span>

<span data-ttu-id="0e5a3-106">Il comando taglia rimuove i dati dall'area di lavoro e li copia negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-106">The cut command removes data from the workspace and copies it to the clipboard.</span></span> <span data-ttu-id="0e5a3-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="0e5a3-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0e5a3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e5a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e5a3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0e5a3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0e5a3-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0e5a3-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0e5a3-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="0e5a3-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="0e5a3-114">Uno dei flag seguenti che identifica l'elemento da tagliare.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-114">One of the following flags identifying the item to cut.</span></span>



| <span data-ttu-id="0e5a3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0e5a3-115">Value</span></span>                 | <span data-ttu-id="0e5a3-116">Significato</span><span class="sxs-lookup"><span data-stu-id="0e5a3-116">Meaning</span></span>                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e5a3-117">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="0e5a3-117">at *rectangle*</span></span>        | <span data-ttu-id="0e5a3-118">Specifica la parte di ogni taglia del fotogramma.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-118">Specifies the portion of each frame cut.</span></span> <span data-ttu-id="0e5a3-119">Se omesso, il valore predefinito è l'intero frame.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-119">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="0e5a3-120">Quando si specifica questo elemento, i frame non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-120">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="0e5a3-121">L'area all'interno del rettangolo diventa invece nero.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-121">Instead the area inside the rectangle becomes black.</span></span>                                       |
| <span data-ttu-id="0e5a3-122">*flusso* del flusso audio</span><span class="sxs-lookup"><span data-stu-id="0e5a3-122">audio stream *stream*</span></span> | <span data-ttu-id="0e5a3-123">Specifica il flusso audio nell'area di lavoro interessata dal comando.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-123">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="0e5a3-124">Se si usa questo flag e si vuole anche tagliare video, è necessario usare anche il flag "flusso video".</span><span class="sxs-lookup"><span data-stu-id="0e5a3-124">If you use this flag and also want to cut video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="0e5a3-125">Se non viene specificato alcun flag, vengono tagliati tutti i flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-125">(If neither flag is specified, all audio and video streams are cut.)</span></span> |
| <span data-ttu-id="0e5a3-126">dalla *posizione*</span><span class="sxs-lookup"><span data-stu-id="0e5a3-126">from *position*</span></span>       | <span data-ttu-id="0e5a3-127">Specifica l'inizio del taglio dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-127">Specifies the start of the range cut.</span></span> <span data-ttu-id="0e5a3-128">Se omesso, il valore predefinito è la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-128">If omitted, it defaults to the current position.</span></span>                                                                                                                                                |
| <span data-ttu-id="0e5a3-129">*posizione*</span><span class="sxs-lookup"><span data-stu-id="0e5a3-129">to *position*</span></span>         | <span data-ttu-id="0e5a3-130">Specifica la fine del taglio dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-130">Specifies the end of the range cut.</span></span> <span data-ttu-id="0e5a3-131">Il taglio di dati audio e video è escluso da questa posizione.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-131">The audio and video data cut are exclusive of this position.</span></span> <span data-ttu-id="0e5a3-132">Se omesso, il valore predefinito è la fine dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-132">If omitted it defaults to the end of the workspace.</span></span>                                                                                  |
| <span data-ttu-id="0e5a3-133">*flusso* del flusso video</span><span class="sxs-lookup"><span data-stu-id="0e5a3-133">video stream *stream*</span></span> | <span data-ttu-id="0e5a3-134">Specifica il flusso video nell'area di lavoro interessata dal comando.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-134">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="0e5a3-135">Se si usa questo flag e si vuole anche tagliare audio, è necessario usare anche il flag "flusso audio".</span><span class="sxs-lookup"><span data-stu-id="0e5a3-135">If you use this flag and also want to cut audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="0e5a3-136">Se non viene specificato alcun flag, vengono tagliati tutti i flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-136">(If neither flag is specified, all audio and video streams are cut.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="0e5a3-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="0e5a3-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0e5a3-138">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-138">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="0e5a3-139">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0e5a3-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e5a3-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e5a3-140">Return Value</span></span>

<span data-ttu-id="0e5a3-141">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e5a3-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e5a3-142">Remarks</span></span>

<span data-ttu-id="0e5a3-143">La modifica diventa permanente solo quando i dati vengono salvati in modo esplicito; Tuttavia, la riproduzione funziona come se i dati fossero stati rimossi.</span><span class="sxs-lookup"><span data-stu-id="0e5a3-143">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e5a3-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e5a3-144">Requirements</span></span>



| <span data-ttu-id="0e5a3-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e5a3-145">Requirement</span></span> | <span data-ttu-id="0e5a3-146">Valore</span><span class="sxs-lookup"><span data-stu-id="0e5a3-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0e5a3-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e5a3-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0e5a3-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0e5a3-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0e5a3-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e5a3-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0e5a3-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0e5a3-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0e5a3-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e5a3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e5a3-152">MCI</span><span class="sxs-lookup"><span data-stu-id="0e5a3-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0e5a3-153">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="0e5a3-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

