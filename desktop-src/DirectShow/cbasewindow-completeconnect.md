---
description: Il metodo CompleteConnect notifica alla finestra che il pin di input del renderer è stato connesso.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Metodo CBaseWindow. CompleteConnect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325342"
---
# <a name="cbasewindowcompleteconnect-method"></a><span data-ttu-id="855da-103">CBaseWindow. CompleteConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="855da-103">CBaseWindow.CompleteConnect method</span></span>

<span data-ttu-id="855da-104">Il `CompleteConnect` metodo notifica alla finestra che il pin di input del renderer è stato connesso.</span><span class="sxs-lookup"><span data-stu-id="855da-104">The `CompleteConnect` method notifies the window that the renderer's input pin has been connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="855da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="855da-105">Syntax</span></span>


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a><span data-ttu-id="855da-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="855da-106">Parameters</span></span>

<span data-ttu-id="855da-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="855da-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="855da-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="855da-108">Return value</span></span>

<span data-ttu-id="855da-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="855da-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="855da-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="855da-110">Remarks</span></span>

<span data-ttu-id="855da-111">Questo metodo reimposta il flag di attivazione della finestra ([**CBaseWindow:: m \_ bActivated**](cbasewindow-m-bactivated.md)) su **false**.</span><span class="sxs-lookup"><span data-stu-id="855da-111">This method resets the window activation flag ([**CBaseWindow::m\_bActivated**](cbasewindow-m-bactivated.md)) to **FALSE**.</span></span> <span data-ttu-id="855da-112">Quando un renderer video completa una connessione pin, può chiamare il metodo [**CBaseWindow:: Activatewindow**](cbasewindow-activatewindow.md) per impostare le dimensioni e la posizione della finestra.</span><span class="sxs-lookup"><span data-stu-id="855da-112">When a video renderer completes a pin connection, it might call the [**CBaseWindow::ActivateWindow**](cbasewindow-activatewindow.md) method to set the window's size and position.</span></span> <span data-ttu-id="855da-113">Per forzare il ricalcolo di questi attributi da parte di **Activatewindow** , chiamare prima il `CompleteConnect` metodo.</span><span class="sxs-lookup"><span data-stu-id="855da-113">To force **ActivateWindow** to recalculate these attributes, first call the `CompleteConnect` method.</span></span>

## <a name="requirements"></a><span data-ttu-id="855da-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="855da-114">Requirements</span></span>



| <span data-ttu-id="855da-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="855da-115">Requirement</span></span> | <span data-ttu-id="855da-116">Valore</span><span class="sxs-lookup"><span data-stu-id="855da-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="855da-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="855da-117">Header</span></span><br/>  | <dl> <span data-ttu-id="855da-118"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="855da-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="855da-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="855da-119">Library</span></span><br/> | <dl> <span data-ttu-id="855da-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="855da-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="855da-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="855da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="855da-122">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="855da-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




