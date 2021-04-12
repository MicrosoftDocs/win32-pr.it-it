---
description: Enumerazione utilizzata per indicare il tipo di un evento.
MS-HAID: vspixengine.EVENTTYPE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione EVENTTYPE
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7A6F396-5BC0-4963-ABFD-ACB7AAE475F5
api_name:
- EVENTTYPE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 60af0090e440cd101211394cff98c9d9a501f4ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401176"
---
# <a name="span-idvspixengineeventtypespaneventtype-enumeration"></a><span data-ttu-id="edd18-103"><span id="vspixengine.eventtype"></span>Enumerazione EVENTTYPE</span><span class="sxs-lookup"><span data-stu-id="edd18-103"><span id="vspixengine.eventtype"></span>EVENTTYPE enumeration</span></span>

<span data-ttu-id="edd18-104">Enumerazione utilizzata per indicare il tipo di un evento.</span><span class="sxs-lookup"><span data-stu-id="edd18-104">An enum used to indicate the type of an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd18-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edd18-105">Syntax</span></span>

```cpp
C++ 
enum EVENTTYPE {
  ET_NONE = 0, 
  ET_SESSIONSTART, 
  ET_SESSIONEND, 
  ET_PROCESSSTART, 
  ET_PROCESSEND, 
  ET_FRAMEBEGIN, 
  ET_FRAMEEND, 
  ET_USEREVENTBEGIN, 
  ET_USEREVENTEND, 
  ET_USERMARKER, 
  ET_CALL, 
  ET_OBJECTCREATION, 
  ET_OBJECTPOPULATION, 
  ET_CALLSYNC, 
  ET_DRAW, 
  ET_DISPATCH 
};
```

## <a name="constants"></a><span data-ttu-id="edd18-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="edd18-106">Constants</span></span>

<span data-ttu-id="edd18-107"><span id="ET_NONE"></span><span id="et_none"></span>**ET \_ None**</span><span class="sxs-lookup"><span data-stu-id="edd18-107"><span id="ET_NONE"></span><span id="et_none"></span>**ET\_NONE**</span></span>  
<span data-ttu-id="edd18-108">Valore che corrisponde a nessun evento.</span><span class="sxs-lookup"><span data-stu-id="edd18-108">A value that corresponds to no event.</span></span>

<span data-ttu-id="edd18-109"><span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**\_SESSIONSTART et**</span><span class="sxs-lookup"><span data-stu-id="edd18-109"><span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**ET\_SESSIONSTART**</span></span>  
<span data-ttu-id="edd18-110">Valore che corrisponde a un evento di avvio della sessione.</span><span class="sxs-lookup"><span data-stu-id="edd18-110">A value that corresponds to a session start event.</span></span>

<span data-ttu-id="edd18-111"><span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**\_SESSIONEND et**</span><span class="sxs-lookup"><span data-stu-id="edd18-111"><span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**ET\_SESSIONEND**</span></span>  
<span data-ttu-id="edd18-112">Valore che corrisponde a un evento di fine sessione.</span><span class="sxs-lookup"><span data-stu-id="edd18-112">A value that corresponds to a session end event.</span></span>

<span data-ttu-id="edd18-113"><span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**\_PROCESSSTART et**</span><span class="sxs-lookup"><span data-stu-id="edd18-113"><span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET\_PROCESSSTART**</span></span>  
<span data-ttu-id="edd18-114">Valore che corrisponde a un evento di avvio del processo.</span><span class="sxs-lookup"><span data-stu-id="edd18-114">A value that corresponds to a process start event.</span></span>

<span data-ttu-id="edd18-115"><span id="ET_PROCESSEND"></span><span id="et_processend"></span>**\_PROCESSEND et**</span><span class="sxs-lookup"><span data-stu-id="edd18-115"><span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET\_PROCESSEND**</span></span>  
<span data-ttu-id="edd18-116">Valore che corrisponde a un evento di fine del processo.</span><span class="sxs-lookup"><span data-stu-id="edd18-116">A value that corresponds to a process end event.</span></span>

<span data-ttu-id="edd18-117"><span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**\_FRAMEBEGIN et**</span><span class="sxs-lookup"><span data-stu-id="edd18-117"><span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**ET\_FRAMEBEGIN**</span></span>  
<span data-ttu-id="edd18-118">Valore che corrisponde a un evento di inizio frame.</span><span class="sxs-lookup"><span data-stu-id="edd18-118">A value that corresponds to a frame begin event.</span></span>

<span data-ttu-id="edd18-119"><span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**\_FRAMEEND et**</span><span class="sxs-lookup"><span data-stu-id="edd18-119"><span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**ET\_FRAMEEND**</span></span>  
<span data-ttu-id="edd18-120">Valore che corrisponde a un evento di fine frame.</span><span class="sxs-lookup"><span data-stu-id="edd18-120">A value that corresponds to a frame end event.</span></span> <span data-ttu-id="edd18-121">Non usato.</span><span class="sxs-lookup"><span data-stu-id="edd18-121">Not used.</span></span>

<span data-ttu-id="edd18-122"><span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**\_USEREVENTBEGIN et**</span><span class="sxs-lookup"><span data-stu-id="edd18-122"><span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET\_USEREVENTBEGIN**</span></span>  
<span data-ttu-id="edd18-123">Valore che corrisponde a un evento di inizio evento utente.</span><span class="sxs-lookup"><span data-stu-id="edd18-123">A value that corresponds to a user-event begin event.</span></span>

<span data-ttu-id="edd18-124"><span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**\_USEREVENTEND et**</span><span class="sxs-lookup"><span data-stu-id="edd18-124"><span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET\_USEREVENTEND**</span></span>  
<span data-ttu-id="edd18-125">Valore che corrisponde a un evento di fine evento utente.</span><span class="sxs-lookup"><span data-stu-id="edd18-125">A value that corresponds to a user-event end event.</span></span> <span data-ttu-id="edd18-126">Non usato.</span><span class="sxs-lookup"><span data-stu-id="edd18-126">Not used.</span></span>

<span data-ttu-id="edd18-127"><span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**\_USERMARKER et**</span><span class="sxs-lookup"><span data-stu-id="edd18-127"><span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**ET\_USERMARKER**</span></span>  
<span data-ttu-id="edd18-128">Valore che corrisponde a un evento dell'indicatore utente.</span><span class="sxs-lookup"><span data-stu-id="edd18-128">A value that corresponds to a user-marker event.</span></span>

<span data-ttu-id="edd18-129"><span id="ET_CALL"></span><span id="et_call"></span>**chiamata a ET \_**</span><span class="sxs-lookup"><span data-stu-id="edd18-129"><span id="ET_CALL"></span><span id="et_call"></span>**ET\_CALL**</span></span>  
<span data-ttu-id="edd18-130">Valore che corrisponde a un evento di chiamata.</span><span class="sxs-lookup"><span data-stu-id="edd18-130">A value that corresponds to a call event.</span></span>

<span data-ttu-id="edd18-131"><span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**\_OBJECTCREATION et**</span><span class="sxs-lookup"><span data-stu-id="edd18-131"><span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET\_OBJECTCREATION**</span></span>  
<span data-ttu-id="edd18-132">Valore che corrisponde a un evento di creazione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="edd18-132">A value that corresponds to an object creation event.</span></span>

<span data-ttu-id="edd18-133"><span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**\_OBJECTPOPULATION et**</span><span class="sxs-lookup"><span data-stu-id="edd18-133"><span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET\_OBJECTPOPULATION**</span></span>  
<span data-ttu-id="edd18-134">Valore che corrisponde a un evento di popolamento dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="edd18-134">A value that corresponds to an object population event.</span></span>

<span data-ttu-id="edd18-135"><span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**\_CALLSYNC et**</span><span class="sxs-lookup"><span data-stu-id="edd18-135"><span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET\_CALLSYNC**</span></span>  

<span data-ttu-id="edd18-136"><span id="ET_DRAW"></span><span id="et_draw"></span>**\_disegni et**</span><span class="sxs-lookup"><span data-stu-id="edd18-136"><span id="ET_DRAW"></span><span id="et_draw"></span>**ET\_DRAW**</span></span>  
<span data-ttu-id="edd18-137">Valore che corrisponde a un evento di chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="edd18-137">A value that corresponds to a draw call event.</span></span>

<span data-ttu-id="edd18-138"><span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**invio di ET \_**</span><span class="sxs-lookup"><span data-stu-id="edd18-138"><span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**ET\_DISPATCH**</span></span>  
<span data-ttu-id="edd18-139">Valore che corrisponde a un evento dispatch.</span><span class="sxs-lookup"><span data-stu-id="edd18-139">A value that corresponds to a dispatch event.</span></span>

## <a name="requirements"></a><span data-ttu-id="edd18-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edd18-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="edd18-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="edd18-141">Header</span></span></p></td><td><span data-ttu-id="edd18-142">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="edd18-142">Vspixengine.h</span></span></td></tr></tbody></table>
