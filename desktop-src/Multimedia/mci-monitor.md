---
title: Comando MCI_MONITOR (mmsystem. h)
description: Il \_ comando MCI monitor specifica l'origine della presentazione. I dispositivi digitali video riconoscono questo comando.
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- Comando MCI_MONITOR Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964528"
---
# <a name="mci_monitor-command"></a><span data-ttu-id="2f1f0-105">\_Comando di monitoraggio MCI</span><span class="sxs-lookup"><span data-stu-id="2f1f0-105">MCI\_MONITOR command</span></span>

<span data-ttu-id="2f1f0-106">Il \_ comando MCI monitor specifica l'origine della presentazione.</span><span class="sxs-lookup"><span data-stu-id="2f1f0-106">The MCI\_MONITOR command specifies the presentation source.</span></span> <span data-ttu-id="2f1f0-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="2f1f0-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="2f1f0-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="2f1f0-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="2f1f0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f1f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f1f0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2f1f0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2f1f0-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="2f1f0-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2f1f0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2f1f0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2f1f0-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="2f1f0-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="2f1f0-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2f1f0-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f1f0-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span><span class="sxs-lookup"><span data-stu-id="2f1f0-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="2f1f0-116">Puntatore a una [**struttura \_ \_ \_ parametri del monitor DGV di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) .</span><span class="sxs-lookup"><span data-stu-id="2f1f0-116">Pointer to an [**MCI\_DGV\_MONITOR\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f1f0-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f1f0-117">Return Value</span></span>

<span data-ttu-id="2f1f0-118">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="2f1f0-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f1f0-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f1f0-119">Remarks</span></span>

<span data-ttu-id="2f1f0-120">I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:</span><span class="sxs-lookup"><span data-stu-id="2f1f0-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="2f1f0-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>\_metodo di \_ monitoraggio MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="2f1f0-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI\_DGV\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="2f1f0-122">Costante che indica che il metodo di monitoraggio è incluso nel membro **dwMethod** della struttura identificata da *lpMonitor*.</span><span class="sxs-lookup"><span data-stu-id="2f1f0-122">A constant indicating the method of monitoring is included in the **dwMethod** member of the structure identified by *lpMonitor*.</span></span>

<span data-ttu-id="2f1f0-123">Quando il \_ \_ flag di input di DGV del monitor MCI \_ viene usato nel membro **dwSource** , viene selezionato il metodo di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="2f1f0-123">When the MCI\_DGV\_MONITOR\_INPUT flag is used in the **dwSource** member, this selects the method of monitoring.</span></span> <span data-ttu-id="2f1f0-124">In genere, diversi metodi di monitoraggio hanno implicazioni diverse sulla modalità di utilizzo dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2f1f0-124">Typically, different monitoring methods have different implications on how the hardware is used.</span></span> <span data-ttu-id="2f1f0-125">Il metodo di monitoraggio predefinito è selezionato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f1f0-125">The default monitoring method is selected by the device.</span></span>

</dd> <dt>

<span data-ttu-id="2f1f0-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>\_ \_ origine monitoraggio DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="2f1f0-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI\_DGV\_MONITOR\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="2f1f0-127">Costante che indica che l'origine del monitoraggio è inclusa nel membro **dwSource** della struttura identificata da *lpMonitor*.</span><span class="sxs-lookup"><span data-stu-id="2f1f0-127">A constant indicating the monitor source is included in the **dwSource** member of the structure identified by *lpMonitor*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f1f0-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f1f0-128">Requirements</span></span>



| <span data-ttu-id="2f1f0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f1f0-129">Requirement</span></span> | <span data-ttu-id="2f1f0-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2f1f0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f1f0-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f1f0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2f1f0-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f1f0-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2f1f0-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f1f0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2f1f0-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f1f0-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2f1f0-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f1f0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f1f0-136"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f1f0-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f1f0-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f1f0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f1f0-138">MCI</span><span class="sxs-lookup"><span data-stu-id="2f1f0-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2f1f0-139">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="2f1f0-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

