---
title: comando escape
description: Il comando escape invia informazioni specifiche del dispositivo a un dispositivo. I dispositivi videodisco riconoscono questo comando.
ms.assetid: 16e0e2b6-6d98-440a-86c1-eca8201ad61a
keywords:
- comando escape Windows Multimedia
topic_type:
- apiref
api_name:
- escape
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b04f7a2ef6c2e91adc9b24a044d0a7e941843f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300960"
---
# <a name="escape-command"></a><span data-ttu-id="937af-105">comando escape</span><span class="sxs-lookup"><span data-stu-id="937af-105">escape command</span></span>

<span data-ttu-id="937af-106">Il comando escape invia informazioni specifiche del dispositivo a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="937af-106">The escape command sends device-specific information to a device.</span></span> <span data-ttu-id="937af-107">I dispositivi videodisco riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="937af-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="937af-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="937af-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("escape %s %s %s"), 
  lpszDeviceID, 
  lpszEscape, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="937af-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="937af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="937af-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="937af-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="937af-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="937af-111">Identifier of an MCI device.</span></span> <span data-ttu-id="937af-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="937af-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="937af-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span><span class="sxs-lookup"><span data-stu-id="937af-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span></span>
</dt> <dd>

<span data-ttu-id="937af-114">Informazioni personalizzate da inviare al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="937af-114">Custom information to send to the device.</span></span>

</dd> <dt>

<span data-ttu-id="937af-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="937af-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="937af-116">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="937af-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="937af-117">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="937af-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="937af-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="937af-118">Return Value</span></span>

<span data-ttu-id="937af-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="937af-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="937af-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="937af-120">Examples</span></span>

<span data-ttu-id="937af-121">Il comando seguente invia la stringa di escape "SA" al dispositivo videodisco.</span><span class="sxs-lookup"><span data-stu-id="937af-121">The following command sends the escape string "SA" to the videodisc device.</span></span>

``` syntax
escape videodisc SA
```

## <a name="requirements"></a><span data-ttu-id="937af-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="937af-122">Requirements</span></span>



| <span data-ttu-id="937af-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="937af-123">Requirement</span></span> | <span data-ttu-id="937af-124">Valore</span><span class="sxs-lookup"><span data-stu-id="937af-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="937af-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="937af-125">Minimum supported client</span></span><br/> | <span data-ttu-id="937af-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="937af-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="937af-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="937af-127">Minimum supported server</span></span><br/> | <span data-ttu-id="937af-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="937af-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="937af-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="937af-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="937af-130">MCI</span><span class="sxs-lookup"><span data-stu-id="937af-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="937af-131">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="937af-131">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

