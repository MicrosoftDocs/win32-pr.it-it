---
description: Il metodo DoGetWindowStyle recupera gli stili correnti della finestra normale o estesa.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Metodo CBaseControlWindow. DoGetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328095"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="aa566-103">CBaseControlWindow. DoGetWindowStyle, metodo</span><span class="sxs-lookup"><span data-stu-id="aa566-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="aa566-104">Il `DoGetWindowStyle` metodo recupera gli stili correnti della finestra normale o estesa.</span><span class="sxs-lookup"><span data-stu-id="aa566-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa566-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa566-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="aa566-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa566-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa566-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="aa566-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="aa566-108">Puntatore a una variabile che riceve le informazioni sullo stile.</span><span class="sxs-lookup"><span data-stu-id="aa566-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="aa566-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="aa566-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="aa566-110">Valore che specifica gli stili da recuperare.</span><span class="sxs-lookup"><span data-stu-id="aa566-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="aa566-111">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa566-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="aa566-112">\_stile GWL</span><span class="sxs-lookup"><span data-stu-id="aa566-112">GWL\_STYLE</span></span>   | <span data-ttu-id="aa566-113">Recuperare gli stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="aa566-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="aa566-114">\_ExStyle GWL</span><span class="sxs-lookup"><span data-stu-id="aa566-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="aa566-115">Recuperare gli stili della finestra estesa.</span><span class="sxs-lookup"><span data-stu-id="aa566-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa566-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa566-116">Return value</span></span>

<span data-ttu-id="aa566-117">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aa566-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa566-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa566-118">Remarks</span></span>

<span data-ttu-id="aa566-119">Questa funzione membro chiama la funzione **GetWindowLong** Win32 per recuperare lo stile della finestra.</span><span class="sxs-lookup"><span data-stu-id="aa566-119">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="aa566-120">Viene chiamato dalle funzioni membro [**CBaseControlWindow:: Get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) e [**CBaseControlWindow:: Get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="aa566-120">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa566-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa566-121">Requirements</span></span>



| <span data-ttu-id="aa566-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa566-122">Requirement</span></span> | <span data-ttu-id="aa566-123">Valore</span><span class="sxs-lookup"><span data-stu-id="aa566-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa566-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa566-124">Header</span></span><br/>  | <dl> <span data-ttu-id="aa566-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa566-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aa566-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa566-126">Library</span></span><br/> | <dl> <span data-ttu-id="aa566-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="aa566-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa566-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa566-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa566-129">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="aa566-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




