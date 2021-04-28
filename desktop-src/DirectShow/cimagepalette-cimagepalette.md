---
description: 'Costruttore CImagePalette.CImagePalette : metodo costruttore.'
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Costruttore CImagePalette.CImagePalette (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5021b165a8fa47bedc7961657d7cdbfa07af301d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085679"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="23d9a-103">Costruttore CImagePalette.CImagePalette</span><span class="sxs-lookup"><span data-stu-id="23d9a-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="23d9a-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="23d9a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="23d9a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23d9a-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="23d9a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23d9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23d9a-107">*pBaseFilter*</span><span class="sxs-lookup"><span data-stu-id="23d9a-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="23d9a-108">Puntatore al filtro proprietario.</span><span class="sxs-lookup"><span data-stu-id="23d9a-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="23d9a-109">*pBaseWindow*</span><span class="sxs-lookup"><span data-stu-id="23d9a-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="23d9a-110">Puntatore a un **oggetto CBaseWindow,** che gestisce la finestra in cui viene realizzata la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="23d9a-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="23d9a-111">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="23d9a-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="23d9a-112">*pDrawImage*</span><span class="sxs-lookup"><span data-stu-id="23d9a-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="23d9a-113">Puntatore a un **oggetto CDrawImage,** che disegna l'immagine video.</span><span class="sxs-lookup"><span data-stu-id="23d9a-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="23d9a-114">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="23d9a-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23d9a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23d9a-115">Requirements</span></span>



| <span data-ttu-id="23d9a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="23d9a-116">Requirement</span></span> | <span data-ttu-id="23d9a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="23d9a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23d9a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23d9a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="23d9a-119"><dt>Winutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="23d9a-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="23d9a-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="23d9a-120">Library</span></span><br/> | <dl> <span data-ttu-id="23d9a-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="23d9a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23d9a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23d9a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23d9a-123">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="23d9a-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




