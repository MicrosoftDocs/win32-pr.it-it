---
title: Copy (comando)
description: Il comando copy copia i dati negli Appunti. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- Copia comando Windows Multimedia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740498"
---
# <a name="copy-command"></a><span data-ttu-id="8f25b-105">Copy (comando)</span><span class="sxs-lookup"><span data-stu-id="8f25b-105">copy command</span></span>

<span data-ttu-id="8f25b-106">Il comando copy copia i dati negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="8f25b-106">The copy command copies data to the clipboard.</span></span> <span data-ttu-id="8f25b-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="8f25b-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="8f25b-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8f25b-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="8f25b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f25b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f25b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8f25b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8f25b-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="8f25b-111">Identifier of an MCI device.</span></span> <span data-ttu-id="8f25b-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="8f25b-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="8f25b-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="8f25b-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="8f25b-114">Uno dei flag seguenti che identifica l'elemento da copiare.</span><span class="sxs-lookup"><span data-stu-id="8f25b-114">One of the following flags identifying the item to copy.</span></span>



| <span data-ttu-id="8f25b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8f25b-115">Value</span></span>                 | <span data-ttu-id="8f25b-116">Significato</span><span class="sxs-lookup"><span data-stu-id="8f25b-116">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f25b-117">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="8f25b-117">at *rectangle*</span></span>        | <span data-ttu-id="8f25b-118">Specifica la parte di ogni frame che verrà copiato.</span><span class="sxs-lookup"><span data-stu-id="8f25b-118">Specifies the portion of each frame that will be copied.</span></span> <span data-ttu-id="8f25b-119">Se omesso, l'impostazione predefinita è l'intero frame.</span><span class="sxs-lookup"><span data-stu-id="8f25b-119">If omitted, the default setting is the entire frame.</span></span>                                                                                                                             |
| <span data-ttu-id="8f25b-120">*flusso* del flusso audio</span><span class="sxs-lookup"><span data-stu-id="8f25b-120">audio stream *stream*</span></span> | <span data-ttu-id="8f25b-121">Specifica il flusso audio nell'area di lavoro interessata dal comando.</span><span class="sxs-lookup"><span data-stu-id="8f25b-121">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="8f25b-122">Se si usa questo flag e si vuole anche copiare il video, è necessario usare anche il flag "flusso video".</span><span class="sxs-lookup"><span data-stu-id="8f25b-122">If you use this flag and also want to copy video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="8f25b-123">Se non viene specificato alcun flag, vengono copiati tutti i flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="8f25b-123">(If neither flag is specified, all audio and video streams are copied.)</span></span> |
| <span data-ttu-id="8f25b-124">dalla *posizione*</span><span class="sxs-lookup"><span data-stu-id="8f25b-124">from *position*</span></span>       | <span data-ttu-id="8f25b-125">Specifica l'inizio dell'intervallo copiato.</span><span class="sxs-lookup"><span data-stu-id="8f25b-125">Specifies the start of the range copied.</span></span> <span data-ttu-id="8f25b-126">Se omesso, l'impostazione predefinita è la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="8f25b-126">If omitted, the default setting is the current position.</span></span>                                                                                                                                         |
| <span data-ttu-id="8f25b-127">*posizione*</span><span class="sxs-lookup"><span data-stu-id="8f25b-127">to *position*</span></span>         | <span data-ttu-id="8f25b-128">Specifica la fine dell'intervallo copiato.</span><span class="sxs-lookup"><span data-stu-id="8f25b-128">Specifies the end of the range copied.</span></span> <span data-ttu-id="8f25b-129">I dati audio e video copiati sono esclusivi di questa posizione.</span><span class="sxs-lookup"><span data-stu-id="8f25b-129">The audio and video data copied are exclusive of this position.</span></span> <span data-ttu-id="8f25b-130">Se omesso, l'impostazione predefinita è la fine dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8f25b-130">If omitted, the default setting is the end of the workspace.</span></span>                                                                       |
| <span data-ttu-id="8f25b-131">*flusso* del flusso video</span><span class="sxs-lookup"><span data-stu-id="8f25b-131">video stream *stream*</span></span> | <span data-ttu-id="8f25b-132">Specifica il flusso video nell'area di lavoro interessata dal comando.</span><span class="sxs-lookup"><span data-stu-id="8f25b-132">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="8f25b-133">Se si usa questo flag e si vuole anche copiare l'audio, è necessario usare anche il flag "flusso audio".</span><span class="sxs-lookup"><span data-stu-id="8f25b-133">If you use this flag and also want to copy audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="8f25b-134">Se non viene specificato alcun flag, vengono copiati tutti i flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="8f25b-134">(If neither flag is specified, all audio and video streams are copied.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="8f25b-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="8f25b-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8f25b-136">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="8f25b-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="8f25b-137">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8f25b-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f25b-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f25b-138">Return Value</span></span>

<span data-ttu-id="8f25b-139">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="8f25b-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f25b-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f25b-140">Requirements</span></span>



| <span data-ttu-id="8f25b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f25b-141">Requirement</span></span> | <span data-ttu-id="8f25b-142">Valore</span><span class="sxs-lookup"><span data-stu-id="8f25b-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8f25b-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f25b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8f25b-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f25b-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8f25b-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f25b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8f25b-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f25b-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8f25b-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f25b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f25b-148">MCI</span><span class="sxs-lookup"><span data-stu-id="8f25b-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8f25b-149">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="8f25b-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

