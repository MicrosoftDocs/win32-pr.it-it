---
description: Contiene una percentuale del ciclo di lavoro desiderata per un PIN o un canale in un controller PWM (Pulse Width Modulation).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: Struttura PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 98811ace7ce8fce760e10757b8bf012cc2b9b27d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401366"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a><span data-ttu-id="c2c7f-103">\_Struttura di \_ \_ \_ \_ \_ input percentuale del ciclo di lavoro attivo \_ per il pin PWM</span><span class="sxs-lookup"><span data-stu-id="c2c7f-103">PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT structure</span></span>

<span data-ttu-id="c2c7f-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="c2c7f-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c2c7f-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="c2c7f-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c2c7f-106">Contiene una percentuale del ciclo di lavoro desiderata per un PIN o un canale in un controller PWM (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="c2c7f-106">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2c7f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2c7f-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a><span data-ttu-id="c2c7f-108">Members</span><span class="sxs-lookup"><span data-stu-id="c2c7f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2c7f-109">**Percentuale**</span><span class="sxs-lookup"><span data-stu-id="c2c7f-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="c2c7f-110">Il ciclo di servizio del segnale PWM desiderato, come \_ percentuale di PWM, che è un valore ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="c2c7f-110">The desired PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2c7f-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2c7f-111">Requirements</span></span>



| <span data-ttu-id="c2c7f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2c7f-112">Requirement</span></span> | <span data-ttu-id="c2c7f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="c2c7f-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c7f-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2c7f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c2c7f-115">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c2c7f-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c2c7f-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2c7f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c2c7f-117">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="c2c7f-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c2c7f-118">Versione KMDF minima</span><span class="sxs-lookup"><span data-stu-id="c2c7f-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="c2c7f-119">1,19</span><span class="sxs-lookup"><span data-stu-id="c2c7f-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="c2c7f-120">Versione UMDF minima</span><span class="sxs-lookup"><span data-stu-id="c2c7f-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="c2c7f-121">2.19</span><span class="sxs-lookup"><span data-stu-id="c2c7f-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="c2c7f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2c7f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2c7f-123"><dt>PWM. h (incluso PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2c7f-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2c7f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2c7f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2c7f-125">**\_percentuale del \_ \_ ciclo di \_ \_ dazio attivo \_ set \_ di pin IOCTL**</span><span class="sxs-lookup"><span data-stu-id="c2c7f-125">**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




