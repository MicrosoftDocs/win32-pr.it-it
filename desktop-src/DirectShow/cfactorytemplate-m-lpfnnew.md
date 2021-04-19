---
description: Puntatore a una funzione che crea un'istanza dell'oggetto.
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'Membro CFactoryTemplate:: m_lpfnNew (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2299f7a87f348ac8a5fa6c6d83b6a17fbf97ca28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329821"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a><span data-ttu-id="c5d45-103">Membro lpfnNew di CFactoryTemplate:: m \_</span><span class="sxs-lookup"><span data-stu-id="c5d45-103">CFactoryTemplate::m\_lpfnNew member</span></span>

<span data-ttu-id="c5d45-104">Puntatore a una funzione che crea un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c5d45-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d45-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5d45-105">Syntax</span></span>


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a><span data-ttu-id="c5d45-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c5d45-106">Remarks</span></span>

<span data-ttu-id="c5d45-107">Nella DLL dichiarare una funzione statica che restituisce un puntatore a una nuova istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c5d45-107">In your DLL, declare a static function that returns a pointer to a new instance of the object.</span></span> <span data-ttu-id="c5d45-108">Nel modello Factory impostare la variabile membro **\_ lpfnNew m** sull'indirizzo della funzione statica.</span><span class="sxs-lookup"><span data-stu-id="c5d45-108">In the factory template, set the **m\_lpfnNew** member variable to the address of this static function.</span></span>

<span data-ttu-id="c5d45-109">Il tipo di puntatore a funzione è [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span><span class="sxs-lookup"><span data-stu-id="c5d45-109">The function pointer type is [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span></span>

<span data-ttu-id="c5d45-110">Nell'esempio seguente viene illustrata una funzione tipica per **m \_ lpfnNew**:</span><span class="sxs-lookup"><span data-stu-id="c5d45-110">The following example shows a typical function for **m\_lpfnNew**:</span></span>


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a><span data-ttu-id="c5d45-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5d45-111">Requirements</span></span>



| <span data-ttu-id="c5d45-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5d45-112">Requirement</span></span> | <span data-ttu-id="c5d45-113">Valore</span><span class="sxs-lookup"><span data-stu-id="c5d45-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d45-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5d45-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c5d45-115"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5d45-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c5d45-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="c5d45-116">Library</span></span><br/> | <dl> <span data-ttu-id="c5d45-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c5d45-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d45-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5d45-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d45-119">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="c5d45-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




