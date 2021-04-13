---
title: Comando MCI_STATUS (mmsystem. h)
description: Il \_ comando MCI status recupera le informazioni su un dispositivo MCI. Tutti i dispositivi riconoscono questo comando. Le informazioni vengono restituite nel membro dwReturn della struttura identificata dal parametro lpStatus.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- Comando MCI_STATUS Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "104350691"
---
# <a name="mci_status-command"></a><span data-ttu-id="a029d-106">\_Comando stato MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-106">MCI\_STATUS command</span></span>

> [!NOTE]
> <span data-ttu-id="a029d-107">Comunicazione senza distorsione Microsoft supporta un ambiente diversificato e di inclusione.</span><span class="sxs-lookup"><span data-stu-id="a029d-107">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="a029d-108">All'interno di questo documento sono presenti riferimenti alla parola "slave".</span><span class="sxs-lookup"><span data-stu-id="a029d-108">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="a029d-109">La [Guida di stile di Microsoft per le comunicazioni di Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) riconosce questo aspetto come una parola di esclusione.</span><span class="sxs-lookup"><span data-stu-id="a029d-109">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="a029d-110">Questo testo viene usato in quanto è attualmente il testo usato nei comandi.</span><span class="sxs-lookup"><span data-stu-id="a029d-110">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="a029d-111">Per coerenza, questo documento contiene questa parola.</span><span class="sxs-lookup"><span data-stu-id="a029d-111">For consistency, this document contains this word.</span></span> <span data-ttu-id="a029d-112">Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo da essere in allineamento.</span><span class="sxs-lookup"><span data-stu-id="a029d-112">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="a029d-113">Il \_ comando MCI status recupera le informazioni su un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="a029d-113">The MCI\_STATUS command retrieves information about an MCI device.</span></span> <span data-ttu-id="a029d-114">Tutti i dispositivi riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="a029d-114">All devices recognize this command.</span></span> <span data-ttu-id="a029d-115">Le informazioni vengono restituite nel membro **dwReturn** della struttura identificata dal parametro *lpStatus* .</span><span class="sxs-lookup"><span data-stu-id="a029d-115">Information is returned in the **dwReturn** member of the structure identified by the *lpStatus* parameter.</span></span>

<span data-ttu-id="a029d-116">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a029d-116">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a029d-117">Parametri</span><span class="sxs-lookup"><span data-stu-id="a029d-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a029d-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a029d-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a029d-119">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="a029d-119">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a029d-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a029d-121">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a029d-121">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="a029d-122">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a029d-122">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a029d-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span><span class="sxs-lookup"><span data-stu-id="a029d-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span></span>
</dt> <dd>

<span data-ttu-id="a029d-124">Puntatore a una [**struttura \_ \_ parametri di stato MCI**](mci-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a029d-124">Pointer to an [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure.</span></span> <span data-ttu-id="a029d-125">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a029d-125">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a029d-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a029d-126">Return Value</span></span>

<span data-ttu-id="a029d-127">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="a029d-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a029d-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="a029d-128">Remarks</span></span>

<span data-ttu-id="a029d-129">Per tutti i dispositivi che supportano lo stato MCI sono validi i flag aggiuntivi e specifici dei comandi seguenti \_ :</span><span class="sxs-lookup"><span data-stu-id="a029d-129">The following additional standard and command-specific flags apply to all devices supporting MCI\_STATUS:</span></span>

<dl> <dt>

<span data-ttu-id="a029d-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>\_elemento stato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>MCI\_STATUS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="a029d-131">Specifica che il membro **dwItem** della struttura identificata da *lpStatus* contiene una costante che specifica l'elemento di stato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a029d-131">Specifies that the **dwItem** member of the structure identified by *lpStatus* contains a constant specifying which status item to obtain.</span></span> <span data-ttu-id="a029d-132">Le costanti seguenti definiscono quale elemento di stato restituire nel membro **dwReturn** della struttura:</span><span class="sxs-lookup"><span data-stu-id="a029d-132">The following constants define which status item to return in the **dwReturn** member of the structure:</span></span>

<span data-ttu-id="a029d-133">\_ \_ traccia corrente stato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-133">MCI\_STATUS\_CURRENT\_TRACK</span></span>

<span data-ttu-id="a029d-134">Il membro **dwReturn** è impostato sul numero di traccia corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-134">The **dwReturn** member is set to the current track number.</span></span> <span data-ttu-id="a029d-135">MCI usa i numeri di traccia continui.</span><span class="sxs-lookup"><span data-stu-id="a029d-135">MCI uses continuous track numbers.</span></span>

<span data-ttu-id="a029d-136">\_lunghezza stato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-136">MCI\_STATUS\_LENGTH</span></span>

<span data-ttu-id="a029d-137">Il membro **dwReturn** è impostato sulla lunghezza totale del supporto.</span><span class="sxs-lookup"><span data-stu-id="a029d-137">The **dwReturn** member is set to the total media length.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modalità stato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-139">Il membro **dwReturn** è impostato sulla modalità corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a029d-139">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="a029d-140">Le modalità includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a029d-140">The modes include the following:</span></span>

-   <span data-ttu-id="a029d-141">\_modalità MCI \_ non \_ pronta</span><span class="sxs-lookup"><span data-stu-id="a029d-141">MCI\_MODE\_NOT\_READY</span></span>
-   <span data-ttu-id="a029d-142">\_sospensione della modalità MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-142">MCI\_MODE\_PAUSE</span></span>
-   <span data-ttu-id="a029d-143">\_riproduzione in modalità MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-143">MCI\_MODE\_PLAY</span></span>
-   <span data-ttu-id="a029d-144">\_arresto modalità \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-144">MCI\_MODE\_STOP</span></span>
-   <span data-ttu-id="a029d-145">\_modalità MCI \_ aperta</span><span class="sxs-lookup"><span data-stu-id="a029d-145">MCI\_MODE\_OPEN</span></span>
-   <span data-ttu-id="a029d-146">\_record in modalità MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-146">MCI\_MODE\_RECORD</span></span>
-   <span data-ttu-id="a029d-147">\_ricerca in modalità MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-147">MCI\_MODE\_SEEK</span></span>

</dd> <dt>

<span data-ttu-id="a029d-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>\_ \_ numero \_ di tracce di stato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>MCI\_STATUS\_NUMBER\_OF\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="a029d-149">Il membro **dwReturn** è impostato sul numero totale di tracce giocabili.</span><span class="sxs-lookup"><span data-stu-id="a029d-149">The **dwReturn** member is set to the total number of playable tracks.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>\_posizione stato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>MCI\_STATUS\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="a029d-151">Il membro **dwReturn** è impostato sulla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-151">The **dwReturn** member is set to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>\_stato MCI \_ pronto</span><span class="sxs-lookup"><span data-stu-id="a029d-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>MCI\_STATUS\_READY</span></span>
</dt> <dd>

<span data-ttu-id="a029d-153">Il membro **dwReturn** è impostato su **true** se il dispositivo è pronto; in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-153">The **dwReturn** member is set to **TRUE** if the device is ready; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>\_ \_ formato ora stato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>MCI\_STATUS\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-155">Il membro **dwReturn** è impostato sul formato dell'ora corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a029d-155">The **dwReturn** member is set to the current time format of the device.</span></span> <span data-ttu-id="a029d-156">I formati di ora includono:</span><span class="sxs-lookup"><span data-stu-id="a029d-156">The time formats include:</span></span>

-   <span data-ttu-id="a029d-157">\_byte in formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-157">MCI\_FORMAT\_BYTES</span></span>
-   <span data-ttu-id="a029d-158">\_frame di formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-158">MCI\_FORMAT\_FRAMES</span></span>
-   <span data-ttu-id="a029d-159">\_formato MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="a029d-159">MCI\_FORMAT\_HMS</span></span>
-   <span data-ttu-id="a029d-160">\_ \_ millisecondi formato MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-160">MCI\_FORMAT\_MILLISECONDS</span></span>
-   <span data-ttu-id="a029d-161">\_MSF formato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-161">MCI\_FORMAT\_MSF</span></span>
-   <span data-ttu-id="a029d-162">\_esempi di formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-162">MCI\_FORMAT\_SAMPLES</span></span>
-   <span data-ttu-id="a029d-163">\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="a029d-163">MCI\_FORMAT\_TMSF</span></span>

</dd> <dt>

<span data-ttu-id="a029d-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>\_inizio stato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI\_STATUS\_START</span></span>
</dt> <dd>

<span data-ttu-id="a029d-165">Ottiene la posizione iniziale del supporto.</span><span class="sxs-lookup"><span data-stu-id="a029d-165">Obtains the starting position of the media.</span></span> <span data-ttu-id="a029d-166">Per ottenere la posizione iniziale, combinare questo flag con l' \_ elemento di stato MCI \_ e impostare il membro **dwItem** della struttura identificata da *LPSTATUS* sulla \_ posizione di stato MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a029d-166">To get the starting position, combine this flag with MCI\_STATUS\_ITEM and set the **dwItem** member of the structure identified by *lpStatus* to MCI\_STATUS\_POSITION.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>\_traccia MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="a029d-168">Indica che il parametro Track status è incluso nel membro **dwTrack** della struttura identificata da *lpStatus*.</span><span class="sxs-lookup"><span data-stu-id="a029d-168">Indicates a status track parameter is included in the **dwTrack** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="a029d-169">È necessario usare questo flag con la \_ posizione di stato MCI o le costanti di \_ \_ lunghezza dello stato MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a029d-169">You must use this flag with the MCI\_STATUS\_POSITION or MCI\_STATUS\_LENGTH constants.</span></span> <span data-ttu-id="a029d-170">Se usata con la \_ \_ posizione di stato MCI, MCI \_ Track ottiene la posizione iniziale della traccia specificata. Se utilizzata con la \_ lunghezza dello stato MCI \_ , \_ la traccia MCI ottiene la lunghezza della traccia specificata. MCI usa i numeri di traccia continui.</span><span class="sxs-lookup"><span data-stu-id="a029d-170">When used with MCI\_STATUS\_POSITION, MCI\_TRACK obtains the starting position of the specified track. When used with MCI\_STATUS\_LENGTH, MCI\_TRACK obtains the length of the specified track. MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="a029d-171">I flag aggiuntivi seguenti vengono utilizzati con il tipo di dispositivo **CDAudio** .</span><span class="sxs-lookup"><span data-stu-id="a029d-171">The following additional flags are used with the **cdaudio** device type.</span></span> <span data-ttu-id="a029d-172">Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a029d-172">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="a029d-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>\_ \_ \_ traccia tipo stato CdA \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI\_CDA\_STATUS\_TYPE\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="a029d-174">Il membro **dwReturn** è impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a029d-174">The **dwReturn** member is set to one of the following values:</span></span>

-   <span data-ttu-id="a029d-175">\_ \_ traccia \_ audio di MCI CdA</span><span class="sxs-lookup"><span data-stu-id="a029d-175">MCI\_CDA\_TRACK\_AUDIO</span></span>
-   <span data-ttu-id="a029d-176">\_ \_ traccia \_ altro per MCI CdA</span><span class="sxs-lookup"><span data-stu-id="a029d-176">MCI\_CDA\_TRACK\_OTHER</span></span>

<span data-ttu-id="a029d-177">Per usare questo flag, \_ è necessario impostare il flag di traccia MCI e il membro **dwTrack** della struttura identificata da *lpStatus* deve contenere un numero di traccia valido.</span><span class="sxs-lookup"><span data-stu-id="a029d-177">To use this flag, the MCI\_TRACK flag must be set, and the **dwTrack** member of the structure identified by *lpStatus* must contain a valid track number.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="a029d-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-179">Il membro **dwReturn** è impostato su **true** se il supporto viene inserito nel dispositivo. in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-179">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="a029d-180">Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a029d-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a029d-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>\_ \_ diskspace stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI\_DGV\_STATUS\_DISKSPACE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-182">Il membro **lpstrDrive** della struttura identificata da *lpStatus* specifica un'unità disco o, in alcune implementazioni, un percorso.</span><span class="sxs-lookup"><span data-stu-id="a029d-182">The **lpstrDrive** member of the structure identified by *lpStatus* specifies a disk drive or, in some implementations, a path.</span></span> <span data-ttu-id="a029d-183">Il \_ comando MCI Status restituisce la quantità approssimativa di spazio su disco che può essere ottenuta dal comando [MCI \_ Reserve](mci-reserve.md) nel membro **dwReturn** della struttura identificata da *lpStatus*.</span><span class="sxs-lookup"><span data-stu-id="a029d-183">The MCI\_STATUS command returns the approximate amount of disk space that could be obtained by the [MCI\_RESERVE](mci-reserve.md) command in the **dwReturn** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="a029d-184">Lo spazio su disco viene misurato in unità del formato ora corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-184">The disk space is measured in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>\_ \_ input stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>MCI\_DGV\_STATUS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-186">La costante specificata dal membro **dwItem** della struttura identificata da *lpStatus* si applica all'input.</span><span class="sxs-lookup"><span data-stu-id="a029d-186">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the input.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>\_stato DGV MCI a \_ \_ sinistra</span><span class="sxs-lookup"><span data-stu-id="a029d-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>MCI\_DGV\_STATUS\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-188">La costante specificata dal membro **dwItem** della struttura identificata da *lpStatus* si applica al canale audio sinistro.</span><span class="sxs-lookup"><span data-stu-id="a029d-188">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>\_stato DGV \_ MCI \_ nominale</span><span class="sxs-lookup"><span data-stu-id="a029d-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI\_DGV\_STATUS\_NOMINAL</span></span>
</dt> <dd>

<span data-ttu-id="a029d-190">La costante specificata dal membro **dwItem** della struttura identificata da *lpStatus* richiede il valore nominale anziché il valore corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-190">The constant specified by the **dwItem** member of the structure identified by *lpStatus* requests the nominal value rather than the current value.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>\_ \_ output stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>MCI\_DGV\_STATUS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-192">La costante specificata dal membro **dwItem** della struttura identificata da *lpStatus* si applica all'output.</span><span class="sxs-lookup"><span data-stu-id="a029d-192">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the output.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>\_record di \_ stato \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI\_DGV\_STATUS\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="a029d-194">La frequenza dei fotogrammi restituiti per il \_ flag di frequenza dei fotogrammi di stato DGV di MCI \_ \_ \_ è la velocità utilizzata per la compressione.</span><span class="sxs-lookup"><span data-stu-id="a029d-194">The frame rate returned for the MCI\_DGV\_STATUS\_FRAME\_RATE flag is the rate used for compression.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>informazioni \_ di \_ riferimento sullo stato di DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>MCI\_DGV\_STATUS\_REFERENCE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-196">Il membro **dwReturn** della struttura identificata da *lpStatus* restituisce l'immagine del fotogramma chiave più vicina che precede il frame specificato nel membro **dwReference** .</span><span class="sxs-lookup"><span data-stu-id="a029d-196">The **dwReturn** member of the structure identified by *lpStatus* returns the nearest key-frame image that precedes the frame specified in the **dwReference** member.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>\_stato DGV MCI- \_ \_ diritto</span><span class="sxs-lookup"><span data-stu-id="a029d-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI\_DGV\_STATUS\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-198">La costante specificata dal membro **dwItem** della struttura identificata da *lpStatus* si applica al canale audio corretto.</span><span class="sxs-lookup"><span data-stu-id="a029d-198">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the right audio channel.</span></span>

</dd> </dl>

<span data-ttu-id="a029d-199">Le costanti seguenti vengono usate con il tipo di dispositivo **digitalvideo** nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a029d-199">The following constants are used with the **digitalvideo** device type in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="a029d-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>\_ \_ \_ interruzioni audio dello stato di MCI AVI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>MCI\_AVI\_STATUS\_AUDIO\_BREAKS</span></span>
</dt> <dd>

<span data-ttu-id="a029d-201">Il membro **dwReturn** restituisce il numero di volte in cui la parte audio dell'ultima sequenza AVI è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="a029d-201">The **dwReturn** member returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="a029d-202">Il sistema conta un'interruzioni audio ogni volta che tenta di scrivere i dati audio nel driver di dispositivo e rileva che il driver ha già eseguito tutti i dati disponibili.</span><span class="sxs-lookup"><span data-stu-id="a029d-202">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="a029d-203">Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="a029d-203">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>frame di stato di MCI \_ AVI \_ \_ \_ ignorati</span><span class="sxs-lookup"><span data-stu-id="a029d-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>MCI\_AVI\_STATUS\_FRAMES\_SKIPPED</span></span>
</dt> <dd>

<span data-ttu-id="a029d-205">Il membro **dwReturn** restituisce il numero di frame che non sono stati disegnati quando è stata riprodotta l'ultima sequenza AVI.</span><span class="sxs-lookup"><span data-stu-id="a029d-205">The **dwReturn** member returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="a029d-206">Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="a029d-206">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>Data \_ \_ \_ ultima esecuzione stato \_ \_ di MCI AVI</span><span class="sxs-lookup"><span data-stu-id="a029d-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI\_AVI\_STATUS\_LAST\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="a029d-208">Il membro **dwReturn** restituisce un valore che rappresenta la precisione del tempo di riproduzione effettivo dell'ultima sequenza AVI corrispondente al tempo di riproduzione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a029d-208">The **dwReturn** member returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="a029d-209">Il valore 1000 indica che l'ora di destinazione e l'ora effettiva sono uguali.</span><span class="sxs-lookup"><span data-stu-id="a029d-209">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="a029d-210">Il valore 2000, ad esempio, indicherebbe che la sequenza AVI ha richiesto due volte la riproduzione del tempo necessario.</span><span class="sxs-lookup"><span data-stu-id="a029d-210">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="a029d-211">Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="a029d-211">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>\_ \_ audio stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI\_DGV\_STATUS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="a029d-213">Il membro **dwReturn** restituisce MCI \_ on o MCI \_ disattivato a seconda dell'opzione più recente del \_ set \_ di impostazioni audio MCI per il comando [ \_ set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="a029d-213">The **dwReturn** member returns MCI\_ON or MCI\_OFF depending on the most recent MCI\_SET\_AUDIO option for the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="a029d-214">Restituisce MCI \_ in se uno o entrambi gli altoparlanti sono abilitati e MCI è \_ disattivato in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a029d-214">It returns MCI\_ON if either or both speakers are enabled, and MCI\_OFF otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>\_ \_ \_ input audio stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI\_DGV\_STATUS\_AUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-216">Il membro **dwReturn** restituisce il livello di audio istantaneo approssimativo del segnale audio analogico.</span><span class="sxs-lookup"><span data-stu-id="a029d-216">The **dwReturn** member returns the approximate instantaneous audio level of the analog audio signal.</span></span> <span data-ttu-id="a029d-217">Un valore maggiore di 1000 implica la distorsione di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="a029d-217">A value greater than 1000 implies there is clipping distortion.</span></span> <span data-ttu-id="a029d-218">Alcuni dispositivi possono determinare questo valore solo durante la registrazione dell'audio.</span><span class="sxs-lookup"><span data-stu-id="a029d-218">Some devices can determine this value only while recording audio.</span></span> <span data-ttu-id="a029d-219">A questo valore di stato non è associato un **\_ set MCI** o un comando [MCI \_ sefonica](mci-setaudio.md) .</span><span class="sxs-lookup"><span data-stu-id="a029d-219">This status value has no associated **MCI\_SET** or [MCI\_SETAUDIO](mci-setaudio.md) command.</span></span> <span data-ttu-id="a029d-220">Questo valore è correlato a, ma normalizzato in modo diverso rispetto a, il livello di stato dell'onda MCI del comando audio Waveform \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a029d-220">This value is related to, but normalized differently from, the waveform-audio command MCI\_WAVE\_STATUS\_LEVEL.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>\_ \_ \_ record audio stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI\_DGV\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="a029d-222">Il membro **dwReturn** restituisce MCI \_ on o MCI \_ off che riflette lo stato impostato dal \_ \_ \_ flag di record DGV di MCI del comando **MCI \_ sefonica** .</span><span class="sxs-lookup"><span data-stu-id="a029d-222">The **dwReturn** member returns MCI\_ON or MCI\_OFF reflecting the state set by the MCI\_DGV\_SETAUDIO\_RECORD flag of the **MCI\_SETAUDIO** command.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>\_ \_ \_ origine audio stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI\_DGV\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-224">Il membro **dwReturn** restituisce l'origine del digitalizzatore audio corrente:</span><span class="sxs-lookup"><span data-stu-id="a029d-224">The **dwReturn** member returns the current audio digitizer source:</span></span>

</dd> <dt>

<span data-ttu-id="a029d-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>\_media DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI\_DGV\_SETAUDIO\_AVERAGE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-226">Specifica la media dei canali audio sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="a029d-226">Specifies the average of the left and right audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_DGV MCI \_ \_ Left</span><span class="sxs-lookup"><span data-stu-id="a029d-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-228">Specifica il canale audio sinistro.</span><span class="sxs-lookup"><span data-stu-id="a029d-228">Specifies the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>DGV MCI a \_ \_ \_ destra</span><span class="sxs-lookup"><span data-stu-id="a029d-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-230">Specifica il canale audio corretto.</span><span class="sxs-lookup"><span data-stu-id="a029d-230">Specifies the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ sefonica \_ stereo</span><span class="sxs-lookup"><span data-stu-id="a029d-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI\_DGV\_SETAUDIO\_STEREO</span></span>
</dt> <dd>

<span data-ttu-id="a029d-232">Specifica lo stereo.</span><span class="sxs-lookup"><span data-stu-id="a029d-232">Specifies stereo.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>\_ \_ \_ flusso audio stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI\_DGV\_STATUS\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="a029d-234">Il membro **dwReturn** restituisce il numero di flusso audio corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-234">The **dwReturn** member returns the current audio-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>\_ \_ AVGBYTESPERSEC stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI\_DGV\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="a029d-236">Il membro **dwReturn** restituisce il numero medio di byte al secondo usati per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="a029d-236">The **dwReturn** member returns the average number of bytes per second used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>\_ \_ basso stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI\_DGV\_STATUS\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="a029d-238">Il membro **dwReturn** restituisce il livello di basso audio corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-238">The **dwReturn** member returns the current audio bass level.</span></span> <span data-ttu-id="a029d-239">Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.</span><span class="sxs-lookup"><span data-stu-id="a029d-239">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>\_ \_ BITSPERPEL stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI\_DGV\_STATUS\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="a029d-241">Il membro **dwReturn** restituisce il numero di bit per pixel usato per salvare i dati acquisiti o registrati.</span><span class="sxs-lookup"><span data-stu-id="a029d-241">The **dwReturn** member returns the number of bits per pixel used for saving captured or recorded data.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>\_ \_ BitsPerSample stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI\_DGV\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-243">Il membro **dwReturn** restituisce il numero di bit per campione usato dal dispositivo per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="a029d-243">The **dwReturn** member returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="a029d-244">Questo vale solo per i dispositivi che supportano il formato PCM.</span><span class="sxs-lookup"><span data-stu-id="a029d-244">This applies only to devices supporting the PCM format.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>\_ \_ BLOCKALIGN stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI\_DGV\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="a029d-246">Il membro **dwReturn** restituisce l'allineamento dei blocchi di dati rispetto all'inizio della forma d'onda di input.</span><span class="sxs-lookup"><span data-stu-id="a029d-246">The **dwReturn** member returns the alignment of data blocks relative to the start of the input waveform.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>\_ \_ luminosità stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>MCI\_DGV\_STATUS\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="a029d-248">Il membro **dwReturn** restituisce il livello di luminosità del video corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-248">The **dwReturn** member returns the current video brightness level.</span></span> <span data-ttu-id="a029d-249">Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.</span><span class="sxs-lookup"><span data-stu-id="a029d-249">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>\_ \_ colore stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI\_DGV\_STATUS\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="a029d-251">Il membro **dwReturn** restituisce il livello di colore corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-251">The **dwReturn** member returns the current color level.</span></span> <span data-ttu-id="a029d-252">Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.</span><span class="sxs-lookup"><span data-stu-id="a029d-252">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>\_ \_ contrasto stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI\_DGV\_STATUS\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="a029d-254">Il membro **dwReturn** restituisce il livello di contrasto corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-254">The **dwReturn** member returns the current contrast level.</span></span> <span data-ttu-id="a029d-255">Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.</span><span class="sxs-lookup"><span data-stu-id="a029d-255">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>\_formato fileDGV di \_ stato MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI\_DGV\_STATUS\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-257">Il membro **dwReturn** restituisce il formato di file corrente per la registrazione o il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="a029d-257">The **dwReturn** member returns the current file format for recording or saving.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>\_ \_ modalità file di stato DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI\_DGV\_STATUS\_FILE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-259">Il membro **dwReturn** restituisce lo stato dell'operazione file:</span><span class="sxs-lookup"><span data-stu-id="a029d-259">The **dwReturn** member returns the state of the file operation:</span></span>

<span data-ttu-id="a029d-260">\_modifica in \_ \_ modalità file DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-260">MCI\_DGV\_FILE\_MODE\_EDITING</span></span>

<span data-ttu-id="a029d-261">Restituito durante le operazioni Taglia, copia, Elimina, Incolla e Annulla.</span><span class="sxs-lookup"><span data-stu-id="a029d-261">Returned during cut, copy, delete, paste, and undo operations.</span></span>

<span data-ttu-id="a029d-262">\_inattività \_ in \_ modalità file DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-262">MCI\_DGV\_FILE\_MODE\_IDLE</span></span>

<span data-ttu-id="a029d-263">Restituito quando il file è pronto per l'operazione successiva.</span><span class="sxs-lookup"><span data-stu-id="a029d-263">Returned when the file is ready for the next operation.</span></span>

<span data-ttu-id="a029d-264">\_caricamento in \_ \_ modalità file DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-264">MCI\_DGV\_FILE\_MODE\_LOADING</span></span>

<span data-ttu-id="a029d-265">Restituito durante il caricamento del file.</span><span class="sxs-lookup"><span data-stu-id="a029d-265">Returned while the file is being loaded.</span></span>

<span data-ttu-id="a029d-266">\_salvataggio in \_ \_ modalità file DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-266">MCI\_DGV\_FILE\_MODE\_SAVING</span></span>

<span data-ttu-id="a029d-267">Restituito durante il salvataggio del file.</span><span class="sxs-lookup"><span data-stu-id="a029d-267">Returned while the file is being saved.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>\_ \_ completamento file di stato DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI\_DGV\_STATUS\_FILE\_COMPLETION</span></span>
</dt> <dd>

<span data-ttu-id="a029d-269">Il membro **dwReturn** restituisce la percentuale stimata. l'operazione di caricamento, salvataggio, acquisizione, taglia, copia, eliminazione, incolla o annullamento è stata progredita.</span><span class="sxs-lookup"><span data-stu-id="a029d-269">The **dwReturn** member returns the estimated percentage a load, save, capture, cut, copy, delete, paste, or undo operation has progressed.</span></span> <span data-ttu-id="a029d-270">(Le applicazioni possono usare questa operazione per fornire un indicatore visivo dello stato di avanzamento). Questo flag non è supportato da tutti i dispositivi video digitali.</span><span class="sxs-lookup"><span data-stu-id="a029d-270">(Applications can use this to provide a visual indicator of progress.) This flag is not supported by all digital-video devices.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>\_stato DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI\_DGV\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="a029d-272">Il membro **dwReturn** restituisce **true** se la direzione del dispositivo è diretta o il dispositivo non viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="a029d-272">The **dwReturn** member returns **TRUE** if the device direction is forward or the device is not playing.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>\_ \_ \_ frequenza fotogrammi di stato DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI\_DGV\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-274">Il membro **dwReturn** deve essere usato con il \_ valore \_ nominale dello stato DGV di MCI, il record di \_ \_ stato DGV MCI \_ \_ o entrambi.</span><span class="sxs-lookup"><span data-stu-id="a029d-274">The **dwReturn** member must be used with MCI\_DGV\_STATUS\_NOMINAL, MCI\_DGV\_STATUS\_RECORD, or both.</span></span> <span data-ttu-id="a029d-275">Quando viene usato con \_ \_ il record di stato DGV MCI \_ , viene restituita la frequenza dei fotogrammi corrente usata per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="a029d-275">When used with MCI\_DGV\_STATUS\_RECORD, the current frame rate used for recording is returned.</span></span> <span data-ttu-id="a029d-276">Quando viene usato con \_ il record di stato DGV di MCI \_ \_ e \_ \_ il valore nominale dello stato DGV di MCI \_ , viene restituita la frequenza dei fotogrammi nominale associata al segnale video di input.</span><span class="sxs-lookup"><span data-stu-id="a029d-276">When used with both MCI\_DGV\_STATUS\_RECORD and MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the input video signal is returned.</span></span> <span data-ttu-id="a029d-277">Se usato con \_ lo stato DGV di MCI \_ \_ , viene restituita la frequenza dei fotogrammi nominale associata al file.</span><span class="sxs-lookup"><span data-stu-id="a029d-277">When used with MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the file is returned.</span></span> <span data-ttu-id="a029d-278">In tutti i casi, le unità sono in frame al secondo moltiplicate per 1000.</span><span class="sxs-lookup"><span data-stu-id="a029d-278">In all cases the units are in frames per second multiplied by 1000.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>\_gamma di \_ stato \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI\_DGV\_STATUS\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="a029d-280">Il membro **dwReturn** restituisce il valore gamma corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-280">The **dwReturn** member returns the current gamma value.</span></span> <span data-ttu-id="a029d-281">Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.</span><span class="sxs-lookup"><span data-stu-id="a029d-281">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>\_ \_ HPAL stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI\_DGV\_STATUS\_HPAL</span></span>
</dt> <dd>

<span data-ttu-id="a029d-283">Il membro **dwReturn** restituisce il valore decimale ASCII per l'handle della tavolozza corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-283">The **dwReturn** member returns the ASCII decimal value for the current palette handle.</span></span> <span data-ttu-id="a029d-284">L'handle è contenuto nella parola di ordine inferiore del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a029d-284">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>\_ \_ HWND stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI\_DGV\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="a029d-286">Il membro **dwReturn** restituisce il valore decimale ASCII per l'handle di finestra esplicito o predefinito corrente associato a questa istanza del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a029d-286">The **dwReturn** member returns the ASCII decimal value for the current explicit or default window handle associated with this device driver instance.</span></span> <span data-ttu-id="a029d-287">L'handle è contenuto nella parola di ordine inferiore del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a029d-287">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>\_ \_ \_ colore chiave stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI\_DGV\_STATUS\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="a029d-289">Il membro **dwReturn** restituisce il valore corrente del colore della chiave.</span><span class="sxs-lookup"><span data-stu-id="a029d-289">The **dwReturn** member returns the current key-color value.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>\_ \_ \_ indice chiave stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI\_DGV\_STATUS\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="a029d-291">Il membro **dwReturn** restituisce il valore di indice della chiave corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-291">The **dwReturn** member returns the current key-index value.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>\_ \_ monitoraggio stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MCI\_DGV\_STATUS\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="a029d-293">Il membro **dwReturn** restituisce una costante che indica l'origine della presentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-293">The **dwReturn** member returns a constant indicating the source of the current presentation.</span></span> <span data-ttu-id="a029d-294">Sono definite le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a029d-294">The following constants are defined:</span></span>

<span data-ttu-id="a029d-295">\_file di \_ monitoraggio \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-295">MCI\_DGV\_MONITOR\_FILE</span></span>

<span data-ttu-id="a029d-296">Un file è l'origine.</span><span class="sxs-lookup"><span data-stu-id="a029d-296">A file is the source.</span></span>

<span data-ttu-id="a029d-297">\_ \_ input monitoraggio DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-297">MCI\_DGV\_MONITOR\_INPUT</span></span>

<span data-ttu-id="a029d-298">L'input è l'origine.</span><span class="sxs-lookup"><span data-stu-id="a029d-298">The input is the source.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>\_metodo di \_ \_ monitoraggio stato DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI\_DGV\_STATUS\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="a029d-300">Il membro **dwReturn** restituisce una costante che indica il metodo utilizzato per il monitoraggio dell'input.</span><span class="sxs-lookup"><span data-stu-id="a029d-300">The **dwReturn** member returns a constant indicating the method used for input monitoring.</span></span> <span data-ttu-id="a029d-301">Sono definite le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a029d-301">The following constants are defined:</span></span>

<span data-ttu-id="a029d-302">\_Metodo DGV \_ MCI \_ diretto</span><span class="sxs-lookup"><span data-stu-id="a029d-302">MCI\_DGV\_METHOD\_DIRECT</span></span>

<span data-ttu-id="a029d-303">Monitoraggio diretto degli input.</span><span class="sxs-lookup"><span data-stu-id="a029d-303">Direct input monitoring.</span></span>

<span data-ttu-id="a029d-304">\_post del \_ metodo \_ DGV di MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-304">MCI\_DGV\_METHOD\_POST</span></span>

<span data-ttu-id="a029d-305">Monitoraggio post-input.</span><span class="sxs-lookup"><span data-stu-id="a029d-305">Post-input monitoring.</span></span>

<span data-ttu-id="a029d-306">\_pre- \_ metodo \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-306">MCI\_DGV\_METHOD\_PRE</span></span>

<span data-ttu-id="a029d-307">Monitoraggio pre-input.</span><span class="sxs-lookup"><span data-stu-id="a029d-307">Pre-input monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>\_modalità di \_ \_ sospensione stato DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI\_DGV\_STATUS\_PAUSE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-309">Il membro **dwReturn** restituisce la \_ riproduzione in modalità MCI \_ se il dispositivo è stato sospeso durante la riproduzione e restituisce \_ \_ il record della modalità MCI se il dispositivo è stato sospeso durante la registrazione.</span><span class="sxs-lookup"><span data-stu-id="a029d-309">The **dwReturn** member returns MCI\_MODE\_PLAY if the device was paused while playing and returns MCI\_MODE\_RECORD if the device was paused while recording.</span></span> <span data-ttu-id="a029d-310">Il comando restituisce MCIERR \_ \_ funzione non applicabile come un errore restituito se il dispositivo non è sospeso.</span><span class="sxs-lookup"><span data-stu-id="a029d-310">The command returns MCIERR\_NONAPPLICABLE\_FUNCTION as an error return if the device is not paused.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>\_ \_ SAMPLESPERSECOND stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI\_DGV\_STATUS\_SAMPLESPERSECOND</span></span>
</dt> <dd>

<span data-ttu-id="a029d-312">Il membro **dwReturn** restituisce il numero di campioni al secondo registrati.</span><span class="sxs-lookup"><span data-stu-id="a029d-312">The **dwReturn** member returns the number of samples per second recorded.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>\_ \_ \_ ricerca \_ esatta stato DGV MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI\_DGV\_STATUS\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="a029d-314">Il membro **dwReturn** restituisce **true** o **false** che indica se è impostato o meno il formato Seek esatto.</span><span class="sxs-lookup"><span data-stu-id="a029d-314">The **dwReturn** member returns **TRUE** or **FALSE** indicating whether or not the seek exactly format is set.</span></span> <span data-ttu-id="a029d-315">(Le applicazioni possono impostare questo formato usando il comando [MCI \_ set](mci-set.md) con il \_ flag DGV \_ set \_ Seek \_ exactly del MCI).</span><span class="sxs-lookup"><span data-stu-id="a029d-315">(Applications can set this format by using the [MCI\_SET](mci-set.md) command with the MCI\_DGV\_SET\_SEEK\_EXACTLY flag.)</span></span>

</dd> <dt>

<span data-ttu-id="a029d-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>\_ \_ nitidezza stato DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI\_DGV\_STATUS\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="a029d-317">Il membro **dwReturn** restituisce il livello di nitidezza corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-317">The **dwReturn** member returns the current sharpness level.</span></span> <span data-ttu-id="a029d-318">Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.</span><span class="sxs-lookup"><span data-stu-id="a029d-318">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>\_ \_ dimensioni stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI\_DGV\_STATUS\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-320">Il membro **dwReturn** restituisce la durata approssimativa della riproduzione dei dati compressi che l'area di lavoro riservata conterrà.</span><span class="sxs-lookup"><span data-stu-id="a029d-320">The **dwReturn** member returns the approximate playback duration of compressed data that the reserved workspace will hold.</span></span> <span data-ttu-id="a029d-321">Le unità di durata sono nel formato di ora corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-321">The duration units are in the current time format.</span></span> <span data-ttu-id="a029d-322">Restituisce zero se non è disponibile spazio su disco riservato.</span><span class="sxs-lookup"><span data-stu-id="a029d-322">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="a029d-323">Le dimensioni restituite sono approssimative poiché lo spazio su disco preciso per i dati compressi non può essere stimato, in generale, fino a quando i dati non sono stati compressi.</span><span class="sxs-lookup"><span data-stu-id="a029d-323">The size returned is approximate since the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>\_SMPTE DGV \_ stato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI\_DGV\_STATUS\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-325">Il membro **dwReturn** restituisce il codice ora SMPTE associato alla posizione corrente nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a029d-325">The **dwReturn** member returns the SMPTE time code associated with the current position in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>\_ \_ velocità stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI\_DGV\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="a029d-327">Il membro **dwReturn** restituisce la velocità di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-327">The **dwReturn** member returns the current playback speed.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>\_stato DGV di MCI \_ ancora in \_ \_ formato FileFormat</span><span class="sxs-lookup"><span data-stu-id="a029d-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI\_DGV\_STATUS\_STILL\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-329">Il membro **dwReturn** restituisce il formato di file corrente per il comando di [ \_ acquisizione MCI](mci-capture.md) .</span><span class="sxs-lookup"><span data-stu-id="a029d-329">The **dwReturn** member returns the current file format for the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>\_ \_ tinta stato DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI\_DGV\_STATUS\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-331">Il membro **dwReturn** restituisce il livello di tinta del video corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-331">The **dwReturn** member returns the current video tint level.</span></span> <span data-ttu-id="a029d-332">Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.</span><span class="sxs-lookup"><span data-stu-id="a029d-332">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>\_ \_ Treble stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI\_DGV\_STATUS\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-334">Il membro **dwReturn** restituisce il livello di acuto audio corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-334">The **dwReturn** member returns the current audio treble level.</span></span> <span data-ttu-id="a029d-335">Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.</span><span class="sxs-lookup"><span data-stu-id="a029d-335">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>\_stato DGV MCI non \_ \_ salvato</span><span class="sxs-lookup"><span data-stu-id="a029d-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>MCI\_DGV\_STATUS\_UNSAVED</span></span>
</dt> <dd>

<span data-ttu-id="a029d-337">Il membro **dwReturn** restituisce **true** se nell'area di lavoro sono presenti dati registrati che potrebbero andare perduti a seguito di un comando [MCI \_ Close](mci-close.md), [MCI \_ Load](mci-load.md), [MCI \_ record](mci-record.md), [MCI \_ Reserve](mci-reserve.md), [MCI \_ Cut](mci-cut.md), [MCI \_ Delete](mci-delete.md)o [MCI \_ paste](mci-paste.md) .</span><span class="sxs-lookup"><span data-stu-id="a029d-337">The **dwReturn** member returns **TRUE** if there is recorded data in the workspace that might be lost as a result of a [MCI\_CLOSE](mci-close.md), [MCI\_LOAD](mci-load.md), [MCI\_RECORD](mci-record.md), [MCI\_RESERVE](mci-reserve.md), [MCI\_CUT](mci-cut.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="a029d-338">Il membro restituisce **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a029d-338">The member returns **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>\_video di \_ stato \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>MCI\_DGV\_STATUS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="a029d-340">Il membro **dwReturn** restituisce MCI \_ in se il video è abilitato o MCI \_ disattivato se è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a029d-340">The **dwReturn** member returns MCI\_ON if video is enabled or MCI\_OFF if it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>\_ \_ \_ record video stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>MCI\_DGV\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="a029d-342">Il membro **dwReturn** restituisce MCI \_ on o MCI \_ off, che riflette lo stato impostato dal \_ \_ flag di record MCI DGV sevideo \_ del comando [MCI \_ sevideo](mci-setvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="a029d-342">The **dwReturn** member returns MCI\_ON or MCI\_OFF, reflecting the state set by the MCI\_DGV\_SETVIDEO\_RECORD flag of the [MCI\_SETVIDEO](mci-setvideo.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>\_ \_ \_ origine video stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI\_DGV\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-344">Il membro **dwReturn** restituisce una costante che indica il tipo di origine video impostato dal \_ \_ flag di origine DGV sevideo MCI \_ del comando **MCI \_ sevideo** .</span><span class="sxs-lookup"><span data-stu-id="a029d-344">The **dwReturn** member returns a constant indicating the type of video source set by the MCI\_DGV\_SETVIDEO\_SOURCE flag of the **MCI\_SETVIDEO** command.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>\_video di stato DGV di MCI-numero \_ \_ \_ src \_</span><span class="sxs-lookup"><span data-stu-id="a029d-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI\_DGV\_STATUS\_VIDEO\_SRC\_NUM</span></span>
</dt> <dd>

<span data-ttu-id="a029d-346">Il membro **dwReturn** restituisce il numero all'interno del tipo di origine di input video attualmente attivo.</span><span class="sxs-lookup"><span data-stu-id="a029d-346">The **dwReturn** member returns the number within its type of the video-input source currently active.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>\_ \_ \_ flusso video stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI\_DGV\_STATUS\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="a029d-348">Il membro **dwReturn** restituisce il numero corrente del flusso video.</span><span class="sxs-lookup"><span data-stu-id="a029d-348">The **dwReturn** member returns the current video-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>\_ \_ volume stato DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI\_DGV\_STATUS\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="a029d-350">Il membro **dwReturn** restituisce la media del volume agli altoparlanti sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="a029d-350">The **dwReturn** member returns the average of the volume to the left and right speakers.</span></span> <span data-ttu-id="a029d-351">Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.</span><span class="sxs-lookup"><span data-stu-id="a029d-351">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>\_finestra di \_ stato DGV MCI \_ \_ visibile</span><span class="sxs-lookup"><span data-stu-id="a029d-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>MCI\_DGV\_STATUS\_WINDOW\_VISIBLE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-353">Il membro **dwReturn** restituisce **true** se la finestra non è nascosta.</span><span class="sxs-lookup"><span data-stu-id="a029d-353">The **dwReturn** member returns **TRUE** if the window is not hidden.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>\_finestra di stato DGV di MCI ridotta a \_ \_ \_ icona</span><span class="sxs-lookup"><span data-stu-id="a029d-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>MCI\_DGV\_STATUS\_WINDOW\_MINIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="a029d-355">Il membro **dwReturn** restituisce **true** se la finestra è ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="a029d-355">The **dwReturn** member returns **TRUE** if the window is minimized.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>\_finestra di \_ stato DGV MCI \_ \_ ingrandita</span><span class="sxs-lookup"><span data-stu-id="a029d-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>MCI\_DGV\_STATUS\_WINDOW\_MAXIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="a029d-357">Il membro **dwReturn** restituisce **true** se la finestra è ingrandita.</span><span class="sxs-lookup"><span data-stu-id="a029d-357">The **dwReturn** member returns **TRUE** if the window is maximized.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="a029d-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-359">Il membro **dwReturn** restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="a029d-359">The **dwReturn** member returns **TRUE**.</span></span>

</dd> </dl>

<span data-ttu-id="a029d-360">Per i dispositivi digitali video, il parametro *lpStatus* punta a una [**struttura \_ DGV \_ stato \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="a029d-360">For digital-video devices, the *lpStatus* parameter points to an [**MCI\_DGV\_STATUS\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) structure.</span></span>

<span data-ttu-id="a029d-361">I flag aggiuntivi seguenti vengono utilizzati con il tipo di dispositivo **sequencer** .</span><span class="sxs-lookup"><span data-stu-id="a029d-361">The following additional flags are used with the **sequencer** device type.</span></span> <span data-ttu-id="a029d-362">Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a029d-362">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="a029d-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>\_ \_ DIVTYPE stato MCI \_ Seq</span><span class="sxs-lookup"><span data-stu-id="a029d-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI\_SEQ\_STATUS\_DIVTYPE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-364">Il membro **dwReturn** è impostato su uno dei valori seguenti, che indica il tipo di divisione corrente di una sequenza:</span><span class="sxs-lookup"><span data-stu-id="a029d-364">The **dwReturn** member is set to one of the following values indicating the current division type of a sequence:</span></span>

-   <span data-ttu-id="a029d-365">PPQN per MCI \_ seq \_ div \_</span><span class="sxs-lookup"><span data-stu-id="a029d-365">MCI\_SEQ\_DIV\_PPQN</span></span>
-   <span data-ttu-id="a029d-366">MCI \_ seq \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="a029d-366">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>
-   <span data-ttu-id="a029d-367">MCI \_ seq \_ div \_ \_ 25</span><span class="sxs-lookup"><span data-stu-id="a029d-367">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>
-   <span data-ttu-id="a029d-368">MCI \_ seq \_ div \_ \_ 30</span><span class="sxs-lookup"><span data-stu-id="a029d-368">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>
-   <span data-ttu-id="a029d-369">MCI \_ seq \_ div \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="a029d-369">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span>

</dd> <dt>

<span data-ttu-id="a029d-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>\_ \_ Master stato SEQ per MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI\_SEQ\_STATUS\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="a029d-371">Il membro **dwReturn** è impostato sul tipo di sincronizzazione utilizzato per l'operazione master.</span><span class="sxs-lookup"><span data-stu-id="a029d-371">The **dwReturn** member is set to the synchronization type used for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>\_ \_ offset dello stato Seq di MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>MCI\_SEQ\_STATUS\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="a029d-373">Il membro **dwReturn** è impostato sull'offset SMPTE corrente di una sequenza.</span><span class="sxs-lookup"><span data-stu-id="a029d-373">The **dwReturn** member is set to the current SMPTE offset of a sequence.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>\_porta di \_ stato Seq seq \_</span><span class="sxs-lookup"><span data-stu-id="a029d-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI\_SEQ\_STATUS\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-375">Il membro **dwReturn** è impostato sull'identificatore del dispositivo MIDI per la porta corrente utilizzata dalla sequenza.</span><span class="sxs-lookup"><span data-stu-id="a029d-375">The **dwReturn** member is set to the MIDI device identifier for the current port used by the sequence.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>\_ \_ stato dello slave Seq stato di MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI\_SEQ\_STATUS\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-377">Il membro **dwReturn** è impostato sul tipo di sincronizzazione usato per l'operazione subordinata.</span><span class="sxs-lookup"><span data-stu-id="a029d-377">The **dwReturn** member is set to the synchronization type used for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>TEMPO di stato di MCI \_ seq \_ \_</span><span class="sxs-lookup"><span data-stu-id="a029d-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI\_SEQ\_STATUS\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="a029d-379">Il membro **dwReturn** è impostato sul tempo corrente di una sequenza MIDI in battute al minuto per i file PPQN o frame al secondo per i file SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a029d-379">The **dwReturn** member is set to the current tempo of a MIDI sequence in beats per minute for PPQN files, or frames per second for SMPTE files.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="a029d-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-381">Il membro **dwReturn** è impostato su **true** se il supporto viene inserito nel dispositivo. in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-381">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="a029d-382">Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a029d-382">The following additional flags are used with the **vcr** device type.</span></span> <span data-ttu-id="a029d-383">Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a029d-383">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="a029d-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="a029d-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-385">Il membro **dwReturn** è impostato su **true** se il supporto viene inserito nel dispositivo. in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-385">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>\_record di \_ \_ assemblaggio stato VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI\_VCR\_STATUS\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="a029d-387">Il membro **dwReturn** è impostato su **true** se la modalità di assemblaggio è on; in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-387">The **dwReturn** member is set to **TRUE** if assemble mode is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>\_ \_ \_ monitoraggio audio stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="a029d-389">Il membro **dwReturn** è impostato su una costante che indica il tipo di monitoraggio audio attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a029d-389">The **dwReturn** member is set to a constant, indicating the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>\_numero di \_ \_ monitor audio \_ stato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="a029d-391">Il membro **dwReturn** è impostato sul numero del tipo di monitoraggio audio attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a029d-391">The **dwReturn** member is set to the number of the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>\_ \_ \_ record audio stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI\_VCR\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="a029d-393">Il membro **dwReturn** è impostato su **true** se l'audio viene registrato quando viene specificato il comando record successivo. in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-393">The **dwReturn** member is set to **TRUE** if audio will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="a029d-394">Se si specifica la \_ traccia MCI nel parametro *dwFlags* di questo comando, **dwTrack** contiene la traccia a cui si applica questa richiesta.</span><span class="sxs-lookup"><span data-stu-id="a029d-394">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>\_ \_ \_ origine audio stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-396">Il membro **dwReturn** è impostato su una costante che indica il tipo di origine audio corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-396">The **dwReturn** member is set to a constant, indicating the current audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>codice \_ \_ \_ sorgente audio stato \_ VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="a029d-398">Il membro **dwReturn** è impostato sul numero del tipo di origine audio attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a029d-398">The **dwReturn** member is set to the number of the currently selected audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>\_ \_ Clock stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI\_VCR\_STATUS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="a029d-400">Il membro **dwReturn** è impostato sul valore clock corrente, in incrementi di clock totali.</span><span class="sxs-lookup"><span data-stu-id="a029d-400">The **dwReturn** member is set to the current clock value, in total clock increments.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>\_ \_ \_ ID Clock stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI\_VCR\_STATUS\_CLOCK\_ID</span></span>
</dt> <dd>

<span data-ttu-id="a029d-402">Il membro **dwReturn** è impostato su un numero che descrive in modo univoco il clock in uso.</span><span class="sxs-lookup"><span data-stu-id="a029d-402">The **dwReturn** member is set to a number which uniquely describes the clock in use.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>\_ \_ \_ formato contatore stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI\_VCR\_STATUS\_COUNTER\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-404">Il membro **dwReturn** è impostato su una costante che descrive il formato del contatore corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-404">The **dwReturn** member is set to a constant describing the current counter format.</span></span> <span data-ttu-id="a029d-405">Per ulteriori informazioni, vedere il \_ flag MCI set \_ time \_ Format del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="a029d-405">For more information, see the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>\_risoluzione del \_ contatore di stato VCR \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>MCI\_VCR\_STATUS\_COUNTER\_RESOLUTION</span></span>
</dt> <dd>

<span data-ttu-id="a029d-407">Il membro **dwReturn** è impostato su una costante che descrive la risoluzione del contatore ed è uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a029d-407">The **dwReturn** member is set to a constant describing the resolution of the counter, and is one of the following values:</span></span>

-   <span data-ttu-id="a029d-408">\_ \_ \_ Frame di res del contatore VCR MCI \_ : il contatore ha la risoluzione dei frame.</span><span class="sxs-lookup"><span data-stu-id="a029d-408">MCI\_VCR\_COUNTER\_RES\_FRAMES: Counter has resolution of frames.</span></span>
-   <span data-ttu-id="a029d-409">\_ \_ Contatori del contatore VCR MCI \_ \_ : contatore con risoluzione dei secondi.</span><span class="sxs-lookup"><span data-stu-id="a029d-409">MCI\_VCR\_COUNTER\_RES\_SECONDS: Counter has resolution of seconds.</span></span>
-   <span data-ttu-id="a029d-410">\_Valore del \_ contatore di stato VCR MCI \_ \_ : il membro **dwReturn** è impostato sul contatore corrente, nel formato del contatore corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-410">MCI\_VCR\_STATUS\_COUNTER\_VALUE: The **dwReturn** member is set to the current counter reading, in the current counter-time format.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>\_ \_ \_ frequenza fotogrammi di stato VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI\_VCR\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-412">Il membro **dwReturn** è impostato sulla frequenza dei fotogrammi nativa corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a029d-412">The **dwReturn** member is set to the current native frame rate of the device.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>\_ \_ Indice stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>MCI\_VCR\_STATUS\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="a029d-414">Il membro **dwReturn** è impostato su una costante, che descrive il contenuto corrente dello schermo sullo schermo, ed è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="a029d-414">The **dwReturn** member is set to a constant, describing the current contents of the on-screen display, and is one of the following:</span></span>

-   <span data-ttu-id="a029d-415">\_ \_ contatore indice VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-415">MCI\_VCR\_INDEX\_COUNTER</span></span>
-   <span data-ttu-id="a029d-416">\_Data di \_ Indice MCI VCR \_</span><span class="sxs-lookup"><span data-stu-id="a029d-416">MCI\_VCR\_INDEX\_DATE</span></span>
-   <span data-ttu-id="a029d-417">\_ora di \_ indicizzazione VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-417">MCI\_VCR\_INDEX\_TIME</span></span>
-   <span data-ttu-id="a029d-418">\_ \_ codice temporale dell'indice MCI VCR \_</span><span class="sxs-lookup"><span data-stu-id="a029d-418">MCI\_VCR\_INDEX\_TIMECODE</span></span>

</dd> <dt>

<span data-ttu-id="a029d-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>\_ \_ Indice stato VCR \_ MCI \_ in</span><span class="sxs-lookup"><span data-stu-id="a029d-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>MCI\_VCR\_STATUS\_INDEX\_ON</span></span>
</dt> <dd>

<span data-ttu-id="a029d-420">Il membro **dwReturn** è impostato su **true** se lo schermo sullo schermo è acceso; in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-420">The **dwReturn** member is set to **TRUE** if the on-screen display is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>\_tipo di \_ supporto di stato VCR \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MCI\_VCR\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-422">Il membro **dwReturn** è impostato su uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="a029d-422">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="a029d-423">\_Supporti VCR \_ MCI \_ 8mm</span><span class="sxs-lookup"><span data-stu-id="a029d-423">MCI\_VCR\_MEDIA\_8MM</span></span>
-   <span data-ttu-id="a029d-424">\_ \_ Hi8 supporti VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-424">MCI\_VCR\_MEDIA\_HI8</span></span>
-   <span data-ttu-id="a029d-425">\_VCR \_ dei supporti \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-425">MCI\_VCR\_MEDIA\_VHS</span></span>
-   <span data-ttu-id="a029d-426">\_ \_ SVHS supporti VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-426">MCI\_VCR\_MEDIA\_SVHS</span></span>
-   <span data-ttu-id="a029d-427">\_supporto VCR \_ MCI \_ beta</span><span class="sxs-lookup"><span data-stu-id="a029d-427">MCI\_VCR\_MEDIA\_BETA</span></span>
-   <span data-ttu-id="a029d-428">\_ \_ EDBETA supporti VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-428">MCI\_VCR\_MEDIA\_EDBETA</span></span>
-   <span data-ttu-id="a029d-429">\_ \_ altri supporti VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-429">MCI\_VCR\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="a029d-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>\_ \_ numero stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>MCI\_VCR\_STATUS\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="a029d-431">Il membro **dwNumber** è impostato sul numero di sintonizzatori logici quando si usa questo flag con il \_ flag del canale del \_ sintonizzatore di stato di MCI VCR \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a029d-431">The **dwNumber** member is set to the logical-tuner number when you use this flag with the MCI\_VCR\_STATUS\_TUNER\_CHANNEL flag.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>\_ \_ \_ numero \_ di \_ tracce audio del \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_AUDIO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="a029d-433">Il membro **dwReturn** è impostato sul numero di tracce audio selezionabili in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="a029d-433">The **dwReturn** member is set to the number of audio tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>\_ \_ stato del videoregistratore \_ MCI \_ numero \_ di \_ tracce video</span><span class="sxs-lookup"><span data-stu-id="a029d-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_VIDEO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="a029d-435">Il membro **dwReturn** è impostato sul numero di tracce video che sono selezionabili in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="a029d-435">The **dwReturn** member is set to the number of video tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>\_timeout di \_ \_ sospensione stato VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI\_VCR\_STATUS\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-437">Il membro **dwReturn** è impostato sulla durata massima, in millisecondi, di un comando pause.</span><span class="sxs-lookup"><span data-stu-id="a029d-437">The **dwReturn** member is set to the maximum duration, in milliseconds, of a pause command.</span></span> <span data-ttu-id="a029d-438">Il valore restituito zero indica che non si verificherà alcun timeout.</span><span class="sxs-lookup"><span data-stu-id="a029d-438">The return value of zero indicates that no time-out will occur.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>\_ \_ \_ formato riproduzione stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI\_VCR\_STATUS\_PLAY\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-440">Il membro **dwReturn** è impostato su uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="a029d-440">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="a029d-441">\_EP del \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-441">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="a029d-442">\_ \_ LP formato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-442">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="a029d-443">\_ \_ altro formato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-443">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="a029d-444">\_ \_ SP formato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-444">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="a029d-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>\_durata del \_ \_ postroll stato VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>MCI\_VCR\_STATUS\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="a029d-446">Il membro **dwReturn** è impostato sulla lunghezza del nastro che verrà riprodotto dopo il punto in cui è stato arrestato, nel formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-446">The **dwReturn** member is set to the length of the videotape that will play after the spot at which it was stopped, in the current time format.</span></span> <span data-ttu-id="a029d-447">Questa operazione è necessaria per frenare il trasporto del nastro VCR da un comando stop o pause.</span><span class="sxs-lookup"><span data-stu-id="a029d-447">This is needed to brake the VCR tape transport from a stop or pause command.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>acceso \_ \_ stato VCR \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI\_VCR\_STATUS\_POWER\_ON</span></span>
</dt> <dd>

<span data-ttu-id="a029d-449">Il membro **dwReturn** è impostato su **true** se l'alimentazione è attiva; in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-449">The **dwReturn** member is set to **TRUE** if the power is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>\_ \_ \_ durata preregistrazione stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>MCI\_VCR\_STATUS\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="a029d-451">Il membro **dwReturn** è impostato sulla lunghezza del nastro che verrà riprodotto prima del punto in cui è stato avviato, nel formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-451">The **dwReturn** member is set to the length of the videotape that will play before the spot at which it was started, in the current time format.</span></span> <span data-ttu-id="a029d-452">Questa operazione è necessaria per stabilizzare l'output del videoregistratore.</span><span class="sxs-lookup"><span data-stu-id="a029d-452">This is needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>\_ \_ formato record di stato VCR \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>MCI\_VCR\_STATUS\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-454">Il membro **dwReturn** è impostato su uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="a029d-454">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="a029d-455">\_EP del \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-455">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="a029d-456">\_ \_ LP formato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-456">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="a029d-457">\_ \_ altro formato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-457">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="a029d-458">\_ \_ SP formato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-458">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="a029d-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>\_ \_ velocità stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>MCI\_VCR\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="a029d-460">Il membro **dwReturn** è impostato sulla velocità corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-460">The **dwReturn** member is set to the current speed.</span></span> <span data-ttu-id="a029d-461">Per ulteriori informazioni, vedere il \_ flag MCI VCR \_ set \_ Speed del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="a029d-461">For more information, see the MCI\_VCR\_SET\_SPEED flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>\_ \_ \_ modalità ora stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI\_VCR\_STATUS\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-463">Il membro **dwReturn** è impostato su uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="a029d-463">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="a029d-464">\_ \_ contatore tempo VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-464">MCI\_VCR\_TIME\_COUNTER</span></span>
-   <span data-ttu-id="a029d-465">\_ \_ rilevamento ora VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-465">MCI\_VCR\_TIME\_DETECT</span></span>
-   <span data-ttu-id="a029d-466">\_ \_ timecode ora VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-466">MCI\_VCR\_TIME\_TIMECODE</span></span>

<span data-ttu-id="a029d-467">Per ulteriori informazioni, vedere il \_ flag MCI VCR \_ set \_ time \_ mode del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="a029d-467">For more information, see the MCI\_VCR\_SET\_TIME\_MODE flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>\_ \_ \_ tipo ora stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI\_VCR\_STATUS\_TIME\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-469">Il membro **dwReturn** è impostato su una costante che descrive il tipo di ora corrente in uso (usato da [Play](play.md), [record](record.md), [Seek](seek.md)e così via) ed è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="a029d-469">The **dwReturn** member is set to a constant describing the current time type in use (used by [play](play.md), [record](record.md), [seek](seek.md), and so on), and is one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="a029d-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_ \_ contatore tempo VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="a029d-471">Il contatore è in uso.</span><span class="sxs-lookup"><span data-stu-id="a029d-471">Counter is in use.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_ \_ timecode ora VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-473">Il codice temporale è in uso.</span><span class="sxs-lookup"><span data-stu-id="a029d-473">Timecode is in use.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>\_ \_ timecode stato VCR \_ MCI \_ presente</span><span class="sxs-lookup"><span data-stu-id="a029d-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>MCI\_VCR\_STATUS\_TIMECODE\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-475">Il membro **dwReturn** è impostato su **true** se il codice temporale è presente nella posizione corrente nel contenuto; in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-475">The **dwReturn** member is set to **TRUE** if timecode is present at the current position in the content; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>\_record del \_ timecode di stato VCR \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI\_VCR\_STATUS\_TIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="a029d-477">Il membro **dwReturn** è impostato su **true** se il codice temporale viene registrato quando viene specificato il comando record successivo. in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-477">The **dwReturn** member is set to **TRUE** if the timecode will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>\_tipo di \_ \_ timecode stato VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>MCI\_VCR\_STATUS\_TIMECODE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-479">Il membro **dwReturn** è impostato su una costante, che descrive il tipo di codice temporale supportato direttamente dal dispositivo ed è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="a029d-479">The **dwReturn** member is set to a constant, describing the type of timecode that is directly supported by the device, and is one of the following:</span></span>

-   <span data-ttu-id="a029d-480">\_Tipo di timecode VCR del videoregistratore MCI \_ \_ \_ : questo dispositivo non usa un timecode.</span><span class="sxs-lookup"><span data-stu-id="a029d-480">MCI\_VCR\_TIMECODE\_TYPE\_NONE: This device does not use a timecode.</span></span>
-   <span data-ttu-id="a029d-481">\_ \_ Tipo di codice temporale VCR MCI \_ \_ : questo dispositivo usa un timecode non specificato.</span><span class="sxs-lookup"><span data-stu-id="a029d-481">MCI\_VCR\_TIMECODE\_TYPE\_OTHER: This device uses an unspecified timecode.</span></span>
-   <span data-ttu-id="a029d-482">MCI \_ VCR \_ tipo di codice \_ \_ SMPTE: questo dispositivo usa il timecode SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a029d-482">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE: This device uses SMPTE timecode.</span></span>
-   <span data-ttu-id="a029d-483">MCI \_ VCR \_ \_ Type timecode \_ \_ Drop: questo dispositivo usa il timecode di rilascio SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a029d-483">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE\_DROP: This device uses SMPTE drop timecode.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>\_ \_ \_ canale Tuner stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI\_VCR\_STATUS\_TUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="a029d-485">Il membro **dwReturn** è impostato sul numero di canale corrente.</span><span class="sxs-lookup"><span data-stu-id="a029d-485">The **dwReturn** member is set to the current channel number.</span></span> <span data-ttu-id="a029d-486">Se si specifica il \_ \_ numero di stato VCR MCI \_ nel parametro *dwFlags* di questo comando, **dwNumber** contiene il numero di Tuner logico a cui si applica questo comando.</span><span class="sxs-lookup"><span data-stu-id="a029d-486">If you specify MCI\_VCR\_STATUS\_NUMBER in the *dwFlags* parameter of this command, **dwNumber** contains the logical-tuner number this command applies to.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>\_ \_ \_ monitoraggio video stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="a029d-488">Il membro **dwReturn** è impostato su una costante che indica il tipo di monitoraggio video attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a029d-488">The **dwReturn** member is set to a constant, indicating the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>\_numero di \_ \_ monitor video \_ stato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="a029d-490">Il membro **dwReturn** è impostato sul numero del tipo di monitor video attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a029d-490">The **dwReturn** member is set to the number of the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>\_ \_ \_ record video stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>MCI\_VCR\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="a029d-492">Il membro **dwReturn** è impostato su **true** se viene registrato il video quando viene specificato il comando record successivo. in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-492">The **dwReturn** member is set to **TRUE** if video will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="a029d-493">Se si specifica la \_ traccia MCI nel parametro *dwFlags* di questo comando, **dwTrack** contiene la traccia a cui si applica questa richiesta.</span><span class="sxs-lookup"><span data-stu-id="a029d-493">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>\_ \_ \_ origine video stato VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-495">Il membro **dwReturn** è impostato su una costante che indica il tipo di origine video attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a029d-495">The **dwReturn** member is set to a constant indicating the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>\_numero di \_ \_ origine video \_ di stato VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="a029d-497">Il membro **dwReturn** è impostato sul numero del tipo di origine video attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a029d-497">The **dwReturn** member is set to the number of the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>\_ \_ \_ scrittura \_ protetta stato VCR MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI\_VCR\_STATUS\_WRITE\_PROTECTED</span></span>
</dt> <dd>

<span data-ttu-id="a029d-499">Il membro **dwReturn** è impostato su **true** se il supporto è protetto da scrittura; in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-499">The **dwReturn** member is set to **TRUE** if the media is write-protected; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="a029d-500">Per i dispositivi VCR, il parametro *lpStatus* punta a una struttura [**\_ \_ \_ parametri di stato VCR di MCI**](mci-vcr-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a029d-500">For VCR devices, the *lpStatus* parameter points to an [**MCI\_VCR\_STATUS\_PARMS**](mci-vcr-status-parms.md) structure.</span></span>

<span data-ttu-id="a029d-501">\_Se si utilizza il flag di lunghezza stato MCI \_ per determinare la lunghezza del supporto, vengono restituiti sempre 2 ore per i dispositivi VCR, a meno che la lunghezza non sia stata modificata in modo esplicito utilizzando il comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="a029d-501">Using the MCI\_STATUS\_LENGTH flag to determine the length of the media always returns 2 hours for VCR devices, unless the length has been explicitly changed using the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="a029d-502">I flag aggiuntivi seguenti vengono utilizzati con il tipo di dispositivo **overlay** .</span><span class="sxs-lookup"><span data-stu-id="a029d-502">The following additional flags are used with the **overlay** device type.</span></span> <span data-ttu-id="a029d-503">Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a029d-503">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="a029d-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>\_ \_ HWND stato OVLY \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI\_OVLY\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="a029d-505">Il membro **dwReturn** è impostato sull'handle della finestra associata al dispositivo di sovrimpressione video.</span><span class="sxs-lookup"><span data-stu-id="a029d-505">The **dwReturn** member is set to the handle of the window associated with the video-overlay device.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>\_ \_ estensione stato OVLY \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI\_OVLY\_STATUS\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="a029d-507">Il membro **dwReturn** è impostato su **true** se l'estensione è abilitata; in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-507">The **dwReturn** member is set to **TRUE** if stretching is enabled; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="a029d-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-509">Il membro **dwReturn** è impostato su **true** se il supporto viene inserito nel dispositivo. in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-509">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="a029d-510">I flag aggiuntivi seguenti vengono utilizzati con il tipo di dispositivo **videodisco** .</span><span class="sxs-lookup"><span data-stu-id="a029d-510">The following additional flags are used with the **videodisc** device type.</span></span> <span data-ttu-id="a029d-511">Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a029d-511">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="a029d-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="a029d-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-513">Il membro **dwReturn** è impostato su **true** se il supporto viene inserito nel dispositivo. in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-513">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modalità stato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-515">Il membro **dwReturn** è impostato sulla modalità corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a029d-515">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="a029d-516">I dispositivi videodisco possono restituire la \_ \_ costante del Parco della modalità di MCI VD \_ , oltre alle costanti che qualsiasi dispositivo può restituire, come documentato con il parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a029d-516">Videodisc devices can return the MCI\_VD\_MODE\_PARK constant, in addition to the constants any device can return, as documented with the *dwFlags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>\_dimensioni del \_ disco di stato MCI VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="a029d-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI\_VD\_STATUS\_DISC\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-518">Il membro **dwReturn** è impostato sulla dimensione del disco caricato in pollici (8 o 12).</span><span class="sxs-lookup"><span data-stu-id="a029d-518">The **dwReturn** member is set to the size of the loaded disc in inches (8 or 12).</span></span>

</dd> <dt>

<span data-ttu-id="a029d-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>stato di MCI \_ VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="a029d-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI\_VD\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="a029d-520">Il membro **dwReturn** è impostato su **true** in caso di riproduzione. in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="a029d-520">The **dwReturn** member is set to **TRUE** if playing forward; it is set to **FALSE** otherwise.</span></span>

<span data-ttu-id="a029d-521">Il dispositivo videodisco MCI non supporta questo flag.</span><span class="sxs-lookup"><span data-stu-id="a029d-521">The MCI videodisc device does not support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>\_tipo di \_ supporto di stato MCI VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="a029d-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI\_VD\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-523">Il membro **dwReturn** è impostato sul tipo di supporto del supporto inserito.</span><span class="sxs-lookup"><span data-stu-id="a029d-523">The **dwReturn** member is set to the media type of the inserted media.</span></span> <span data-ttu-id="a029d-524">È possibile restituire i tipi di supporto seguenti:</span><span class="sxs-lookup"><span data-stu-id="a029d-524">The following media types can be returned:</span></span>

<span data-ttu-id="a029d-525">MCI \_ VD \_ media \_ CAV</span><span class="sxs-lookup"><span data-stu-id="a029d-525">MCI\_VD\_MEDIA\_CAV</span></span>

<span data-ttu-id="a029d-526">MCI \_ VD \_ media \_ CLV</span><span class="sxs-lookup"><span data-stu-id="a029d-526">MCI\_VD\_MEDIA\_CLV</span></span>

<span data-ttu-id="a029d-527">\_ \_ altri supporti MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="a029d-527">MCI\_VD\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="a029d-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>\_ \_ lato stato di MCI VD \_</span><span class="sxs-lookup"><span data-stu-id="a029d-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI\_VD\_STATUS\_SIDE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-529">Il membro **dwReturn** è impostato su 1 o 2 per indicare quale lato del disco è caricato.</span><span class="sxs-lookup"><span data-stu-id="a029d-529">The **dwReturn** member is set to 1 or 2 to indicate which side of the disc is loaded.</span></span> <span data-ttu-id="a029d-530">Questo flag non è supportato da tutti i dispositivi videodisco.</span><span class="sxs-lookup"><span data-stu-id="a029d-530">Not all videodisc devices support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>\_ \_ velocità stato MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="a029d-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI\_VD\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="a029d-532">Il membro **dwReturn** è impostato sulla velocità di riproduzione in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="a029d-532">The **dwReturn** member is set to the play speed in frames per second.</span></span> <span data-ttu-id="a029d-533">MCIPIONR. Il driver di dispositivo DRV restituisce MCIERR \_ funzione non supportata \_ .</span><span class="sxs-lookup"><span data-stu-id="a029d-533">The MCIPIONR.DRV device driver returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> </dl>

<span data-ttu-id="a029d-534">I flag aggiuntivi seguenti vengono utilizzati con il tipo di dispositivo **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="a029d-534">The following additional flags are used with the **waveaudio** device type.</span></span> <span data-ttu-id="a029d-535">Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a029d-535">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="a029d-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>\_FORMATTAG Wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI\_WAVE\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="a029d-537">Il membro **dwReturn** è impostato sul tag di formato corrente usato per la riproduzione, la registrazione e il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="a029d-537">The **dwReturn** member is set to the current format tag used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_input wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-539">Il membro **dwReturn** è impostato sul dispositivo di input wave usato per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="a029d-539">The **dwReturn** member is set to the wave input device used for recording.</span></span> <span data-ttu-id="a029d-540">Se non è in uso alcun dispositivo e non è stato impostato in modo esplicito alcun dispositivo, il risultato dell'errore è MCIERR \_ Wave \_ INPUTUNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="a029d-540">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_INPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_Output Wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="a029d-542">Il membro **dwReturn** è impostato sul dispositivo di output wave usato per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a029d-542">The **dwReturn** member is set to the wave output device used for playing.</span></span> <span data-ttu-id="a029d-543">Se non è in uso alcun dispositivo e non è stato impostato in modo esplicito alcun dispositivo, il risultato dell'errore è MCIERR \_ Wave \_ OUTPUTUNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="a029d-543">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_OUTPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>\_stato dell'onda MCI \_ \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="a029d-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI\_WAVE\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="a029d-545">Il membro **dwReturn** è impostato sui byte correnti al secondo usati per la riproduzione, la registrazione e il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="a029d-545">The **dwReturn** member is set to the current bytes per second used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>\_stato dell'onda MCI \_ \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="a029d-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI\_WAVE\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="a029d-547">Il membro **dwReturn** è impostato sui bit correnti per campione usato per la riproduzione, la registrazione e il salvataggio dei dati in formato PCM.</span><span class="sxs-lookup"><span data-stu-id="a029d-547">The **dwReturn** member is set to the current bits per sample used for playing, recording, and saving PCM formatted data.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>\_stato dell'onda MCI \_ \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="a029d-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI\_WAVE\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="a029d-549">Il membro **dwReturn** è impostato sull'allineamento a blocchi corrente utilizzato per la riproduzione, la registrazione e il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="a029d-549">The **dwReturn** member is set to the current block alignment used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>\_canali di \_ stato dell'onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI\_WAVE\_STATUS\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="a029d-551">Il membro **dwReturn** è impostato sul numero di canali corrente usato per la riproduzione, la registrazione e il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="a029d-551">The **dwReturn** member is set to the current channel count used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>\_livello di \_ stato dell'onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI\_WAVE\_STATUS\_LEVEL</span></span>
</dt> <dd>

<span data-ttu-id="a029d-553">Il membro **dwReturn** è impostato sul livello di riproduzione o record corrente dei dati in formato PCM.</span><span class="sxs-lookup"><span data-stu-id="a029d-553">The **dwReturn** member is set to the current record or playback level of PCM formatted data.</span></span> <span data-ttu-id="a029d-554">Il valore viene restituito come valore a 8 o a 16 bit, a seconda delle dimensioni del campione utilizzate.</span><span class="sxs-lookup"><span data-stu-id="a029d-554">The value is returned as an 8- or 16-bit value, depending on the sample size used.</span></span> <span data-ttu-id="a029d-555">Il livello di canale destro o mono viene restituito nella parola di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="a029d-555">The right or mono channel level is returned in the low-order word.</span></span> <span data-ttu-id="a029d-556">Il livello di canale sinistro viene restituito nella parola più ordinata.</span><span class="sxs-lookup"><span data-stu-id="a029d-556">The left channel level is returned in the high-order word.</span></span>

</dd> <dt>

<span data-ttu-id="a029d-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>\_stato dell'onda MCI \_ \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="a029d-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI\_WAVE\_STATUS\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="a029d-558">Il membro **dwReturn** è impostato sugli esempi correnti al secondo usati per la riproduzione, la registrazione e il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="a029d-558">The **dwReturn** member is set to the current samples per second used for playing, recording, and saving.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a029d-559">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a029d-559">Requirements</span></span>



| <span data-ttu-id="a029d-560">Requisito</span><span class="sxs-lookup"><span data-stu-id="a029d-560">Requirement</span></span> | <span data-ttu-id="a029d-561">Valore</span><span class="sxs-lookup"><span data-stu-id="a029d-561">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a029d-562">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a029d-562">Minimum supported client</span></span><br/> | <span data-ttu-id="a029d-563">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a029d-563">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a029d-564">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a029d-564">Minimum supported server</span></span><br/> | <span data-ttu-id="a029d-565">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a029d-565">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a029d-566">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a029d-566">Header</span></span><br/>                   | <dl> <span data-ttu-id="a029d-567"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a029d-567"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a029d-568">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a029d-568">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a029d-569">MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-569">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a029d-570">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-570">MCI Commands</span></span>](mci-commands.md)
</dt> <dt>

[<span data-ttu-id="a029d-571">\_taglia MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-571">MCI\_CUT</span></span>](mci-cut.md)
</dt> <dt>

[<span data-ttu-id="a029d-572">eliminazione di MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-572">MCI\_DELETE</span></span>](mci-delete.md)
</dt> <dt>

[<span data-ttu-id="a029d-573">\_Incolla MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-573">MCI\_PASTE</span></span>](mci-paste.md)
</dt> <dt>

[<span data-ttu-id="a029d-574">\_riserva MCI</span><span class="sxs-lookup"><span data-stu-id="a029d-574">MCI\_RESERVE</span></span>](mci-reserve.md)
</dt> <dt>

[<span data-ttu-id="a029d-575">SET di MCI \_</span><span class="sxs-lookup"><span data-stu-id="a029d-575">MCI\_SET</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="a029d-576">Play</span><span class="sxs-lookup"><span data-stu-id="a029d-576">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="a029d-577">record</span><span class="sxs-lookup"><span data-stu-id="a029d-577">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="a029d-578">cercare</span><span class="sxs-lookup"><span data-stu-id="a029d-578">seek</span></span>](seek.md)
</dt> </dl>

 

