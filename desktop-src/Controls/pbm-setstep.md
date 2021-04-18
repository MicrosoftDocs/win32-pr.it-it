---
title: Messaggio PBM_SETSTEP (COMmctrl. h)
description: Specifica l'incremento del passaggio per un indicatore di stato. L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che viene ricevuto un \_ messaggio STEPIT PBM. Per impostazione predefinita, l'incremento del passaggio è impostato su 10.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- Controlli di Windows Message PBM_SETSTEP
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240d09aeadcd7994187704d0b5a4630ab1b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302054"
---
# <a name="pbm_setstep-message"></a><span data-ttu-id="e862e-106">Messaggio in fase di esecuzione di PBM \_</span><span class="sxs-lookup"><span data-stu-id="e862e-106">PBM\_SETSTEP message</span></span>

<span data-ttu-id="e862e-107">Specifica l'incremento del passaggio per un indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="e862e-107">Specifies the step increment for a progress bar.</span></span> <span data-ttu-id="e862e-108">L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che viene ricevuto un messaggio [**\_ STEPIT PBM**](pbm-stepit.md) .</span><span class="sxs-lookup"><span data-stu-id="e862e-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="e862e-109">Per impostazione predefinita, l'incremento del passaggio è impostato su 10.</span><span class="sxs-lookup"><span data-stu-id="e862e-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="e862e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e862e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e862e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e862e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e862e-112">Incremento nuovo passaggio.</span><span class="sxs-lookup"><span data-stu-id="e862e-112">New step increment.</span></span>

</dd> <dt>

<span data-ttu-id="e862e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e862e-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e862e-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e862e-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e862e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e862e-115">Return value</span></span>

<span data-ttu-id="e862e-116">Restituisce l'incremento del passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="e862e-116">Returns the previous step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="e862e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e862e-117">Requirements</span></span>



| <span data-ttu-id="e862e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e862e-118">Requirement</span></span> | <span data-ttu-id="e862e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e862e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e862e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e862e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e862e-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e862e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e862e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e862e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e862e-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e862e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e862e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e862e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e862e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e862e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





