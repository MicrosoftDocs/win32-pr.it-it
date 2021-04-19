---
description: 'Il metodo QueryId recupera un identificatore per il PIN. Questo metodo implementa il metodo IPin:: QueryId.'
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: Metodo CTransformInputPin. QueryId (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daae425e82bbc89cfbc863baea1924e36e63f122
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329961"
---
# <a name="ctransforminputpinqueryid-method"></a><span data-ttu-id="0fa65-104">CTransformInputPin. QueryId, metodo</span><span class="sxs-lookup"><span data-stu-id="0fa65-104">CTransformInputPin.QueryId method</span></span>

<span data-ttu-id="0fa65-105">Il `QueryId` metodo recupera un identificatore per il PIN.</span><span class="sxs-lookup"><span data-stu-id="0fa65-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="0fa65-106">Questo metodo implementa il metodo [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="0fa65-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fa65-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fa65-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="0fa65-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fa65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fa65-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="0fa65-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="0fa65-110">Riceve una stringa che contiene l'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="0fa65-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fa65-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0fa65-111">Return value</span></span>

<span data-ttu-id="0fa65-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0fa65-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="0fa65-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0fa65-113">Return code</span></span>                                                                                   | <span data-ttu-id="0fa65-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fa65-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="0fa65-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0fa65-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0fa65-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="0fa65-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="0fa65-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0fa65-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0fa65-118">Memoria insufficiente</span><span class="sxs-lookup"><span data-stu-id="0fa65-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="0fa65-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="0fa65-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0fa65-120">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="0fa65-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0fa65-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fa65-121">Remarks</span></span>

<span data-ttu-id="0fa65-122">L'identificatore del PIN viene usato per la persistenza del grafo.</span><span class="sxs-lookup"><span data-stu-id="0fa65-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="0fa65-123">L'identificatore del PIN per questa classe è in.</span><span class="sxs-lookup"><span data-stu-id="0fa65-123">The pin identifier for this class is In.</span></span> <span data-ttu-id="0fa65-124">Questa classe esegue l'override del comportamento della classe [**CBasePin**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="0fa65-124">This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="0fa65-125">Nella classe **CBasePin** l'identificatore del PIN è uguale al nome del PIN, specificato nel costruttore della classe.</span><span class="sxs-lookup"><span data-stu-id="0fa65-125">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="0fa65-126">Nella classe **CTransformInputPin** , l'identificatore del PIN e il nome del PIN non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="0fa65-126">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fa65-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fa65-127">Requirements</span></span>



| <span data-ttu-id="0fa65-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fa65-128">Requirement</span></span> | <span data-ttu-id="0fa65-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0fa65-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa65-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0fa65-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0fa65-131"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fa65-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0fa65-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="0fa65-132">Library</span></span><br/> | <dl> <span data-ttu-id="0fa65-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0fa65-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




