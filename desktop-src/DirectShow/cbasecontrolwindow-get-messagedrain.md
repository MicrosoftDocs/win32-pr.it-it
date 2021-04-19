---
description: Il \_ metodo Get MessageDrain recupera lo svuotamento del messaggio corrente.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: Metodo CBaseControlWindow.get_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326068"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a><span data-ttu-id="57440-103">Metodo CBaseControlWindow. Get \_ MessageDrain</span><span class="sxs-lookup"><span data-stu-id="57440-103">CBaseControlWindow.get\_MessageDrain method</span></span>

<span data-ttu-id="57440-104">Il `get_MessageDrain` metodo recupera lo svuotamento del messaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="57440-104">The `get_MessageDrain` method retrieves the current message drain.</span></span>

## <a name="syntax"></a><span data-ttu-id="57440-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57440-105">Syntax</span></span>


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a><span data-ttu-id="57440-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="57440-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57440-107">*Scarico*</span><span class="sxs-lookup"><span data-stu-id="57440-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="57440-108">Puntatore alla finestra corrente che riceve i messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="57440-108">Pointer to the current window receiving window messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57440-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57440-109">Return value</span></span>

<span data-ttu-id="57440-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57440-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57440-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="57440-111">Remarks</span></span>

<span data-ttu-id="57440-112">I messaggi inviati al filtro renderer video possono essere inseriti in un'altra finestra.</span><span class="sxs-lookup"><span data-stu-id="57440-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="57440-113">La finestra registrata per ricevere questi messaggi (usando la funzione membro **CBaseControlWindow:: Get \_ MessageDrain** ) è lo svuotamento del messaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="57440-113">The window registered to receive these messages (using the **CBaseControlWindow::get\_MessageDrain** member function) is the current message drain.</span></span>

## <a name="requirements"></a><span data-ttu-id="57440-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57440-114">Requirements</span></span>



| <span data-ttu-id="57440-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="57440-115">Requirement</span></span> | <span data-ttu-id="57440-116">Valore</span><span class="sxs-lookup"><span data-stu-id="57440-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57440-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57440-117">Header</span></span><br/>  | <dl> <span data-ttu-id="57440-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57440-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="57440-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="57440-119">Library</span></span><br/> | <dl> <span data-ttu-id="57440-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="57440-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57440-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57440-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57440-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="57440-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




