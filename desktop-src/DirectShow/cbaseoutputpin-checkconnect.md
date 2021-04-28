---
description: 'Metodo CBaseOutputPin.CheckConnect: il metodo CheckConnect determina se una connessione pin è adatta.'
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Metodo CBaseOutputPin.CheckConnect (Amfilter.h)
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
ms.openlocfilehash: 7ea5ad32de18046f3d23145d82e971391c3e304c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096189"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="83208-103">Metodo CBaseOutputPin.CheckConnect</span><span class="sxs-lookup"><span data-stu-id="83208-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="83208-104">Il `CheckConnect` metodo determina se una connessione pin è adatta.</span><span class="sxs-lookup"><span data-stu-id="83208-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="83208-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83208-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="83208-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83208-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="83208-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="83208-108">Puntatore all'interfaccia [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin di input.</span><span class="sxs-lookup"><span data-stu-id="83208-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83208-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83208-109">Return value</span></span>

<span data-ttu-id="83208-110">Restituisce uno dei valori **HRESULT** seguenti.</span><span class="sxs-lookup"><span data-stu-id="83208-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="83208-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="83208-111">Return code</span></span>                                                                                               | <span data-ttu-id="83208-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83208-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83208-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="83208-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="83208-114">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="83208-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="83208-115"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="83208-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="83208-116">Il pin di input non supporta [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)</span><span class="sxs-lookup"><span data-stu-id="83208-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="83208-117"><dt>**DIREZIONE VFW \_ E \_ NON \_ VALIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="83208-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="83208-118">Le indicazioni stradali non sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="83208-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="83208-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="83208-119">Remarks</span></span>

<span data-ttu-id="83208-120">Questo metodo chiama il metodo [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) della classe base e quindi esegue una query sul pin di input per [**l'interfaccia IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)</span><span class="sxs-lookup"><span data-stu-id="83208-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="83208-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83208-121">Requirements</span></span>



| <span data-ttu-id="83208-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="83208-122">Requirement</span></span> | <span data-ttu-id="83208-123">Valore</span><span class="sxs-lookup"><span data-stu-id="83208-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83208-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83208-124">Header</span></span><br/>  | <dl> <span data-ttu-id="83208-125"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="83208-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="83208-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="83208-126">Library</span></span><br/> | <dl> <span data-ttu-id="83208-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="83208-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83208-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83208-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83208-129">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="83208-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




