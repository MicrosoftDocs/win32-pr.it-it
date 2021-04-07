---
title: Messaggio TVM_SHOWINFOTIP (COMmctrl. h)
description: Mostra infotip per un elemento specificato in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ShowInfoTip di TreeView.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- Controlli di Windows Message TVM_SHOWINFOTIP
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874590"
---
# <a name="tvm_showinfotip-message"></a><span data-ttu-id="1d8e1-105">\_Messaggio SHOWINFOTIP TVM</span><span class="sxs-lookup"><span data-stu-id="1d8e1-105">TVM\_SHOWINFOTIP message</span></span>

<span data-ttu-id="1d8e1-106">Mostra infotip per un elemento specificato in un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="1d8e1-106">Shows the infotip for a specified item in a tree-view control.</span></span> <span data-ttu-id="1d8e1-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ ShowInfoTip di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) .</span><span class="sxs-lookup"><span data-stu-id="1d8e1-107">You can send this message explicitly or by using the [**TreeView\_ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) macro..</span></span>

## <a name="parameters"></a><span data-ttu-id="1d8e1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d8e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d8e1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d8e1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1d8e1-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1d8e1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1d8e1-111">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d8e1-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d8e1-112">Handle per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="1d8e1-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d8e1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d8e1-113">Return value</span></span>

<span data-ttu-id="1d8e1-114">Restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="1d8e1-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d8e1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d8e1-115">Remarks</span></span>

<span data-ttu-id="1d8e1-116">La maggior parte delle applicazioni non usa questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="1d8e1-116">Most applications do not use this message.</span></span> <span data-ttu-id="1d8e1-117">Infotip vengono visualizzate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1d8e1-117">Infotips are shown automatically.</span></span> <span data-ttu-id="1d8e1-118">Per altre informazioni, vedere uso di infotip di visualizzazione ad albero nella panoramica [sui controlli Tree-View](tree-view-controls.md) .</span><span class="sxs-lookup"><span data-stu-id="1d8e1-118">For more information, see Using Tree-view Infotips in the [About Tree-View Controls](tree-view-controls.md) overview.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d8e1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d8e1-119">Requirements</span></span>



| <span data-ttu-id="1d8e1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d8e1-120">Requirement</span></span> | <span data-ttu-id="1d8e1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1d8e1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8e1-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d8e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1d8e1-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d8e1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d8e1-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d8e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1d8e1-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1d8e1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d8e1-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d8e1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d8e1-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d8e1-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





