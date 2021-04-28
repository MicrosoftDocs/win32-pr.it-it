---
description: "Metodo CMediaPosition.GetTypeInfo: il metodo GetTypeInfo recupera le informazioni sul tipo per l'oggetto, che possono quindi essere usate per ottenere le informazioni sul tipo per un'interfaccia."
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Metodo CMediaPosition.GetTypeInfo (Ctlutil.h)
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
ms.openlocfilehash: f7827a3599f05061b5760084bed46cd2554b45f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099139"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="87355-103">Metodo CMediaPosition.GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="87355-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="87355-104">Il metodo recupera le informazioni sul tipo per l'oggetto , che può quindi essere usato per `GetTypeInfo` ottenere le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="87355-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="87355-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87355-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="87355-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87355-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87355-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="87355-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="87355-108">Informazioni sul tipo da restituire.</span><span class="sxs-lookup"><span data-stu-id="87355-108">Type information to return.</span></span> <span data-ttu-id="87355-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="87355-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="87355-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="87355-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="87355-111">Identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="87355-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="87355-112">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="87355-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="87355-113">Indirizzo di una variabile che riceve un **puntatore ITypeInfo.**</span><span class="sxs-lookup"><span data-stu-id="87355-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87355-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87355-114">Return value</span></span>

<span data-ttu-id="87355-115">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="87355-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="87355-116">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="87355-116">Possible values include the following.</span></span>



| <span data-ttu-id="87355-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="87355-117">Return code</span></span>                                                                                             | <span data-ttu-id="87355-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87355-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="87355-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87355-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="87355-120">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="87355-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="87355-121"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="87355-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="87355-122">Argomento del puntatore **NULL.**</span><span class="sxs-lookup"><span data-stu-id="87355-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="87355-123"><dt>**TIPO \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="87355-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="87355-124">Il *parametro itinfo* non è zero.</span><span class="sxs-lookup"><span data-stu-id="87355-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="87355-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87355-125">Requirements</span></span>



| <span data-ttu-id="87355-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="87355-126">Requirement</span></span> | <span data-ttu-id="87355-127">Valore</span><span class="sxs-lookup"><span data-stu-id="87355-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87355-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87355-128">Header</span></span><br/>  | <dl> <span data-ttu-id="87355-129"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="87355-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="87355-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="87355-130">Library</span></span><br/> | <dl> <span data-ttu-id="87355-131"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="87355-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87355-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87355-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87355-133">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="87355-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




