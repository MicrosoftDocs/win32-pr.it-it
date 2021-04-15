---
title: Messaggio CB_SETLOCALE (winuser. h)
description: Un'applicazione invia un \_ messaggio setlocale di CB per impostare le impostazioni locali correnti della casella combinata. Se la casella combinata ha lo \_ stile di ordinamento CBS e le stringhe vengono aggiunte tramite CB \_ ADDSTRING, le impostazioni locali di una casella combinata influiscono sulla modalità di ordinamento degli elementi dell'elenco.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- Controlli di Windows Message CB_SETLOCALE
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477650"
---
# <a name="cb_setlocale-message"></a><span data-ttu-id="7c4c0-105">\_Messaggio setlocale di CB</span><span class="sxs-lookup"><span data-stu-id="7c4c0-105">CB\_SETLOCALE message</span></span>

<span data-ttu-id="7c4c0-106">Un'applicazione invia un **messaggio \_ setlocale di CB** per impostare le impostazioni locali correnti della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="7c4c0-106">An application sends a **CB\_SETLOCALE** message to set the current locale of the combo box.</span></span> <span data-ttu-id="7c4c0-107">Se la casella combinata ha lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) e le stringhe vengono aggiunte tramite [**CB \_ ADDSTRING**](cb-addstring.md), le impostazioni locali di una casella combinata influiscono sulla modalità di ordinamento degli elementi dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7c4c0-107">If the combo box has the [**CBS\_SORT**](combo-box-styles.md) style and strings are added using [**CB\_ADDSTRING**](cb-addstring.md), the locale of a combo box affects how list items are sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c4c0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c4c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c4c0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c4c0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4c0-110">Specifica l'identificatore delle impostazioni locali per la casella combinata da usare per l'ordinamento quando si aggiunge il testo.</span><span class="sxs-lookup"><span data-stu-id="7c4c0-110">Specifies the locale identifier for the combo box to use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="7c4c0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c4c0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4c0-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="7c4c0-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c4c0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c4c0-113">Return value</span></span>

<span data-ttu-id="7c4c0-114">Il valore restituito è l'identificatore delle impostazioni locali precedente.</span><span class="sxs-lookup"><span data-stu-id="7c4c0-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="7c4c0-115">Se *wParam* specifica le impostazioni locali non installate nel sistema, il valore restituito è CB \_ Err e le impostazioni locali correnti della casella combinata non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="7c4c0-115">If *wParam* specifies a locale not installed on the system, the return value is CB\_ERR and the current combo box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c4c0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c4c0-116">Remarks</span></span>

<span data-ttu-id="7c4c0-117">Usare la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) per creare un identificatore delle impostazioni locali e la macro [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) per costruire un identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="7c4c0-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier and the [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) macro to construct a language identifier.</span></span> <span data-ttu-id="7c4c0-118">L'identificatore di lingua è costituito da un identificatore di lingua principale e da un identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="7c4c0-118">The language identifier is made up of a primary language identifier and a sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4c0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c4c0-119">Requirements</span></span>



| <span data-ttu-id="7c4c0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c4c0-120">Requirement</span></span> | <span data-ttu-id="7c4c0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7c4c0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4c0-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c4c0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7c4c0-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c4c0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7c4c0-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c4c0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7c4c0-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c4c0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7c4c0-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c4c0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c4c0-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c4c0-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c4c0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c4c0-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c4c0-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7c4c0-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c4c0-130">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="7c4c0-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="7c4c0-131">**CB \_ GETlocale**</span><span class="sxs-lookup"><span data-stu-id="7c4c0-131">**CB\_GETLOCALE**</span></span>](cb-getlocale.md)
</dt> <dt>

<span data-ttu-id="7c4c0-132">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="7c4c0-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7c4c0-133">**MAKELANGID**</span><span class="sxs-lookup"><span data-stu-id="7c4c0-133">**MAKELANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[<span data-ttu-id="7c4c0-134">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="7c4c0-134">**MAKELCID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

