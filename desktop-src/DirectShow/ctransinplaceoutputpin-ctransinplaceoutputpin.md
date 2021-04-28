---
description: Costruttore CTransInPlaceOutputPin.CTransInPlaceOutputPin - Metodo costruttore.
ms.assetid: fe7b2d62-0e6a-4253-b469-6cede5dc9bb1
title: Costruttore CTransInPlaceOutputPin.CTransInPlaceOutputPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b63ee3aa52bc0363bcab90275be4148659b3bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094709"
---
# <a name="ctransinplaceoutputpinctransinplaceoutputpin-constructor"></a><span data-ttu-id="b7ae6-103">Costruttore CTransInPlaceOutputPin.CTransInPlaceOutputPin</span><span class="sxs-lookup"><span data-stu-id="b7ae6-103">CTransInPlaceOutputPin.CTransInPlaceOutputPin constructor</span></span>

<span data-ttu-id="b7ae6-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7ae6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7ae6-105">Syntax</span></span>


```C++
CTransInPlaceOutputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="b7ae6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7ae6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7ae6-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="b7ae6-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="b7ae6-108">Stringa contenente il nome di debug dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-108">String containing the debug name of the object.</span></span> <span data-ttu-id="b7ae6-109">Per altre informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="b7ae6-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7ae6-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="b7ae6-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="b7ae6-111">Puntatore al filtro che ha creato questo pin, che deve essere un [**oggetto CTransInPlaceFilter.**](ctransinplacefilter.md)</span><span class="sxs-lookup"><span data-stu-id="b7ae6-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="b7ae6-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="b7ae6-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b7ae6-113">Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="b7ae6-114">Inizializzare il valore su S \_ OK prima di creare l'oggetto .</span><span class="sxs-lookup"><span data-stu-id="b7ae6-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="b7ae6-115">Il valore viene modificato solo se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="b7ae6-116">*Pname*</span><span class="sxs-lookup"><span data-stu-id="b7ae6-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="b7ae6-117">Stringa di caratteri wide contenente il nome del pin.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7ae6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7ae6-118">Remarks</span></span>

<span data-ttu-id="b7ae6-119">Il *parametro pName* specifica il nome del pin, restituito dal metodo [**IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)</span><span class="sxs-lookup"><span data-stu-id="b7ae6-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="b7ae6-120">Tuttavia, la stringa non viene usata per l'identificatore pin.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="b7ae6-121">L'identificatore pin per questa classe è sempre "Out".</span><span class="sxs-lookup"><span data-stu-id="b7ae6-121">The pin identifier for this class is always "Out".</span></span> <span data-ttu-id="b7ae6-122">Per altre informazioni, vedere [**QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="b7ae6-122">For more information, see [**QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7ae6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7ae6-123">Requirements</span></span>



| <span data-ttu-id="b7ae6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7ae6-124">Requirement</span></span> | <span data-ttu-id="b7ae6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b7ae6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ae6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7ae6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b7ae6-127"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7ae6-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b7ae6-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7ae6-128">Library</span></span><br/> | <dl> <span data-ttu-id="b7ae6-129"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b7ae6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7ae6-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7ae6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ae6-131">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="b7ae6-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




