---
description: Il metodo SetWindowPosition imposta la posizione della finestra sul desktop.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Metodo CBaseControlWindow. SetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329866"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a><span data-ttu-id="ae701-103">CBaseControlWindow. SetWindowPosition, metodo</span><span class="sxs-lookup"><span data-stu-id="ae701-103">CBaseControlWindow.SetWindowPosition method</span></span>

<span data-ttu-id="ae701-104">Il `SetWindowPosition` metodo imposta la posizione della finestra sul desktop.</span><span class="sxs-lookup"><span data-stu-id="ae701-104">The `SetWindowPosition` method sets the window position on the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae701-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae701-105">Syntax</span></span>


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="ae701-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae701-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae701-107">*Sinistra*</span><span class="sxs-lookup"><span data-stu-id="ae701-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="ae701-108">Nuova coordinata sinistra.</span><span class="sxs-lookup"><span data-stu-id="ae701-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="ae701-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="ae701-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="ae701-110">Nuova coordinata superiore.</span><span class="sxs-lookup"><span data-stu-id="ae701-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="ae701-111">*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="ae701-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="ae701-112">Larghezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="ae701-112">Width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="ae701-113">*Altezza*</span><span class="sxs-lookup"><span data-stu-id="ae701-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="ae701-114">Altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="ae701-114">Height of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae701-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae701-115">Return value</span></span>

<span data-ttu-id="ae701-116">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae701-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae701-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae701-117">Requirements</span></span>



| <span data-ttu-id="ae701-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae701-118">Requirement</span></span> | <span data-ttu-id="ae701-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ae701-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae701-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae701-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ae701-121"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae701-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ae701-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="ae701-122">Library</span></span><br/> | <dl> <span data-ttu-id="ae701-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ae701-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae701-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae701-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae701-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="ae701-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




