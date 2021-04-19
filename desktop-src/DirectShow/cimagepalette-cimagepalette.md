---
description: Metodo del costruttore.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Costruttore CImagePalette. CImagePalette (Winutil. h)
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
ms.openlocfilehash: 38b5766617e1d17fa3917048c2fb845b5194cc42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332273"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="6104c-103">Costruttore CImagePalette. CImagePalette</span><span class="sxs-lookup"><span data-stu-id="6104c-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="6104c-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="6104c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6104c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6104c-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="6104c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6104c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6104c-107">*pBaseFilter*</span><span class="sxs-lookup"><span data-stu-id="6104c-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="6104c-108">Puntatore al filtro proprietario.</span><span class="sxs-lookup"><span data-stu-id="6104c-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="6104c-109">*pBaseWindow*</span><span class="sxs-lookup"><span data-stu-id="6104c-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="6104c-110">Puntatore a un oggetto **CBaseWindow** , che gestisce la finestra in cui viene realizzata la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="6104c-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="6104c-111">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6104c-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6104c-112">*pDrawImage*</span><span class="sxs-lookup"><span data-stu-id="6104c-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="6104c-113">Puntatore a un oggetto **CDrawImage** , che consente di disegnare l'immagine del video.</span><span class="sxs-lookup"><span data-stu-id="6104c-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="6104c-114">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6104c-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6104c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6104c-115">Requirements</span></span>



| <span data-ttu-id="6104c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6104c-116">Requirement</span></span> | <span data-ttu-id="6104c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6104c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6104c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6104c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6104c-119"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6104c-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6104c-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="6104c-120">Library</span></span><br/> | <dl> <span data-ttu-id="6104c-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6104c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6104c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6104c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6104c-123">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="6104c-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




