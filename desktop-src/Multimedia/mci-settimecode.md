---
title: Comando MCI_SETTIMECODE (mmsystem. h)
description: Il \_ comando MCI timecode Abilita o Disabilita la registrazione del timecode per un VCR. I dispositivi VCR riconoscono questo comando.
ms.assetid: b014fbe0-de97-4540-a5fe-b22d157361f7
keywords:
- Comando MCI_SETTIMECODE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETTIMECODE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df0727f4386bad46b3fde7f2d816ce951850b8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302628"
---
# <a name="mci_settimecode-command"></a><span data-ttu-id="0dd0c-105">\_Comando MCI timecode</span><span class="sxs-lookup"><span data-stu-id="0dd0c-105">MCI\_SETTIMECODE command</span></span>

<span data-ttu-id="0dd0c-106">Il \_ comando MCI timecode Abilita o Disabilita la registrazione del timecode per un VCR.</span><span class="sxs-lookup"><span data-stu-id="0dd0c-106">The MCI\_SETTIMECODE command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="0dd0c-107">I dispositivi VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="0dd0c-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="0dd0c-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="0dd0c-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTIMECODE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTimeCode
);
```



## <a name="parameters"></a><span data-ttu-id="0dd0c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0dd0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dd0c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0dd0c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0dd0c-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="0dd0c-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="0dd0c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="0dd0c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0dd0c-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="0dd0c-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="0dd0c-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0dd0c-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="0dd0c-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span><span class="sxs-lookup"><span data-stu-id="0dd0c-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="0dd0c-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="0dd0c-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="0dd0c-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0dd0c-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dd0c-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0dd0c-118">Return Value</span></span>

<span data-ttu-id="0dd0c-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="0dd0c-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dd0c-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="0dd0c-120">Remarks</span></span>

<span data-ttu-id="0dd0c-121">Il flag aggiuntivo seguente si applica ai dispositivi VCR:</span><span class="sxs-lookup"><span data-stu-id="0dd0c-121">The following additional flag applies to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="0dd0c-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>\_record del \_ timecode del VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="0dd0c-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>MCI\_VCR\_SETTIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="0dd0c-123">Imposta la registrazione del timecode Track su on o off.</span><span class="sxs-lookup"><span data-stu-id="0dd0c-123">Sets the timecode track recording to on or off.</span></span> <span data-ttu-id="0dd0c-124">Questo flag viene utilizzato in combinazione con uno dei flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0dd0c-124">This flag is used in combination with one of the following additional flags:</span></span>

</dd> <dt>

<span data-ttu-id="0dd0c-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su</span><span class="sxs-lookup"><span data-stu-id="0dd0c-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="0dd0c-126">Registrazione del timecode in.</span><span class="sxs-lookup"><span data-stu-id="0dd0c-126">Timecode recording on.</span></span>

</dd> <dt>

<span data-ttu-id="0dd0c-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato</span><span class="sxs-lookup"><span data-stu-id="0dd0c-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="0dd0c-128">Registrazione del timecode disabilitata.</span><span class="sxs-lookup"><span data-stu-id="0dd0c-128">Timecode recording off.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0dd0c-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dd0c-129">Requirements</span></span>



| <span data-ttu-id="0dd0c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dd0c-130">Requirement</span></span> | <span data-ttu-id="0dd0c-131">Valore</span><span class="sxs-lookup"><span data-stu-id="0dd0c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd0c-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0dd0c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0dd0c-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0dd0c-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0dd0c-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0dd0c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0dd0c-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0dd0c-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0dd0c-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0dd0c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dd0c-137"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0dd0c-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dd0c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dd0c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd0c-139">MCI</span><span class="sxs-lookup"><span data-stu-id="0dd0c-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0dd0c-140">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="0dd0c-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

