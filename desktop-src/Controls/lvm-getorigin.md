---
title: Messaggio LVM_GETORIGIN (COMmctrl. h)
description: Recupera l'origine della visualizzazione corrente per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView getOrigin.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- Controlli di Windows Message LVM_GETORIGIN
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af42f3d616aa609d6b9e41d3991adb9d68eb24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120982"
---
# <a name="lvm_getorigin-message"></a><span data-ttu-id="0ba2d-105">\_Messaggio GETORIGIN LVM</span><span class="sxs-lookup"><span data-stu-id="0ba2d-105">LVM\_GETORIGIN message</span></span>

<span data-ttu-id="0ba2d-106">Recupera l'origine della visualizzazione corrente per un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-106">Retrieves the current view origin for a list-view control.</span></span> <span data-ttu-id="0ba2d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ListView \_ getOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) .</span><span class="sxs-lookup"><span data-stu-id="0ba2d-107">You can send this message explicitly or by using the [**ListView\_GetOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ba2d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ba2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba2d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ba2d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0ba2d-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0ba2d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ba2d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ba2d-112">Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che riceve l'origine della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the view origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ba2d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ba2d-113">Return value</span></span>

<span data-ttu-id="0ba2d-114">Restituisce **true** se ha esito positivo o **false** se la visualizzazione corrente è elenco o visualizzazione report.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-114">Returns **TRUE** if successful, or **FALSE** if the current view is list or report view.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba2d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ba2d-115">Requirements</span></span>



| <span data-ttu-id="0ba2d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ba2d-116">Requirement</span></span> | <span data-ttu-id="0ba2d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0ba2d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba2d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ba2d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba2d-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ba2d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ba2d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ba2d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba2d-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0ba2d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ba2d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ba2d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ba2d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ba2d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

