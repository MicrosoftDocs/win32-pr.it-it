---
description: Questa classe è la classe padre per gli eventi di traccia dello stack.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: Classe StackWalk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977623"
---
# <a name="stackwalk-class"></a><span data-ttu-id="3eefe-103">Classe StackWalk</span><span class="sxs-lookup"><span data-stu-id="3eefe-103">StackWalk class</span></span>

<span data-ttu-id="3eefe-104">Questa classe è la classe padre per gli eventi di traccia dello stack.</span><span class="sxs-lookup"><span data-stu-id="3eefe-104">This class is the parent class for stack tracing events.</span></span>

<span data-ttu-id="3eefe-105">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3eefe-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eefe-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3eefe-106">Syntax</span></span>

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="3eefe-107">Members</span><span class="sxs-lookup"><span data-stu-id="3eefe-107">Members</span></span>

<span data-ttu-id="3eefe-108">La classe **StackWalk** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="3eefe-108">The **StackWalk** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eefe-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3eefe-109">Remarks</span></span>

<span data-ttu-id="3eefe-110">Per abilitare la traccia dello stack degli eventi del kernel, chiamare la funzione [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) e specificare gli eventi del kernel e i tipi per i quali si desidera acquisire la traccia dello stack.</span><span class="sxs-lookup"><span data-stu-id="3eefe-110">To enable stack tracing of kernel events, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function and specify the kernel events and types for which you want to capture the stack trace.</span></span> <span data-ttu-id="3eefe-111">Per abilitare la traccia dello stack per altri eventi, impostare il membro **EnableProperty** di [**Abilita traccia \_ \_ parametri di traccia**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) per abilitare la **\_ \_ \_ \_ traccia dello stack della proprietà**.</span><span class="sxs-lookup"><span data-stu-id="3eefe-111">To enable stack tracing for other events, set the **EnableProperty** member of [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) to **EVENT\_ENABLE\_PROPERTY\_STACK\_TRACE**.</span></span>

<span data-ttu-id="3eefe-112">Usare il tipo di evento seguente per identificare l'evento effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="3eefe-112">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="3eefe-113">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="3eefe-113">Event type</span></span>           | <span data-ttu-id="3eefe-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3eefe-114">Description</span></span>                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eefe-115">Valore del tipo di evento, 32</span><span class="sxs-lookup"><span data-stu-id="3eefe-115">Event type value, 32</span></span> | <span data-ttu-id="3eefe-116">Evento di traccia dello stack.</span><span class="sxs-lookup"><span data-stu-id="3eefe-116">Stack tracing event.</span></span> <span data-ttu-id="3eefe-117">La classe MOF dell' [**\_ evento StackWalk**](stackwalk-event.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="3eefe-117">The [**StackWalk\_Event**](stackwalk-event.md) MOF class defines the event data for this event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3eefe-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3eefe-118">Requirements</span></span>



| <span data-ttu-id="3eefe-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eefe-119">Requirement</span></span> | <span data-ttu-id="3eefe-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3eefe-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3eefe-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eefe-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3eefe-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3eefe-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3eefe-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eefe-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3eefe-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3eefe-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 
