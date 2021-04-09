---
title: Comando MCI_UNFREEZE (mmsystem. h)
description: Il \_ comando MCI Unfreeze ripristina il movimento in un'area del buffer video bloccata con il \_ comando di blocco MCI. I dispositivi Digital-video, VCR e overlay video riconoscono questo comando.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- Comando MCI_UNFREEZE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121259"
---
# <a name="mci_unfreeze-command"></a><span data-ttu-id="a66c2-105">\_Comando di UNFREEZE MCI</span><span class="sxs-lookup"><span data-stu-id="a66c2-105">MCI\_UNFREEZE command</span></span>

<span data-ttu-id="a66c2-106">Il \_ comando MCI Unfreeze ripristina il movimento in un'area del buffer video bloccata con il comando di [ \_ blocco MCI](mci-freeze.md) .</span><span class="sxs-lookup"><span data-stu-id="a66c2-106">The MCI\_UNFREEZE command restores motion to an area of the video buffer frozen with the [MCI\_FREEZE](mci-freeze.md) command.</span></span> <span data-ttu-id="a66c2-107">I dispositivi Digital-video, VCR e overlay video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="a66c2-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="a66c2-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a66c2-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
);
```



## <a name="parameters"></a><span data-ttu-id="a66c2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a66c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a66c2-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a66c2-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a66c2-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="a66c2-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a66c2-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a66c2-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a66c2-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a66c2-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="a66c2-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a66c2-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a66c2-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span><span class="sxs-lookup"><span data-stu-id="a66c2-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="a66c2-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a66c2-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="a66c2-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a66c2-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a66c2-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a66c2-118">Return Value</span></span>

<span data-ttu-id="a66c2-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="a66c2-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a66c2-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="a66c2-120">Remarks</span></span>

<span data-ttu-id="a66c2-121">Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="a66c2-121">The following additional flag is used with the **digitalvideo** device type:</span></span>

<span data-ttu-id="a66c2-122">DGV di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="a66c2-122">MCI\_DGV\_RECT</span></span>

<span data-ttu-id="a66c2-123">Il membro **RC** della struttura identificato da *lpUnfreeze* contiene un rettangolo di visualizzazione valido.</span><span class="sxs-lookup"><span data-stu-id="a66c2-123">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="a66c2-124">Il rettangolo specifica un'area all'interno del buffer dei frame i cui pixel dovrebbero avere il bit di maschera di blocco disattivato.</span><span class="sxs-lookup"><span data-stu-id="a66c2-124">The rectangle specifies a region within the frame buffer whose pixels should have their lock mask bit turned off.</span></span> <span data-ttu-id="a66c2-125">Le aree rettangolari vengono specificate come descritto per il comando [MCI \_ put](mci-put.md) .</span><span class="sxs-lookup"><span data-stu-id="a66c2-125">Rectangular regions are specified as described for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="a66c2-126">Se omesso, il rettangolo viene impostato sull'intero buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="a66c2-126">If omitted, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="a66c2-127">Utilizzando una sequenza di comandi Freeze e Unfreeze con rettangoli diversi, è possibile descrivere modelli arbitrari di bit della maschera di blocco.</span><span class="sxs-lookup"><span data-stu-id="a66c2-127">By using a sequence of freeze and unfreeze commands with different rectangles, arbitrary patterns of lock mask bits can be described.</span></span>

<span data-ttu-id="a66c2-128">Per i dispositivi digitali video, il parametro *lpUnfreeze* punta a una **struttura \_ DGV \_ decongelata MCI \_ parametri** .</span><span class="sxs-lookup"><span data-stu-id="a66c2-128">For digital-video devices, the *lpUnfreeze* parameter points to an **MCI\_DGV\_UNFREEZE\_PARMS** structure.</span></span> <span data-ttu-id="a66c2-129">Per ulteriori informazioni, vedere i commenti per la [**struttura \_ DGV \_ Rect \_ parametri di MCI**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="a66c2-129">For more information, see the comments for the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="a66c2-130">Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a66c2-130">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a66c2-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>\_ \_ input sbloccare VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a66c2-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI\_VCR\_UNFREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="a66c2-132">Sbloccare l'input.</span><span class="sxs-lookup"><span data-stu-id="a66c2-132">Unfreeze the input.</span></span>

</dd> <dt>

<span data-ttu-id="a66c2-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>\_output di \_ sbloccaggio \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="a66c2-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI\_VCR\_UNFREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="a66c2-134">Sbloccare l'output.</span><span class="sxs-lookup"><span data-stu-id="a66c2-134">Unfreeze the output.</span></span>

</dd> </dl>

<span data-ttu-id="a66c2-135">Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **overlay** :</span><span class="sxs-lookup"><span data-stu-id="a66c2-135">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a66c2-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>OVLY di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="a66c2-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="a66c2-137">Il membro **RC** della struttura identificato da *lpUnfreeze* contiene un rettangolo di visualizzazione valido.</span><span class="sxs-lookup"><span data-stu-id="a66c2-137">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="a66c2-138">Parametro obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a66c2-138">This is a required parameter.</span></span>

</dd> </dl>

<span data-ttu-id="a66c2-139">Per i dispositivi con sovrimpressione video, il parametro *lpUnfreeze* punta a una struttura [**\_ OVLY \_ Rect \_ parametri di MCI**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a66c2-139">For video-overlay devices, the *lpUnfreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a66c2-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a66c2-140">Requirements</span></span>



| <span data-ttu-id="a66c2-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a66c2-141">Requirement</span></span> | <span data-ttu-id="a66c2-142">Valore</span><span class="sxs-lookup"><span data-stu-id="a66c2-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a66c2-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a66c2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a66c2-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a66c2-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a66c2-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a66c2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a66c2-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a66c2-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a66c2-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a66c2-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a66c2-148"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a66c2-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a66c2-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a66c2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a66c2-150">MCI</span><span class="sxs-lookup"><span data-stu-id="a66c2-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a66c2-151">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="a66c2-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

