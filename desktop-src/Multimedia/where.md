---
title: comando Where
description: Il comando WHERE recupera il rettangolo che specifica l'area di origine o di destinazione. Questo rettangolo è stato specificato utilizzando il comando put. I dispositivi Digital-video e overlay video riconoscono questo comando.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- comando Where Windows Multimedia
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964778"
---
# <a name="where-command"></a><span data-ttu-id="24f84-106">comando Where</span><span class="sxs-lookup"><span data-stu-id="24f84-106">where command</span></span>

<span data-ttu-id="24f84-107">Il comando WHERE recupera il rettangolo che specifica l'area di origine o di destinazione.</span><span class="sxs-lookup"><span data-stu-id="24f84-107">The where command retrieves the rectangle specifying the source or destination area.</span></span> <span data-ttu-id="24f84-108">Questo rettangolo è stato specificato utilizzando il comando [put](put.md) .</span><span class="sxs-lookup"><span data-stu-id="24f84-108">This rectangle was specified using the [put](put.md) command.</span></span> <span data-ttu-id="24f84-109">I dispositivi Digital-video e overlay video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="24f84-109">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="24f84-110">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="24f84-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="24f84-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="24f84-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f84-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="24f84-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="24f84-113">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="24f84-113">Identifier of an MCI device.</span></span> <span data-ttu-id="24f84-114">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="24f84-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="24f84-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span><span class="sxs-lookup"><span data-stu-id="24f84-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span></span>
</dt> <dd>

<span data-ttu-id="24f84-116">Flag che identifica il rettangolo le cui dimensioni vengono recuperate.</span><span class="sxs-lookup"><span data-stu-id="24f84-116">Flag that identifies the rectangle whose dimensions are retrieved.</span></span> <span data-ttu-id="24f84-117">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **where** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="24f84-117">The following table lists device types that recognize the **where** command and the flags used by each type.</span></span>



| <span data-ttu-id="24f84-118">Valore</span><span class="sxs-lookup"><span data-stu-id="24f84-118">Value</span></span>        | <span data-ttu-id="24f84-119">Significato</span><span class="sxs-lookup"><span data-stu-id="24f84-119">Meaning</span></span>                                                       | <span data-ttu-id="24f84-120">Significato</span><span class="sxs-lookup"><span data-stu-id="24f84-120">Meaning</span></span>                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="24f84-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="24f84-121">digitalvideo</span></span> | <span data-ttu-id="24f84-122">destinationdestination [**Max**](max.md)frameFrame maxsource</span><span class="sxs-lookup"><span data-stu-id="24f84-122">destinationdestination [**max**](max.md)frameframe maxsource</span></span> | <span data-ttu-id="24f84-123">maxvideovideo di origine maxwindowwindow max</span><span class="sxs-lookup"><span data-stu-id="24f84-123">source maxvideovideo maxwindowwindow max</span></span> |
| <span data-ttu-id="24f84-124">overlay</span><span class="sxs-lookup"><span data-stu-id="24f84-124">overlay</span></span>      | <span data-ttu-id="24f84-125">destinationframe</span><span class="sxs-lookup"><span data-stu-id="24f84-125">destinationframe</span></span>                                              | <span data-ttu-id="24f84-126">sourcevideo</span><span class="sxs-lookup"><span data-stu-id="24f84-126">sourcevideo</span></span>                              |



 

<span data-ttu-id="24f84-127">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszRequestRect** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="24f84-127">The following table lists the flags that can be specified in the **lpszRequestRect** parameter and their meanings.</span></span>



| <span data-ttu-id="24f84-128">Valore</span><span class="sxs-lookup"><span data-stu-id="24f84-128">Value</span></span>                          | <span data-ttu-id="24f84-129">Significato</span><span class="sxs-lookup"><span data-stu-id="24f84-129">Meaning</span></span>                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24f84-130">destination</span><span class="sxs-lookup"><span data-stu-id="24f84-130">destination</span></span>                    | <span data-ttu-id="24f84-131">Recupera l'offset e l'extent di destinazione.</span><span class="sxs-lookup"><span data-stu-id="24f84-131">Retrieves the destination offset and extent.</span></span> <span data-ttu-id="24f84-132">Per i dispositivi con sovrimpressione video, il rettangolo di destinazione definisce l'area dell'area client della finestra di visualizzazione che consente di visualizzare i dati dell'immagine dal buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="24f84-132">For video-overlay devices, the destination rectangle defines the area of the display window client area that displays the image data from the frame buffer.</span></span>                                                                                             |
| <span data-ttu-id="24f84-133">[ **massimo** destinazione](max.md)</span><span class="sxs-lookup"><span data-stu-id="24f84-133">destination [**max**](max.md)</span></span> | <span data-ttu-id="24f84-134">Recupera le dimensioni correnti del rettangolo client.</span><span class="sxs-lookup"><span data-stu-id="24f84-134">Retrieves the current size of the client rectangle.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="24f84-135">frame</span><span class="sxs-lookup"><span data-stu-id="24f84-135">frame</span></span>                          | <span data-ttu-id="24f84-136">Recupera l'offset e l'extent del rettangolo del buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="24f84-136">Retrieves the offset and extent of the frame buffer rectangle.</span></span> <span data-ttu-id="24f84-137">Il rettangolo del buffer del frame definisce l'area del buffer del frame che riceve i dati video in arrivo.</span><span class="sxs-lookup"><span data-stu-id="24f84-137">The frame buffer rectangle defines the area of the frame buffer that receives incoming video data.</span></span> <span data-ttu-id="24f84-138">Le immagini del rettangolo "video" vengono ridimensionate in questa area.</span><span class="sxs-lookup"><span data-stu-id="24f84-138">Images from the "video" rectangle are scaled into this region.</span></span>                                                                     |
| <span data-ttu-id="24f84-139">[ **massimo** frame](max.md)</span><span class="sxs-lookup"><span data-stu-id="24f84-139">frame [**max**](max.md)</span></span>       | <span data-ttu-id="24f84-140">Restituisce la dimensione massima del buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="24f84-140">Returns the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="24f84-141">source</span><span class="sxs-lookup"><span data-stu-id="24f84-141">source</span></span>                         | <span data-ttu-id="24f84-142">Recupera l'offset di origine e l'extent.</span><span class="sxs-lookup"><span data-stu-id="24f84-142">Retrieves the source offset and extent.</span></span> <span data-ttu-id="24f84-143">Per i dispositivi con sovrimpressione video, il rettangolo di origine definisce l'area del buffer del frame visualizzato nella finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="24f84-143">For video-overlay devices, the source rectangle defines the region of the frame buffer that is displayed in the destination window.</span></span> <span data-ttu-id="24f84-144">Il dispositivo utilizza questo rettangolo per ritagliare l'immagine prima che sia adattata al rettangolo di destinazione sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="24f84-144">The device uses this rectangle to crop the image before it is stretched to fit the destination rectangle on the display.</span></span> |
| <span data-ttu-id="24f84-145">[ **numero massimo** di origine](max.md)</span><span class="sxs-lookup"><span data-stu-id="24f84-145">source [**max**](max.md)</span></span>      | <span data-ttu-id="24f84-146">Recupera la dimensione massima del buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="24f84-146">Retrieves the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="24f84-147">Video</span><span class="sxs-lookup"><span data-stu-id="24f84-147">video</span></span>                          | <span data-ttu-id="24f84-148">Recupera l'offset e l'extent del rettangolo video.</span><span class="sxs-lookup"><span data-stu-id="24f84-148">Retrieves the offset and extent of the video rectangle.</span></span> <span data-ttu-id="24f84-149">Il rettangolo video definisce l'area dei dati video in arrivo trasferiti al buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="24f84-149">The video rectangle defines the region of the incoming video data that is transferred to the frame buffer.</span></span>                                                                                                                                   |
| <span data-ttu-id="24f84-150">[ **massimo** video](max.md)</span><span class="sxs-lookup"><span data-stu-id="24f84-150">video [**max**](max.md)</span></span>       | <span data-ttu-id="24f84-151">Restituisce la dimensione massima dell'input.</span><span class="sxs-lookup"><span data-stu-id="24f84-151">Returns the maximum size of the input.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="24f84-152">Finestra</span><span class="sxs-lookup"><span data-stu-id="24f84-152">window</span></span>                         | <span data-ttu-id="24f84-153">Recupera le dimensioni e la posizione correnti della cornice della finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="24f84-153">Retrieves the current size and position of the display-window frame.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="24f84-154">[ **massimo** finestra](max.md)</span><span class="sxs-lookup"><span data-stu-id="24f84-154">window [**max**](max.md)</span></span>      | <span data-ttu-id="24f84-155">Recupera le dimensioni dell'intero schermo.</span><span class="sxs-lookup"><span data-stu-id="24f84-155">Retrieves the size of the entire display.</span></span>                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="24f84-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="24f84-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="24f84-157">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="24f84-157">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="24f84-158">Per i dispositivi digitali video è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="24f84-158">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="24f84-159">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="24f84-159">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f84-160">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24f84-160">Return Value</span></span>

<span data-ttu-id="24f84-161">Restituisce un rettangolo nel parametro *lpszReturnString* della funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="24f84-161">Returns a rectangle in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="24f84-162">Il rettangolo descrive l'area specificata nel parametro *lpszRequestRect* di questo comando.</span><span class="sxs-lookup"><span data-stu-id="24f84-162">The rectangle describes the area specified in the *lpszRequestRect* parameter of this command.</span></span> <span data-ttu-id="24f84-163">Il rettangolo viene specificato come *X1 Y1 Y1 2*.</span><span class="sxs-lookup"><span data-stu-id="24f84-163">The rectangle is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="24f84-164">Le coordinate *X1 Y1* specificano l'angolo superiore sinistro del rettangolo e le coordinate *X2 Y2* specificano la larghezza e l'altezza.</span><span class="sxs-lookup"><span data-stu-id="24f84-164">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span>

## <a name="examples"></a><span data-ttu-id="24f84-165">Esempio</span><span class="sxs-lookup"><span data-stu-id="24f84-165">Examples</span></span>

<span data-ttu-id="24f84-166">Il comando seguente restituisce il rettangolo di visualizzazione del dispositivo "Movie".</span><span class="sxs-lookup"><span data-stu-id="24f84-166">The following command returns the display rectangle of the "movie" device.</span></span>

``` syntax
where movie destination
```

## <a name="requirements"></a><span data-ttu-id="24f84-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24f84-167">Requirements</span></span>



| <span data-ttu-id="24f84-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="24f84-168">Requirement</span></span> | <span data-ttu-id="24f84-169">Valore</span><span class="sxs-lookup"><span data-stu-id="24f84-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="24f84-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24f84-170">Minimum supported client</span></span><br/> | <span data-ttu-id="24f84-171">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24f84-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="24f84-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24f84-172">Minimum supported server</span></span><br/> | <span data-ttu-id="24f84-173">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24f84-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="24f84-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24f84-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f84-175">MCI</span><span class="sxs-lookup"><span data-stu-id="24f84-175">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="24f84-176">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="24f84-176">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="24f84-177">mettere</span><span class="sxs-lookup"><span data-stu-id="24f84-177">put</span></span>](put.md)
</dt> </dl>

 

