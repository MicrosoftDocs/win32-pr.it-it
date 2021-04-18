---
title: Messaggio PGM_GETPOS (COMmctrl. h)
description: Recupera la posizione di scorrimento corrente del controllo cercapersone. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro GetPos del cercapersone.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- Controlli di Windows Message PGM_GETPOS
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302049"
---
# <a name="pgm_getpos-message"></a><span data-ttu-id="5fd83-105">\_Messaggio GETPOS PGM</span><span class="sxs-lookup"><span data-stu-id="5fd83-105">PGM\_GETPOS message</span></span>

<span data-ttu-id="5fd83-106">Recupera la posizione di scorrimento corrente del controllo cercapersone.</span><span class="sxs-lookup"><span data-stu-id="5fd83-106">Retrieves the current scroll position of the pager control.</span></span> <span data-ttu-id="5fd83-107">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetPos del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) .</span><span class="sxs-lookup"><span data-stu-id="5fd83-107">You can send this message explicitly or use the [**Pager\_GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5fd83-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fd83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd83-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5fd83-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5fd83-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5fd83-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5fd83-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fd83-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5fd83-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5fd83-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd83-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fd83-113">Return value</span></span>

<span data-ttu-id="5fd83-114">Restituisce un valore INT che contiene la posizione di scorrimento corrente, in pixel.</span><span class="sxs-lookup"><span data-stu-id="5fd83-114">Returns an INT value that contains the current scroll position, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd83-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fd83-115">Requirements</span></span>



| <span data-ttu-id="5fd83-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fd83-116">Requirement</span></span> | <span data-ttu-id="5fd83-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5fd83-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd83-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fd83-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd83-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fd83-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5fd83-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fd83-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd83-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5fd83-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5fd83-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fd83-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fd83-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fd83-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





