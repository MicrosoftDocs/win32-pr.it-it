---
title: Messaggio TTM_SETTITLE (COMmctrl. h)
description: Aggiunge un'icona standard e una stringa del titolo a una descrizione comando.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- Controlli di Windows Message TTM_SETTITLE
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7972a9d40347995e9d641e7fc8706f9ad4c58bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874486"
---
# <a name="ttm_settitle-message"></a><span data-ttu-id="8c839-104">\_Messaggio TTM</span><span class="sxs-lookup"><span data-stu-id="8c839-104">TTM\_SETTITLE message</span></span>

<span data-ttu-id="8c839-105">Aggiunge un'icona standard e una stringa del titolo a una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="8c839-105">Adds a standard icon and title string to a tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c839-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c839-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c839-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c839-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c839-108">Impostare *wParam* su uno dei valori seguenti per specificare l'icona da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="8c839-108">Set *wParam* to one of the following values to specify the icon to be displayed.</span></span> <span data-ttu-id="8c839-109">A partire da Windows XP SP2 e versioni successive, questo parametro può contenere anche un valore **HICON** .</span><span class="sxs-lookup"><span data-stu-id="8c839-109">As of Windows XP SP2 and later, this parameter can also contain an **HICON** value.</span></span> <span data-ttu-id="8c839-110">Si presuppone che un valore maggiore di TTI sia \_ un errore di **HICON**.</span><span class="sxs-lookup"><span data-stu-id="8c839-110">Any value greater than TTI\_ERROR is assumed to be an **HICON**.</span></span>



| <span data-ttu-id="8c839-111">Valore</span><span class="sxs-lookup"><span data-stu-id="8c839-111">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="8c839-112">Significato</span><span class="sxs-lookup"><span data-stu-id="8c839-112">Meaning</span></span>                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <span data-ttu-id="8c839-113"><dt>**TTI \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="8c839-113"><dt>**TTI\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="8c839-114">Nessuna icona.</span><span class="sxs-lookup"><span data-stu-id="8c839-114">No icon.</span></span><br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <span data-ttu-id="8c839-115"><dt>**\_informazioni tti**</dt></span><span class="sxs-lookup"><span data-stu-id="8c839-115"><dt>**TTI\_INFO**</dt></span></span> </dl>                             | <span data-ttu-id="8c839-116">Icona info.</span><span class="sxs-lookup"><span data-stu-id="8c839-116">Info icon.</span></span><br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <span data-ttu-id="8c839-117"><dt>**avviso di TTI \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c839-117"><dt>**TTI\_WARNING**</dt></span></span> </dl>                    | <span data-ttu-id="8c839-118">Icona avviso</span><span class="sxs-lookup"><span data-stu-id="8c839-118">Warning icon</span></span><br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <span data-ttu-id="8c839-119"><dt>**\_errore tti**</dt></span><span class="sxs-lookup"><span data-stu-id="8c839-119"><dt>**TTI\_ERROR**</dt></span></span> </dl>                          | <span data-ttu-id="8c839-120">Icona di errore</span><span class="sxs-lookup"><span data-stu-id="8c839-120">Error Icon</span></span><br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <span data-ttu-id="8c839-121"><dt>**\_informazioni tti \_ large**</dt></span><span class="sxs-lookup"><span data-stu-id="8c839-121"><dt>**TTI\_INFO\_LARGE**</dt></span></span> </dl>          | <span data-ttu-id="8c839-122">Icona di errore grande</span><span class="sxs-lookup"><span data-stu-id="8c839-122">Large error Icon</span></span><br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <span data-ttu-id="8c839-123"><dt>**\_avviso tti \_ grande**</dt></span><span class="sxs-lookup"><span data-stu-id="8c839-123"><dt>**TTI\_WARNING\_LARGE**</dt></span></span> </dl> | <span data-ttu-id="8c839-124">Icona di errore grande</span><span class="sxs-lookup"><span data-stu-id="8c839-124">Large error Icon</span></span><br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <span data-ttu-id="8c839-125"><dt>**\_errore tti \_ grande**</dt></span><span class="sxs-lookup"><span data-stu-id="8c839-125"><dt>**TTI\_ERROR\_LARGE**</dt></span></span> </dl>       | <span data-ttu-id="8c839-126">Icona di errore grande</span><span class="sxs-lookup"><span data-stu-id="8c839-126">Large error Icon</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8c839-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c839-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c839-128">Puntatore alla stringa del titolo.</span><span class="sxs-lookup"><span data-stu-id="8c839-128">Pointer to the title string.</span></span> <span data-ttu-id="8c839-129">È necessario assegnare un valore a *lParam*.</span><span class="sxs-lookup"><span data-stu-id="8c839-129">You must assign a value to *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c839-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c839-130">Return value</span></span>

<span data-ttu-id="8c839-131">Restituisce **true** se l'operazione ha esito positivo, **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8c839-131">Returns **TRUE** if successful, **FALSE** if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c839-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c839-132">Remarks</span></span>

<span data-ttu-id="8c839-133">Il titolo di una descrizione comando viene visualizzato sopra il testo, in un tipo di carattere diverso.</span><span class="sxs-lookup"><span data-stu-id="8c839-133">The title of a tooltip appears above the text, in a different font.</span></span> <span data-ttu-id="8c839-134">Non è sufficiente avere un titolo; la descrizione comando deve avere anche testo o non è visualizzata.</span><span class="sxs-lookup"><span data-stu-id="8c839-134">It is not sufficient to have a title; the tooltip must have text as well, or it is not displayed.</span></span>

<span data-ttu-id="8c839-135">Quando *wParam* contiene un **HICON**, viene creata una copia dell'icona dalla finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="8c839-135">When *wParam* contains an **HICON**, a copy of the icon is created by the tooltip window.</span></span>

<span data-ttu-id="8c839-136">Quando si **chiama \_ TTM setitle**, la stringa a cui fa riferimento *lParam* non deve superare 100 **TCHARs** di lunghezza, incluso il **null** di terminazione.</span><span class="sxs-lookup"><span data-stu-id="8c839-136">When calling **TTM\_SETTITLE**, the string pointed to by *lParam* must not exceed 100 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="8c839-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="8c839-137">Examples</span></span>

<span data-ttu-id="8c839-138">Nell'esempio seguente viene illustrato come aggiungere un titolo e un'icona di sistema a una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="8c839-138">The following example shows how to add a title and a system icon to a tooltip.</span></span>


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a><span data-ttu-id="8c839-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c839-139">Requirements</span></span>



| <span data-ttu-id="8c839-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c839-140">Requirement</span></span> | <span data-ttu-id="8c839-141">Valore</span><span class="sxs-lookup"><span data-stu-id="8c839-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c839-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c839-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8c839-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c839-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c839-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c839-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8c839-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8c839-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c839-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c839-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c839-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c839-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8c839-148">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8c839-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8c839-149">**TTM \_ SETTITLEW** (Unicode) e **TTM \_ setitlea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8c839-149">**TTM\_SETTITLEW** (Unicode) and **TTM\_SETTITLEA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8c839-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c839-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c839-151">Informazioni sui controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="8c839-151">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





