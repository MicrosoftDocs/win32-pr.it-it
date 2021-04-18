---
description: Il \_ metodo Put left Imposta la coordinata sinistra per la finestra.
ms.assetid: 4ba6b243-e7a7-4c41-a2c5-248b05b42f4f
title: Metodo CBaseControlWindow.put_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1dcd56bc10e60d263ce385246a6ea01aee721bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331944"
---
# <a name="cbasecontrolwindowput_left-method"></a><span data-ttu-id="5d2f8-103">Metodo Left di CBaseControlWindow. put \_</span><span class="sxs-lookup"><span data-stu-id="5d2f8-103">CBaseControlWindow.put\_Left method</span></span>

<span data-ttu-id="5d2f8-104">Il `put_Left` metodo imposta la coordinata sinistra per la finestra.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-104">The `put_Left` method sets the left coordinate for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d2f8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d2f8-105">Syntax</span></span>


```C++
HRESULT put_Left(
   long Left
);
```



## <a name="parameters"></a><span data-ttu-id="5d2f8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d2f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d2f8-107">*Sinistra*</span><span class="sxs-lookup"><span data-stu-id="5d2f8-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="5d2f8-108">Nuova coordinata sinistra, espressa in pixel.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-108">New left coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d2f8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d2f8-109">Return value</span></span>

<span data-ttu-id="5d2f8-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d2f8-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d2f8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d2f8-111">Remarks</span></span>

<span data-ttu-id="5d2f8-112">La finestra è posizionata sul desktop.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-112">The window has a position on the desktop.</span></span> <span data-ttu-id="5d2f8-113">Questo è espresso in pixel da quattro coordinate, a sinistra, in alto, a destra e in basso.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="5d2f8-114">Le interfacce automatizzate da OLE generalmente esprimono questa posizione attraverso Left, top, Width e Height. si tratta della convenzione usata in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="5d2f8-115">Tutte le coordinate sono espresse in pixel e la modifica di tutte le coordinate aggiornerà immediatamente la finestra.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="5d2f8-116">L'impostazione delle coordinate di sinistra o superiore sposta la finestra verso sinistra o verso l'alto rispettivamente; Queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="5d2f8-117">Analogamente, l'impostazione della larghezza e dell'altezza non influisce sulle coordinate di sinistra e di primo livello.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2f8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d2f8-118">Requirements</span></span>



| <span data-ttu-id="5d2f8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d2f8-119">Requirement</span></span> | <span data-ttu-id="5d2f8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5d2f8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2f8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d2f8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5d2f8-122"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f8-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5d2f8-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="5d2f8-123">Library</span></span><br/> | <dl> <span data-ttu-id="5d2f8-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d2f8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d2f8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2f8-126">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="5d2f8-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




