---
description: Il metodo getmascheres recupera le maschere dei colori per un formato VIDEOINFO specificato.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Metodo CImageDisplay. getmascherations (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333076"
---
# <a name="cimagedisplaygetbitmasks-method"></a><span data-ttu-id="eaa4f-103">Metodo CImageDisplay. getmascherations</span><span class="sxs-lookup"><span data-stu-id="eaa4f-103">CImageDisplay.GetBitMasks method</span></span>

<span data-ttu-id="eaa4f-104">Il `GetBitMasks` metodo recupera le maschere dei colori per un formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) specificato.</span><span class="sxs-lookup"><span data-stu-id="eaa4f-104">The `GetBitMasks` method retrieves the color masks for a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaa4f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eaa4f-105">Syntax</span></span>


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="eaa4f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eaa4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa4f-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="eaa4f-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="eaa4f-108">Puntatore alla struttura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="eaa4f-108">Pointer to the **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaa4f-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eaa4f-109">Return value</span></span>

<span data-ttu-id="eaa4f-110">Restituisce una matrice di tre valori **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="eaa4f-110">Returns an array of three **DWORD** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaa4f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="eaa4f-111">Remarks</span></span>

<span data-ttu-id="eaa4f-112">Se il membro di **biCompression** è bi \_ campi, il metodo restituisce un puntatore alle maschere dei colori fornite nel membro **dwBitMasks** .</span><span class="sxs-lookup"><span data-stu-id="eaa4f-112">If the **biCompression** member is BI\_BITFIELDS, the method returns a pointer to the color masks that are supplied in the **dwBitMasks** member.</span></span> <span data-ttu-id="eaa4f-113">Se il membro di **biCompression** è bi \_ RGB, il metodo restituisce le maschere dei colori che corrispondono alla profondità del bit.</span><span class="sxs-lookup"><span data-stu-id="eaa4f-113">If the **biCompression** member is BI\_RGB, the method returns the color masks that correspond to the bit depth.</span></span> <span data-ttu-id="eaa4f-114">Se il metodo ha esito negativo, ad esempio se la profondità del bit è inferiore a 16, il metodo restituisce la matrice {0,0,0} .</span><span class="sxs-lookup"><span data-stu-id="eaa4f-114">If the method fails (for example, the bit depth is less than 16), the method returns the array {0,0,0}.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa4f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eaa4f-115">Requirements</span></span>



| <span data-ttu-id="eaa4f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaa4f-116">Requirement</span></span> | <span data-ttu-id="eaa4f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="eaa4f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa4f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eaa4f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="eaa4f-119"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eaa4f-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eaa4f-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="eaa4f-120">Library</span></span><br/> | <dl> <span data-ttu-id="eaa4f-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eaa4f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaa4f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eaa4f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaa4f-123">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="eaa4f-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




