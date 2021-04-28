---
description: Costruttore CTransInPlaceInputPin.CTransInPlaceInputPin - Metodo costruttore.
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: Costruttore CTransInPlaceInputPin.CTransInPlaceInputPin (Transip.h)
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
ms.openlocfilehash: 6f97c89142e43691c91b2a4c0d04721d9112ed49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084759"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a><span data-ttu-id="37dca-103">Costruttore CTransInPlaceInputPin.CTransInPlaceInputPin</span><span class="sxs-lookup"><span data-stu-id="37dca-103">CTransInPlaceInputPin.CTransInPlaceInputPin constructor</span></span>

<span data-ttu-id="37dca-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="37dca-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="37dca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37dca-105">Syntax</span></span>


```C++
CTransInPlaceInputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="37dca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="37dca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37dca-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="37dca-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="37dca-108">Stringa contenente il nome di debug dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="37dca-108">String containing the debug name of the object.</span></span> <span data-ttu-id="37dca-109">Per altre informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="37dca-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="37dca-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="37dca-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="37dca-111">Puntatore al filtro che ha creato questo pin, che deve essere un [**oggetto CTransInPlaceFilter.**](ctransinplacefilter.md)</span><span class="sxs-lookup"><span data-stu-id="37dca-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="37dca-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="37dca-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="37dca-113">Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="37dca-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="37dca-114">Inizializzare il valore su S \_ OK prima di creare l'oggetto .</span><span class="sxs-lookup"><span data-stu-id="37dca-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="37dca-115">Il valore viene modificato solo se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="37dca-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="37dca-116">*Pname*</span><span class="sxs-lookup"><span data-stu-id="37dca-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="37dca-117">Stringa di caratteri wide contenente il nome del pin.</span><span class="sxs-lookup"><span data-stu-id="37dca-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37dca-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="37dca-118">Remarks</span></span>

<span data-ttu-id="37dca-119">Il *parametro pName* specifica il nome del pin, restituito dal metodo [**IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)</span><span class="sxs-lookup"><span data-stu-id="37dca-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="37dca-120">Tuttavia, questa stringa non viene usata per l'identificatore pin.</span><span class="sxs-lookup"><span data-stu-id="37dca-120">However, this string is not used for the pin identifier.</span></span> <span data-ttu-id="37dca-121">L'identificatore pin per questa classe è sempre In.</span><span class="sxs-lookup"><span data-stu-id="37dca-121">The pin identifier for this class is always In.</span></span> <span data-ttu-id="37dca-122">Per altre informazioni, vedere [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="37dca-122">For more information, see [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37dca-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37dca-123">Requirements</span></span>



| <span data-ttu-id="37dca-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="37dca-124">Requirement</span></span> | <span data-ttu-id="37dca-125">Valore</span><span class="sxs-lookup"><span data-stu-id="37dca-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37dca-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37dca-126">Header</span></span><br/>  | <dl> <span data-ttu-id="37dca-127"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="37dca-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="37dca-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="37dca-128">Library</span></span><br/> | <dl> <span data-ttu-id="37dca-129"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="37dca-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37dca-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37dca-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37dca-131">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="37dca-131">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




