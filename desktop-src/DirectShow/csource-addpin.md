---
description: Il metodo AddPin aggiunge un nuovo PIN di output al filtro.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: Metodo CSource. AddPin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324658"
---
# <a name="csourceaddpin-method"></a><span data-ttu-id="c242c-103">CSource. AddPin, metodo</span><span class="sxs-lookup"><span data-stu-id="c242c-103">CSource.AddPin method</span></span>

<span data-ttu-id="c242c-104">Il `AddPin` metodo aggiunge un nuovo PIN di output al filtro.</span><span class="sxs-lookup"><span data-stu-id="c242c-104">The `AddPin` method adds a new output pin to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c242c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c242c-105">Syntax</span></span>


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="c242c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c242c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c242c-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="c242c-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="c242c-108">Puntatore all'oggetto [**CSourceStream**](csourcestream.md) che implementa il PIN.</span><span class="sxs-lookup"><span data-stu-id="c242c-108">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c242c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c242c-109">Return value</span></span>

<span data-ttu-id="c242c-110">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c242c-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c242c-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c242c-111">Return code</span></span>                                                                                   | <span data-ttu-id="c242c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c242c-112">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="c242c-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c242c-113"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c242c-114">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="c242c-114">Success</span></span><br/>             |
| <dl> <span data-ttu-id="c242c-115"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="c242c-115"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c242c-116">Memoria insufficiente</span><span class="sxs-lookup"><span data-stu-id="c242c-116">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c242c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c242c-117">Remarks</span></span>

<span data-ttu-id="c242c-118">Quando si crea un nuovo PIN derivato da **CSourceStream**, il costruttore **CSourceStream** chiama automaticamente questo metodo per aggiungere il pin di output al filtro.</span><span class="sxs-lookup"><span data-stu-id="c242c-118">When you create a new pin derived from **CSourceStream**, the **CSourceStream** constructor automatically calls this method, to add the output pin to the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c242c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c242c-119">Requirements</span></span>



| <span data-ttu-id="c242c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c242c-120">Requirement</span></span> | <span data-ttu-id="c242c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c242c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c242c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c242c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c242c-123"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c242c-123"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c242c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="c242c-124">Library</span></span><br/> | <dl> <span data-ttu-id="c242c-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c242c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c242c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c242c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c242c-127">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="c242c-127">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




