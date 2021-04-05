---
title: Messaggio CB_GETDROPPEDWIDTH (winuser. h)
description: Ottiene la larghezza minima consentita, in pixel, della casella di riepilogo di una casella combinata con l'elenco a \_ discesa CBS o \_ lo stile DropDownList CBS.
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- Controlli di Windows Message CB_GETDROPPEDWIDTH
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048362"
---
# <a name="cb_getdroppedwidth-message"></a><span data-ttu-id="24f04-104">\_Messaggio GETDROPPEDWIDTH CB</span><span class="sxs-lookup"><span data-stu-id="24f04-104">CB\_GETDROPPEDWIDTH message</span></span>

<span data-ttu-id="24f04-105">Ottiene la larghezza minima consentita, in pixel, della casella di riepilogo di una casella combinata con l'elenco a [**\_ discesa CBS**](combo-box-styles.md) o lo stile [**\_ DropDownList CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="24f04-105">Gets the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="24f04-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="24f04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f04-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24f04-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24f04-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="24f04-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="24f04-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24f04-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24f04-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="24f04-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f04-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24f04-111">Return value</span></span>

<span data-ttu-id="24f04-112">Se il messaggio ha esito positivo, il valore restituito è la larghezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="24f04-112">If the message succeeds, the return value is the width, in pixels.</span></span>

<span data-ttu-id="24f04-113">Se il messaggio ha esito negativo, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="24f04-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="24f04-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="24f04-114">Remarks</span></span>

<span data-ttu-id="24f04-115">Per impostazione predefinita, la larghezza minima consentita della casella di riepilogo a discesa è zero.</span><span class="sxs-lookup"><span data-stu-id="24f04-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="24f04-116">La larghezza della casella di riepilogo è la larghezza minima consentita o la larghezza della casella combinata, a seconda del valore maggiore.</span><span class="sxs-lookup"><span data-stu-id="24f04-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f04-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24f04-117">Requirements</span></span>



| <span data-ttu-id="24f04-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24f04-118">Requirement</span></span> | <span data-ttu-id="24f04-119">Valore</span><span class="sxs-lookup"><span data-stu-id="24f04-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24f04-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24f04-120">Minimum supported client</span></span><br/> | <span data-ttu-id="24f04-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24f04-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="24f04-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24f04-122">Minimum supported server</span></span><br/> | <span data-ttu-id="24f04-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24f04-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24f04-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24f04-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="24f04-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24f04-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24f04-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24f04-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f04-127">**CB \_ SETDROPPEDWIDTH**</span><span class="sxs-lookup"><span data-stu-id="24f04-127">**CB\_SETDROPPEDWIDTH**</span></span>](cb-setdroppedwidth.md)
</dt> </dl>

 

 





