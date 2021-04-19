---
description: Il \_ metodo Get WindowStyleEx recupera gli stili della finestra estesa.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: Metodo CBaseControlWindow.get_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c59336ab57e92e99366494a272f2b995191b494b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332346"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a><span data-ttu-id="764d2-103">Metodo CBaseControlWindow. Get \_ WindowStyleEx</span><span class="sxs-lookup"><span data-stu-id="764d2-103">CBaseControlWindow.get\_WindowStyleEx method</span></span>

<span data-ttu-id="764d2-104">Il `get_WindowStyleEx` metodo recupera gli stili della finestra estesa.</span><span class="sxs-lookup"><span data-stu-id="764d2-104">The `get_WindowStyleEx` method retrieves the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="764d2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="764d2-105">Syntax</span></span>


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="764d2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="764d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="764d2-107">*pWindowStyleEx*</span><span class="sxs-lookup"><span data-stu-id="764d2-107">*pWindowStyleEx*</span></span> 
</dt> <dd>

<span data-ttu-id="764d2-108">Puntatore agli stili della finestra estesa.</span><span class="sxs-lookup"><span data-stu-id="764d2-108">Pointer to extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="764d2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="764d2-109">Return value</span></span>

<span data-ttu-id="764d2-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="764d2-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="764d2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="764d2-111">Remarks</span></span>

<span data-ttu-id="764d2-112">Questa funzione membro recupera gli stili della finestra estesa.</span><span class="sxs-lookup"><span data-stu-id="764d2-112">This member function retrieves the extended window styles.</span></span> <span data-ttu-id="764d2-113">Chiama la funzione membro [**CBaseControlWindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="764d2-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="764d2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="764d2-114">Requirements</span></span>



| <span data-ttu-id="764d2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="764d2-115">Requirement</span></span> | <span data-ttu-id="764d2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="764d2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="764d2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="764d2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="764d2-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="764d2-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="764d2-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="764d2-119">Library</span></span><br/> | <dl> <span data-ttu-id="764d2-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="764d2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="764d2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="764d2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="764d2-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="764d2-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




