---
description: Il metodo GetStdDev stima la deviazione standard in millisecondi tra il momento in cui ogni frame è dovuto e quando viene effettivamente eseguito il rendering, per le statistiche per fotogramma.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Metodo CBaseVideoRenderer. GetStdDev (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326413"
---
# <a name="cbasevideorenderergetstddev-method"></a><span data-ttu-id="a9b64-103">CBaseVideoRenderer. GetStdDev, metodo</span><span class="sxs-lookup"><span data-stu-id="a9b64-103">CBaseVideoRenderer.GetStdDev method</span></span>

<span data-ttu-id="a9b64-104">Il `GetStdDev` Metodo stima la deviazione standard in millisecondi tra il momento in cui ogni frame è dovuto e quando viene effettivamente eseguito il rendering, per le statistiche per fotogramma.</span><span class="sxs-lookup"><span data-stu-id="a9b64-104">The `GetStdDev` method estimates the standard deviation in milliseconds between when each frame is due and when it is actually rendered, for per-frame statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9b64-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9b64-105">Syntax</span></span>


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a><span data-ttu-id="a9b64-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9b64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9b64-107">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="a9b64-107">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b64-108">Valore intero che contiene il numero di campioni video ricevuti dal renderer video.</span><span class="sxs-lookup"><span data-stu-id="a9b64-108">Integer value that contains the number of video samples received by the video renderer.</span></span>

</dd> <dt>

<span data-ttu-id="a9b64-109">*piResult*</span><span class="sxs-lookup"><span data-stu-id="a9b64-109">*piResult*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b64-110">Puntatore a un valore integer che conterrà la deviazione standard.</span><span class="sxs-lookup"><span data-stu-id="a9b64-110">Pointer to an integer value that will contain the standard deviation.</span></span>

</dd> <dt>

<span data-ttu-id="a9b64-111">*llSumSq*</span><span class="sxs-lookup"><span data-stu-id="a9b64-111">*llSumSq*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b64-112">Valore che rappresenta la deviazione standard, in millisecondi, di tutti gli esempi video sottoposti a rendering.</span><span class="sxs-lookup"><span data-stu-id="a9b64-112">Value that represents the standard deviation, in milliseconds, of all rendered video samples.</span></span> <span data-ttu-id="a9b64-113">Più basso è il valore, più è coerente il rendering.</span><span class="sxs-lookup"><span data-stu-id="a9b64-113">The lower the value, the more consistent the rendering.</span></span>

</dd> <dt>

<span data-ttu-id="a9b64-114">*iTot*</span><span class="sxs-lookup"><span data-stu-id="a9b64-114">*iTot*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b64-115">Valore che rappresenta il valore medio, in millisecondi, tra l'ora timbrata e il tempo di rendering per tutti gli esempi video sottoposti a rendering.</span><span class="sxs-lookup"><span data-stu-id="a9b64-115">Value that represents the mean value, in milliseconds, between the stamped time and rendered time for all rendered video samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9b64-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9b64-116">Return value</span></span>

<span data-ttu-id="a9b64-117">Restituisce NOERROR.</span><span class="sxs-lookup"><span data-stu-id="a9b64-117">Returns NOERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b64-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9b64-118">Requirements</span></span>



| <span data-ttu-id="a9b64-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9b64-119">Requirement</span></span> | <span data-ttu-id="a9b64-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a9b64-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b64-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9b64-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a9b64-122"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9b64-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a9b64-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9b64-123">Library</span></span><br/> | <dl> <span data-ttu-id="a9b64-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a9b64-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9b64-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9b64-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9b64-126">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="a9b64-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




