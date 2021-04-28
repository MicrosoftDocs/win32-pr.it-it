---
description: 'Metodo CTransformInputPin.CheckConnect: il metodo CheckConnect determina se una connessione pin è adatta.'
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Metodo CTransformInputPin.CheckConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e981254677c2e0a361a0a21f125f734ff1403db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095089"
---
# <a name="ctransforminputpincheckconnect-method"></a><span data-ttu-id="c6c2a-103">Metodo CTransformInputPin.CheckConnect</span><span class="sxs-lookup"><span data-stu-id="c6c2a-103">CTransformInputPin.CheckConnect method</span></span>

<span data-ttu-id="c6c2a-104">Il `CheckConnect` metodo determina se una connessione pin è adatta.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c2a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6c2a-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="c6c2a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6c2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c2a-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="c6c2a-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c2a-108">Puntatore all'interfaccia [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di output.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c2a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6c2a-109">Return value</span></span>

<span data-ttu-id="c6c2a-110">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c6c2a-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c6c2a-111">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c6c2a-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c6c2a-112">Return code</span></span>                                                                                               | <span data-ttu-id="c6c2a-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6c2a-113">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="c6c2a-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c6c2a-114"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="c6c2a-115">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="c6c2a-115">Success</span></span><br/>             |
| <dl> <span data-ttu-id="c6c2a-116"><dt>**DIREZIONE VFW \_ E \_ NON \_ VALIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="c6c2a-116"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="c6c2a-117">Direzione del segnaposto errata</span><span class="sxs-lookup"><span data-stu-id="c6c2a-117">Wrong pin direction</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c6c2a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6c2a-118">Remarks</span></span>

<span data-ttu-id="c6c2a-119">Questo metodo esegue l'override [**del metodo CBasePin::CheckConnect.**](cbasepin-checkconnect.md)</span><span class="sxs-lookup"><span data-stu-id="c6c2a-119">This method overrides the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method.</span></span> <span data-ttu-id="c6c2a-120">Chiama il metodo [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) del filtro, che restituisce S \_ OK nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="c6c2a-121">La classe derivata può eseguire l'override del **metodo CTransformFilter::CheckConnect** per eseguire controlli aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c2a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6c2a-122">Requirements</span></span>



| <span data-ttu-id="c6c2a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6c2a-123">Requirement</span></span> | <span data-ttu-id="c6c2a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c6c2a-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c2a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6c2a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c6c2a-126"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c2a-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c6c2a-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="c6c2a-127">Library</span></span><br/> | <dl> <span data-ttu-id="c6c2a-128"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c2a-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




