---
title: Configura comando
description: Il comando Configura Visualizza una finestra di dialogo usata per configurare il dispositivo. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 17d99992-f432-4b8a-ae98-2a70637c29c3
keywords:
- configurare il comando Windows Multimedia
topic_type:
- apiref
api_name:
- configure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f131159d389577e3c717e5630633bb46558d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739839"
---
# <a name="configure-command"></a><span data-ttu-id="02e7e-105">Configura comando</span><span class="sxs-lookup"><span data-stu-id="02e7e-105">configure command</span></span>

<span data-ttu-id="02e7e-106">Il comando Configura Visualizza una finestra di dialogo usata per configurare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02e7e-106">The configure command displays a dialog box used to configure the device.</span></span> <span data-ttu-id="02e7e-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="02e7e-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="02e7e-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="02e7e-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("configure %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="02e7e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="02e7e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e7e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="02e7e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="02e7e-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="02e7e-111">Identifier of an MCI device.</span></span> <span data-ttu-id="02e7e-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="02e7e-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="02e7e-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="02e7e-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="02e7e-114">Può essere "Wait", "notify" o "test".</span><span class="sxs-lookup"><span data-stu-id="02e7e-114">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="02e7e-115">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="02e7e-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e7e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02e7e-116">Return Value</span></span>

<span data-ttu-id="02e7e-117">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="02e7e-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e7e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02e7e-118">Requirements</span></span>



| <span data-ttu-id="02e7e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e7e-119">Requirement</span></span> | <span data-ttu-id="02e7e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="02e7e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="02e7e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e7e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="02e7e-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="02e7e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="02e7e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e7e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="02e7e-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="02e7e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="02e7e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02e7e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e7e-126">MCI</span><span class="sxs-lookup"><span data-stu-id="02e7e-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="02e7e-127">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="02e7e-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

