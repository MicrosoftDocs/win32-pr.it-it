---
title: comando Quality
description: Il comando qualità definisce un livello di qualità personalizzato per la compressione di dati audio, video o di immagine continua. I dispositivi digitali video riconoscono questo comando.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- controllo qualità Windows Multimedia
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de9cc61d72db541b5f06d8903d7c9dcf153ce07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302352"
---
# <a name="quality-command"></a><span data-ttu-id="c9690-105">comando Quality</span><span class="sxs-lookup"><span data-stu-id="c9690-105">quality command</span></span>

<span data-ttu-id="c9690-106">Il comando qualità definisce un livello di qualità personalizzato per la compressione di dati audio, video o di immagine continua.</span><span class="sxs-lookup"><span data-stu-id="c9690-106">The quality command defines a custom quality level for either audio, video or still image data compression.</span></span> <span data-ttu-id="c9690-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="c9690-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="c9690-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c9690-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c9690-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9690-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9690-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c9690-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c9690-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c9690-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c9690-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="c9690-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c9690-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span><span class="sxs-lookup"><span data-stu-id="c9690-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span></span>
</dt> <dd>

<span data-ttu-id="c9690-114">Uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9690-114">One or more of the following flags.</span></span> <span data-ttu-id="c9690-115">(Uno dei tre flag "audio", "ancora" e "video" deve essere presente).</span><span class="sxs-lookup"><span data-stu-id="c9690-115">(One of the three flags "audio", "still", and "video" must be present.)</span></span>



| <span data-ttu-id="c9690-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c9690-116">Value</span></span>                 | <span data-ttu-id="c9690-117">Significato</span><span class="sxs-lookup"><span data-stu-id="c9690-117">Meaning</span></span>                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9690-118">algoritmo *algoritmo*</span><span class="sxs-lookup"><span data-stu-id="c9690-118">algorithm *algorithm*</span></span> | <span data-ttu-id="c9690-119">Associa il livello di qualità all' *algoritmo* specificato.</span><span class="sxs-lookup"><span data-stu-id="c9690-119">Associates the quality level with the specified *algorithm*.</span></span> <span data-ttu-id="c9690-120">Questo *algoritmo* deve essere supportato dal dispositivo ed essere compatibile con il flag "audio", "ancora" o "video" usato.</span><span class="sxs-lookup"><span data-stu-id="c9690-120">This *algorithm* must be supported by the device and be compatible with the "audio", "still", or "video" flag that is used.</span></span> <span data-ttu-id="c9690-121">Se omesso, viene utilizzato l'algoritmo corrente.</span><span class="sxs-lookup"><span data-stu-id="c9690-121">If omitted, the current algorithm is used.</span></span> |
| <span data-ttu-id="c9690-122">*nome* audio</span><span class="sxs-lookup"><span data-stu-id="c9690-122">audio *name*</span></span>          | <span data-ttu-id="c9690-123">Indica che questo comando specifica un livello di qualità "audio" identificato con il *nome*.</span><span class="sxs-lookup"><span data-stu-id="c9690-123">Indicates this command specifies an "audio" quality level identified with *name*.</span></span>                                                                                                                                                   |
| <span data-ttu-id="c9690-124">dialogo</span><span class="sxs-lookup"><span data-stu-id="c9690-124">dialog</span></span>                | <span data-ttu-id="c9690-125">Richiede che il dispositivo visualizzi una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c9690-125">Requests that the device display a dialog box.</span></span> <span data-ttu-id="c9690-126">Questa finestra di dialogo contiene campi specifici dell'algoritmo che vengono usati internamente dal dispositivo per creare la struttura che descrive un livello di qualità specifico.</span><span class="sxs-lookup"><span data-stu-id="c9690-126">This dialog box has algorithm-specific fields that are used internally by the device to create the structure describing a specific quality level.</span></span>                                    |
| <span data-ttu-id="c9690-127">handle *handle*</span><span class="sxs-lookup"><span data-stu-id="c9690-127">handle *handle*</span></span>       | <span data-ttu-id="c9690-128">Specifica un *handle* per una struttura che contiene dati specifici dell'algoritmo che descrivono un livello di qualità specifico.</span><span class="sxs-lookup"><span data-stu-id="c9690-128">Specifies a *handle* to a structure that contains algorithmic-specific data describing a specific quality level.</span></span> <span data-ttu-id="c9690-129">Le strutture per i dati a cui fa riferimento questo handle sono specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9690-129">The structures for the data referenced by this handle are device specific.</span></span>                                         |
| <span data-ttu-id="c9690-130">*nome* ancora</span><span class="sxs-lookup"><span data-stu-id="c9690-130">still *name*</span></span>          | <span data-ttu-id="c9690-131">Indica che il comando specifica un livello di qualità "ancora" identificato con il *nome.*</span><span class="sxs-lookup"><span data-stu-id="c9690-131">Indicates the command specifies a "still" quality level identified with *name.*</span></span>                                                                                                                                                     |
| <span data-ttu-id="c9690-132">*nome* del video</span><span class="sxs-lookup"><span data-stu-id="c9690-132">video *name*</span></span>          | <span data-ttu-id="c9690-133">Indica che il comando specifica un livello di qualità "video" identificato con il *nome*.</span><span class="sxs-lookup"><span data-stu-id="c9690-133">Indicates the command specifies a "video" quality level identified with *name*.</span></span>                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="c9690-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c9690-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c9690-135">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="c9690-135">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="c9690-136">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c9690-136">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9690-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9690-137">Return Value</span></span>

<span data-ttu-id="c9690-138">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="c9690-138">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9690-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9690-139">Remarks</span></span>

<span data-ttu-id="c9690-140">Questo comando definisce un nome di stringa per il livello di qualità, che può quindi essere utilizzato in un comando [sevideo](setvideo.md) "Quality", sevideo "still Quality [" o "Quality",](setaudio.md) per stabilirlo come il video corrente, ancora o il livello di qualità della compressione audio.</span><span class="sxs-lookup"><span data-stu-id="c9690-140">This command defines a string name for the quality level, which can then be used in a [setvideo](setvideo.md) "quality", setvideo "still quality", or [setaudio](setaudio.md) "quality" command to establish it as the current video, still, or audio-compression quality level.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9690-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9690-141">Requirements</span></span>



| <span data-ttu-id="c9690-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9690-142">Requirement</span></span> | <span data-ttu-id="c9690-143">Valore</span><span class="sxs-lookup"><span data-stu-id="c9690-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c9690-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9690-144">Minimum supported client</span></span><br/> | <span data-ttu-id="c9690-145">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c9690-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c9690-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9690-146">Minimum supported server</span></span><br/> | <span data-ttu-id="c9690-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c9690-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c9690-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9690-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9690-149">MCI</span><span class="sxs-lookup"><span data-stu-id="c9690-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c9690-150">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="c9690-150">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c9690-151">SetAudio</span><span class="sxs-lookup"><span data-stu-id="c9690-151">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="c9690-152">video</span><span class="sxs-lookup"><span data-stu-id="c9690-152">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

