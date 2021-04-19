---
description: Il metodo CopyPalette copia la tavolozza da qualsiasi struttura VIDEOINFO a qualsiasi struttura pallettizzati VIDEOINFO.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Metodo CImagePalette. CopyPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332272"
---
# <a name="cimagepalettecopypalette-method"></a><span data-ttu-id="f3d09-103">CImagePalette. CopyPalette, metodo</span><span class="sxs-lookup"><span data-stu-id="f3d09-103">CImagePalette.CopyPalette method</span></span>

<span data-ttu-id="f3d09-104">Il `CopyPalette` metodo copia la tavolozza da qualsiasi struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) a qualsiasi struttura **VIDEOINFO** di pallettizzati.</span><span class="sxs-lookup"><span data-stu-id="f3d09-104">The `CopyPalette` method copies the palette from any [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure to any palettized **VIDEOINFO** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3d09-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3d09-105">Syntax</span></span>


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a><span data-ttu-id="f3d09-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3d09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3d09-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="f3d09-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="f3d09-108">Puntatore al tipo di supporto di origine.</span><span class="sxs-lookup"><span data-stu-id="f3d09-108">Pointer to the source media type.</span></span>

</dd> <dt>

<span data-ttu-id="f3d09-109">*pDest*</span><span class="sxs-lookup"><span data-stu-id="f3d09-109">*pDest*</span></span> 
</dt> <dd>

<span data-ttu-id="f3d09-110">Puntatore al tipo di supporto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f3d09-110">Pointer to the destination media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3d09-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3d09-111">Return value</span></span>

<span data-ttu-id="f3d09-112">Restituisce \_ OK se la tavolozza è stata copiata.</span><span class="sxs-lookup"><span data-stu-id="f3d09-112">Returns S\_OK if the palette was copied.</span></span> <span data-ttu-id="f3d09-113">Restituisce \_ false se il tipo di supporto di origine o di destinazione non dispone di una tavolozza.</span><span class="sxs-lookup"><span data-stu-id="f3d09-113">Returns S\_FALSE if either the source or destination media type does not have a palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3d09-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3d09-114">Remarks</span></span>

<span data-ttu-id="f3d09-115">Il tipo di supporto *pDest* deve essere un formato pallettizzati con una profondità di colore pari o inferiore a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="f3d09-115">The *pDest* media type must be a palettized format with a color depth of 8 bits or less.</span></span> <span data-ttu-id="f3d09-116">Il tipo di supporto *pSrc* può essere qualsiasi tipo [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con una tavolozza, inclusi i formati YUV e true-color con le voci della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="f3d09-116">The *pSrc* media type can be any [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) type with a palette, including YUV and true-color formats with palette entries.</span></span> <span data-ttu-id="f3d09-117">Il metodo copia le voci della tavolozza da *pSrc* in una nuova tavolozza e connette la nuova tavolozza a *pDest*.</span><span class="sxs-lookup"><span data-stu-id="f3d09-117">The method copies the palette entries from *pSrc* into a new palette, and attaches the new palette to *pDest*.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3d09-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3d09-118">Requirements</span></span>



| <span data-ttu-id="f3d09-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3d09-119">Requirement</span></span> | <span data-ttu-id="f3d09-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f3d09-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d09-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3d09-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f3d09-122"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3d09-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f3d09-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f3d09-123">Library</span></span><br/> | <dl> <span data-ttu-id="f3d09-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f3d09-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3d09-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3d09-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3d09-126">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="f3d09-126">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




