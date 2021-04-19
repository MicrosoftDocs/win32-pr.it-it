---
description: Il metodo OnPaletteChange gestisce i messaggi di modifica della tavolozza.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Metodo CBaseWindow. OnPaletteChange (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325764"
---
# <a name="cbasewindowonpalettechange-method"></a><span data-ttu-id="e7aa1-103">CBaseWindow. OnPaletteChange, metodo</span><span class="sxs-lookup"><span data-stu-id="e7aa1-103">CBaseWindow.OnPaletteChange method</span></span>

<span data-ttu-id="e7aa1-104">Il `OnPaletteChange` metodo gestisce i messaggi di modifica della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-104">The `OnPaletteChange` method handles palette-change messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7aa1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7aa1-105">Syntax</span></span>


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a><span data-ttu-id="e7aa1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7aa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7aa1-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="e7aa1-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e7aa1-108">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="e7aa1-109">*Messaggio*</span><span class="sxs-lookup"><span data-stu-id="e7aa1-109">*Message*</span></span> 
</dt> <dd>

<span data-ttu-id="e7aa1-110">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-110">Message identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7aa1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7aa1-111">Return value</span></span>

<span data-ttu-id="e7aa1-112">Restituisce 0 se il messaggio è stato elaborato oppure 1 se il messaggio non è stato elaborato.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-112">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7aa1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7aa1-113">Remarks</span></span>

<span data-ttu-id="e7aa1-114">Questo metodo gestisce \_ i messaggi WM PALETTECHANGED e WM \_ QUERYNEWPALETTE.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-114">This method handles WM\_PALETTECHANGED and WM\_QUERYNEWPALETTE messages.</span></span> <span data-ttu-id="e7aa1-115">Chiama il metodo [**CBaseWindow::D orealisepalette**](cbasewindow-dorealisepalette.md) per realizzare la nuova tavolozza.</span><span class="sxs-lookup"><span data-stu-id="e7aa1-115">It calls the [**CBaseWindow::DoRealisePalette**](cbasewindow-dorealisepalette.md) method to realize the new palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7aa1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7aa1-116">Requirements</span></span>



| <span data-ttu-id="e7aa1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7aa1-117">Requirement</span></span> | <span data-ttu-id="e7aa1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e7aa1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7aa1-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7aa1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e7aa1-120"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7aa1-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e7aa1-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="e7aa1-121">Library</span></span><br/> | <dl> <span data-ttu-id="e7aa1-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e7aa1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7aa1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7aa1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7aa1-124">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="e7aa1-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




