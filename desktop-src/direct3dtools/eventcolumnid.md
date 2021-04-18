---
description: Enumerazione utilizzata per indicare gli ID di colonna noti; si tratta di ID di colonna che tutte le implementazioni devono supportare.
MS-HAID: vspixengine.EVENTCOLUMNID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione EVENTCOLUMNID
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 908CC94B-DD06-4FEC-9DC8-B61D03D34F6E
api_name:
- EVENTCOLUMNID
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7bf01eda2c43df3f0ec9553f61341406c541cac9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303956"
---
# <a name="span-idvspixengineeventcolumnidspaneventcolumnid-enumeration"></a><span data-ttu-id="4b210-103"><span id="vspixengine.eventcolumnid"></span>Enumerazione EVENTCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="4b210-103"><span id="vspixengine.eventcolumnid"></span>EVENTCOLUMNID enumeration</span></span>

<span data-ttu-id="4b210-104">Enumerazione utilizzata per indicare gli ID di colonna noti; si tratta di ID di colonna che tutte le implementazioni devono supportare.</span><span class="sxs-lookup"><span data-stu-id="4b210-104">An enum used to indicate well-known column IDs; these are column IDs that all implementations should support.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b210-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b210-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="4b210-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="4b210-106">Constants</span></span>

<span data-ttu-id="4b210-107"><span id="EventColumnID_EVENTTYPE"></span><span id="eventcolumnid_eventtype"></span><span id="EVENTCOLUMNID_EVENTTYPE"></span>**EventColumnID \_ eventType**</span><span class="sxs-lookup"><span data-stu-id="4b210-107"><span id="EventColumnID_EVENTTYPE"></span><span id="eventcolumnid_eventtype"></span><span id="EVENTCOLUMNID_EVENTTYPE"></span>**EventColumnID\_EVENTTYPE**</span></span>  
<span data-ttu-id="4b210-108">ID che corrisponde alla colonna del tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="4b210-108">An ID that corresponds to the Event Type column.</span></span>

<span data-ttu-id="4b210-109"><span id="EventColumnID_EID"></span><span id="eventcolumnid_eid"></span><span id="EVENTCOLUMNID_EID"></span>**EventColumnID \_ Eid**</span><span class="sxs-lookup"><span data-stu-id="4b210-109"><span id="EventColumnID_EID"></span><span id="eventcolumnid_eid"></span><span id="EVENTCOLUMNID_EID"></span>**EventColumnID\_EID**</span></span>  
<span data-ttu-id="4b210-110">ID che corrisponde alla colonna ID evento.</span><span class="sxs-lookup"><span data-stu-id="4b210-110">An ID that corresponds to the Event ID column.</span></span>

<span data-ttu-id="4b210-111"><span id="EventColumnID_PARENTEID"></span><span id="eventcolumnid_parenteid"></span><span id="EVENTCOLUMNID_PARENTEID"></span>**\_PARENTEID EventColumnID**</span><span class="sxs-lookup"><span data-stu-id="4b210-111"><span id="EventColumnID_PARENTEID"></span><span id="eventcolumnid_parenteid"></span><span id="EVENTCOLUMNID_PARENTEID"></span>**EventColumnID\_PARENTEID**</span></span>  
<span data-ttu-id="4b210-112">ID che corrisponde alla colonna dell'ID evento padre.</span><span class="sxs-lookup"><span data-stu-id="4b210-112">An ID that corresponds to the Parent Event ID column.</span></span>

<span data-ttu-id="4b210-113"><span id="EventColumnID_EVENTNAME"></span><span id="eventcolumnid_eventname"></span><span id="EVENTCOLUMNID_EVENTNAME"></span>**\_Evento EventColumnID**</span><span class="sxs-lookup"><span data-stu-id="4b210-113"><span id="EventColumnID_EVENTNAME"></span><span id="eventcolumnid_eventname"></span><span id="EVENTCOLUMNID_EVENTNAME"></span>**EventColumnID\_EVENTNAME**</span></span>  
<span data-ttu-id="4b210-114">ID che corrisponde alla colonna nome evento.</span><span class="sxs-lookup"><span data-stu-id="4b210-114">An ID that corresponds to the Event Name column.</span></span>

<span data-ttu-id="4b210-115"><span id="EventColumnID_FRAME"></span><span id="eventcolumnid_frame"></span><span id="EVENTCOLUMNID_FRAME"></span>**\_Frame EventColumnID**</span><span class="sxs-lookup"><span data-stu-id="4b210-115"><span id="EventColumnID_FRAME"></span><span id="eventcolumnid_frame"></span><span id="EVENTCOLUMNID_FRAME"></span>**EventColumnID\_FRAME**</span></span>  
<span data-ttu-id="4b210-116">ID che corrisponde alla colonna del frame.</span><span class="sxs-lookup"><span data-stu-id="4b210-116">An ID that corresponds to the Frame column.</span></span>

<span data-ttu-id="4b210-117"><span id="EventColumnID_EVENTSTRING"></span><span id="eventcolumnid_eventstring"></span><span id="EVENTCOLUMNID_EVENTSTRING"></span>**\_EVENTSTRING EventColumnID**</span><span class="sxs-lookup"><span data-stu-id="4b210-117"><span id="EventColumnID_EVENTSTRING"></span><span id="eventcolumnid_eventstring"></span><span id="EVENTCOLUMNID_EVENTSTRING"></span>**EventColumnID\_EVENTSTRING**</span></span>  
<span data-ttu-id="4b210-118">ID che corrisponde alla stringa completa da analizzare per l'evento.</span><span class="sxs-lookup"><span data-stu-id="4b210-118">An ID that corresponds to the full string to be parsed for the event.</span></span>

<span data-ttu-id="4b210-119"><span id="EventColumnID_THISPTR"></span><span id="eventcolumnid_thisptr"></span><span id="EVENTCOLUMNID_THISPTR"></span>**\_THISPTR EventColumnID**</span><span class="sxs-lookup"><span data-stu-id="4b210-119"><span id="EventColumnID_THISPTR"></span><span id="eventcolumnid_thisptr"></span><span id="EVENTCOLUMNID_THISPTR"></span>**EventColumnID\_THISPTR**</span></span>  
<span data-ttu-id="4b210-120">ID che corrisponde all'handle di risorsa per il puntatore this.</span><span class="sxs-lookup"><span data-stu-id="4b210-120">An ID that corresponds to the resource handle for the this pointer.</span></span>

<span data-ttu-id="4b210-121"><span id="EventColumnID_STARTMOMENTHANDLE"></span><span id="eventcolumnid_startmomenthandle"></span><span id="EVENTCOLUMNID_STARTMOMENTHANDLE"></span>**\_STARTMOMENTHANDLE EventColumnID**</span><span class="sxs-lookup"><span data-stu-id="4b210-121"><span id="EventColumnID_STARTMOMENTHANDLE"></span><span id="eventcolumnid_startmomenthandle"></span><span id="EVENTCOLUMNID_STARTMOMENTHANDLE"></span>**EventColumnID\_STARTMOMENTHANDLE**</span></span>  
<span data-ttu-id="4b210-122">ID che corrisponde all'handle del momento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="4b210-122">An ID that corresponds to the moment handle for this event.</span></span>

<span data-ttu-id="4b210-123"><span id="EventColumnID_InfoQueueMessages"></span><span id="eventcolumnid_infoqueuemessages"></span><span id="EVENTCOLUMNID_INFOQUEUEMESSAGES"></span>**\_InfoQueueMessages EventColumnID**</span><span class="sxs-lookup"><span data-stu-id="4b210-123"><span id="EventColumnID_InfoQueueMessages"></span><span id="eventcolumnid_infoqueuemessages"></span><span id="EVENTCOLUMNID_INFOQUEUEMESSAGES"></span>**EventColumnID\_InfoQueueMessages**</span></span>  
<span data-ttu-id="4b210-124">ID che corrisponde a tutti i messaggi generati da questo oggetto nei livelli SDK.</span><span class="sxs-lookup"><span data-stu-id="4b210-124">An ID that corresponds to any message that this generated in the SDK layers.</span></span>

<span data-ttu-id="4b210-125"><span id="EventColumnID_ThreadId"></span><span id="eventcolumnid_threadid"></span><span id="EVENTCOLUMNID_THREADID"></span>**\_ThreadID EventColumnID**</span><span class="sxs-lookup"><span data-stu-id="4b210-125"><span id="EventColumnID_ThreadId"></span><span id="eventcolumnid_threadid"></span><span id="EVENTCOLUMNID_THREADID"></span>**EventColumnID\_ThreadId**</span></span>  
<span data-ttu-id="4b210-126">ID che corrisponde all'ID del thread.</span><span class="sxs-lookup"><span data-stu-id="4b210-126">An ID that corresponds to the Thread ID.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b210-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b210-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4b210-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b210-128">Header</span></span></p></td><td><span data-ttu-id="4b210-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4b210-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



