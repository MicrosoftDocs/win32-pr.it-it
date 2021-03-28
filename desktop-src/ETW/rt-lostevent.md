---
description: Questa classe di tipo evento viene utilizzata per indicare che gli eventi sono stati persi in una sessione in tempo reale. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: Classe RT_LostEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526383"
---
# <a name="rt_lostevent-class"></a><span data-ttu-id="3ebb5-104">RT \_ LostEvent (classe)</span><span class="sxs-lookup"><span data-stu-id="3ebb5-104">RT\_LostEvent class</span></span>

<span data-ttu-id="3ebb5-105">Questa classe di tipo evento viene utilizzata per indicare che gli eventi sono stati persi in una sessione in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-105">This event type class is used to indicate that events were lost in a real-time session.</span></span>

<span data-ttu-id="3ebb5-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ebb5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ebb5-107">Syntax</span></span>

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a><span data-ttu-id="3ebb5-108">Members</span><span class="sxs-lookup"><span data-stu-id="3ebb5-108">Members</span></span>

<span data-ttu-id="3ebb5-109">La classe **RT \_ LostEvent** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-109">The **RT\_LostEvent** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ebb5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ebb5-110">Remarks</span></span>

<span data-ttu-id="3ebb5-111">Il tipo di evento RTLostEvent indica che uno o più eventi sono stati persi.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-111">The RTLostEvent event type indicates that one or more events were lost.</span></span> <span data-ttu-id="3ebb5-112">Il tipo di evento RTLostBuffer indica che uno o più buffer sono stati persi.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-112">The RTLostBuffer event type indicates that one or more buffers were lost.</span></span> <span data-ttu-id="3ebb5-113">I tipi di evento RTLostEvent e RTLostBuffer vengono recapitati prima di elaborare gli eventi dal buffer.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-113">The RTLostEvent and RTLostBuffer event types are delivered before processing events from the buffer.</span></span>

<span data-ttu-id="3ebb5-114">RTLostFile indica che il file di supporto usato dall'autologger per acquisire gli eventi è andato perso.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-114">The RTLostFile indicates that the backing file used by the AutoLogger to capture events was lost.</span></span>

<span data-ttu-id="3ebb5-115">La perdita di eventi dipende dalla frequenza con cui gli eventi vengono registrati e dal tempo impiegato dall'utente per l'elaborazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-115">Loosing events depends on the frequency with which the events are logged and how much time the consumer spends processing the events.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ebb5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ebb5-116">Requirements</span></span>



| <span data-ttu-id="3ebb5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ebb5-117">Requirement</span></span> | <span data-ttu-id="3ebb5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3ebb5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------|
| <span data-ttu-id="3ebb5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ebb5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3ebb5-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ebb5-120">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3ebb5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ebb5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3ebb5-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3ebb5-122">None supported</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="3ebb5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ebb5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ebb5-124">**\_Evento perso**</span><span class="sxs-lookup"><span data-stu-id="3ebb5-124">**Lost\_Event**</span></span>](lost-event.md)
</dt> </dl>

 

 




