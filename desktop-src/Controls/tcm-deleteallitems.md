---
title: Messaggio TCM_DELETEALLITEMS (COMmctrl. h)
description: Rimuove tutti gli elementi da un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl DeleteAllItems.
ms.assetid: 733494c4-38f4-44ba-98d2-c33a8d63c3b7
keywords:
- Controlli di Windows Message TCM_DELETEALLITEMS
topic_type:
- apiref
api_name:
- TCM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b73a91cd6ec3b5472b6e7da2127f8224062cfbbc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518736"
---
# <a name="tcm_deleteallitems-message"></a><span data-ttu-id="768d1-105">\_Messaggio TCM DELETEALLITEMS</span><span class="sxs-lookup"><span data-stu-id="768d1-105">TCM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="768d1-106">Rimuove tutti gli elementi da un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="768d1-106">Removes all items from a tab control.</span></span> <span data-ttu-id="768d1-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) .</span><span class="sxs-lookup"><span data-stu-id="768d1-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="768d1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="768d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="768d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="768d1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="768d1-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="768d1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="768d1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="768d1-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="768d1-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="768d1-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="768d1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="768d1-113">Return value</span></span>

<span data-ttu-id="768d1-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="768d1-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="768d1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="768d1-115">Requirements</span></span>



| <span data-ttu-id="768d1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="768d1-116">Requirement</span></span> | <span data-ttu-id="768d1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="768d1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="768d1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="768d1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="768d1-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="768d1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="768d1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="768d1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="768d1-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="768d1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="768d1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="768d1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="768d1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="768d1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





