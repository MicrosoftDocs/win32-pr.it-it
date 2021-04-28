---
description: 'Metodo CTransformOutputPin.CheckMediaType: il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.'
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Metodo CTransformOutputPin.CheckMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7dc0edc642687518979eab1d47c69af039bc3173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084909"
---
# <a name="ctransformoutputpincheckmediatype-method"></a><span data-ttu-id="931d8-103">Metodo CTransformOutputPin.CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="931d8-103">CTransformOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="931d8-104">Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="931d8-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="931d8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="931d8-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="931d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="931d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="931d8-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="931d8-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="931d8-108">Puntatore a un [**oggetto CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="931d8-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="931d8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="931d8-109">Return value</span></span>

<span data-ttu-id="931d8-110">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="931d8-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="931d8-111">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="931d8-111">Possible values include the following.</span></span>



| <span data-ttu-id="931d8-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="931d8-112">Return code</span></span>                                                                                  | <span data-ttu-id="931d8-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="931d8-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="931d8-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="931d8-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="931d8-115">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="931d8-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="931d8-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="931d8-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="931d8-117">Il pin di input del filtro non è connesso.</span><span class="sxs-lookup"><span data-stu-id="931d8-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="931d8-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="931d8-118">Remarks</span></span>

<span data-ttu-id="931d8-119">Questo metodo implementa il metodo [**CBasePin::CheckMediaType virtuale**](cbasepin-checkmediatype.md) puro.</span><span class="sxs-lookup"><span data-stu-id="931d8-119">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="931d8-120">Il metodo ha esito negativo se il pin di input del filtro non è connesso.</span><span class="sxs-lookup"><span data-stu-id="931d8-120">The method fails if the filter's input pin is not connected.</span></span> <span data-ttu-id="931d8-121">In caso contrario, chiama il metodo [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) del filtro, che è anche virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="931d8-121">Otherwise, it calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method, which is also pure virtual.</span></span> <span data-ttu-id="931d8-122">La classe derivata del filtro deve implementare **CheckTransform**, che determina se il tipo di supporto di output proposto è compatibile con il tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="931d8-122">The filter's derived class must implement **CheckTransform**, which determines if the proposed output media type is compatible with the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="931d8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="931d8-123">Requirements</span></span>



| <span data-ttu-id="931d8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="931d8-124">Requirement</span></span> | <span data-ttu-id="931d8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="931d8-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="931d8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="931d8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="931d8-127"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="931d8-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="931d8-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="931d8-128">Library</span></span><br/> | <dl> <span data-ttu-id="931d8-129"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="931d8-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




