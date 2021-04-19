---
description: Il \_ metodo get WindowState recupera lo stato corrente della finestra.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: Metodo CBaseControlWindow.get_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332348"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a><span data-ttu-id="fd800-103">Metodo CBaseControlWindow. Get \_ WindowState</span><span class="sxs-lookup"><span data-stu-id="fd800-103">CBaseControlWindow.get\_WindowState method</span></span>

<span data-ttu-id="fd800-104">Il `get_WindowState` metodo recupera lo stato corrente della finestra.</span><span class="sxs-lookup"><span data-stu-id="fd800-104">The `get_WindowState` method retrieves the current window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd800-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd800-105">Syntax</span></span>


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a><span data-ttu-id="fd800-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd800-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd800-107">*pWindowState*</span><span class="sxs-lookup"><span data-stu-id="fd800-107">*pWindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="fd800-108">Puntatore allo stato della finestra.</span><span class="sxs-lookup"><span data-stu-id="fd800-108">Pointer to the window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd800-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd800-109">Return value</span></span>

<span data-ttu-id="fd800-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fd800-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd800-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd800-111">Remarks</span></span>

<span data-ttu-id="fd800-112">Questa funzione membro restituisce un subset dei parametri della funzione **ShowWindow** di Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="fd800-112">This member function returns a subset of the parameters of the Microsoft Win32 **ShowWindow** function.</span></span> <span data-ttu-id="fd800-113">In particolare, restituisce SW \_ Show e SW \_ Hide, a seconda della visibilità corrente della finestra.</span><span class="sxs-lookup"><span data-stu-id="fd800-113">In particular, it returns SW\_SHOW and SW\_HIDE, depending on the current visibility of the window.</span></span> <span data-ttu-id="fd800-114">Restituisce inoltre SW \_ Riduci a icona e SW \_ ingrandito, a seconda che la finestra sia un'icona o espansa.</span><span class="sxs-lookup"><span data-stu-id="fd800-114">It also returns SW\_MINIMIZE and SW\_MAXIMIZE, depending on whether the window is an icon or is expanded.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd800-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd800-115">Requirements</span></span>



| <span data-ttu-id="fd800-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd800-116">Requirement</span></span> | <span data-ttu-id="fd800-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fd800-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd800-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd800-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fd800-119"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd800-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fd800-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="fd800-120">Library</span></span><br/> | <dl> <span data-ttu-id="fd800-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fd800-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd800-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd800-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd800-123">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="fd800-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




