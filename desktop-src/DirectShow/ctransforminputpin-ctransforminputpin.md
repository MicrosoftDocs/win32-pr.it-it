---
description: 'Costruttore CTransformInputPin.CTransformInputPin : metodo costruttore.'
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: Costruttore CTransformInputPin.CTransformInputPin (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e893b4e1c7d4f396644a468d3d71fa3046fb712
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095049"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a><span data-ttu-id="561ec-103">Costruttore CTransformInputPin.CTransformInputPin</span><span class="sxs-lookup"><span data-stu-id="561ec-103">CTransformInputPin.CTransformInputPin constructor</span></span>

<span data-ttu-id="561ec-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="561ec-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="561ec-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="561ec-105">Syntax</span></span>


```C++
CTransformInputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="561ec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="561ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="561ec-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="561ec-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="561ec-108">Stringa contenente il nome di debug dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="561ec-108">String containing the debug name of the object.</span></span> <span data-ttu-id="561ec-109">Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="561ec-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="561ec-110">*pTransformFilter*</span><span class="sxs-lookup"><span data-stu-id="561ec-110">*pTransformFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="561ec-111">Puntatore al filtro che ha creato questo segnaposto, che deve essere un [**oggetto CTransformFilter.**](ctransformfilter.md)</span><span class="sxs-lookup"><span data-stu-id="561ec-111">Pointer to the filter that created this pin, which must be a [**CTransformFilter**](ctransformfilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="561ec-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="561ec-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="561ec-113">Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="561ec-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="561ec-114">Inizializzare il valore su S \_ OK prima di creare l'oggetto .</span><span class="sxs-lookup"><span data-stu-id="561ec-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="561ec-115">Il valore viene modificato solo se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="561ec-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="561ec-116">*Pname*</span><span class="sxs-lookup"><span data-stu-id="561ec-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="561ec-117">Stringa di caratteri wide contenente il nome del segnaposto.</span><span class="sxs-lookup"><span data-stu-id="561ec-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="561ec-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="561ec-118">Remarks</span></span>

<span data-ttu-id="561ec-119">Il *parametro pName* specifica il nome del pin, restituito dal [**metodo IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)</span><span class="sxs-lookup"><span data-stu-id="561ec-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="561ec-120">Tuttavia, la stringa non viene usata per l'identificatore pin.</span><span class="sxs-lookup"><span data-stu-id="561ec-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="561ec-121">L'identificatore pin per questa classe è sempre "In".</span><span class="sxs-lookup"><span data-stu-id="561ec-121">The pin identifier for this class is always "In".</span></span> <span data-ttu-id="561ec-122">Per altre informazioni, vedere [**QueryId.**](ctransforminputpin-queryid.md)</span><span class="sxs-lookup"><span data-stu-id="561ec-122">For more information, see [**QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="561ec-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="561ec-123">Requirements</span></span>



| <span data-ttu-id="561ec-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="561ec-124">Requirement</span></span> | <span data-ttu-id="561ec-125">Valore</span><span class="sxs-lookup"><span data-stu-id="561ec-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="561ec-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="561ec-126">Header</span></span><br/>  | <dl> <span data-ttu-id="561ec-127"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="561ec-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="561ec-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="561ec-128">Library</span></span><br/> | <dl> <span data-ttu-id="561ec-129"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="561ec-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




