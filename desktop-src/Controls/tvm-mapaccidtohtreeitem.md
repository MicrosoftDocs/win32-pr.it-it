---
title: Messaggio TVM_MAPACCIDTOHTREEITEM (COMmctrl. h)
description: Esegue il mapping di un ID di accessibilità a un HTREEITEM.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- Controlli di Windows Message TVM_MAPACCIDTOHTREEITEM
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048102"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a><span data-ttu-id="d13db-104">\_Messaggio MAPACCIDTOHTREEITEM TVM</span><span class="sxs-lookup"><span data-stu-id="d13db-104">TVM\_MAPACCIDTOHTREEITEM message</span></span>

<span data-ttu-id="d13db-105">Esegue il mapping di un ID di accessibilità a un **HTREEITEM**.</span><span class="sxs-lookup"><span data-stu-id="d13db-105">Maps an accessibility ID to an **HTREEITEM**.</span></span>

## <a name="parameters"></a><span data-ttu-id="d13db-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d13db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d13db-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d13db-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d13db-108">**Uint** che contiene l'ID di accessibilità di cui eseguire il mapping a un **HTREEITEM**.</span><span class="sxs-lookup"><span data-stu-id="d13db-108">**UINT** that contains the accessibility ID to map to an **HTREEITEM**.</span></span> </dd> <dt>

<span data-ttu-id="d13db-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d13db-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d13db-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d13db-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d13db-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d13db-111">Return value</span></span>

<span data-ttu-id="d13db-112">Restituisce l' **HTREEITEM** a cui è stato eseguito il mapping dell'ID di accessibilità specificato.</span><span class="sxs-lookup"><span data-stu-id="d13db-112">Returns the **HTREEITEM** that the specified accessibility ID is mapped to.</span></span>

## <a name="remarks"></a><span data-ttu-id="d13db-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d13db-113">Remarks</span></span>

<span data-ttu-id="d13db-114">Quando si aggiunge un elemento a un controllo di visualizzazione albero, un **HTREEITEM** restituisce un valore che identifica in modo univoco l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d13db-114">When you add an item to a tree-view control an **HTREEITEM** returns, which uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="d13db-115">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="d13db-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d13db-116">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d13db-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d13db-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d13db-117">Requirements</span></span>



| <span data-ttu-id="d13db-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d13db-118">Requirement</span></span> | <span data-ttu-id="d13db-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d13db-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d13db-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d13db-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d13db-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d13db-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d13db-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d13db-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d13db-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d13db-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d13db-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d13db-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d13db-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d13db-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d13db-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d13db-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d13db-127">**\_MapAccIDToHTREEITEM TreeView**</span><span class="sxs-lookup"><span data-stu-id="d13db-127">**TreeView\_MapAccIDToHTREEITEM**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





