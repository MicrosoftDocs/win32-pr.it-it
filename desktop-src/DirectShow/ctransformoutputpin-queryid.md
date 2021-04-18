---
description: 'Il metodo QueryId recupera un identificatore per il PIN. Questo metodo implementa il metodo IPin:: QueryId.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: Metodo CTransformOutputPin. QueryId (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e8e5fbc4b4da7b38853df5b4dcf3580a8c198d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330838"
---
# <a name="ctransformoutputpinqueryid-method"></a><span data-ttu-id="0b416-104">CTransformOutputPin. QueryId, metodo</span><span class="sxs-lookup"><span data-stu-id="0b416-104">CTransformOutputPin.QueryId method</span></span>

<span data-ttu-id="0b416-105">Il `QueryId` metodo recupera un identificatore per il PIN.</span><span class="sxs-lookup"><span data-stu-id="0b416-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="0b416-106">Questo metodo implementa il metodo [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="0b416-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b416-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b416-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="0b416-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b416-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b416-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="0b416-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="0b416-110">Riceve una stringa che contiene l'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="0b416-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b416-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b416-111">Return value</span></span>

<span data-ttu-id="0b416-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0b416-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="0b416-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0b416-113">Return code</span></span>                                                                                   | <span data-ttu-id="0b416-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b416-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="0b416-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b416-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0b416-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="0b416-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="0b416-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0b416-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0b416-118">Memoria insufficiente</span><span class="sxs-lookup"><span data-stu-id="0b416-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="0b416-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="0b416-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0b416-120">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="0b416-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b416-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b416-121">Remarks</span></span>

<span data-ttu-id="0b416-122">L'identificatore del PIN viene usato per la persistenza del grafo.</span><span class="sxs-lookup"><span data-stu-id="0b416-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="0b416-123">L'identificatore del PIN per questa classe è out. Questa classe esegue l'override del comportamento della classe [**CBasePin**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="0b416-123">The pin identifier for this class is Out. This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="0b416-124">Nella classe **CBasePin** l'identificatore del PIN è uguale al nome del PIN, specificato nel costruttore della classe.</span><span class="sxs-lookup"><span data-stu-id="0b416-124">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="0b416-125">Nella classe **CTransformInputPin** , l'identificatore del PIN e il nome del PIN non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="0b416-125">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b416-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b416-126">Requirements</span></span>



| <span data-ttu-id="0b416-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b416-127">Requirement</span></span> | <span data-ttu-id="0b416-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0b416-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b416-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b416-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0b416-130"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b416-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0b416-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b416-131">Library</span></span><br/> | <dl> <span data-ttu-id="0b416-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0b416-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




