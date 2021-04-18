---
description: Il metodo GetDisplayFormat recupera un formato video che descrive la modalità di visualizzazione corrente.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: Metodo CImageDisplay. GetDisplayFormat (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901d61f3597156853b0f2d6f93b43c3cf99ec5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331184"
---
# <a name="cimagedisplaygetdisplayformat-method"></a><span data-ttu-id="bc588-103">CImageDisplay. GetDisplayFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="bc588-103">CImageDisplay.GetDisplayFormat method</span></span>

<span data-ttu-id="bc588-104">Il `GetDisplayFormat` metodo recupera un formato video che descrive la modalità di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="bc588-104">The `GetDisplayFormat` method retrieves a video format that describes the current display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc588-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc588-105">Syntax</span></span>


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a><span data-ttu-id="bc588-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc588-106">Parameters</span></span>

<span data-ttu-id="bc588-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bc588-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc588-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc588-108">Return value</span></span>

<span data-ttu-id="bc588-109">Restituisce un puntatore a una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="bc588-109">Returns a pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc588-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc588-110">Requirements</span></span>



| <span data-ttu-id="bc588-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc588-111">Requirement</span></span> | <span data-ttu-id="bc588-112">Valore</span><span class="sxs-lookup"><span data-stu-id="bc588-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc588-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc588-113">Header</span></span><br/>  | <dl> <span data-ttu-id="bc588-114"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc588-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bc588-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="bc588-115">Library</span></span><br/> | <dl> <span data-ttu-id="bc588-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bc588-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc588-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc588-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc588-118">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="bc588-118">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




