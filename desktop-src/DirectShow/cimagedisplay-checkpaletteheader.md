---
description: Il metodo CheckPaletteHeader convalida le voci della tavolozza in una struttura VIDEOINFO.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Metodo CImageDisplay. CheckPaletteHeader (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331643"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a><span data-ttu-id="11c36-103">CImageDisplay. CheckPaletteHeader, metodo</span><span class="sxs-lookup"><span data-stu-id="11c36-103">CImageDisplay.CheckPaletteHeader method</span></span>

<span data-ttu-id="11c36-104">Il `CheckPaletteHeader` metodo convalida le voci della tavolozza in una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="11c36-104">The `CheckPaletteHeader` method validates the palette entries in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c36-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11c36-105">Syntax</span></span>


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="11c36-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="11c36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c36-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="11c36-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="11c36-108">Puntatore a una struttura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="11c36-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11c36-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11c36-109">Return value</span></span>

<span data-ttu-id="11c36-110">Restituisce **true** se le voci della tavolozza sono valide o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="11c36-110">Returns **TRUE** if the palette entries are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="11c36-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="11c36-111">Remarks</span></span>

<span data-ttu-id="11c36-112">Se il formato dell'immagine non è pallettizzati, il metodo verifica che **biClrUsed** sia uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="11c36-112">If the image format is not palettized, the method verifies that **biClrUsed** equals zero.</span></span> <span data-ttu-id="11c36-113">In caso contrario, il metodo verifica che il flag di **bicompressione** sia bi \_ RGB; **biClrImportant** non è maggiore di **biClrUsed**; il numero di voci della tavolozza non supera il valore massimo, in base alla profondità del colore.</span><span class="sxs-lookup"><span data-stu-id="11c36-113">Otherwise, the method verifies that the **biCompression** flag is BI\_RGB; **biClrImportant** is not greater than **biClrUsed**; and the number of palette entries does not exceed the maximum, given the color depth.</span></span>

## <a name="requirements"></a><span data-ttu-id="11c36-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11c36-114">Requirements</span></span>



| <span data-ttu-id="11c36-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="11c36-115">Requirement</span></span> | <span data-ttu-id="11c36-116">Valore</span><span class="sxs-lookup"><span data-stu-id="11c36-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c36-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11c36-117">Header</span></span><br/>  | <dl> <span data-ttu-id="11c36-118"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11c36-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="11c36-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="11c36-119">Library</span></span><br/> | <dl> <span data-ttu-id="11c36-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="11c36-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11c36-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11c36-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c36-122">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="11c36-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




