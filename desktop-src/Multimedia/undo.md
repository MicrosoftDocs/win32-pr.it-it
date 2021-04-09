---
title: comando Annulla
description: Il comando Annulla inverte l'azione eseguita dal comando copia, taglia, Elimina, Annulla o incolla più recente. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 81d696a9-5288-4efd-bc76-8416dd63e694
keywords:
- comando Annulla Windows Multimedia
topic_type:
- apiref
api_name:
- undo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0814dff2c684095299b6820b8dc9a2464aa26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048729"
---
# <a name="undo-command"></a><span data-ttu-id="c8805-105">comando Annulla</span><span class="sxs-lookup"><span data-stu-id="c8805-105">undo command</span></span>

<span data-ttu-id="c8805-106">Il comando Annulla inverte l'azione eseguita dal comando [copia](copy.md), [taglia](cut.md), [Elimina](delete.md), Annulla o [Incolla](paste.md) più recente.</span><span class="sxs-lookup"><span data-stu-id="c8805-106">The undo command reverses the action taken by the most recent successful [copy](copy.md), [cut](cut.md), [delete](delete.md), undo, or [paste](paste.md) command.</span></span> <span data-ttu-id="c8805-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="c8805-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="c8805-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c8805-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("undo %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c8805-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8805-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8805-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c8805-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c8805-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c8805-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c8805-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="c8805-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c8805-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c8805-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c8805-114">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="c8805-114">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="c8805-115">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c8805-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8805-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8805-116">Return Value</span></span>

<span data-ttu-id="c8805-117">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="c8805-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8805-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8805-118">Requirements</span></span>



| <span data-ttu-id="c8805-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8805-119">Requirement</span></span> | <span data-ttu-id="c8805-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c8805-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c8805-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8805-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c8805-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8805-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c8805-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8805-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c8805-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8805-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c8805-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8805-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8805-126">MCI</span><span class="sxs-lookup"><span data-stu-id="c8805-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c8805-127">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="c8805-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c8805-128">copy</span><span class="sxs-lookup"><span data-stu-id="c8805-128">copy</span></span>](copy.md)
</dt> <dt>

[<span data-ttu-id="c8805-129">tagliare</span><span class="sxs-lookup"><span data-stu-id="c8805-129">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="c8805-130">delete</span><span class="sxs-lookup"><span data-stu-id="c8805-130">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="c8805-131">Incolla</span><span class="sxs-lookup"><span data-stu-id="c8805-131">paste</span></span>](paste.md)
</dt> </dl>

 

