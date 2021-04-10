---
title: comando realizza
description: Il comando realizza indica a un dispositivo di selezionare e realizzare la relativa tavolozza nel contesto di visualizzazione della finestra visualizzata. I dispositivi digitali video riconoscono questo comando.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- realizzare il comando Windows Multimedia
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33accaa9638210adf4385a1776fcd8d2bd2021e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964780"
---
# <a name="realize-command"></a><span data-ttu-id="d4f00-105">comando realizza</span><span class="sxs-lookup"><span data-stu-id="d4f00-105">realize command</span></span>

<span data-ttu-id="d4f00-106">Il comando realizza indica a un dispositivo di selezionare e realizzare la relativa tavolozza nel contesto di visualizzazione della finestra visualizzata.</span><span class="sxs-lookup"><span data-stu-id="d4f00-106">The realize command instructs a device to select and realize its palette into the display context of the displayed window.</span></span> <span data-ttu-id="d4f00-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="d4f00-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d4f00-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d4f00-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d4f00-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4f00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f00-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d4f00-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d4f00-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="d4f00-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d4f00-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="d4f00-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d4f00-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span><span class="sxs-lookup"><span data-stu-id="d4f00-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span></span>
</dt> <dd>

<span data-ttu-id="d4f00-114">Uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="d4f00-114">One of the following flags.</span></span>



| <span data-ttu-id="d4f00-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d4f00-115">Value</span></span>      | <span data-ttu-id="d4f00-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d4f00-116">Meaning</span></span>                                                                   |
|------------|---------------------------------------------------------------------------|
| <span data-ttu-id="d4f00-117">background</span><span class="sxs-lookup"><span data-stu-id="d4f00-117">background</span></span> | <span data-ttu-id="d4f00-118">Realizza la tavolozza come tavolozza di sfondo.</span><span class="sxs-lookup"><span data-stu-id="d4f00-118">Realizes the palette as a background palette.</span></span>                             |
| <span data-ttu-id="d4f00-119">normale</span><span class="sxs-lookup"><span data-stu-id="d4f00-119">normal</span></span>     | <span data-ttu-id="d4f00-120">Realizza la tavolozza per una finestra di primo livello.</span><span class="sxs-lookup"><span data-stu-id="d4f00-120">Realizes the palette for a top-level window.</span></span> <span data-ttu-id="d4f00-121">Si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d4f00-121">This is the default setting.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d4f00-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d4f00-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d4f00-123">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="d4f00-123">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="d4f00-124">Per i dispositivi digitali video è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="d4f00-124">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="d4f00-125">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d4f00-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f00-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4f00-126">Return Value</span></span>

<span data-ttu-id="d4f00-127">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="d4f00-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4f00-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4f00-128">Remarks</span></span>

<span data-ttu-id="d4f00-129">Usare questo comando solo se l'applicazione usa un handle di finestra e riceve un messaggio **WM \_ QUERYNEWPALLETTE** o **WM \_ PALETTECHANGED** .</span><span class="sxs-lookup"><span data-stu-id="d4f00-129">Use this command only if your application uses a window handle and receives a **WM\_QUERYNEWPALLETTE** or **WM\_PALETTECHANGED** message.</span></span>

## <a name="examples"></a><span data-ttu-id="d4f00-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="d4f00-130">Examples</span></span>

<span data-ttu-id="d4f00-131">Il comando seguente indica al dispositivo "video" di realizzare la propria tavolozza.</span><span class="sxs-lookup"><span data-stu-id="d4f00-131">The following command tells the "myvideo" device to realize its palette.</span></span>

``` syntax
realize myvideo normal
```

## <a name="requirements"></a><span data-ttu-id="d4f00-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4f00-132">Requirements</span></span>



| <span data-ttu-id="d4f00-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4f00-133">Requirement</span></span> | <span data-ttu-id="d4f00-134">Valore</span><span class="sxs-lookup"><span data-stu-id="d4f00-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d4f00-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4f00-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f00-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d4f00-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d4f00-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4f00-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f00-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d4f00-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d4f00-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4f00-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f00-140">MCI</span><span class="sxs-lookup"><span data-stu-id="d4f00-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d4f00-141">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="d4f00-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

