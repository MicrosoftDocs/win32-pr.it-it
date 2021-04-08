---
title: index (comando)
description: Il comando index controlla la visualizzazione sullo schermo di un videoregistratore. I dispositivi VCR riconoscono questo comando.
ms.assetid: 16066acf-37aa-4bff-b97e-5eb2420ac3c4
keywords:
- comando indice Windows Multimedia
topic_type:
- apiref
api_name:
- index
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da652b1a7a48dffd9850c435345fcfcb11c2e674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964988"
---
# <a name="index-command"></a><span data-ttu-id="62ece-105">index (comando)</span><span class="sxs-lookup"><span data-stu-id="62ece-105">index command</span></span>

<span data-ttu-id="62ece-106">Il comando index controlla la visualizzazione sullo schermo di un videoregistratore.</span><span class="sxs-lookup"><span data-stu-id="62ece-106">The index command controls a VCR's on-screen display.</span></span> <span data-ttu-id="62ece-107">I dispositivi VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="62ece-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="62ece-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="62ece-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("index %s %s %s"), 
  lpszDeviceID, 
  lpszIndex, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="62ece-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="62ece-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62ece-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="62ece-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="62ece-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="62ece-111">Identifier of an MCI device.</span></span> <span data-ttu-id="62ece-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="62ece-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="62ece-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span><span class="sxs-lookup"><span data-stu-id="62ece-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span></span>
</dt> <dd>

<span data-ttu-id="62ece-114">Uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="62ece-114">One of the following flags.</span></span>



| <span data-ttu-id="62ece-115">Valore</span><span class="sxs-lookup"><span data-stu-id="62ece-115">Value</span></span> | <span data-ttu-id="62ece-116">Significato</span><span class="sxs-lookup"><span data-stu-id="62ece-116">Meaning</span></span>                                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ece-117">spento</span><span class="sxs-lookup"><span data-stu-id="62ece-117">off</span></span>   | <span data-ttu-id="62ece-118">Disattiva la visualizzazione sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="62ece-118">Turns off the on-screen display.</span></span>                                                                                         |
| <span data-ttu-id="62ece-119">on</span><span class="sxs-lookup"><span data-stu-id="62ece-119">on</span></span>    | <span data-ttu-id="62ece-120">Attiva la visualizzazione sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="62ece-120">Turns on the on-screen display.</span></span> <span data-ttu-id="62ece-121">L'elemento da visualizzare è specificato dal flag "index" del comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="62ece-121">The item to be displayed is specified by the "index" flag of the [set](set.md) command.</span></span> |



 

</dd> <dt>

<span data-ttu-id="62ece-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="62ece-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="62ece-123">Può essere "Wait", "notify" o "test".</span><span class="sxs-lookup"><span data-stu-id="62ece-123">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="62ece-124">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="62ece-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62ece-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62ece-125">Return Value</span></span>

<span data-ttu-id="62ece-126">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="62ece-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ece-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62ece-127">Requirements</span></span>



| <span data-ttu-id="62ece-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="62ece-128">Requirement</span></span> | <span data-ttu-id="62ece-129">Valore</span><span class="sxs-lookup"><span data-stu-id="62ece-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="62ece-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62ece-130">Minimum supported client</span></span><br/> | <span data-ttu-id="62ece-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62ece-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="62ece-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62ece-132">Minimum supported server</span></span><br/> | <span data-ttu-id="62ece-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62ece-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="62ece-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62ece-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ece-135">MCI</span><span class="sxs-lookup"><span data-stu-id="62ece-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="62ece-136">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="62ece-136">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="62ece-137">set</span><span class="sxs-lookup"><span data-stu-id="62ece-137">set</span></span>](set.md)
</dt> </dl>

 

