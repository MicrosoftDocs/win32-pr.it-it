---
description: Il \_ metodo Get WindowStyle recupera gli stili della finestra standard.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: Metodo CBaseControlWindow.get_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91e04efac3a67c262b4eeb85948f846dbb06086a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332347"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a><span data-ttu-id="1e2b2-103">Metodo CBaseControlWindow. Get \_ WindowStyle</span><span class="sxs-lookup"><span data-stu-id="1e2b2-103">CBaseControlWindow.get\_WindowStyle method</span></span>

<span data-ttu-id="1e2b2-104">Il `get_WindowStyle` metodo recupera gli stili della finestra standard.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-104">The `get_WindowStyle` method retrieves the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e2b2-105">Syntax</span></span>


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="1e2b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e2b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e2b2-107">*pWindowStyle*</span><span class="sxs-lookup"><span data-stu-id="1e2b2-107">*pWindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="1e2b2-108">Puntatore agli stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-108">Pointer to window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e2b2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e2b2-109">Return value</span></span>

<span data-ttu-id="1e2b2-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e2b2-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e2b2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e2b2-111">Remarks</span></span>

<span data-ttu-id="1e2b2-112">Questa funzione membro restituisce gli stili standard della finestra, ad esempio WS \_ child e WS \_ Visible.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-112">This member function returns the standard window styles, such as WS\_CHILD and WS\_VISIBLE.</span></span> <span data-ttu-id="1e2b2-113">Chiama la funzione membro [**CBaseControlWindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="1e2b2-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e2b2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e2b2-114">Requirements</span></span>



| <span data-ttu-id="1e2b2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e2b2-115">Requirement</span></span> | <span data-ttu-id="1e2b2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1e2b2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2b2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e2b2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1e2b2-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e2b2-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1e2b2-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="1e2b2-119">Library</span></span><br/> | <dl> <span data-ttu-id="1e2b2-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1e2b2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e2b2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e2b2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e2b2-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="1e2b2-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




