---
description: 'Metodo CTransformOutputPin.CheckConnect: il metodo CheckConnect determina se una connessione pin è adatta.'
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Metodo CTransformOutputPin.CheckConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 190acd2fbab5206b114b57719d350e3ad5eac0c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094949"
---
# <a name="ctransformoutputpincheckconnect-method"></a><span data-ttu-id="6c555-103">Metodo CTransformOutputPin.CheckConnect</span><span class="sxs-lookup"><span data-stu-id="6c555-103">CTransformOutputPin.CheckConnect method</span></span>

<span data-ttu-id="6c555-104">Il `CheckConnect` metodo determina se una connessione pin è adatta.</span><span class="sxs-lookup"><span data-stu-id="6c555-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c555-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c555-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="6c555-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c555-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c555-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="6c555-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="6c555-108">Puntatore all'interfaccia [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di output.</span><span class="sxs-lookup"><span data-stu-id="6c555-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c555-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c555-109">Return value</span></span>

<span data-ttu-id="6c555-110">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="6c555-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6c555-111">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="6c555-111">Possible values include the following.</span></span>



| <span data-ttu-id="6c555-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6c555-112">Return code</span></span>                                                                                  | <span data-ttu-id="6c555-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c555-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="6c555-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6c555-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6c555-115">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="6c555-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="6c555-116"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="6c555-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="6c555-117">Il pin di input del filtro non è connesso.</span><span class="sxs-lookup"><span data-stu-id="6c555-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c555-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c555-118">Remarks</span></span>

<span data-ttu-id="6c555-119">Questo metodo esegue l'override [**del metodo CBaseOutputPin::CheckConnect.**](cbaseoutputpin-checkconnect.md)</span><span class="sxs-lookup"><span data-stu-id="6c555-119">This method overrides the [**CBaseOutputPin::CheckConnect**](cbaseoutputpin-checkconnect.md) method.</span></span> <span data-ttu-id="6c555-120">Chiama il metodo [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) del filtro, che restituisce S \_ OK nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="6c555-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="6c555-121">La classe derivata può eseguire l'override del **metodo CTransformFilter::CheckConnect** per eseguire controlli aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="6c555-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c555-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c555-122">Requirements</span></span>



| <span data-ttu-id="6c555-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c555-123">Requirement</span></span> | <span data-ttu-id="6c555-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6c555-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c555-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c555-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6c555-126"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c555-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6c555-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c555-127">Library</span></span><br/> | <dl> <span data-ttu-id="6c555-128"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6c555-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




