---
title: comando Load
description: Il comando Load carica un file in un formato specifico del dispositivo. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- comando carica Windows Multimedia
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742495"
---
# <a name="load-command"></a><span data-ttu-id="c9eae-105">comando Load</span><span class="sxs-lookup"><span data-stu-id="c9eae-105">load command</span></span>

<span data-ttu-id="c9eae-106">Il comando Load carica un file in un formato specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9eae-106">The load command loads a file in a device-specific format.</span></span> <span data-ttu-id="c9eae-107">I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="c9eae-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="c9eae-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c9eae-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c9eae-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9eae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9eae-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c9eae-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c9eae-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c9eae-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c9eae-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="c9eae-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c9eae-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span><span class="sxs-lookup"><span data-stu-id="c9eae-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="c9eae-114">Percorso e nome del file da caricare.</span><span class="sxs-lookup"><span data-stu-id="c9eae-114">Path and filename to load.</span></span> <span data-ttu-id="c9eae-115">Per i dispositivi con sovrimpressione video, può includere anche un rettangolo di destinazione per i dati.</span><span class="sxs-lookup"><span data-stu-id="c9eae-115">For video-overlay devices, this can also include a target rectangle for the data.</span></span> <span data-ttu-id="c9eae-116">Per specificare un rettangolo di destinazione, specificare "at" seguito da **x1 y1 x2 y2**, dove **X1 Y1** specificare l'angolo superiore sinistro del rettangolo e **X2 Y2** specificare la larghezza e l'altezza.</span><span class="sxs-lookup"><span data-stu-id="c9eae-116">To specify a target rectangle, specify "at" followed by **X1 Y1 X2 Y2**, where **X1 Y1** specify the upper left corner of the rectangle, and **X2 Y2** specify the width and height.</span></span> <span data-ttu-id="c9eae-117">Il rettangolo è relativo all'origine del buffer del video.</span><span class="sxs-lookup"><span data-stu-id="c9eae-117">The rectangle is relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="c9eae-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c9eae-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c9eae-119">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="c9eae-119">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c9eae-120">Per i dispositivi digitali video è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="c9eae-120">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="c9eae-121">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c9eae-121">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9eae-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9eae-122">Return Value</span></span>

<span data-ttu-id="c9eae-123">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="c9eae-123">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9eae-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9eae-124">Remarks</span></span>

<span data-ttu-id="c9eae-125">Il dispositivo "vidboard" Invia un messaggio di notifica al termine del caricamento.</span><span class="sxs-lookup"><span data-stu-id="c9eae-125">The "vidboard" device sends a notification message when the loading is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="c9eae-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="c9eae-126">Examples</span></span>

<span data-ttu-id="c9eae-127">Il comando seguente carica un file nel dispositivo "vidboard".</span><span class="sxs-lookup"><span data-stu-id="c9eae-127">The following command loads a file into the "vidboard" device.</span></span>

``` syntax
load vidboard c:\vid\fish.vid notify
```

## <a name="requirements"></a><span data-ttu-id="c9eae-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9eae-128">Requirements</span></span>



| <span data-ttu-id="c9eae-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9eae-129">Requirement</span></span> | <span data-ttu-id="c9eae-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c9eae-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c9eae-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9eae-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c9eae-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c9eae-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c9eae-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9eae-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c9eae-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c9eae-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c9eae-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9eae-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9eae-136">MCI</span><span class="sxs-lookup"><span data-stu-id="c9eae-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c9eae-137">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="c9eae-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

