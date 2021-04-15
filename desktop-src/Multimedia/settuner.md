---
title: comando setuner
description: Il comando setuner modifica il sintonizzatore corrente o l'impostazione del canale del sintonizzatore corrente. I dispositivi VCR riconoscono questo comando.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- comando di setuner Windows Multimedia
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479367"
---
# <a name="settuner-command"></a><span data-ttu-id="43c30-105">comando setuner</span><span class="sxs-lookup"><span data-stu-id="43c30-105">settuner command</span></span>

<span data-ttu-id="43c30-106">Il comando setuner modifica il sintonizzatore corrente o l'impostazione del canale del sintonizzatore corrente.</span><span class="sxs-lookup"><span data-stu-id="43c30-106">The settuner command changes the current tuner or the channel setting of the current tuner.</span></span> <span data-ttu-id="43c30-107">I dispositivi VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="43c30-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="43c30-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="43c30-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="43c30-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="43c30-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43c30-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="43c30-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="43c30-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="43c30-111">Identifier of an MCI device.</span></span> <span data-ttu-id="43c30-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="43c30-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="43c30-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span><span class="sxs-lookup"><span data-stu-id="43c30-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span></span>
</dt> <dd>

<span data-ttu-id="43c30-114">Uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="43c30-114">One of the following flags.</span></span>



| <span data-ttu-id="43c30-115">Valore</span><span class="sxs-lookup"><span data-stu-id="43c30-115">Value</span></span>                            | <span data-ttu-id="43c30-116">Significato</span><span class="sxs-lookup"><span data-stu-id="43c30-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c30-117">*canale* canale</span><span class="sxs-lookup"><span data-stu-id="43c30-117">channel *channel*</span></span>                | <span data-ttu-id="43c30-118">Imposta il sintonizzatore sul *canale*.</span><span class="sxs-lookup"><span data-stu-id="43c30-118">Sets the tuner to *channel*.</span></span> <span data-ttu-id="43c30-119">Potrebbe non essere possibile modificare il canale durante la registrazione, a seconda del videoregistratore.</span><span class="sxs-lookup"><span data-stu-id="43c30-119">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="43c30-120">Un canale di dimensioni maggiori rispetto al valore massimo imposta il sintonizzatore sul canale massimo.</span><span class="sxs-lookup"><span data-stu-id="43c30-120">A channel larger than the maximum sets the tuner to the maximum channel.</span></span>                                                                                                                    |
| <span data-ttu-id="43c30-121">ricerca canale verso il basso</span><span class="sxs-lookup"><span data-stu-id="43c30-121">channel seek upchannel seek down</span></span> | <span data-ttu-id="43c30-122">Cerca il canale successivo con un segnale valido.</span><span class="sxs-lookup"><span data-stu-id="43c30-122">Seeks the next channel with a valid signal.</span></span> <span data-ttu-id="43c30-123">"Seek Up" incrementa il numero di canale nella ricerca.</span><span class="sxs-lookup"><span data-stu-id="43c30-123">"Seek up" increments the channel number in its search.</span></span> <span data-ttu-id="43c30-124">"Seek Down" decrementa il numero di canale nella ricerca.</span><span class="sxs-lookup"><span data-stu-id="43c30-124">"Seek down" decrements the channel number in its search.</span></span> <span data-ttu-id="43c30-125">Il sintonizzatore esegue il wrapping sul canale 1 quando viene superato il numero massimo di canali.</span><span class="sxs-lookup"><span data-stu-id="43c30-125">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="43c30-126">Analogamente, durante la ricerca, il sintonizzatore esegue il wrapping sul canale massimo.</span><span class="sxs-lookup"><span data-stu-id="43c30-126">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span> |
| <span data-ttu-id="43c30-127">canale verso il basso</span><span class="sxs-lookup"><span data-stu-id="43c30-127">channel upchannel down</span></span>           | <span data-ttu-id="43c30-128">Incrementa o decrementa il canale del sintonizzatore.</span><span class="sxs-lookup"><span data-stu-id="43c30-128">Increments or decrements the tuner channel.</span></span> <span data-ttu-id="43c30-129">Potrebbe non essere possibile modificare il canale durante la registrazione, a seconda del videoregistratore.</span><span class="sxs-lookup"><span data-stu-id="43c30-129">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="43c30-130">Il sintonizzatore esegue il wrapping sul canale 1 quando viene superato il numero massimo di canali.</span><span class="sxs-lookup"><span data-stu-id="43c30-130">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="43c30-131">Analogamente, durante la ricerca, il sintonizzatore esegue il wrapping sul canale massimo.</span><span class="sxs-lookup"><span data-stu-id="43c30-131">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span>                              |
| <span data-ttu-id="43c30-132">numero </span><span class="sxs-lookup"><span data-stu-id="43c30-132">number *number*</span></span>                  | <span data-ttu-id="43c30-133">Specifica il sintonizzatore interessato dal comando setuner.</span><span class="sxs-lookup"><span data-stu-id="43c30-133">Specifies the tuner to be affected by the settuner command.</span></span> <span data-ttu-id="43c30-134">Se il *numero* non viene specificato, viene utilizzato il valore predefinito 1.</span><span class="sxs-lookup"><span data-stu-id="43c30-134">If *number* is not given, the default value of 1 is assumed.</span></span>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="43c30-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="43c30-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="43c30-136">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="43c30-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="43c30-137">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="43c30-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43c30-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43c30-138">Return Value</span></span>

<span data-ttu-id="43c30-139">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="43c30-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="43c30-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43c30-140">Requirements</span></span>



| <span data-ttu-id="43c30-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="43c30-141">Requirement</span></span> | <span data-ttu-id="43c30-142">Valore</span><span class="sxs-lookup"><span data-stu-id="43c30-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="43c30-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43c30-143">Minimum supported client</span></span><br/> | <span data-ttu-id="43c30-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="43c30-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="43c30-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43c30-145">Minimum supported server</span></span><br/> | <span data-ttu-id="43c30-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="43c30-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="43c30-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43c30-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c30-148">MCI</span><span class="sxs-lookup"><span data-stu-id="43c30-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="43c30-149">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="43c30-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

