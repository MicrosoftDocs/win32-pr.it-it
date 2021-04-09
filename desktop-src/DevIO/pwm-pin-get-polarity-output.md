---
description: Contiene un valore di polarità da restituire.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: Struttura PWM_PIN_GET_POLARITY_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 81cf7b658a0024c3280db1523af34aaf2ef17262
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966085"
---
# <a name="pwm_pin_get_polarity_output-structure"></a><span data-ttu-id="299a2-103">Struttura di output del pin PWM per \_ ottenere la \_ \_ polarità \_</span><span class="sxs-lookup"><span data-stu-id="299a2-103">PWM\_PIN\_GET\_POLARITY\_OUTPUT structure</span></span>

<span data-ttu-id="299a2-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="299a2-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="299a2-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="299a2-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="299a2-106">Contiene un valore di polarità da restituire.</span><span class="sxs-lookup"><span data-stu-id="299a2-106">Contains a polarity value to return.</span></span>

## <a name="syntax"></a><span data-ttu-id="299a2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="299a2-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="299a2-108">Members</span><span class="sxs-lookup"><span data-stu-id="299a2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="299a2-109">**Polarità**</span><span class="sxs-lookup"><span data-stu-id="299a2-109">**Polarity**</span></span>
</dt> <dd>

<span data-ttu-id="299a2-110">Polarità del PIN o del canale come valore di [**\_ polarità PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) .</span><span class="sxs-lookup"><span data-stu-id="299a2-110">The polarity of the pin or channel as a [**PWM\_POLARITY**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) value.</span></span> <span data-ttu-id="299a2-111">La polarità è attiva alta o attiva bassa.</span><span class="sxs-lookup"><span data-stu-id="299a2-111">The polarity is either Active High or Active Low.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="299a2-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="299a2-112">Requirements</span></span>



| <span data-ttu-id="299a2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="299a2-113">Requirement</span></span> | <span data-ttu-id="299a2-114">Valore</span><span class="sxs-lookup"><span data-stu-id="299a2-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="299a2-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="299a2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="299a2-116">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="299a2-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="299a2-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="299a2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="299a2-118">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="299a2-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="299a2-119">Versione KMDF minima</span><span class="sxs-lookup"><span data-stu-id="299a2-119">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="299a2-120">1,19</span><span class="sxs-lookup"><span data-stu-id="299a2-120">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="299a2-121">Versione UMDF minima</span><span class="sxs-lookup"><span data-stu-id="299a2-121">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="299a2-122">2.19</span><span class="sxs-lookup"><span data-stu-id="299a2-122">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="299a2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="299a2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="299a2-124"><dt>PWM. h (incluso PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="299a2-124"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="299a2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="299a2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299a2-126">**\_ \_ \_ polarità pin IOCTL \_ PWM**</span><span class="sxs-lookup"><span data-stu-id="299a2-126">**IOCTL\_PWM\_PIN\_GET\_POLARITY**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[<span data-ttu-id="299a2-127">**\_polarità PWM**</span><span class="sxs-lookup"><span data-stu-id="299a2-127">**PWM\_POLARITY**</span></span>](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

