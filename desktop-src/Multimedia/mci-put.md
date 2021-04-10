---
title: Comando MCI_PUT (mmsystem. h)
description: Il \_ comando MCI put imposta i rettangoli di origine, di destinazione e di frame. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- Comando MCI_PUT Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121675"
---
# <a name="mci_put-command"></a><span data-ttu-id="44ef1-105">\_Comando MCI put</span><span class="sxs-lookup"><span data-stu-id="44ef1-105">MCI\_PUT command</span></span>

<span data-ttu-id="44ef1-106">Il \_ comando MCI put imposta i rettangoli di origine, di destinazione e di frame.</span><span class="sxs-lookup"><span data-stu-id="44ef1-106">The MCI\_PUT command sets the source, destination, and frame rectangles.</span></span> <span data-ttu-id="44ef1-107">I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="44ef1-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="44ef1-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="44ef1-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="44ef1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="44ef1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44ef1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="44ef1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="44ef1-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="44ef1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi video digitali, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="44ef1-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="44ef1-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="44ef1-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span><span class="sxs-lookup"><span data-stu-id="44ef1-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="44ef1-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="44ef1-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44ef1-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44ef1-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44ef1-118">Return Value</span></span>

<span data-ttu-id="44ef1-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="44ef1-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="44ef1-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="44ef1-120">Remarks</span></span>

<span data-ttu-id="44ef1-121">Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="44ef1-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="44ef1-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>\_client DGV \_ put \_ MCI</span><span class="sxs-lookup"><span data-stu-id="44ef1-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI\_DGV\_PUT\_CLIENT</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-123">Il rettangolo definito per MCI \_ DGV \_ Rect si applica alla posizione della finestra client.</span><span class="sxs-lookup"><span data-stu-id="44ef1-123">The rectangle defined for MCI\_DGV\_RECT applies to the position of the client window.</span></span> <span data-ttu-id="44ef1-124">Il rettangolo specificato è relativo alla finestra padre della finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="44ef1-124">The rectangle specified is relative to the parent window of the display window.</span></span> <span data-ttu-id="44ef1-125">\_ \_ \_ La finestra put DGV di MCI deve essere impostata simultaneamente con questo flag.</span><span class="sxs-lookup"><span data-stu-id="44ef1-125">MCI\_DGV\_PUT\_WINDOW must be set concurrently with this flag.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>\_destinazione DGV MCI \_ put \_</span><span class="sxs-lookup"><span data-stu-id="44ef1-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI\_DGV\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-127">Il rettangolo definito per MCI \_ DGV \_ Rect specifica un rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="44ef1-127">The rectangle defined for MCI\_DGV\_RECT specifies a destination rectangle.</span></span> <span data-ttu-id="44ef1-128">Il rettangolo di destinazione specifica la parte della finestra client associata a questa istanza del driver di dispositivo che Visualizza l'immagine o il video.</span><span class="sxs-lookup"><span data-stu-id="44ef1-128">The destination rectangle specifies the portion of the client window associated with this device driver instance that shows the image or video.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>\_ \_ frame put DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="44ef1-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI\_DGV\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-130">Il rettangolo definito per MCI \_ DGV \_ Rect viene applicato al rettangolo del frame.</span><span class="sxs-lookup"><span data-stu-id="44ef1-130">The rectangle defined for MCI\_DGV\_RECT applies to the frame rectangle.</span></span> <span data-ttu-id="44ef1-131">Il rettangolo del frame specifica la parte del buffer del frame utilizzata come destinazione delle immagini video ottenute dal rettangolo video.</span><span class="sxs-lookup"><span data-stu-id="44ef1-131">The frame rectangle specifies the portion of the frame buffer used as the destination of the video images obtained from the video rectangle.</span></span> <span data-ttu-id="44ef1-132">Il video deve essere ridimensionato in base al rettangolo del buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="44ef1-132">The video should be scaled to fit within the frame buffer rectangle.</span></span>

<span data-ttu-id="44ef1-133">Il rettangolo viene specificato nelle coordinate del buffer dei frame.</span><span class="sxs-lookup"><span data-stu-id="44ef1-133">The rectangle is specified in frame buffer coordinates.</span></span> <span data-ttu-id="44ef1-134">Il rettangolo predefinito è il buffer di frame completo.</span><span class="sxs-lookup"><span data-stu-id="44ef1-134">The default rectangle is the full frame buffer.</span></span> <span data-ttu-id="44ef1-135">La specifica di questo rettangolo consente al dispositivo di ridimensionare l'immagine mentre digitalizza i dati.</span><span class="sxs-lookup"><span data-stu-id="44ef1-135">Specifying this rectangle lets the device scale the image as it digitizes the data.</span></span> <span data-ttu-id="44ef1-136">I dispositivi che non possono ridimensionare l'immagine rifiutano questo comando con MCIERR \_ funzione non supportata \_ .</span><span class="sxs-lookup"><span data-stu-id="44ef1-136">Devices that cannot scale the image reject this command with MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="44ef1-137">È possibile usare il \_ flag MCI GETDEVCAPS \_ can \_ stretch con il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) per determinare se un dispositivo ridimensiona l'immagine.</span><span class="sxs-lookup"><span data-stu-id="44ef1-137">You can use the MCI\_GETDEVCAPS\_CAN\_STRETCH flag with the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command to determine if a device scales the image.</span></span> <span data-ttu-id="44ef1-138">Un dispositivo restituisce **false** se non è possibile ridimensionare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="44ef1-138">A device returns **FALSE** if it cannot scale the image.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>\_origine DGV MCI \_ put \_</span><span class="sxs-lookup"><span data-stu-id="44ef1-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI\_DGV\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-140">Il rettangolo definito per MCI \_ DGV \_ Rect specifica un rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="44ef1-140">The rectangle defined for MCI\_DGV\_RECT specifies a source rectangle.</span></span> <span data-ttu-id="44ef1-141">Il rettangolo di origine specifica quale parte del buffer del frame deve essere ridimensionata per adattarsi al rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="44ef1-141">The source rectangle specifies which portion of the frame buffer is to be scaled to fit into the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>\_video di DGV MCI \_ put \_</span><span class="sxs-lookup"><span data-stu-id="44ef1-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>MCI\_DGV\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-143">Il rettangolo definito per MCI \_ DGV \_ Rect viene applicato al rettangolo del video.</span><span class="sxs-lookup"><span data-stu-id="44ef1-143">The rectangle defined for MCI\_DGV\_RECT applies to the video rectangle.</span></span> <span data-ttu-id="44ef1-144">Il rettangolo video specifica quale parte dell'origine della presentazione corrente è archiviata nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="44ef1-144">The video rectangle specifies which portion of the current presentation source is stored in the frame buffer.</span></span> <span data-ttu-id="44ef1-145">Il rettangolo viene specificato utilizzando le coordinate naturali dell'origine della presentazione.</span><span class="sxs-lookup"><span data-stu-id="44ef1-145">The rectangle is specified using the natural coordinates of the presentation source.</span></span> <span data-ttu-id="44ef1-146">Consente di specificare il ritaglio che si verifica prima di archiviare immagini e video nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="44ef1-146">It allows the specification of cropping that occurs prior to storing images and video in the frame buffer.</span></span> <span data-ttu-id="44ef1-147">Il rettangolo predefinito è l'area di analisi attiva completa oppure le immagini e il video decompressi completi.</span><span class="sxs-lookup"><span data-stu-id="44ef1-147">The default rectangle is the full active scan area or the full decompressed images and video.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>\_ \_ finestra put DGV di MCI \_</span><span class="sxs-lookup"><span data-stu-id="44ef1-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>MCI\_DGV\_PUT\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-149">Il rettangolo definito per MCI \_ DGV \_ Rect viene applicato alla finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="44ef1-149">The rectangle defined for MCI\_DGV\_RECT applies to the display window.</span></span> <span data-ttu-id="44ef1-150">Questo rettangolo è relativo alla finestra padre della finestra di visualizzazione, in genere il desktop.</span><span class="sxs-lookup"><span data-stu-id="44ef1-150">This rectangle is relative to the parent window of the display window (usually the desktop).</span></span> <span data-ttu-id="44ef1-151">Se la finestra non è specificata, il valore predefinito è la dimensione e la posizione iniziali della finestra.</span><span class="sxs-lookup"><span data-stu-id="44ef1-151">If the window is not specified, it defaults to the initial window size and position.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>DGV di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="44ef1-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-153">Il membro **RC** della struttura identificato da *lpDest* contiene un rettangolo valido.</span><span class="sxs-lookup"><span data-stu-id="44ef1-153">The **rc** member of the structure identified by *lpDest* contains a valid rectangle.</span></span>

</dd> </dl>

<span data-ttu-id="44ef1-154">Per i dispositivi digitali video, *lpDest* punta a una [**struttura \_ DGV \_ put \_ parametri di MCI**](/previous-versions//dd743397(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="44ef1-154">For digital-video devices, *lpDest* points to an [**MCI\_DGV\_PUT\_PARMS**](/previous-versions//dd743397(v=vs.85)) structure.</span></span>

<span data-ttu-id="44ef1-155">Con il tipo di dispositivo **overlay** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="44ef1-155">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="44ef1-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>\_destinazione OVLY MCI \_ put \_</span><span class="sxs-lookup"><span data-stu-id="44ef1-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI\_OVLY\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-157">Il rettangolo definito per MCI \_ OVLY \_ Rect specifica l'area della finestra client utilizzata per visualizzare un'immagine.</span><span class="sxs-lookup"><span data-stu-id="44ef1-157">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the client window used to display an image.</span></span> <span data-ttu-id="44ef1-158">Il rettangolo contiene l'offset e l'extent visibile dell'immagine rispetto all'origine della finestra.</span><span class="sxs-lookup"><span data-stu-id="44ef1-158">The rectangle contains the offset and visible extent of the image relative to the window origin.</span></span> <span data-ttu-id="44ef1-159">Se il frame viene allungato, l'origine viene allungata al rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="44ef1-159">If the frame is being stretched, the source is stretched to the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>\_ \_ frame put OVLY \_ MCI</span><span class="sxs-lookup"><span data-stu-id="44ef1-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI\_OVLY\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-161">Il rettangolo definito per MCI \_ OVLY \_ Rect specifica l'area del buffer video usato per ricevere l'immagine del video.</span><span class="sxs-lookup"><span data-stu-id="44ef1-161">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used to receive the video image.</span></span> <span data-ttu-id="44ef1-162">Il rettangolo contiene l'offset e l'extent dell'area del buffer rispetto all'origine del buffer del video.</span><span class="sxs-lookup"><span data-stu-id="44ef1-162">The rectangle contains the offset and extent of the buffer area relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>\_origine OVLY MCI \_ put \_</span><span class="sxs-lookup"><span data-stu-id="44ef1-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI\_OVLY\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-164">Il rettangolo definito per MCI \_ OVLY \_ Rect specifica l'area del buffer video utilizzato come origine dell'immagine digitale.</span><span class="sxs-lookup"><span data-stu-id="44ef1-164">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used as the source of the digital image.</span></span> <span data-ttu-id="44ef1-165">Il rettangolo contiene l'offset e l'extent del rettangolo di ridimensionamento per il buffer video relativo all'origine.</span><span class="sxs-lookup"><span data-stu-id="44ef1-165">The rectangle contains the offset and extent of the clipping rectangle for the video buffer relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>\_video di OVLY MCI \_ put \_</span><span class="sxs-lookup"><span data-stu-id="44ef1-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>MCI\_OVLY\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-167">Il rettangolo definito per MCI \_ OVLY \_ Rect specifica l'area di acquisizione video dell'origine dal buffer video.</span><span class="sxs-lookup"><span data-stu-id="44ef1-167">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video source capture by the video buffer.</span></span> <span data-ttu-id="44ef1-168">Il rettangolo contiene l'offset e l'extent del rettangolo di ridimensionamento per l'origine video rispetto all'origine.</span><span class="sxs-lookup"><span data-stu-id="44ef1-168">The rectangle contains the offset and extent of the clipping rectangle for the video source relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>OVLY di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="44ef1-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-170">Il membro **RC** della struttura identificato da *lpDest* contiene un rettangolo di visualizzazione valido.</span><span class="sxs-lookup"><span data-stu-id="44ef1-170">The **rc** member of the structure identified by *lpDest* contains a valid display rectangle.</span></span> <span data-ttu-id="44ef1-171">Se questo flag non è specificato, il rettangolo predefinito corrisponde alle coordinate del buffer video o della finestra da ritagliare.</span><span class="sxs-lookup"><span data-stu-id="44ef1-171">If this flag is not specified, the default rectangle matches the coordinates of the video buffer or window being clipped.</span></span>

</dd> </dl>

<span data-ttu-id="44ef1-172">Per i dispositivi con sovrimpressione video, *lpDest* punta a una struttura [**\_ OVLY \_ Rect \_ parametri di MCI**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="44ef1-172">For video-overlay devices, *lpDest* points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="44ef1-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44ef1-173">Requirements</span></span>



| <span data-ttu-id="44ef1-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="44ef1-174">Requirement</span></span> | <span data-ttu-id="44ef1-175">Valore</span><span class="sxs-lookup"><span data-stu-id="44ef1-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44ef1-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44ef1-176">Minimum supported client</span></span><br/> | <span data-ttu-id="44ef1-177">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="44ef1-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="44ef1-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44ef1-178">Minimum supported server</span></span><br/> | <span data-ttu-id="44ef1-179">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="44ef1-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="44ef1-180">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44ef1-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="44ef1-181"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44ef1-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44ef1-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44ef1-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ef1-183">MCI</span><span class="sxs-lookup"><span data-stu-id="44ef1-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="44ef1-184">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="44ef1-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

