---
description: Contiene il periodo di segnale di output effettivo per un controller PWM (Pulse Width Modulation).
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: Struttura PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: f63057299a8ef37ed1b38151958d2e0061ad2727
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748343"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a><span data-ttu-id="33574-103">Il \_ controller PWM \_ ottiene la struttura di \_ \_ output del periodo effettivo \_</span><span class="sxs-lookup"><span data-stu-id="33574-103">PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT structure</span></span>

<span data-ttu-id="33574-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="33574-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="33574-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="33574-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="33574-106">Contiene il periodo di segnale di output effettivo per un controller PWM (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="33574-106">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="33574-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33574-107">Syntax</span></span>


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="33574-108">Members</span><span class="sxs-lookup"><span data-stu-id="33574-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="33574-109">**ActualPeriod**</span><span class="sxs-lookup"><span data-stu-id="33574-109">**ActualPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="33574-110">Il periodo effettivo del segnale di output viene misurato nei canali di output del controller.</span><span class="sxs-lookup"><span data-stu-id="33574-110">The effective output signal period as it would be measured on the output channels of the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33574-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33574-111">Requirements</span></span>



| <span data-ttu-id="33574-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="33574-112">Requirement</span></span> | <span data-ttu-id="33574-113">Valore</span><span class="sxs-lookup"><span data-stu-id="33574-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33574-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33574-114">Minimum supported client</span></span><br/> | <span data-ttu-id="33574-115">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="33574-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="33574-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33574-116">Minimum supported server</span></span><br/> | <span data-ttu-id="33574-117">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="33574-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="33574-118">Versione KMDF minima</span><span class="sxs-lookup"><span data-stu-id="33574-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="33574-119">1,19</span><span class="sxs-lookup"><span data-stu-id="33574-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="33574-120">Versione UMDF minima</span><span class="sxs-lookup"><span data-stu-id="33574-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="33574-121">2.19</span><span class="sxs-lookup"><span data-stu-id="33574-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="33574-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33574-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="33574-123"><dt>PWM. h (incluso PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33574-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33574-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33574-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33574-125">**\_controller IOCTL PWM \_ ottiene il \_ \_ \_ periodo effettivo**</span><span class="sxs-lookup"><span data-stu-id="33574-125">**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 




