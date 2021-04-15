---
title: Messaggio LB_GETLOCALE (winuser. h)
description: Ottiene le impostazioni locali correnti della casella di riepilogo. È possibile utilizzare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo \_ stile di ordinamento lbs) e del testo aggiunto dal \_ messaggio ADDSTRING lb.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- Controlli di Windows Message LB_GETLOCALE
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477290"
---
# <a name="lb_getlocale-message"></a><span data-ttu-id="2a0ec-105">LB \_ GetLocale messaggio</span><span class="sxs-lookup"><span data-stu-id="2a0ec-105">LB\_GETLOCALE message</span></span>

<span data-ttu-id="2a0ec-106">Ottiene le impostazioni locali correnti della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-106">Gets the current locale of the list box.</span></span> <span data-ttu-id="2a0ec-107">È possibile utilizzare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo stile di [**\_ ordinamento lbs**](list-box-styles.md) ) e del testo aggiunto dal [**messaggio \_ ADDSTRING lb**](lb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="2a0ec-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a0ec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a0ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a0ec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a0ec-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a0ec-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2a0ec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a0ec-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a0ec-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a0ec-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a0ec-113">Return value</span></span>

<span data-ttu-id="2a0ec-114">Il valore restituito specifica le impostazioni locali correnti della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-114">The return value specifies the current locale of the list box.</span></span> <span data-ttu-id="2a0ec-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene il codice paese/area geografica e il [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della lingua.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a0ec-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a0ec-116">Remarks</span></span>

<span data-ttu-id="2a0ec-117">L'identificatore della lingua è costituito da un identificatore di lingua e da un identificatore di lingua primaria.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-117">The language identifier consists of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="2a0ec-118">Utilizzare la macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) per estrarre l'identificatore di lingua principale da [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del valore restituito e la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) per estrarre l'identificatore del linguaggio di sottolinguaggio.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-118">Use the [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro to extract the primary language identifier from the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro to extract the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a0ec-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a0ec-119">Requirements</span></span>



| <span data-ttu-id="2a0ec-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a0ec-120">Requirement</span></span> | <span data-ttu-id="2a0ec-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2a0ec-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0ec-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a0ec-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2a0ec-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a0ec-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2a0ec-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a0ec-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2a0ec-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a0ec-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a0ec-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a0ec-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a0ec-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a0ec-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a0ec-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a0ec-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a0ec-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2a0ec-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2a0ec-130">**\_ADDSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="2a0ec-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="2a0ec-131">**\_impostazioni locali lb**</span><span class="sxs-lookup"><span data-stu-id="2a0ec-131">**LB\_SETLOCALE**</span></span>](lb-setlocale.md)
</dt> <dt>

<span data-ttu-id="2a0ec-132">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="2a0ec-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2a0ec-133">**PRIMARYLANGID**</span><span class="sxs-lookup"><span data-stu-id="2a0ec-133">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="2a0ec-134">**SUBLANGID**</span><span class="sxs-lookup"><span data-stu-id="2a0ec-134">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

