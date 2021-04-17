---
description: Classe padre per gli eventi di intestazione del log. Questa classe è sempre la prima classe di traccia eventi inviata a un consumer (questo evento non viene inviato ai consumer in tempo reale). La sintassi seguente è semplificata dal codice MOF.
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: Classe EventTraceEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977671"
---
# <a name="eventtraceevent-class"></a><span data-ttu-id="58b6f-105">Classe EventTraceEvent</span><span class="sxs-lookup"><span data-stu-id="58b6f-105">EventTraceEvent class</span></span>

<span data-ttu-id="58b6f-106">Classe padre per gli eventi di intestazione del log.</span><span class="sxs-lookup"><span data-stu-id="58b6f-106">The parent class for log header events.</span></span> <span data-ttu-id="58b6f-107">Questa classe è sempre la prima classe di traccia eventi inviata a un consumer (questo evento non viene inviato ai consumer in tempo reale).</span><span class="sxs-lookup"><span data-stu-id="58b6f-107">This class is always the first event trace class sent to a consumer (this event is not sent to real-time consumers).</span></span>

<span data-ttu-id="58b6f-108">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="58b6f-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="58b6f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58b6f-109">Syntax</span></span>

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="58b6f-110">Members</span><span class="sxs-lookup"><span data-stu-id="58b6f-110">Members</span></span>

<span data-ttu-id="58b6f-111">La classe **EventTraceEvent** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="58b6f-111">The **EventTraceEvent** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="58b6f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58b6f-112">Requirements</span></span>



| <span data-ttu-id="58b6f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="58b6f-113">Requirement</span></span> | <span data-ttu-id="58b6f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="58b6f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58b6f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58b6f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="58b6f-116">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="58b6f-116">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="58b6f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58b6f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="58b6f-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58b6f-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58b6f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58b6f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58b6f-120">**\_SYSTEMTRACE MSNT**</span><span class="sxs-lookup"><span data-stu-id="58b6f-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="58b6f-121">**\_Intestazione EventTrace**</span><span class="sxs-lookup"><span data-stu-id="58b6f-121">**EventTrace\_Header**</span></span>](eventtrace-header.md)
</dt> </dl>

 

 




