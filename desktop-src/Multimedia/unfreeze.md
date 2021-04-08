---
title: Sblocca comando
description: Il comando Unfreeze riabilita l'acquisizione video nel buffer del frame dopo che è stata disabilitata tramite il comando Freeze. I dispositivi Digital-video, VCR e overlay video riconoscono questo comando.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- sbloccare il comando Windows Multimedia
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743559"
---
# <a name="unfreeze-command"></a><span data-ttu-id="c3f6a-105">Sblocca comando</span><span class="sxs-lookup"><span data-stu-id="c3f6a-105">unfreeze command</span></span>

<span data-ttu-id="c3f6a-106">Il comando Unfreeze riabilita l'acquisizione video nel buffer del frame dopo che è stata disabilitata tramite il comando [Freeze](freeze.md) .</span><span class="sxs-lookup"><span data-stu-id="c3f6a-106">The unfreeze command reenables video acquisition to the frame buffer after it has been disabled by the [freeze](freeze.md) command.</span></span> <span data-ttu-id="c3f6a-107">I dispositivi Digital-video, VCR e overlay video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="c3f6a-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c3f6a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3f6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3f6a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c3f6a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c3f6a-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c3f6a-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c3f6a-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span><span class="sxs-lookup"><span data-stu-id="c3f6a-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="c3f6a-114">Flag per la riabilitazione dell'acquisizione video nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-114">Flag for reenabling video acquisition to the frame buffer.</span></span> <span data-ttu-id="c3f6a-115">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Unfreeze** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-115">The following table lists device types that recognize the **unfreeze** command and the flags used by each type.</span></span>



| <span data-ttu-id="c3f6a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c3f6a-116">Value</span></span>        | <span data-ttu-id="c3f6a-117">Significato</span><span class="sxs-lookup"><span data-stu-id="c3f6a-117">Meaning</span></span>        |
|--------------|----------------|
| <span data-ttu-id="c3f6a-118">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="c3f6a-118">digitalvideo</span></span> | <span data-ttu-id="c3f6a-119">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c3f6a-119">at *rectangle*</span></span> |
| <span data-ttu-id="c3f6a-120">overlay</span><span class="sxs-lookup"><span data-stu-id="c3f6a-120">overlay</span></span>      | <span data-ttu-id="c3f6a-121">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c3f6a-121">at *rectangle*</span></span> |
| <span data-ttu-id="c3f6a-122">VCR</span><span class="sxs-lookup"><span data-stu-id="c3f6a-122">vcr</span></span>          | <span data-ttu-id="c3f6a-123">input output</span><span class="sxs-lookup"><span data-stu-id="c3f6a-123">input output</span></span>   |



 

<span data-ttu-id="c3f6a-124">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszUnfreeze** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-124">The following table lists the flags that can be specified in the **lpszUnfreeze** parameter and their meanings.</span></span>



| <span data-ttu-id="c3f6a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c3f6a-125">Value</span></span>          | <span data-ttu-id="c3f6a-126">Significato</span><span class="sxs-lookup"><span data-stu-id="c3f6a-126">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f6a-127">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c3f6a-127">at *rectangle*</span></span> | <span data-ttu-id="c3f6a-128">Specifica l'area in cui sarà riabilitata l'acquisizione dei video.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-128">Specifies the region that will have video acquisition reenabled.</span></span> <span data-ttu-id="c3f6a-129">Il rettangolo è relativo all'origine del buffer video ed è specificato come *X1 Y1 Y1 2*.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-129">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="c3f6a-130">Le coordinate *X1 Y1* specificano l'angolo superiore sinistro del rettangolo e le coordinate *X2 Y2* specificano la larghezza e l'altezza.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-130">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="c3f6a-131">input</span><span class="sxs-lookup"><span data-stu-id="c3f6a-131">input</span></span>          | <span data-ttu-id="c3f6a-132">Sbloccare l'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-132">Unfreeze the input image.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c3f6a-133">output</span><span class="sxs-lookup"><span data-stu-id="c3f6a-133">output</span></span>         | <span data-ttu-id="c3f6a-134">Sbloccare l'immagine di output.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-134">Unfreeze the output image.</span></span> <span data-ttu-id="c3f6a-135">Se non viene specificato né "input" né "output", viene utilizzato "output".</span><span class="sxs-lookup"><span data-stu-id="c3f6a-135">If neither "input" nor "output" is given, "output" is assumed.</span></span>                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="c3f6a-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c3f6a-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c3f6a-137">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-137">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c3f6a-138">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="c3f6a-138">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="c3f6a-139">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c3f6a-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3f6a-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3f6a-140">Return Value</span></span>

<span data-ttu-id="c3f6a-141">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="c3f6a-142">Esempio</span><span class="sxs-lookup"><span data-stu-id="c3f6a-142">Examples</span></span>

<span data-ttu-id="c3f6a-143">Il comando seguente Sblocca un'area del buffer video.</span><span class="sxs-lookup"><span data-stu-id="c3f6a-143">The following command unfreezes a region of the video buffer.</span></span>

``` syntax
unfreeze vboard at 10 20 90 165
```

## <a name="requirements"></a><span data-ttu-id="c3f6a-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3f6a-144">Requirements</span></span>



| <span data-ttu-id="c3f6a-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3f6a-145">Requirement</span></span> | <span data-ttu-id="c3f6a-146">Valore</span><span class="sxs-lookup"><span data-stu-id="c3f6a-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c3f6a-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3f6a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f6a-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c3f6a-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c3f6a-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3f6a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f6a-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c3f6a-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c3f6a-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3f6a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f6a-152">MCI</span><span class="sxs-lookup"><span data-stu-id="c3f6a-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c3f6a-153">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="c3f6a-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c3f6a-154">congelare</span><span class="sxs-lookup"><span data-stu-id="c3f6a-154">freeze</span></span>](freeze.md)
</dt> </dl>

 

