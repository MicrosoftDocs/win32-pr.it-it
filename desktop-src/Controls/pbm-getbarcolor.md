---
title: Messaggio PBM_GETBARCOLOR (COMmctrl. h)
description: Ottiene il colore dell'indicatore di stato.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- Controlli di Windows Message PBM_GETBARCOLOR
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35586d3483d1d487f740a1a3d991c884c814f452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120518"
---
# <a name="pbm_getbarcolor-message"></a><span data-ttu-id="8c586-104">\_Messaggio GETBARCOLOR PBM</span><span class="sxs-lookup"><span data-stu-id="8c586-104">PBM\_GETBARCOLOR message</span></span>

<span data-ttu-id="8c586-105">Ottiene il colore dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="8c586-105">Gets the color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c586-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c586-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c586-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c586-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8c586-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8c586-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8c586-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c586-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8c586-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8c586-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c586-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c586-111">Return value</span></span>

<span data-ttu-id="8c586-112">Restituisce il colore dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="8c586-112">Returns the color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c586-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c586-113">Remarks</span></span>

<span data-ttu-id="8c586-114">Questo è il colore impostato dal messaggio [**\_ SETBARCOLOR di PBM**](pbm-setbarcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="8c586-114">This is the color set by the [**PBM\_SETBARCOLOR**](pbm-setbarcolor.md) message.</span></span> <span data-ttu-id="8c586-115">Il valore predefinito è CLR \_ default, definito in commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="8c586-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="8c586-116">Questa funzione ha effetto solo sulla modalità classica, non su qualsiasi stile di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8c586-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c586-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c586-117">Requirements</span></span>



| <span data-ttu-id="8c586-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c586-118">Requirement</span></span> | <span data-ttu-id="8c586-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8c586-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c586-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c586-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c586-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c586-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c586-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c586-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c586-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c586-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c586-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c586-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c586-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c586-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





