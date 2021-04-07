---
title: Messaggio LB_SETLOCALE (winuser. h)
description: Imposta le impostazioni locali correnti della casella di riepilogo. È possibile utilizzare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo \_ stile di ordinamento lbs) e del testo aggiunto dal \_ messaggio ADDSTRING lb.
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- Controlli di Windows Message LB_SETLOCALE
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048648"
---
# <a name="lb_setlocale-message"></a><span data-ttu-id="1bb1b-105">\_Messaggio setlocale di lb</span><span class="sxs-lookup"><span data-stu-id="1bb1b-105">LB\_SETLOCALE message</span></span>

<span data-ttu-id="1bb1b-106">Imposta le impostazioni locali correnti della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="1bb1b-106">Sets the current locale of the list box.</span></span> <span data-ttu-id="1bb1b-107">È possibile utilizzare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo stile di [**\_ ordinamento lbs**](list-box-styles.md) ) e del testo aggiunto dal [**messaggio \_ ADDSTRING lb**](lb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="1bb1b-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="1bb1b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1bb1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bb1b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1bb1b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bb1b-110">Specifica l'identificatore delle impostazioni locali che la casella di riepilogo utilizzerà per l'ordinamento quando si aggiunge il testo.</span><span class="sxs-lookup"><span data-stu-id="1bb1b-110">Specifies the locale identifier that the list box will use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="1bb1b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1bb1b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bb1b-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="1bb1b-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bb1b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1bb1b-113">Return value</span></span>

<span data-ttu-id="1bb1b-114">Il valore restituito è l'identificatore delle impostazioni locali precedente.</span><span class="sxs-lookup"><span data-stu-id="1bb1b-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="1bb1b-115">Se il parametro *wParam* specifica impostazioni locali non installate nel sistema, il valore restituito è lb \_ Err e le impostazioni locali correnti della casella di riepilogo non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="1bb1b-115">If the *wParam* parameter specifies a locale that is not installed on the system, the return value is LB\_ERR and the current list box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bb1b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1bb1b-116">Remarks</span></span>

<span data-ttu-id="1bb1b-117">Usare la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) per costruire un identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="1bb1b-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bb1b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1bb1b-118">Requirements</span></span>



| <span data-ttu-id="1bb1b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bb1b-119">Requirement</span></span> | <span data-ttu-id="1bb1b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1bb1b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bb1b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bb1b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1bb1b-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1bb1b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1bb1b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bb1b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1bb1b-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1bb1b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1bb1b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1bb1b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bb1b-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bb1b-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bb1b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bb1b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="1bb1b-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1bb1b-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1bb1b-129">**\_ADDSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="1bb1b-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="1bb1b-130">**LB \_ GETlocale**</span><span class="sxs-lookup"><span data-stu-id="1bb1b-130">**LB\_GETLOCALE**</span></span>](lb-getlocale.md)
</dt> </dl>

 

