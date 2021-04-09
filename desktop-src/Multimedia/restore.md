---
title: comando Restore
description: Tramite il comando Restore viene copiata un'immagine ancora da un file al buffer dei frame. Si tratta del contrario del comando di acquisizione. I dispositivi digitali video riconoscono questo comando.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- comando di ripristino Windows Multimedia
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d7f0f236b26e3e73807b32485442d597e93d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963784"
---
# <a name="restore-command"></a><span data-ttu-id="6f580-106">comando Restore</span><span class="sxs-lookup"><span data-stu-id="6f580-106">restore command</span></span>

<span data-ttu-id="6f580-107">Tramite il comando Restore viene copiata un'immagine ancora da un file al buffer dei frame.</span><span class="sxs-lookup"><span data-stu-id="6f580-107">The restore command copies a still image from a file to the frame buffer.</span></span> <span data-ttu-id="6f580-108">Si tratta del contrario del comando di [acquisizione](capture.md) .</span><span class="sxs-lookup"><span data-stu-id="6f580-108">This is the reverse of the [capture](capture.md) command.</span></span> <span data-ttu-id="6f580-109">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="6f580-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6f580-110">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="6f580-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6f580-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f580-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f580-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6f580-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6f580-113">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="6f580-113">Identifier of an MCI device.</span></span> <span data-ttu-id="6f580-114">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="6f580-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6f580-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span><span class="sxs-lookup"><span data-stu-id="6f580-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span></span>
</dt> <dd>

<span data-ttu-id="6f580-116">Uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="6f580-116">One or more of the following flags.</span></span>



| <span data-ttu-id="6f580-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6f580-117">Value</span></span>           | <span data-ttu-id="6f580-118">Significato</span><span class="sxs-lookup"><span data-stu-id="6f580-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f580-119">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="6f580-119">at *rectangle*</span></span>  | <span data-ttu-id="6f580-120">Specifica un rettangolo relativo all'origine del buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="6f580-120">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="6f580-121">Il *rettangolo* viene specificato come *X1 Y1 Y1 2*.</span><span class="sxs-lookup"><span data-stu-id="6f580-121">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="6f580-122">Le coordinate *X1 Y1* specificano l'angolo superiore sinistro e le coordinate *X2 Y2* specificano la larghezza e l'altezza. Se questo flag non viene utilizzato, l'immagine viene copiata nell'angolo superiore sinistro del buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="6f580-122">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.If this flag is not used, the image is copied to the upper left corner of the frame buffer.</span></span><br/> |
| <span data-ttu-id="6f580-123">da *filename*</span><span class="sxs-lookup"><span data-stu-id="6f580-123">from *filename*</span></span> | <span data-ttu-id="6f580-124">Specifica il nome del file di immagine da richiamare.</span><span class="sxs-lookup"><span data-stu-id="6f580-124">Specifies the image filename to recall.</span></span> <span data-ttu-id="6f580-125">Questo flag è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f580-125">This flag is required.</span></span>                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="6f580-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6f580-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6f580-127">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="6f580-127">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="6f580-128">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6f580-128">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f580-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f580-129">Return Value</span></span>

<span data-ttu-id="6f580-130">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="6f580-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f580-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f580-131">Remarks</span></span>

<span data-ttu-id="6f580-132">I dispositivi possono riconoscere diversi formati di immagine; viene sempre riconosciuta una bitmap indipendente dalla periferica Windows.</span><span class="sxs-lookup"><span data-stu-id="6f580-132">Devices can recognize a variety of image formats; a Windows device-independent bitmap is always recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f580-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f580-133">Requirements</span></span>



| <span data-ttu-id="6f580-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f580-134">Requirement</span></span> | <span data-ttu-id="6f580-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6f580-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6f580-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f580-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6f580-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f580-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6f580-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f580-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6f580-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f580-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6f580-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f580-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f580-141">MCI</span><span class="sxs-lookup"><span data-stu-id="6f580-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6f580-142">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="6f580-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="6f580-143">catturare</span><span class="sxs-lookup"><span data-stu-id="6f580-143">capture</span></span>](capture.md)
</dt> </dl>

 

