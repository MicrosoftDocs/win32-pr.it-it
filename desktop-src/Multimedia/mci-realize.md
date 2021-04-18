---
title: Comando MCI_REALIZE (mmsystem. h)
description: Il \_ comando MCI realizz fa in modo che un dispositivo grafico realizzi la propria tavolozza in un contesto di dispositivo (DC). I dispositivi digitali video riconoscono questo comando.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- Comando MCI_REALIZE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f2e59bfe9bbe1443f55ae0fbcf8819b932bb1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301465"
---
# <a name="mci_realize-command"></a><span data-ttu-id="54441-105">\_Comando MCI realizz</span><span class="sxs-lookup"><span data-stu-id="54441-105">MCI\_REALIZE command</span></span>

<span data-ttu-id="54441-106">Il \_ comando MCI realizz fa in modo che un dispositivo grafico realizzi la propria tavolozza in un contesto di dispositivo (DC).</span><span class="sxs-lookup"><span data-stu-id="54441-106">The MCI\_REALIZE command causes a graphic device to realize its palette into a device context (DC).</span></span> <span data-ttu-id="54441-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="54441-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="54441-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="54441-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
);
```



## <a name="parameters"></a><span data-ttu-id="54441-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="54441-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54441-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="54441-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="54441-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="54441-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="54441-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="54441-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="54441-113">**MCI \_ NOTIFICA**, **MCI \_ wait** o, per i dispositivi video digitali, **MCI \_ test**.</span><span class="sxs-lookup"><span data-stu-id="54441-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="54441-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="54441-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="54441-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span><span class="sxs-lookup"><span data-stu-id="54441-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span></span>
</dt> <dd>

<span data-ttu-id="54441-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="54441-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="54441-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="54441-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54441-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54441-118">Return Value</span></span>

<span data-ttu-id="54441-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="54441-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="54441-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="54441-120">Remarks</span></span>

<span data-ttu-id="54441-121">Usare questo comando quando l'applicazione riceve il messaggio [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) .</span><span class="sxs-lookup"><span data-stu-id="54441-121">You should use this command when your application receives the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message.</span></span>

<span data-ttu-id="54441-122">Con il tipo di dispositivo "digitalvideo" vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="54441-122">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="54441-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ realizza \_ bkgd</span><span class="sxs-lookup"><span data-stu-id="54441-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI\_DGV\_REALIZE\_BKGD</span></span>
</dt> <dd>

<span data-ttu-id="54441-124">Realizza la tavolozza come tavolozza di sfondo.</span><span class="sxs-lookup"><span data-stu-id="54441-124">Realizes the palette as a background palette.</span></span>

</dd> <dt>

<span data-ttu-id="54441-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>norma per la realizzazione di MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="54441-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI\_DGV\_REALIZE\_NORM</span></span>
</dt> <dd>

<span data-ttu-id="54441-126">Realizza la tavolozza normalmente.</span><span class="sxs-lookup"><span data-stu-id="54441-126">Realizes the palette normally.</span></span> <span data-ttu-id="54441-127">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="54441-127">This is the default.</span></span>

</dd> </dl>

<span data-ttu-id="54441-128">Per i dispositivi digitali video, il parametro *lpRealize* punta a una **struttura \_ \_ parametri** per la realizzazione di un MCI.</span><span class="sxs-lookup"><span data-stu-id="54441-128">For digital-video devices, the *lpRealize* parameter points to an **MCI\_REALIZE\_PARMS** structure.</span></span> <span data-ttu-id="54441-129">Per ulteriori informazioni, vedere la pagina relativa ai commenti nella struttura [**\_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="54441-129">For more information, see comments in the [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="54441-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54441-130">Requirements</span></span>



| <span data-ttu-id="54441-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="54441-131">Requirement</span></span> | <span data-ttu-id="54441-132">Valore</span><span class="sxs-lookup"><span data-stu-id="54441-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54441-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54441-133">Minimum supported client</span></span><br/> | <span data-ttu-id="54441-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54441-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="54441-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54441-135">Minimum supported server</span></span><br/> | <span data-ttu-id="54441-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54441-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="54441-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54441-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="54441-138"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54441-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54441-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54441-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54441-140">MCI</span><span class="sxs-lookup"><span data-stu-id="54441-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="54441-141">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="54441-141">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

