---
title: Messaggio TVM_MAPHTREEITEMTOACCID (COMmctrl. h)
description: Esegue il mapping di un HTREEITEM a un ID di accessibilità.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- Controlli di Windows Message TVM_MAPHTREEITEMTOACCID
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119798"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a><span data-ttu-id="39961-104">\_Messaggio MAPHTREEITEMTOACCID TVM</span><span class="sxs-lookup"><span data-stu-id="39961-104">TVM\_MAPHTREEITEMTOACCID message</span></span>

<span data-ttu-id="39961-105">Esegue il mapping di un **HTREEITEM** a un ID di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="39961-105">Maps an **HTREEITEM** to an accessibility ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="39961-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="39961-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39961-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39961-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="39961-108">**HTREEITEM** di cui è stato eseguito il mapping a un ID di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="39961-108">**HTREEITEM** that is mapped to an accessibility ID.</span></span></dd> <dt>

<span data-ttu-id="39961-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39961-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="39961-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="39961-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39961-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39961-111">Return value</span></span>

<span data-ttu-id="39961-112">Restituisce un ID di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="39961-112">Returns an accessibility ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="39961-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="39961-113">Remarks</span></span>

<span data-ttu-id="39961-114">Quando si aggiunge un elemento a un controllo di visualizzazione albero, viene restituito un handle **HTREEITEM** che identifica in modo univoco l'elemento.</span><span class="sxs-lookup"><span data-stu-id="39961-114">When you add an item to a tree-view control an **HTREEITEM** handle is returned that uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="39961-115">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="39961-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="39961-116">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="39961-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="39961-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39961-117">Requirements</span></span>



| <span data-ttu-id="39961-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="39961-118">Requirement</span></span> | <span data-ttu-id="39961-119">Valore</span><span class="sxs-lookup"><span data-stu-id="39961-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39961-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39961-120">Minimum supported client</span></span><br/> | <span data-ttu-id="39961-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39961-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39961-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39961-122">Minimum supported server</span></span><br/> | <span data-ttu-id="39961-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39961-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39961-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39961-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="39961-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="39961-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39961-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39961-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39961-127">**\_MapHTREEITEMtoAccID TreeView**</span><span class="sxs-lookup"><span data-stu-id="39961-127">**TreeView\_MapHTREEITEMtoAccID**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





