---
description: Metodo del costruttore.
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Costruttore CBaseObject. CBaseObject (ComBase. h)
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
ms.openlocfilehash: 4b13fe906af1900dbf067e8aa9273d811b3c1ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324689"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="56175-103">Costruttore CBaseObject. CBaseObject</span><span class="sxs-lookup"><span data-stu-id="56175-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="56175-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="56175-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="56175-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56175-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="56175-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="56175-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56175-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="56175-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="56175-108">Stringa che contiene il nome dell'oggetto, a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="56175-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56175-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="56175-109">Remarks</span></span>

<span data-ttu-id="56175-110">Questo metodo incrementa il conteggio degli oggetti attivi.</span><span class="sxs-lookup"><span data-stu-id="56175-110">This method increments the active-object count.</span></span> <span data-ttu-id="56175-111">Vedere [**CBaseObject:: ObjectsActive**](cbaseobject-objectsactive.md).</span><span class="sxs-lookup"><span data-stu-id="56175-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="56175-112">Allocare il parametro *pname* nella memoria statica:</span><span class="sxs-lookup"><span data-stu-id="56175-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="56175-113">La macro del [**nome**](name.md) viene compilata in **null** nelle compilazioni finali, in modo che le stringhe statiche vengano visualizzate solo nelle build di debug.</span><span class="sxs-lookup"><span data-stu-id="56175-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="56175-114">Per ulteriori informazioni, vedere [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span><span class="sxs-lookup"><span data-stu-id="56175-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56175-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56175-115">Requirements</span></span>



| <span data-ttu-id="56175-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="56175-116">Requirement</span></span> | <span data-ttu-id="56175-117">Valore</span><span class="sxs-lookup"><span data-stu-id="56175-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56175-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56175-118">Header</span></span><br/>  | <dl> <span data-ttu-id="56175-119"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56175-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="56175-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="56175-120">Library</span></span><br/> | <dl> <span data-ttu-id="56175-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="56175-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56175-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56175-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56175-123">**Classe CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="56175-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




