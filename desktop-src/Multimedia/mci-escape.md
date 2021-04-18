---
title: Comando MCI_ESCAPE (mmsystem. h)
description: Il \_ comando di escape MCI invia una stringa direttamente al dispositivo. I dispositivi videodisco riconoscono questo comando.
ms.assetid: 56ebc717-f0f7-4612-8e51-57b13ff9d42b
keywords:
- Comando MCI_ESCAPE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_ESCAPE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4bcd55590cb1b2cab5482eeb921118531002c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301758"
---
# <a name="mci_escape-command"></a><span data-ttu-id="d5bb8-105">\_Comando di escape MCI</span><span class="sxs-lookup"><span data-stu-id="d5bb8-105">MCI\_ESCAPE command</span></span>

<span data-ttu-id="d5bb8-106">Il \_ comando di escape MCI invia una stringa direttamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-106">The MCI\_ESCAPE command sends a string directly to the device.</span></span> <span data-ttu-id="d5bb8-107">I dispositivi videodisco riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="d5bb8-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_ESCAPE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_VD_ESCAPE_PARMS) lpEscape
);
```



## <a name="parameters"></a><span data-ttu-id="d5bb8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5bb8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5bb8-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d5bb8-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d5bb8-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d5bb8-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d5bb8-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d5bb8-113">\_Attesa notifica MCI o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d5bb8-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="d5bb8-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d5bb8-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5bb8-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span><span class="sxs-lookup"><span data-stu-id="d5bb8-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span></span>
</dt> <dd>

<span data-ttu-id="d5bb8-116">Puntatore a una [**struttura \_ \_ \_ parametri di escape MCI VD**](mci-vd-escape-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d5bb8-116">Pointer to an [**MCI\_VD\_ESCAPE\_PARMS**](mci-vd-escape-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5bb8-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5bb8-117">Return Value</span></span>

<span data-ttu-id="d5bb8-118">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5bb8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5bb8-119">Remarks</span></span>

<span data-ttu-id="d5bb8-120">I dati inviati con l' \_ escape MCI sono dipendenti dal dispositivo e vengono in genere passati direttamente all'hardware associato al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-120">The data sent with MCI\_ESCAPE is device-dependent and is usually passed directly to the hardware associated with the device.</span></span>

<span data-ttu-id="d5bb8-121">Il flag aggiuntivo seguente si applica ai dispositivi videodisco:</span><span class="sxs-lookup"><span data-stu-id="d5bb8-121">The following additional flag applies to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="d5bb8-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>\_stringa di \_ escape MCI VD \_</span><span class="sxs-lookup"><span data-stu-id="d5bb8-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>MCI\_VD\_ESCAPE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="d5bb8-123">Una stringa di comando viene specificata nel membro **lpstrCommand** della struttura identificata da *lpEscape*.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-123">A command string is specified in the **lpstrCommand** member of the structure identified by *lpEscape*.</span></span> <span data-ttu-id="d5bb8-124">Questo flag è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-124">This flag is required.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5bb8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5bb8-125">Requirements</span></span>



| <span data-ttu-id="d5bb8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5bb8-126">Requirement</span></span> | <span data-ttu-id="d5bb8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d5bb8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5bb8-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5bb8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d5bb8-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d5bb8-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d5bb8-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5bb8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d5bb8-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d5bb8-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d5bb8-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5bb8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5bb8-133"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5bb8-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5bb8-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5bb8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5bb8-135">MCI</span><span class="sxs-lookup"><span data-stu-id="d5bb8-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d5bb8-136">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="d5bb8-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

