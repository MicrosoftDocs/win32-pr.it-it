---
title: Comando MCI_GETDEVCAPS (mmsystem. h)
description: Il \_ comando MCI GETDEVCAPS recupera informazioni statiche su un dispositivo.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- Comando MCI_GETDEVCAPS Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519042"
---
# <a name="mci_getdevcaps-command"></a><span data-ttu-id="d38f7-104">\_Comando GETDEVCAPS di MCI</span><span class="sxs-lookup"><span data-stu-id="d38f7-104">MCI\_GETDEVCAPS command</span></span>

<span data-ttu-id="d38f7-105">Il \_ comando MCI GETDEVCAPS recupera informazioni statiche su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d38f7-105">The MCI\_GETDEVCAPS command retrieves static information about a device.</span></span> <span data-ttu-id="d38f7-106">Tutti i dispositivi riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="d38f7-106">All devices recognize this command.</span></span> <span data-ttu-id="d38f7-107">I parametri e i flag disponibili per questo comando dipendono dal dispositivo selezionato.</span><span class="sxs-lookup"><span data-stu-id="d38f7-107">The parameters and flags available for this command depend on the selected device.</span></span> <span data-ttu-id="d38f7-108">Le informazioni vengono restituite nel membro **dwReturn** della struttura identificata da *lpCapsParms*.</span><span class="sxs-lookup"><span data-stu-id="d38f7-108">Information is returned in the **dwReturn** member of the structure identified by *lpCapsParms*.</span></span>

<span data-ttu-id="d38f7-109">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="d38f7-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
);
```



## <a name="parameters"></a><span data-ttu-id="d38f7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d38f7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d38f7-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d38f7-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-112">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="d38f7-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d38f7-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-114">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d38f7-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="d38f7-115">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d38f7-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span><span class="sxs-lookup"><span data-stu-id="d38f7-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-117">Puntatore a una [**struttura \_ \_ parametri GETDEVCAPS di MCI**](mci-getdevcaps-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d38f7-117">Pointer to an [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d38f7-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d38f7-118">Return Value</span></span>

<span data-ttu-id="d38f7-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="d38f7-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d38f7-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d38f7-120">Remarks</span></span>

<span data-ttu-id="d38f7-121">Per tutti i dispositivi che supportano MCI GETDEVCAPS sono applicabili i flag aggiuntivi standard e specifici dei comandi seguenti \_ :</span><span class="sxs-lookup"><span data-stu-id="d38f7-121">The following additional standard and command-specific flags apply to all devices supporting MCI\_GETDEVCAPS:</span></span>

<dl> <dt>

<span data-ttu-id="d38f7-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>\_ \_ dispositivo composto GETDEVCAPS \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d38f7-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI\_GETDEVCAPS\_COMPOUND\_DEVICE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-123">Il membro **dwReturn** è impostato su **true** se il dispositivo utilizza l'archiviazione dei dati che deve essere aperta e chiusa in modo esplicito; in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="d38f7-123">The **dwReturn** member is set to **TRUE** if the device uses data storage that must be explicitly opened and closed; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>\_tipo di \_ dispositivo \_ GETDEVCAPS MCI</span><span class="sxs-lookup"><span data-stu-id="d38f7-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI\_GETDEVCAPS\_DEVICE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-125">Il membro **dwReturn** è impostato su uno dei valori elencati nei [tipi di dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="d38f7-125">The **dwReturn** member is set to one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>\_GETDEVCAPS MCI \_ con \_ audio</span><span class="sxs-lookup"><span data-stu-id="d38f7-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI\_GETDEVCAPS\_HAS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-127">Il membro **dwReturn** è impostato su **true** se il dispositivo ha un output audio. in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="d38f7-127">The **dwReturn** member is set to **TRUE** if the device has audio output; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>GETDEVCAPS di MCI \_ \_ con \_ video</span><span class="sxs-lookup"><span data-stu-id="d38f7-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI\_GETDEVCAPS\_HAS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-129">Il membro **dwReturn** è impostato su **true** se l'output del dispositivo è video; in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="d38f7-129">The **dwReturn** member is set to **TRUE** if the device has video output; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="d38f7-130">Ad esempio, il membro è impostato su **true** per i dispositivi che supportano il set di comandi videodisco.</span><span class="sxs-lookup"><span data-stu-id="d38f7-130">For example, the member is set to **TRUE** for devices that support the videodisc command set.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>\_elemento GETDEVCAPS di MCI \_</span><span class="sxs-lookup"><span data-stu-id="d38f7-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI\_GETDEVCAPS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-132">Specifica che il membro **dwItem** della struttura [**\_ GETDEVCAPS \_ parametri di MCI**](mci-getdevcaps-parms.md) contiene una delle costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="d38f7-132">Specifies that the **dwItem** member of the [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure contains one of the following constants:</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>\_GETDEVCAPS MCI \_ possono essere \_ espulsione</span><span class="sxs-lookup"><span data-stu-id="d38f7-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI\_GETDEVCAPS\_CAN\_EJECT</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-134">Il membro **dwReturn** è impostato su **true** se il dispositivo può espellere il supporto. in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-134">The **dwReturn** member is set to **TRUE** if the device can eject the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>\_GETDEVCAPS MCI \_ può essere \_ riprodotto</span><span class="sxs-lookup"><span data-stu-id="d38f7-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI\_GETDEVCAPS\_CAN\_PLAY</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-136">Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di riprodurre i supporti; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-136">The **dwReturn** member is set to **TRUE** if the device can play the media; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="d38f7-137">Se un dispositivo specifica **true**, significa che il dispositivo supporta i comandi [MCI \_ pause](mci-pause.md) e [MCI \_ Stop](mci-stop.md) , oltre al comando [MCI \_ Play](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="d38f7-137">If a device specifies **TRUE**, it implies the device supports the [MCI\_PAUSE](mci-pause.md) and [MCI\_STOP](mci-stop.md) commands as well as the [MCI\_PLAY](mci-play.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>\_GETDEVCAPS MCI \_ può \_ registrare</span><span class="sxs-lookup"><span data-stu-id="d38f7-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI\_GETDEVCAPS\_CAN\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-139">Il membro **dwReturn** è impostato su **true** se il dispositivo supporta la registrazione; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-139">The **dwReturn** member is set to **TRUE** if the device supports recording; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="d38f7-140">Se un dispositivo specifica **true**, significa che il dispositivo supporta i \_ comandi MCI pause e MCI stop, nonché \_ il comando [MCI \_ record](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="d38f7-140">If a device specifies **TRUE**, it implies the device supports the MCI\_PAUSE and MCI\_STOP commands as well as the [MCI\_RECORD](mci-record.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>\_GETDEVCAPS MCI \_ può \_ salvare</span><span class="sxs-lookup"><span data-stu-id="d38f7-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI\_GETDEVCAPS\_CAN\_SAVE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-142">Il membro **dwReturn** è impostato su **true** se il dispositivo può salvare un file; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-142">The **dwReturn** member is set to **TRUE** if the device can save a file; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ Usa \_ i file</span><span class="sxs-lookup"><span data-stu-id="d38f7-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI\_GETDEVCAPS\_USES\_FILES</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-144">Il membro **dwReturn** è impostato su **true** se il dispositivo richiede un nome file; in caso contrario, viene impostato su **false** .</span><span class="sxs-lookup"><span data-stu-id="d38f7-144">The **dwReturn** member is set to **TRUE** if the device requires a filename; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="d38f7-145">Solo i dispositivi composti utilizzano i file.</span><span class="sxs-lookup"><span data-stu-id="d38f7-145">Only compound devices use files.</span></span>

</dd> </dl>

<span data-ttu-id="d38f7-146">I flag seguenti possono essere specificati nel membro **dwItem** di [**MCI \_ GETDEVCAPS \_ parametri**](mci-getdevcaps-parms.md) per il tipo di dispositivo **digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="d38f7-146">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d38f7-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS \_ can \_ Freeze</span><span class="sxs-lookup"><span data-stu-id="d38f7-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-148">Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di bloccare i frame; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-148">The **dwReturn** member is set to **TRUE** if the device can freeze frames; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ can \_ Lock</span><span class="sxs-lookup"><span data-stu-id="d38f7-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-150">Il membro **dwReturn** è impostato su **true** se il dispositivo può bloccarsi; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-150">The **dwReturn** member is set to **TRUE** if the device can lock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ GETDEVCAPS \_ can \_ Reverse</span><span class="sxs-lookup"><span data-stu-id="d38f7-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-152">Il membro **dwReturn** è impostato su **true** se il dispositivo può essere riprodotto in senso inverso. in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-152">The **dwReturn** member is set to **TRUE** if the device can play in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ può \_ Str \_ in</span><span class="sxs-lookup"><span data-stu-id="d38f7-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STR\_IN</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-154">Il membro **dwReturn** è impostato su **true** se il dispositivo può estendere l'input; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-154">The **dwReturn** member is set to **TRUE** if the device can stretch input; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ GETDEVCAPS \_ può \_ estendersi</span><span class="sxs-lookup"><span data-stu-id="d38f7-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-156">Il membro **dwReturn** è impostato su **true** se il dispositivo può allungare un'immagine; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-156">The **dwReturn** member is set to **TRUE** if the device can stretch an image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ GETDEVCAPS \_ può \_ testare</span><span class="sxs-lookup"><span data-stu-id="d38f7-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-158">Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di eseguire i test; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-158">The **dwReturn** member is set to **TRUE** if the device can perform tests; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>\_GETDEVCAPS DGV di MCI \_ \_ è \_ ancora</span><span class="sxs-lookup"><span data-stu-id="d38f7-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI\_DGV\_GETDEVCAPS\_HAS\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-160">Il membro **dwReturn** è impostato su **true** se il dispositivo può visualizzare ancora le immagini; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-160">The **dwReturn** member is set to **TRUE** if the device can display still images; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>\_ \_ GETDEVCAPS max DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="d38f7-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI\_DGV\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-162">Il membro **dwReturn** è impostato sul numero massimo di finestre che il dispositivo è in grado di gestire simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="d38f7-162">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>\_ \_ \_ frequenza massima GETDEVCAPS DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d38f7-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MAXIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-164">Il membro **dwReturn** è impostato sulla velocità di riproduzione massima per il dispositivo, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="d38f7-164">The **dwReturn** member is set to the maximum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>\_DGV MCI \_ GETDEVCAPS \_ - \_ frequenza minima</span><span class="sxs-lookup"><span data-stu-id="d38f7-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MINIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-166">Il membro **dwReturn** è impostato sulla velocità di riproduzione minima per il dispositivo, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="d38f7-166">The **dwReturn** member is set to the minimum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>\_ \_ tavolozze GETDEVCAPS DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="d38f7-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI\_DGV\_GETDEVCAPS\_PALETTES</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-168">Il membro **dwReturn** è impostato su **true** se il dispositivo può restituire un handle della tavolozza; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-168">The **dwReturn** member is set to **TRUE** if the device can return a palette handle; otherwise, it is set to **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="d38f7-169">I flag seguenti possono essere specificati nel membro **dwItem** di [**MCI \_ GETDEVCAPS \_ parametri**](mci-getdevcaps-parms.md) per il tipo di dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="d38f7-169">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d38f7-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>\_frequenza di \_ incremento del clock GETDEVCAPS \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="d38f7-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI\_GETDEVCAPS\_CLOCK\_INCREMENT\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-171">Il membro **dwReturn** è impostato sul numero di incrementi al secondo.</span><span class="sxs-lookup"><span data-stu-id="d38f7-171">The **dwReturn** member is set to the number of increments per second.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>\_GETDEVCAPS VCR \_ MCI \_ può \_ rilevare la \_ lunghezza</span><span class="sxs-lookup"><span data-stu-id="d38f7-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_DETECT\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-173">Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di rilevare la lunghezza del supporto; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-173">The **dwReturn** member is set to **TRUE** if the device is capable of detecting the length of the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>il \_ GETDEVCAPS del VCR MCI \_ \_ può \_ bloccarsi</span><span class="sxs-lookup"><span data-stu-id="d38f7-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-175">Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di bloccare l'immagine di output; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-175">The **dwReturn** member is set to **TRUE** if the device is capable of freezing the output image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>\_GETDEVCAPS VCR di MCI \_ \_ possono monitorare le \_ \_ origini</span><span class="sxs-lookup"><span data-stu-id="d38f7-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_MONITOR\_SOURCES</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-177">Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di monitorare le origini; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-177">The **dwReturn** member is set to **TRUE** if the device is capable of monitoring sources; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>\_GETDEVCAPS VCR \_ MCI \_ può essere \_ preroll</span><span class="sxs-lookup"><span data-stu-id="d38f7-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-179">Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di eseguire la preregistrazione; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-179">The **dwReturn** member is set to **TRUE** if the device is capable of preroll; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>GETDEVCAPS VCR di MCI è \_ \_ \_ possibile \_ visualizzare in anteprima</span><span class="sxs-lookup"><span data-stu-id="d38f7-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREVIEW</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-181">Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di visualizzare le anteprime; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-181">The **dwReturn** member is set to **TRUE** if the device is capable of previews; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>\_GETDEVCAPS VCR \_ MCI \_ possono \_ invertire</span><span class="sxs-lookup"><span data-stu-id="d38f7-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-183">Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di riprodurre in senso inverso. in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-183">The **dwReturn** member is set to **TRUE** if the device is capable of playing in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>\_GETDEVCAPS VCR di MCI \_ \_ possono \_ eseguire test</span><span class="sxs-lookup"><span data-stu-id="d38f7-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-185">Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di eseguire il test; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-185">The **dwReturn** member is set to **TRUE** if the device is capable of testing; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>\_GETDEVCAPS VCR \_ MCI \_ con \_ Clock</span><span class="sxs-lookup"><span data-stu-id="d38f7-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-187">Il membro **dwReturn** è impostato su **true** se il dispositivo supporta un clock esterno. in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-187">The **dwReturn** member is set to **TRUE** if the device supports an external clock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>\_GETDEVCAPS VCR \_ MCI \_ con \_ timecode</span><span class="sxs-lookup"><span data-stu-id="d38f7-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-189">Il membro **dwReturn** è impostato su **true** se il dispositivo ha una funzionalità timecode o se questa funzionalità è sconosciuta. in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-189">The **dwReturn** member is set to **TRUE** if device has timecode capability or if this capability is unknown; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>\_ \_ \_ numero \_ di \_ CONTRASSEGNi GETDEVCAPS del VCR MCI</span><span class="sxs-lookup"><span data-stu-id="d38f7-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI\_VCR\_GETDEVCAPS\_NUMBER\_OF\_MARKS</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-191">Il membro **dwReturn** è impostato sul numero di contrassegni (99).</span><span class="sxs-lookup"><span data-stu-id="d38f7-191">The **dwReturn** member is set to the number of marks (99).</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>\_ \_ \_ accuratezza ricerca GETDEVCAPS VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="d38f7-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI\_VCR\_GETDEVCAPS\_SEEK\_ACCURACY</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-193">Il membro **dwReturn** è impostato sull'accuratezza della ricerca del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d38f7-193">The **dwReturn** member is set to the seek accuracy of the device.</span></span>

</dd> </dl>

<span data-ttu-id="d38f7-194">I flag seguenti possono essere specificati nel membro **dwItem** di [**MCI \_ GETDEVCAPS \_ parametri**](mci-getdevcaps-parms.md) per il tipo di dispositivo **overlay** :</span><span class="sxs-lookup"><span data-stu-id="d38f7-194">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d38f7-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ GETDEVCAPS \_ can \_ Freeze</span><span class="sxs-lookup"><span data-stu-id="d38f7-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-196">Il membro **dwReturn** è impostato su **true** se il dispositivo può bloccare l'immagine; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-196">The **dwReturn** member is set to **TRUE** if the device can freeze the image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI \_ OVLY \_ GETDEVCAPS \_ può \_ estendersi</span><span class="sxs-lookup"><span data-stu-id="d38f7-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-198">Il membro **dwReturn** è impostato su **true** se il dispositivo può allungare l'immagine per riempire il frame; in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-198">The **dwReturn** member is set to **TRUE** if the device can stretch the image to fill the frame; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>\_ \_ GETDEVCAPS max OVLY \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="d38f7-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI\_OVLY\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-200">Il membro **dwReturn** è impostato sul numero massimo di finestre che il dispositivo è in grado di gestire simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="d38f7-200">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> </dl>

<span data-ttu-id="d38f7-201">I flag seguenti possono essere specificati nel membro **dwItem** di [**MCI \_ GETDEVCAPS \_ parametri**](mci-getdevcaps-parms.md) per il tipo di dispositivo **videodisco** :</span><span class="sxs-lookup"><span data-stu-id="d38f7-201">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d38f7-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ VD \_ GETDEVCAPS \_ può \_ invertire</span><span class="sxs-lookup"><span data-stu-id="d38f7-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI\_VD\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-203">Il membro **dwReturn** è impostato su **true** se il lettore videodisco può riprodurre in ordine inverso. in caso contrario, viene impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f7-203">The **dwReturn** member is set to **TRUE** if the videodisc player can play in reverse; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="d38f7-204">Alcuni lettori possono riprodurre dischi CLV in senso inverso, oltre ai dischi CAV.</span><span class="sxs-lookup"><span data-stu-id="d38f7-204">Some players can play CLV discs in reverse as well as CAV discs.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ VD \_ GETDEVCAPS \_ CAV</span><span class="sxs-lookup"><span data-stu-id="d38f7-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI\_VD\_GETDEVCAPS\_CAV</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-206">In combinazione con altri elementi, specifica che le informazioni restituite si applicano al formato CAV videodischi.</span><span class="sxs-lookup"><span data-stu-id="d38f7-206">When combined with other items, specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="d38f7-207">Si tratta dell'impostazione predefinita se non viene inserito alcun videodisco.</span><span class="sxs-lookup"><span data-stu-id="d38f7-207">This is the default if no videodisc is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ GETDEVCAPS \_ CLV</span><span class="sxs-lookup"><span data-stu-id="d38f7-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI\_VD\_GETDEVCAPS\_CLV</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-209">In combinazione con altri elementi, specifica che le informazioni restituite si applicano al formato CLV videodischi.</span><span class="sxs-lookup"><span data-stu-id="d38f7-209">When combined with other items, specifies that the return information applies to CLV format videodiscs.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>\_ \_ \_ frequenza veloce GETDEVCAPS MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="d38f7-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI\_VD\_GETDEVCAPS\_FAST\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-211">Il membro **dwReturn** è impostato sulla frequenza di riproduzione veloce standard in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="d38f7-211">The **dwReturn** member is set to the standard fast play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>\_ \_ \_ frequenza normale GETDEVCAPS MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="d38f7-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI\_VD\_GETDEVCAPS\_NORMAL\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-213">Il membro **dwReturn** è impostato sulla frequenza di riproduzione normale in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="d38f7-213">The **dwReturn** member is set to the normal play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>\_ \_ \_ frequenza lenta GETDEVCAPS MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="d38f7-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>MCI\_VD\_GETDEVCAPS\_SLOW\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-215">Il membro **dwReturn** è impostato sulla frequenza di riproduzione lenta standard in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="d38f7-215">The **dwReturn** member is set to the standard slow play rate in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="d38f7-216">I flag seguenti possono essere specificati nel membro **dwItem** di [**MCI \_ GETDEVCAPS \_ parametri**](mci-getdevcaps-parms.md) per il tipo di dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="d38f7-216">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d38f7-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>\_ \_ input GETDEVCAPS Wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d38f7-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI\_WAVE\_GETDEVCAPS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-218">Il membro **dwReturn** è impostato sul numero totale di dispositivi di input della forma d'onda (registrazione).</span><span class="sxs-lookup"><span data-stu-id="d38f7-218">The **dwReturn** member is set to the total number of waveform input (recording) devices.</span></span>

</dd> <dt>

<span data-ttu-id="d38f7-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>\_ \_ output GETDEVCAPS Wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d38f7-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI\_WAVE\_GETDEVCAPS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="d38f7-220">Il membro **dwReturn** è impostato sul numero totale di dispositivi di output della forma d'onda (riproduzione).</span><span class="sxs-lookup"><span data-stu-id="d38f7-220">The **dwReturn** member is set to the total number of waveform output (playback) devices.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d38f7-221">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d38f7-221">Requirements</span></span>



| <span data-ttu-id="d38f7-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="d38f7-222">Requirement</span></span> | <span data-ttu-id="d38f7-223">Valore</span><span class="sxs-lookup"><span data-stu-id="d38f7-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d38f7-224">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d38f7-224">Minimum supported client</span></span><br/> | <span data-ttu-id="d38f7-225">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d38f7-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d38f7-226">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d38f7-226">Minimum supported server</span></span><br/> | <span data-ttu-id="d38f7-227">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d38f7-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d38f7-228">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d38f7-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="d38f7-229"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d38f7-229"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d38f7-230">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d38f7-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38f7-231">MCI</span><span class="sxs-lookup"><span data-stu-id="d38f7-231">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d38f7-232">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="d38f7-232">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

