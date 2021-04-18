---
title: comando Mark
description: Il comando Mark controlla la registrazione e l'eliminazione dei contrassegni sul nastro. I dispositivi VCR riconoscono questo comando.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- contrassegna il comando Windows Multimedia
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570968af05424597a7fe2b59e86e0364694e0e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301468"
---
# <a name="mark-command"></a><span data-ttu-id="3c566-105">comando Mark</span><span class="sxs-lookup"><span data-stu-id="3c566-105">mark command</span></span>

<span data-ttu-id="3c566-106">Il comando Mark controlla la registrazione e l'eliminazione dei contrassegni sul nastro.</span><span class="sxs-lookup"><span data-stu-id="3c566-106">The mark command controls recording and erasing of marks on the videotape.</span></span> <span data-ttu-id="3c566-107">I dispositivi VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="3c566-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="3c566-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="3c566-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="3c566-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c566-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c566-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3c566-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3c566-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="3c566-111">Identifier of an MCI device.</span></span> <span data-ttu-id="3c566-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="3c566-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="3c566-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span><span class="sxs-lookup"><span data-stu-id="3c566-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span></span>
</dt> <dd>

<span data-ttu-id="3c566-114">Uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="3c566-114">One of the following flags.</span></span>



| <span data-ttu-id="3c566-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3c566-115">Value</span></span> | <span data-ttu-id="3c566-116">Significato</span><span class="sxs-lookup"><span data-stu-id="3c566-116">Meaning</span></span>                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c566-117">erase</span><span class="sxs-lookup"><span data-stu-id="3c566-117">erase</span></span> | <span data-ttu-id="3c566-118">Cancella un contrassegno in corrispondenza della posizione corrente, se presente.</span><span class="sxs-lookup"><span data-stu-id="3c566-118">Erases a mark at the current position, if one exists.</span></span> <span data-ttu-id="3c566-119">Per cancellare un contrassegno, cercare innanzitutto il contrassegno e quindi eseguire il comando "Erase" del contrassegno.</span><span class="sxs-lookup"><span data-stu-id="3c566-119">To erase a mark, first seek to the mark and then issue the mark "erase" command.</span></span> |
| <span data-ttu-id="3c566-120">scrittura</span><span class="sxs-lookup"><span data-stu-id="3c566-120">write</span></span> | <span data-ttu-id="3c566-121">Scrive un contrassegno nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="3c566-121">Writes a mark at the current position.</span></span> <span data-ttu-id="3c566-122">È possibile che il VCR debba essere in modalità riproduzione o registrazione affinché il comando abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3c566-122">The VCR might need to be in play or record mode for this command to succeed.</span></span>                    |



 

</dd> <dt>

<span data-ttu-id="3c566-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="3c566-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3c566-124">Può essere "Wait", "notify" o "test".</span><span class="sxs-lookup"><span data-stu-id="3c566-124">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="3c566-125">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3c566-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c566-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c566-126">Return Value</span></span>

<span data-ttu-id="3c566-127">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="3c566-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c566-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c566-128">Remarks</span></span>

<span data-ttu-id="3c566-129">I contrassegni sono segnali speciali scritti nel contenuto che possono essere rilevati dal VCR durante le ricerche ad alta velocità.</span><span class="sxs-lookup"><span data-stu-id="3c566-129">Marks are special signals written to the content that can be detected by the VCR during high-speed searches.</span></span> <span data-ttu-id="3c566-130">I contrassegni sono specifici del VCR.</span><span class="sxs-lookup"><span data-stu-id="3c566-130">Marks are VCR specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c566-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c566-131">Requirements</span></span>



| <span data-ttu-id="3c566-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c566-132">Requirement</span></span> | <span data-ttu-id="3c566-133">Valore</span><span class="sxs-lookup"><span data-stu-id="3c566-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3c566-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c566-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3c566-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c566-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3c566-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c566-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3c566-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c566-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3c566-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c566-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c566-139">MCI</span><span class="sxs-lookup"><span data-stu-id="3c566-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3c566-140">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="3c566-140">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

