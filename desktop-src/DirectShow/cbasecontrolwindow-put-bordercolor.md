---
description: Il \_ metodo Put BorderColor modifica il colore del bordo.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: Metodo CBaseControlWindow.put_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328354"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a><span data-ttu-id="3c4b6-103">CBaseControlWindow. Put, \_ Metodo BorderColor</span><span class="sxs-lookup"><span data-stu-id="3c4b6-103">CBaseControlWindow.put\_BorderColor method</span></span>

<span data-ttu-id="3c4b6-104">Il `put_BorderColor` metodo modifica il colore del bordo.</span><span class="sxs-lookup"><span data-stu-id="3c4b6-104">The `put_BorderColor` method changes the border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c4b6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c4b6-105">Syntax</span></span>


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a><span data-ttu-id="3c4b6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c4b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c4b6-107">*Colore*</span><span class="sxs-lookup"><span data-stu-id="3c4b6-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="3c4b6-108">Colore nuovo bordo.</span><span class="sxs-lookup"><span data-stu-id="3c4b6-108">New border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c4b6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c4b6-109">Return value</span></span>

<span data-ttu-id="3c4b6-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c4b6-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c4b6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c4b6-111">Remarks</span></span>

<span data-ttu-id="3c4b6-112">Un'applicazione può stabilire un rettangolo di destinazione in cui deve essere visualizzato il video.</span><span class="sxs-lookup"><span data-stu-id="3c4b6-112">An application can establish a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="3c4b6-113">Questo rettangolo è relativo all'area client per la finestra.</span><span class="sxs-lookup"><span data-stu-id="3c4b6-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="3c4b6-114">Se questa operazione viene eseguita (l'impostazione predefinita consiste nel disegnare sempre l'intera finestra), è presente un bordo che circonda il video.</span><span class="sxs-lookup"><span data-stu-id="3c4b6-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="3c4b6-115">Questa proprietà influiscono sul colore utilizzato dal bordo.</span><span class="sxs-lookup"><span data-stu-id="3c4b6-115">This property affects the color used by the border.</span></span> <span data-ttu-id="3c4b6-116">Anche se il parametro viene specificato come tipo **Long** , si tratta in realtà di un valore **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="3c4b6-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c4b6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c4b6-117">Requirements</span></span>



| <span data-ttu-id="3c4b6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c4b6-118">Requirement</span></span> | <span data-ttu-id="3c4b6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3c4b6-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c4b6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c4b6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3c4b6-121"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c4b6-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c4b6-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c4b6-122">Library</span></span><br/> | <dl> <span data-ttu-id="3c4b6-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3c4b6-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c4b6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c4b6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c4b6-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="3c4b6-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




