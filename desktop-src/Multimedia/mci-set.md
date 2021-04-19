---
title: Comando MCI_SET (mmsystem. h)
description: Il \_ set di comandi MCI set imposta le informazioni sul dispositivo. CD audio, Digital-video, MIDI sequencer, VCR, videodisco, video-overlay e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- Comando MCI_SET Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "106320057"
---
# <a name="mci_set-command"></a><span data-ttu-id="a0f90-105">\_Comando set MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-105">MCI\_SET command</span></span>

> [!NOTE]
> <span data-ttu-id="a0f90-106">Comunicazione senza distorsione Microsoft supporta un ambiente diversificato e di inclusione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="a0f90-107">All'interno di questo documento sono presenti riferimenti alla parola "slave".</span><span class="sxs-lookup"><span data-stu-id="a0f90-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="a0f90-108">La [Guida di stile di Microsoft per le comunicazioni di Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) riconosce questo aspetto come una parola di esclusione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="a0f90-109">Questo testo viene usato in quanto è attualmente il testo usato nei comandi.</span><span class="sxs-lookup"><span data-stu-id="a0f90-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="a0f90-110">Per coerenza, questo documento contiene questa parola.</span><span class="sxs-lookup"><span data-stu-id="a0f90-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="a0f90-111">Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo da essere in allineamento.</span><span class="sxs-lookup"><span data-stu-id="a0f90-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="a0f90-112">Il \_ set di comandi MCI set imposta le informazioni sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0f90-112">The MCI\_SET command sets device information.</span></span> <span data-ttu-id="a0f90-113">CD audio, Digital-video, MIDI sequencer, VCR, videodisco, video-overlay e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="a0f90-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="a0f90-114">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a0f90-114">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
);
```



## <a name="parameters"></a><span data-ttu-id="a0f90-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0f90-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f90-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a0f90-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-117">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="a0f90-117">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a0f90-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-119">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a0f90-119">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="a0f90-120">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a0f90-120">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span><span class="sxs-lookup"><span data-stu-id="a0f90-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-122">Puntatore a una [**struttura \_ \_ parametri set di MCI**](mci-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f90-122">Pointer to an [**MCI\_SET\_PARMS**](mci-set-parms.md) structure.</span></span> <span data-ttu-id="a0f90-123">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0f90-123">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f90-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0f90-124">Return Value</span></span>

<span data-ttu-id="a0f90-125">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="a0f90-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0f90-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0f90-126">Remarks</span></span>

<span data-ttu-id="a0f90-127">I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano \_ set MCI:</span><span class="sxs-lookup"><span data-stu-id="a0f90-127">The following additional flags apply to all devices supporting MCI\_SET:</span></span>

<dl> <dt>

<span data-ttu-id="a0f90-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>\_audio set \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI\_SET\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-129">Un numero di canale audio è incluso nel membro dwAudio della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-129">An audio channel number is included in the dwAudio member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="a0f90-130">Questo flag deve essere utilizzato con MCI \_ impostato \_ su o MCI \_ impostato su \_ off.</span><span class="sxs-lookup"><span data-stu-id="a0f90-130">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="a0f90-131">Per indicare il numero di canale, utilizzare una delle costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-131">Use one of the following constants to indicate the channel number:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>\_ \_ tutti i set audio MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI\_SET\_AUDIO\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-133">Tutti i canali audio.</span><span class="sxs-lookup"><span data-stu-id="a0f90-133">All audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>\_audio set \_ MCI \_ lasciato</span><span class="sxs-lookup"><span data-stu-id="a0f90-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI\_SET\_AUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-135">Canale sinistro.</span><span class="sxs-lookup"><span data-stu-id="a0f90-135">Left channel.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>\_set di \_ audio a \_ destra di MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI\_SET\_AUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-137">Canale destro.</span><span class="sxs-lookup"><span data-stu-id="a0f90-137">Right channel.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>\_sportello set \_ MCI \_ chiuso</span><span class="sxs-lookup"><span data-stu-id="a0f90-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI\_SET\_DOOR\_CLOSED</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-139">Chiude il coperchio del supporto (se presente).</span><span class="sxs-lookup"><span data-stu-id="a0f90-139">Closes the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>\_ \_ Apri sportello set \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI\_SET\_DOOR\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-141">Apre il coperchio del supporto (se presente).</span><span class="sxs-lookup"><span data-stu-id="a0f90-141">Opens the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato</span><span class="sxs-lookup"><span data-stu-id="a0f90-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-143">Disabilita il video o il canale audio specificato.</span><span class="sxs-lookup"><span data-stu-id="a0f90-143">Disables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su</span><span class="sxs-lookup"><span data-stu-id="a0f90-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-145">Abilita il canale audio o video specificato.</span><span class="sxs-lookup"><span data-stu-id="a0f90-145">Enables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>\_ \_ formato ora set \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI\_SET\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-147">Un parametro di formato dell'ora è incluso nel membro **dwTimeFormat** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-147">A time format parameter is included in the **dwTimeFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="a0f90-148">Con questo flag vengono usati i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-148">The following flags are used with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>\_byte in formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>MCI\_FORMAT\_BYTES</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-150">All'interno di un formato dati PCM (Pulse Code Modulation), modifica la descrizione del membro dell'ora in byte per l'input o l'output.</span><span class="sxs-lookup"><span data-stu-id="a0f90-150">Within a PCM (Pulse Code Modulation) data format, changes the time member description to bytes for input or output.</span></span> <span data-ttu-id="a0f90-151">Riconosciuta dal tipo di dispositivo **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="a0f90-151">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>\_frame di formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MCI\_FORMAT\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-153">I comandi successivi utilizzeranno i frame.</span><span class="sxs-lookup"><span data-stu-id="a0f90-153">Subsequent commands will use frames.</span></span> <span data-ttu-id="a0f90-154">Riconosciuta dai tipi di dispositivi **digitalvideo**, **VCR** e **videodisco** .</span><span class="sxs-lookup"><span data-stu-id="a0f90-154">Recognized by the **digitalvideo**, **vcr**, and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>\_formato MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="a0f90-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI\_FORMAT\_HMS</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-156">Modifica il formato dell'ora in ore, minuti e secondi.</span><span class="sxs-lookup"><span data-stu-id="a0f90-156">Changes the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="a0f90-157">Riconosciuta dai tipi di dispositivo **VCR** e **videodisco** .</span><span class="sxs-lookup"><span data-stu-id="a0f90-157">Recognized by the **vcr** and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>\_ \_ millisecondi formato MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MCI\_FORMAT\_MILLISECONDS</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-159">Modifica il formato dell'ora in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a0f90-159">Changes the time format to milliseconds.</span></span> <span data-ttu-id="a0f90-160">Riconosciuta da tutti i tipi di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0f90-160">Recognized by all device types.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>\_MSF formato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI\_FORMAT\_MSF</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-162">Modifica il formato dell'ora in minuti, secondi e frame.</span><span class="sxs-lookup"><span data-stu-id="a0f90-162">Changes the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="a0f90-163">Riconosciuta dai tipi di dispositivo **CDAudio** e **VCR** .</span><span class="sxs-lookup"><span data-stu-id="a0f90-163">Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>\_esempi di formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>MCI\_FORMAT\_SAMPLES</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-165">Modifica il formato dell'ora in esempi per l'input o l'output.</span><span class="sxs-lookup"><span data-stu-id="a0f90-165">Changes the time format to samples for input or output.</span></span> <span data-ttu-id="a0f90-166">Riconosciuta dal tipo di dispositivo **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="a0f90-166">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI \_ Format \_ SMPTE \_ 24, MCI \_ Format \_ SMPTE \_ 25 e MCI \_ Format \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="a0f90-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI\_FORMAT\_SMPTE\_24, MCI\_FORMAT\_SMPTE\_25, and MCI\_FORMAT\_SMPTE\_30</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-168">Imposta il formato dell'ora su 24, 25 e 30 frame SMPTE (Society of Motion Picture and Television Engineers), rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="a0f90-168">Sets the time format to 24, 25, and 30 frame SMPTE (Society of Motion Picture and Television Engineers), respectively.</span></span> <span data-ttu-id="a0f90-169">Riconosciuta dai tipi di dispositivo **sequencer** e **VCR** .</span><span class="sxs-lookup"><span data-stu-id="a0f90-169">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>\_Formato MCI \_ \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="a0f90-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI\_FORMAT\_SMPTE\_30DROP</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-171">Imposta il formato dell'ora su 30 SMPTE del frame di rilascio.</span><span class="sxs-lookup"><span data-stu-id="a0f90-171">Sets the time format to 30 drop-frame SMPTE.</span></span> <span data-ttu-id="a0f90-172">Riconosciuta dai tipi di dispositivo **sequencer** e **VCR** .</span><span class="sxs-lookup"><span data-stu-id="a0f90-172">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="a0f90-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>MCI\_FORMAT\_TMSF</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-174">Modifica il formato dell'ora in tracce, minuti, secondi e frame.</span><span class="sxs-lookup"><span data-stu-id="a0f90-174">Changes the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="a0f90-175">(MCI usa i numeri di traccia continui). Riconosciuta dai tipi di dispositivo **CDAudio** e **VCR** .</span><span class="sxs-lookup"><span data-stu-id="a0f90-175">(MCI uses continuous track numbers.) Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>\_video su set MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI\_SET\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-177">Imposta il segnale video su on o off.</span><span class="sxs-lookup"><span data-stu-id="a0f90-177">Sets the video signal on or off.</span></span> <span data-ttu-id="a0f90-178">Questo flag deve essere utilizzato con MCI \_ impostato \_ su o MCI \_ impostato su \_ off.</span><span class="sxs-lookup"><span data-stu-id="a0f90-178">This flag must be used with either MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="a0f90-179">I dispositivi che non hanno il video restituiscono MCIERR \_ funzione non supportata \_ .</span><span class="sxs-lookup"><span data-stu-id="a0f90-179">Devices that do not have video return MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="a0f90-180">Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a0f90-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>\_ \_ set \_ FileFormat DGV di MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI\_DGV\_SET\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-182">Un parametro del formato di file è incluso nel membro **dwFileFormat** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-182">A file format parameter is included in the **dwFileFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="a0f90-183">Per i dispositivi digitali video, il formato di file viene usato per i comandi di salvataggio o acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-183">For digital-video devices, the file format is used for save or capture commands.</span></span> <span data-ttu-id="a0f90-184">Se omesso, per impostazione predefinita è possibile che sia un formato definito dal driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0f90-184">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="a0f90-185">Se il formato di file specificato è in conflitto con l'algoritmo e la qualità attualmente selezionati, verranno modificati nei valori predefiniti per il formato di file.</span><span class="sxs-lookup"><span data-stu-id="a0f90-185">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="a0f90-186">Sono definite le costanti di formato di file seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-186">The following file format constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>DGV di MCI \_ \_ FF \_ AVI</span><span class="sxs-lookup"><span data-stu-id="a0f90-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI\_DGV\_FF\_AVI</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-188">Formato AVI.</span><span class="sxs-lookup"><span data-stu-id="a0f90-188">AVI format.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ avss</span><span class="sxs-lookup"><span data-stu-id="a0f90-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI\_DGV\_FF\_AVSS</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-190">Formato AVSS.</span><span class="sxs-lookup"><span data-stu-id="a0f90-190">AVSS format.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>\_DIB DGV MCI \_ FF \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI\_DGV\_FF\_DIB</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-192">Formato DIB.</span><span class="sxs-lookup"><span data-stu-id="a0f90-192">DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ JFIF</span><span class="sxs-lookup"><span data-stu-id="a0f90-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI\_DGV\_FF\_JFIF</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-194">Formato JFIF.</span><span class="sxs-lookup"><span data-stu-id="a0f90-194">JFIF format.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>DGV di MCI \_ \_ FF \_ JPEG</span><span class="sxs-lookup"><span data-stu-id="a0f90-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI\_DGV\_FF\_JPEG</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-196">Formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="a0f90-196">JPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>DGV di MCI \_ \_ FF \_ MPEG</span><span class="sxs-lookup"><span data-stu-id="a0f90-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI\_DGV\_FF\_MPEG</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-198">Formato MPEG.</span><span class="sxs-lookup"><span data-stu-id="a0f90-198">MPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ RDIB</span><span class="sxs-lookup"><span data-stu-id="a0f90-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI\_DGV\_FF\_RDIB</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-200">Formato DIB RLE.</span><span class="sxs-lookup"><span data-stu-id="a0f90-200">RLE DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ RJPEG</span><span class="sxs-lookup"><span data-stu-id="a0f90-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI\_DGV\_FF\_RJPEG</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-202">Formato RJPEG.</span><span class="sxs-lookup"><span data-stu-id="a0f90-202">RJPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>la \_ ricerca del set di DGV MCI è \_ \_ \_ esatta</span><span class="sxs-lookup"><span data-stu-id="a0f90-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI\_DGV\_SET\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-204">Imposta il formato utilizzato per il posizionamento.</span><span class="sxs-lookup"><span data-stu-id="a0f90-204">Sets the format used for positioning.</span></span> <span data-ttu-id="a0f90-205">Questo flag deve essere utilizzato con MCI \_ impostato \_ su o MCI \_ impostato su \_ off.</span><span class="sxs-lookup"><span data-stu-id="a0f90-205">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="a0f90-206">Se \_ \_ è specificato MCI impostato su, la riproduzione o la registrazione di accede con precisione al frame specificato con il \_ flag MCI from.</span><span class="sxs-lookup"><span data-stu-id="a0f90-206">If MCI\_SET\_ON is specified, playing or recording precisely accesses the frame specified with the MCI\_FROM flag.</span></span> <span data-ttu-id="a0f90-207">Questo potrebbe aggiungere un ritardo aggiuntivo se il frame richiesto non è un fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="a0f90-207">This might add some extra delay if the requested frame is not a key frame.</span></span> <span data-ttu-id="a0f90-208">Se \_ si specifica MCI impostato su \_ off, il dispositivo cercherà un'immagine con fotogrammi chiave che precede il frame richiesto.</span><span class="sxs-lookup"><span data-stu-id="a0f90-208">If MCI\_SET\_OFF is specified, the device will seek to a key-frame image that precedes the requested frame.</span></span> <span data-ttu-id="a0f90-209">Per alcuni file e dispositivi, potrebbe trattarsi del primo frame del file.</span><span class="sxs-lookup"><span data-stu-id="a0f90-209">For some files and devices, this might be the first frame of the file.</span></span> <span data-ttu-id="a0f90-210">Il valore predefinito per questo flag è dipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0f90-210">The default for this flag is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>\_velocità di \_ impostazione \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI\_DGV\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-212">Un parametro della velocità è incluso nel membro **dwSpeed** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-212">A speed parameter is included in the **dwSpeed** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="a0f90-213">La velocità viene specificata come rapporto tra la frequenza dei fotogrammi nominale e la frequenza dei fotogrammi desiderata, in cui la frequenza dei fotogrammi nominale viene designata come 1000.</span><span class="sxs-lookup"><span data-stu-id="a0f90-213">Speed is specified as a ratio between the nominal frame rate and the desired frame rate where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="a0f90-214">La metà della velocità è 500 e la velocità doppia è 2000.</span><span class="sxs-lookup"><span data-stu-id="a0f90-214">Half speed is 500 and double speed is 2000.</span></span> <span data-ttu-id="a0f90-215">L'intervallo di velocità consentito dipende anche dal dispositivo e possibilmente dal file.</span><span class="sxs-lookup"><span data-stu-id="a0f90-215">The allowable speed range is dependent on the device and possibly the file, too.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>\_set di DGV MCI \_ \_ ancora</span><span class="sxs-lookup"><span data-stu-id="a0f90-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>MCI\_DGV\_SET\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-217">Se usato con MCI \_ DGV \_ set \_ FileFormat, MCI \_ set imposta il formato di file usato per i comandi di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-217">When used with MCI\_DGV\_SET\_FILEFORMAT, MCI\_SET sets the file format used for capture commands.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="a0f90-218">Per i dispositivi digitali video, il parametro *lpSet* punta a una struttura [**MCI \_ DGV \_ set \_ parametri**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) .</span><span class="sxs-lookup"><span data-stu-id="a0f90-218">For digital-video devices, the *lpSet* parameter points to an [**MCI\_DGV\_SET\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) structure.</span></span>

<span data-ttu-id="a0f90-219">Con il tipo di dispositivo **sequencer** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-219">The following additional flags are used with the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a0f90-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>\_ \_ formato SONGPTR MCI \_ Seq</span><span class="sxs-lookup"><span data-stu-id="a0f90-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI\_SEQ\_FORMAT\_SONGPTR</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-221">Imposta il formato dell'ora sulle unità del puntatore del brano.</span><span class="sxs-lookup"><span data-stu-id="a0f90-221">Sets the time format to song pointer units.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>\_ \_ Master set Seq di MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI\_SEQ\_SET\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-223">Imposta sequencer come origine dei dati di sincronizzazione e indica che il tipo di sincronizzazione viene specificato nel membro **dwMaster** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-223">Sets the sequencer as a source of synchronization data and indicates that the type of synchronization is specified in the **dwMaster** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="a0f90-224">MCISEQ restituisce la \_ funzione MCIERR non supportata \_ .</span><span class="sxs-lookup"><span data-stu-id="a0f90-224">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="a0f90-225">Per il tipo di sincronizzazione sono definite le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-225">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>\_MIDI seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="a0f90-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-227">Sequencer invierà i dati di sincronizzazione del formato MIDI.</span><span class="sxs-lookup"><span data-stu-id="a0f90-227">The sequencer will send MIDI format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>sequenza di MCI \_ seq \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-229">Sequencer invierà i dati di sincronizzazione del formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a0f90-229">The sequencer will send SMPTE format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_nessuno Seq seq \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-231">Sequencer non invierà i dati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-231">The sequencer will not send synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>\_ \_ offset set seq \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI\_SEQ\_SET\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-233">Modifica l'offset SMPTE di una sequenza in quella specificata dal membro **dwOffset** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-233">Changes the SMPTE offset of a sequence to that specified by the **dwOffset** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="a0f90-234">Questa operazione ha effetto solo sulle sequenze con un tipo di divisione SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a0f90-234">This affects only sequences with a SMPTE division type.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>\_ \_ porta set SEQ per MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI\_SEQ\_SET\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-236">Imposta la porta MIDI di output di una sequenza su quella specificata dall'identificatore del dispositivo MIDI nel membro **dwPort** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-236">Sets the output MIDI port of a sequence to that specified by the MIDI device identifier in the **dwPort** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="a0f90-237">Il dispositivo chiude la porta precedente (se presente) e tenta di aprire e usare la nuova porta.</span><span class="sxs-lookup"><span data-stu-id="a0f90-237">The device closes the previous port (if any), and attempts to open and use the new port.</span></span> <span data-ttu-id="a0f90-238">Se ha esito negativo, restituisce un errore e riapre la porta usata in precedenza (se presente).</span><span class="sxs-lookup"><span data-stu-id="a0f90-238">If it fails, it returns an error and reopens the previously used port (if any).</span></span> <span data-ttu-id="a0f90-239">Per le porte sono definite le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-239">The following constants are defined for the ports:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_nessuno Seq seq \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-241">Chiude la porta utilizzata in precedenza (se presente).</span><span class="sxs-lookup"><span data-stu-id="a0f90-241">Closes the previously used port (if any).</span></span> <span data-ttu-id="a0f90-242">Sequencer si comporta esattamente come se fosse aperta una porta, ad eccezione del fatto che non viene inviato alcun messaggio MIDI.</span><span class="sxs-lookup"><span data-stu-id="a0f90-242">The sequencer behaves exactly the same as if a port were open, except no MIDI message is sent.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>\_Mapper MIDI</span><span class="sxs-lookup"><span data-stu-id="a0f90-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI\_MAPPER</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-244">Imposta la porta aperta per il mapper MIDI.</span><span class="sxs-lookup"><span data-stu-id="a0f90-244">Sets the port opened to the MIDI mapper.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>\_ \_ set \_ slave per MCI Seq</span><span class="sxs-lookup"><span data-stu-id="a0f90-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI\_SEQ\_SET\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-246">Imposta sequencer per la ricezione dei dati di sincronizzazione e indica che il tipo di sincronizzazione viene specificato nel membro **dwSlave** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-246">Sets the sequencer to receive synchronization data and indicates that the type of synchronization is specified in the **dwSlave** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="a0f90-247">MCISEQ restituisce la \_ funzione MCIERR non supportata \_ .</span><span class="sxs-lookup"><span data-stu-id="a0f90-247">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="a0f90-248">Per il tipo di sincronizzazione sono definite le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-248">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>\_file SEQ di MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI\_SEQ\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-250">Imposta sequencer per la ricezione dei dati di sincronizzazione contenuti nel file MIDI.</span><span class="sxs-lookup"><span data-stu-id="a0f90-250">Sets the sequencer to receive synchronization data contained in the MIDI file.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>\_MIDI seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="a0f90-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-252">Imposta sequencer per la ricezione dei dati di sincronizzazione MIDI.</span><span class="sxs-lookup"><span data-stu-id="a0f90-252">Sets the sequencer to receive MIDI synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_nessuno Seq seq \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-254">Imposta sequencer per ignorare i dati di sincronizzazione in un flusso MIDI.</span><span class="sxs-lookup"><span data-stu-id="a0f90-254">Sets the sequencer to ignore synchronization data in a MIDI stream.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>sequenza di MCI \_ seq \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-256">Imposta sequencer per la ricezione dei dati di sincronizzazione SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a0f90-256">Sets the sequencer to receive SMPTE synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>\_ \_ set \_ tempo per MCI Seq</span><span class="sxs-lookup"><span data-stu-id="a0f90-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI\_SEQ\_SET\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-258">Imposta il tempo della sequenza MIDI su quello specificato dal membro **dwTempo** della struttura a cui punta *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-258">Changes the tempo of the MIDI sequence to that specified by the **dwTempo** member of the structure pointed to by *lpSet*.</span></span> <span data-ttu-id="a0f90-259">Per le sequenze con tipo di divisione PPQN, il tempo viene specificato in battute al minuto; per le sequenze con tipo di divisione SMPTE, il tempo viene specificato in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="a0f90-259">For sequences with division type PPQN, tempo is specified in beats per minute; for sequences with division type SMPTE, tempo is specified in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="a0f90-260">Per i dispositivi sequencer, il parametro *lpSet* punta a una struttura [**parametri di MCI \_ seq \_ set \_**](mci-seq-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f90-260">For sequencer devices, the *lpSet* parameter points to an [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure.</span></span>

<span data-ttu-id="a0f90-261">Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-261">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a0f90-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>\_record di \_ \_ assemblaggio set VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI\_VCR\_SET\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-263">Imposta la registrazione del dispositivo in modalità assembla o Inserisci (quando il montaggio è disattivato, INSERT è on e viceversa).</span><span class="sxs-lookup"><span data-stu-id="a0f90-263">Sets the device to record in assemble or insert modes (when assemble is off, insert is on, and vice-versa).</span></span> <span data-ttu-id="a0f90-264">Usare con uno dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-264">Use with one of the following flag:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su</span><span class="sxs-lookup"><span data-stu-id="a0f90-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-266">Imposta assembla record su e disattiva il record di inserimento.</span><span class="sxs-lookup"><span data-stu-id="a0f90-266">Sets assemble record on, and turns insert record off.</span></span> <span data-ttu-id="a0f90-267">Registra tutte le tracce video, audio e timecode.</span><span class="sxs-lookup"><span data-stu-id="a0f90-267">Records all video, audio and timecode tracks.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato</span><span class="sxs-lookup"><span data-stu-id="a0f90-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-269">Imposta assembla record off e attiva il record di inserimento.</span><span class="sxs-lookup"><span data-stu-id="a0f90-269">Sets assemble record off, and turns insert record on.</span></span> <span data-ttu-id="a0f90-270">Quando il record di assemblaggio è disattivato, è possibile selezionare singole tracce di video, audio e timecode per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-270">When assemble record is off, individual tracks of video, audio, and timecode can be selected for recording.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>\_ \_ clock set VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI\_VCR\_SET\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-272">Il membro **dwClock** della struttura identificata da *lpSet* contiene la nuova ora di clock.</span><span class="sxs-lookup"><span data-stu-id="a0f90-272">The **dwClock** member of the structure identified by *lpSet* contains the new clock time.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>forma \_ \_ contatore set \_ VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI\_VCR\_SET\_COUNTER\_FORMA</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-274">Il membro **dwCounterFormat** della struttura identificata da *lpSet* contiene una costante che specifica il nuovo formato del contatore di tempo che deve essere utilizzato dal contatore di stato.</span><span class="sxs-lookup"><span data-stu-id="a0f90-274">The **dwCounterFormat** member of the structure identified by *lpSet* contains a constant specifying the new counter-time format to be used by the status counter.</span></span> <span data-ttu-id="a0f90-275">Per un elenco di costanti valide, vedere MCI \_ set \_ time \_ format nell'elenco di flag aggiuntivi per questo comando.</span><span class="sxs-lookup"><span data-stu-id="a0f90-275">For a list of valid constants, see MCI\_SET\_TIME\_FORMAT in the list of additional flags for this command.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>\_ \_ \_ valore contatore set VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI\_VCR\_SET\_COUNTER\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-277">Il membro **dwCounterValue** della struttura identificata da *lpSet* contiene il nuovo valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="a0f90-277">The **dwCounterValue** member of the structure identified by *lpSet* contains the new counter value.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>\_ \_ indice set VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI\_VCR\_SET\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-279">Il membro **dwIndex** della struttura identificata da *lpSet* contiene una costante che indica il contenuto della visualizzazione sullo schermo e deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-279">The **dwIndex** member of the structure identified by *lpSet* contains a constant indicating the contents of the on-screen display and must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>\_ \_ contatore indice VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>MCI\_VCR\_INDEX\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-281">Visualizza il contatore.</span><span class="sxs-lookup"><span data-stu-id="a0f90-281">Displays counter.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>\_Data di \_ Indice MCI VCR \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>MCI\_VCR\_INDEX\_DATE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-283">Visualizza la data.</span><span class="sxs-lookup"><span data-stu-id="a0f90-283">Displays date.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>\_ora di \_ indicizzazione VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI\_VCR\_INDEX\_TIME</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-285">Visualizza l'ora.</span><span class="sxs-lookup"><span data-stu-id="a0f90-285">Displays time.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>\_ \_ codice temporale dell'indice MCI VCR \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>MCI\_VCR\_INDEX\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-287">Visualizza il timecode.</span><span class="sxs-lookup"><span data-stu-id="a0f90-287">Displays timecode.</span></span>

<span data-ttu-id="a0f90-288">Per ulteriori informazioni, vedere il comando [MCI \_ index](mci-index.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f90-288">For more information, see the [MCI\_INDEX](mci-index.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>\_timeout della \_ \_ pausa set del VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI\_VCR\_SET\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-290">Il membro **dwPauseTimeout** della struttura identificata da *lpSet* contiene la durata massima, in millisecondi, di un comando di sospensione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-290">The **dwPauseTimeout** member of the structure identified by *lpSet* contains the maximum duration, in milliseconds, of a pause command.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>\_ \_ \_ durata postroll del set di VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI\_VCR\_SET\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-292">Il membro **dwPostrollDuration** della struttura identificata da *lpSet* contiene la lunghezza del nastro, nel formato dell'ora corrente, necessaria per bloccare il trasporto del videoregistratore quando viene emesso un comando di arresto o sospensione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-292">The **dwPostrollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to brake the VCR transport when a stop or pause command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>\_ \_ Power set VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI\_VCR\_SET\_POWER</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-294">Consente di attivare o disattivare l'accensione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-294">Sets the power on or off.</span></span> <span data-ttu-id="a0f90-295">Deve essere usato con uno dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-295">Must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato</span><span class="sxs-lookup"><span data-stu-id="a0f90-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-297">Disattiva lo spegnimento.</span><span class="sxs-lookup"><span data-stu-id="a0f90-297">Turns power off.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su</span><span class="sxs-lookup"><span data-stu-id="a0f90-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-299">Attiva l'accensione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-299">Turns power on.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>\_ \_ \_ durata preregistrazione set VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>MCI\_VCR\_SET\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-301">Il membro **dwPrerollDuration** della struttura identificata da *lpSet* contiene la lunghezza del nastro, nel formato dell'ora corrente, necessaria per stabilizzare l'output del VCR.</span><span class="sxs-lookup"><span data-stu-id="a0f90-301">The **dwPrerollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>\_ \_ \_ formato record set VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI\_VCR\_SET\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-303">Il membro **dwRecordFormat** della struttura identificata da *lpSet* contiene una costante che descrive la velocità del record, che deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-303">The **dwRecordFormat** member of the structure identified by *lpSet* contains a constant describing the record speed, which must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>\_EP del \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI\_VCR\_FORMAT\_EP</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-305">Record a velocità ridotta.</span><span class="sxs-lookup"><span data-stu-id="a0f90-305">Records at slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>\_ \_ LP formato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI\_VCR\_FORMAT\_LP</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-307">Registra la velocità media rallentata.</span><span class="sxs-lookup"><span data-stu-id="a0f90-307">Records at medium-slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>\_ \_ SP formato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI\_VCR\_FORMAT\_SP</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-309">Registra la velocità standard.</span><span class="sxs-lookup"><span data-stu-id="a0f90-309">Records at standard speed.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>\_velocità di \_ set \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI\_VCR\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-311">Il membro **dwSpeed** della struttura identificata da *lpSet* contiene la nuova impostazione della velocità, dove 1000 è la velocità normale, 2000 è la doppia velocità e 500 è la metà della velocità e così via.</span><span class="sxs-lookup"><span data-stu-id="a0f90-311">The **dwSpeed** member of the structure identified by *lpSet* contains the new speed setting, where 1000 is normal speed, 2000 is double speed, and 500 is half speed, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>\_ \_ \_ Lunghezza nastri set VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI\_VCR\_SET\_TAPE\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-313">Il membro **dwTapeLength** della struttura identificata da *lpSet* contiene la nuova lunghezza del nastro, purché la lunghezza del nastro non sia rilevabile.</span><span class="sxs-lookup"><span data-stu-id="a0f90-313">The **dwTapeLength** member of the structure identified by *lpSet* contains the new length of the tape, provided that the length of the tape is undetectable.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>\_ \_ modalità ora di impostazione del VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI\_VCR\_SET\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-315">Il membro **dwTimeMode** della struttura identificata da *lpSet* contiene una costante che indica la nuova modalità di tempo posizionale.</span><span class="sxs-lookup"><span data-stu-id="a0f90-315">The **dwTimeMode** member of the structure identified by *lpSet* contains a constant indicating the new positional time mode.</span></span> <span data-ttu-id="a0f90-316">Sono valide le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-316">The following constants are valid:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_ \_ contatore tempo VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-318">Impone al dispositivo di usare esclusivamente il contatore.</span><span class="sxs-lookup"><span data-stu-id="a0f90-318">Forces the device to use counter exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>\_ \_ rilevamento ora VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI\_VCR\_TIME\_DETECT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-320">Ogni volta che un nuovo nastro viene inserito nel dispositivo o la modalità passa da non pronto a pronto, il dispositivo deve tentare di determinare se è disponibile un timecode sul nastro.</span><span class="sxs-lookup"><span data-stu-id="a0f90-320">Each time a new videotape is inserted into the device, or the mode changes from not ready to ready, the device should attempt to determine if there is timecode available on the videotape.</span></span> <span data-ttu-id="a0f90-321">Se il codice timecode è disponibile, usare il codice temporale in tutti i comandi successivi che specificano le posizioni.</span><span class="sxs-lookup"><span data-stu-id="a0f90-321">If timecode is available, use timecode in all subsequent commands that specify positions.</span></span> <span data-ttu-id="a0f90-322">In caso contrario, utilizzare il contatore.</span><span class="sxs-lookup"><span data-stu-id="a0f90-322">Otherwise, use the counter.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_ \_ timecode ora VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-324">Impone al dispositivo di usare esclusivamente il timecode.</span><span class="sxs-lookup"><span data-stu-id="a0f90-324">Forces the device to use timecode exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>\_ \_ Rilevamento set VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>MCI\_VCR\_SET\_TRACKING</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-326">Ottimizza la velocità del trasporto del nastro VCR con una rettifica corretta e deve essere utilizzata con uno dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-326">Tunes the speed of the VCR tape transport with a fine adjustment, and must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>\_VCR MCI \_ Plus</span><span class="sxs-lookup"><span data-stu-id="a0f90-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI\_VCR\_PLUS</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-328">Aumenta la velocità di trasporto del nastro.</span><span class="sxs-lookup"><span data-stu-id="a0f90-328">Increases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>\_VCR MCI \_ meno</span><span class="sxs-lookup"><span data-stu-id="a0f90-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI\_VCR\_MINUS</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-330">Diminuisce la velocità del trasporto del nastro.</span><span class="sxs-lookup"><span data-stu-id="a0f90-330">Decreases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>\_reimpostazione VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI\_VCR\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-332">Restituisce zero per la regolazione del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="a0f90-332">Returns the tracking adjustment to zero.</span></span>

</dd> </dl>

<span data-ttu-id="a0f90-333">Per i dispositivi VCR, il parametro *lpSet* punta a una struttura [**\_ \_ \_ parametri del VCR MCI**](mci-vcr-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f90-333">For VCR devices, the *lpSet* parameter points to an [**MCI\_VCR\_SET\_PARMS**](mci-vcr-set-parms.md) structure.</span></span>

<span data-ttu-id="a0f90-334">Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **videodisco** :</span><span class="sxs-lookup"><span data-stu-id="a0f90-334">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a0f90-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>\_traccia del \_ formato MCI VD \_</span><span class="sxs-lookup"><span data-stu-id="a0f90-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI\_VD\_FORMAT\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-336">Modifica il formato dell'ora in tracce.</span><span class="sxs-lookup"><span data-stu-id="a0f90-336">Changes the time format to tracks.</span></span> <span data-ttu-id="a0f90-337">MCI usa i numeri di traccia continui.</span><span class="sxs-lookup"><span data-stu-id="a0f90-337">MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="a0f90-338">Con il tipo di dispositivo **WaveAudio** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f90-338">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a0f90-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_input wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-340">Imposta l'input utilizzato per la registrazione nel membro **wInput** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-340">Sets the input used for recording to the **wInput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_Output Wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-342">Imposta l'output utilizzato per la riproduzione nel membro **wOutput** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-342">Sets the output used for playing to the **wOutput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>\_set di Wave MCI \_ \_ ANYINPUT</span><span class="sxs-lookup"><span data-stu-id="a0f90-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI\_WAVE\_SET\_ANYINPUT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-344">Qualsiasi input wave compatibile con il formato corrente può essere usato per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-344">Any wave input compatible with the current format can be used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>\_set di Wave MCI \_ \_ ANYOUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0f90-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI\_WAVE\_SET\_ANYOUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-346">Qualsiasi output wave compatibile con il formato corrente può essere usato per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-346">Any wave output compatible with the current format can be used for playing.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>\_set di Wave MCI \_ \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="a0f90-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-348">Imposta i byte al secondo usati per la riproduzione, la registrazione e il salvataggio nel membro **nAvgBytesPerSec** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-348">Sets the bytes per second used for playing, recording, and saving to the **nAvgBytesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>\_set di Wave MCI \_ \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="a0f90-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-350">Imposta i bit per esempio usati per la riproduzione, la registrazione e il salvataggio nel membro **nBitsPerSample** del formato di dati PCM identificato da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-350">Sets the bits per sample used for playing, recording, and saving to the **nBitsPerSample** member of the PCM data format identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>\_set di Wave MCI \_ \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="a0f90-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-352">Imposta l'allineamento del blocco utilizzato per la riproduzione, la registrazione e il salvataggio nel membro **nBlockAlign** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-352">Sets the block alignment used for playing, recording, and saving to the **nBlockAlign** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>\_ \_ canali set Wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>MCI\_WAVE\_SET\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-354">Il numero di canali è indicato nel membro **nChannels** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-354">The number of channels is indicated in the **nChannels** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>\_set di Wave MCI \_ \_ FORMATTAG</span><span class="sxs-lookup"><span data-stu-id="a0f90-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI\_WAVE\_SET\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-356">Imposta il tipo di formato utilizzato per la riproduzione, la registrazione e il salvataggio nel membro **wFormatTag** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-356">Sets the format type used for playing, recording, and saving to the **wFormatTag** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="a0f90-357">Specificando \_ \_ il PCM in formato Wave, il formato viene modificato in PCM.</span><span class="sxs-lookup"><span data-stu-id="a0f90-357">Specifying WAVE\_FORMAT\_PCM changes the format to PCM.</span></span>

</dd> <dt>

<span data-ttu-id="a0f90-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>\_set di Wave MCI \_ \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="a0f90-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="a0f90-359">Imposta gli esempi al secondo usati per la riproduzione, la registrazione e il salvataggio nel membro **nSamplesPerSec** della struttura identificata da *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="a0f90-359">Sets the samples per second used for playing, recording, and saving to the **nSamplesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> </dl>

<span data-ttu-id="a0f90-360">Per i dispositivi Waveform-Audio, il parametro *lpSet* punta a una struttura [**parametri del \_ \_ set \_ di Wave MCI**](mci-wave-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f90-360">For waveform-audio devices, the *lpSet* parameter points to an [**MCI\_WAVE\_SET\_PARMS**](mci-wave-set-parms.md) structure.</span></span>

<span data-ttu-id="a0f90-361">Quando viene creato il file in cui archiviare i dati, vengono definite diverse proprietà dei dati audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="a0f90-361">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="a0f90-362">Queste proprietà descrivono la struttura dei dati all'interno del file e non possono essere modificate una volta avviata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="a0f90-362">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="a0f90-363">Il seguente elenco di flag identifica queste proprietà:</span><span class="sxs-lookup"><span data-stu-id="a0f90-363">The following list of flags identifies these properties:</span></span>

-   <span data-ttu-id="a0f90-364">\_set di Wave MCI \_ \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="a0f90-364">MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
-   <span data-ttu-id="a0f90-365">\_set di Wave MCI \_ \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="a0f90-365">MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
-   <span data-ttu-id="a0f90-366">\_set di Wave MCI \_ \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="a0f90-366">MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
-   <span data-ttu-id="a0f90-367">\_ \_ canali set Wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-367">MCI\_WAVE\_SET\_CHANNELS</span></span>
-   <span data-ttu-id="a0f90-368">\_set di Wave MCI \_ \_ FORMATTAG</span><span class="sxs-lookup"><span data-stu-id="a0f90-368">MCI\_WAVE\_SET\_FORMATTAG</span></span>
-   <span data-ttu-id="a0f90-369">\_set di Wave MCI \_ \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="a0f90-369">MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f90-370">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0f90-370">Requirements</span></span>



| <span data-ttu-id="a0f90-371">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f90-371">Requirement</span></span> | <span data-ttu-id="a0f90-372">Valore</span><span class="sxs-lookup"><span data-stu-id="a0f90-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f90-373">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0f90-373">Minimum supported client</span></span><br/> | <span data-ttu-id="a0f90-374">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0f90-374">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a0f90-375">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0f90-375">Minimum supported server</span></span><br/> | <span data-ttu-id="a0f90-376">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0f90-376">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a0f90-377">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0f90-377">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0f90-378"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0f90-378"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0f90-379">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0f90-379">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f90-380">MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-380">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a0f90-381">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="a0f90-381">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

