---
description: Il metodo GetVideoSize recupera la larghezza e l'altezza del video nativo.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: Metodo CBaseControlVideo. GetVideoSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b1df6fe781f036043728050354519dfa6e28d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332082"
---
# <a name="cbasecontrolvideogetvideosize-method"></a><span data-ttu-id="92db9-103">CBaseControlVideo. GetVideoSize, metodo</span><span class="sxs-lookup"><span data-stu-id="92db9-103">CBaseControlVideo.GetVideoSize method</span></span>

<span data-ttu-id="92db9-104">Il `GetVideoSize` metodo recupera la larghezza e l'altezza del video nativo.</span><span class="sxs-lookup"><span data-stu-id="92db9-104">The `GetVideoSize` method retrieves the native video's width and height.</span></span>

## <a name="syntax"></a><span data-ttu-id="92db9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92db9-105">Syntax</span></span>


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="92db9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="92db9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92db9-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="92db9-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="92db9-108">Puntatore alla larghezza del video.</span><span class="sxs-lookup"><span data-stu-id="92db9-108">Pointer to the video width.</span></span>

</dd> <dt>

<span data-ttu-id="92db9-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="92db9-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="92db9-110">Puntatore all'altezza del video.</span><span class="sxs-lookup"><span data-stu-id="92db9-110">Pointer to the video height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92db9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92db9-111">Return value</span></span>

<span data-ttu-id="92db9-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="92db9-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="92db9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92db9-113">Requirements</span></span>



| <span data-ttu-id="92db9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="92db9-114">Requirement</span></span> | <span data-ttu-id="92db9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="92db9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92db9-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92db9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="92db9-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92db9-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="92db9-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="92db9-118">Library</span></span><br/> | <dl> <span data-ttu-id="92db9-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="92db9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92db9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92db9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92db9-121">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="92db9-121">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




