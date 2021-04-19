---
description: Il metodo AgreeMediaType Cerca un tipo di supporto per creare una connessione pin.
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: Metodo CBasePin. AgreeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332783"
---
# <a name="cbasepinagreemediatype-method"></a><span data-ttu-id="3beb6-103">CBasePin. AgreeMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="3beb6-103">CBasePin.AgreeMediaType method</span></span>

<span data-ttu-id="3beb6-104">Il `AgreeMediaType` metodo cerca un tipo di supporto per creare una connessione pin.</span><span class="sxs-lookup"><span data-stu-id="3beb6-104">The `AgreeMediaType` method searches for a media type to make a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3beb6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3beb6-105">Syntax</span></span>


```C++
virtual HRESULT AgreeMediaType(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="3beb6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3beb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3beb6-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="3beb6-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="3beb6-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di ricezione.</span><span class="sxs-lookup"><span data-stu-id="3beb6-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="3beb6-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="3beb6-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="3beb6-110">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica un tipo di supporto o **null**.</span><span class="sxs-lookup"><span data-stu-id="3beb6-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies a media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3beb6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3beb6-111">Return value</span></span>

<span data-ttu-id="3beb6-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3beb6-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3beb6-113">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3beb6-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="3beb6-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3beb6-114">Return code</span></span>                                                                                                  | <span data-ttu-id="3beb6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3beb6-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="3beb6-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3beb6-116"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="3beb6-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3beb6-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="3beb6-118"><dt>**VFW \_ E \_ nessun \_ \_ tipo accettabile**</dt></span><span class="sxs-lookup"><span data-stu-id="3beb6-118"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="3beb6-119">Non è stato trovato alcun tipo di supporto accettabile.</span><span class="sxs-lookup"><span data-stu-id="3beb6-119">No acceptable media type was found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3beb6-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="3beb6-120">Remarks</span></span>

<span data-ttu-id="3beb6-121">Se il parametro *PMT* è non **null** e specifica completamente un tipo di supporto, questo metodo tenta una connessione usando tale tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="3beb6-121">If the *pmt* parameter is non-**NULL** and fully specifies a media type, this method attempts a connection using that media type.</span></span> <span data-ttu-id="3beb6-122">Se il tentativo ha esito negativo, il metodo restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="3beb6-122">If the attempt fails, the method returns an error.</span></span>

<span data-ttu-id="3beb6-123">Se il parametro *PMT* è **null** o specifica un tipo di supporto parziale, questo metodo tenta i tipi di supporto nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="3beb6-123">If the *pmt* parameter is **NULL** or specifies a partial media type, this method tries media types in the following order:</span></span>

1.  <span data-ttu-id="3beb6-124">Tipi di supporto preferiti del PIN di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3beb6-124">The receiving pin's preferred media types.</span></span>
2.  <span data-ttu-id="3beb6-125">Tipi di supporti preferiti del PIN.</span><span class="sxs-lookup"><span data-stu-id="3beb6-125">This pin's preferred media types.</span></span>

<span data-ttu-id="3beb6-126">I tipi di supporto Preferiti vengono enumerati con il metodo [**CBasePin:: EnumMediaTypes**](cbasepin-enummediatypes.md) e l'enumeratore risultante viene passato al metodo [**CBasePin:: TryMediaTypes**](cbasepin-trymediatypes.md) .</span><span class="sxs-lookup"><span data-stu-id="3beb6-126">Preferred media types are enumerated with the [**CBasePin::EnumMediaTypes**](cbasepin-enummediatypes.md) method, and the resulting enumerator is passed to the [**CBasePin::TryMediaTypes**](cbasepin-trymediatypes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3beb6-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3beb6-127">Requirements</span></span>



| <span data-ttu-id="3beb6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3beb6-128">Requirement</span></span> | <span data-ttu-id="3beb6-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3beb6-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3beb6-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3beb6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3beb6-131"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3beb6-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3beb6-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="3beb6-132">Library</span></span><br/> | <dl> <span data-ttu-id="3beb6-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3beb6-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3beb6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3beb6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3beb6-135">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="3beb6-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




