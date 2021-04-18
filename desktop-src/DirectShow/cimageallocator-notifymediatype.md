---
description: Il metodo NotifyMediaType informa l'oggetto del tipo di supporto corrente.
ms.assetid: 6fb708ff-e968-4867-baca-ebe2515c9fab
title: Metodo CImageAllocator. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9261884b8940b571876502741fcc52e1c40a33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331185"
---
# <a name="cimageallocatornotifymediatype-method"></a><span data-ttu-id="c2aba-103">CImageAllocator. NotifyMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="c2aba-103">CImageAllocator.NotifyMediaType method</span></span>

<span data-ttu-id="c2aba-104">Il `NotifyMediaType` metodo informa l'oggetto del tipo di supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="c2aba-104">The `NotifyMediaType` method informs the object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2aba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2aba-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="c2aba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2aba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2aba-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="c2aba-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="c2aba-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) o **null** per cancellare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c2aba-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2aba-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2aba-109">Return value</span></span>

<span data-ttu-id="c2aba-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c2aba-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2aba-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2aba-111">Remarks</span></span>

<span data-ttu-id="c2aba-112">Il filtro proprietario deve chiamare questo metodo ogni volta che viene modificato il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c2aba-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="c2aba-113">Questa situazione si verifica in genere quando il pin si connette per la prima volta e dopo una modifica del formato dinamico.</span><span class="sxs-lookup"><span data-stu-id="c2aba-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span> <span data-ttu-id="c2aba-114">L'allocatore usa il tipo di supporto per convalidare le proprietà dell'allocatore proposto e anche quando crea esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="c2aba-114">The allocator uses the media type to validate proposed allocator properties, and also when it creates media samples.</span></span>

<span data-ttu-id="c2aba-115">L'oggetto **CImageAllocator** archivia il puntatore *pMediaType* nella variabile **membro \_ pMediaType m** .</span><span class="sxs-lookup"><span data-stu-id="c2aba-115">The **CImageAllocator** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="c2aba-116">Se pertanto il chiamante deve rilasciare l'oggetto **CMediaType** , deve aggiornare l'allocatore chiamando nuovamente questo metodo con un nuovo puntatore o con un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="c2aba-116">Therefore, if the caller needs to release the **CMediaType** object, it should update the allocator by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="c2aba-117">In caso contrario, può verificarsi un errore quando l'allocatore tenta di fare riferimento al puntatore precedente.</span><span class="sxs-lookup"><span data-stu-id="c2aba-117">Otherwise, an error can occur when the allocator attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2aba-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2aba-118">Requirements</span></span>



| <span data-ttu-id="c2aba-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2aba-119">Requirement</span></span> | <span data-ttu-id="c2aba-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c2aba-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2aba-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2aba-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c2aba-122"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2aba-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c2aba-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="c2aba-123">Library</span></span><br/> | <dl> <span data-ttu-id="c2aba-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c2aba-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2aba-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2aba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2aba-126">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="c2aba-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




