---
description: La funzione CheckVideoInfoType controlla un tipo di supporto che contiene una struttura di formato VIDEOINFOHEADER per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: Funzione CheckVideoInfoType (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 7c3a3c9603f974458ed3012dc651815abd432645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329777"
---
# <a name="checkvideoinfotype-function"></a><span data-ttu-id="583ac-103">CheckVideoInfoType (funzione)</span><span class="sxs-lookup"><span data-stu-id="583ac-103">CheckVideoInfoType function</span></span>

<span data-ttu-id="583ac-104">La `CheckVideoInfoType` funzione controlla un tipo di supporto che contiene una struttura di formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.</span><span class="sxs-lookup"><span data-stu-id="583ac-104">The `CheckVideoInfoType` function checks a media type that contains a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="583ac-105">Questa funzione non garantisce che il tipo di supporto sia valido o che il codice che utilizza la struttura sia protetto.</span><span class="sxs-lookup"><span data-stu-id="583ac-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="583ac-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="583ac-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="583ac-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="583ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="583ac-108">*PMT*</span><span class="sxs-lookup"><span data-stu-id="583ac-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="583ac-109">Puntatore alla struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) da convalidare</span><span class="sxs-lookup"><span data-stu-id="583ac-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="583ac-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="583ac-110">Return value</span></span>

<span data-ttu-id="583ac-111">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="583ac-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="583ac-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="583ac-112">Return code</span></span>                                                                                                | <span data-ttu-id="583ac-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="583ac-113">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="583ac-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="583ac-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="583ac-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="583ac-115">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="583ac-116"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="583ac-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="583ac-117">Valore del puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="583ac-117">**NULL** pointer value.</span></span><br/> |
| <dl> <span data-ttu-id="583ac-118"><dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt></span><span class="sxs-lookup"><span data-stu-id="583ac-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="583ac-119">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="583ac-119">Invalid media type.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="583ac-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="583ac-120">Remarks</span></span>

<span data-ttu-id="583ac-121">Questa funzione chiama [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) per convalidare la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="583ac-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="583ac-122">Se il tipo di formato non è FORMAT \_ videoinfo, la funzione restituisce il \_ tipo VFW E non è \_ \_ \_ accettato.</span><span class="sxs-lookup"><span data-stu-id="583ac-122">If the format type is not FORMAT\_VideoInfo, the function returns VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="583ac-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="583ac-123">Requirements</span></span>



| <span data-ttu-id="583ac-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="583ac-124">Requirement</span></span> | <span data-ttu-id="583ac-125">Valore</span><span class="sxs-lookup"><span data-stu-id="583ac-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="583ac-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="583ac-126">Header</span></span><br/> | <dl> <span data-ttu-id="583ac-127"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="583ac-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="583ac-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="583ac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="583ac-129">Funzioni video e immagine</span><span class="sxs-lookup"><span data-stu-id="583ac-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




