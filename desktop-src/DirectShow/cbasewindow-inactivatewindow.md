---
description: Il metodo InactivateWindow disattiva la finestra. Nella classe di base, questo metodo nasconde la finestra.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Metodo CBaseWindow. InactivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1c5e925a3d9b510918636a221d5ad6e1b7da736
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327937"
---
# <a name="cbasewindowinactivatewindow-method"></a><span data-ttu-id="3f632-104">CBaseWindow. InactivateWindow, metodo</span><span class="sxs-lookup"><span data-stu-id="3f632-104">CBaseWindow.InactivateWindow method</span></span>

<span data-ttu-id="3f632-105">Il `InactivateWindow` metodo disattiva la finestra.</span><span class="sxs-lookup"><span data-stu-id="3f632-105">The `InactivateWindow` method inactivates the window.</span></span> <span data-ttu-id="3f632-106">Nella classe di base, questo metodo nasconde la finestra.</span><span class="sxs-lookup"><span data-stu-id="3f632-106">In the base class, this method hides the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f632-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f632-107">Syntax</span></span>


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="3f632-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f632-108">Parameters</span></span>

<span data-ttu-id="3f632-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3f632-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f632-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f632-110">Return value</span></span>

<span data-ttu-id="3f632-111">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3f632-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="3f632-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3f632-112">Return code</span></span>                                                                             | <span data-ttu-id="3f632-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f632-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="3f632-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3f632-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="3f632-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3f632-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="3f632-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3f632-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="3f632-117">La finestra è già inattiva.</span><span class="sxs-lookup"><span data-stu-id="3f632-117">Window is already inactive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3f632-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f632-118">Requirements</span></span>



| <span data-ttu-id="3f632-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f632-119">Requirement</span></span> | <span data-ttu-id="3f632-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3f632-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f632-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f632-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3f632-122"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f632-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3f632-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f632-123">Library</span></span><br/> | <dl> <span data-ttu-id="3f632-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3f632-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f632-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f632-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f632-126">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="3f632-126">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




