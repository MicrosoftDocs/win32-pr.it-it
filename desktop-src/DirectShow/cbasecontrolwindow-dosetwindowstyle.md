---
description: Il metodo DoSetWindowStyle modifica gli stili di finestra tipici o estesi.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Metodo CBaseControlWindow. DoSetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d57d023dff803caf5da7e61dea266670ec8bde5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325391"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="f64e0-103">CBaseControlWindow. DoSetWindowStyle, metodo</span><span class="sxs-lookup"><span data-stu-id="f64e0-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="f64e0-104">Il `DoSetWindowStyle` metodo modifica gli stili di finestra tipici o estesi.</span><span class="sxs-lookup"><span data-stu-id="f64e0-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="f64e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f64e0-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="f64e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f64e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f64e0-107">*Style*</span><span class="sxs-lookup"><span data-stu-id="f64e0-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="f64e0-108">Stili di finestra appropriati.</span><span class="sxs-lookup"><span data-stu-id="f64e0-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="f64e0-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="f64e0-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="f64e0-110">Valore che specifica gli stili da impostare.</span><span class="sxs-lookup"><span data-stu-id="f64e0-110">Value specifying which styles to set.</span></span> <span data-ttu-id="f64e0-111">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f64e0-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="f64e0-112">\_stile GWL</span><span class="sxs-lookup"><span data-stu-id="f64e0-112">GWL\_STYLE</span></span>   | <span data-ttu-id="f64e0-113">Recuperare gli stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="f64e0-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="f64e0-114">\_ExStyle GWL</span><span class="sxs-lookup"><span data-stu-id="f64e0-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="f64e0-115">Recuperare gli stili della finestra estesa.</span><span class="sxs-lookup"><span data-stu-id="f64e0-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f64e0-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f64e0-116">Return value</span></span>

<span data-ttu-id="f64e0-117">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f64e0-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f64e0-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f64e0-118">Remarks</span></span>

<span data-ttu-id="f64e0-119">Questa funzione membro chiama la funzione **SetWindowLong** Win32 per impostare lo stile della finestra e quindi Visualizza nuovamente la finestra nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="f64e0-119">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="f64e0-120">Questa funzione membro viene chiamata dalle funzioni membro [**CBaseControlWindow::p UT \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) e [**CBaseControlWindow::p UT \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="f64e0-120">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f64e0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f64e0-121">Requirements</span></span>



| <span data-ttu-id="f64e0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f64e0-122">Requirement</span></span> | <span data-ttu-id="f64e0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f64e0-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f64e0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f64e0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f64e0-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f64e0-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f64e0-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="f64e0-126">Library</span></span><br/> | <dl> <span data-ttu-id="f64e0-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f64e0-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f64e0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f64e0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f64e0-129">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="f64e0-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




