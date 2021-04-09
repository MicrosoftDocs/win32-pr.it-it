---
title: Comando MCI_CAPTURE (mmsystem. h)
description: Il \_ comando di acquisizione di MCI acquisisce il contenuto del buffer del frame e lo archivia in un file specificato. I dispositivi digitali video riconoscono questo comando.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- Comando MCI_CAPTURE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964531"
---
# <a name="mci_capture-command"></a><span data-ttu-id="ddd5d-105">\_Comando di acquisizione MCI</span><span class="sxs-lookup"><span data-stu-id="ddd5d-105">MCI\_CAPTURE command</span></span>

<span data-ttu-id="ddd5d-106">Il \_ comando di acquisizione di MCI acquisisce il contenuto del buffer del frame e lo archivia in un file specificato.</span><span class="sxs-lookup"><span data-stu-id="ddd5d-106">The MCI\_CAPTURE command captures the contents of the frame buffer and stores it in a specified file.</span></span> <span data-ttu-id="ddd5d-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="ddd5d-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="ddd5d-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="ddd5d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
);
```



## <a name="parameters"></a><span data-ttu-id="ddd5d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ddd5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddd5d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ddd5d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ddd5d-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="ddd5d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ddd5d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ddd5d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ddd5d-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="ddd5d-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="ddd5d-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ddd5d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddd5d-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span><span class="sxs-lookup"><span data-stu-id="ddd5d-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span></span>
</dt> <dd>

<span data-ttu-id="ddd5d-116">Puntatore a una [**struttura \_ DGV \_ Capture \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="ddd5d-116">Pointer to an [**MCI\_DGV\_CAPTURE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddd5d-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ddd5d-117">Return Value</span></span>

<span data-ttu-id="ddd5d-118">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="ddd5d-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddd5d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ddd5d-119">Remarks</span></span>

<span data-ttu-id="ddd5d-120">I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:</span><span class="sxs-lookup"><span data-stu-id="ddd5d-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="ddd5d-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>\_DGV \_ di acquisizione \_ MCI</span><span class="sxs-lookup"><span data-stu-id="ddd5d-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI\_DGV\_CAPTURE\_AS</span></span>
</dt> <dd>

<span data-ttu-id="ddd5d-122">Il membro **lpstrFileName** della struttura identificata da *lpCapture* contiene un indirizzo di un buffer che specifica il percorso e il nome del file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ddd5d-122">The **lpstrFileName** member of the structure identified by *lpCapture* contains an address of a buffer specifying the destination path and filename.</span></span> <span data-ttu-id="ddd5d-123">(Questo flag è obbligatorio).</span><span class="sxs-lookup"><span data-stu-id="ddd5d-123">(This flag is required.)</span></span>

</dd> <dt>

<span data-ttu-id="ddd5d-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>\_acquisizione DGV \_ MCI \_ in</span><span class="sxs-lookup"><span data-stu-id="ddd5d-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI\_DGV\_CAPTURE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="ddd5d-125">Il membro **RC** della struttura identificato da *lpCapture* contiene un rettangolo valido.</span><span class="sxs-lookup"><span data-stu-id="ddd5d-125">The **rc** member of the structure identified by *lpCapture* contains a valid rectangle.</span></span> <span data-ttu-id="ddd5d-126">Il rettangolo specifica l'area rettangolare all'interno del buffer del frame che viene ritagliata e salvata su disco.</span><span class="sxs-lookup"><span data-stu-id="ddd5d-126">The rectangle specifies the rectangular region within the frame buffer that is cropped and saved to disk.</span></span> <span data-ttu-id="ddd5d-127">Se omesso, per impostazione predefinita l'area ritagliata viene impostata sul rettangolo specificato o impostato come predefinito in un comando [MCI \_ put](mci-put.md) precedente che specifica l'area di origine per questa istanza del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddd5d-127">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [MCI\_PUT](mci-put.md) command that specifies the source area for this instance of the device driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddd5d-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddd5d-128">Requirements</span></span>



| <span data-ttu-id="ddd5d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddd5d-129">Requirement</span></span> | <span data-ttu-id="ddd5d-130">Valore</span><span class="sxs-lookup"><span data-stu-id="ddd5d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd5d-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddd5d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd5d-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ddd5d-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ddd5d-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddd5d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd5d-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ddd5d-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ddd5d-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ddd5d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddd5d-136"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ddd5d-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddd5d-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddd5d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddd5d-138">MCI</span><span class="sxs-lookup"><span data-stu-id="ddd5d-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ddd5d-139">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="ddd5d-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

