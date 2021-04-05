---
title: Comando MCI_OPEN (mmsystem. h)
description: Il \_ comando MCI Open Inizializza un dispositivo o un file. Tutti i dispositivi riconoscono questo comando.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- Comando MCI_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873273"
---
# <a name="mci_open-command"></a><span data-ttu-id="52166-105">\_Comando di apertura MCI</span><span class="sxs-lookup"><span data-stu-id="52166-105">MCI\_OPEN command</span></span>

<span data-ttu-id="52166-106">Il \_ comando MCI Open Inizializza un dispositivo o un file.</span><span class="sxs-lookup"><span data-stu-id="52166-106">The MCI\_OPEN command initializes a device or file.</span></span> <span data-ttu-id="52166-107">Tutti i dispositivi riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="52166-107">All devices recognize this command.</span></span>

<span data-ttu-id="52166-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="52166-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
);
```



## <a name="parameters"></a><span data-ttu-id="52166-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="52166-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52166-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="52166-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="52166-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="52166-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="52166-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="52166-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="52166-113">\_Attesa notifica MCI o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="52166-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="52166-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="52166-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="52166-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span><span class="sxs-lookup"><span data-stu-id="52166-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span></span>
</dt> <dd>

<span data-ttu-id="52166-116">Puntatore a una [**struttura \_ \_ parametri aperta di MCI**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="52166-116">Pointer to an [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span> <span data-ttu-id="52166-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="52166-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52166-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52166-118">Return Value</span></span>

<span data-ttu-id="52166-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="52166-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="52166-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="52166-120">Remarks</span></span>

<span data-ttu-id="52166-121">Il \_ \_ flag di tipo di apertura MCI deve essere usato ogni volta che un dispositivo viene specificato nella funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="52166-121">The MCI\_OPEN\_TYPE flag must be used whenever a device is specified in the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="52166-122">Se si apre un dispositivo specificando una costante del tipo di dispositivo, è necessario specificare il \_ \_ flag ID tipo aperto MCI \_ oltre al \_ tipo di apertura MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="52166-122">If you open a device by specifying a device-type constant, you must specify the MCI\_OPEN\_TYPE\_ID flag in addition to MCI\_OPEN\_TYPE.</span></span> <span data-ttu-id="52166-123">Per un elenco di costanti di tipo dispositivo, vedere [tipi di dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="52166-123">For a list of device-type constants, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="52166-124">Se il \_ \_ flag di condivisione Open di MCI non viene specificato quando un dispositivo o un file viene aperto inizialmente, tutti i \_ comandi di apertura di MCI successivi al dispositivo o al file avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="52166-124">If the MCI\_OPEN\_SHAREABLE flag is not specified when a device or file is initially opened, all subsequent MCI\_OPEN commands to the device or file will fail.</span></span> <span data-ttu-id="52166-125">Se il dispositivo o il file è già aperto e questo flag non è specificato, la chiamata avrà esito negativo anche se il primo comando aperto specificato MCI \_ Open \_ Shareable.</span><span class="sxs-lookup"><span data-stu-id="52166-125">If the device or file is already open and this flag is not specified, the call will fail even if the first open command specified MCI\_OPEN\_SHAREABLE.</span></span> <span data-ttu-id="52166-126">File aperti per MCISEQ. DRV e MCIWAVE. I dispositivi DRV non sono condivisibili.</span><span class="sxs-lookup"><span data-stu-id="52166-126">Files opened for the MCISEQ.DRV and MCIWAVE.DRV devices are nonsharable.</span></span>

<span data-ttu-id="52166-127">Il caso viene ignorato nel nome del dispositivo, ma non possono essere presenti spazi vuoti iniziali o finali.</span><span class="sxs-lookup"><span data-stu-id="52166-127">Case is ignored in the device name, but there cannot be leading or trailing blanks.</span></span>

<span data-ttu-id="52166-128">Per usare la selezione automatica dei tipi (tramite le voci nel registro di sistema), assegnare il nome file e l'estensione del file al membro **lpstrElementName** della struttura identificata da *lpOpen*, impostare il membro **lpstrDeviceType** su **null** e impostare il flag di elemento di \_ apertura MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="52166-128">To use automatic type selection (via the entries in the registry), assign the filename and file extension to the **lpstrElementName** member of the structure identified by *lpOpen*, set the **lpstrDeviceType** member to **NULL**, and set the MCI\_OPEN\_ELEMENT flag.</span></span>

<span data-ttu-id="52166-129">I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano MCI \_ Open:</span><span class="sxs-lookup"><span data-stu-id="52166-129">The following additional flags apply to all devices supporting MCI\_OPEN:</span></span>

<dl> <dt>

<span data-ttu-id="52166-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>\_alias di apertura MCI \_</span><span class="sxs-lookup"><span data-stu-id="52166-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI\_OPEN\_ALIAS</span></span>
</dt> <dd>

<span data-ttu-id="52166-131">Un alias è incluso nel membro **lpstrAlias** della struttura identificata da *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="52166-131">An alias is included in the **lpstrAlias** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="52166-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>\_ \_ condivisibile aperto MCI</span><span class="sxs-lookup"><span data-stu-id="52166-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI\_OPEN\_SHAREABLE</span></span>
</dt> <dd>

<span data-ttu-id="52166-133">Il dispositivo o il file deve essere aperto come condivisibile.</span><span class="sxs-lookup"><span data-stu-id="52166-133">The device or file should be opened as sharable.</span></span>

</dd> <dt>

<span data-ttu-id="52166-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>\_tipo di apertura MCI \_</span><span class="sxs-lookup"><span data-stu-id="52166-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI\_OPEN\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="52166-135">Un nome o una costante del tipo di dispositivo è incluso nel membro **lpstrDeviceType** della struttura identificata da *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="52166-135">A device type name or constant is included in the **lpstrDeviceType** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="52166-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>\_ \_ ID tipo aperto \_ MCI</span><span class="sxs-lookup"><span data-stu-id="52166-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI\_OPEN\_TYPE\_ID</span></span>
</dt> <dd>

<span data-ttu-id="52166-137">La parola meno significativa del membro **lpstrDeviceType** della struttura identificata da *lpOpen* contiene un identificatore del tipo di dispositivo MCI standard e la parola più significativa, facoltativamente, contiene l'indice ordinale per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="52166-137">The low-order word of the **lpstrDeviceType** member of the structure identified by *lpOpen* contains a standard MCI device type identifier and the high-order word optionally contains the ordinal index for the device.</span></span> <span data-ttu-id="52166-138">Utilizzare questo flag con il \_ flag di \_ tipo aperto MCI.</span><span class="sxs-lookup"><span data-stu-id="52166-138">Use this flag with the MCI\_OPEN\_TYPE flag.</span></span>

</dd> </dl>

<span data-ttu-id="52166-139">I flag aggiuntivi seguenti si applicano ai dispositivi composti:</span><span class="sxs-lookup"><span data-stu-id="52166-139">The following additional flags apply to compound devices:</span></span>

<dl> <dt>

<span data-ttu-id="52166-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>\_elemento Open di MCI \_</span><span class="sxs-lookup"><span data-stu-id="52166-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI\_OPEN\_ELEMENT</span></span>
</dt> <dd>

<span data-ttu-id="52166-141">Un nome file è incluso nel membro **lpstrElementName** della struttura identificata da *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="52166-141">A filename is included in the **lpstrElementName** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="52166-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>\_ \_ ID elemento aperto \_ MCI</span><span class="sxs-lookup"><span data-stu-id="52166-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI\_OPEN\_ELEMENT\_ID</span></span>
</dt> <dd>

<span data-ttu-id="52166-143">Il membro **lpstrElementName** della struttura identificata da *lpOpen* viene interpretato come valore **DWORD** e ha un significato interno al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="52166-143">The **lpstrElementName** member of the structure identified by *lpOpen* is interpreted as a **DWORD** value and has meaning internal to the device.</span></span> <span data-ttu-id="52166-144">Utilizzare questo flag con il \_ flag di \_ elemento aperto MCI.</span><span class="sxs-lookup"><span data-stu-id="52166-144">Use this flag with the MCI\_OPEN\_ELEMENT flag.</span></span>

</dd> </dl>

<span data-ttu-id="52166-145">Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="52166-145">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="52166-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>\_DGV MCI \_ aperto \_ Nostatic</span><span class="sxs-lookup"><span data-stu-id="52166-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI\_DGV\_OPEN\_NOSTATIC</span></span>
</dt> <dd>

<span data-ttu-id="52166-147">Il dispositivo deve ridurre il numero di colori statici (di sistema) nella tavolozza.</span><span class="sxs-lookup"><span data-stu-id="52166-147">The device should reduce the number of static (system) colors in the palette.</span></span> <span data-ttu-id="52166-148">Questo aumenta il numero di colori disponibili per il rendering del flusso video.</span><span class="sxs-lookup"><span data-stu-id="52166-148">This increases the number of colors available for rendering the video stream.</span></span> <span data-ttu-id="52166-149">Questo flag si applica solo ai dispositivi che condividono una tavolozza con Windows.</span><span class="sxs-lookup"><span data-stu-id="52166-149">This flag applies only to devices that share a palette with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="52166-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>\_DGV \_ padre aperto \_ MCI</span><span class="sxs-lookup"><span data-stu-id="52166-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI\_DGV\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="52166-151">L'handle della finestra padre viene specificato nel membro **hwndParent** della struttura identificata da *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="52166-151">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="52166-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>\_DGV MCI \_ aperto \_ WS</span><span class="sxs-lookup"><span data-stu-id="52166-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI\_DGV\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="52166-153">Uno stile della finestra viene specificato nel membro **dwStyle** della struttura identificata da *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="52166-153">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="52166-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>DGV di MCI \_ \_ aperto \_ 16 bit</span><span class="sxs-lookup"><span data-stu-id="52166-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI\_DGV\_OPEN\_16BIT</span></span>
</dt> <dd>

<span data-ttu-id="52166-155">Indica una preferenza per il supporto dei dispositivi MCI a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="52166-155">Indicates a preference for 16-bit MCI device support.</span></span>

</dd> <dt>

<span data-ttu-id="52166-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>\_DGV MCI \_ aperto a \_ 32 bit</span><span class="sxs-lookup"><span data-stu-id="52166-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI\_DGV\_OPEN\_32BIT</span></span>
</dt> <dd>

<span data-ttu-id="52166-157">Indica una preferenza per il supporto dei dispositivi MCI a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="52166-157">Indicates a preference for 32-bit MCI device support.</span></span>

</dd> </dl>

<span data-ttu-id="52166-158">Per i dispositivi digitali video, il parametro *lpOpen* punta a una [**struttura \_ DGV \_ Open \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="52166-158">For digital-video devices, the *lpOpen* parameter points to an [**MCI\_DGV\_OPEN\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) structure.</span></span>

<span data-ttu-id="52166-159">Con il tipo di dispositivo **overlay** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="52166-159">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="52166-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>\_OVLY \_ padre aperto \_ MCI</span><span class="sxs-lookup"><span data-stu-id="52166-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI\_OVLY\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="52166-161">L'handle della finestra padre viene specificato nel membro **hwndParent** della struttura identificata da *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="52166-161">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="52166-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>\_OVLY MCI \_ aperto \_ WS</span><span class="sxs-lookup"><span data-stu-id="52166-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI\_OVLY\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="52166-163">Uno stile della finestra viene specificato nel membro **dwStyle** della struttura identificata da *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="52166-163">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span> <span data-ttu-id="52166-164">Il valore **dwStyle** specifica lo stile della finestra che il driver creerà e visualizzerà se l'applicazione non ne fornisce uno.</span><span class="sxs-lookup"><span data-stu-id="52166-164">The **dwStyle** value specifies the style of the window that the driver will create and display if the application does not provide one.</span></span> <span data-ttu-id="52166-165">Il parametro style accetta un intero che definisce lo stile della finestra.</span><span class="sxs-lookup"><span data-stu-id="52166-165">The style parameter takes an integer that defines the window style.</span></span> <span data-ttu-id="52166-166">Queste costanti sono le stesse degli stili della finestra standard (ad esempio WS \_ child, WS \_ OVERLAPPEDWINDOW o WS \_ popup).</span><span class="sxs-lookup"><span data-stu-id="52166-166">These constants are the same as the standard window styles (such as WS\_CHILD, WS\_OVERLAPPEDWINDOW, or WS\_POPUP).</span></span>

</dd> </dl>

<span data-ttu-id="52166-167">Per i dispositivi con sovrimpressione video, il parametro *lpOpen* punta a una struttura [**\_ OVLY \_ Open \_ parametri di MCI**](mci-ovly-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="52166-167">For video-overlay devices, the *lpOpen* parameter points to an [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md) structure.</span></span>

<span data-ttu-id="52166-168">Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="52166-168">The following additional flag is used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="52166-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>\_buffer di \_ apertura \_ Wave MCI</span><span class="sxs-lookup"><span data-stu-id="52166-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI\_WAVE\_OPEN\_BUFFER</span></span>
</dt> <dd>

<span data-ttu-id="52166-170">Viene specificata una lunghezza del buffer nel membro **dwBufferSeconds** della struttura identificata da *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="52166-170">A buffer length is specified in the **dwBufferSeconds** member of the structure identified by *lpOpen*.</span></span>

</dd> </dl>

<span data-ttu-id="52166-171">Per i dispositivi Waveform-Audio, il parametro *lpOpen* punta a una struttura [**\_ \_ \_ parametri Wave Open di MCI**](mci-wave-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="52166-171">For waveform-audio devices, the *lpOpen* parameter points to an [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) structure.</span></span> <span data-ttu-id="52166-172">Il driver MCIWAVE richiede un dispositivo audio e una forma d'onda asincrona.</span><span class="sxs-lookup"><span data-stu-id="52166-172">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="52166-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52166-173">Requirements</span></span>



| <span data-ttu-id="52166-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="52166-174">Requirement</span></span> | <span data-ttu-id="52166-175">Valore</span><span class="sxs-lookup"><span data-stu-id="52166-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52166-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52166-176">Minimum supported client</span></span><br/> | <span data-ttu-id="52166-177">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="52166-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="52166-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52166-178">Minimum supported server</span></span><br/> | <span data-ttu-id="52166-179">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="52166-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="52166-180">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52166-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="52166-181"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52166-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52166-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52166-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52166-183">MCI</span><span class="sxs-lookup"><span data-stu-id="52166-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="52166-184">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="52166-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

