---
description: Il \_ metodo get Left recupera la coordinata corrente della finestra a sinistra.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: Metodo CBaseControlWindow.get_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04f586cede24f8ff2017ae4004fc45c584a57f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331331"
---
# <a name="cbasecontrolwindowget_left-method"></a><span data-ttu-id="ea74e-103">Metodo CBaseControlWindow. Get \_ Left</span><span class="sxs-lookup"><span data-stu-id="ea74e-103">CBaseControlWindow.get\_Left method</span></span>

<span data-ttu-id="ea74e-104">Il `get_Left` metodo recupera la coordinata corrente della finestra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="ea74e-104">The `get_Left` method retrieves the current left window coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea74e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea74e-105">Syntax</span></span>


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a><span data-ttu-id="ea74e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea74e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea74e-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="ea74e-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="ea74e-108">Puntatore alla coordinata sinistra, espressa in pixel.</span><span class="sxs-lookup"><span data-stu-id="ea74e-108">Pointer to the left coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea74e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea74e-109">Return value</span></span>

<span data-ttu-id="ea74e-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ea74e-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea74e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea74e-111">Remarks</span></span>

<span data-ttu-id="ea74e-112">La finestra è posizionata sul desktop.</span><span class="sxs-lookup"><span data-stu-id="ea74e-112">The window has a position on the desktop.</span></span> <span data-ttu-id="ea74e-113">Questa posizione è espressa in pixel da quattro coordinate, a sinistra, in alto, a destra e in basso.</span><span class="sxs-lookup"><span data-stu-id="ea74e-113">This position is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="ea74e-114">Le interfacce automatizzate da OLE generalmente esprimono questa posizione attraverso Left, top, Width e Height. si tratta della convenzione usata in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ea74e-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="ea74e-115">Tutte le coordinate sono espresse in pixel e la modifica di tutte le coordinate aggiornerà immediatamente la finestra.</span><span class="sxs-lookup"><span data-stu-id="ea74e-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="ea74e-116">L'impostazione delle coordinate di sinistra o superiore sposta la finestra verso l'alto e verso l'alto rispettivamente; Queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="ea74e-116">Setting the left or top coordinates moves the window left and up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="ea74e-117">Analogamente, l'impostazione della larghezza e dell'altezza non ha alcun effetto sulle coordinate a sinistra e in alto.</span><span class="sxs-lookup"><span data-stu-id="ea74e-117">Likewise, setting the width and height have no effect on the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea74e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea74e-118">Requirements</span></span>



| <span data-ttu-id="ea74e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea74e-119">Requirement</span></span> | <span data-ttu-id="ea74e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ea74e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea74e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea74e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ea74e-122"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea74e-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ea74e-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="ea74e-123">Library</span></span><br/> | <dl> <span data-ttu-id="ea74e-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ea74e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea74e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea74e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea74e-126">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="ea74e-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




