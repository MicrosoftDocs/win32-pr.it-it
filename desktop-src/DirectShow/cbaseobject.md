---
description: La classe CBaseObject è una classe astratta per l'implementazione di oggetti DirectShow. Per implementare oggetti Component Object Model (COM), usare la classe CUnknown che deriva da CBaseObject.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: Classe CBaseObject (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbc3e072c31618dab6a7bc07048728f60dbcf0d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326430"
---
# <a name="cbaseobject-class"></a><span data-ttu-id="de5fa-104">Classe CBaseObject</span><span class="sxs-lookup"><span data-stu-id="de5fa-104">CBaseObject class</span></span>

<span data-ttu-id="de5fa-105">La classe **CBaseObject** è una classe astratta per l'implementazione di oggetti DirectShow.</span><span class="sxs-lookup"><span data-stu-id="de5fa-105">The **CBaseObject** class is an abstract class for implementing DirectShow objects.</span></span> <span data-ttu-id="de5fa-106">Per implementare oggetti Component Object Model (COM), usare la classe [**CUnknown**](cunknown.md) che deriva da **CBaseObject**.</span><span class="sxs-lookup"><span data-stu-id="de5fa-106">To implement Component Object Model (COM) objects, use the [**CUnknown**](cunknown.md) class, which derives from **CBaseObject**.</span></span>



| <span data-ttu-id="de5fa-107">Metodi della classe</span><span class="sxs-lookup"><span data-stu-id="de5fa-107">Class Methods</span></span>                                      | <span data-ttu-id="de5fa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de5fa-108">Description</span></span>                            |
|----------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="de5fa-109">**CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="de5fa-109">**CBaseObject**</span></span>](cbaseobject-cbaseobject.md)     | <span data-ttu-id="de5fa-110">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="de5fa-110">Constructor method.</span></span>                    |
| [<span data-ttu-id="de5fa-111">**~ CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="de5fa-111">**~CBaseObject**</span></span>](cbaseobject--cbaseobject.md)   | <span data-ttu-id="de5fa-112">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="de5fa-112">Destructor method.</span></span>                     |
| [<span data-ttu-id="de5fa-113">**ObjectsActive**</span><span class="sxs-lookup"><span data-stu-id="de5fa-113">**ObjectsActive**</span></span>](cbaseobject-objectsactive.md) | <span data-ttu-id="de5fa-114">Recupera il numero di oggetti attivi.</span><span class="sxs-lookup"><span data-stu-id="de5fa-114">Retrieves the count of active objects.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="de5fa-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="de5fa-115">Remarks</span></span>

<span data-ttu-id="de5fa-116">La maggior parte delle classi base di DirectShow derivano da **CBaseObject**.</span><span class="sxs-lookup"><span data-stu-id="de5fa-116">Most of the DirectShow base classes derive from **CBaseObject**.</span></span> <span data-ttu-id="de5fa-117">Questa classe fornisce assistenza per il debug mantenendo un conteggio di tutti gli oggetti DirectShow attivi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="de5fa-117">This class provides debugging assistance by keeping a count of all the DirectShow objects active during run time.</span></span> <span data-ttu-id="de5fa-118">Il numero di oggetti viene archiviato in una variabile membro statica della classe:</span><span class="sxs-lookup"><span data-stu-id="de5fa-118">The object count is stored in a class-static member variable:</span></span>


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



<span data-ttu-id="de5fa-119">Nelle build di debug, la DLL asserirà se viene scaricata mentre il conteggio oggetti è maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="de5fa-119">In debug builds, the DLL will assert if it is unloaded while the object count is greater than zero.</span></span> <span data-ttu-id="de5fa-120">In questo modo è più semplice rilevare le perdite dovute a problemi di conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="de5fa-120">This makes it easier to track down leaks caused by reference-counting problems.</span></span>

<span data-ttu-id="de5fa-121">Il costruttore **CBaseObject** accetta un argomento, un nome di debug per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="de5fa-121">The **CBaseObject** constructor takes one argument, a debugging name for the object.</span></span> <span data-ttu-id="de5fa-122">Questo nome viene archiviato in una tabella globale della DLL.</span><span class="sxs-lookup"><span data-stu-id="de5fa-122">This name is stored in a global table in the DLL.</span></span> <span data-ttu-id="de5fa-123">La funzione [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) formatta un elenco degli oggetti attivi nella dll e li invia all'output di debug.</span><span class="sxs-lookup"><span data-stu-id="de5fa-123">The [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function formats a list of the objects active in the DLL, and sends it to the debug output.</span></span>

## <a name="requirements"></a><span data-ttu-id="de5fa-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de5fa-124">Requirements</span></span>



| <span data-ttu-id="de5fa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="de5fa-125">Requirement</span></span> | <span data-ttu-id="de5fa-126">Valore</span><span class="sxs-lookup"><span data-stu-id="de5fa-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de5fa-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de5fa-127">Header</span></span><br/>  | <dl> <span data-ttu-id="de5fa-128"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de5fa-128"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de5fa-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="de5fa-129">Library</span></span><br/> | <dl> <span data-ttu-id="de5fa-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="de5fa-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de5fa-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de5fa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5fa-132">Classi base di DirectShow</span><span class="sxs-lookup"><span data-stu-id="de5fa-132">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




