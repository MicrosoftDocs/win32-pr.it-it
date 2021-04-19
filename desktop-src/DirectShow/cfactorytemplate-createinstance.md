---
description: Il metodo CreateInstance chiama la funzione di creazione di oggetti per la classe.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Metodo CFactoryTemplate. CreateInstance (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329831"
---
# <a name="cfactorytemplatecreateinstance-method"></a><span data-ttu-id="d738d-103">Metodo CFactoryTemplate. CreateInstance</span><span class="sxs-lookup"><span data-stu-id="d738d-103">CFactoryTemplate.CreateInstance method</span></span>

<span data-ttu-id="d738d-104">Il `CreateInstance` metodo chiama la funzione di creazione di oggetti per la classe.</span><span class="sxs-lookup"><span data-stu-id="d738d-104">The `CreateInstance` method calls the object-creation function for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="d738d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d738d-105">Syntax</span></span>


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="d738d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d738d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d738d-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="d738d-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d738d-108">Puntatore all'interfaccia **IUnknown** di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="d738d-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="d738d-109">*PHR*</span><span class="sxs-lookup"><span data-stu-id="d738d-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d738d-110">Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="d738d-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d738d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d738d-111">Return value</span></span>

<span data-ttu-id="d738d-112">Restituisce un'istanza dell'oggetto classe.</span><span class="sxs-lookup"><span data-stu-id="d738d-112">Returns an instance of the class object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d738d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d738d-113">Remarks</span></span>

<span data-ttu-id="d738d-114">Il metodo **IClassFactory:: CreateInstance** chiama questo metodo della classe.</span><span class="sxs-lookup"><span data-stu-id="d738d-114">The **IClassFactory::CreateInstance** method calls this class method.</span></span> <span data-ttu-id="d738d-115">Questo metodo chiama la funzione a cui fa riferimento la variabile membro [**CFactoryTemplate:: m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) .</span><span class="sxs-lookup"><span data-stu-id="d738d-115">This method calls the function pointed to by the [**CFactoryTemplate::m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="d738d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d738d-116">Requirements</span></span>



| <span data-ttu-id="d738d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d738d-117">Requirement</span></span> | <span data-ttu-id="d738d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d738d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d738d-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d738d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d738d-120"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d738d-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d738d-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d738d-121">Library</span></span><br/> | <dl> <span data-ttu-id="d738d-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d738d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d738d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d738d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d738d-124">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="d738d-124">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




