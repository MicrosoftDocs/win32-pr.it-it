---
title: comando Capture
description: Il comando Capture copia il contenuto del buffer del frame e lo archivia nel file specificato. I dispositivi digitali video riconoscono questo comando.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- comando Acquisisci Windows Multimedia
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121263"
---
# <a name="capture-command"></a><span data-ttu-id="6b8de-105">comando Capture</span><span class="sxs-lookup"><span data-stu-id="6b8de-105">capture command</span></span>

<span data-ttu-id="6b8de-106">Il comando Capture copia il contenuto del buffer del frame e lo archivia nel file specificato.</span><span class="sxs-lookup"><span data-stu-id="6b8de-106">The capture command copies the contents of the frame buffer and stores it in the specified file.</span></span> <span data-ttu-id="6b8de-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="6b8de-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6b8de-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="6b8de-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6b8de-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b8de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b8de-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6b8de-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6b8de-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="6b8de-111">Identifier of an MCI device.</span></span> <span data-ttu-id="6b8de-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="6b8de-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6b8de-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span><span class="sxs-lookup"><span data-stu-id="6b8de-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span></span>
</dt> <dd>

<span data-ttu-id="6b8de-114">Uno o più dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b8de-114">One or more of the following flags:</span></span>



| <span data-ttu-id="6b8de-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8de-115">Value</span></span>          | <span data-ttu-id="6b8de-116">Significato</span><span class="sxs-lookup"><span data-stu-id="6b8de-116">Meaning</span></span>                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8de-117">*nome percorso*</span><span class="sxs-lookup"><span data-stu-id="6b8de-117">as *pathname*</span></span>  | <span data-ttu-id="6b8de-118">Specifica il percorso e il nome file di destinazione per l'immagine acquisita.</span><span class="sxs-lookup"><span data-stu-id="6b8de-118">Specifies the destination path and filename for the captured image.</span></span> <span data-ttu-id="6b8de-119">Questo flag è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6b8de-119">This flag is required.</span></span>                                                                                                                                                                |
| <span data-ttu-id="6b8de-120">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="6b8de-120">at *rectangle*</span></span> | <span data-ttu-id="6b8de-121">Specifica l'area rettangolare all'interno del buffer di frame che il dispositivo Ritaglia e Salva su disco.</span><span class="sxs-lookup"><span data-stu-id="6b8de-121">Specifies the rectangular region within the frame buffer that the device crops and saves to disk.</span></span> <span data-ttu-id="6b8de-122">Se omesso, l'area ritagliata viene impostata per impostazione predefinita sul rettangolo specificato o impostato come predefinito in un comando [put](put.md) "Source" precedente per questa istanza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b8de-122">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [put](put.md) "source" command for this device instance.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6b8de-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6b8de-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6b8de-124">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="6b8de-124">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="6b8de-125">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6b8de-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b8de-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b8de-126">Return Value</span></span>

<span data-ttu-id="6b8de-127">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="6b8de-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b8de-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b8de-128">Remarks</span></span>

<span data-ttu-id="6b8de-129">Questo comando può avere esito negativo se il dispositivo sta attualmente eseguendo il video di movimento o se è in esecuzione un'altra operazione a elevato utilizzo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b8de-129">This command might fail if the device is currently playing motion video or executing some other resource-intensive operation.</span></span> <span data-ttu-id="6b8de-130">Se il buffer del frame viene aggiornato in tempo reale, l'aggiornamento viene momentaneamente sospeso in modo che venga acquisita un'immagine completa.</span><span class="sxs-lookup"><span data-stu-id="6b8de-130">If the frame buffer is being updated in real time, the updating momentarily pauses so that a complete image is captured.</span></span> <span data-ttu-id="6b8de-131">Se il dispositivo sospende l'aggiornamento, è possibile che si verifichi un effetto visivo o acustico.</span><span class="sxs-lookup"><span data-stu-id="6b8de-131">If the device pauses the updating, there might be a visual or audible effect.</span></span> <span data-ttu-id="6b8de-132">Se il formato di file, l'algoritmo di compressione e i livelli di qualità non sono stati impostati, vengono usate le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="6b8de-132">If the file format, compression algorithm, and quality levels have not been set, their defaults are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8de-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b8de-133">Requirements</span></span>



| <span data-ttu-id="6b8de-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b8de-134">Requirement</span></span> | <span data-ttu-id="6b8de-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8de-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6b8de-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8de-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6b8de-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b8de-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6b8de-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8de-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6b8de-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b8de-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6b8de-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b8de-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8de-141">MCI</span><span class="sxs-lookup"><span data-stu-id="6b8de-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6b8de-142">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="6b8de-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="6b8de-143">mettere</span><span class="sxs-lookup"><span data-stu-id="6b8de-143">put</span></span>](put.md)
</dt> </dl>

 

