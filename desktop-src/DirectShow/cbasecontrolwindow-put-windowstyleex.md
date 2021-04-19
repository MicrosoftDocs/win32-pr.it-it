---
description: Il \_ metodo Put WindowStyleEx imposta gli stili della finestra estesa.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: Metodo CBaseControlWindow.put_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333365"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a><span data-ttu-id="39b9e-103">CBaseControlWindow. put \_ WindowStyleEx (metodo)</span><span class="sxs-lookup"><span data-stu-id="39b9e-103">CBaseControlWindow.put\_WindowStyleEx method</span></span>

<span data-ttu-id="39b9e-104">Il `put_WindowStyleEx` metodo imposta gli stili della finestra estesa.</span><span class="sxs-lookup"><span data-stu-id="39b9e-104">The `put_WindowStyleEx` method sets the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39b9e-105">Syntax</span></span>


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="39b9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="39b9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39b9e-107">*WindowStyleEx* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39b9e-107">*WindowStyleEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39b9e-108">Valore che specifica lo stile della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="39b9e-108">Value that specifies the style of the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39b9e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39b9e-109">Return value</span></span>

<span data-ttu-id="39b9e-110">Restituisce NOERROR.</span><span class="sxs-lookup"><span data-stu-id="39b9e-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="39b9e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="39b9e-111">Remarks</span></span>

<span data-ttu-id="39b9e-112">Questo metodo utilizza gli stili estesi della finestra.</span><span class="sxs-lookup"><span data-stu-id="39b9e-112">This method uses extended window styles.</span></span> <span data-ttu-id="39b9e-113">Per un elenco completo degli stili della finestra estesa, vedere la funzione **CreateWindowEx** di Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="39b9e-113">For a complete list of extended window styles, see the Microsoft Win32 **CreateWindowEx** function.</span></span> <span data-ttu-id="39b9e-114">Per modificare lo stile della finestra, recuperare lo stile della finestra corrente, quindi aggiungere o rimuovere i campi di bit necessari.</span><span class="sxs-lookup"><span data-stu-id="39b9e-114">To change the window style, retrieve the current window style, and then add or remove the necessary bit fields.</span></span>

<span data-ttu-id="39b9e-115">Non usare gli stili della finestra seguenti perché non vengono convalidati.</span><span class="sxs-lookup"><span data-stu-id="39b9e-115">Do not use the following window styles because they are not validated.</span></span>

-   <span data-ttu-id="39b9e-116">WS \_ disabilitato</span><span class="sxs-lookup"><span data-stu-id="39b9e-116">WS\_DISABLED</span></span>
-   <span data-ttu-id="39b9e-117">WS \_ HSCROLL</span><span class="sxs-lookup"><span data-stu-id="39b9e-117">WS\_HSCROLL</span></span>
-   <span data-ttu-id="39b9e-118">\_icona WS</span><span class="sxs-lookup"><span data-stu-id="39b9e-118">WS\_ICONIC</span></span>
-   <span data-ttu-id="39b9e-119">WS- \_ Ingrandisc</span><span class="sxs-lookup"><span data-stu-id="39b9e-119">WS\_MAXIMIZE</span></span>
-   <span data-ttu-id="39b9e-120">WS- \_ riduzione a icona</span><span class="sxs-lookup"><span data-stu-id="39b9e-120">WS\_MINIMIZE</span></span>
-   <span data-ttu-id="39b9e-121">WS \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="39b9e-121">WS\_VSCROLL</span></span>

<span data-ttu-id="39b9e-122">Con alcune eccezioni (indicate qui), i flag accettabili sono gli stessi di quelli consentiti dalla funzione Win32 **CreateWindow** .</span><span class="sxs-lookup"><span data-stu-id="39b9e-122">With some exceptions (noted here), the acceptable flags are the same as those allowed by the Win32 **CreateWindow** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b9e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39b9e-123">Requirements</span></span>



| <span data-ttu-id="39b9e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="39b9e-124">Requirement</span></span> | <span data-ttu-id="39b9e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="39b9e-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39b9e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39b9e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="39b9e-127"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39b9e-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="39b9e-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="39b9e-128">Library</span></span><br/> | <dl> <span data-ttu-id="39b9e-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="39b9e-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39b9e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39b9e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b9e-131">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="39b9e-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




