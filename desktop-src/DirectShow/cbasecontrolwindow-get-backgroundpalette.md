---
description: Il \_ metodo Get BackgroundPalette recupera la tavolozza realizzata nel flag di sfondo.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: Metodo CBaseControlWindow.get_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325394"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a><span data-ttu-id="7d4b1-103">Metodo CBaseControlWindow. Get \_ BackgroundPalette</span><span class="sxs-lookup"><span data-stu-id="7d4b1-103">CBaseControlWindow.get\_BackgroundPalette method</span></span>

<span data-ttu-id="7d4b1-104">Il `get_BackgroundPalette` metodo recupera la tavolozza realizzata nel flag di sfondo.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-104">The `get_BackgroundPalette` method retrieves the realized palette in the background flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d4b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d4b1-105">Syntax</span></span>


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="7d4b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d4b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d4b1-107">*pBackgroundPalette*</span><span class="sxs-lookup"><span data-stu-id="7d4b1-107">*pBackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="7d4b1-108">Puntatore a un flag booleano di automazione (0 è disattivato, 1 è on).</span><span class="sxs-lookup"><span data-stu-id="7d4b1-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d4b1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d4b1-109">Return value</span></span>

<span data-ttu-id="7d4b1-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7d4b1-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d4b1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d4b1-111">Remarks</span></span>

<span data-ttu-id="7d4b1-112">Questa funzione membro implementa il metodo [**IVideoWindow:: Get \_ BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) .</span><span class="sxs-lookup"><span data-stu-id="7d4b1-112">This member function implements the [**IVideoWindow::get\_BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) method.</span></span> <span data-ttu-id="7d4b1-113">Se un video viene riprodotto all'interno di un'altra applicazione o documento, l'applicazione potrebbe voler usare la propria tavolozza.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-113">If a video will be played within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="7d4b1-114">È possibile che il video usi la tavolozza di primo piano corrente anziché la propria impostando questo flag su 1.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-114">It can ask that the video use the current foreground palette rather than its own by setting this flag to  1.</span></span> <span data-ttu-id="7d4b1-115">Se questa proprietà è impostata su 0, la finestra verrà installata e si renderà conto della tavolozza preferita.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-115">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="7d4b1-116">Si noti che la richiesta della finestra di utilizzare una tavolozza diversa provocherà gravi sanzioni in termini di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-116">Note that asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d4b1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d4b1-117">Requirements</span></span>



| <span data-ttu-id="7d4b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d4b1-118">Requirement</span></span> | <span data-ttu-id="7d4b1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7d4b1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d4b1-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d4b1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7d4b1-121"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d4b1-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7d4b1-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="7d4b1-122">Library</span></span><br/> | <dl> <span data-ttu-id="7d4b1-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7d4b1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d4b1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d4b1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d4b1-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="7d4b1-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




