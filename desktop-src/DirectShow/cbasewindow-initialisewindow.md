---
description: Il metodo InitialiseWindow Inizializza la finestra.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: Metodo CBaseWindow.InitialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327935"
---
# <a name="cbasewindowinitialisewindow-method"></a><span data-ttu-id="fce40-103">Metodo tialiseWindow CBaseWindow.Ini</span><span class="sxs-lookup"><span data-stu-id="fce40-103">CBaseWindow.InitialiseWindow method</span></span>

<span data-ttu-id="fce40-104">Il `InitialiseWindow` metodo inizializza la finestra.</span><span class="sxs-lookup"><span data-stu-id="fce40-104">The `InitialiseWindow` method initializes the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce40-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fce40-105">Syntax</span></span>


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="fce40-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fce40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fce40-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="fce40-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="fce40-108">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="fce40-108">Handle to the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fce40-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fce40-109">Return value</span></span>

<span data-ttu-id="fce40-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fce40-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fce40-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="fce40-111">Remarks</span></span>

<span data-ttu-id="fce40-112">Per impostazione predefinita, questo metodo recupera un handle per il contesto di dispositivo (DC) della finestra e crea un controller di dominio di memoria compatibile.</span><span class="sxs-lookup"><span data-stu-id="fce40-112">By default, this method retrieves a handle to the window's device context (DC) and creates a compatible memory DC.</span></span> <span data-ttu-id="fce40-113">Se il valore del flag [**\_ BDoGetDC di CBaseWindow:: m**](cbasewindow-m-bdogetdc.md) è **false**, tuttavia, questo metodo non recupera i contesti di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fce40-113">If the value of the [**CBaseWindow::m\_bDoGetDC**](cbasewindow-m-bdogetdc.md) flag is **FALSE**, however, this method does not retrieve the device contexts.</span></span> <span data-ttu-id="fce40-114">Il controller di dominio della memoria è utile per la selezione di bitmap prima di blitting nella finestra.</span><span class="sxs-lookup"><span data-stu-id="fce40-114">The memory DC is useful for selecting bitmaps before blitting them to the window.</span></span>

<span data-ttu-id="fce40-115">Il metodo [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fce40-115">The [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce40-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fce40-116">Requirements</span></span>



| <span data-ttu-id="fce40-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fce40-117">Requirement</span></span> | <span data-ttu-id="fce40-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fce40-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fce40-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fce40-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fce40-120"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fce40-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fce40-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="fce40-121">Library</span></span><br/> | <dl> <span data-ttu-id="fce40-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fce40-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce40-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fce40-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce40-124">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="fce40-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




