---
description: Il metodo CheckConnect determina se una connessione pin è adatta.
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Metodo CTransformInputPin. CheckConnect (Transfrm. h)
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
ms.openlocfilehash: e10c174a4e295576cfa9ce902faeac889f5a6a9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328814"
---
# <a name="ctransforminputpincheckconnect-method"></a><span data-ttu-id="eb5aa-103">CTransformInputPin. CheckConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="eb5aa-103">CTransformInputPin.CheckConnect method</span></span>

<span data-ttu-id="eb5aa-104">Il `CheckConnect` metodo determina se una connessione pin è adatta.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb5aa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb5aa-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="eb5aa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb5aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb5aa-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="eb5aa-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="eb5aa-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb5aa-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb5aa-109">Return value</span></span>

<span data-ttu-id="eb5aa-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="eb5aa-111">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="eb5aa-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="eb5aa-112">Return code</span></span>                                                                                               | <span data-ttu-id="eb5aa-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb5aa-113">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="eb5aa-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eb5aa-114"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="eb5aa-115">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="eb5aa-115">Success</span></span><br/>             |
| <dl> <span data-ttu-id="eb5aa-116"><dt>**\_direzione VFW E \_ non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb5aa-116"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="eb5aa-117">Direzione del pin errata</span><span class="sxs-lookup"><span data-stu-id="eb5aa-117">Wrong pin direction</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb5aa-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb5aa-118">Remarks</span></span>

<span data-ttu-id="eb5aa-119">Questo metodo esegue l'override del metodo [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="eb5aa-119">This method overrides the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method.</span></span> <span data-ttu-id="eb5aa-120">Chiama il metodo [**CTransformFilter:: CheckConnect**](ctransformfilter-checkconnect.md) del filtro, che restituisce \_ OK nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="eb5aa-121">La classe derivata può eseguire l'override del metodo **CTransformFilter:: CheckConnect** per eseguire ulteriori controlli.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb5aa-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb5aa-122">Requirements</span></span>



| <span data-ttu-id="eb5aa-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb5aa-123">Requirement</span></span> | <span data-ttu-id="eb5aa-124">Valore</span><span class="sxs-lookup"><span data-stu-id="eb5aa-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5aa-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb5aa-125">Header</span></span><br/>  | <dl> <span data-ttu-id="eb5aa-126"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb5aa-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb5aa-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb5aa-127">Library</span></span><br/> | <dl> <span data-ttu-id="eb5aa-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eb5aa-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




