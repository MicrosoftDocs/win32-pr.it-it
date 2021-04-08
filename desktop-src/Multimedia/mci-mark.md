---
title: Comando MCI_MARK (mmsystem. h)
description: Il \_ comando MCI Mark registra o cancella i contrassegni che possono essere usati con il \_ comando di ricerca MCI per le ricerche ad alta velocità. I dispositivi VCR riconoscono questo comando.
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- Comando MCI_MARK Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddc80decb4559659efb29132f17f18459c334fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048055"
---
# <a name="mci_mark-command"></a><span data-ttu-id="a5bdb-105">\_Comando MCI Mark</span><span class="sxs-lookup"><span data-stu-id="a5bdb-105">MCI\_MARK command</span></span>

<span data-ttu-id="a5bdb-106">Il \_ comando MCI Mark registra o cancella i contrassegni che possono essere usati con il comando di [ \_ ricerca MCI](mci-seek.md) per le ricerche ad alta velocità.</span><span class="sxs-lookup"><span data-stu-id="a5bdb-106">The MCI\_MARK command records or erases marks that can be used with the [MCI\_SEEK](mci-seek.md) command for high-speed searches.</span></span> <span data-ttu-id="a5bdb-107">I dispositivi VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="a5bdb-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="a5bdb-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a5bdb-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
);
```



## <a name="parameters"></a><span data-ttu-id="a5bdb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5bdb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5bdb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a5bdb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a5bdb-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="a5bdb-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a5bdb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a5bdb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a5bdb-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a5bdb-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="a5bdb-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a5bdb-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5bdb-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span><span class="sxs-lookup"><span data-stu-id="a5bdb-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span></span>
</dt> <dd>

<span data-ttu-id="a5bdb-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a5bdb-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="a5bdb-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5bdb-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5bdb-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5bdb-118">Return Value</span></span>

<span data-ttu-id="a5bdb-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="a5bdb-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5bdb-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5bdb-120">Remarks</span></span>

<span data-ttu-id="a5bdb-121">I seguenti flag aggiuntivi si applicano ai dispositivi VCR:</span><span class="sxs-lookup"><span data-stu-id="a5bdb-121">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="a5bdb-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>\_ \_ cancellazione contrassegno VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a5bdb-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>MCI\_VCR\_MARK\_ERASE</span></span>
</dt> <dd>

<span data-ttu-id="a5bdb-123">Elimina un contrassegno nella posizione corrente, se esistente.</span><span class="sxs-lookup"><span data-stu-id="a5bdb-123">Erases a mark at the current position if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="a5bdb-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>\_ \_ scrittura contrassegno VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a5bdb-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>MCI\_VCR\_MARK\_WRITE</span></span>
</dt> <dd>

<span data-ttu-id="a5bdb-125">Scrive un contrassegno nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a5bdb-125">Writes a mark at the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5bdb-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5bdb-126">Requirements</span></span>



| <span data-ttu-id="a5bdb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5bdb-127">Requirement</span></span> | <span data-ttu-id="a5bdb-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a5bdb-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bdb-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5bdb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a5bdb-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a5bdb-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a5bdb-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5bdb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a5bdb-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a5bdb-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a5bdb-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5bdb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5bdb-134"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5bdb-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5bdb-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5bdb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5bdb-136">MCI</span><span class="sxs-lookup"><span data-stu-id="a5bdb-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a5bdb-137">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="a5bdb-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

