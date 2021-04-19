---
description: Il \_ metodo Put Visible consente di visualizzare o nascondere la finestra.
ms.assetid: 77e8d071-f876-4e35-945c-d1daf96ad02b
title: Metodo CBaseControlWindow.put_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf713b4ccb9932b1201e7ced40fddcd87407ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333372"
---
# <a name="cbasecontrolwindowput_visible-method"></a><span data-ttu-id="a7c2c-103">CBaseControlWindow. Put ( \_ metodo visibile)</span><span class="sxs-lookup"><span data-stu-id="a7c2c-103">CBaseControlWindow.put\_Visible method</span></span>

<span data-ttu-id="a7c2c-104">Il `put_Visible` metodo consente di visualizzare o nascondere la finestra.</span><span class="sxs-lookup"><span data-stu-id="a7c2c-104">The `put_Visible` method makes shows or hides the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c2c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7c2c-105">Syntax</span></span>


```C++
HRESULT put_Visible(
   long Visible
);
```



## <a name="parameters"></a><span data-ttu-id="a7c2c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7c2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7c2c-107">*Visible*</span><span class="sxs-lookup"><span data-stu-id="a7c2c-107">*Visible*</span></span> 
</dt> <dd>

<span data-ttu-id="a7c2c-108">Flag booleano di automazione (0 indica che la finestra è nascosta, 1 indica che la finestra è visualizzata).</span><span class="sxs-lookup"><span data-stu-id="a7c2c-108">Automation Boolean flag (0 means window is hidden,  1 means window is shown).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7c2c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7c2c-109">Return value</span></span>

<span data-ttu-id="a7c2c-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7c2c-110">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7c2c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7c2c-111">Requirements</span></span>



| <span data-ttu-id="a7c2c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7c2c-112">Requirement</span></span> | <span data-ttu-id="a7c2c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a7c2c-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c2c-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7c2c-114">Header</span></span><br/>  | <dl> <span data-ttu-id="a7c2c-115"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7c2c-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7c2c-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="a7c2c-116">Library</span></span><br/> | <dl> <span data-ttu-id="a7c2c-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a7c2c-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7c2c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7c2c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7c2c-119">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="a7c2c-119">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




