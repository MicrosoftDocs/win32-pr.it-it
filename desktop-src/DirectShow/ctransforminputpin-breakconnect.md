---
description: 'Metodo CTransformInputPin.BreakConnect: il metodo BreakConnect rilascia il pin da una connessione.'
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Metodo CTransformInputPin.BreakConnect (Transfrm.h)
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
ms.openlocfilehash: fe425ba617909dcfb1d66dbb4777b579139d436b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085019"
---
# <a name="ctransforminputpinbreakconnect-method"></a><span data-ttu-id="23497-103">Metodo CTransformInputPin.BreakConnect</span><span class="sxs-lookup"><span data-stu-id="23497-103">CTransformInputPin.BreakConnect method</span></span>

<span data-ttu-id="23497-104">Il `BreakConnect` metodo rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="23497-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="23497-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23497-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="23497-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23497-106">Parameters</span></span>

<span data-ttu-id="23497-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="23497-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="23497-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23497-108">Return value</span></span>

<span data-ttu-id="23497-109">Restituisce S \_ OK o un altro valore **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="23497-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23497-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="23497-110">Remarks</span></span>

<span data-ttu-id="23497-111">Questo metodo esegue l'override [**del metodo CBaseInputPin::BreakConnect.**](cbaseinputpin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="23497-111">This method overrides the [**CBaseInputPin::BreakConnect**](cbaseinputpin-breakconnect.md) method.</span></span> <span data-ttu-id="23497-112">Chiama il metodo [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) del filtro, che restituisce S \_ OK nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="23497-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="23497-113">La classe derivata può eseguire l'override del metodo **CTransformFilter::BreakConnect.**</span><span class="sxs-lookup"><span data-stu-id="23497-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="23497-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23497-114">Requirements</span></span>



| <span data-ttu-id="23497-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="23497-115">Requirement</span></span> | <span data-ttu-id="23497-116">Valore</span><span class="sxs-lookup"><span data-stu-id="23497-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23497-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23497-117">Header</span></span><br/>  | <dl> <span data-ttu-id="23497-118"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="23497-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="23497-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="23497-119">Library</span></span><br/> | <dl> <span data-ttu-id="23497-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="23497-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




