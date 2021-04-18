---
description: Il metodo DoRealisePalette realizza la tavolozza corrente della finestra.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Metodo CBaseWindow. DoRealisePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325331"
---
# <a name="cbasewindowdorealisepalette-method"></a><span data-ttu-id="1a0a1-103">CBaseWindow. DoRealisePalette, metodo</span><span class="sxs-lookup"><span data-stu-id="1a0a1-103">CBaseWindow.DoRealisePalette method</span></span>

<span data-ttu-id="1a0a1-104">Il `DoRealisePalette` Metodo realizza la tavolozza corrente della finestra.</span><span class="sxs-lookup"><span data-stu-id="1a0a1-104">The `DoRealisePalette` method realizes the window's current palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a0a1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a0a1-105">Syntax</span></span>


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a><span data-ttu-id="1a0a1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a0a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a0a1-107">*bForceBackground*</span><span class="sxs-lookup"><span data-stu-id="1a0a1-107">*bForceBackground*</span></span> 
</dt> <dd>

<span data-ttu-id="1a0a1-108">Valore booleano che specifica se la tavolozza è forzato a essere una tavolozza di sfondo.</span><span class="sxs-lookup"><span data-stu-id="1a0a1-108">Boolean value that specifies whether the palette is forced to be a background palette.</span></span> <span data-ttu-id="1a0a1-109">Per ulteriori informazioni, vedere **SelectPalette** in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="1a0a1-109">For more information, see **SelectPalette** in the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a0a1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a0a1-110">Return value</span></span>

<span data-ttu-id="1a0a1-111">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1a0a1-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="1a0a1-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1a0a1-112">Return code</span></span>                                                                             | <span data-ttu-id="1a0a1-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a0a1-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="1a0a1-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1a0a1-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="1a0a1-115">Una chiamata interna a **GDIFlush** ha restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="1a0a1-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="1a0a1-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1a0a1-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="1a0a1-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1a0a1-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="1a0a1-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a0a1-118">Remarks</span></span>

<span data-ttu-id="1a0a1-119">Il metodo [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="1a0a1-119">The [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method calls this method.</span></span> <span data-ttu-id="1a0a1-120">Per impostare una nuova tavolozza, chiamare il metodo [**CBaseWindow:: sepalette**](cbasewindow-setpalette.md) .</span><span class="sxs-lookup"><span data-stu-id="1a0a1-120">To set a new palette, call the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a0a1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a0a1-121">Requirements</span></span>



| <span data-ttu-id="1a0a1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a0a1-122">Requirement</span></span> | <span data-ttu-id="1a0a1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1a0a1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a0a1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a0a1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1a0a1-125"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a0a1-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1a0a1-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="1a0a1-126">Library</span></span><br/> | <dl> <span data-ttu-id="1a0a1-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1a0a1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a0a1-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a0a1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a0a1-129">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="1a0a1-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




