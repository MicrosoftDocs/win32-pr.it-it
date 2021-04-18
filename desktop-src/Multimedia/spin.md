---
title: comando Spin
description: Il comando Spin inizia a ruotare un disco o interrompe la rotazione del disco. I dispositivi videodisco riconoscono questo comando.
ms.assetid: 1fdf4d09-fafd-4245-ad92-397114d0f473
keywords:
- casella di controllo di selezione di Windows
topic_type:
- apiref
api_name:
- spin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c25e25f5a44ad6e6c9562d05653ab25cb2950b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301823"
---
# <a name="spin-command"></a><span data-ttu-id="d6212-105">comando Spin</span><span class="sxs-lookup"><span data-stu-id="d6212-105">spin command</span></span>

<span data-ttu-id="d6212-106">Il comando Spin inizia a ruotare un disco o interrompe la rotazione del disco.</span><span class="sxs-lookup"><span data-stu-id="d6212-106">The spin command starts spinning a disc or stops the disc from spinning.</span></span> <span data-ttu-id="d6212-107">I dispositivi videodisco riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="d6212-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="d6212-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d6212-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("spin %s %s %s"), 
  lpszDeviceID, 
  lpszUpDown, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d6212-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6212-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6212-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d6212-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d6212-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="d6212-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d6212-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="d6212-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d6212-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span><span class="sxs-lookup"><span data-stu-id="d6212-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span></span>
</dt> <dd>

<span data-ttu-id="d6212-114">Uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="d6212-114">One of the following flags.</span></span>



| <span data-ttu-id="d6212-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d6212-115">Value</span></span> | <span data-ttu-id="d6212-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d6212-116">Meaning</span></span>                       |
|-------|-------------------------------|
| <span data-ttu-id="d6212-117">sistema</span><span class="sxs-lookup"><span data-stu-id="d6212-117">down</span></span>  | <span data-ttu-id="d6212-118">Arresta la rotazione del disco.</span><span class="sxs-lookup"><span data-stu-id="d6212-118">Stops the disc from spinning.</span></span> |
| <span data-ttu-id="d6212-119">up</span><span class="sxs-lookup"><span data-stu-id="d6212-119">up</span></span>    | <span data-ttu-id="d6212-120">Avvia la rotazione del disco.</span><span class="sxs-lookup"><span data-stu-id="d6212-120">Starts spinning the disc.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="d6212-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d6212-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d6212-122">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="d6212-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="d6212-123">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d6212-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6212-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6212-124">Return Value</span></span>

<span data-ttu-id="d6212-125">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="d6212-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="d6212-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="d6212-126">Examples</span></span>

<span data-ttu-id="d6212-127">Il comando seguente avvia la rotazione di un dispositivo videodisco.</span><span class="sxs-lookup"><span data-stu-id="d6212-127">The following command starts spinning a videodisc device.</span></span>

``` syntax
spin videodisc up
```

## <a name="requirements"></a><span data-ttu-id="d6212-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6212-128">Requirements</span></span>



| <span data-ttu-id="d6212-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6212-129">Requirement</span></span> | <span data-ttu-id="d6212-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d6212-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d6212-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6212-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d6212-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d6212-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d6212-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6212-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d6212-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d6212-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d6212-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6212-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6212-136">MCI</span><span class="sxs-lookup"><span data-stu-id="d6212-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d6212-137">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="d6212-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

