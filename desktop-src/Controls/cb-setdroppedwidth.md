---
title: Messaggio CB_SETDROPPEDWIDTH (winuser. h)
description: Un'applicazione invia il \_ messaggio CB SETDROPPEDWIDTH per impostare la larghezza minima consentita, in pixel, della casella di riepilogo di una casella combinata con lo \_ stile di menu a discesa CBS o CBS \_ DropDownList.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- Controlli di Windows Message CB_SETDROPPEDWIDTH
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873789"
---
# <a name="cb_setdroppedwidth-message"></a><span data-ttu-id="58292-104">\_Messaggio SETDROPPEDWIDTH CB</span><span class="sxs-lookup"><span data-stu-id="58292-104">CB\_SETDROPPEDWIDTH message</span></span>

<span data-ttu-id="58292-105">Un'applicazione invia il messaggio **CB \_ SETDROPPEDWIDTH** per impostare la larghezza minima consentita, in pixel, della casella di riepilogo di una casella combinata con lo stile di [**menu a \_ discesa CBS**](combo-box-styles.md) o [**CBS \_ DropDownList**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="58292-105">An application sends the **CB\_SETDROPPEDWIDTH** message to set the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="58292-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58292-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58292-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58292-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58292-108">Larghezza minima consentita della casella di riepilogo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="58292-108">The minimum allowable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="58292-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58292-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58292-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="58292-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58292-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58292-111">Return value</span></span>

<span data-ttu-id="58292-112">Se il messaggio ha esito positivo, il valore restituito è la nuova larghezza della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="58292-112">If the message is successful, The return value is the new width of the list box.</span></span>

<span data-ttu-id="58292-113">Se il messaggio ha esito negativo, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="58292-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="58292-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="58292-114">Remarks</span></span>

<span data-ttu-id="58292-115">Per impostazione predefinita, la larghezza minima consentita della casella di riepilogo a discesa è zero.</span><span class="sxs-lookup"><span data-stu-id="58292-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="58292-116">La larghezza della casella di riepilogo è la larghezza minima consentita o la larghezza della casella combinata, a seconda del valore maggiore.</span><span class="sxs-lookup"><span data-stu-id="58292-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="58292-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58292-117">Requirements</span></span>



| <span data-ttu-id="58292-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="58292-118">Requirement</span></span> | <span data-ttu-id="58292-119">Valore</span><span class="sxs-lookup"><span data-stu-id="58292-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58292-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58292-120">Minimum supported client</span></span><br/> | <span data-ttu-id="58292-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58292-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="58292-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58292-122">Minimum supported server</span></span><br/> | <span data-ttu-id="58292-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58292-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58292-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58292-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="58292-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58292-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58292-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58292-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58292-127">**CB \_ GETDROPPEDWIDTH**</span><span class="sxs-lookup"><span data-stu-id="58292-127">**CB\_GETDROPPEDWIDTH**</span></span>](cb-getdroppedwidth.md)
</dt> </dl>

 

 





