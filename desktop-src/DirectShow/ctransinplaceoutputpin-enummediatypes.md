---
description: 'Metodo CTransInPlaceOutputPin.EnumMediaTypes: il metodo EnumMediaTypes enumera i tipi di supporti preferiti del pin. Questo metodo implementa il metodo IPin::EnumMediaTypes.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: Metodo CTransInPlaceOutputPin.EnumMediaTypes (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26dd58f23dc18a086c6c59f6f8a6a098e3449fea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084635"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a><span data-ttu-id="11cfb-104">Metodo CTransInPlaceOutputPin.EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="11cfb-104">CTransInPlaceOutputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="11cfb-105">Il `EnumMediaTypes` metodo enumera i tipi di supporti preferiti del pin.</span><span class="sxs-lookup"><span data-stu-id="11cfb-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="11cfb-106">Questo metodo implementa il [**metodo IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)</span><span class="sxs-lookup"><span data-stu-id="11cfb-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="11cfb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11cfb-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="11cfb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="11cfb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11cfb-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="11cfb-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="11cfb-110">Riceve un puntatore [**all'interfaccia IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)</span><span class="sxs-lookup"><span data-stu-id="11cfb-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11cfb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11cfb-111">Return value</span></span>

<span data-ttu-id="11cfb-112">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="11cfb-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="11cfb-113">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="11cfb-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="11cfb-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="11cfb-114">Return code</span></span>                                                                                           | <span data-ttu-id="11cfb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11cfb-115">Description</span></span>                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="11cfb-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11cfb-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="11cfb-117">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="11cfb-117">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="11cfb-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="11cfb-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="11cfb-119">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="11cfb-119">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="11cfb-120"><dt>**PUNTATORE E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="11cfb-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="11cfb-121">**Puntatore NULL.**</span><span class="sxs-lookup"><span data-stu-id="11cfb-121">**NULL** pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="11cfb-122"><dt>**VFW \_ E \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="11cfb-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="11cfb-123">Il pin di input del filtro non è connesso.</span><span class="sxs-lookup"><span data-stu-id="11cfb-123">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11cfb-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="11cfb-124">Remarks</span></span>

<span data-ttu-id="11cfb-125">Questo metodo restituisce **l'interfaccia IEnumMediaTypes** dal pin di output upstream.</span><span class="sxs-lookup"><span data-stu-id="11cfb-125">This method returns the **IEnumMediaTypes** interface from the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="11cfb-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11cfb-126">Requirements</span></span>



| <span data-ttu-id="11cfb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="11cfb-127">Requirement</span></span> | <span data-ttu-id="11cfb-128">Valore</span><span class="sxs-lookup"><span data-stu-id="11cfb-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11cfb-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11cfb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="11cfb-130"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="11cfb-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="11cfb-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="11cfb-131">Library</span></span><br/> | <dl> <span data-ttu-id="11cfb-132"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="11cfb-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11cfb-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11cfb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11cfb-134">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="11cfb-134">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




