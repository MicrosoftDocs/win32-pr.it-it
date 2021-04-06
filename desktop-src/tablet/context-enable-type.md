---
description: Indica se i messaggi di contesto devono essere inviati alla routine della finestra proprietaria.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: Enumerazione CONTEXT_ENABLE_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd741eeff1cc3e2ce055a84dd646c3aa2563f217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758855"
---
# <a name="context_enable_type-enumeration"></a><span data-ttu-id="3f82e-103">\_Enumerazione del tipo abilitata per il contesto \_</span><span class="sxs-lookup"><span data-stu-id="3f82e-103">CONTEXT\_ENABLE\_TYPE enumeration</span></span>

<span data-ttu-id="3f82e-104">Indica se i messaggi di contesto devono essere inviati alla routine della finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="3f82e-104">Indicates whether context messages should be sent to the owning window's window procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f82e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f82e-105">Syntax</span></span>


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="3f82e-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="3f82e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3f82e-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**\_Abilita contesto**</span><span class="sxs-lookup"><span data-stu-id="3f82e-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**CONTEXT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="3f82e-108">È necessario abilitare il contesto della tavoletta, in modo da inviare messaggi di contesto alla routine della finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="3f82e-108">The tablet context should be enabled, resulting in context messages being sent to the owning window's window procedure.</span></span>

</dd> <dt>

<span data-ttu-id="3f82e-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**\_disabilitazione del contesto**</span><span class="sxs-lookup"><span data-stu-id="3f82e-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**CONTEXT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="3f82e-110">Il contesto del tablet deve essere disabilitato, impedendo l'invio di altri messaggi di contesto alla routine della finestra o al sink di evento della finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="3f82e-110">The tablet context should be disabled, preventing any further context messages from being sent to the owning window's window procedure or event sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f82e-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f82e-111">Requirements</span></span>



| <span data-ttu-id="3f82e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f82e-112">Requirement</span></span> | <span data-ttu-id="3f82e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="3f82e-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3f82e-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f82e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3f82e-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3f82e-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3f82e-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f82e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3f82e-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3f82e-117">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="3f82e-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f82e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f82e-119">**Metodo ITablet:: CreateContext**</span><span class="sxs-lookup"><span data-stu-id="3f82e-119">**ITablet::CreateContext Method**</span></span>](itablet-createcontext.md)
</dt> </dl>

 

 




