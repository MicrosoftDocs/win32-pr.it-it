---
description: Metodo del costruttore.
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: Costruttore CTransInPlaceInputPin. CTransInPlaceInputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a801b2c4286f903ef450cac2fd76252f451f9add
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326202"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a><span data-ttu-id="3f210-103">Costruttore CTransInPlaceInputPin. CTransInPlaceInputPin</span><span class="sxs-lookup"><span data-stu-id="3f210-103">CTransInPlaceInputPin.CTransInPlaceInputPin constructor</span></span>

<span data-ttu-id="3f210-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="3f210-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f210-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f210-105">Syntax</span></span>


```C++
CTransInPlaceInputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="3f210-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f210-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f210-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="3f210-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="3f210-108">Stringa contenente il nome di debug dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3f210-108">String containing the debug name of the object.</span></span> <span data-ttu-id="3f210-109">Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="3f210-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f210-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="3f210-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="3f210-111">Puntatore al filtro che ha creato questo pin, che deve essere un oggetto [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="3f210-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3f210-112">*PHR*</span><span class="sxs-lookup"><span data-stu-id="3f210-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3f210-113">Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="3f210-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="3f210-114">Inizializzare il valore su S \_ OK prima di creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3f210-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="3f210-115">Il valore viene modificato solo se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="3f210-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="3f210-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="3f210-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3f210-117">Stringa di caratteri wide contenente il nome del PIN.</span><span class="sxs-lookup"><span data-stu-id="3f210-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f210-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f210-118">Remarks</span></span>

<span data-ttu-id="3f210-119">Il parametro *pname* specifica il nome del PIN, restituito dal metodo [**Ipin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="3f210-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="3f210-120">Questa stringa non viene tuttavia utilizzata per l'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="3f210-120">However, this string is not used for the pin identifier.</span></span> <span data-ttu-id="3f210-121">L'identificatore del PIN per questa classe è sempre in.</span><span class="sxs-lookup"><span data-stu-id="3f210-121">The pin identifier for this class is always In.</span></span> <span data-ttu-id="3f210-122">Per ulteriori informazioni, vedere [**CTransformInputPin:: QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="3f210-122">For more information, see [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f210-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f210-123">Requirements</span></span>



| <span data-ttu-id="3f210-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f210-124">Requirement</span></span> | <span data-ttu-id="3f210-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3f210-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f210-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f210-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3f210-127"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f210-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3f210-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f210-128">Library</span></span><br/> | <dl> <span data-ttu-id="3f210-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3f210-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f210-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f210-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f210-131">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="3f210-131">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




