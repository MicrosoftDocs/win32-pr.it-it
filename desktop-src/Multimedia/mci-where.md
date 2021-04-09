---
title: Comando MCI_WHERE (mmsystem. h)
description: Il \_ comando MCI where ottiene il rettangolo di ridimensionamento per il dispositivo video.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- Comando MCI_WHERE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964278"
---
# <a name="mci_where-command"></a><span data-ttu-id="41918-104">\_Comando MCI where</span><span class="sxs-lookup"><span data-stu-id="41918-104">MCI\_WHERE command</span></span>

<span data-ttu-id="41918-105">Il \_ comando MCI where ottiene il rettangolo di ridimensionamento per il dispositivo video.</span><span class="sxs-lookup"><span data-stu-id="41918-105">The MCI\_WHERE command obtains the clipping rectangle for the video device.</span></span> <span data-ttu-id="41918-106">I dispositivi Digital-video e overlay video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="41918-106">Digital-video, and video-overlay devices recognize this command.</span></span> <span data-ttu-id="41918-107">I membri **superiore** e **sinistro** dell'oggetto [Rect](/previous-versions//ms536136(v=vs.85)) restituito contengono l'origine del rettangolo di ritaglio e i membri **destro** e **inferiore** contengono la larghezza e l'altezza del rettangolo di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="41918-107">The **top** and **left** members of the returned [RECT](/previous-versions//ms536136(v=vs.85)) contain the origin of the clipping rectangle, and the **right** and **bottom** members contain the width and height of the clipping rectangle.</span></span> <span data-ttu-id="41918-108">(Non si tratta dell'utilizzo standard dei membri **destro** e **inferiore** ).</span><span class="sxs-lookup"><span data-stu-id="41918-108">(This is not the standard use of the **right** and **bottom** members.)</span></span>

<span data-ttu-id="41918-109">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="41918-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
);
```



## <a name="parameters"></a><span data-ttu-id="41918-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="41918-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41918-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="41918-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="41918-112">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="41918-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="41918-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="41918-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="41918-114">\_Notifica MCI, \_ attesa MCI o, per i dispositivi video digitali, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="41918-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="41918-115">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="41918-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="41918-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span><span class="sxs-lookup"><span data-stu-id="41918-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span></span>
</dt> <dd>

<span data-ttu-id="41918-117">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="41918-117">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="41918-118">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41918-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41918-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41918-119">Return Value</span></span>

<span data-ttu-id="41918-120">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="41918-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="41918-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="41918-121">Remarks</span></span>

<span data-ttu-id="41918-122">Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="41918-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="41918-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>DGV MCI in \_ \_ cui \_ destinazione</span><span class="sxs-lookup"><span data-stu-id="41918-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI\_DGV\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="41918-124">Ottiene una descrizione dell'area rettangolare utilizzata per visualizzare video e immagini nell'area client della finestra corrente.</span><span class="sxs-lookup"><span data-stu-id="41918-124">Obtains a description of the rectangular region used to display video and images in the client area of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="41918-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>DGV MCI in \_ \_ cui \_ frame</span><span class="sxs-lookup"><span data-stu-id="41918-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI\_DGV\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="41918-126">Ottiene una descrizione dell'area rettangolare del buffer del frame in cui vengono ridimensionate le immagini del rettangolo video.</span><span class="sxs-lookup"><span data-stu-id="41918-126">Obtains a description of the rectangular region of the frame buffer into which images from the video rectangle are scaled.</span></span> <span data-ttu-id="41918-127">Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="41918-127">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="41918-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>DGV MCI in \_ \_ cui \_ Max</span><span class="sxs-lookup"><span data-stu-id="41918-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI\_DGV\_WHERE\_MAX</span></span>
</dt> <dd>

<span data-ttu-id="41918-129">Se usato con MCI \_ DGV \_ dove \_ Destination o \_ MCI DGV \_ dove \_ source, il rettangolo restituito indica la larghezza e l'altezza massime dell'area specificata.</span><span class="sxs-lookup"><span data-stu-id="41918-129">When used with MCI\_DGV\_WHERE\_DESTINATION or MCI\_DGV\_WHERE\_SOURCE, the rectangle returned indicates the maximum width and height of the specified region.</span></span> <span data-ttu-id="41918-130">Se usato con la \_ \_ finestra DGV \_ di MCI, il rettangolo restituito indica le dimensioni dell'intero schermo.</span><span class="sxs-lookup"><span data-stu-id="41918-130">When used with MCI\_DGV\_WHERE\_WINDOW, the rectangle returned indicates the size of the entire display.</span></span>

</dd> <dt>

<span data-ttu-id="41918-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ DGV \_ Where \_ source</span><span class="sxs-lookup"><span data-stu-id="41918-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI\_DGV\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="41918-132">Ottiene una descrizione dell'area rettangolare (ritagliata dal buffer del frame) allungata per adattarsi al rettangolo di destinazione sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="41918-132">Obtains a description of the rectangular region (cropped from the frame buffer) that is stretched to fit the destination rectangle on the display.</span></span>

</dd> <dt>

<span data-ttu-id="41918-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>DGV MCI in \_ \_ cui \_ video</span><span class="sxs-lookup"><span data-stu-id="41918-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI\_DGV\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="41918-134">Ottiene una descrizione dell'area rettangolare ritagliata dall'origine della presentazione per riempire il rettangolo del frame nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="41918-134">Obtains a description of the rectangular region cropped from the presentation source to fill the frame rectangle in the frame buffer.</span></span> <span data-ttu-id="41918-135">Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="41918-135">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="41918-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>DGV MCI in \_ \_ cui \_ finestra</span><span class="sxs-lookup"><span data-stu-id="41918-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI\_DGV\_WHERE\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="41918-137">Ottiene una descrizione della cornice della finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="41918-137">Obtains a description of the display-window frame.</span></span>

</dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="41918-138">Per i dispositivi digitali video, il parametro *lpQuery* punta a un **DGV MCI in cui è presente la struttura \_ \_ \_ parametri** .</span><span class="sxs-lookup"><span data-stu-id="41918-138">For digital-video devices, the *lpQuery* parameter points to an **MCI\_DGV\_WHERE\_PARMS** structure.</span></span> <span data-ttu-id="41918-139">**DGV MCI in cui la struttura \_ \_ \_ parametri** è identica alla [**struttura \_ DGV \_ Rect \_ parametri di MCI**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="41918-139">The **MCI\_DGV\_WHERE\_PARMS** structure is identical to the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="41918-140">Con il tipo di dispositivo **overlay** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="41918-140">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="41918-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>OVLY MCI in \_ \_ cui \_ destinazione</span><span class="sxs-lookup"><span data-stu-id="41918-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI\_OVLY\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="41918-142">Ottiene il rettangolo di visualizzazione della destinazione.</span><span class="sxs-lookup"><span data-stu-id="41918-142">Obtains the destination display rectangle.</span></span> <span data-ttu-id="41918-143">Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="41918-143">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="41918-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>OVLY MCI in \_ \_ cui \_ frame</span><span class="sxs-lookup"><span data-stu-id="41918-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI\_OVLY\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="41918-145">Ottiene il rettangolo del frame di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="41918-145">Obtains the overlay frame rectangle.</span></span> <span data-ttu-id="41918-146">Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="41918-146">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="41918-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ OVLY \_ Where \_ source</span><span class="sxs-lookup"><span data-stu-id="41918-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI\_OVLY\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="41918-148">Ottiene il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="41918-148">Obtains the source rectangle.</span></span> <span data-ttu-id="41918-149">Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="41918-149">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="41918-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>OVLY MCI in \_ \_ cui \_ video</span><span class="sxs-lookup"><span data-stu-id="41918-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI\_OVLY\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="41918-151">Ottiene il rettangolo del video.</span><span class="sxs-lookup"><span data-stu-id="41918-151">Obtains the video rectangle.</span></span> <span data-ttu-id="41918-152">Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="41918-152">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> </dl>

<span data-ttu-id="41918-153">Per i dispositivi con sovrimpressione video, il parametro *lpQuery* punta a una struttura [**\_ OVLY \_ Rect \_ parametri di MCI**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="41918-153">For video-overlay devices, the *lpQuery* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="41918-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41918-154">Requirements</span></span>



| <span data-ttu-id="41918-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="41918-155">Requirement</span></span> | <span data-ttu-id="41918-156">Valore</span><span class="sxs-lookup"><span data-stu-id="41918-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41918-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41918-157">Minimum supported client</span></span><br/> | <span data-ttu-id="41918-158">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41918-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="41918-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41918-159">Minimum supported server</span></span><br/> | <span data-ttu-id="41918-160">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41918-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="41918-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41918-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="41918-162"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41918-162"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41918-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41918-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41918-164">MCI</span><span class="sxs-lookup"><span data-stu-id="41918-164">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="41918-165">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="41918-165">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

