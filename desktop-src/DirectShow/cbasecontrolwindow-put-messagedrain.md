---
description: Il \_ metodo Put MessageDrain imposta la finestra per la ricezione di messaggi della finestra inviati al renderer video.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: Metodo CBaseControlWindow.put_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331943"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a><span data-ttu-id="6ead2-103">CBaseControlWindow. put \_ MessageDrain (metodo)</span><span class="sxs-lookup"><span data-stu-id="6ead2-103">CBaseControlWindow.put\_MessageDrain method</span></span>

<span data-ttu-id="6ead2-104">Il `put_MessageDrain` metodo imposta la finestra per la ricezione di messaggi della finestra inviati al renderer video.</span><span class="sxs-lookup"><span data-stu-id="6ead2-104">The `put_MessageDrain` method sets the window to receive window messages sent to the video renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ead2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ead2-105">Syntax</span></span>


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a><span data-ttu-id="6ead2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ead2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ead2-107">*Scarico*</span><span class="sxs-lookup"><span data-stu-id="6ead2-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="6ead2-108">Finestra in cui pubblicare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="6ead2-108">Window to post messages to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ead2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ead2-109">Return value</span></span>

<span data-ttu-id="6ead2-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ead2-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ead2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ead2-111">Remarks</span></span>

<span data-ttu-id="6ead2-112">I messaggi inviati al filtro renderer video possono essere inseriti in un'altra finestra.</span><span class="sxs-lookup"><span data-stu-id="6ead2-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="6ead2-113">Questa funzione membro registra la finestra per ricevere questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="6ead2-113">This member function registers the window to receive these messages.</span></span> <span data-ttu-id="6ead2-114">A differenza della funzione membro [**CBaseControlWindow::p UT \_ owner**](cbasecontrolwindow-put-owner.md) , questa funzione membro non rende la finestra video un elemento figlio di un'altra finestra.</span><span class="sxs-lookup"><span data-stu-id="6ead2-114">Unlike the [**CBaseControlWindow::put\_Owner**](cbasecontrolwindow-put-owner.md) member function, this member function does not make the video window a child of another window.</span></span> <span data-ttu-id="6ead2-115">È particolarmente utile per i renderer video a schermo intero, che non possono essere finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="6ead2-115">It is particularly useful for full-screen video renderers, which cannot be child windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ead2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ead2-116">Requirements</span></span>



| <span data-ttu-id="6ead2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ead2-117">Requirement</span></span> | <span data-ttu-id="6ead2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6ead2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ead2-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ead2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6ead2-120"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ead2-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6ead2-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="6ead2-121">Library</span></span><br/> | <dl> <span data-ttu-id="6ead2-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6ead2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ead2-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ead2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ead2-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="6ead2-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




