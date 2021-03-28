---
description: Questa classe è la classe padre per gli eventi i/o divisi. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: Classe SplitIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: f2efc14ce8804852f983ebe9dcb852c8c0669899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978842"
---
# <a name="splitio-class"></a><span data-ttu-id="776e1-104">Classe SplitIo</span><span class="sxs-lookup"><span data-stu-id="776e1-104">SplitIo class</span></span>

<span data-ttu-id="776e1-105">Questa classe è la classe padre per gli eventi i/o divisi.</span><span class="sxs-lookup"><span data-stu-id="776e1-105">This class is the parent class for split IO events.</span></span>

<span data-ttu-id="776e1-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="776e1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="776e1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="776e1-107">Syntax</span></span>

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="776e1-108">Members</span><span class="sxs-lookup"><span data-stu-id="776e1-108">Members</span></span>

<span data-ttu-id="776e1-109">La classe **SplitIo** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="776e1-109">The **SplitIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="776e1-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="776e1-110">Remarks</span></span>

<span data-ttu-id="776e1-111">Per abilitare gli eventi di i/o suddivisi in una sessione di registrazione del kernel NT, specificare il flag di traccia di i/o **\_ \_ \_ \_ Split** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="776e1-111">To enable split IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_SPLIT\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="776e1-112">I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi di i/o suddivisi chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**SplitIoGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="776e1-112">Event trace consumers can implement special processing for split IO events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**SplitIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="776e1-113">Usare il tipo di evento seguente per identificare l'evento effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="776e1-113">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="776e1-114">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="776e1-114">Event type</span></span>           | <span data-ttu-id="776e1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="776e1-115">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="776e1-116">Valore del tipo di evento, 32</span><span class="sxs-lookup"><span data-stu-id="776e1-116">Event type value, 32</span></span> | <span data-ttu-id="776e1-117">Evento Split IO.</span><span class="sxs-lookup"><span data-stu-id="776e1-117">Split IO event.</span></span> <span data-ttu-id="776e1-118">La classe [**SplitIo \_ info**](splitio-info.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="776e1-118">The [**SplitIo\_Info**](splitio-info.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="776e1-119">Gli eventi di i/o suddivisi indicano che le richieste di i/o sono state suddivise in più richieste IO disco a causa dell'hardware sottostante del disco di mirroring.</span><span class="sxs-lookup"><span data-stu-id="776e1-119">Split IO events indicate that the IO requests have been split into multiple disk IO requests due to the underlying mirroring disk hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="776e1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="776e1-120">Requirements</span></span>



| <span data-ttu-id="776e1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="776e1-121">Requirement</span></span> | <span data-ttu-id="776e1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="776e1-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="776e1-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="776e1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="776e1-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="776e1-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="776e1-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="776e1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="776e1-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="776e1-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
