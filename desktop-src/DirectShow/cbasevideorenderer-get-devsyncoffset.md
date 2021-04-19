---
description: Il \_ metodo Get DevSyncOffset recupera la deviazione standard del tempo in millisecondi tra il momento in cui ogni frame era dovuto e il rendering effettivamente eseguito, per tutti i frame dall'avvio dello streaming.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: Metodo CBaseVideoRenderer.get_DevSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326424"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a><span data-ttu-id="6f6bb-103">Metodo CBaseVideoRenderer. Get \_ DevSyncOffset</span><span class="sxs-lookup"><span data-stu-id="6f6bb-103">CBaseVideoRenderer.get\_DevSyncOffset method</span></span>

<span data-ttu-id="6f6bb-104">Il `get_DevSyncOffset` metodo recupera la deviazione standard dell'intervallo di tempo in millisecondi tra il momento in cui ogni frame è dovuto e il momento in cui è stato eseguito il rendering, per tutti i frame dall'avvio del flusso.</span><span class="sxs-lookup"><span data-stu-id="6f6bb-104">The `get_DevSyncOffset` method retrieves the standard deviation of the time in milliseconds between when each frame was due and when it was actually rendered, for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f6bb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f6bb-105">Syntax</span></span>


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a><span data-ttu-id="6f6bb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f6bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f6bb-107">*piDev*</span><span class="sxs-lookup"><span data-stu-id="6f6bb-107">*piDev*</span></span> 
</dt> <dd>

<span data-ttu-id="6f6bb-108">Puntatore alla deviazione standard dell'ora descritta in precedenza.</span><span class="sxs-lookup"><span data-stu-id="6f6bb-108">Pointer to the standard deviation of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f6bb-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f6bb-109">Return value</span></span>

<span data-ttu-id="6f6bb-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f6bb-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f6bb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f6bb-111">Remarks</span></span>

<span data-ttu-id="6f6bb-112">Questa funzione membro implementa il metodo [**IQualProp:: Get \_ DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) .</span><span class="sxs-lookup"><span data-stu-id="6f6bb-112">This member function implements the [**IQualProp::get\_DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f6bb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f6bb-113">Requirements</span></span>



| <span data-ttu-id="6f6bb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f6bb-114">Requirement</span></span> | <span data-ttu-id="6f6bb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6f6bb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f6bb-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f6bb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6f6bb-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f6bb-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6f6bb-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="6f6bb-118">Library</span></span><br/> | <dl> <span data-ttu-id="6f6bb-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6f6bb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f6bb-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f6bb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f6bb-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="6f6bb-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




