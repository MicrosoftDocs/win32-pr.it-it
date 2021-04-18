---
description: Il metodo GetMaxIdealImageSize recupera le dimensioni massime dell'immagine ideale.
ms.assetid: 881c1c3d-7505-44a2-964d-3255e2072f6b
title: Metodo CBaseControlWindow. GetMaxIdealImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMaxIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc8ac53dd30c62f3ebb50585677f83f356b593f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328093"
---
# <a name="cbasecontrolwindowgetmaxidealimagesize-method"></a><span data-ttu-id="e727e-103">CBaseControlWindow. GetMaxIdealImageSize, metodo</span><span class="sxs-lookup"><span data-stu-id="e727e-103">CBaseControlWindow.GetMaxIdealImageSize method</span></span>

<span data-ttu-id="e727e-104">Il `GetMaxIdealImageSize` metodo recupera le dimensioni massime dell'immagine ideale.</span><span class="sxs-lookup"><span data-stu-id="e727e-104">The `GetMaxIdealImageSize` method retrieves the maximum ideal image size.</span></span>

## <a name="syntax"></a><span data-ttu-id="e727e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e727e-105">Syntax</span></span>


```C++
HRESULT GetMaxIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="e727e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e727e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e727e-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="e727e-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="e727e-108">Puntatore alla larghezza ideale massima, in pixel.</span><span class="sxs-lookup"><span data-stu-id="e727e-108">Pointer to the maximum ideal width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e727e-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="e727e-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="e727e-110">Puntatore all'altezza ideale massima, in pixel.</span><span class="sxs-lookup"><span data-stu-id="e727e-110">Pointer to the maximum ideal height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e727e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e727e-111">Return value</span></span>

<span data-ttu-id="e727e-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e727e-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e727e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e727e-113">Remarks</span></span>

<span data-ttu-id="e727e-114">Vari renderer presentano limitazioni delle prestazioni sulle dimensioni delle immagini che è possibile visualizzare.</span><span class="sxs-lookup"><span data-stu-id="e727e-114">Various renderers have performance restrictions on the size of images they can display.</span></span> <span data-ttu-id="e727e-115">Sebbene debbano ancora funzionare correttamente quando viene richiesto di visualizzare immagini di dimensioni maggiori del valore massimo specificato, i renderer possono designare le dimensioni minime e massime ideali tramite l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="e727e-115">Although they should still function properly when requested to display images larger than the specified maximum, renderers can nominate the minimum and maximum ideal sizes through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="e727e-116">Questa interfaccia può essere chiamata solo quando il grafico del filtro è in pausa o in esecuzione, perché non è fino a quel momento che le risorse vengono allocate e il renderer è in grado di riconoscere le restrizioni.</span><span class="sxs-lookup"><span data-stu-id="e727e-116">This interface can be called only when the filter graph is paused or running, because it is not until then that resources are allocated and the renderer can recognize its restrictions.</span></span> <span data-ttu-id="e727e-117">Se non esistono restrizioni, il renderer inserisce i parametri *pWidth* e *pHeight* con le dimensioni video native e restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="e727e-117">If no restrictions exist, the renderer fills in the *pWidth* and *pHeight* parameters with the native video dimensions and returns S\_FALSE.</span></span> <span data-ttu-id="e727e-118">Se esistono restrizioni, viene immesso l'altezza e la larghezza con restrizioni e la funzione membro restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e727e-118">If restrictions do exist, the restricted width and height are entered, and the member function returns S\_OK.</span></span>

<span data-ttu-id="e727e-119">Le dimensioni si applicano alle dimensioni del video di destinazione e non alle dimensioni complessive della finestra.</span><span class="sxs-lookup"><span data-stu-id="e727e-119">The dimensions apply to the size of the destination video and not to the overall window size.</span></span> <span data-ttu-id="e727e-120">Quindi, quando si calcolano le dimensioni della finestra da impostare, tenere conto degli stili correnti della finestra, ad esempio WS \_ Caption e WS \_ Border.</span><span class="sxs-lookup"><span data-stu-id="e727e-120">So, when calculating the size of the window to set, account for the current window styles (for example, WS\_CAPTION and WS\_BORDER).</span></span>

## <a name="requirements"></a><span data-ttu-id="e727e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e727e-121">Requirements</span></span>



| <span data-ttu-id="e727e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e727e-122">Requirement</span></span> | <span data-ttu-id="e727e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e727e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e727e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e727e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e727e-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e727e-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e727e-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e727e-126">Library</span></span><br/> | <dl> <span data-ttu-id="e727e-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e727e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e727e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e727e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e727e-129">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="e727e-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




