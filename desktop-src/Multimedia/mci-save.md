---
title: Comando MCI_SAVE (mmsystem. h)
description: Il \_ comando MCI Save Salva il file corrente.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- Comando MCI_SAVE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475694"
---
# <a name="mci_save-command"></a><span data-ttu-id="ba4ad-104">\_Comando di salvataggio MCI</span><span class="sxs-lookup"><span data-stu-id="ba4ad-104">MCI\_SAVE command</span></span>

<span data-ttu-id="ba4ad-105">Il \_ comando MCI Save Salva il file corrente.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-105">The MCI\_SAVE command saves the current file.</span></span> <span data-ttu-id="ba4ad-106">I dispositivi che modificano i file non devono eliminare definitivamente la copia originale fino a quando non ricevono il messaggio di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-106">Devices that modify files should not destroy the original copy until they receive the save message.</span></span> <span data-ttu-id="ba4ad-107">Video-overlay e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-107">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="ba4ad-108">Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo implementano.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-108">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="ba4ad-109">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
);
```



## <a name="parameters"></a><span data-ttu-id="ba4ad-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba4ad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba4ad-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ba4ad-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ba4ad-112">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ba4ad-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ba4ad-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ba4ad-114">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="ba4ad-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="ba4ad-115">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ba4ad-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba4ad-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span><span class="sxs-lookup"><span data-stu-id="ba4ad-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span></span>
</dt> <dd>

<span data-ttu-id="ba4ad-117">Puntatore a una struttura di [**\_ salvataggio \_ parametri di MCI**](mci-save-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ba4ad-117">Pointer to an [**MCI\_SAVE\_PARMS**](mci-save-parms.md) structure.</span></span> <span data-ttu-id="ba4ad-118">I dispositivi con parametri aggiuntivi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-118">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba4ad-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba4ad-119">Return Value</span></span>

<span data-ttu-id="ba4ad-120">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba4ad-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba4ad-121">Remarks</span></span>

<span data-ttu-id="ba4ad-122">Questo comando è supportato dai dispositivi che restituiscono **true** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con MCI \_ GETDEVCAPS \_ can \_ Save flag.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-122">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_SAVE flag.</span></span>

<span data-ttu-id="ba4ad-123">Il flag aggiuntivo seguente si applica a tutti i dispositivi che supportano [MCI \_ Save](/windows):</span><span class="sxs-lookup"><span data-stu-id="ba4ad-123">The following additional flag applies to all devices supporting [MCI\_SAVE](/windows):</span></span>

<dl> <dt>

<span data-ttu-id="ba4ad-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>\_file di salvataggio MCI \_</span><span class="sxs-lookup"><span data-stu-id="ba4ad-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>MCI\_SAVE\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="ba4ad-125">Il membro **lpFileName** della struttura identificata da *lpSave* contiene un indirizzo di un buffer contenente il nome file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-125">The **lpfilename** member of the structure identified by *lpSave* contains an address of a buffer containing the destination filename.</span></span>

</dd> </dl>

<span data-ttu-id="ba4ad-126">Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ba4ad-126">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ba4ad-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>DGV di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba4ad-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="ba4ad-128">Il membro **RC** della struttura identificato da *lpSave* contiene un rettangolo valido.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-128">The **rc** member of the structure identified by *lpSave* contains a valid rectangle.</span></span> <span data-ttu-id="ba4ad-129">Il rettangolo specifica un'area del buffer del frame che verrà salvata nel file specificato.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-129">The rectangle specifies a region of the frame buffer that will be saved to the specified file.</span></span> <span data-ttu-id="ba4ad-130">La prima coppia di coordinate specifica l'angolo superiore sinistro del rettangolo. la seconda coppia specifica la larghezza e l'altezza.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="ba4ad-131">I dispositivi digitali video devono usare il comando di [ \_ acquisizione MCI](mci-capture.md) per acquisire il contenuto del buffer dei frame.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-131">Digital-video devices must use the [MCI\_CAPTURE](mci-capture.md) command to capture the contents of the frame buffer.</span></span> <span data-ttu-id="ba4ad-132">(I dispositivi overlay video devono usare anche MCI \_ ACQUISISCi.) Questo flag è per la compatibilità con il set di comandi video-overlay di MCI esistente.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-132">(Video-overlay devices should also use MCI\_CAPTURE.) This flag is for compatibility with the existing MCI video-overlay command set.</span></span>

</dd> <dt>

<span data-ttu-id="ba4ad-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>\_interruzione del \_ salvataggio \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="ba4ad-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI\_DGV\_SAVE\_ABORT</span></span>
</dt> <dd>

<span data-ttu-id="ba4ad-134">Arresta un'operazione di salvataggio in corso.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-134">Stops a save operation in progress.</span></span> <span data-ttu-id="ba4ad-135">Deve essere l'unico flag presente.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-135">This must be the only flag present.</span></span>

</dd> <dt>

<span data-ttu-id="ba4ad-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>\_KEEPRESERVE DGV per il \_ salvataggio di MCI \_</span><span class="sxs-lookup"><span data-stu-id="ba4ad-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI\_DGV\_SAVE\_KEEPRESERVE</span></span>
</dt> <dd>

<span data-ttu-id="ba4ad-137">Lo spazio inutilizzato su disco rimasto dal comando [di \_ riserva MCI](mci-reserve.md) originale non viene deallocato.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-137">Unused disk space left over from the original [MCI\_RESERVE](mci-reserve.md) command is not deallocated.</span></span>

</dd> </dl>

<span data-ttu-id="ba4ad-138">Per i dispositivi digitali video, il parametro *lpSave* punta a una [**struttura \_ DGV \_ Save \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="ba4ad-138">For digital-video devices, the *lpSave* parameter points to an [**MCI\_DGV\_SAVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) structure.</span></span>

<span data-ttu-id="ba4ad-139">Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **overlay** :</span><span class="sxs-lookup"><span data-stu-id="ba4ad-139">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ba4ad-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>OVLY di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba4ad-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="ba4ad-141">Il membro **RC** della struttura identificato da *lpSave* contiene un rettangolo di visualizzazione valido che indica l'area del buffer video da salvare.</span><span class="sxs-lookup"><span data-stu-id="ba4ad-141">The **rc** member of the structure identified by *lpSave* contains a valid display rectangle indicating the area of the video buffer to save.</span></span>

</dd> </dl>

<span data-ttu-id="ba4ad-142">Per i dispositivi con sovrimpressione video, il parametro *lpSave* punta a una struttura [**\_ OVLY \_ Save \_ parametri di MCI**](/previous-versions//dd743447(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ba4ad-142">For video-overlay devices, the *lpSave* parameter points to an [**MCI\_OVLY\_SAVE\_PARMS**](/previous-versions//dd743447(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba4ad-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba4ad-143">Requirements</span></span>



| <span data-ttu-id="ba4ad-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba4ad-144">Requirement</span></span> | <span data-ttu-id="ba4ad-145">Valore</span><span class="sxs-lookup"><span data-stu-id="ba4ad-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba4ad-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba4ad-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ba4ad-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ba4ad-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ba4ad-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba4ad-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ba4ad-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ba4ad-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ba4ad-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba4ad-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba4ad-151"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba4ad-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba4ad-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba4ad-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba4ad-153">MCI</span><span class="sxs-lookup"><span data-stu-id="ba4ad-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ba4ad-154">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="ba4ad-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

