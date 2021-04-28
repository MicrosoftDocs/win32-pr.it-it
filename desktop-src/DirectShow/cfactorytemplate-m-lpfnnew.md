---
description: "CFactoryTemplate::m_lpfnNew membro : puntatore a una funzione che crea un'istanza dell'oggetto."
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: Membro CFactoryTemplate::m_lpfnNew (Combase.h)
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
ms.openlocfilehash: ee4ec8e1503d3b260e025d154624b2d7c09bb49b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095649"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a><span data-ttu-id="f2c65-103">CFactoryTemplate::m \_ lpfnNew member</span><span class="sxs-lookup"><span data-stu-id="f2c65-103">CFactoryTemplate::m\_lpfnNew member</span></span>

<span data-ttu-id="f2c65-104">Puntatore a una funzione che crea un'istanza dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="f2c65-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c65-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2c65-105">Syntax</span></span>


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a><span data-ttu-id="f2c65-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f2c65-106">Remarks</span></span>

<span data-ttu-id="f2c65-107">Nella DLL dichiarare una funzione statica che restituisce un puntatore a una nuova istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f2c65-107">In your DLL, declare a static function that returns a pointer to a new instance of the object.</span></span> <span data-ttu-id="f2c65-108">Nel modello factory impostare la variabile **membro m \_ lpfnNew** sull'indirizzo di questa funzione statica.</span><span class="sxs-lookup"><span data-stu-id="f2c65-108">In the factory template, set the **m\_lpfnNew** member variable to the address of this static function.</span></span>

<span data-ttu-id="f2c65-109">Il tipo di puntatore a funzione [**è LPFNNewCOMObject**](lpfnnewcomobject.md).</span><span class="sxs-lookup"><span data-stu-id="f2c65-109">The function pointer type is [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span></span>

<span data-ttu-id="f2c65-110">L'esempio seguente illustra una funzione tipica per **m \_ lpfnNew**:</span><span class="sxs-lookup"><span data-stu-id="f2c65-110">The following example shows a typical function for **m\_lpfnNew**:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f2c65-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2c65-111">Requirements</span></span>



| <span data-ttu-id="f2c65-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2c65-112">Requirement</span></span> | <span data-ttu-id="f2c65-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f2c65-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c65-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2c65-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f2c65-115"><dt>Combase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2c65-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2c65-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2c65-116">Library</span></span><br/> | <dl> <span data-ttu-id="f2c65-117"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f2c65-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2c65-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2c65-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c65-119">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="f2c65-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




