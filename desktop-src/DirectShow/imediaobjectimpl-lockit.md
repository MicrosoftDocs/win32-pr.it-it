---
description: La classe LockIt è una classe interna che blocca e sblocca DMO.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'Classe IMediaObjectImpl:: LockIt (Dmoimpl. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326273"
---
# <a name="imediaobjectimpllockit-class"></a><span data-ttu-id="d30dd-103">Classe IMediaObjectImpl:: LockIt</span><span class="sxs-lookup"><span data-stu-id="d30dd-103">IMediaObjectImpl::LockIt Class</span></span>

<span data-ttu-id="d30dd-104">La `LockIt` classe è una classe interna che blocca e sblocca DMO.</span><span class="sxs-lookup"><span data-stu-id="d30dd-104">The `LockIt` class is an internal class that locks and unlocks the DMO.</span></span>

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a><span data-ttu-id="d30dd-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d30dd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d30dd-106"><span id="p"></span><span id="P"></span>*p*</span><span class="sxs-lookup"><span data-stu-id="d30dd-106"><span id="p"></span><span id="P"></span>*p*</span></span>
</dt> <dd>

<span data-ttu-id="d30dd-107">Puntatore all'oggetto derivato.</span><span class="sxs-lookup"><span data-stu-id="d30dd-107">Pointer to the derived object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d30dd-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d30dd-108">Remarks</span></span>

<span data-ttu-id="d30dd-109">Il `LockIt` Costruttore blocca il DMO e il distruttore Sblocca il DMO.</span><span class="sxs-lookup"><span data-stu-id="d30dd-109">The `LockIt` constructor locks the DMO, and the destructor unlocks the DMO.</span></span> <span data-ttu-id="d30dd-110">Per bloccare l'oggetto dall'interno della classe derivata, dichiarare una variabile locale di tipo `LockIt` .</span><span class="sxs-lookup"><span data-stu-id="d30dd-110">To lock the object from inside your derived class, declare a local variable of type `LockIt`.</span></span> <span data-ttu-id="d30dd-111">DMO è bloccato mentre l' `LockIt` oggetto rimane nell'ambito:</span><span class="sxs-lookup"><span data-stu-id="d30dd-111">The DMO is locked while the `LockIt` object remains in scope:</span></span>


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



<span data-ttu-id="d30dd-112">I metodi in **IMediaObjectImpl** bloccano automaticamente DMO.</span><span class="sxs-lookup"><span data-stu-id="d30dd-112">The methods in **IMediaObjectImpl** automatically lock the DMO.</span></span>

## <a name="requirements"></a><span data-ttu-id="d30dd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d30dd-113">Requirements</span></span>



| <span data-ttu-id="d30dd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d30dd-114">Requirement</span></span> | <span data-ttu-id="d30dd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d30dd-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d30dd-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d30dd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d30dd-117"><dt>Dmoimpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d30dd-117"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="d30dd-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="d30dd-118">Library</span></span><br/> | <dl> <span data-ttu-id="d30dd-119"><dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d30dd-119"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d30dd-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d30dd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d30dd-121">**Modello di classe IMediaObjectImpl**</span><span class="sxs-lookup"><span data-stu-id="d30dd-121">**IMediaObjectImpl Class Template**</span></span>](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




