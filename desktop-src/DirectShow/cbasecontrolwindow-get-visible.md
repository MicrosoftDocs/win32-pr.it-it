---
description: Il \_ metodo get Visible recupera la visibilità della finestra corrente.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: Metodo CBaseControlWindow.get_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332351"
---
# <a name="cbasecontrolwindowget_visible-method"></a><span data-ttu-id="623b6-103">CBaseControlWindow. Get ( \_ metodo visibile)</span><span class="sxs-lookup"><span data-stu-id="623b6-103">CBaseControlWindow.get\_Visible method</span></span>

<span data-ttu-id="623b6-104">Il `get_Visible` metodo recupera la visibilità della finestra corrente.</span><span class="sxs-lookup"><span data-stu-id="623b6-104">The `get_Visible` method retrieves the current window visibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="623b6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="623b6-105">Syntax</span></span>


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a><span data-ttu-id="623b6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="623b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="623b6-107">*pVisible*</span><span class="sxs-lookup"><span data-stu-id="623b6-107">*pVisible*</span></span> 
</dt> <dd>

<span data-ttu-id="623b6-108">Puntatore a un flag booleano di automazione (0 è disattivato, 1 è on).</span><span class="sxs-lookup"><span data-stu-id="623b6-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="623b6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="623b6-109">Return value</span></span>

<span data-ttu-id="623b6-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="623b6-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="623b6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="623b6-111">Remarks</span></span>

<span data-ttu-id="623b6-112">Questa funzione membro restituisce 1 se la finestra ha lo stile di visualizzazione WS \_ ; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="623b6-112">This member function returns  1 if the window has the WS\_VISIBLE style; 0 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="623b6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="623b6-113">Requirements</span></span>



| <span data-ttu-id="623b6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="623b6-114">Requirement</span></span> | <span data-ttu-id="623b6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="623b6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="623b6-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="623b6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="623b6-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="623b6-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="623b6-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="623b6-118">Library</span></span><br/> | <dl> <span data-ttu-id="623b6-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="623b6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="623b6-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="623b6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="623b6-121">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="623b6-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




