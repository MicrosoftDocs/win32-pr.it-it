---
description: Il metodo DoShowWindow imposta lo stato di visualizzazione della finestra.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Metodo CBaseWindow. DoShowWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2a1f7d4cd9bc4600733d5d33f9df6d3b6998f57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327952"
---
# <a name="cbasewindowdoshowwindow-method"></a><span data-ttu-id="b84c9-103">CBaseWindow. DoShowWindow, metodo</span><span class="sxs-lookup"><span data-stu-id="b84c9-103">CBaseWindow.DoShowWindow method</span></span>

<span data-ttu-id="b84c9-104">Il metodo **DoShowWindow** imposta lo stato di visualizzazione della finestra.</span><span class="sxs-lookup"><span data-stu-id="b84c9-104">The **DoShowWindow** method sets the window's show state.</span></span>

## <a name="syntax"></a><span data-ttu-id="b84c9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b84c9-105">Syntax</span></span>


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a><span data-ttu-id="b84c9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b84c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b84c9-107">*ShowCmd*</span><span class="sxs-lookup"><span data-stu-id="b84c9-107">*ShowCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="b84c9-108">Flag che specifica come deve essere visualizzata la finestra.</span><span class="sxs-lookup"><span data-stu-id="b84c9-108">Flag that specifies how the window is to be shown.</span></span> <span data-ttu-id="b84c9-109">Il valore può essere qualsiasi costante definita per il parametro *nCmdShow* della funzione [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="b84c9-109">The value can be any constant defined for the *nCmdShow* parameter of the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b84c9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b84c9-110">Return value</span></span>

<span data-ttu-id="b84c9-111">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b84c9-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b84c9-112">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b84c9-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b84c9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b84c9-113">Requirements</span></span>



| <span data-ttu-id="b84c9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b84c9-114">Requirement</span></span> | <span data-ttu-id="b84c9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b84c9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b84c9-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b84c9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b84c9-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b84c9-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b84c9-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="b84c9-118">Library</span></span><br/> | <dl> <span data-ttu-id="b84c9-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b84c9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b84c9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b84c9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b84c9-121">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="b84c9-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

