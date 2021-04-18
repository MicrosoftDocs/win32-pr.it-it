---
description: Il metodo CheckHeaderValidity convalida una struttura BITMAPINFOHEADER. Questo metodo è utile solo per i tipi RGB non compressi, non per i tipi compressi o i tipi YUV.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Metodo CImageDisplay. CheckHeaderValidity (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325324"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a><span data-ttu-id="8b95e-104">CImageDisplay. CheckHeaderValidity, metodo</span><span class="sxs-lookup"><span data-stu-id="8b95e-104">CImageDisplay.CheckHeaderValidity method</span></span>

<span data-ttu-id="8b95e-105">Il `CheckHeaderValidity` metodo convalida una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="8b95e-105">The `CheckHeaderValidity` method validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="8b95e-106">Questo metodo è utile solo per i tipi RGB non compressi, non per i tipi compressi o i tipi YUV.</span><span class="sxs-lookup"><span data-stu-id="8b95e-106">This method is useful only for uncompressed RGB types, not for compressed types or YUV types.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b95e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b95e-107">Syntax</span></span>


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="8b95e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b95e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b95e-109">*pInput*</span><span class="sxs-lookup"><span data-stu-id="8b95e-109">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="8b95e-110">Puntatore a una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) contenente la struttura **BITMAPINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="8b95e-110">Pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure containing the **BITMAPINFOHEADER** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b95e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b95e-111">Return value</span></span>

<span data-ttu-id="8b95e-112">Restituisce **true** se **BITMAPINFOHEADER** è valido o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8b95e-112">Returns **TRUE** if the **BITMAPINFOHEADER** is valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b95e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b95e-113">Remarks</span></span>

<span data-ttu-id="8b95e-114">Questo metodo verifica che le dimensioni dell'immagine siano non negative; il tipo di compressione è BI \_ RGB o \_ bi campi; le maschere di colore e profondità sono valide; il membro **Biplanes** è uguale a uno e i membri **bidimensionali** e **biSizeImage** sono corretti.</span><span class="sxs-lookup"><span data-stu-id="8b95e-114">This method checks that the image dimensions are non-negative; the compression type is BI\_RGB or BI\_BITFIELDS; the color depth and color masks are valid; the **biPlanes** member equals one; and the **biSize** and **biSizeImage** members are correct.</span></span> <span data-ttu-id="8b95e-115">Verifica anche la presenza di errori comuni nelle voci della tavolozza, se presenti.</span><span class="sxs-lookup"><span data-stu-id="8b95e-115">It also checks for common errors in the palette entries, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b95e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b95e-116">Requirements</span></span>



| <span data-ttu-id="8b95e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b95e-117">Requirement</span></span> | <span data-ttu-id="8b95e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8b95e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b95e-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b95e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8b95e-120"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b95e-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8b95e-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b95e-121">Library</span></span><br/> | <dl> <span data-ttu-id="8b95e-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8b95e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b95e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b95e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b95e-124">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="8b95e-124">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




