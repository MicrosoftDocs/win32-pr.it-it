---
description: Il metodo BreakConnect rilascia il pin da una connessione.
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Metodo CTransformInputPin. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2274b71b67a54ecacb291d77d2eef4ad8a110fa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332707"
---
# <a name="ctransforminputpinbreakconnect-method"></a><span data-ttu-id="ebbd5-103">CTransformInputPin. BreakConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="ebbd5-103">CTransformInputPin.BreakConnect method</span></span>

<span data-ttu-id="ebbd5-104">Il `BreakConnect` metodo rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="ebbd5-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebbd5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebbd5-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="ebbd5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebbd5-106">Parameters</span></span>

<span data-ttu-id="ebbd5-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ebbd5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebbd5-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebbd5-108">Return value</span></span>

<span data-ttu-id="ebbd5-109">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ebbd5-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebbd5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebbd5-110">Remarks</span></span>

<span data-ttu-id="ebbd5-111">Questo metodo esegue l'override del metodo [**CBaseInputPin:: BreakConnect**](cbaseinputpin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="ebbd5-111">This method overrides the [**CBaseInputPin::BreakConnect**](cbaseinputpin-breakconnect.md) method.</span></span> <span data-ttu-id="ebbd5-112">Chiama il metodo [**CTransformFilter:: BreakConnect**](ctransformfilter-breakconnect.md) del filtro, che restituisce \_ OK nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="ebbd5-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="ebbd5-113">La classe derivata può eseguire l'override del metodo **CTransformFilter:: BreakConnect** .</span><span class="sxs-lookup"><span data-stu-id="ebbd5-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebbd5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebbd5-114">Requirements</span></span>



| <span data-ttu-id="ebbd5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebbd5-115">Requirement</span></span> | <span data-ttu-id="ebbd5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ebbd5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebbd5-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebbd5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ebbd5-118"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebbd5-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ebbd5-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="ebbd5-119">Library</span></span><br/> | <dl> <span data-ttu-id="ebbd5-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ebbd5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




