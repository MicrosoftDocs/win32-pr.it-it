---
description: Il \_ metodo Put BackgroundPalette imposta un flag per realizzare la tavolozza in background.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: Metodo CBaseControlWindow.put_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328355"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a><span data-ttu-id="46986-103">CBaseControlWindow. put \_ BackgroundPalette (metodo)</span><span class="sxs-lookup"><span data-stu-id="46986-103">CBaseControlWindow.put\_BackgroundPalette method</span></span>

<span data-ttu-id="46986-104">Il `put_BackgroundPalette` metodo imposta un flag per realizzare la tavolozza in background.</span><span class="sxs-lookup"><span data-stu-id="46986-104">The `put_BackgroundPalette` method sets a flag to realize the palette in the background.</span></span>

## <a name="syntax"></a><span data-ttu-id="46986-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46986-105">Syntax</span></span>


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="46986-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46986-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46986-107">*BackgroundPalette*</span><span class="sxs-lookup"><span data-stu-id="46986-107">*BackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="46986-108">Flag booleano di automazione (0 è disattivato, 1 è on).</span><span class="sxs-lookup"><span data-stu-id="46986-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46986-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46986-109">Return value</span></span>

<span data-ttu-id="46986-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46986-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46986-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="46986-111">Remarks</span></span>

<span data-ttu-id="46986-112">Per riprodurre un video all'interno di un'altra applicazione o documento, l'applicazione potrebbe voler usare la propria tavolozza.</span><span class="sxs-lookup"><span data-stu-id="46986-112">To play a video within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="46986-113">È possibile che il video usi la tavolozza di primo piano corrente anziché la relativa tavolozza, impostando questo flag su 1.</span><span class="sxs-lookup"><span data-stu-id="46986-113">It can ask that the video use the current foreground palette rather than its own as the background palette by setting this flag to  1.</span></span> <span data-ttu-id="46986-114">Se questa proprietà è impostata su 0, la finestra verrà installata e si renderà conto della tavolozza preferita.</span><span class="sxs-lookup"><span data-stu-id="46986-114">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="46986-115">La richiesta di utilizzo di una tavolozza diversa provocherà gravi sanzioni in termini di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="46986-115">Asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="46986-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46986-116">Requirements</span></span>



| <span data-ttu-id="46986-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="46986-117">Requirement</span></span> | <span data-ttu-id="46986-118">Valore</span><span class="sxs-lookup"><span data-stu-id="46986-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46986-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46986-119">Header</span></span><br/>  | <dl> <span data-ttu-id="46986-120"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46986-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46986-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="46986-121">Library</span></span><br/> | <dl> <span data-ttu-id="46986-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="46986-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46986-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46986-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46986-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="46986-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




