---
title: Interrompi comando
description: Il comando break specifica una chiave per interrompere un comando che è stato richiamato usando il valore \ 0034; Wait \ 0034; bandiera. Questo comando è un comando di sistema MCI; viene interpretato direttamente da MCI.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- comando Interrompi Windows Multimedia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478934"
---
# <a name="break-command"></a><span data-ttu-id="3a3fb-105">Interrompi comando</span><span class="sxs-lookup"><span data-stu-id="3a3fb-105">break command</span></span>

<span data-ttu-id="3a3fb-106">Il comando break specifica una chiave per interrompere un comando che è stato richiamato usando il flag "Wait".</span><span class="sxs-lookup"><span data-stu-id="3a3fb-106">The break command specifies a key to abort a command that was invoked using the "wait" flag.</span></span> <span data-ttu-id="3a3fb-107">Questo comando è un comando di sistema MCI; viene interpretato direttamente da MCI.</span><span class="sxs-lookup"><span data-stu-id="3a3fb-107">This command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="3a3fb-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="3a3fb-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="3a3fb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a3fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a3fb-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3a3fb-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3a3fb-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="3a3fb-111">Identifier of an MCI device.</span></span> <span data-ttu-id="3a3fb-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="3a3fb-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="3a3fb-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span><span class="sxs-lookup"><span data-stu-id="3a3fb-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span></span>
</dt> <dd>

<span data-ttu-id="3a3fb-114">Uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a3fb-114">One of the following flags.</span></span>



| <span data-ttu-id="3a3fb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3a3fb-115">Value</span></span>                 | <span data-ttu-id="3a3fb-116">Significato</span><span class="sxs-lookup"><span data-stu-id="3a3fb-116">Meaning</span></span>                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="3a3fb-117">nel *codice della chiave virtuale*</span><span class="sxs-lookup"><span data-stu-id="3a3fb-117">on *virtual key code*</span></span> | <span data-ttu-id="3a3fb-118">Specifica la chiave che interrompe un comando che è stato avviato utilizzando il flag "Wait".</span><span class="sxs-lookup"><span data-stu-id="3a3fb-118">Specifies the key that aborts a command that was started using the "wait" flag.</span></span> |
| <span data-ttu-id="3a3fb-119">spento</span><span class="sxs-lookup"><span data-stu-id="3a3fb-119">off</span></span>                   | <span data-ttu-id="3a3fb-120">Disabilita la chiave di break corrente.</span><span class="sxs-lookup"><span data-stu-id="3a3fb-120">Disables the current break key.</span></span>                                                 |



 

</dd> <dt>

<span data-ttu-id="3a3fb-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="3a3fb-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3a3fb-122">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="3a3fb-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="3a3fb-123">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="3a3fb-123">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="3a3fb-124">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3a3fb-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a3fb-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a3fb-125">Return Value</span></span>

<span data-ttu-id="3a3fb-126">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="3a3fb-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a3fb-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a3fb-127">Remarks</span></span>

<span data-ttu-id="3a3fb-128">Quando il tasto Break è abilitato e l'utente preme il tasto identificato dal codice della chiave virtuale specificato nel parametro *lpszVirtKey* , il dispositivo restituisce il controllo all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a3fb-128">When the break key is enabled and the user presses the key identified by the virtual-key code specified in the *lpszVirtKey* parameter, the device returns control to the application.</span></span> <span data-ttu-id="3a3fb-129">Se possibile, il comando continua l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3a3fb-129">If possible, the command continues execution.</span></span>

## <a name="examples"></a><span data-ttu-id="3a3fb-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="3a3fb-130">Examples</span></span>

<span data-ttu-id="3a3fb-131">Il seguente comando imposta F2 come chiave di break per il dispositivo "audio".</span><span class="sxs-lookup"><span data-stu-id="3a3fb-131">The following command sets F2 as the break key for the "mysound" device.</span></span>

``` syntax
break mysound on 113
```

## <a name="requirements"></a><span data-ttu-id="3a3fb-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a3fb-132">Requirements</span></span>



| <span data-ttu-id="3a3fb-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a3fb-133">Requirement</span></span> | <span data-ttu-id="3a3fb-134">Valore</span><span class="sxs-lookup"><span data-stu-id="3a3fb-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3a3fb-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a3fb-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3a3fb-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a3fb-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3a3fb-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a3fb-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3a3fb-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a3fb-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3a3fb-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a3fb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a3fb-140">MCI</span><span class="sxs-lookup"><span data-stu-id="3a3fb-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3a3fb-141">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="3a3fb-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

