---
description: 'Costruttore CSourceStream.CSourceStream : metodo costruttore.'
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Costruttore CSourceStream.CSourceStream (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75d94bb89ca109c2a7974c294153d46235f92f23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085189"
---
# <a name="csourcestreamcsourcestream-constructor"></a><span data-ttu-id="dfe0d-103">Costruttore CSourceStream.CSourceStream</span><span class="sxs-lookup"><span data-stu-id="dfe0d-103">CSourceStream.CSourceStream constructor</span></span>

<span data-ttu-id="dfe0d-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="dfe0d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfe0d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfe0d-105">Syntax</span></span>


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="dfe0d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dfe0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfe0d-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="dfe0d-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="dfe0d-108">Puntatore a una stringa contenente il nome di debug del segnaposto.</span><span class="sxs-lookup"><span data-stu-id="dfe0d-108">Pointer to a string containing the debug name of the pin.</span></span>

</dd> <dt>

<span data-ttu-id="dfe0d-109">*Phr*</span><span class="sxs-lookup"><span data-stu-id="dfe0d-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="dfe0d-110">Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="dfe0d-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="dfe0d-111">Inizializzare il valore su S \_ OK prima di creare l'oggetto .</span><span class="sxs-lookup"><span data-stu-id="dfe0d-111">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="dfe0d-112">Il valore viene modificato solo se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="dfe0d-112">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="dfe0d-113">*Pms*</span><span class="sxs-lookup"><span data-stu-id="dfe0d-113">*pms*</span></span> 
</dt> <dd>

<span data-ttu-id="dfe0d-114">Puntatore al [**filtro CSource**](csource.md) che ha creato questo segnaposto.</span><span class="sxs-lookup"><span data-stu-id="dfe0d-114">Pointer to the [**CSource**](csource.md) filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="dfe0d-115">*Pname*</span><span class="sxs-lookup"><span data-stu-id="dfe0d-115">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="dfe0d-116">Puntatore a una stringa che contiene il nome del segnaposto.</span><span class="sxs-lookup"><span data-stu-id="dfe0d-116">Pointer to a string that contains the name of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfe0d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfe0d-117">Remarks</span></span>

<span data-ttu-id="dfe0d-118">La stringa specificata nel *parametro pObjectName* viene usata solo a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="dfe0d-118">The string given in the *pObjectName* parameter is used only for debugging purposes.</span></span> <span data-ttu-id="dfe0d-119">Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="dfe0d-119">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

<span data-ttu-id="dfe0d-120">La stringa specificata nel *parametro pName* è il nome restituito dal [**metodo IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)</span><span class="sxs-lookup"><span data-stu-id="dfe0d-120">The string given in the *pName* parameter is the name returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="dfe0d-121">La `CSourceStream` classe non usa questo nome per l'identificatore pin restituito dal metodo [**CSourceStream::QueryId.**](csourcestream-queryid.md)</span><span class="sxs-lookup"><span data-stu-id="dfe0d-121">The `CSourceStream` class does not use this name for the pin identifier returned by the [**CSourceStream::QueryId**](csourcestream-queryid.md) method.</span></span> <span data-ttu-id="dfe0d-122">QueryId calcola **invece** un identificatore pin in base al numero di pin.</span><span class="sxs-lookup"><span data-stu-id="dfe0d-122">Instead, **QueryId** calculates a pin identifier based on the pin number.</span></span> <span data-ttu-id="dfe0d-123">Gli identificatori pin supportano la persistenza del grafo.</span><span class="sxs-lookup"><span data-stu-id="dfe0d-123">(Pin identifiers support graph persistence.</span></span> <span data-ttu-id="dfe0d-124">Per altre informazioni, vedere [**IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)</span><span class="sxs-lookup"><span data-stu-id="dfe0d-124">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span></span>

<span data-ttu-id="dfe0d-125">Il costruttore aggiunge automaticamente il pin al filtro proprietario chiamando [**CSource::AddPin**](csource-addpin.md).</span><span class="sxs-lookup"><span data-stu-id="dfe0d-125">The constructor automatically adds the pin to the owning filter, by calling [**CSource::AddPin**](csource-addpin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfe0d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfe0d-126">Requirements</span></span>



| <span data-ttu-id="dfe0d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfe0d-127">Requirement</span></span> | <span data-ttu-id="dfe0d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="dfe0d-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe0d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dfe0d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="dfe0d-130"><dt>Source.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfe0d-130"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="dfe0d-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="dfe0d-131">Library</span></span><br/> | <dl> <span data-ttu-id="dfe0d-132"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dfe0d-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfe0d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfe0d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe0d-134">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="dfe0d-134">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




