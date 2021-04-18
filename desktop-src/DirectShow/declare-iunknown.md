---
description: La \_ macro DECLARE IUnknown dichiara i tre metodi dell'interfaccia di base per una nuova interfaccia.
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: DECLARE_IUNKNOWN (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4823c1b4bd4832b1047a732bc503f04b4da65483
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330661"
---
# <a name="declare_iunknown"></a><span data-ttu-id="00936-103">DICHIARARE \_ IUnknown</span><span class="sxs-lookup"><span data-stu-id="00936-103">DECLARE\_IUNKNOWN</span></span>

<span data-ttu-id="00936-104">La macro **Declare \_ IUnknown** dichiara i tre metodi dell'interfaccia di base per una nuova interfaccia.</span><span class="sxs-lookup"><span data-stu-id="00936-104">The **DECLARE\_IUNKNOWN** macro declares the three methods of the base interface for a new interface.</span></span>

<span data-ttu-id="00936-105">**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="00936-105">**Syntax**</span></span>

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a><span data-ttu-id="00936-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="00936-106">Remarks</span></span>

<span data-ttu-id="00936-107">Quando si crea una nuova interfaccia, deve derivare da **IUnknown**, che ha tre metodi: **QueryInterface**, **AddRef** e **Release**.</span><span class="sxs-lookup"><span data-stu-id="00936-107">When you create a new interface, it must derive from **IUnknown**, which has three methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="00936-108">Questa macro semplifica il processo di dichiarazione dichiarando ognuno di questi metodi per la nuova interfaccia.</span><span class="sxs-lookup"><span data-stu-id="00936-108">This macro simplifies the declaration process by declaring each of these methods for the new interface.</span></span>

<span data-ttu-id="00936-109">Questa macro funziona solo con le classi che derivano, direttamente o indirettamente, dalla classe [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="00936-109">This macro works only with classes that derive, directly or indirectly, from the [**CUnknown**](cunknown.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="00936-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00936-110">Requirements</span></span>



| <span data-ttu-id="00936-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="00936-111">Requirement</span></span> | <span data-ttu-id="00936-112">Valore</span><span class="sxs-lookup"><span data-stu-id="00936-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00936-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00936-113">Header</span></span><br/>  | <dl> <span data-ttu-id="00936-114"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00936-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="00936-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="00936-115">Library</span></span><br/> | <dl> <span data-ttu-id="00936-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="00936-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00936-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00936-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00936-118">**Funzioni helper COM**</span><span class="sxs-lookup"><span data-stu-id="00936-118">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="00936-119">**CUnknown:: GetOwner**</span><span class="sxs-lookup"><span data-stu-id="00936-119">**CUnknown::GetOwner**</span></span>](cunknown-getowner.md)
</dt> <dt>

[<span data-ttu-id="00936-120">Come implementare IUnknown</span><span class="sxs-lookup"><span data-stu-id="00936-120">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 




