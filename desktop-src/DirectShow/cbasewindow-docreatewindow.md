---
description: Il metodo DoCreateWindow crea la finestra.
ms.assetid: bbe38a71-bbf7-4380-96a3-074b992a1d1e
title: Metodo CBaseWindow.DoCreateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoCreateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76bea1523f48a6e22a3c2d9370fa32bcea022621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325340"
---
# <a name="cbasewindowdocreatewindow-method"></a><span data-ttu-id="04b4d-103">Metodo reateWindow CBaseWindow.DoC</span><span class="sxs-lookup"><span data-stu-id="04b4d-103">CBaseWindow.DoCreateWindow method</span></span>

<span data-ttu-id="04b4d-104">Il `DoCreateWindow` metodo crea la finestra.</span><span class="sxs-lookup"><span data-stu-id="04b4d-104">The `DoCreateWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b4d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04b4d-105">Syntax</span></span>


```C++
HRESULT DoCreateWindow();
```



## <a name="parameters"></a><span data-ttu-id="04b4d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04b4d-106">Parameters</span></span>

<span data-ttu-id="04b4d-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="04b4d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="04b4d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04b4d-108">Return value</span></span>

<span data-ttu-id="04b4d-109">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="04b4d-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="04b4d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="04b4d-110">Remarks</span></span>

<span data-ttu-id="04b4d-111">Il metodo [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="04b4d-111">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b4d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04b4d-112">Requirements</span></span>



| <span data-ttu-id="04b4d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="04b4d-113">Requirement</span></span> | <span data-ttu-id="04b4d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="04b4d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b4d-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04b4d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="04b4d-116"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04b4d-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="04b4d-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="04b4d-117">Library</span></span><br/> | <dl> <span data-ttu-id="04b4d-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="04b4d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b4d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04b4d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b4d-120">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="04b4d-120">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




