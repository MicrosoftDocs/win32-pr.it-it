---
description: Contiene la percentuale del ciclo di lavoro corrente per un PIN o un canale in un controller PWM (Pulse Width Modulation).
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: Struttura PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 607fcb1ab429e7cbe9aee593f75d48f0f9d308bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126771"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a><span data-ttu-id="1af54-103">\_Struttura di \_ \_ \_ \_ \_ output percentuale del ciclo di dazio attivo \_ per pin PWM</span><span class="sxs-lookup"><span data-stu-id="1af54-103">PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT structure</span></span>

<span data-ttu-id="1af54-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="1af54-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1af54-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="1af54-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1af54-106">Contiene la percentuale del ciclo di lavoro corrente per un PIN o un canale in un controller PWM (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="1af54-106">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="1af54-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1af54-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="1af54-108">Members</span><span class="sxs-lookup"><span data-stu-id="1af54-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1af54-109">**Percentuale**</span><span class="sxs-lookup"><span data-stu-id="1af54-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="1af54-110">Il ciclo del dazio del segnale PWM corrente, come \_ percentuale di PWM, che è un valore ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="1af54-110">The current PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1af54-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1af54-111">Requirements</span></span>



| <span data-ttu-id="1af54-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1af54-112">Requirement</span></span> | <span data-ttu-id="1af54-113">Valore</span><span class="sxs-lookup"><span data-stu-id="1af54-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1af54-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1af54-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1af54-115">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1af54-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1af54-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1af54-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1af54-117">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="1af54-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1af54-118">Versione KMDF minima</span><span class="sxs-lookup"><span data-stu-id="1af54-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="1af54-119">1,19</span><span class="sxs-lookup"><span data-stu-id="1af54-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="1af54-120">Versione UMDF minima</span><span class="sxs-lookup"><span data-stu-id="1af54-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="1af54-121">2.19</span><span class="sxs-lookup"><span data-stu-id="1af54-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="1af54-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1af54-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1af54-123"><dt>PWM. h (incluso PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1af54-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af54-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1af54-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af54-125">**\_percentuale del \_ ciclo di lavoro per pin PWM \_ get \_ attivo \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1af54-125">**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




