---
title: Comando MCI_SEEK (mmsystem. h)
description: Il \_ comando MCI Seek imposta la posizione corrente nel contenuto il più rapidamente possibile.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- Comando MCI_SEEK Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048053"
---
# <a name="mci_seek-command"></a><span data-ttu-id="7c758-104">\_Comando di ricerca MCI</span><span class="sxs-lookup"><span data-stu-id="7c758-104">MCI\_SEEK command</span></span>

<span data-ttu-id="7c758-105">Il \_ comando MCI Seek imposta la posizione corrente nel contenuto il più rapidamente possibile.</span><span class="sxs-lookup"><span data-stu-id="7c758-105">The MCI\_SEEK command changes the current position in the content as quickly as possible.</span></span> <span data-ttu-id="7c758-106">L'output di video e audio è disabilitato durante la ricerca.</span><span class="sxs-lookup"><span data-stu-id="7c758-106">Video and audio output are disabled during the seek.</span></span> <span data-ttu-id="7c758-107">Al termine della ricerca, il dispositivo viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="7c758-107">After the seek is complete, the device is stopped.</span></span> <span data-ttu-id="7c758-108">CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="7c758-108">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="7c758-109">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="7c758-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
);
```



## <a name="parameters"></a><span data-ttu-id="7c758-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c758-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c758-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7c758-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7c758-112">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="7c758-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="7c758-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7c758-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7c758-114">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="7c758-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="7c758-115">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7c758-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c758-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span><span class="sxs-lookup"><span data-stu-id="7c758-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span></span>
</dt> <dd>

<span data-ttu-id="7c758-117">Puntatore a una [**struttura \_ \_ parametri Seek di MCI**](mci-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="7c758-117">Pointer to an [**MCI\_SEEK\_PARMS**](mci-seek-parms.md) structure.</span></span> <span data-ttu-id="7c758-118">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c758-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c758-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c758-119">Return Value</span></span>

<span data-ttu-id="7c758-120">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="7c758-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c758-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c758-121">Remarks</span></span>

<span data-ttu-id="7c758-122">Se la dimensione di un campione di dati per un dispositivo è maggiore di 1 byte, ad esempio con i dati audio stereo della forma d'onda, questo comando si sposta all'inizio dell'esempio più vicino quando una posizione specificata non coincide con l'inizio di un campione.</span><span class="sxs-lookup"><span data-stu-id="7c758-122">If a data sample size for a device is larger than 1 byte (such as with waveform-audio stereo data), this command moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

<span data-ttu-id="7c758-123">I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano la \_ ricerca MCI:</span><span class="sxs-lookup"><span data-stu-id="7c758-123">The following additional flags apply to all devices supporting MCI\_SEEK:</span></span>

<dl> <dt>

<span data-ttu-id="7c758-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>\_ricerca \_ di MCI alla \_ fine</span><span class="sxs-lookup"><span data-stu-id="7c758-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI\_SEEK\_TO\_END</span></span>
</dt> <dd>

<span data-ttu-id="7c758-125">Consente di cercare alla fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="7c758-125">Seek to the end of the content.</span></span>

</dd> <dt>

<span data-ttu-id="7c758-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>\_Inizio ricerca \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="7c758-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI\_SEEK\_TO\_START</span></span>
</dt> <dd>

<span data-ttu-id="7c758-127">Consente di cercare all'inizio del contenuto.</span><span class="sxs-lookup"><span data-stu-id="7c758-127">Seek to the beginning of the content.</span></span>

</dd> <dt>

<span data-ttu-id="7c758-128"><span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a</span><span class="sxs-lookup"><span data-stu-id="7c758-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="7c758-129">Una posizione viene inclusa nel membro **dwTo** della struttura identificata da *lpSeek*.</span><span class="sxs-lookup"><span data-stu-id="7c758-129">A position is included in the **dwTo** member of the structure identified by *lpSeek*.</span></span> <span data-ttu-id="7c758-130">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="7c758-130">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="7c758-131">Non utilizzare questo flag con la ricerca \_ MCI \_ per \_ terminare o MCI \_ Seek \_ per \_ avviare.</span><span class="sxs-lookup"><span data-stu-id="7c758-131">Do not use this flag with MCI\_SEEK\_TO\_END or MCI\_SEEK\_TO\_START.</span></span>

</dd> </dl>

<span data-ttu-id="7c758-132">Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c758-132">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7c758-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI \_ VCR \_ Seek \_ at</span><span class="sxs-lookup"><span data-stu-id="7c758-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI\_VCR\_SEEK\_AT</span></span>
</dt> <dd>

<span data-ttu-id="7c758-134">Il membro **dwAt** della struttura identificata da *lpSeek* contiene un'ora di inizio dell'intero comando.</span><span class="sxs-lookup"><span data-stu-id="7c758-134">The **dwAt** member of the structure identified by *lpSeek* contains a time when the entire command begins.</span></span>

</dd> <dt>

<span data-ttu-id="7c758-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>\_indicatore di \_ ricerca \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="7c758-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI\_VCR\_SEEK\_MARK</span></span>
</dt> <dd>

<span data-ttu-id="7c758-136">Il membro **dwMark** della struttura identificata da *lpSeek* contiene il contrassegno numerato da cercare.</span><span class="sxs-lookup"><span data-stu-id="7c758-136">The **dwMark** member of the structure identified by *lpSeek* contains the numbered mark to search for.</span></span>

</dd> <dt>

<span data-ttu-id="7c758-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>\_ \_ ricerca \_ INversa VCR MCI</span><span class="sxs-lookup"><span data-stu-id="7c758-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI\_VCR\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="7c758-138">Direzione di ricerca inversa; viene usato solo con il flag del \_ contrassegno di ricerca MCI VCR \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7c758-138">Seek direction is reverse; this is used only with the MCI\_VCR\_SEEK\_MARK flag.</span></span>

</dd> </dl>

<span data-ttu-id="7c758-139">Per i dispositivi VCR, il parametro *lpSeek* punta a una struttura [**\_ \_ \_ parametri di ricerca VCR MCI**](mci-vcr-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="7c758-139">For VCR devices, the *lpSeek* parameter points to an [**MCI\_VCR\_SEEK\_PARMS**](mci-vcr-seek-parms.md) structure.</span></span>

<span data-ttu-id="7c758-140">Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **videodisco** :</span><span class="sxs-lookup"><span data-stu-id="7c758-140">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7c758-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI \_ VD \_ Seek \_ inverso</span><span class="sxs-lookup"><span data-stu-id="7c758-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI\_VD\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="7c758-142">Direzione di ricerca inversa.</span><span class="sxs-lookup"><span data-stu-id="7c758-142">Seek direction is reverse.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c758-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c758-143">Requirements</span></span>



| <span data-ttu-id="7c758-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c758-144">Requirement</span></span> | <span data-ttu-id="7c758-145">Valore</span><span class="sxs-lookup"><span data-stu-id="7c758-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c758-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c758-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7c758-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c758-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7c758-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c758-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7c758-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c758-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7c758-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c758-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c758-151"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c758-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c758-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c758-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c758-153">MCI</span><span class="sxs-lookup"><span data-stu-id="7c758-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7c758-154">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="7c758-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

