---
description: Il metodo UpdateFormat compila alcuni membri facoltativi della struttura VIDEOINFO.
ms.assetid: 5ca34fa0-eef4-44f5-bbcc-e686e5181d86
title: Metodo CImageDisplay. UpdateFormat (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.UpdateFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6966da171e37e1cc285afc1872d221ca7aad99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328350"
---
# <a name="cimagedisplayupdateformat-method"></a><span data-ttu-id="507f3-103">CImageDisplay. UpdateFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="507f3-103">CImageDisplay.UpdateFormat method</span></span>

<span data-ttu-id="507f3-104">Il `UpdateFormat` metodo compila alcuni membri facoltativi della struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="507f3-104">The `UpdateFormat` method fills in some optional members of the [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="507f3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="507f3-105">Syntax</span></span>


```C++
HRESULT UpdateFormat(
   VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="507f3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="507f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="507f3-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="507f3-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="507f3-108">Puntatore a una struttura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="507f3-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="507f3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="507f3-109">Return value</span></span>

<span data-ttu-id="507f3-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="507f3-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="507f3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="507f3-111">Remarks</span></span>

<span data-ttu-id="507f3-112">Questo metodo imposta i membri **biClrUsed**, **biClrImportant** e **biSizeImage** sui valori corretti e cancella i rettangoli di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="507f3-112">This method sets the **biClrUsed**, **biClrImportant**, and **biSizeImage** members to the correct values, and clears the source and target rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="507f3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="507f3-113">Requirements</span></span>



| <span data-ttu-id="507f3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="507f3-114">Requirement</span></span> | <span data-ttu-id="507f3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="507f3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="507f3-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="507f3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="507f3-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="507f3-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="507f3-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="507f3-118">Library</span></span><br/> | <dl> <span data-ttu-id="507f3-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="507f3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="507f3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="507f3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="507f3-121">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="507f3-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




