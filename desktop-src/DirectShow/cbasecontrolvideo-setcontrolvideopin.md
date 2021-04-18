---
description: Il metodo SetControlVideoPin imposta il PIN utilizzato dal filtro.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Metodo CBaseControlVideo. SetControlVideoPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325398"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a><span data-ttu-id="10d75-103">CBaseControlVideo. SetControlVideoPin, metodo</span><span class="sxs-lookup"><span data-stu-id="10d75-103">CBaseControlVideo.SetControlVideoPin method</span></span>

<span data-ttu-id="10d75-104">Il `SetControlVideoPin` metodo imposta il PIN utilizzato dal filtro.</span><span class="sxs-lookup"><span data-stu-id="10d75-104">The `SetControlVideoPin` method sets the pin used by the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d75-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10d75-105">Syntax</span></span>


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="10d75-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="10d75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d75-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="10d75-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="10d75-108">Puntatore al pin con il quale viene sincronizzata l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="10d75-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d75-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10d75-109">Return value</span></span>

<span data-ttu-id="10d75-110">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="10d75-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10d75-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="10d75-111">Remarks</span></span>

<span data-ttu-id="10d75-112">L'interfaccia può essere chiamata solo quando il filtro è stato connesso correttamente.</span><span class="sxs-lookup"><span data-stu-id="10d75-112">The interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="10d75-113">L'oggetto viene passato tramite questo metodo al pin con il quale è sincronizzato; nella maggior parte dei casi determinerà se il PIN è connesso quando dispone di un metodo di interfaccia denominato e restituirà VFW \_ e \_ non sarà connesso in caso di \_ errore.</span><span class="sxs-lookup"><span data-stu-id="10d75-113">The object is passed through this method to the pin with which it is synchronized; in most cases it will determine if the pin is connected when it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d75-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10d75-114">Requirements</span></span>



| <span data-ttu-id="10d75-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="10d75-115">Requirement</span></span> | <span data-ttu-id="10d75-116">Valore</span><span class="sxs-lookup"><span data-stu-id="10d75-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d75-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10d75-117">Header</span></span><br/>  | <dl> <span data-ttu-id="10d75-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10d75-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="10d75-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="10d75-119">Library</span></span><br/> | <dl> <span data-ttu-id="10d75-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="10d75-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10d75-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10d75-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d75-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="10d75-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




