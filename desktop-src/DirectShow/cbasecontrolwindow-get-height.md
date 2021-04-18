---
description: Il \_ metodo Get Height recupera l'altezza della finestra corrente.
ms.assetid: 841c7d5d-f633-41fb-9cde-6126cd1cab9b
title: Metodo CBaseControlWindow.get_Height (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bed7beaac064ce9d97b9c93264eab8d56b27c9df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327124"
---
# <a name="cbasecontrolwindowget_height-method"></a><span data-ttu-id="da7da-103">Metodo CBaseControlWindow. Get \_ Height</span><span class="sxs-lookup"><span data-stu-id="da7da-103">CBaseControlWindow.get\_Height method</span></span>

<span data-ttu-id="da7da-104">Il `get_Height` metodo recupera l'altezza della finestra corrente.</span><span class="sxs-lookup"><span data-stu-id="da7da-104">The `get_Height` method retrieves the current window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="da7da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da7da-105">Syntax</span></span>


```C++
HRESULT get_Height(
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="da7da-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da7da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da7da-107">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="da7da-107">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="da7da-108">Puntatore all'altezza corrente della finestra, in pixel.</span><span class="sxs-lookup"><span data-stu-id="da7da-108">Pointer to the current window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da7da-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da7da-109">Return value</span></span>

<span data-ttu-id="da7da-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="da7da-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="da7da-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="da7da-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da7da-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="da7da-112">Remarks</span></span>

<span data-ttu-id="da7da-113">La finestra è posizionata sul desktop.</span><span class="sxs-lookup"><span data-stu-id="da7da-113">The window has a position on the desktop.</span></span> <span data-ttu-id="da7da-114">Questo è espresso in pixel da quattro coordinate, a sinistra, in alto, a destra e in basso.</span><span class="sxs-lookup"><span data-stu-id="da7da-114">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="da7da-115">Le interfacce automatizzate da OLE generalmente esprimono questa posizione attraverso Left, top, Width e Height. si tratta della convenzione usata in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="da7da-115">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="da7da-116">Tutte le coordinate sono espresse in pixel e la modifica di tutte le coordinate aggiornerà immediatamente la finestra.</span><span class="sxs-lookup"><span data-stu-id="da7da-116">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="da7da-117">L'impostazione delle coordinate di sinistra o superiore sposta la finestra verso sinistra o verso l'alto rispettivamente; Queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="da7da-117">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="da7da-118">Analogamente, l'impostazione della larghezza e dell'altezza non influisce sulle coordinate di sinistra e di primo livello.</span><span class="sxs-lookup"><span data-stu-id="da7da-118">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="da7da-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da7da-119">Requirements</span></span>



| <span data-ttu-id="da7da-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="da7da-120">Requirement</span></span> | <span data-ttu-id="da7da-121">Valore</span><span class="sxs-lookup"><span data-stu-id="da7da-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da7da-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da7da-122">Header</span></span><br/>  | <dl> <span data-ttu-id="da7da-123"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da7da-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="da7da-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="da7da-124">Library</span></span><br/> | <dl> <span data-ttu-id="da7da-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="da7da-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da7da-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da7da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da7da-127">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="da7da-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




