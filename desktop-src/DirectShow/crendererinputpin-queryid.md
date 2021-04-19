---
description: "Il metodo QueryId recupera l'identificatore del PIN. Questo metodo esegue l'override del Metodo CBasePin:: QueryId."
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: Metodo CRendererInputPin. QueryId (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b56ae2a846b4d89da4c6a9d4c8f88bd3094c5cff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333182"
---
# <a name="crendererinputpinqueryid-method"></a><span data-ttu-id="45ecd-104">CRendererInputPin. QueryId, metodo</span><span class="sxs-lookup"><span data-stu-id="45ecd-104">CRendererInputPin.QueryId method</span></span>

<span data-ttu-id="45ecd-105">Il `QueryId` metodo recupera l'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="45ecd-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="45ecd-106">Questo metodo esegue l'override del metodo [**CBasePin:: QueryId**](cbasepin-queryid.md) .</span><span class="sxs-lookup"><span data-stu-id="45ecd-106">This method overrides the [**CBasePin::QueryId**](cbasepin-queryid.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="45ecd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45ecd-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="45ecd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="45ecd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45ecd-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="45ecd-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="45ecd-110">Riceve una stringa che contiene l'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="45ecd-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45ecd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45ecd-111">Return value</span></span>

<span data-ttu-id="45ecd-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="45ecd-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="45ecd-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="45ecd-113">Return code</span></span>                                                                                   | <span data-ttu-id="45ecd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45ecd-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="45ecd-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="45ecd-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="45ecd-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="45ecd-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="45ecd-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="45ecd-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="45ecd-118">Memoria insufficiente</span><span class="sxs-lookup"><span data-stu-id="45ecd-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="45ecd-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="45ecd-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="45ecd-120">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="45ecd-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="45ecd-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="45ecd-121">Remarks</span></span>

<span data-ttu-id="45ecd-122">Questo metodo alloca la stringa di caratteri wide "in" e la assegna al parametro *ID* .</span><span class="sxs-lookup"><span data-stu-id="45ecd-122">This method allocates the wide-character string "In" and assigns it to the *Id* parameter.</span></span> <span data-ttu-id="45ecd-123">Il chiamante deve liberare la memoria allocata tramite la funzione **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="45ecd-123">The caller must free the allocated memory, using the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="45ecd-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45ecd-124">Requirements</span></span>



| <span data-ttu-id="45ecd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="45ecd-125">Requirement</span></span> | <span data-ttu-id="45ecd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="45ecd-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ecd-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45ecd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="45ecd-128"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45ecd-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="45ecd-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="45ecd-129">Library</span></span><br/> | <dl> <span data-ttu-id="45ecd-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="45ecd-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45ecd-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45ecd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ecd-132">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="45ecd-132">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




