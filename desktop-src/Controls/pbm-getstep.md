---
title: Messaggio PBM_GETSTEP (COMmctrl. h)
description: Recupera l'incremento di passaggio da un indicatore di stato. L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che viene ricevuto un \_ messaggio STEPIT PBM. Per impostazione predefinita, l'incremento del passaggio è impostato su 10.
ms.assetid: 0cf3052a-cf86-4c0e-ad59-ddab7c6e3602
keywords:
- Controlli di Windows Message PBM_GETSTEP
topic_type:
- apiref
api_name:
- PBM_GETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dcc4adb18d2b60d2936c2cdc7ab79d00389b3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964564"
---
# <a name="pbm_getstep-message"></a><span data-ttu-id="8b2f8-106">\_Messaggio dell'istruzione GETstep di PBM</span><span class="sxs-lookup"><span data-stu-id="8b2f8-106">PBM\_GETSTEP message</span></span>

<span data-ttu-id="8b2f8-107">Recupera l'incremento di passaggio da un indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-107">Retrieves the step increment from a progress bar.</span></span> <span data-ttu-id="8b2f8-108">L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che viene ricevuto un messaggio [**\_ STEPIT PBM**](pbm-stepit.md) .</span><span class="sxs-lookup"><span data-stu-id="8b2f8-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="8b2f8-109">Per impostazione predefinita, l'incremento del passaggio è impostato su 10.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b2f8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b2f8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b2f8-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b2f8-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8b2f8-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8b2f8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b2f8-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8b2f8-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b2f8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b2f8-115">Return value</span></span>

<span data-ttu-id="8b2f8-116">Restituisce l'incremento del passaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-116">Returns the current step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b2f8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b2f8-117">Requirements</span></span>



| <span data-ttu-id="8b2f8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b2f8-118">Requirement</span></span> | <span data-ttu-id="8b2f8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8b2f8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b2f8-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b2f8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8b2f8-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b2f8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b2f8-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b2f8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8b2f8-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8b2f8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b2f8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b2f8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b2f8-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b2f8-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





