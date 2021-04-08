---
title: Messaggio CB_GETLOCALE (winuser. h)
description: Ottiene le impostazioni locali correnti della casella combinata. Le impostazioni locali vengono utilizzate per determinare l'ordinamento corretto del testo visualizzato per le caselle combinate con lo \_ stile di ordinamento CBS e il testo aggiunto tramite il \_ messaggio CB ADDSTRING.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- Controlli di Windows Message CB_GETLOCALE
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048355"
---
# <a name="cb_getlocale-message"></a><span data-ttu-id="796e8-105">\_Messaggio GETlocals CB</span><span class="sxs-lookup"><span data-stu-id="796e8-105">CB\_GETLOCALE message</span></span>

<span data-ttu-id="796e8-106">Ottiene le impostazioni locali correnti della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="796e8-106">Gets the current locale of the combo box.</span></span> <span data-ttu-id="796e8-107">Le impostazioni locali vengono utilizzate per determinare l'ordinamento corretto del testo visualizzato per le caselle combinate con lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) e il testo aggiunto tramite il messaggio [**CB \_ ADDSTRING**](cb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="796e8-107">The locale is used to determine the correct sorting order of displayed text for combo boxes with the [**CBS\_SORT**](combo-box-styles.md) style and text added by using the [**CB\_ADDSTRING**](cb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="796e8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="796e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="796e8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="796e8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="796e8-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="796e8-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="796e8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="796e8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="796e8-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="796e8-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="796e8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="796e8-113">Return value</span></span>

<span data-ttu-id="796e8-114">Il valore restituito specifica le impostazioni locali correnti della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="796e8-114">The return value specifies the current locale of the combo box.</span></span> <span data-ttu-id="796e8-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene il codice paese/area geografica e il [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della lingua.</span><span class="sxs-lookup"><span data-stu-id="796e8-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="796e8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="796e8-116">Remarks</span></span>

<span data-ttu-id="796e8-117">L'identificatore di lingua è costituito da un identificatore di lingua e da un identificatore di lingua primaria.</span><span class="sxs-lookup"><span data-stu-id="796e8-117">The language identifier is made up of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="796e8-118">La macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) Ottiene l'identificatore della lingua principale e la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) Ottiene l'identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="796e8-118">The [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro obtains the primary language identifier and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro obtains the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="796e8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="796e8-119">Requirements</span></span>



| <span data-ttu-id="796e8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="796e8-120">Requirement</span></span> | <span data-ttu-id="796e8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="796e8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="796e8-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="796e8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="796e8-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="796e8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="796e8-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="796e8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="796e8-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="796e8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="796e8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="796e8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="796e8-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="796e8-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="796e8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="796e8-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="796e8-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="796e8-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="796e8-130">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="796e8-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="796e8-131">**\_impostazioni locali CB**</span><span class="sxs-lookup"><span data-stu-id="796e8-131">**CB\_SETLOCALE**</span></span>](cb-setlocale.md)
</dt> <dt>

<span data-ttu-id="796e8-132">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="796e8-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="796e8-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="796e8-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="796e8-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="796e8-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="796e8-135">**PRIMARYLANGID**</span><span class="sxs-lookup"><span data-stu-id="796e8-135">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="796e8-136">**SUBLANGID**</span><span class="sxs-lookup"><span data-stu-id="796e8-136">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

