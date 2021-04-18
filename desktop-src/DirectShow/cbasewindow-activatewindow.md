---
description: Il metodo ActivateWindow ridimensiona la finestra in base ai requisiti della classe derivata.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Metodo CBaseWindow. ActivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330524"
---
# <a name="cbasewindowactivatewindow-method"></a><span data-ttu-id="a5a00-103">CBaseWindow. ActivateWindow, metodo</span><span class="sxs-lookup"><span data-stu-id="a5a00-103">CBaseWindow.ActivateWindow method</span></span>

<span data-ttu-id="a5a00-104">Il `ActivateWindow` metodo ridimensiona la finestra in base ai requisiti della classe derivata.</span><span class="sxs-lookup"><span data-stu-id="a5a00-104">The `ActivateWindow` method sizes the window according to the requirements of the derived class.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5a00-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5a00-105">Syntax</span></span>


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="a5a00-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5a00-106">Parameters</span></span>

<span data-ttu-id="a5a00-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a5a00-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5a00-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5a00-108">Return value</span></span>

<span data-ttu-id="a5a00-109">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a5a00-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a5a00-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a5a00-110">Return code</span></span>                                                                             | <span data-ttu-id="a5a00-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5a00-111">Description</span></span>                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="a5a00-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a00-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="a5a00-113">La finestra è già stata attivata.</span><span class="sxs-lookup"><span data-stu-id="a5a00-113">Window was already activated.</span></span><br/> |
| <dl> <span data-ttu-id="a5a00-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a00-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="a5a00-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a5a00-115">Success.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="a5a00-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5a00-116">Remarks</span></span>

<span data-ttu-id="a5a00-117">Questo metodo chiama il metodo [**CBaseWindow:: GetDefaultRect**](cbasewindow-getdefaultrect.md) per determinare le dimensioni della finestra.</span><span class="sxs-lookup"><span data-stu-id="a5a00-117">This methods calls the [**CBaseWindow::GetDefaultRect**](cbasewindow-getdefaultrect.md) method to determine the window size.</span></span> <span data-ttu-id="a5a00-118">La classe derivata deve eseguire l'override di **GetDefaultRect** per restituire la dimensione delle immagini che verranno visualizzate.</span><span class="sxs-lookup"><span data-stu-id="a5a00-118">The derived class should override **GetDefaultRect** to return the size of the images that will be displayed.</span></span>

<span data-ttu-id="a5a00-119">Se la finestra è già attiva, la chiamata `ActivateWindow` Sposta la finestra nella parte superiore del z order, ma non ridimensiona la finestra.</span><span class="sxs-lookup"><span data-stu-id="a5a00-119">If the window is already active, calling `ActivateWindow` moves the window to the top of the Z order, but does not resize the window.</span></span> <span data-ttu-id="a5a00-120">Lo stesso vale se la finestra dispone di un elemento padre.</span><span class="sxs-lookup"><span data-stu-id="a5a00-120">The same is true if the window has a parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5a00-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5a00-121">Requirements</span></span>



| <span data-ttu-id="a5a00-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5a00-122">Requirement</span></span> | <span data-ttu-id="a5a00-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a5a00-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a00-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5a00-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a5a00-125"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5a00-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a5a00-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a5a00-126">Library</span></span><br/> | <dl> <span data-ttu-id="a5a00-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a5a00-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5a00-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5a00-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5a00-129">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="a5a00-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




