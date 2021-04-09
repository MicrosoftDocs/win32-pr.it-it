---
title: Put (comando)
description: Il comando put definisce l'area dell'immagine di origine e della finestra di destinazione utilizzata per la visualizzazione. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- inserire i contenuti multimediali di Windows
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121122"
---
# <a name="put-command"></a><span data-ttu-id="c77c1-105">Put (comando)</span><span class="sxs-lookup"><span data-stu-id="c77c1-105">put command</span></span>

<span data-ttu-id="c77c1-106">Il comando put definisce l'area dell'immagine di origine e della finestra di destinazione utilizzata per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c77c1-106">The put command defines the area of the source image and destination window used for display.</span></span> <span data-ttu-id="c77c1-107">I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="c77c1-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="c77c1-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c77c1-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c77c1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c77c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c77c1-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c77c1-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c77c1-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c77c1-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c77c1-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="c77c1-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c77c1-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span><span class="sxs-lookup"><span data-stu-id="c77c1-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span></span>
</dt> <dd>

<span data-ttu-id="c77c1-114">Flag per la definizione dell'area.</span><span class="sxs-lookup"><span data-stu-id="c77c1-114">Flag for defining the area.</span></span> <span data-ttu-id="c77c1-115">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando put e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="c77c1-115">The following table lists device types that recognize the put command and the flags used by each type.</span></span>



| <span data-ttu-id="c77c1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c77c1-116">Value</span></span>        | <span data-ttu-id="c77c1-117">Significato</span><span class="sxs-lookup"><span data-stu-id="c77c1-117">Meaning</span></span>                                                                                      | <span data-ttu-id="c77c1-118">Significato</span><span class="sxs-lookup"><span data-stu-id="c77c1-118">Meaning</span></span>                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c77c1-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="c77c1-119">digitalvideo</span></span> | <span data-ttu-id="c77c1-120">destinazione destinazione al frame frame *rettangolo* all'origine di origine *rettangolo* al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c77c1-120">destination destination at *rectangle* frame frame at *rectangle* source source at *rectangle*</span></span> | <span data-ttu-id="c77c1-121">video video sulla finestra della finestra *rettangolare* nel client della finestra del client della finestra *rettangolare* al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c77c1-121">video video at *rectangle* window window at *rectangle* window client window client at *rectangle*</span></span> |
| <span data-ttu-id="c77c1-122">overlay</span><span class="sxs-lookup"><span data-stu-id="c77c1-122">overlay</span></span>      | <span data-ttu-id="c77c1-123">destinazione destinazione al frame frame *rettangolo* al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c77c1-123">destination destination at *rectangle* frame frame at *rectangle*</span></span>                             | <span data-ttu-id="c77c1-124">origine di origine in un video video *rettangolare* nel *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c77c1-124">source source at *rectangle* video video at *rectangle*</span></span>                                           |



 

<span data-ttu-id="c77c1-125">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszRegions** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="c77c1-125">The following table lists the flags that can be specified in the **lpszRegions** parameter and their meanings.</span></span>



| <span data-ttu-id="c77c1-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c77c1-126">Value</span></span>                        | <span data-ttu-id="c77c1-127">Significato</span><span class="sxs-lookup"><span data-stu-id="c77c1-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c77c1-128">destination</span><span class="sxs-lookup"><span data-stu-id="c77c1-128">destination</span></span>                  | <span data-ttu-id="c77c1-129">Consente di selezionare l'intera area client della finestra di destinazione in cui visualizzare i dati.</span><span class="sxs-lookup"><span data-stu-id="c77c1-129">Selects the entire client area of the destination window to display the data.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c77c1-130">destinazione al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c77c1-130">destination at *rectangle*</span></span>   | <span data-ttu-id="c77c1-131">Seleziona una parte dell'area client della finestra di destinazione utilizzata per visualizzare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="c77c1-131">Selects a portion of the client area of the destination window used to display the image.</span></span> <span data-ttu-id="c77c1-132">Quando si specifica un'area della finestra di visualizzazione e il dispositivo supporta l'estensione, l'immagine di origine viene allungata all'offset e all'extent di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c77c1-132">When an area of the display window is specified and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                     |
| <span data-ttu-id="c77c1-133">frame</span><span class="sxs-lookup"><span data-stu-id="c77c1-133">frame</span></span>                        | <span data-ttu-id="c77c1-134">Seleziona l'intero buffer di frame per ricevere le immagini video in arrivo.</span><span class="sxs-lookup"><span data-stu-id="c77c1-134">Selects the entire frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c77c1-135">cornice al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c77c1-135">frame at *rectangle*</span></span>         | <span data-ttu-id="c77c1-136">Seleziona una parte del buffer del frame per ricevere le immagini video in arrivo.</span><span class="sxs-lookup"><span data-stu-id="c77c1-136">Selects a portion of the frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c77c1-137">source</span><span class="sxs-lookup"><span data-stu-id="c77c1-137">source</span></span>                       | <span data-ttu-id="c77c1-138">Consente di selezionare l'intera immagine da visualizzare nella finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c77c1-138">Selects the entire image for display in the destination window.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="c77c1-139">origine al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c77c1-139">source at *rectangle*</span></span>        | <span data-ttu-id="c77c1-140">Seleziona una parte dell'immagine da visualizzare nella finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c77c1-140">Selects a portion of the image to display in the destination window.</span></span> <span data-ttu-id="c77c1-141">Quando si specifica un'area dell'immagine di origine e il dispositivo supporta l'estensione, l'immagine di origine viene allungata all'offset e all'extent di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c77c1-141">When an area of the source image is specified, and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                                           |
| <span data-ttu-id="c77c1-142">Video</span><span class="sxs-lookup"><span data-stu-id="c77c1-142">video</span></span>                        | <span data-ttu-id="c77c1-143">Seleziona l'intera immagine video in ingresso da acquisire nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="c77c1-143">Selects the entire incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c77c1-144">video al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c77c1-144">video at *rectangle*</span></span>         | <span data-ttu-id="c77c1-145">Seleziona una parte dell'immagine video in ingresso da acquisire nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="c77c1-145">Selects a portion of the incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c77c1-146">Finestra</span><span class="sxs-lookup"><span data-stu-id="c77c1-146">window</span></span>                       | <span data-ttu-id="c77c1-147">Ripristina le dimensioni iniziali della finestra sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="c77c1-147">Restores the initial window size on the display.</span></span> <span data-ttu-id="c77c1-148">Questo comando Visualizza anche la finestra.</span><span class="sxs-lookup"><span data-stu-id="c77c1-148">This command also displays the window.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c77c1-149">finestra al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c77c1-149">window at *rectangle*</span></span>        | <span data-ttu-id="c77c1-150">Modifica le dimensioni e la posizione della finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c77c1-150">Changes the size and location of the display window.</span></span> <span data-ttu-id="c77c1-151">Il rettangolo specificato è relativo alla finestra padre della finestra di visualizzazione (in genere il desktop) se il flag "stile figlio" è stato usato per il comando [Apri](open.md) .</span><span class="sxs-lookup"><span data-stu-id="c77c1-151">The specified rectangle is relative to the parent window of the display window (usually the desktop) if the "style child" flag has been used for the [open](open.md) command.</span></span> <span data-ttu-id="c77c1-152">Per modificare la posizione della finestra senza modificarne l'altezza o la larghezza, specificare zero per l'altezza e la larghezza.</span><span class="sxs-lookup"><span data-stu-id="c77c1-152">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span> |
| <span data-ttu-id="c77c1-153">client finestra</span><span class="sxs-lookup"><span data-stu-id="c77c1-153">window client</span></span>                | <span data-ttu-id="c77c1-154">Ripristina l'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="c77c1-154">Restores the client area of the window.</span></span>                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c77c1-155">client finestra al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="c77c1-155">window client at *rectangle*</span></span> | <span data-ttu-id="c77c1-156">Modifica le dimensioni e la posizione dell'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="c77c1-156">Changes the size and location of the client area of the window.</span></span> <span data-ttu-id="c77c1-157">Il rettangolo specificato è relativo alla finestra padre della finestra del client.</span><span class="sxs-lookup"><span data-stu-id="c77c1-157">The specified rectangle is relative to the parent window of the client window.</span></span> <span data-ttu-id="c77c1-158">Per modificare la posizione della finestra senza modificarne l'altezza o la larghezza, specificare zero per l'altezza e la larghezza.</span><span class="sxs-lookup"><span data-stu-id="c77c1-158">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span>                                                                                      |



 

<span data-ttu-id="c77c1-159">Quando un flag include un rettangolo, le coordinate del rettangolo sono relative all'origine della finestra o all'origine dell'immagine, a seconda delle esigenze, e sono specificate come **X1 Y1 2 x y2**.</span><span class="sxs-lookup"><span data-stu-id="c77c1-159">When a flag includes a rectangle, the rectangle coordinates are relative to the window origin or the image origin, as appropriate, and are specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="c77c1-160">Le coordinate **X1Y1** specificano l'angolo superiore sinistro e le coordinate **X2Y2** specificano la larghezza e l'altezza del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="c77c1-160">The coordinates **X1Y1** specify the upper left corner, and the coordinates **X2Y2** specify the width and height of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="c77c1-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c77c1-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c77c1-162">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="c77c1-162">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c77c1-163">Per i dispositivi digitali video è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="c77c1-163">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="c77c1-164">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c77c1-164">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c77c1-165">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c77c1-165">Return Value</span></span>

<span data-ttu-id="c77c1-166">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="c77c1-166">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c77c1-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="c77c1-167">Remarks</span></span>

<span data-ttu-id="c77c1-168">Il comando put definisce uno o più dei seguenti rettangoli quando si lavora con dispositivi con sovrimpressione video:</span><span class="sxs-lookup"><span data-stu-id="c77c1-168">The put command defines one or more of the following rectangles when working with video-overlay devices:</span></span>

-   <span data-ttu-id="c77c1-169">Il rettangolo video definisce l'area dell'immagine video in ingresso da acquisire.</span><span class="sxs-lookup"><span data-stu-id="c77c1-169">The video rectangle defines the region of the incoming video image to capture.</span></span>
-   <span data-ttu-id="c77c1-170">Il rettangolo del frame definisce l'area del buffer del frame che riceve l'immagine video in arrivo.</span><span class="sxs-lookup"><span data-stu-id="c77c1-170">The frame rectangle defines the region of the frame buffer that receives the incoming video image.</span></span>
-   <span data-ttu-id="c77c1-171">Il rettangolo di origine definisce quale area del buffer dei frame viene copiata nel rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c77c1-171">The source rectangle defines which region of the frame buffer is copied to the destination rectangle.</span></span>
-   <span data-ttu-id="c77c1-172">Il rettangolo di destinazione definisce l'area dell'area client della finestra di visualizzazione che riceve l'immagine del video.</span><span class="sxs-lookup"><span data-stu-id="c77c1-172">The destination rectangle defines the region of the display window client area that receives the video image.</span></span>

<span data-ttu-id="c77c1-173">Il rettangolo video è correlato al rettangolo frame nello stesso modo in cui il rettangolo di origine è correlato al rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c77c1-173">The video rectangle is related to the frame rectangle in the same way the source rectangle is related to the destination rectangle.</span></span> <span data-ttu-id="c77c1-174">L'estensione può verificarsi dal rettangolo video al rettangolo del frame e dal rettangolo di origine al rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c77c1-174">Stretching can occur from the video rectangle to the frame rectangle and from the source rectangle to the destination rectangle.</span></span> <span data-ttu-id="c77c1-175">Non tutti i dispositivi supportano l'estensione e l'allungamento deve essere abilitato (usando il comando [set](set.md) ).</span><span class="sxs-lookup"><span data-stu-id="c77c1-175">Not all devices support stretching, and stretching must be enabled (by using the [set](set.md) command).</span></span>

<span data-ttu-id="c77c1-176">Il comando che segue definisce tre aree per il video, il frame e l'origine.</span><span class="sxs-lookup"><span data-stu-id="c77c1-176">The following command defines three regions for the video, frame, and source.</span></span>

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

<span data-ttu-id="c77c1-177">Le aree in questo esempio sono definite come segue:</span><span class="sxs-lookup"><span data-stu-id="c77c1-177">The regions in this example are defined as follows:</span></span>

-   <span data-ttu-id="c77c1-178">Un'area 200 per 200 pixel dei dati video in arrivo, a partire da un'origine 120 pixel dall'angolo superiore sinistro, verrà acquisita nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="c77c1-178">A 200- by 200-pixel region of the incoming video data, starting at an origin 120 pixels from the upper left corner, will be captured to the frame buffer.</span></span>
-   <span data-ttu-id="c77c1-179">I dati video verranno posizionati in un'area 200 per 200 pixel nell'angolo superiore sinistro del buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="c77c1-179">The video data will be placed in a 200- by 200-pixel region at the upper left corner of the frame buffer.</span></span>
-   <span data-ttu-id="c77c1-180">I trasferimenti vengono effettuati dall'area 200-by 200-pixel nell'angolo superiore sinistro del buffer del frame alla finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c77c1-180">Transfers are made from the 200- by 200-pixel region at the upper left corner of the frame buffer to the destination window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c77c1-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c77c1-181">Requirements</span></span>



| <span data-ttu-id="c77c1-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="c77c1-182">Requirement</span></span> | <span data-ttu-id="c77c1-183">Valore</span><span class="sxs-lookup"><span data-stu-id="c77c1-183">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c77c1-184">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c77c1-184">Minimum supported client</span></span><br/> | <span data-ttu-id="c77c1-185">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c77c1-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c77c1-186">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c77c1-186">Minimum supported server</span></span><br/> | <span data-ttu-id="c77c1-187">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c77c1-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c77c1-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c77c1-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c77c1-189">MCI</span><span class="sxs-lookup"><span data-stu-id="c77c1-189">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c77c1-190">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="c77c1-190">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c77c1-191">open</span><span class="sxs-lookup"><span data-stu-id="c77c1-191">open</span></span>](open.md)
</dt> <dt>

[<span data-ttu-id="c77c1-192">set</span><span class="sxs-lookup"><span data-stu-id="c77c1-192">set</span></span>](set.md)
</dt> </dl>

 

