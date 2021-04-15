---
title: Messaggio HKM_GETHOTKEY (COMmctrl. h)
description: Ottiene il codice della chiave virtuale e i flag di modifica di un tasto di scelta da un controllo tasto di scelta.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- Controlli di Windows Message HKM_GETHOTKEY
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476319"
---
# <a name="hkm_gethotkey-message"></a><span data-ttu-id="d5172-104">\_Messaggio GETHOTKEY HKM</span><span class="sxs-lookup"><span data-stu-id="d5172-104">HKM\_GETHOTKEY message</span></span>

<span data-ttu-id="d5172-105">Ottiene il codice della chiave virtuale e i flag di modifica di un tasto di scelta da un controllo tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="d5172-105">Gets the virtual key code and modifier flags of a hot key from a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5172-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5172-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5172-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5172-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d5172-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d5172-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d5172-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5172-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d5172-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d5172-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5172-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5172-111">Return value</span></span>

<span data-ttu-id="d5172-112">Restituisce il codice della chiave virtuale e i flag di modifica.</span><span class="sxs-lookup"><span data-stu-id="d5172-112">Returns the virtual key code and modifier flags.</span></span> <span data-ttu-id="d5172-113">Il [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) del [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è il codice della chiave virtuale del tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="d5172-113">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="d5172-114">[**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) di **LOWORD** è il modificatore di chiave che specifica le chiavi che definiscono una combinazione di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="d5172-114">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that specifies the keys that define a hot key combination.</span></span> <span data-ttu-id="d5172-115">I flag di modifica possono essere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d5172-115">The modifier flags can be a combination of the following values.</span></span>



| <span data-ttu-id="d5172-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d5172-116">Value</span></span>            | <span data-ttu-id="d5172-117">Significato</span><span class="sxs-lookup"><span data-stu-id="d5172-117">Meaning</span></span>      |
|------------------|--------------|
| <span data-ttu-id="d5172-118">HOTKEYF \_ ALT</span><span class="sxs-lookup"><span data-stu-id="d5172-118">HOTKEYF\_ALT</span></span>     | <span data-ttu-id="d5172-119">ALT (tasto)</span><span class="sxs-lookup"><span data-stu-id="d5172-119">ALT key</span></span>      |
| <span data-ttu-id="d5172-120">\_controllo HOTKEYF</span><span class="sxs-lookup"><span data-stu-id="d5172-120">HOTKEYF\_CONTROL</span></span> | <span data-ttu-id="d5172-121">Chiave di controllo</span><span class="sxs-lookup"><span data-stu-id="d5172-121">CONTROL key</span></span>  |
| <span data-ttu-id="d5172-122">HOTKEYF \_ ext</span><span class="sxs-lookup"><span data-stu-id="d5172-122">HOTKEYF\_EXT</span></span>     | <span data-ttu-id="d5172-123">Chiave estesa</span><span class="sxs-lookup"><span data-stu-id="d5172-123">Extended key</span></span> |
| <span data-ttu-id="d5172-124">HOTKEYF \_ Shift</span><span class="sxs-lookup"><span data-stu-id="d5172-124">HOTKEYF\_SHIFT</span></span>   | <span data-ttu-id="d5172-125">Tasto MAIUSC</span><span class="sxs-lookup"><span data-stu-id="d5172-125">SHIFT key</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="d5172-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5172-126">Remarks</span></span>

<span data-ttu-id="d5172-127">Il valore a 16 bit restituito da questo messaggio può essere utilizzato come parametro *wParam* nel messaggio del [**\_ sehotkey WM**](/windows/desktop/inputdev/wm-sethotkey) .</span><span class="sxs-lookup"><span data-stu-id="d5172-127">The 16-bit value returned by this message can be used as the *wParam* parameter in the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5172-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5172-128">Requirements</span></span>



| <span data-ttu-id="d5172-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5172-129">Requirement</span></span> | <span data-ttu-id="d5172-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d5172-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5172-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5172-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d5172-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5172-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5172-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5172-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d5172-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5172-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5172-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5172-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5172-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5172-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

