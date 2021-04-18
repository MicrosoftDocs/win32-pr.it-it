---
description: Il \_ metodo Put FullScreenMode imposta la modalità a schermo intero del renderer.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: Metodo CBaseControlWindow.put_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328351"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a><span data-ttu-id="815fa-103">CBaseControlWindow. put \_ FullScreenMode (metodo)</span><span class="sxs-lookup"><span data-stu-id="815fa-103">CBaseControlWindow.put\_FullScreenMode method</span></span>

<span data-ttu-id="815fa-104">Il `put_FullScreenMode` metodo imposta la modalità a schermo intero del renderer.</span><span class="sxs-lookup"><span data-stu-id="815fa-104">The `put_FullScreenMode` method sets the full-screen mode of the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="815fa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="815fa-105">Syntax</span></span>


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="815fa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="815fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="815fa-107">*FullScreenMode*</span><span class="sxs-lookup"><span data-stu-id="815fa-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="815fa-108">Modalità schermo intero da applicare.</span><span class="sxs-lookup"><span data-stu-id="815fa-108">Full-screen mode to apply.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="815fa-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="815fa-109">Return value</span></span>

<span data-ttu-id="815fa-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="815fa-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="815fa-111">L'implementazione corrente restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="815fa-111">The current implementation returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="815fa-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="815fa-112">Remarks</span></span>

<span data-ttu-id="815fa-113">Un renderer video che implementa una modalità a schermo intero deve eseguire l'override di questa funzione membro e implementare qualsiasi modalità supportata.</span><span class="sxs-lookup"><span data-stu-id="815fa-113">A video renderer that implements a full-screen mode should override this member function and implement whatever modes it supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="815fa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="815fa-114">Requirements</span></span>



| <span data-ttu-id="815fa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="815fa-115">Requirement</span></span> | <span data-ttu-id="815fa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="815fa-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="815fa-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="815fa-117">Header</span></span><br/>  | <dl> <span data-ttu-id="815fa-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="815fa-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="815fa-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="815fa-119">Library</span></span><br/> | <dl> <span data-ttu-id="815fa-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="815fa-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="815fa-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="815fa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="815fa-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="815fa-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




