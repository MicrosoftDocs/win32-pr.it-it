---
title: Comando MCI_WINDOW (mmsystem. h)
description: Il \_ comando finestra MCI specifica la finestra e le caratteristiche della finestra per i dispositivi grafici. I dispositivi Digital-video e overlay video riconoscono questo comando.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- Comando MCI_WINDOW Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964366"
---
# <a name="mci_window-command"></a><span data-ttu-id="610d9-105">\_Comando finestra MCI</span><span class="sxs-lookup"><span data-stu-id="610d9-105">MCI\_WINDOW command</span></span>

<span data-ttu-id="610d9-106">Il \_ comando finestra MCI specifica la finestra e le caratteristiche della finestra per i dispositivi grafici.</span><span class="sxs-lookup"><span data-stu-id="610d9-106">The MCI\_WINDOW command specifies the window and the window characteristics for graphic devices.</span></span> <span data-ttu-id="610d9-107">I dispositivi Digital-video e overlay video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="610d9-107">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="610d9-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="610d9-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
);
```



## <a name="parameters"></a><span data-ttu-id="610d9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="610d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="610d9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="610d9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="610d9-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="610d9-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="610d9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="610d9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="610d9-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi video digitali, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="610d9-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="610d9-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="610d9-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="610d9-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span><span class="sxs-lookup"><span data-stu-id="610d9-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span></span>
</dt> <dd>

<span data-ttu-id="610d9-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="610d9-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="610d9-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="610d9-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="610d9-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="610d9-118">Return Value</span></span>

<span data-ttu-id="610d9-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="610d9-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="610d9-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="610d9-120">Remarks</span></span>

<span data-ttu-id="610d9-121">I dispositivi grafici devono creare una finestra predefinita quando un dispositivo viene aperto, ma non deve visualizzarlo fino a quando non riceve il comando [MCI \_ Play](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="610d9-121">Graphic devices should create a default window when a device is opened but should not display it until they receive the [MCI\_PLAY](mci-play.md) command.</span></span> <span data-ttu-id="610d9-122">Il \_ comando della finestra MCI viene usato per fornire al dispositivo una finestra creata dall'applicazione e per modificare le caratteristiche di visualizzazione di una finestra di visualizzazione predefinita o definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="610d9-122">The MCI\_WINDOW command is used to supply an application-created window to the device and to change the display characteristics of an application-defined or default display window.</span></span> <span data-ttu-id="610d9-123">Se l'applicazione fornisce la finestra di visualizzazione, dovrebbe essere preparata ad aggiornare un rettangolo non valido nella finestra.</span><span class="sxs-lookup"><span data-stu-id="610d9-123">If the application supplies the display window, it should be prepared to update an invalid rectangle on the window.</span></span>

<span data-ttu-id="610d9-124">Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="610d9-124">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="610d9-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>\_ \_ HWND finestra DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="610d9-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI\_DGV\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="610d9-126">L'handle della finestra necessaria per l'utilizzo come destinazione è incluso nel membro **HWND** della struttura identificata da *lpWindow*.</span><span class="sxs-lookup"><span data-stu-id="610d9-126">The handle of the window needed for use as the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span>

</dd> <dt>

<span data-ttu-id="610d9-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>\_stato della \_ finestra \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="610d9-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>MCI\_DGV\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="610d9-128">Il membro **nCmdShow** della struttura identificata da *lpWindow* contiene i parametri per l'impostazione dello stato della finestra.</span><span class="sxs-lookup"><span data-stu-id="610d9-128">The **nCmdShow** member of the structure identified by *lpWindow* contains parameters for setting the window state.</span></span>

</dd> <dt>

<span data-ttu-id="610d9-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>\_ \_ testo finestra DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="610d9-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI\_DGV\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="610d9-130">Il membro **lpstrText** della struttura identificata da *lpWindow* contiene un indirizzo di un buffer contenente la didascalia usata nella barra del titolo della finestra.</span><span class="sxs-lookup"><span data-stu-id="610d9-130">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used in the window title bar.</span></span>

</dd> </dl>

<span data-ttu-id="610d9-131">Per i dispositivi digitali video, il parametro *lpWindow* punta a una struttura [**DGV della \_ \_ finestra \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="610d9-131">For digital-video devices, the *lpWindow* parameter points to an [**MCI\_DGV\_WINDOW\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) structure.</span></span>

<span data-ttu-id="610d9-132">Con il tipo di dispositivo **overlay** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="610d9-132">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="610d9-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>\_ \_ \_ disabilitazione dell' \_ estensione OVLY della finestra MCI</span><span class="sxs-lookup"><span data-stu-id="610d9-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI\_OVLY\_WINDOW\_DISABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="610d9-134">Disabilita l'allungamento dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="610d9-134">Disables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="610d9-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>\_ \_ \_ Abilita stretch per la finestra OVLY di MCI \_</span><span class="sxs-lookup"><span data-stu-id="610d9-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI\_OVLY\_WINDOW\_ENABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="610d9-136">Abilita l'allungamento dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="610d9-136">Enables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="610d9-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>\_ \_ HWND finestra OVLY \_ MCI</span><span class="sxs-lookup"><span data-stu-id="610d9-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI\_OVLY\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="610d9-138">L'handle della finestra utilizzata per la destinazione è incluso nel membro **HWND** della struttura identificata da *lpWindow*.</span><span class="sxs-lookup"><span data-stu-id="610d9-138">The handle of the window used for the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span> <span data-ttu-id="610d9-139">Impostare questo flag su MCI \_ OVLY \_ Window \_ default per tornare alla finestra predefinita.</span><span class="sxs-lookup"><span data-stu-id="610d9-139">Set this flag to MCI\_OVLY\_WINDOW\_DEFAULT to return to the default window.</span></span>

</dd> <dt>

<span data-ttu-id="610d9-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>\_stato della \_ finestra \_ OVLY MCI</span><span class="sxs-lookup"><span data-stu-id="610d9-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>MCI\_OVLY\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="610d9-141">Il membro **nCmdShow** della struttura *lpWindow* contiene i parametri per l'impostazione dello stato della finestra.</span><span class="sxs-lookup"><span data-stu-id="610d9-141">The **nCmdShow** member of the *lpWindow* structure contains parameters for setting the window state.</span></span> <span data-ttu-id="610d9-142">Questo flag equivale a chiamare [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) con il parametro *state* .</span><span class="sxs-lookup"><span data-stu-id="610d9-142">This flag is equivalent to calling [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) with the *state* parameter.</span></span> <span data-ttu-id="610d9-143">Le costanti sono le stesse definite in WINDOWS. H (ad esempio \_ , Hide SW, SW \_ Riduci a icona o SW \_ SHOWNORMAL).</span><span class="sxs-lookup"><span data-stu-id="610d9-143">The constants are the same as those defined in WINDOWS.H (such as SW\_HIDE, SW\_MINIMIZE, or SW\_SHOWNORMAL).</span></span>

</dd> <dt>

<span data-ttu-id="610d9-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>\_ \_ testo finestra OVLY \_ MCI</span><span class="sxs-lookup"><span data-stu-id="610d9-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>MCI\_OVLY\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="610d9-145">Il membro **lpstrText** della struttura identificata da *lpWindow* contiene un indirizzo di un buffer contenente la didascalia utilizzata per la finestra.</span><span class="sxs-lookup"><span data-stu-id="610d9-145">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used for the window.</span></span>

</dd> </dl>

<span data-ttu-id="610d9-146">Per i dispositivi con sovrimpressione video, il parametro *lpWindow* punta a una struttura [**OVLY della \_ \_ finestra \_ parametri di MCI**](mci-ovly-window-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="610d9-146">For video-overlay devices, the *lpWindow* parameter points to an [**MCI\_OVLY\_WINDOW\_PARMS**](mci-ovly-window-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="610d9-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="610d9-147">Requirements</span></span>



| <span data-ttu-id="610d9-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="610d9-148">Requirement</span></span> | <span data-ttu-id="610d9-149">Valore</span><span class="sxs-lookup"><span data-stu-id="610d9-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="610d9-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="610d9-150">Minimum supported client</span></span><br/> | <span data-ttu-id="610d9-151">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="610d9-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="610d9-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="610d9-152">Minimum supported server</span></span><br/> | <span data-ttu-id="610d9-153">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="610d9-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="610d9-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="610d9-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="610d9-155"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="610d9-155"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="610d9-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="610d9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="610d9-157">MCI</span><span class="sxs-lookup"><span data-stu-id="610d9-157">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="610d9-158">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="610d9-158">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

