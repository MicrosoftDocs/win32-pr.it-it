---
description: Il \_ metodo Get AvgSyncOffset recupera la media del tempo in millisecondi tra la scadenza di ogni frame e il rendering effettivo per tutti i frame dall'avvio del flusso.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: Metodo CBaseVideoRenderer.get_AvgSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326425"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a><span data-ttu-id="474f7-103">Metodo CBaseVideoRenderer. Get \_ AvgSyncOffset</span><span class="sxs-lookup"><span data-stu-id="474f7-103">CBaseVideoRenderer.get\_AvgSyncOffset method</span></span>

<span data-ttu-id="474f7-104">Il `get_AvgSyncOffset` metodo recupera la media del tempo in millisecondi tra la scadenza di ogni frame e il rendering effettivo per tutti i frame dall'avvio del flusso.</span><span class="sxs-lookup"><span data-stu-id="474f7-104">The `get_AvgSyncOffset` method retrieves the average of the time in milliseconds between when each frame was due and when it was actually rendered for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="474f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="474f7-105">Syntax</span></span>


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a><span data-ttu-id="474f7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="474f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="474f7-107">*piAvg*</span><span class="sxs-lookup"><span data-stu-id="474f7-107">*piAvg*</span></span> 
</dt> <dd>

<span data-ttu-id="474f7-108">Puntatore alla media del tempo descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="474f7-108">Pointer to the average of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="474f7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="474f7-109">Return value</span></span>

<span data-ttu-id="474f7-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="474f7-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="474f7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="474f7-111">Remarks</span></span>

<span data-ttu-id="474f7-112">Questa funzione membro implementa il metodo [**IQualProp:: Get \_ AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .</span><span class="sxs-lookup"><span data-stu-id="474f7-112">This member function implements the [**IQualProp::get\_AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="474f7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="474f7-113">Requirements</span></span>



| <span data-ttu-id="474f7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="474f7-114">Requirement</span></span> | <span data-ttu-id="474f7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="474f7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="474f7-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="474f7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="474f7-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="474f7-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="474f7-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="474f7-118">Library</span></span><br/> | <dl> <span data-ttu-id="474f7-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="474f7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="474f7-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="474f7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="474f7-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="474f7-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




