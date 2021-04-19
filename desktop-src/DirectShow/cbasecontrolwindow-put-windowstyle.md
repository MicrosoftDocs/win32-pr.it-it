---
description: Il \_ metodo Put WindowStyle imposta gli stili della finestra standard.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: Metodo CBaseControlWindow.put_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333366"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a><span data-ttu-id="760e8-103">CBaseControlWindow. put \_ WindowStyle (metodo)</span><span class="sxs-lookup"><span data-stu-id="760e8-103">CBaseControlWindow.put\_WindowStyle method</span></span>

<span data-ttu-id="760e8-104">Il `put_WindowStyle` metodo imposta gli stili della finestra standard.</span><span class="sxs-lookup"><span data-stu-id="760e8-104">The `put_WindowStyle` method sets the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="760e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="760e8-105">Syntax</span></span>


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="760e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="760e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="760e8-107">*WindowStyle*</span><span class="sxs-lookup"><span data-stu-id="760e8-107">*WindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="760e8-108">Nuovi stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="760e8-108">New window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="760e8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="760e8-109">Return value</span></span>

<span data-ttu-id="760e8-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="760e8-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="760e8-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="760e8-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="760e8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="760e8-112">Remarks</span></span>

<span data-ttu-id="760e8-113">Prestare attenzione quando si modificano gli stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="760e8-113">Take care when changing the window styles.</span></span> <span data-ttu-id="760e8-114">Nella maggior parte dei casi, un'applicazione deve recuperare lo stile corrente e quindi aggiungere o rimuovere i bit non appropriati.</span><span class="sxs-lookup"><span data-stu-id="760e8-114">In most cases, an application should retrieve the current style and then add or remove the inappropriate bits.</span></span> <span data-ttu-id="760e8-115">Questa procedura consente di mantenere intatti diversi stili interni della finestra utilizzati da Windows.</span><span class="sxs-lookup"><span data-stu-id="760e8-115">This procedure allows various internal window styles used by Windows to remain intact.</span></span>

## <a name="requirements"></a><span data-ttu-id="760e8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="760e8-116">Requirements</span></span>



| <span data-ttu-id="760e8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="760e8-117">Requirement</span></span> | <span data-ttu-id="760e8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="760e8-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="760e8-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="760e8-119">Header</span></span><br/>  | <dl> <span data-ttu-id="760e8-120"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="760e8-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="760e8-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="760e8-121">Library</span></span><br/> | <dl> <span data-ttu-id="760e8-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="760e8-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="760e8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="760e8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="760e8-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="760e8-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




