---
description: Dato un elenco di tipi di supporto, il metodo TryMediaTypes tenta di completare una connessione usando uno di questi tipi.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Metodo CBasePin. TryMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19b8da39d07b8aae9401bdc6ccf2eecb5d3a1e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327345"
---
# <a name="cbasepintrymediatypes-method"></a><span data-ttu-id="d9b96-103">CBasePin. TryMediaTypes, metodo</span><span class="sxs-lookup"><span data-stu-id="d9b96-103">CBasePin.TryMediaTypes method</span></span>

<span data-ttu-id="d9b96-104">Dato un elenco di tipi di supporto, il `TryMediaTypes` Metodo prova a completare una connessione usando uno di questi tipi.</span><span class="sxs-lookup"><span data-stu-id="d9b96-104">Given a list of media types, the `TryMediaTypes` method tries to complete a connection using one of those types.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9b96-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9b96-105">Syntax</span></span>


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="d9b96-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9b96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b96-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="d9b96-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b96-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di ricezione.</span><span class="sxs-lookup"><span data-stu-id="d9b96-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d9b96-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="d9b96-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b96-110">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che limita i tipi di supporti possibili o **null**.</span><span class="sxs-lookup"><span data-stu-id="d9b96-110">Pointer to a [**CMediaType**](cmediatype.md) object that limits the possible media types, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d9b96-111">*pEnum*</span><span class="sxs-lookup"><span data-stu-id="d9b96-111">*pEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b96-112">Puntatore a un'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) , usata per enumerare l'elenco dei tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="d9b96-112">Pointer to an [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface, used to enumerate the list of media types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b96-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9b96-113">Return value</span></span>

<span data-ttu-id="d9b96-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d9b96-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d9b96-115">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d9b96-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="d9b96-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d9b96-116">Return code</span></span>                                                                                                  | <span data-ttu-id="d9b96-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9b96-117">Description</span></span>                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="d9b96-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b96-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="d9b96-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d9b96-119">Success.</span></span><br/>                               |
| <dl> <span data-ttu-id="d9b96-120"><dt>**VFW \_ E \_ nessun \_ \_ tipo accettabile**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b96-120"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="d9b96-121">Non è stato trovato alcun tipo di supporto accettabile.</span><span class="sxs-lookup"><span data-stu-id="d9b96-121">Did not find an acceptable media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d9b96-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9b96-122">Remarks</span></span>

<span data-ttu-id="d9b96-123">Per ogni tipo di supporto restituito dall'interfaccia **IEnumMediaTypes** , questo metodo tenta una connessione chiamando il metodo [**CBasePin:: AttemptConnection**](cbasepin-attemptconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="d9b96-123">For each media type returned by the **IEnumMediaTypes** interface, this method attempts a connection by calling the [**CBasePin::AttemptConnection**](cbasepin-attemptconnection.md) method.</span></span>

<span data-ttu-id="d9b96-124">Se il parametro *PMT* è diverso da **null**, il pin ignora i tipi di supporto che non corrispondono a questo tipo.</span><span class="sxs-lookup"><span data-stu-id="d9b96-124">If the *pmt* parameter is non-**NULL**, the pin skips media types that do not match this type.</span></span> <span data-ttu-id="d9b96-125">Il parametro *PMT* può specificare un tipo di supporto parziale.</span><span class="sxs-lookup"><span data-stu-id="d9b96-125">The *pmt* parameter can specify a partial media type.</span></span> <span data-ttu-id="d9b96-126">Un tipo di supporto parziale ha un valore GUID \_ null per il tipo principale, il sottotipo o il formato.</span><span class="sxs-lookup"><span data-stu-id="d9b96-126">A partial media type has a value of GUID\_NULL for either the major type, the subtype, or the format.</span></span> <span data-ttu-id="d9b96-127">Il \_ valore null del GUID corrisponde a qualsiasi tipo, simile a un valore "jolly".</span><span class="sxs-lookup"><span data-stu-id="d9b96-127">The GUID\_NULL value matches any type, similar to a "wildcard" value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b96-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9b96-128">Requirements</span></span>



| <span data-ttu-id="d9b96-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9b96-129">Requirement</span></span> | <span data-ttu-id="d9b96-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d9b96-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b96-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9b96-131">Header</span></span><br/>  | <dl> <span data-ttu-id="d9b96-132"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9b96-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d9b96-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="d9b96-133">Library</span></span><br/> | <dl> <span data-ttu-id="d9b96-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d9b96-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b96-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9b96-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b96-136">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="d9b96-136">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




