---
description: 'Metodo CTransformOutputPin.QueryId: il metodo QueryId recupera un identificatore per il pin. Questo metodo implementa il metodo IPin::QueryId.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: Metodo CTransformOutputPin.QueryId (Transfrm.h)
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
ms.openlocfilehash: d4c2d222ca4dd184adfe41f9f610b10f15ee9f02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094849"
---
# <a name="ctransformoutputpinqueryid-method"></a><span data-ttu-id="76131-104">Metodo CTransformOutputPin.QueryId</span><span class="sxs-lookup"><span data-stu-id="76131-104">CTransformOutputPin.QueryId method</span></span>

<span data-ttu-id="76131-105">Il `QueryId` metodo recupera un identificatore per il pin.</span><span class="sxs-lookup"><span data-stu-id="76131-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="76131-106">Questo metodo implementa il [**metodo IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)</span><span class="sxs-lookup"><span data-stu-id="76131-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="76131-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76131-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="76131-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="76131-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76131-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="76131-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="76131-110">Riceve una stringa contenente l'identificatore pin.</span><span class="sxs-lookup"><span data-stu-id="76131-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76131-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76131-111">Return value</span></span>

<span data-ttu-id="76131-112">Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="76131-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="76131-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="76131-113">Return code</span></span>                                                                                   | <span data-ttu-id="76131-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76131-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="76131-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="76131-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="76131-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="76131-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="76131-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="76131-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="76131-118">Memoria insufficiente</span><span class="sxs-lookup"><span data-stu-id="76131-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="76131-119"><dt>**PUNTATORE E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76131-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="76131-120">**Argomento puntatore NULL**</span><span class="sxs-lookup"><span data-stu-id="76131-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76131-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="76131-121">Remarks</span></span>

<span data-ttu-id="76131-122">L'identificatore pin viene usato per la persistenza del grafico.</span><span class="sxs-lookup"><span data-stu-id="76131-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="76131-123">L'identificatore pin per questa classe è Out. Questa classe esegue l'override del comportamento della [**classe CBasePin.**](cbasepin.md)</span><span class="sxs-lookup"><span data-stu-id="76131-123">The pin identifier for this class is Out. This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="76131-124">Nella classe **CBasePin** l'identificatore pin corrisponde al nome del pin, specificato nel costruttore della classe.</span><span class="sxs-lookup"><span data-stu-id="76131-124">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="76131-125">Nella classe **CTransformInputPin** l'identificatore del pin e il nome del pin non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="76131-125">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="76131-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76131-126">Requirements</span></span>



| <span data-ttu-id="76131-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="76131-127">Requirement</span></span> | <span data-ttu-id="76131-128">Valore</span><span class="sxs-lookup"><span data-stu-id="76131-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76131-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76131-129">Header</span></span><br/>  | <dl> <span data-ttu-id="76131-130"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="76131-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="76131-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="76131-131">Library</span></span><br/> | <dl> <span data-ttu-id="76131-132"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="76131-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




