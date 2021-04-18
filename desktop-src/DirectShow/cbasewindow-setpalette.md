---
description: Il metodo setavolozza installa una tavolozza per la finestra.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Metodo CBaseWindow. setavolozze (Winutil. h)
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
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325757"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a><span data-ttu-id="ca132-103">Metodo CBaseWindow. setavolozze (Winutil. h)</span><span class="sxs-lookup"><span data-stu-id="ca132-103">CBaseWindow.SetPalette method (Winutil.h)</span></span>

<span data-ttu-id="ca132-104">Il `SetPalette` metodo installa una tavolozza per la finestra.</span><span class="sxs-lookup"><span data-stu-id="ca132-104">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca132-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca132-105">Syntax</span></span>


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a><span data-ttu-id="ca132-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca132-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca132-107">*hPalette*</span><span class="sxs-lookup"><span data-stu-id="ca132-107">*hPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="ca132-108">Handle per la nuova tavolozza.</span><span class="sxs-lookup"><span data-stu-id="ca132-108">Handle to the new palette.</span></span> <span data-ttu-id="ca132-109">Non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="ca132-109">Cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca132-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca132-110">Return value</span></span>

<span data-ttu-id="ca132-111">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ca132-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ca132-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ca132-112">Return code</span></span>                                                                             | <span data-ttu-id="ca132-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca132-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="ca132-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ca132-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ca132-115">Una chiamata interna a **GDIFlush** ha restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="ca132-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="ca132-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca132-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ca132-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ca132-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="ca132-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca132-118">Remarks</span></span>

<span data-ttu-id="ca132-119">Se il valore della variabile membro [**\_ BNoRealize di CBaseWindow:: m**](cbasewindow-m-bnorealize.md) è **false** (impostazione predefinita), questo metodo seleziona la tavolozza e la realizza.</span><span class="sxs-lookup"><span data-stu-id="ca132-119">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="ca132-120">In caso contrario, seleziona la tavolozza, ma non la realizza.</span><span class="sxs-lookup"><span data-stu-id="ca132-120">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="ca132-121">L'oggetto non elimina le tavolozze precedenti utilizzate.</span><span class="sxs-lookup"><span data-stu-id="ca132-121">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="ca132-122">Il chiamante è responsabile dell'eliminazione delle tavolozze.</span><span class="sxs-lookup"><span data-stu-id="ca132-122">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="ca132-123">Qualsiasi thread può chiamare in modo sicuro questo metodo, non solo il thread proprietario della finestra.</span><span class="sxs-lookup"><span data-stu-id="ca132-123">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="ca132-124">La finestra Invia un messaggio privato a se stesso, che attiva una chiamata al metodo [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .</span><span class="sxs-lookup"><span data-stu-id="ca132-124">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca132-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca132-125">Requirements</span></span>



| <span data-ttu-id="ca132-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca132-126">Requirement</span></span> | <span data-ttu-id="ca132-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ca132-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca132-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca132-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ca132-129"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca132-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ca132-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca132-130">Library</span></span><br/> | <dl> <span data-ttu-id="ca132-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ca132-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca132-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca132-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca132-133">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="ca132-133">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




