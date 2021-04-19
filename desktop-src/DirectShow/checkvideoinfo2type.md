---
description: La funzione CheckVideoInfo2Type controlla un tipo di supporto che contiene una struttura di formato VIDEOINFOHEADER2 per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: Funzione CheckVideoInfo2Type (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 5ec092bdea1e3dd00de36893d1816f70ca6d7945
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329778"
---
# <a name="checkvideoinfo2type-function"></a><span data-ttu-id="fee2e-103">CheckVideoInfo2Type (funzione)</span><span class="sxs-lookup"><span data-stu-id="fee2e-103">CheckVideoInfo2Type function</span></span>

<span data-ttu-id="fee2e-104">La `CheckVideoInfo2Type` funzione controlla un tipo di supporto che contiene una struttura di formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.</span><span class="sxs-lookup"><span data-stu-id="fee2e-104">The `CheckVideoInfo2Type` function checks a media type that contains a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="fee2e-105">Questa funzione non garantisce che il tipo di supporto sia valido o che il codice che utilizza la struttura sia protetto.</span><span class="sxs-lookup"><span data-stu-id="fee2e-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fee2e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fee2e-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="fee2e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fee2e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fee2e-108">*PMT*</span><span class="sxs-lookup"><span data-stu-id="fee2e-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="fee2e-109">Puntatore alla struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) da convalidare.</span><span class="sxs-lookup"><span data-stu-id="fee2e-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fee2e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fee2e-110">Return value</span></span>

<span data-ttu-id="fee2e-111">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fee2e-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="fee2e-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fee2e-112">Return code</span></span>                                                                                                | <span data-ttu-id="fee2e-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fee2e-113">Description</span></span>                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="fee2e-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fee2e-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="fee2e-115">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="fee2e-115">Success</span></span><br/>                |
| <dl> <span data-ttu-id="fee2e-116"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="fee2e-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="fee2e-117">Valore del puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="fee2e-117">**NULL** pointer value</span></span><br/> |
| <dl> <span data-ttu-id="fee2e-118"><dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt></span><span class="sxs-lookup"><span data-stu-id="fee2e-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="fee2e-119">Tipo di supporto non valido</span><span class="sxs-lookup"><span data-stu-id="fee2e-119">Invalid media type</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="fee2e-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="fee2e-120">Remarks</span></span>

<span data-ttu-id="fee2e-121">Questa funzione chiama [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) per convalidare la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="fee2e-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="fee2e-122">Se il tipo di formato non è **Format \_ VideoInfo2**, la funzione restituisce il **\_ tipo VFW E non è \_ \_ \_ accettato**.</span><span class="sxs-lookup"><span data-stu-id="fee2e-122">If the format type is not **FORMAT\_VideoInfo2**, the function returns **VFW\_E\_TYPE\_NOT\_ACCEPTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fee2e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fee2e-123">Requirements</span></span>



| <span data-ttu-id="fee2e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fee2e-124">Requirement</span></span> | <span data-ttu-id="fee2e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fee2e-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fee2e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fee2e-126">Header</span></span><br/> | <dl> <span data-ttu-id="fee2e-127"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fee2e-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fee2e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fee2e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee2e-129">Funzioni video e immagine</span><span class="sxs-lookup"><span data-stu-id="fee2e-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




