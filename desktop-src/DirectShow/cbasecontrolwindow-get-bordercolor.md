---
description: Il \_ metodo Get BorderColor Recupera il colore del bordo corrente.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: Metodo CBaseControlWindow.get_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325386"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a><span data-ttu-id="3e0b9-103">Metodo CBaseControlWindow. Get \_ BorderColor</span><span class="sxs-lookup"><span data-stu-id="3e0b9-103">CBaseControlWindow.get\_BorderColor method</span></span>

<span data-ttu-id="3e0b9-104">Il `get_BorderColor` metodo recupera il colore del bordo corrente.</span><span class="sxs-lookup"><span data-stu-id="3e0b9-104">The `get_BorderColor` method retrieves the current border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e0b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e0b9-105">Syntax</span></span>


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a><span data-ttu-id="3e0b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e0b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e0b9-107">*Colore*</span><span class="sxs-lookup"><span data-stu-id="3e0b9-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="3e0b9-108">Puntatore al colore del bordo corrente.</span><span class="sxs-lookup"><span data-stu-id="3e0b9-108">Pointer to the current border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e0b9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e0b9-109">Return value</span></span>

<span data-ttu-id="3e0b9-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3e0b9-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e0b9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e0b9-111">Remarks</span></span>

<span data-ttu-id="3e0b9-112">Un'applicazione può impostare un rettangolo di destinazione in cui deve essere visualizzato il video.</span><span class="sxs-lookup"><span data-stu-id="3e0b9-112">An application can set a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="3e0b9-113">Questo rettangolo è relativo all'area client per la finestra.</span><span class="sxs-lookup"><span data-stu-id="3e0b9-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="3e0b9-114">Se questa operazione viene eseguita (l'impostazione predefinita consiste nel disegnare sempre l'intera finestra), è presente un bordo che circonda il video.</span><span class="sxs-lookup"><span data-stu-id="3e0b9-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="3e0b9-115">Questa proprietà influiscono sul colore utilizzato dal bordo.</span><span class="sxs-lookup"><span data-stu-id="3e0b9-115">This property affects the color used by the border.</span></span> <span data-ttu-id="3e0b9-116">Anche se il parametro viene specificato come tipo **Long** , si tratta in realtà di un valore **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="3e0b9-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

<span data-ttu-id="3e0b9-117">Questa funzione membro deve essere chiamata da oggetti esterni tramite l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e pertanto blocca la sezione critica per la sincronizzazione con il filtro associato.</span><span class="sxs-lookup"><span data-stu-id="3e0b9-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="3e0b9-118">Chiamare la funzione membro [**CBaseControlWindow:: GetBorderColour**](cbasecontrolwindow-getbordercolour.md) per recuperare questa proprietà se non viene chiamata da un oggetto esterno.</span><span class="sxs-lookup"><span data-stu-id="3e0b9-118">Call the [**CBaseControlWindow::GetBorderColour**](cbasecontrolwindow-getbordercolour.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e0b9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e0b9-119">Requirements</span></span>



| <span data-ttu-id="3e0b9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e0b9-120">Requirement</span></span> | <span data-ttu-id="3e0b9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3e0b9-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e0b9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e0b9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3e0b9-123"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e0b9-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e0b9-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e0b9-124">Library</span></span><br/> | <dl> <span data-ttu-id="3e0b9-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3e0b9-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e0b9-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e0b9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e0b9-127">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="3e0b9-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




