---
description: Il metodo DoGetWindowStyle recupera gli stili di finestra normali o estesi correnti.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Metodo CBaseControlWindow.DoGetWindowStyle (Ctlutil.h)
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
ms.openlocfilehash: d970ee52203c5c8dfe8a897c5612604becc2b2e1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909819"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="8727c-103">Metodo CBaseControlWindow.DoGetWindowStyle</span><span class="sxs-lookup"><span data-stu-id="8727c-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="8727c-104">Il `DoGetWindowStyle` metodo recupera gli stili di finestra normali o estesi correnti.</span><span class="sxs-lookup"><span data-stu-id="8727c-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="8727c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8727c-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="8727c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8727c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8727c-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="8727c-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="8727c-108">Puntatore a una variabile che riceve le informazioni sullo stile.</span><span class="sxs-lookup"><span data-stu-id="8727c-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="8727c-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="8727c-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="8727c-110">Valore che specifica gli stili da recuperare.</span><span class="sxs-lookup"><span data-stu-id="8727c-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="8727c-111">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8727c-111">Must be one of the following:</span></span>



| <span data-ttu-id="8727c-112">Label</span><span class="sxs-lookup"><span data-stu-id="8727c-112">Label</span></span> | <span data-ttu-id="8727c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="8727c-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="8727c-114">STILE \_ GWL</span><span class="sxs-lookup"><span data-stu-id="8727c-114">GWL\_STYLE</span></span>   | <span data-ttu-id="8727c-115">Recuperare gli stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="8727c-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="8727c-116">GWL \_ EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="8727c-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="8727c-117">Recuperare gli stili di finestra estesi.</span><span class="sxs-lookup"><span data-stu-id="8727c-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8727c-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8727c-118">Return value</span></span>

<span data-ttu-id="8727c-119">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="8727c-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8727c-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="8727c-120">Remarks</span></span>

<span data-ttu-id="8727c-121">Questa funzione membro chiama la funzione Win32 **GetWindowLong** per recuperare lo stile della finestra.</span><span class="sxs-lookup"><span data-stu-id="8727c-121">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="8727c-122">Viene chiamato dalle funzioni membro [**CBaseControlWindow::get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) e [**CBaseControlWindow::get \_ WindowStyleEx.**](cbasecontrolwindow-get-windowstyleex.md)</span><span class="sxs-lookup"><span data-stu-id="8727c-122">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8727c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8727c-123">Requirements</span></span>



| <span data-ttu-id="8727c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8727c-124">Requirement</span></span> | <span data-ttu-id="8727c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8727c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8727c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8727c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8727c-127"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="8727c-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8727c-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="8727c-128">Library</span></span><br/> | <dl> <span data-ttu-id="8727c-129"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8727c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8727c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8727c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8727c-131">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="8727c-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




