---
description: 'Metodo CDynamicOutputPin.Disconnect: il metodo Disconnect interrompe la connessione pin corrente. Questo metodo implementa il metodo IPin::D isconnect.'
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Metodo CDynamicOutputPin.Disconnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a775146973b353413fa2e74584a6c763b721e7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099299"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="d5616-104">Metodo CDynamicOutputPin.Disconnect</span><span class="sxs-lookup"><span data-stu-id="d5616-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="d5616-105">Il `Disconnect` metodo interrompe la connessione pin corrente.</span><span class="sxs-lookup"><span data-stu-id="d5616-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="d5616-106">Questo metodo implementa il [**metodo IPin::D isconnect.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)</span><span class="sxs-lookup"><span data-stu-id="d5616-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5616-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5616-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="d5616-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5616-108">Parameters</span></span>

<span data-ttu-id="d5616-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d5616-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5616-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5616-110">Return value</span></span>

<span data-ttu-id="d5616-111">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d5616-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d5616-112">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d5616-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d5616-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d5616-113">Return code</span></span>                                                                             | <span data-ttu-id="d5616-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5616-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d5616-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d5616-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d5616-116">Il pin non è stato connesso.</span><span class="sxs-lookup"><span data-stu-id="d5616-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="d5616-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d5616-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d5616-118">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="d5616-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="d5616-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5616-119">Remarks</span></span>

<span data-ttu-id="d5616-120">Questo metodo esegue l'override del metodo [**CBasePin::D isconnect**](cbasepin-disconnect.md) per abilitare la disconnessione mentre il filtro è attivo.</span><span class="sxs-lookup"><span data-stu-id="d5616-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5616-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5616-121">Requirements</span></span>



| <span data-ttu-id="d5616-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5616-122">Requirement</span></span> | <span data-ttu-id="d5616-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d5616-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5616-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5616-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d5616-125"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5616-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d5616-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5616-126">Library</span></span><br/> | <dl> <span data-ttu-id="d5616-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d5616-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5616-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5616-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5616-129">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="d5616-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




