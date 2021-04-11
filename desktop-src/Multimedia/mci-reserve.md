---
title: Comando MCI_RESERVE (mmsystem. h)
description: Il \_ comando MCI Reserve alloca spazio su disco contiguo per l'area di lavoro dell'istanza del driver di dispositivo da usare con la registrazione successiva. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- Comando MCI_RESERVE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964686"
---
# <a name="mci_reserve-command"></a><span data-ttu-id="2223c-105">\_Comando di riserva MCI</span><span class="sxs-lookup"><span data-stu-id="2223c-105">MCI\_RESERVE command</span></span>

<span data-ttu-id="2223c-106">Il \_ comando MCI Reserve alloca spazio su disco contiguo per l'area di lavoro dell'istanza del driver di dispositivo da usare con la registrazione successiva.</span><span class="sxs-lookup"><span data-stu-id="2223c-106">The MCI\_RESERVE command allocates contiguous disk space for the workspace of the device driver instance for use with subsequent recording.</span></span> <span data-ttu-id="2223c-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="2223c-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="2223c-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="2223c-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
);
```



## <a name="parameters"></a><span data-ttu-id="2223c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2223c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2223c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2223c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2223c-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="2223c-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2223c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2223c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2223c-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="2223c-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="2223c-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2223c-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2223c-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span><span class="sxs-lookup"><span data-stu-id="2223c-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span></span>
</dt> <dd>

<span data-ttu-id="2223c-116">Puntatore a una [**struttura \_ \_ \_ parametri della riserva DGV di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="2223c-116">Pointer to an [**MCI\_DGV\_RESERVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2223c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2223c-117">Return Value</span></span>

<span data-ttu-id="2223c-118">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="2223c-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2223c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2223c-119">Remarks</span></span>

<span data-ttu-id="2223c-120">Se l'area di lavoro contiene dati non salvati, i dati andranno perduti.</span><span class="sxs-lookup"><span data-stu-id="2223c-120">If the workspace contains unsaved data, this data is lost.</span></span> <span data-ttu-id="2223c-121">Se lo spazio su disco non è riservato prima della registrazione, il comando [MCI \_ record](mci-record.md) esegue una riserva implicita con parametri predefiniti specifici del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2223c-121">If disk space is not reserved prior to recording, the [MCI\_RECORD](mci-record.md) command performs an implied reserve with device-specific default parameters.</span></span> <span data-ttu-id="2223c-122">In alcune implementazioni, Reserve non è obbligatorio e potrebbe essere ignorato dal driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2223c-122">On some implementations, reserve is not required and might be ignored by the device driver.</span></span> <span data-ttu-id="2223c-123">Il mantenimento dello spazio in modo esplicito garantisce un maggiore controllo sul momento in cui si verifica il ritardo nell'allocazione dei dischi, sulla quantità di spazio allocato e sulla posizione di allocazione dello spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="2223c-123">Explicitly reserving space gives you better control over when the delay for disk allocation occurs, how much space is allocated, and where the disk space is allocated.</span></span> <span data-ttu-id="2223c-124">La quantità e la posizione dello spazio su disco già riservata per questa istanza del dispositivo possono essere modificate rilasciando la riserva di MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="2223c-124">The amount and location of disk space already reserved for this device instance can be changed by issuing MCI\_RESERVE again.</span></span> <span data-ttu-id="2223c-125">Qualsiasi spazio su disco allocato e ancora inutilizzato non viene deallocato fino al salvataggio dei dati registrati o fino alla chiusura dell'istanza del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2223c-125">Any allocated and still unused disk space is not deallocated until any recorded data is saved or until the device driver instance is closed.</span></span>

<span data-ttu-id="2223c-126">Se il video è disattivato con il \_ flag MCI off del comando [MCI \_ sevideo](mci-setvideo.md) , lo spazio riservato non include alcun video.</span><span class="sxs-lookup"><span data-stu-id="2223c-126">If video is turned off with the MCI\_OFF flag of the [MCI\_SETVIDEO](mci-setvideo.md) command, the space reserved does not include any video.</span></span> <span data-ttu-id="2223c-127">Se l'audio è disattivato con il \_ flag MCI off del comando [MCI \_ sefonica](mci-setaudio.md) , lo spazio riservato non include alcun audio.</span><span class="sxs-lookup"><span data-stu-id="2223c-127">If audio is turned off with the MCI\_OFF flag of the [MCI\_SETAUDIO](mci-setaudio.md) command, the space reserved does not include any audio.</span></span> <span data-ttu-id="2223c-128">Se l'audio e il video sono spenti o se le dimensioni richieste sono pari a zero, nessuno spazio viene riservato e lo spazio riservato esistente viene deallocato.</span><span class="sxs-lookup"><span data-stu-id="2223c-128">If both audio and video are turned off or if the requested size is zero, no space is reserved and any existing reserved space is deallocated.</span></span>

<span data-ttu-id="2223c-129">I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:</span><span class="sxs-lookup"><span data-stu-id="2223c-129">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="2223c-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>\_riserva DGV \_ MCI \_ in</span><span class="sxs-lookup"><span data-stu-id="2223c-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI\_DGV\_RESERVE\_IN</span></span>
</dt> <dd>

<span data-ttu-id="2223c-131">Il membro **lpstrPath** della struttura identificata da *lpReserve* contiene un indirizzo di un buffer contenente il percorso di un file temporaneo.</span><span class="sxs-lookup"><span data-stu-id="2223c-131">The **lpstrPath** member of the structure identified by *lpReserve* contains an address of a buffer containing the location of a temporary file.</span></span> <span data-ttu-id="2223c-132">Il buffer contiene solo l'unità e il percorso della directory del file utilizzato per contenere i dati registrati. il nome file viene specificato dal driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2223c-132">The buffer contains only the drive and directory path of the file used to hold recorded data; the filename is specified by the device driver.</span></span> <span data-ttu-id="2223c-133">Questo file temporaneo viene eliminato quando l'istanza del dispositivo viene chiusa, a meno che non venga salvata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="2223c-133">This temporary file is deleted when the device instance is closed unless it is explicitly saved.</span></span> <span data-ttu-id="2223c-134">Se questo flag viene omesso, il driver di dispositivo specifica la posizione in cui è allocato lo spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="2223c-134">If this flag is omitted, the device driver specifies where disk space is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="2223c-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>\_ \_ dimensioni riserva DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="2223c-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI\_DGV\_RESERVE\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="2223c-136">Il membro **dwSize** della struttura identificata da *lpReserve* specifica la quantità approssimativa di spazio su disco da riservare nell'area di lavoro per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="2223c-136">The **dwSize** member of the structure identified by *lpReserve* specifies the approximate amount of disk space to reserve in the workspace for recording.</span></span> <span data-ttu-id="2223c-137">Il valore viene specificato nel formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="2223c-137">The value is specified in the current time format.</span></span> <span data-ttu-id="2223c-138">La quantità di spazio su disco è stimata dal tempo richiesto e da quali formati di file e algoritmi video e audio e valori di qualità sono attivi.</span><span class="sxs-lookup"><span data-stu-id="2223c-138">The amount of disk space is estimated from the requested time and from which file format and video and audio algorithm and quality values are in effect.</span></span> <span data-ttu-id="2223c-139">Se questo flag viene omesso, è possibile che il driver di dispositivo usi un valore predefinito che definisce.</span><span class="sxs-lookup"><span data-stu-id="2223c-139">If this flag is omitted, the device driver might use a default value it defines.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2223c-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2223c-140">Requirements</span></span>



| <span data-ttu-id="2223c-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2223c-141">Requirement</span></span> | <span data-ttu-id="2223c-142">Valore</span><span class="sxs-lookup"><span data-stu-id="2223c-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2223c-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2223c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2223c-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2223c-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2223c-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2223c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2223c-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2223c-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2223c-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2223c-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="2223c-148"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2223c-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2223c-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2223c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2223c-150">MCI</span><span class="sxs-lookup"><span data-stu-id="2223c-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2223c-151">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="2223c-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

