---
description: Il metodo PrepareWindow crea la finestra.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Metodo CBaseWindow. PrepareWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332586"
---
# <a name="cbasewindowpreparewindow-method"></a><span data-ttu-id="66cbf-103">CBaseWindow. PrepareWindow, metodo</span><span class="sxs-lookup"><span data-stu-id="66cbf-103">CBaseWindow.PrepareWindow method</span></span>

<span data-ttu-id="66cbf-104">Il `PrepareWindow` metodo crea la finestra.</span><span class="sxs-lookup"><span data-stu-id="66cbf-104">The `PrepareWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="66cbf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66cbf-105">Syntax</span></span>


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a><span data-ttu-id="66cbf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="66cbf-106">Parameters</span></span>

<span data-ttu-id="66cbf-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="66cbf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66cbf-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66cbf-108">Return value</span></span>

<span data-ttu-id="66cbf-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66cbf-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="66cbf-110">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="66cbf-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="66cbf-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="66cbf-111">Return code</span></span>                                                                            | <span data-ttu-id="66cbf-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66cbf-112">Description</span></span>         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="66cbf-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66cbf-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="66cbf-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="66cbf-114">Success.</span></span><br/> |
| <dl> <span data-ttu-id="66cbf-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="66cbf-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="66cbf-116">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="66cbf-116">Failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66cbf-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="66cbf-117">Remarks</span></span>

<span data-ttu-id="66cbf-118">Chiamare questo metodo dopo avere creato l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="66cbf-118">Call this method after creating the object.</span></span> <span data-ttu-id="66cbf-119">Questo metodo esegue una contabilità iniziale e quindi chiama il metodo [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) per creare la finestra.</span><span class="sxs-lookup"><span data-stu-id="66cbf-119">This method performs some initial bookkeeping and then calls the [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method to create the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="66cbf-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66cbf-120">Requirements</span></span>



| <span data-ttu-id="66cbf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="66cbf-121">Requirement</span></span> | <span data-ttu-id="66cbf-122">Valore</span><span class="sxs-lookup"><span data-stu-id="66cbf-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66cbf-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66cbf-123">Header</span></span><br/>  | <dl> <span data-ttu-id="66cbf-124"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66cbf-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="66cbf-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="66cbf-125">Library</span></span><br/> | <dl> <span data-ttu-id="66cbf-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="66cbf-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66cbf-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66cbf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66cbf-128">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="66cbf-128">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




