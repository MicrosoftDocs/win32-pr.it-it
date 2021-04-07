---
title: comando Close (Corecrt \_ io. h)
description: Il comando Chiudi chiude il dispositivo o il file e tutte le risorse associate. MCI Scarica un dispositivo quando vengono chiuse tutte le istanze del dispositivo o tutti i file. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- Chiudi comando Windows Multimedia
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c255e518553c022dfc833c857b792f43fdbe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964100"
---
# <a name="close-command"></a><span data-ttu-id="330fd-106">Chiudi comando</span><span class="sxs-lookup"><span data-stu-id="330fd-106">close command</span></span>

<span data-ttu-id="330fd-107">Il comando Chiudi chiude il dispositivo o il file e tutte le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="330fd-107">The close command closes the device or file and any associated resources.</span></span> <span data-ttu-id="330fd-108">MCI Scarica un dispositivo quando vengono chiuse tutte le istanze del dispositivo o tutti i file.</span><span class="sxs-lookup"><span data-stu-id="330fd-108">MCI unloads a device when all instances of the device or all files are closed.</span></span> <span data-ttu-id="330fd-109">Tutti i dispositivi MCI riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="330fd-109">All MCI devices recognize this command.</span></span>

<span data-ttu-id="330fd-110">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="330fd-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="330fd-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="330fd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="330fd-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="330fd-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="330fd-113">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="330fd-113">Identifier of an MCI device.</span></span> <span data-ttu-id="330fd-114">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="330fd-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="330fd-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="330fd-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="330fd-116">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="330fd-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="330fd-117">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="330fd-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="330fd-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="330fd-118">Return Value</span></span>

<span data-ttu-id="330fd-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="330fd-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="330fd-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="330fd-120">Remarks</span></span>

<span data-ttu-id="330fd-121">Per chiudere tutti i dispositivi aperti dall'applicazione, specificare l'identificatore di dispositivo "All" per il parametro *lpszDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="330fd-121">To close all devices opened by your application, specify the "all" device identifier for the *lpszDeviceID* parameter.</span></span>

<span data-ttu-id="330fd-122">La chiusura del dispositivo **CDAudio** interrompe la riproduzione audio.</span><span class="sxs-lookup"><span data-stu-id="330fd-122">Closing the **cdaudio** device stops audio playback.</span></span>

<span data-ttu-id="330fd-123">**Windows 2000/XP:** Se il dispositivo **CDAudio** è in esecuzione, la chiusura del dispositivo **CDAudio** non comporta l'interruzione della riproduzione dell'audio.</span><span class="sxs-lookup"><span data-stu-id="330fd-123">**Windows 2000/XP:** If the **cdaudio** device is playing, closing the **cdaudio** device does not cause the audio to stop playing.</span></span> <span data-ttu-id="330fd-124">Inviare prima il comando [Stop](stop.md) .</span><span class="sxs-lookup"><span data-stu-id="330fd-124">Send the [stop](stop.md) command first.</span></span>

## <a name="examples"></a><span data-ttu-id="330fd-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="330fd-125">Examples</span></span>

<span data-ttu-id="330fd-126">Il comando seguente chiude il dispositivo "audio".</span><span class="sxs-lookup"><span data-stu-id="330fd-126">The following command closes the "mysound" device.</span></span>

``` syntax
close mysound
```

## <a name="requirements"></a><span data-ttu-id="330fd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="330fd-127">Requirements</span></span>



| <span data-ttu-id="330fd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="330fd-128">Requirement</span></span> | <span data-ttu-id="330fd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="330fd-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="330fd-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="330fd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="330fd-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="330fd-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="330fd-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="330fd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="330fd-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="330fd-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="330fd-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="330fd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="330fd-135"><dt>\_Io. h Corecrt</dt></span><span class="sxs-lookup"><span data-stu-id="330fd-135"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="330fd-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="330fd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="330fd-137">MCI</span><span class="sxs-lookup"><span data-stu-id="330fd-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="330fd-138">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="330fd-138">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

