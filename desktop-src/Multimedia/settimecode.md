---
title: setimecode (comando)
description: Il comando setimecode Abilita o Disabilita la registrazione del timecode per un VCR. I dispositivi VCR riconoscono questo comando.
ms.assetid: 1b4b82e8-4f13-4bc9-afb0-796339cabb51
keywords:
- comando setimecode Windows Multimedia
topic_type:
- apiref
api_name:
- settimecode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32092e5af7c77cdc274491b20663218d39a1ec1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743903"
---
# <a name="settimecode-command"></a><span data-ttu-id="9f636-105">setimecode (comando)</span><span class="sxs-lookup"><span data-stu-id="9f636-105">settimecode command</span></span>

<span data-ttu-id="9f636-106">Il comando setimecode Abilita o Disabilita la registrazione del timecode per un VCR.</span><span class="sxs-lookup"><span data-stu-id="9f636-106">The settimecode command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="9f636-107">I dispositivi VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="9f636-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="9f636-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="9f636-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settimecode %s %s %s"), 
  lpszDeviceID,
  lpszTimecode, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="9f636-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f636-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f636-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="9f636-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9f636-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="9f636-111">Identifier of an MCI device.</span></span> <span data-ttu-id="9f636-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="9f636-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="9f636-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span><span class="sxs-lookup"><span data-stu-id="9f636-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span></span>
</dt> <dd>

<span data-ttu-id="9f636-114">Uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="9f636-114">One of the following flags.</span></span>



| <span data-ttu-id="9f636-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9f636-115">Value</span></span>      | <span data-ttu-id="9f636-116">Significato</span><span class="sxs-lookup"><span data-stu-id="9f636-116">Meaning</span></span>                          |
|------------|----------------------------------|
| <span data-ttu-id="9f636-117">registra in</span><span class="sxs-lookup"><span data-stu-id="9f636-117">record on</span></span>  | <span data-ttu-id="9f636-118">Imposta il VCR per registrare il timecode.</span><span class="sxs-lookup"><span data-stu-id="9f636-118">Sets the VCR to record timecode.</span></span> |
| <span data-ttu-id="9f636-119">record disattivato</span><span class="sxs-lookup"><span data-stu-id="9f636-119">record off</span></span> | <span data-ttu-id="9f636-120">Disabilita la registrazione del timecode.</span><span class="sxs-lookup"><span data-stu-id="9f636-120">Disables timecode recording.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="9f636-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="9f636-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9f636-122">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="9f636-122">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="9f636-123">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9f636-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f636-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f636-124">Return Value</span></span>

<span data-ttu-id="9f636-125">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="9f636-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f636-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f636-126">Requirements</span></span>



| <span data-ttu-id="9f636-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f636-127">Requirement</span></span> | <span data-ttu-id="9f636-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9f636-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9f636-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f636-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9f636-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f636-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9f636-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f636-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9f636-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f636-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9f636-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f636-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f636-134">MCI</span><span class="sxs-lookup"><span data-stu-id="9f636-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9f636-135">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="9f636-135">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

