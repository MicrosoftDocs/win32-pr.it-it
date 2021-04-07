---
title: Comando MCI_SETTUNER (mmsystem. h)
description: Il \_ comando MCI SEtuner imposta il canale corrente sul sintonizzatore. I dispositivi VCR riconoscono questo comando.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- Comando MCI_SETTUNER Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5774a927e1f41cf5d3bf42d6e93e532e0c2961a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048741"
---
# <a name="mci_settuner-command"></a><span data-ttu-id="bec97-105">\_Comando MCI SEtuner</span><span class="sxs-lookup"><span data-stu-id="bec97-105">MCI\_SETTUNER command</span></span>

<span data-ttu-id="bec97-106">Il \_ comando MCI SEtuner imposta il canale corrente sul sintonizzatore.</span><span class="sxs-lookup"><span data-stu-id="bec97-106">The MCI\_SETTUNER command sets the current channel on the tuner.</span></span> <span data-ttu-id="bec97-107">I dispositivi VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="bec97-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="bec97-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="bec97-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
);
```



## <a name="parameters"></a><span data-ttu-id="bec97-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bec97-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bec97-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="bec97-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bec97-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="bec97-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="bec97-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="bec97-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bec97-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="bec97-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="bec97-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="bec97-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="bec97-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span><span class="sxs-lookup"><span data-stu-id="bec97-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span></span>
</dt> <dd>

<span data-ttu-id="bec97-116">Puntatore a una [**struttura \_ \_ \_ parametri di MCI VCR**](mci-vcr-settuner-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="bec97-116">Pointer to an [**MCI\_VCR\_SETTUNER\_PARMS**](mci-vcr-settuner-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bec97-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bec97-117">Return Value</span></span>

<span data-ttu-id="bec97-118">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="bec97-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bec97-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bec97-119">Remarks</span></span>

<span data-ttu-id="bec97-120">I seguenti flag aggiuntivi si applicano ai dispositivi VCR:</span><span class="sxs-lookup"><span data-stu-id="bec97-120">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="bec97-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>\_canale di \_ regolazione del VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="bec97-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>MCI\_VCR\_SETTUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="bec97-122">Il membro **dwChannel** della struttura identificata da *lpSetTuner* contiene il nuovo numero di canale.</span><span class="sxs-lookup"><span data-stu-id="bec97-122">The **dwChannel** member of the structure identified by *lpSetTuner* contains the new channel number.</span></span>

</dd> <dt>

<span data-ttu-id="bec97-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>\_canale di \_ setuner VCR MCI \_ \_ disattivato</span><span class="sxs-lookup"><span data-stu-id="bec97-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="bec97-124">Decrementa il canale del sintonizzatore.</span><span class="sxs-lookup"><span data-stu-id="bec97-124">Decrements the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="bec97-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>\_ricerca del \_ \_ canale MCI VCR \_ \_</span><span class="sxs-lookup"><span data-stu-id="bec97-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="bec97-126">Cerca un canale valido nella direzione inversa.</span><span class="sxs-lookup"><span data-stu-id="bec97-126">Searches for a valid channel in the reverse direction.</span></span>

</dd> <dt>

<span data-ttu-id="bec97-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>\_ \_ \_ ricerca canale MCI \_ VCR \_</span><span class="sxs-lookup"><span data-stu-id="bec97-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_UP</span></span>
</dt> <dd>

<span data-ttu-id="bec97-128">Cerca un canale valido nella direzione in avanti.</span><span class="sxs-lookup"><span data-stu-id="bec97-128">Searches for a valid channel in the forward direction.</span></span>

</dd> <dt>

<span data-ttu-id="bec97-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>\_canale di \_ setuner VCR MCI \_ \_ attivo</span><span class="sxs-lookup"><span data-stu-id="bec97-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_UP</span></span>
</dt> <dd>

<span data-ttu-id="bec97-130">Incrementa il canale del sintonizzatore.</span><span class="sxs-lookup"><span data-stu-id="bec97-130">Increments the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="bec97-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>\_numero di \_ setuner \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="bec97-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI\_VCR\_SETTUNER\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="bec97-132">Il membro **dwNumber** della struttura identificata da *lpSetTuner* specifica quale sintonizzatore logico influisce su questo comando.</span><span class="sxs-lookup"><span data-stu-id="bec97-132">The **dwNumber** member of the structure identified by *lpSetTuner* specifies which logical tuner to affect with this command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bec97-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bec97-133">Requirements</span></span>



| <span data-ttu-id="bec97-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="bec97-134">Requirement</span></span> | <span data-ttu-id="bec97-135">Valore</span><span class="sxs-lookup"><span data-stu-id="bec97-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec97-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bec97-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bec97-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bec97-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bec97-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bec97-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bec97-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bec97-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bec97-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bec97-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bec97-141"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bec97-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bec97-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bec97-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec97-143">MCI</span><span class="sxs-lookup"><span data-stu-id="bec97-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bec97-144">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="bec97-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

