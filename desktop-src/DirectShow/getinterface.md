---
description: La funzione GetInterface recupera un puntatore a interfaccia.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: Funzione GetInterface (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 317f08af2a4ff0e9410c61da8b19d14735a14f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330936"
---
# <a name="getinterface-function"></a><span data-ttu-id="e7854-103">Funzione GetInterface</span><span class="sxs-lookup"><span data-stu-id="e7854-103">GetInterface function</span></span>

<span data-ttu-id="e7854-104">La `GetInterface` funzione recupera un puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e7854-104">The `GetInterface` function retrieves an interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7854-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7854-105">Syntax</span></span>


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="e7854-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7854-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7854-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="e7854-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e7854-108">Puntatore all'interfaccia **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="e7854-108">Pointer to the **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="e7854-109">*PPV*</span><span class="sxs-lookup"><span data-stu-id="e7854-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="e7854-110">Indirizzo di un puntatore all'interfaccia recuperata.</span><span class="sxs-lookup"><span data-stu-id="e7854-110">Address of a pointer to the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7854-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7854-111">Return value</span></span>

<span data-ttu-id="e7854-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7854-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7854-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7854-113">Remarks</span></span>

<span data-ttu-id="e7854-114">Questa funzione membro esegue un incremento thread-safe del conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="e7854-114">This member function performs a thread-safe increment of the reference count.</span></span> <span data-ttu-id="e7854-115">Per recuperare l'interfaccia e aggiungere un riferimento, chiamare questa funzione dall'implementazione di override del metodo **INonDelegatingUnknown:: NonDelegatingQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="e7854-115">To retrieve the interface and add a reference, call this function from your overriding implementation of the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7854-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7854-116">Requirements</span></span>



| <span data-ttu-id="e7854-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7854-117">Requirement</span></span> | <span data-ttu-id="e7854-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e7854-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7854-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7854-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e7854-120"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7854-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e7854-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="e7854-121">Library</span></span><br/> | <dl> <span data-ttu-id="e7854-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e7854-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7854-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7854-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7854-124">**Funzioni helper COM**</span><span class="sxs-lookup"><span data-stu-id="e7854-124">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="e7854-125">**INonDelegatingUnknown**</span><span class="sxs-lookup"><span data-stu-id="e7854-125">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md)
</dt> </dl>

 

 




