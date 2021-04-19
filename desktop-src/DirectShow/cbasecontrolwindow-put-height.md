---
description: Il \_ metodo Put height Imposta l'altezza della finestra.
ms.assetid: 11026ee5-e83a-4d82-9069-a302d55a2d46
title: Metodo CBaseControlWindow.put_Height (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798719c60b830caebee348032abce3e39a742e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331945"
---
# <a name="cbasecontrolwindowput_height-method"></a><span data-ttu-id="10c23-103">CBaseControlWindow. Put, \_ Metodo Height</span><span class="sxs-lookup"><span data-stu-id="10c23-103">CBaseControlWindow.put\_Height method</span></span>

<span data-ttu-id="10c23-104">Il `put_Height` metodo imposta l'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="10c23-104">The `put_Height` method sets the window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c23-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10c23-105">Syntax</span></span>


```C++
HRESULT put_Height(
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="10c23-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="10c23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10c23-107">*Altezza*</span><span class="sxs-lookup"><span data-stu-id="10c23-107">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="10c23-108">Nuova altezza della finestra, in pixel.</span><span class="sxs-lookup"><span data-stu-id="10c23-108">New window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10c23-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10c23-109">Return value</span></span>

<span data-ttu-id="10c23-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="10c23-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10c23-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="10c23-111">Remarks</span></span>

<span data-ttu-id="10c23-112">La finestra è posizionata sul desktop.</span><span class="sxs-lookup"><span data-stu-id="10c23-112">The window has a position on the desktop.</span></span> <span data-ttu-id="10c23-113">Questo è espresso in pixel da quattro coordinate, a sinistra, in alto, a destra e in basso.</span><span class="sxs-lookup"><span data-stu-id="10c23-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="10c23-114">Le interfacce automatizzate da OLE generalmente esprimono questa posizione attraverso Left, top, Width e Height. si tratta della convenzione usata in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="10c23-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="10c23-115">Tutte le coordinate sono espresse in pixel e la modifica di tutte le coordinate aggiornerà immediatamente la finestra.</span><span class="sxs-lookup"><span data-stu-id="10c23-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="10c23-116">L'impostazione delle coordinate di sinistra o superiore sposta la finestra verso sinistra o verso l'alto rispettivamente; Queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="10c23-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="10c23-117">Analogamente, l'impostazione della larghezza e dell'altezza non influisce sulle coordinate di sinistra e di primo livello.</span><span class="sxs-lookup"><span data-stu-id="10c23-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="10c23-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10c23-118">Requirements</span></span>



| <span data-ttu-id="10c23-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="10c23-119">Requirement</span></span> | <span data-ttu-id="10c23-120">Valore</span><span class="sxs-lookup"><span data-stu-id="10c23-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10c23-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10c23-121">Header</span></span><br/>  | <dl> <span data-ttu-id="10c23-122"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10c23-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="10c23-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="10c23-123">Library</span></span><br/> | <dl> <span data-ttu-id="10c23-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="10c23-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10c23-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10c23-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c23-126">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="10c23-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




