---
description: Il Metodo GetOwnerWindow recupera l'handle della finestra proprietaria, m \_ hwndOwner.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Metodo CBaseControlWindow. GetOwnerWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328090"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a><span data-ttu-id="318b2-103">CBaseControlWindow. GetOwnerWindow, metodo</span><span class="sxs-lookup"><span data-stu-id="318b2-103">CBaseControlWindow.GetOwnerWindow method</span></span>

<span data-ttu-id="318b2-104">Il `GetOwnerWindow` metodo recupera l'handle della finestra proprietaria, **m \_ hwndOwner**.</span><span class="sxs-lookup"><span data-stu-id="318b2-104">The `GetOwnerWindow` method retrieves the owning window handle, **m\_hwndOwner**.</span></span>

## <a name="syntax"></a><span data-ttu-id="318b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="318b2-105">Syntax</span></span>


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a><span data-ttu-id="318b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="318b2-106">Parameters</span></span>

<span data-ttu-id="318b2-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="318b2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="318b2-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="318b2-108">Return value</span></span>

<span data-ttu-id="318b2-109">Restituisce la finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="318b2-109">Returns the owner window.</span></span>

## <a name="remarks"></a><span data-ttu-id="318b2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="318b2-110">Remarks</span></span>

<span data-ttu-id="318b2-111">Recupera la finestra proprietaria senza chiamare il metodo di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="318b2-111">Retrieves the owning window without calling the interface method.</span></span> <span data-ttu-id="318b2-112">Usare questa funzione membro invece di [**CBaseControlWindow:: Get \_ owner**](cbasecontrolwindow-get-owner.md), a meno che non si chiami esternamente tramite il metodo [**IVideoWindow:: Get \_ owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) .</span><span class="sxs-lookup"><span data-stu-id="318b2-112">Use this member function instead of [**CBaseControlWindow::get\_Owner**](cbasecontrolwindow-get-owner.md), unless you are calling this externally through the [**IVideoWindow::get\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="318b2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="318b2-113">Requirements</span></span>



| <span data-ttu-id="318b2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="318b2-114">Requirement</span></span> | <span data-ttu-id="318b2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="318b2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="318b2-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="318b2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="318b2-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="318b2-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="318b2-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="318b2-118">Library</span></span><br/> | <dl> <span data-ttu-id="318b2-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="318b2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="318b2-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="318b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="318b2-121">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="318b2-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




