---
description: Il metodo GetTypeInfo recupera le informazioni sul tipo per l'oggetto, che può quindi essere usato per ottenere le informazioni sul tipo per un'interfaccia.
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Metodo CMediaPosition. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa776ca71daff67185bf9fd2c1727f9535f8ac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332331"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="d425b-103">CMediaPosition. GetTypeInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="d425b-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="d425b-104">Il `GetTypeInfo` metodo recupera le informazioni sul tipo per l'oggetto, che può quindi essere usato per ottenere le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d425b-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d425b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d425b-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="d425b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d425b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d425b-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="d425b-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="d425b-108">Informazioni sul tipo da restituire.</span><span class="sxs-lookup"><span data-stu-id="d425b-108">Type information to return.</span></span> <span data-ttu-id="d425b-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d425b-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d425b-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="d425b-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="d425b-111">Identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="d425b-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d425b-112">*ppTInfo*</span><span class="sxs-lookup"><span data-stu-id="d425b-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="d425b-113">Indirizzo di una variabile che riceve un puntatore **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="d425b-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d425b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d425b-114">Return value</span></span>

<span data-ttu-id="d425b-115">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d425b-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d425b-116">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="d425b-116">Possible values include the following.</span></span>



| <span data-ttu-id="d425b-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d425b-117">Return code</span></span>                                                                                             | <span data-ttu-id="d425b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d425b-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="d425b-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d425b-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="d425b-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d425b-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="d425b-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d425b-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="d425b-122">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="d425b-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="d425b-123"><dt>**Digitare \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="d425b-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="d425b-124">Il parametro *itinfo* è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="d425b-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d425b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d425b-125">Requirements</span></span>



| <span data-ttu-id="d425b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d425b-126">Requirement</span></span> | <span data-ttu-id="d425b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d425b-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d425b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d425b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d425b-129"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d425b-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d425b-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="d425b-130">Library</span></span><br/> | <dl> <span data-ttu-id="d425b-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d425b-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d425b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d425b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d425b-133">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="d425b-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




