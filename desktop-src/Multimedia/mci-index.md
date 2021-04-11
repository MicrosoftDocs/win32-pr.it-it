---
title: Comando MCI_INDEX (mmsystem. h)
description: Il \_ comando MCI index attiva o disattiva la visualizzazione sullo schermo. I dispositivi VCR riconoscono questo comando.
ms.assetid: c0f18f28-3578-4648-9b75-2d3ede68b3df
keywords:
- Comando MCI_INDEX Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_INDEX
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e93890b8c3db1150bc7224b0fd8b6ee7475ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121454"
---
# <a name="mci_index-command"></a><span data-ttu-id="2f751-105">\_Comando di indice MCI</span><span class="sxs-lookup"><span data-stu-id="2f751-105">MCI\_INDEX command</span></span>

<span data-ttu-id="2f751-106">Il \_ comando MCI index attiva o disattiva la visualizzazione sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="2f751-106">The MCI\_INDEX command turns the on-screen display on or off.</span></span> <span data-ttu-id="2f751-107">I dispositivi VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="2f751-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="2f751-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="2f751-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INDEX, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpIndex
);
```



## <a name="parameters"></a><span data-ttu-id="2f751-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f751-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f751-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2f751-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2f751-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="2f751-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2f751-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2f751-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2f751-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="2f751-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="2f751-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2f751-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f751-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span><span class="sxs-lookup"><span data-stu-id="2f751-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span></span>
</dt> <dd>

<span data-ttu-id="2f751-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="2f751-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="2f751-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f751-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f751-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f751-118">Return Value</span></span>

<span data-ttu-id="2f751-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="2f751-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f751-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f751-120">Remarks</span></span>

<span data-ttu-id="2f751-121">Le informazioni visualizzate nella schermata sullo schermo sono controllate dal \_ flag MCI VCR \_ set \_ index nel comando [ \_ set di MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="2f751-121">The information presented in the on-screen display is controlled by the MCI\_VCR\_SET\_INDEX flag in the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="2f751-122">I seguenti flag aggiuntivi si applicano ai dispositivi VCR:</span><span class="sxs-lookup"><span data-stu-id="2f751-122">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="2f751-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato</span><span class="sxs-lookup"><span data-stu-id="2f751-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="2f751-124">Attiva la visualizzazione sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="2f751-124">Turns on-screen display off.</span></span>

</dd> <dt>

<span data-ttu-id="2f751-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su</span><span class="sxs-lookup"><span data-stu-id="2f751-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="2f751-126">Attiva la visualizzazione sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="2f751-126">Turns on-screen display on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f751-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f751-127">Requirements</span></span>



| <span data-ttu-id="2f751-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f751-128">Requirement</span></span> | <span data-ttu-id="2f751-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2f751-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f751-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f751-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2f751-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f751-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2f751-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f751-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2f751-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f751-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2f751-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f751-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f751-135"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f751-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f751-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f751-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f751-137">MCI</span><span class="sxs-lookup"><span data-stu-id="2f751-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2f751-138">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="2f751-138">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

