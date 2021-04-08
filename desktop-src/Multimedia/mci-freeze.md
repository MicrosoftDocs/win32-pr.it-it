---
title: Comando MCI_FREEZE (mmsystem. h)
description: Il \_ comando di blocco MCI blocca il movimento sullo schermo. I dispositivi Digital-video, video-overlay e VCR riconoscono questo comando.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- Comando MCI_FREEZE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048058"
---
# <a name="mci_freeze-command"></a><span data-ttu-id="a9d3a-105">\_Comando blocca MCI</span><span class="sxs-lookup"><span data-stu-id="a9d3a-105">MCI\_FREEZE command</span></span>

<span data-ttu-id="a9d3a-106">Il \_ comando di blocco MCI blocca il movimento sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-106">The MCI\_FREEZE command freezes motion on the display.</span></span> <span data-ttu-id="a9d3a-107">I dispositivi Digital-video, video-overlay e VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="a9d3a-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
);
```



## <a name="parameters"></a><span data-ttu-id="a9d3a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9d3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d3a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a9d3a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a9d3a-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a9d3a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a9d3a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a9d3a-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a9d3a-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="a9d3a-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a9d3a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9d3a-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span><span class="sxs-lookup"><span data-stu-id="a9d3a-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span></span>
</dt> <dd>

<span data-ttu-id="a9d3a-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a9d3a-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="a9d3a-117">I dispositivi con parametri aggiuntivi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-117">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9d3a-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9d3a-118">Return Value</span></span>

<span data-ttu-id="a9d3a-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9d3a-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9d3a-120">Remarks</span></span>

<span data-ttu-id="a9d3a-121">I flag aggiuntivi seguenti vengono usati dal tipo di dispositivo **digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="a9d3a-121">The following additional flags are used by the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a9d3a-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>\_blocco DGV \_ MCI \_ in</span><span class="sxs-lookup"><span data-stu-id="a9d3a-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI\_DGV\_FREEZE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="a9d3a-123">Il membro **RC** della struttura identificato da *lpFreeze* contiene un rettangolo valido.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-123">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="a9d3a-124">Il rettangolo specifica un'area all'interno del buffer del frame che avrà il bit della maschera di blocco per ogni pixel attivato.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-124">The rectangle specifies a region within the frame buffer that will have the lock mask bit for each pixel turned on.</span></span> <span data-ttu-id="a9d3a-125">I pixel specificati non verranno aggiornati finché il bit della maschera di blocco non viene disattivato.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-125">The specified pixels will not be updated until their lock mask bit is turned off.</span></span> <span data-ttu-id="a9d3a-126">Se questo flag non è specificato, il rettangolo viene impostato sull'intero buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-126">If this flag is not specified, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="a9d3a-127">Questo flag è supportato solo se il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) restituisce **true** per il \_ flag MCI DGV \_ GETDEVCAPS \_ can \_ Lock.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-127">This flag is supported only if the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command returns **TRUE** for the MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK flag.</span></span>

</dd> <dt>

<span data-ttu-id="a9d3a-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>\_blocco DGV \_ MCI \_ esterno</span><span class="sxs-lookup"><span data-stu-id="a9d3a-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI\_DGV\_FREEZE\_OUTSIDE</span></span>
</dt> <dd>

<span data-ttu-id="a9d3a-129">L'area al di fuori dell'area specificata per il \_ flag di blocco DGV del MCI \_ \_ è bloccata.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-129">The area outside the region specified for the MCI\_DGV\_FREEZE\_AT flag is frozen.</span></span>

</dd> </dl>

<span data-ttu-id="a9d3a-130">Per i dispositivi digitali video, il parametro *lpFreeze* punta a una [**struttura \_ DGV \_ Freeze \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="a9d3a-130">For digital-video devices, the *lpFreeze* parameter points to an [**MCI\_DGV\_FREEZE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="a9d3a-131">I flag aggiuntivi seguenti vengono usati dal tipo di dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="a9d3a-131">The following additional flags are used by the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a9d3a-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>\_ \_ campo blocco videoregistratore \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a9d3a-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>MCI\_VCR\_FREEZE\_FIELD</span></span>
</dt> <dd>

<span data-ttu-id="a9d3a-133">Blocca solo un membro del frame corrente.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-133">Freeze only one member of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="a9d3a-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>\_frame di \_ blocco \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="a9d3a-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>MCI\_VCR\_FREEZE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="a9d3a-135">Blocca entrambi i campi del frame corrente.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-135">Freeze both fields of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="a9d3a-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>\_ \_ input blocco VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a9d3a-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>MCI\_VCR\_FREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="a9d3a-137">Blocca il frame corrente sullo schermo (usato per la registrazione).</span><span class="sxs-lookup"><span data-stu-id="a9d3a-137">Freeze the current frame on the screen (used for recording).</span></span>

</dd> <dt>

<span data-ttu-id="a9d3a-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>\_ \_ output blocco VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a9d3a-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>MCI\_VCR\_FREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="a9d3a-139">Blocca il frame corrente dal VCR (usato con l'acquisizione dei frame).</span><span class="sxs-lookup"><span data-stu-id="a9d3a-139">Freeze the current frame from the VCR (used with frame capture).</span></span>

</dd> </dl>

<span data-ttu-id="a9d3a-140">Per i dispositivi VCR, il parametro *lpFreeze* punta a una struttura [**\_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a9d3a-140">For VCR devices, the *lpFreeze* parameter points to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

<span data-ttu-id="a9d3a-141">Il flag aggiuntivo seguente viene usato dal tipo di dispositivo **overlay** :</span><span class="sxs-lookup"><span data-stu-id="a9d3a-141">The following additional flag is used by the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a9d3a-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>OVLY di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="a9d3a-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="a9d3a-143">Il membro **RC** della struttura identificato da *lpFreeze* contiene un rettangolo valido.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-143">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="a9d3a-144">Se questo flag non è specificato, il driver di dispositivo blocca l'intero frame.</span><span class="sxs-lookup"><span data-stu-id="a9d3a-144">If this flag is not specified, the device driver will freeze the entire frame.</span></span>

</dd> </dl>

<span data-ttu-id="a9d3a-145">Per i dispositivi con sovrimpressione video, il parametro *lpFreeze* punta a una struttura [**\_ OVLY \_ Rect \_ parametri di MCI**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a9d3a-145">For video-overlay devices, the *lpFreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d3a-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9d3a-146">Requirements</span></span>



| <span data-ttu-id="a9d3a-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9d3a-147">Requirement</span></span> | <span data-ttu-id="a9d3a-148">Valore</span><span class="sxs-lookup"><span data-stu-id="a9d3a-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d3a-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9d3a-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d3a-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9d3a-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a9d3a-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9d3a-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d3a-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9d3a-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a9d3a-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9d3a-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9d3a-154"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9d3a-154"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d3a-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9d3a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d3a-156">MCI</span><span class="sxs-lookup"><span data-stu-id="a9d3a-156">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a9d3a-157">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="a9d3a-157">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

