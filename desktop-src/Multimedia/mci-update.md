---
title: Comando MCI_UPDATE (mmsystem. h)
description: Il \_ comando di aggiornamento MCI Aggiorna il rettangolo di visualizzazione. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- Comando MCI_UPDATE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121258"
---
# <a name="mci_update-command"></a><span data-ttu-id="8cf4d-105">\_Comando di aggiornamento MCI</span><span class="sxs-lookup"><span data-stu-id="8cf4d-105">MCI\_UPDATE command</span></span>

<span data-ttu-id="8cf4d-106">Il \_ comando di aggiornamento MCI Aggiorna il rettangolo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-106">The MCI\_UPDATE command updates the display rectangle.</span></span> <span data-ttu-id="8cf4d-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="8cf4d-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="8cf4d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8cf4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf4d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8cf4d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8cf4d-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="8cf4d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8cf4d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8cf4d-113">**MCI \_ NOTIFICA**, **MCI \_ wait** o, per i dispositivi video digitali, **MCI \_ test**.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="8cf4d-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8cf4d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cf4d-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span><span class="sxs-lookup"><span data-stu-id="8cf4d-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="8cf4d-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="8cf4d-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="8cf4d-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cf4d-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8cf4d-118">Return Value</span></span>

<span data-ttu-id="8cf4d-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cf4d-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="8cf4d-120">Remarks</span></span>

<span data-ttu-id="8cf4d-121">Con il tipo di dispositivo "digitalvideo" vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cf4d-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="8cf4d-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>\_ \_ aggiornamento HDC DGV \_ di MCI</span><span class="sxs-lookup"><span data-stu-id="8cf4d-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI\_DGV\_UPDATE\_HDC</span></span>
</dt> <dd>

<span data-ttu-id="8cf4d-123">Il membro **HDC** della struttura identificato da *lpDest* contiene una finestra valida del controller di dominio da disegnare.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-123">The **hDC** member of the structure identified by *lpDest* contains a valid window of the DC to paint.</span></span> <span data-ttu-id="8cf4d-124">Questo flag è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-124">This flag is required.</span></span>

</dd> <dt>

<span data-ttu-id="8cf4d-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>DGV di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="8cf4d-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="8cf4d-126">Il membro **RC** della struttura identificato da *lpUnfreeze* contiene un rettangolo di visualizzazione valido.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-126">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="8cf4d-127">Il rettangolo specifica il rettangolo di ridimensionamento rispetto al rettangolo client.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-127">The rectangle specifies the clipping rectangle relative to the client rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="8cf4d-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>\_ \_ disegno aggiornamento DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="8cf4d-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI\_DGV\_UPDATE\_PAINT</span></span>
</dt> <dd>

<span data-ttu-id="8cf4d-129">Un'applicazione utilizza questo flag quando riceve un messaggio [**di \_ disegno WM**](/windows/desktop/gdi/wm-paint) destinato a un controller di dominio di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-129">An application uses this flag when it receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message that is intended for a display DC.</span></span> <span data-ttu-id="8cf4d-130">Un dispositivo buffer frame in genere disegna il colore della chiave.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-130">A frame-buffer device usually paints the key color.</span></span> <span data-ttu-id="8cf4d-131">Se il dispositivo di visualizzazione non dispone di un buffer di frame, potrebbe ignorare il \_ comando di aggiornamento MCI quando viene usato il flag di **\_ \_ \_ disegno dell'aggiornamento DGV di MCI** , perché la visualizzazione verrà ridisegnata durante l'operazione di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-131">If the display device does not have a frame buffer, it might ignore the MCI\_UPDATE command when the **MCI\_DGV\_UPDATE\_PAINT** flag is used because the display will be repainted during the playback operation.</span></span>

</dd> </dl>

<span data-ttu-id="8cf4d-132">Per i dispositivi digitali video, il parametro *lpDest* punta a una [**struttura \_ DGV \_ Update \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) .</span><span class="sxs-lookup"><span data-stu-id="8cf4d-132">For digital-video devices, the *lpDest* parameter points to an [**MCI\_DGV\_UPDATE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf4d-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8cf4d-133">Requirements</span></span>



| <span data-ttu-id="8cf4d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cf4d-134">Requirement</span></span> | <span data-ttu-id="8cf4d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="8cf4d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf4d-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cf4d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf4d-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8cf4d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8cf4d-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cf4d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf4d-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8cf4d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8cf4d-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8cf4d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cf4d-141"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8cf4d-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cf4d-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cf4d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf4d-143">MCI</span><span class="sxs-lookup"><span data-stu-id="8cf4d-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8cf4d-144">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="8cf4d-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

