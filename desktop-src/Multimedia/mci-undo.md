---
title: Comando MCI_UNDO (mmsystem. h)
description: Il \_ comando di annullamento MCI Annulla la versione più recente del \_ comando MCI Cut, MCI \_ Copy, MCI \_ Delete o MCI \_ Past. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 1593457a-e680-4732-a89e-00f4eff7605a
keywords:
- Comando MCI_UNDO Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_UNDO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d099d95159afee8d91acb77eb64e8e80bee5425d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047977"
---
# <a name="mci_undo-command"></a><span data-ttu-id="f2746-105">\_Comando Annulla MCI</span><span class="sxs-lookup"><span data-stu-id="f2746-105">MCI\_UNDO command</span></span>

<span data-ttu-id="f2746-106">Il \_ comando di annullamento MCI Annulla la versione più recente del comando MCI [ \_ Cut](mci-cut.md), [MCI \_ Copy](mci-copy.md), [MCI \_ Delete](mci-delete.md)o [MCI \_ Past](mci-paste.md) .</span><span class="sxs-lookup"><span data-stu-id="f2746-106">The MCI\_UNDO command reverses the most recent successful [MCI\_CUT](mci-cut.md), [MCI\_COPY](mci-copy.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="f2746-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="f2746-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="f2746-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="f2746-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNDO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUndo
);
```



## <a name="parameters"></a><span data-ttu-id="f2746-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2746-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2746-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f2746-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f2746-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="f2746-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f2746-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f2746-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f2746-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="f2746-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="f2746-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f2746-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2746-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span><span class="sxs-lookup"><span data-stu-id="f2746-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span></span>
</dt> <dd>

<span data-ttu-id="f2746-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f2746-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="f2746-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2746-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2746-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2746-118">Return Value</span></span>

<span data-ttu-id="f2746-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="f2746-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2746-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2746-120">Requirements</span></span>



| <span data-ttu-id="f2746-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2746-121">Requirement</span></span> | <span data-ttu-id="f2746-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f2746-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2746-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2746-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f2746-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2746-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f2746-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2746-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f2746-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2746-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f2746-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2746-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2746-128"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2746-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2746-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2746-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2746-130">MCI</span><span class="sxs-lookup"><span data-stu-id="f2746-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f2746-131">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="f2746-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

