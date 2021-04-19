---
description: Il \_ metodo Put WindowState imposta lo stato della finestra.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: Metodo CBaseControlWindow.put_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333369"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a><span data-ttu-id="4b9e3-103">CBaseControlWindow. put \_ WindowState (metodo)</span><span class="sxs-lookup"><span data-stu-id="4b9e3-103">CBaseControlWindow.put\_WindowState method</span></span>

<span data-ttu-id="4b9e3-104">Il `put_WindowState` metodo imposta lo stato della finestra.</span><span class="sxs-lookup"><span data-stu-id="4b9e3-104">The `put_WindowState` method sets the window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b9e3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b9e3-105">Syntax</span></span>


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a><span data-ttu-id="4b9e3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b9e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b9e3-107">*WindowState*</span><span class="sxs-lookup"><span data-stu-id="4b9e3-107">*WindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9e3-108">Nuovo stato della finestra.</span><span class="sxs-lookup"><span data-stu-id="4b9e3-108">New window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b9e3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b9e3-109">Return value</span></span>

<span data-ttu-id="4b9e3-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b9e3-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b9e3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b9e3-111">Remarks</span></span>

<span data-ttu-id="4b9e3-112">Questa funzione membro accetta gli stessi parametri della funzione **ShowWindow** di Microsoft Win32 (ad esempio, WS \_ SHOWNORMAL, WS \_ SHOWMINNOACTIVATE e WS \_ SHOWMAXIMIZED).</span><span class="sxs-lookup"><span data-stu-id="4b9e3-112">This member function takes the same parameters as the Microsoft Win32 **ShowWindow** function (for example, WS\_SHOWNORMAL, WS\_SHOWMINNOACTIVATE, and WS\_SHOWMAXIMIZED).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b9e3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b9e3-113">Requirements</span></span>



| <span data-ttu-id="4b9e3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b9e3-114">Requirement</span></span> | <span data-ttu-id="4b9e3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4b9e3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9e3-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b9e3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4b9e3-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b9e3-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4b9e3-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="4b9e3-118">Library</span></span><br/> | <dl> <span data-ttu-id="4b9e3-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4b9e3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b9e3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b9e3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b9e3-121">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="4b9e3-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




