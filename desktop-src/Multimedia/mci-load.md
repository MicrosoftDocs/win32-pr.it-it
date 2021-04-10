---
title: Comando MCI_LOAD (mmsystem. h)
description: Il \_ comando MCI Load carica un file. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- Comando MCI_LOAD Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963745"
---
# <a name="mci_load-command"></a><span data-ttu-id="cab81-105">\_Comando di caricamento MCI</span><span class="sxs-lookup"><span data-stu-id="cab81-105">MCI\_LOAD command</span></span>

<span data-ttu-id="cab81-106">Il \_ comando MCI Load carica un file.</span><span class="sxs-lookup"><span data-stu-id="cab81-106">The MCI\_LOAD command loads a file.</span></span> <span data-ttu-id="cab81-107">I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="cab81-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="cab81-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="cab81-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
);
```



## <a name="parameters"></a><span data-ttu-id="cab81-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cab81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cab81-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="cab81-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="cab81-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="cab81-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="cab81-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="cab81-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cab81-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi video digitali, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="cab81-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="cab81-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="cab81-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="cab81-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span><span class="sxs-lookup"><span data-stu-id="cab81-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span></span>
</dt> <dd>

<span data-ttu-id="cab81-116">Puntatore a una [**struttura \_ \_ parametri di caricamento MCI**](mci-load-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="cab81-116">Pointer to an [**MCI\_LOAD\_PARMS**](mci-load-parms.md) structure.</span></span> <span data-ttu-id="cab81-117">I dispositivi con parametri aggiuntivi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cab81-117">(Devices with additional parameters might replace this structure with a device-specific structure.</span></span> <span data-ttu-id="cab81-118">Per i dispositivi digitali video, il parametro **lpLoad** punta a una [**struttura \_ DGV \_ Load \_ parametri di MCI**](/previous-versions//dd743391(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cab81-118">For digital-video devices, the **lpLoad** parameter points to an [**MCI\_DGV\_LOAD\_PARMS**](/previous-versions//dd743391(v=vs.85)) structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cab81-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cab81-119">Return Value</span></span>

<span data-ttu-id="cab81-120">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="cab81-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cab81-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="cab81-121">Remarks</span></span>

<span data-ttu-id="cab81-122">Il flag aggiuntivo seguente si applica a tutti i dispositivi che supportano il \_ carico MCI:</span><span class="sxs-lookup"><span data-stu-id="cab81-122">The following additional flag applies to all devices supporting MCI\_LOAD:</span></span>

<dl> <dt>

<span data-ttu-id="cab81-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>\_file di caricamento MCI \_</span><span class="sxs-lookup"><span data-stu-id="cab81-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>MCI\_LOAD\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="cab81-124">Il membro **lpFileName** della struttura identificata da *lpLoad* contiene un indirizzo di un buffer contenente il nome del file.</span><span class="sxs-lookup"><span data-stu-id="cab81-124">The **lpfilename** member of the structure identified by *lpLoad* contains an address of a buffer containing the filename.</span></span>

</dd> </dl>

<span data-ttu-id="cab81-125">Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **overlay** :</span><span class="sxs-lookup"><span data-stu-id="cab81-125">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="cab81-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>OVLY di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="cab81-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="cab81-127">Il membro **RC** della struttura identificato da *lpLoad* contiene un rettangolo di visualizzazione valido che identifica l'area del buffer video da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="cab81-127">The **rc** member of the structure identified by *lpLoad* contains a valid display rectangle that identifies the area of the video buffer to update.</span></span>

</dd> </dl>

<span data-ttu-id="cab81-128">Per i dispositivi con sovrimpressione video, il parametro *lpLoad* punta a una struttura [**\_ OVLY \_ Load \_ parametri di MCI**](mci-ovly-load-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="cab81-128">For video-overlay devices, the *lpLoad* parameter points to an [**MCI\_OVLY\_LOAD\_PARMS**](mci-ovly-load-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cab81-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cab81-129">Requirements</span></span>



| <span data-ttu-id="cab81-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cab81-130">Requirement</span></span> | <span data-ttu-id="cab81-131">Valore</span><span class="sxs-lookup"><span data-stu-id="cab81-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cab81-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cab81-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cab81-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cab81-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cab81-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cab81-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cab81-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cab81-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cab81-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cab81-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cab81-137"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cab81-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cab81-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cab81-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab81-139">MCI</span><span class="sxs-lookup"><span data-stu-id="cab81-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cab81-140">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="cab81-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

