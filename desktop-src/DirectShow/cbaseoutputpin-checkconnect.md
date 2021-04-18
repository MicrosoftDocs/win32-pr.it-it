---
description: Il metodo CheckConnect determina se una connessione pin è adatta.
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Metodo CBaseOutputPin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3274e47e9a77d86f350c17aaca04ec0cdb95ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329553"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="5cee1-103">CBaseOutputPin. CheckConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="5cee1-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="5cee1-104">Il `CheckConnect` metodo determina se una connessione pin è adatta.</span><span class="sxs-lookup"><span data-stu-id="5cee1-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cee1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5cee1-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="5cee1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cee1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cee1-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="5cee1-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="5cee1-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="5cee1-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cee1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cee1-109">Return value</span></span>

<span data-ttu-id="5cee1-110">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5cee1-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="5cee1-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5cee1-111">Return code</span></span>                                                                                               | <span data-ttu-id="5cee1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cee1-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5cee1-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5cee1-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="5cee1-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5cee1-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="5cee1-115"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="5cee1-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="5cee1-116">Il pin di input non supporta [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span><span class="sxs-lookup"><span data-stu-id="5cee1-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="5cee1-117"><dt>**\_direzione VFW E \_ non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5cee1-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="5cee1-118">Le direzioni del PIN non sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="5cee1-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="5cee1-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cee1-119">Remarks</span></span>

<span data-ttu-id="5cee1-120">Questo metodo chiama il metodo [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) della classe di base e quindi esegue una query sul pin di input per la relativa interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="5cee1-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cee1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cee1-121">Requirements</span></span>



| <span data-ttu-id="5cee1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cee1-122">Requirement</span></span> | <span data-ttu-id="5cee1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5cee1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cee1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cee1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5cee1-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5cee1-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5cee1-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="5cee1-126">Library</span></span><br/> | <dl> <span data-ttu-id="5cee1-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5cee1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cee1-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cee1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cee1-129">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="5cee1-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




