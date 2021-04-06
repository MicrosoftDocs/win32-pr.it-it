---
title: Comando MCI_RESTORE (mmsystem. h)
description: Il \_ comando di ripristino MCI copia una bitmap da un file nel buffer dei frame. I dispositivi digitali video riconoscono questo comando. Questo comando esegue l'azione opposta del \_ comando di acquisizione MCI.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- Comando MCI_RESTORE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742810"
---
# <a name="mci_restore-command"></a><span data-ttu-id="cc3b6-106">\_Comando di ripristino MCI</span><span class="sxs-lookup"><span data-stu-id="cc3b6-106">MCI\_RESTORE command</span></span>

<span data-ttu-id="cc3b6-107">Il \_ comando di ripristino MCI copia una bitmap da un file nel buffer dei frame.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-107">The MCI\_RESTORE command copies a bitmap from a file to the frame buffer.</span></span> <span data-ttu-id="cc3b6-108">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="cc3b6-109">Questo comando esegue l'azione opposta del comando di [ \_ acquisizione MCI](mci-capture.md) .</span><span class="sxs-lookup"><span data-stu-id="cc3b6-109">This command performs the opposite action of the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

<span data-ttu-id="cc3b6-110">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
);
```



## <a name="parameters"></a><span data-ttu-id="cc3b6-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc3b6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc3b6-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="cc3b6-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="cc3b6-113">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="cc3b6-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="cc3b6-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cc3b6-115">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="cc3b6-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="cc3b6-116">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="cc3b6-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3b6-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span><span class="sxs-lookup"><span data-stu-id="cc3b6-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span></span>
</dt> <dd>

<span data-ttu-id="cc3b6-118">Puntatore a una [**struttura \_ \_ \_ parametri DGV Restore MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="cc3b6-118">Pointer to an [**MCI\_DGV\_RESTORE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc3b6-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc3b6-119">Return Value</span></span>

<span data-ttu-id="cc3b6-120">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc3b6-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc3b6-121">Remarks</span></span>

<span data-ttu-id="cc3b6-122">L'implementazione di è in grado di riconoscere diversi formati di immagine, ma viene sempre accettata una bitmap indipendente dal dispositivo (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-122">The implementation can recognize a variety of image formats, but a Windows device-independent bitmap (DIB) is always accepted.</span></span>

<span data-ttu-id="cc3b6-123">I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:</span><span class="sxs-lookup"><span data-stu-id="cc3b6-123">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="cc3b6-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>\_ \_ ripristino di MCI DGV \_ da</span><span class="sxs-lookup"><span data-stu-id="cc3b6-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>MCI\_DGV\_RESTORE\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="cc3b6-125">Il membro **lpstrFileName** della struttura identificata da *lpRestore* contiene un indirizzo di un buffer contenente il nome del file di origine.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-125">The **lpstrFileName** member of the structure identified by *lpRestore* contains an address of a buffer containing the source filename.</span></span> <span data-ttu-id="cc3b6-126">Il nome file è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-126">The filename is required.</span></span>

</dd> <dt>

<span data-ttu-id="cc3b6-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>\_ripristino DGV \_ MCI \_ in</span><span class="sxs-lookup"><span data-stu-id="cc3b6-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>MCI\_DGV\_RESTORE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="cc3b6-128">Il membro **RC** della struttura identificato da *lpRestore* contiene un rettangolo valido.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-128">The **rc** member of the structure identified by *lpRestore* contains a valid rectangle.</span></span> <span data-ttu-id="cc3b6-129">Il rettangolo specifica un'area del buffer del frame rispetto all'origine.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-129">The rectangle specifies a region of the frame buffer relative to its origin.</span></span> <span data-ttu-id="cc3b6-130">La prima coppia di coordinate specifica l'angolo superiore sinistro del rettangolo. la seconda coppia specifica la larghezza e l'altezza.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="cc3b6-131">Se questo flag non è specificato, l'immagine viene copiata nell'angolo superiore sinistro del buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="cc3b6-131">If this flag is not specified, the image is copied to the upper left corner of the frame buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc3b6-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc3b6-132">Requirements</span></span>



| <span data-ttu-id="cc3b6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc3b6-133">Requirement</span></span> | <span data-ttu-id="cc3b6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="cc3b6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc3b6-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc3b6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cc3b6-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cc3b6-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cc3b6-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc3b6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cc3b6-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cc3b6-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cc3b6-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc3b6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc3b6-140"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc3b6-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc3b6-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc3b6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc3b6-142">MCI</span><span class="sxs-lookup"><span data-stu-id="cc3b6-142">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cc3b6-143">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="cc3b6-143">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

