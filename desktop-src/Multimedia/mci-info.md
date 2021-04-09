---
title: Comando MCI_INFO (mmsystem. h)
description: Il \_ comando MCI info recupera le informazioni sulla stringa da un dispositivo.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- Comando MCI_INFO Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121123"
---
# <a name="mci_info-command"></a><span data-ttu-id="81054-104">\_Comando informazioni MCI</span><span class="sxs-lookup"><span data-stu-id="81054-104">MCI\_INFO command</span></span>

<span data-ttu-id="81054-105">Il \_ comando MCI info recupera le informazioni sulla stringa da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81054-105">The MCI\_INFO command retrieves string information from a device.</span></span> <span data-ttu-id="81054-106">Tutti i dispositivi riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="81054-106">All devices recognize this command.</span></span> <span data-ttu-id="81054-107">Le informazioni vengono restituite nel membro **lpstrReturn** della struttura identificata da *lpinfo*.</span><span class="sxs-lookup"><span data-stu-id="81054-107">Information is returned in the **lpstrReturn** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="81054-108">Il membro **dwRetSize** specifica la lunghezza del buffer per i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="81054-108">The **dwRetSize** member specifies the buffer length for the returned data.</span></span>

<span data-ttu-id="81054-109">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="81054-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
);
```



## <a name="parameters"></a><span data-ttu-id="81054-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="81054-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81054-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="81054-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="81054-112">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="81054-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="81054-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="81054-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="81054-114">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="81054-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="81054-115">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="81054-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="81054-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span><span class="sxs-lookup"><span data-stu-id="81054-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span></span>
</dt> <dd>

<span data-ttu-id="81054-117">Puntatore a una [**struttura \_ \_ parametri info di MCI**](mci-info-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="81054-117">Pointer to an [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure.</span></span> <span data-ttu-id="81054-118">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81054-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81054-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81054-119">Return Value</span></span>

<span data-ttu-id="81054-120">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="81054-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="81054-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="81054-121">Remarks</span></span>

<span data-ttu-id="81054-122">Per tutti i dispositivi che supportano le informazioni su MCI, viene applicato il flag di comando e lo standard aggiuntivo seguente \_ :</span><span class="sxs-lookup"><span data-stu-id="81054-122">The following additional standard and command-specific flag applies to all devices supporting MCI\_INFO:</span></span>

<dl> <dt>

<span data-ttu-id="81054-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>\_prodotto info \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI\_INFO\_PRODUCT</span></span>
</dt> <dd>

<span data-ttu-id="81054-124">Ottiene una descrizione dell'hardware associato a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81054-124">Obtains a description of the hardware associated with a device.</span></span> <span data-ttu-id="81054-125">I dispositivi devono fornire una descrizione che identifichi sia il driver che l'hardware usato.</span><span class="sxs-lookup"><span data-stu-id="81054-125">Devices should supply a description that identifies both the driver and the hardware used.</span></span>

</dd> </dl>

<span data-ttu-id="81054-126">I flag aggiuntivi seguenti si applicano al tipo di dispositivo **CDAudio** :</span><span class="sxs-lookup"><span data-stu-id="81054-126">The following additional flags apply to the **cdaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="81054-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>\_ \_ identità supporto informazioni \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI\_INFO\_MEDIA\_IDENTITY</span></span>
</dt> <dd>

<span data-ttu-id="81054-128">Produce un identificatore univoco per il CD audio attualmente caricato nel lettore sottoposto a query.</span><span class="sxs-lookup"><span data-stu-id="81054-128">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span> <span data-ttu-id="81054-129">Questo flag restituisce una stringa di 16 cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="81054-129">This flag returns a string of 16 hexadecimal digits.</span></span>

</dd> <dt>

<span data-ttu-id="81054-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>\_Media informazioni MCI- \_ \_ UPC</span><span class="sxs-lookup"><span data-stu-id="81054-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI\_INFO\_MEDIA\_UPC</span></span>
</dt> <dd>

<span data-ttu-id="81054-131">Genera il codice di prodotto universale (UPC) codificato in un CD audio.</span><span class="sxs-lookup"><span data-stu-id="81054-131">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="81054-132">L'UPC è una stringa di cifre.</span><span class="sxs-lookup"><span data-stu-id="81054-132">The UPC is a string of digits.</span></span> <span data-ttu-id="81054-133">Potrebbe non essere disponibile per tutti i CDs.</span><span class="sxs-lookup"><span data-stu-id="81054-133">It might not be available for all CDs.</span></span>

</dd> </dl>

<span data-ttu-id="81054-134">I flag aggiuntivi seguenti si applicano al tipo di dispositivo **digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="81054-134">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="81054-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>\_ \_ elemento info DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI\_DGV\_INFO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="81054-136">Costante che indica che le informazioni desiderate sono incluse nel membro **dwItem** della struttura identificata da *lpinfo*.</span><span class="sxs-lookup"><span data-stu-id="81054-136">A constant indicating the information desired is included in the **dwItem** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="81054-137">Per i dispositivi digitali video sono definite le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="81054-137">The following constants are defined for digital-video devices:</span></span>

</dd> <dt>

<span data-ttu-id="81054-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ info \_ audio \_ ALG</span><span class="sxs-lookup"><span data-stu-id="81054-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI\_DGV\_INFO\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="81054-139">Restituisce il nome dell'algoritmo di compressione audio corrente.</span><span class="sxs-lookup"><span data-stu-id="81054-139">Returns the name for the current audio compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="81054-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>\_ \_ \_ qualità audio informazioni DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI\_DGV\_INFO\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="81054-141">Restituisce il nome del descrittore di qualità audio corrente.</span><span class="sxs-lookup"><span data-stu-id="81054-141">Returns the name for the current audio quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="81054-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>\_informazioni su DGV MCI \_ \_ ancora \_ ALG</span><span class="sxs-lookup"><span data-stu-id="81054-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI\_DGV\_INFO\_STILL\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="81054-143">Restituisce il nome dell'algoritmo di compressione delle immagini ancora corrente.</span><span class="sxs-lookup"><span data-stu-id="81054-143">Returns the name for the current still image compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="81054-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>\_informazioni sul DGV MCI \_ \_ ancora \_ qualità</span><span class="sxs-lookup"><span data-stu-id="81054-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI\_DGV\_INFO\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="81054-145">Restituisce il nome del descrittore di qualità dell'immagine ancora corrente.</span><span class="sxs-lookup"><span data-stu-id="81054-145">Returns the name for the current still image quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="81054-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>\_utilizzo delle \_ informazioni \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="81054-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>MCI\_DGV\_INFO\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="81054-147">Restituisce una stringa che descrive le restrizioni di utilizzo che potrebbero essere imposte dal proprietario dei dati visivi o udibili nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="81054-147">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audible data in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="81054-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI \_ DGV \_ info \_ video \_ ALG</span><span class="sxs-lookup"><span data-stu-id="81054-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI\_DGV\_INFO\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="81054-149">Restituisce il nome dell'algoritmo di compressione video corrente.</span><span class="sxs-lookup"><span data-stu-id="81054-149">Returns the name for the current video compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="81054-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>\_ \_ \_ qualità video informazioni DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI\_DGV\_INFO\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="81054-151">Restituisce il nome del descrittore di qualità video corrente.</span><span class="sxs-lookup"><span data-stu-id="81054-151">Returns the name for the current video quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="81054-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>\_versione informazioni \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="81054-153">Restituisce il livello di rilascio del driver e dell'hardware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81054-153">Returns the release level of the device driver and hardware.</span></span> <span data-ttu-id="81054-154">Gli sviluppatori di driver di dispositivo devono documentare la sintassi della stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="81054-154">Device driver developers must document the syntax of the returned string.</span></span>

</dd> <dt>

<span data-ttu-id="81054-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>\_ \_ testo informazioni DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI\_DGV\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="81054-156">Ottiene la didascalia della finestra.</span><span class="sxs-lookup"><span data-stu-id="81054-156">Obtains the window caption.</span></span>

</dd> <dt>

<span data-ttu-id="81054-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_file di informazioni MCI \_</span><span class="sxs-lookup"><span data-stu-id="81054-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="81054-158">Ottiene il percorso e il nome del file dell'ultimo file specificato con il comando [MCI \_ Open](mci-open.md) o [MCI \_ Load](mci-load.md) .</span><span class="sxs-lookup"><span data-stu-id="81054-158">Obtains the path and filename of the last file specified with the [MCI\_OPEN](mci-open.md) or [MCI\_LOAD](mci-load.md) command.</span></span> <span data-ttu-id="81054-159">Se non è stato specificato un file, il dispositivo restituisce una stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="81054-159">If a file has not been specified, the device returns a null-terminated string.</span></span> <span data-ttu-id="81054-160">Questo flag è supportato solo dai dispositivi che restituiscono **true** al \_ GETDEVCAPS MCI \_ Usa il \_ flag file del [comando \_ GETDEVCAPS di MCI](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="81054-160">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

<span data-ttu-id="81054-161">Per i dispositivi digitali video, *lpinfo* punta a una [**struttura \_ DGV \_ info \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="81054-161">For digital-video devices, *lpInfo* points to an [**MCI\_DGV\_INFO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) structure.</span></span>

<span data-ttu-id="81054-162">I flag aggiuntivi seguenti si applicano al tipo di dispositivo **sequencer** :</span><span class="sxs-lookup"><span data-stu-id="81054-162">The following additional flags apply to the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="81054-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>\_informazioni \_ sul copyright di MCI</span><span class="sxs-lookup"><span data-stu-id="81054-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI\_INFO\_COPYRIGHT</span></span>
</dt> <dd>

<span data-ttu-id="81054-164">Ottiene le informazioni sul copyright del file MIDI dall'evento meta del copyright.</span><span class="sxs-lookup"><span data-stu-id="81054-164">Obtains the MIDI file copyright notice from the copyright meta event.</span></span>

</dd> <dt>

<span data-ttu-id="81054-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_file di informazioni MCI \_</span><span class="sxs-lookup"><span data-stu-id="81054-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="81054-166">Ottiene il nome del file corrente.</span><span class="sxs-lookup"><span data-stu-id="81054-166">Obtains the filename of the current file.</span></span> <span data-ttu-id="81054-167">Questo flag è supportato solo dai dispositivi che restituiscono **true** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con il \_ flag MCI GETDEVCAPS \_ Usa \_ i file.</span><span class="sxs-lookup"><span data-stu-id="81054-167">This flag is supported only by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="81054-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>\_nome informazioni \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI\_INFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="81054-169">Ottiene il nome della sequenza dall'evento meta del nome di sequenza/track.</span><span class="sxs-lookup"><span data-stu-id="81054-169">Obtains the sequence name from the sequence/track name meta event.</span></span>

</dd> </dl>

<span data-ttu-id="81054-170">Il flag aggiuntivo seguente si applica al tipo di dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="81054-170">The following additional flag applies to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="81054-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>\_ \_ versione informazioni VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI\_VCR\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="81054-172">Imposta il membro **lpstrReturn** della [**struttura \_ \_ parametri info di MCI**](mci-info-parms.md) in modo che punti al numero di versione.</span><span class="sxs-lookup"><span data-stu-id="81054-172">Sets **lpstrReturn** member of the [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure to point to the version number.</span></span> <span data-ttu-id="81054-173">Imposta anche il membro **dwRetSize** uguale alla lunghezza della stringa a cui punta.</span><span class="sxs-lookup"><span data-stu-id="81054-173">Also sets the **dwRetSize** member equal to the length of the string pointed to.</span></span>

</dd> </dl>

<span data-ttu-id="81054-174">I flag aggiuntivi seguenti si applicano al tipo di dispositivo **overlay** :</span><span class="sxs-lookup"><span data-stu-id="81054-174">The following additional flags apply to the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="81054-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_file di informazioni MCI \_</span><span class="sxs-lookup"><span data-stu-id="81054-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="81054-176">Ottiene il nome del file corrente.</span><span class="sxs-lookup"><span data-stu-id="81054-176">Obtains the filename of the current file.</span></span> <span data-ttu-id="81054-177">Questo flag è supportato solo dai dispositivi che restituiscono **true** al \_ GETDEVCAPS MCI \_ Usa il \_ flag file del [comando \_ GETDEVCAPS di MCI](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="81054-177">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="81054-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>\_ \_ testo informazioni OVLY \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI\_OVLY\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="81054-179">Ottiene la didascalia della finestra associata al dispositivo di sovrimpressione video.</span><span class="sxs-lookup"><span data-stu-id="81054-179">Obtains the caption of the window associated with the video-overlay device.</span></span>

</dd> </dl>

<span data-ttu-id="81054-180">I flag aggiuntivi seguenti si applicano al tipo di dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="81054-180">The following additional flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="81054-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_file di informazioni MCI \_</span><span class="sxs-lookup"><span data-stu-id="81054-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="81054-182">Ottiene il nome del file corrente.</span><span class="sxs-lookup"><span data-stu-id="81054-182">Obtains the filename of the current file.</span></span> <span data-ttu-id="81054-183">Questo flag è supportato dai dispositivi che restituiscono **true** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con il \_ flag MCI GETDEVCAPS \_ Usa \_ i file.</span><span class="sxs-lookup"><span data-stu-id="81054-183">This flag is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="81054-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_input wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="81054-185">Ottiene il nome del prodotto dell'input corrente.</span><span class="sxs-lookup"><span data-stu-id="81054-185">Obtains the product name of the current input.</span></span>

</dd> <dt>

<span data-ttu-id="81054-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_Output Wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="81054-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="81054-187">Ottiene il nome del prodotto dell'output corrente e il relativo valore è specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81054-187">Obtains the product name of the current output and its value is device specific.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81054-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81054-188">Requirements</span></span>



| <span data-ttu-id="81054-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="81054-189">Requirement</span></span> | <span data-ttu-id="81054-190">Valore</span><span class="sxs-lookup"><span data-stu-id="81054-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81054-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81054-191">Minimum supported client</span></span><br/> | <span data-ttu-id="81054-192">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81054-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="81054-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81054-193">Minimum supported server</span></span><br/> | <span data-ttu-id="81054-194">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81054-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="81054-195">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81054-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="81054-196"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81054-196"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81054-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81054-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81054-198">MCI</span><span class="sxs-lookup"><span data-stu-id="81054-198">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="81054-199">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="81054-199">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

