---
description: 'Metodo CTransInPlaceInputPin.EnumMediaTypes: il metodo EnumMediaTypes enumera i tipi di supporti preferiti del pin. Questo metodo implementa il metodo IPin::EnumMediaTypes.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Metodo CTransInPlaceInputPin.EnumMediaTypes (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f9e05d0e9db50cabc700da7b3803c1606efab78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094759"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="1265f-104">Metodo CTransInPlaceInputPin.EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="1265f-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="1265f-105">Il `EnumMediaTypes` metodo enumera i tipi di supporti preferiti del pin.</span><span class="sxs-lookup"><span data-stu-id="1265f-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="1265f-106">Questo metodo implementa il [**metodo IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)</span><span class="sxs-lookup"><span data-stu-id="1265f-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1265f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1265f-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="1265f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1265f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1265f-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="1265f-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="1265f-110">Riceve un puntatore [**all'interfaccia IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)</span><span class="sxs-lookup"><span data-stu-id="1265f-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1265f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1265f-111">Return value</span></span>

<span data-ttu-id="1265f-112">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="1265f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1265f-113">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1265f-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1265f-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1265f-114">Return code</span></span>                                                                                           | <span data-ttu-id="1265f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1265f-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="1265f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1265f-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="1265f-117">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="1265f-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="1265f-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1265f-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="1265f-119">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="1265f-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="1265f-120"><dt>**PUNTATORE E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1265f-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="1265f-121">**Puntatore NULL.**</span><span class="sxs-lookup"><span data-stu-id="1265f-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="1265f-122"><dt>**VFW \_ E \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="1265f-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1265f-123">Il pin di output non è connesso.</span><span class="sxs-lookup"><span data-stu-id="1265f-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1265f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="1265f-124">Remarks</span></span>

<span data-ttu-id="1265f-125">Questo metodo restituisce **l'interfaccia IEnumMediaTypes** dal pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="1265f-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1265f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1265f-126">Requirements</span></span>



| <span data-ttu-id="1265f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1265f-127">Requirement</span></span> | <span data-ttu-id="1265f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="1265f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1265f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1265f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1265f-130"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1265f-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1265f-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="1265f-131">Library</span></span><br/> | <dl> <span data-ttu-id="1265f-132"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1265f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1265f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1265f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1265f-134">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="1265f-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




