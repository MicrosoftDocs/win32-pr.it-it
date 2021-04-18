---
description: Il metodo GetBorderColour Recupera il colore del bordo della finestra corrente, m \_ BorderColour.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Metodo CBaseControlWindow. GetBorderColour (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329267"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a><span data-ttu-id="3ccaa-103">CBaseControlWindow. GetBorderColour, metodo</span><span class="sxs-lookup"><span data-stu-id="3ccaa-103">CBaseControlWindow.GetBorderColour method</span></span>

<span data-ttu-id="3ccaa-104">Il `GetBorderColour` metodo recupera il colore del bordo della finestra corrente, **m \_ BorderColour**.</span><span class="sxs-lookup"><span data-stu-id="3ccaa-104">The `GetBorderColour` method retrieves the current window border color, **m\_BorderColour**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ccaa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ccaa-105">Syntax</span></span>


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a><span data-ttu-id="3ccaa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ccaa-106">Parameters</span></span>

<span data-ttu-id="3ccaa-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3ccaa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ccaa-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ccaa-108">Return value</span></span>

<span data-ttu-id="3ccaa-109">Restituisce il colore del bordo.</span><span class="sxs-lookup"><span data-stu-id="3ccaa-109">Returns the color of the border.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ccaa-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ccaa-110">Remarks</span></span>

<span data-ttu-id="3ccaa-111">Un'applicazione può impostare un rettangolo di destinazione per visualizzare il video.</span><span class="sxs-lookup"><span data-stu-id="3ccaa-111">An application can set a destination rectangle to display the video.</span></span> <span data-ttu-id="3ccaa-112">Questo rettangolo deve essere relativo all'area client per la finestra.</span><span class="sxs-lookup"><span data-stu-id="3ccaa-112">This rectangle should be relative to the client area for the window.</span></span> <span data-ttu-id="3ccaa-113">Se questa operazione viene eseguita (l'impostazione predefinita consiste nel disegnare sempre l'intera finestra), esiste un'area che racchiude il video; ovvero il bordo.</span><span class="sxs-lookup"><span data-stu-id="3ccaa-113">If this is done (the default is to always paint the entire window), there is an area that surrounds the video; that is, the border.</span></span> <span data-ttu-id="3ccaa-114">Il colore del bordo può essere impostato tramite la funzione membro [**CBaseControlWindow::p UT \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) .</span><span class="sxs-lookup"><span data-stu-id="3ccaa-114">The border color can be set through the [**CBaseControlWindow::put\_BorderColor**](cbasecontrolwindow-put-bordercolor.md) member function.</span></span> <span data-ttu-id="3ccaa-115">Questa proprietà influiscono sul colore del bordo.</span><span class="sxs-lookup"><span data-stu-id="3ccaa-115">This property affects the color of the border.</span></span> <span data-ttu-id="3ccaa-116">Usare questa funzione membro anziché [**CBaseControlWindow:: Get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), a meno che non si chiami esternamente tramite il metodo [**IVideoWindow:: Get \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) .</span><span class="sxs-lookup"><span data-stu-id="3ccaa-116">Use this member function instead of [**CBaseControlWindow::get\_BorderColor**](cbasecontrolwindow-get-bordercolor.md), unless you are calling this externally through the [**IVideoWindow::get\_BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ccaa-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ccaa-117">Requirements</span></span>



| <span data-ttu-id="3ccaa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ccaa-118">Requirement</span></span> | <span data-ttu-id="3ccaa-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3ccaa-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ccaa-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ccaa-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3ccaa-121"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ccaa-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3ccaa-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="3ccaa-122">Library</span></span><br/> | <dl> <span data-ttu-id="3ccaa-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3ccaa-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ccaa-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ccaa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ccaa-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="3ccaa-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




