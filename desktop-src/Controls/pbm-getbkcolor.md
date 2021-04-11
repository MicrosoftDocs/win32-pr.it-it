---
title: Messaggio PBM_GETBKCOLOR (COMmctrl. h)
description: Ottiene il colore di sfondo dell'indicatore di stato.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- Controlli di Windows Message PBM_GETBKCOLOR
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874161"
---
# <a name="pbm_getbkcolor-message"></a><span data-ttu-id="4ca79-104">\_Messaggio GETBKCOLOR PBM</span><span class="sxs-lookup"><span data-stu-id="4ca79-104">PBM\_GETBKCOLOR message</span></span>

<span data-ttu-id="4ca79-105">Ottiene il colore di sfondo dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="4ca79-105">Gets the background color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ca79-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ca79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ca79-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ca79-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4ca79-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4ca79-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4ca79-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ca79-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4ca79-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4ca79-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ca79-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ca79-111">Return value</span></span>

<span data-ttu-id="4ca79-112">Restituisce il colore di sfondo dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="4ca79-112">Returns the background color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca79-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ca79-113">Remarks</span></span>

<span data-ttu-id="4ca79-114">Questo è il colore impostato dal messaggio [**\_ SETBKCOLOR di PBM**](pbm-setbkcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="4ca79-114">This is the color set by the [**PBM\_SETBKCOLOR**](pbm-setbkcolor.md) message.</span></span> <span data-ttu-id="4ca79-115">Il valore predefinito è CLR \_ default, definito in commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="4ca79-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="4ca79-116">Questa funzione ha effetto solo sulla modalità classica, non su qualsiasi stile di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4ca79-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca79-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ca79-117">Requirements</span></span>



| <span data-ttu-id="4ca79-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca79-118">Requirement</span></span> | <span data-ttu-id="4ca79-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4ca79-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca79-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ca79-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca79-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ca79-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4ca79-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ca79-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca79-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ca79-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ca79-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ca79-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ca79-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ca79-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





