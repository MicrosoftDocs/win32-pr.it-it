---
description: Il metodo CheckStreaming determina se il pin può accettare esempi.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Metodo CTransformInputPin. CheckStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328811"
---
# <a name="ctransforminputpincheckstreaming-method"></a><span data-ttu-id="8e341-103">CTransformInputPin. CheckStreaming, metodo</span><span class="sxs-lookup"><span data-stu-id="8e341-103">CTransformInputPin.CheckStreaming method</span></span>

<span data-ttu-id="8e341-104">Il `CheckStreaming` metodo determina se il pin può accettare esempi.</span><span class="sxs-lookup"><span data-stu-id="8e341-104">The `CheckStreaming` method determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e341-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e341-105">Syntax</span></span>


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="8e341-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e341-106">Parameters</span></span>

<span data-ttu-id="8e341-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8e341-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e341-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e341-108">Return value</span></span>

<span data-ttu-id="8e341-109">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8e341-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="8e341-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8e341-110">Return code</span></span>                                                                                           | <span data-ttu-id="8e341-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e341-111">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="8e341-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8e341-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="8e341-113">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8e341-113">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="8e341-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="8e341-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="8e341-115">È in corso lo scaricamento del PIN.</span><span class="sxs-lookup"><span data-stu-id="8e341-115">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="8e341-116"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="8e341-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8e341-117">Il pin di output non è connesso.</span><span class="sxs-lookup"><span data-stu-id="8e341-117">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="8e341-118"><dt>**errore di runtime di VFW \_ E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8e341-118"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="8e341-119">Si è verificato un errore in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8e341-119">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="8e341-120"><dt>**\_ \_ stato non corretto di VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8e341-120"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="8e341-121">Il PIN è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="8e341-121">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="8e341-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e341-122">Remarks</span></span>

<span data-ttu-id="8e341-123">Questo metodo esegue l'override del metodo [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="8e341-123">This method overrides the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e341-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e341-124">Requirements</span></span>



| <span data-ttu-id="8e341-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e341-125">Requirement</span></span> | <span data-ttu-id="8e341-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8e341-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e341-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e341-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8e341-128"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e341-128"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8e341-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="8e341-129">Library</span></span><br/> | <dl> <span data-ttu-id="8e341-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8e341-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




