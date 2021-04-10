---
title: Messaggio TCM_GETCURFOCUS (COMmctrl. h)
description: Restituisce l'indice dell'elemento con lo stato attivo in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl GetCurFocus.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- Controlli di Windows Message TCM_GETCURFOCUS
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0d0f3d2bbd4a7cf0ab2a63c5a988f60768eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964792"
---
# <a name="tcm_getcurfocus-message"></a><span data-ttu-id="10a78-105">\_Messaggio TCM GETCURFOCUS</span><span class="sxs-lookup"><span data-stu-id="10a78-105">TCM\_GETCURFOCUS message</span></span>

<span data-ttu-id="10a78-106">Restituisce l'indice dell'elemento con lo stato attivo in un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="10a78-106">Returns the index of the item that has the focus in a tab control.</span></span> <span data-ttu-id="10a78-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) .</span><span class="sxs-lookup"><span data-stu-id="10a78-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="10a78-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="10a78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10a78-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10a78-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="10a78-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="10a78-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="10a78-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10a78-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="10a78-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="10a78-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10a78-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10a78-113">Return value</span></span>

<span data-ttu-id="10a78-114">Restituisce l'indice dell'elemento di scheda con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="10a78-114">Returns the index of the tab item that has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="10a78-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="10a78-115">Remarks</span></span>

<span data-ttu-id="10a78-116">L'elemento con lo stato attivo può essere diverso dall'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="10a78-116">The item that has the focus may be different than the selected item.</span></span>

## <a name="requirements"></a><span data-ttu-id="10a78-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10a78-117">Requirements</span></span>



| <span data-ttu-id="10a78-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="10a78-118">Requirement</span></span> | <span data-ttu-id="10a78-119">Valore</span><span class="sxs-lookup"><span data-stu-id="10a78-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10a78-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10a78-120">Minimum supported client</span></span><br/> | <span data-ttu-id="10a78-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10a78-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10a78-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10a78-122">Minimum supported server</span></span><br/> | <span data-ttu-id="10a78-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10a78-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10a78-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10a78-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="10a78-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10a78-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





