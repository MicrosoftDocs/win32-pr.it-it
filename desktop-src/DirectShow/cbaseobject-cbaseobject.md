---
description: 'Costruttore CBaseObject.CBaseObject : metodo costruttore.'
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Costruttore CBaseObject.CBaseObject (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14fa2d3d38d42fa0feb387b477205cc51e0b6b87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099619"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="15124-103">Costruttore CBaseObject.CBaseObject</span><span class="sxs-lookup"><span data-stu-id="15124-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="15124-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="15124-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="15124-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15124-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="15124-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="15124-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15124-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="15124-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="15124-108">Stringa che contiene il nome dell'oggetto a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="15124-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15124-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="15124-109">Remarks</span></span>

<span data-ttu-id="15124-110">Questo metodo incrementa il conteggio degli oggetti attivi.</span><span class="sxs-lookup"><span data-stu-id="15124-110">This method increments the active-object count.</span></span> <span data-ttu-id="15124-111">Vedere [**CBaseObject::ObjectsActive.**](cbaseobject-objectsactive.md)</span><span class="sxs-lookup"><span data-stu-id="15124-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="15124-112">Allocare il *parametro pName* nella memoria statica:</span><span class="sxs-lookup"><span data-stu-id="15124-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="15124-113">La macro [**NAME**](name.md) viene compilata come **NULL nelle** build per la vendita al dettaglio, in modo che le stringhe statiche vengano visualizzate solo nelle build di debug.</span><span class="sxs-lookup"><span data-stu-id="15124-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="15124-114">Per altre informazioni, vedere [**DbgDumpObjectRegister.**](dbgdumpobjectregister.md)</span><span class="sxs-lookup"><span data-stu-id="15124-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15124-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15124-115">Requirements</span></span>



| <span data-ttu-id="15124-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="15124-116">Requirement</span></span> | <span data-ttu-id="15124-117">Valore</span><span class="sxs-lookup"><span data-stu-id="15124-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15124-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15124-118">Header</span></span><br/>  | <dl> <span data-ttu-id="15124-119"><dt>Combase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="15124-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15124-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="15124-120">Library</span></span><br/> | <dl> <span data-ttu-id="15124-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="15124-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15124-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15124-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15124-123">**Classe CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="15124-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




