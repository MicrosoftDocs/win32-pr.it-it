---
description: Il metodo DoSetWindowStyle modifica gli stili di finestra tipici o estesi.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Metodo CBaseControlWindow.DoSetWindowStyle (Ctlutil.h)
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
ms.openlocfilehash: db88c5818d31d65f361ae1a805bd50c285d4a5c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909809"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="e5421-103">Metodo CBaseControlWindow.DoSetWindowStyle</span><span class="sxs-lookup"><span data-stu-id="e5421-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="e5421-104">Il metodo modifica gli stili di finestra tipici `DoSetWindowStyle` o estesi.</span><span class="sxs-lookup"><span data-stu-id="e5421-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5421-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5421-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="e5421-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5421-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5421-107">*Style*</span><span class="sxs-lookup"><span data-stu-id="e5421-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="e5421-108">Stili di finestra appropriati.</span><span class="sxs-lookup"><span data-stu-id="e5421-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="e5421-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="e5421-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="e5421-110">Valore che specifica gli stili da impostare.</span><span class="sxs-lookup"><span data-stu-id="e5421-110">Value specifying which styles to set.</span></span> <span data-ttu-id="e5421-111">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5421-111">Must be one of the following:</span></span>



| <span data-ttu-id="e5421-112">Label</span><span class="sxs-lookup"><span data-stu-id="e5421-112">Label</span></span> | <span data-ttu-id="e5421-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e5421-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="e5421-114">STILE \_ GWL</span><span class="sxs-lookup"><span data-stu-id="e5421-114">GWL\_STYLE</span></span>   | <span data-ttu-id="e5421-115">Recuperare gli stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="e5421-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="e5421-116">GWL \_ EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="e5421-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="e5421-117">Recuperare gli stili di finestra estesi.</span><span class="sxs-lookup"><span data-stu-id="e5421-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5421-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5421-118">Return value</span></span>

<span data-ttu-id="e5421-119">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="e5421-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5421-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5421-120">Remarks</span></span>

<span data-ttu-id="e5421-121">Questa funzione membro chiama la funzione **Win32 SetWindowLong** per impostare lo stile della finestra e quindi visualizza nuovamente la finestra nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="e5421-121">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="e5421-122">Questa funzione membro viene chiamata dalle funzioni membro [**CBaseControlWindow::p ut \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) e [**CBaseControlWindow::p ut \_ WindowStyleEx.**](cbasecontrolwindow-put-windowstyleex.md)</span><span class="sxs-lookup"><span data-stu-id="e5421-122">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5421-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5421-123">Requirements</span></span>



| <span data-ttu-id="e5421-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5421-124">Requirement</span></span> | <span data-ttu-id="e5421-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e5421-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5421-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5421-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e5421-127"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5421-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e5421-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5421-128">Library</span></span><br/> | <dl> <span data-ttu-id="e5421-129"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e5421-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5421-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5421-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5421-131">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="e5421-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




