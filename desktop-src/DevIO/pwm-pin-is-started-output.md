---
description: Contiene lo stato corrente di generazione del segnale di un PIN.
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: Struttura PWM_PIN_IS_STARTED_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 11350c3bb0fbec0f05ab3153c339f8fa30baeed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304466"
---
# <a name="pwm_pin_is_started_output-structure"></a><span data-ttu-id="b7781-103">\_La struttura di output del pin PWM \_ è stata \_ avviata \_</span><span class="sxs-lookup"><span data-stu-id="b7781-103">PWM\_PIN\_IS\_STARTED\_OUTPUT structure</span></span>

<span data-ttu-id="b7781-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b7781-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b7781-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b7781-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b7781-106">Contiene lo stato corrente di generazione del segnale di un PIN.</span><span class="sxs-lookup"><span data-stu-id="b7781-106">Contains the current signal generation state of a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7781-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7781-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="b7781-108">Members</span><span class="sxs-lookup"><span data-stu-id="b7781-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b7781-109">**IsStarted**</span><span class="sxs-lookup"><span data-stu-id="b7781-109">**IsStarted**</span></span>
</dt> <dd>

<span data-ttu-id="b7781-110">Stato di generazione del segnale corrente del PIN.</span><span class="sxs-lookup"><span data-stu-id="b7781-110">The pin current signal generation state.</span></span> <span data-ttu-id="b7781-111">Il valore true indica che il PIN è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="b7781-111">A value of true means that the pin is started.</span></span> <span data-ttu-id="b7781-112">Il valore false indica che il PIN è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="b7781-112">A value of false means that the pin is stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7781-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7781-113">Requirements</span></span>



| <span data-ttu-id="b7781-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7781-114">Requirement</span></span> | <span data-ttu-id="b7781-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b7781-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7781-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7781-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b7781-117">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b7781-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b7781-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7781-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b7781-119">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="b7781-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b7781-120">Versione KMDF minima</span><span class="sxs-lookup"><span data-stu-id="b7781-120">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="b7781-121">1,19</span><span class="sxs-lookup"><span data-stu-id="b7781-121">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="b7781-122">Versione UMDF minima</span><span class="sxs-lookup"><span data-stu-id="b7781-122">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="b7781-123">2.19</span><span class="sxs-lookup"><span data-stu-id="b7781-123">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="b7781-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7781-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7781-125"><dt>PWM. h (incluso PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7781-125"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7781-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7781-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7781-127">**\_pin PWM di IOCTL \_ \_ \_ avviato**</span><span class="sxs-lookup"><span data-stu-id="b7781-127">**IOCTL\_PWM\_PIN\_IS\_STARTED**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 




