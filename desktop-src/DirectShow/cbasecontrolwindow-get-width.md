---
description: Il \_ metodo get Width recupera la larghezza corrente della finestra.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: Metodo CBaseControlWindow.get_Width (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56e863b8add52e1b98714e13466a48e3d0d52bba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332349"
---
# <a name="cbasecontrolwindowget_width-method"></a><span data-ttu-id="5713c-103">Metodo CBaseControlWindow. Get \_ Width</span><span class="sxs-lookup"><span data-stu-id="5713c-103">CBaseControlWindow.get\_Width method</span></span>

<span data-ttu-id="5713c-104">Il `get_Width` metodo recupera la larghezza corrente della finestra.</span><span class="sxs-lookup"><span data-stu-id="5713c-104">The `get_Width` method retrieves the current window width.</span></span>

## <a name="syntax"></a><span data-ttu-id="5713c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5713c-105">Syntax</span></span>


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a><span data-ttu-id="5713c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5713c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5713c-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="5713c-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="5713c-108">Puntatore alla larghezza della finestra, in pixel.</span><span class="sxs-lookup"><span data-stu-id="5713c-108">Pointer to the window width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5713c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5713c-109">Return value</span></span>

<span data-ttu-id="5713c-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5713c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5713c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5713c-111">Remarks</span></span>

<span data-ttu-id="5713c-112">La finestra è posizionata sul desktop.</span><span class="sxs-lookup"><span data-stu-id="5713c-112">The window has a position on the desktop.</span></span> <span data-ttu-id="5713c-113">Questo è espresso in pixel da quattro coordinate, a sinistra, in alto, a destra e in basso.</span><span class="sxs-lookup"><span data-stu-id="5713c-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="5713c-114">Le interfacce automatizzate da OLE generalmente esprimono questa posizione attraverso Left, top, Width e Height. si tratta della convenzione usata in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5713c-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="5713c-115">Tutte le coordinate sono espresse in pixel e la modifica di tutte le coordinate aggiornerà immediatamente la finestra.</span><span class="sxs-lookup"><span data-stu-id="5713c-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="5713c-116">L'impostazione delle coordinate di sinistra o superiore sposta la finestra verso sinistra o verso l'alto rispettivamente; Queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="5713c-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="5713c-117">Analogamente, l'impostazione della larghezza e dell'altezza non influisce sulle coordinate di sinistra e di primo livello.</span><span class="sxs-lookup"><span data-stu-id="5713c-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="5713c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5713c-118">Requirements</span></span>



| <span data-ttu-id="5713c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5713c-119">Requirement</span></span> | <span data-ttu-id="5713c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5713c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5713c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5713c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5713c-122"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5713c-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5713c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="5713c-123">Library</span></span><br/> | <dl> <span data-ttu-id="5713c-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5713c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5713c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5713c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5713c-126">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="5713c-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




