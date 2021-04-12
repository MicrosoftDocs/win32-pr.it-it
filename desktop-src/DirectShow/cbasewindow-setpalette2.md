---
description: Il metodo setavolozza installa una tavolozza per la finestra. Questo metodo non presenta parametri.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: Metodo CBaseWindow. setavolozze (Winutil. h)-nessun parametro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1203b6aeedd39eb82d7188c4e5d5503b01d167fe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104235234"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a><span data-ttu-id="e4f37-104">Metodo CBaseWindow. setavolozze (Winutil. h)-nessun parametro</span><span class="sxs-lookup"><span data-stu-id="e4f37-104">CBaseWindow.SetPalette method (Winutil.h) - No parameters</span></span>

<span data-ttu-id="e4f37-105">Il `SetPalette` metodo installa una tavolozza per la finestra.</span><span class="sxs-lookup"><span data-stu-id="e4f37-105">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f37-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4f37-106">Syntax</span></span>


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a><span data-ttu-id="e4f37-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4f37-107">Parameters</span></span>

<span data-ttu-id="e4f37-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e4f37-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4f37-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4f37-109">Return value</span></span>

<span data-ttu-id="e4f37-110">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e4f37-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e4f37-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e4f37-111">Return code</span></span>                                                                             | <span data-ttu-id="e4f37-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4f37-112">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="e4f37-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e4f37-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e4f37-114">Una chiamata interna a **GDIFlush** ha restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="e4f37-114">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="e4f37-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4f37-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e4f37-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e4f37-116">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="e4f37-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4f37-117">Remarks</span></span>

<span data-ttu-id="e4f37-118">Viene selezionata la tavolozza fornita dalla variabile membro [**CBaseWindow:: m \_ hPalette**](cbasewindow-m-hpalette.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f37-118">The palette given by the [**CBaseWindow::m\_hPalette**](cbasewindow-m-hpalette.md) member variable is selected.</span></span> <span data-ttu-id="e4f37-119">Il chiamante deve garantire la validità di **m \_ hPalette**.</span><span class="sxs-lookup"><span data-stu-id="e4f37-119">The caller must ensure the validity of **m\_hPalette**.</span></span>

<span data-ttu-id="e4f37-120">Se il valore della variabile membro [**\_ BNoRealize di CBaseWindow:: m**](cbasewindow-m-bnorealize.md) è **false** (impostazione predefinita), questo metodo seleziona la tavolozza e la realizza.</span><span class="sxs-lookup"><span data-stu-id="e4f37-120">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="e4f37-121">In caso contrario, seleziona la tavolozza, ma non la realizza.</span><span class="sxs-lookup"><span data-stu-id="e4f37-121">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="e4f37-122">L'oggetto non elimina le tavolozze precedenti utilizzate.</span><span class="sxs-lookup"><span data-stu-id="e4f37-122">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="e4f37-123">Il chiamante è responsabile dell'eliminazione delle tavolozze.</span><span class="sxs-lookup"><span data-stu-id="e4f37-123">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="e4f37-124">Qualsiasi thread può chiamare in modo sicuro questo metodo, non solo il thread proprietario della finestra.</span><span class="sxs-lookup"><span data-stu-id="e4f37-124">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="e4f37-125">La finestra Invia un messaggio privato a se stesso, che attiva una chiamata al metodo [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f37-125">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f37-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4f37-126">Requirements</span></span>

| <span data-ttu-id="e4f37-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4f37-127">Requirement</span></span> | <span data-ttu-id="e4f37-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e4f37-128">Value</span></span> |
|-|-|
| <span data-ttu-id="e4f37-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4f37-129">Header</span></span> | <span data-ttu-id="e4f37-130">WinUtil. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="e4f37-130">Winutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="e4f37-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="e4f37-131">Library</span></span>| <span data-ttu-id="e4f37-132">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="e4f37-132">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e4f37-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4f37-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f37-134">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="e4f37-134">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




