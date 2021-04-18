---
description: Il metodo GetDIBData recupera le informazioni sulla bitmap indipendente dal dispositivo (DIB) GDI gestita da questo oggetto.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Metodo CImageSample. GetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325055"
---
# <a name="cimagesamplegetdibdata-method"></a><span data-ttu-id="700c6-103">CImageSample. GetDIBData, metodo</span><span class="sxs-lookup"><span data-stu-id="700c6-103">CImageSample.GetDIBData method</span></span>

<span data-ttu-id="700c6-104">Il `GetDIBData` metodo recupera le informazioni sulla bitmap indipendente dal dispositivo (DIB) GDI gestita da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="700c6-104">The `GetDIBData` method retrieves information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span>

## <a name="syntax"></a><span data-ttu-id="700c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="700c6-105">Syntax</span></span>


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a><span data-ttu-id="700c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="700c6-106">Parameters</span></span>

<span data-ttu-id="700c6-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="700c6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="700c6-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="700c6-108">Return value</span></span>

<span data-ttu-id="700c6-109">Restituisce un puntatore a una struttura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="700c6-109">Returns a pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="700c6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="700c6-110">Remarks</span></span>

<span data-ttu-id="700c6-111">Il chiamante deve inizializzare la struttura **DIBDATA** prima di chiamare questo metodo. verificare il valore di **CImageSample:: m \_ Binit**.</span><span class="sxs-lookup"><span data-stu-id="700c6-111">The caller must initialize the **DIBDATA** structure before calling this method; check the value of **CImageSample::m\_bInit**.</span></span> <span data-ttu-id="700c6-112">Per inizializzare la struttura, chiamare il metodo [**CImageSample:: SetDIBData**](cimagesample-setdibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="700c6-112">To initialize the structure, call the [**CImageSample::SetDIBData**](cimagesample-setdibdata.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="700c6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="700c6-113">Requirements</span></span>



| <span data-ttu-id="700c6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="700c6-114">Requirement</span></span> | <span data-ttu-id="700c6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="700c6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="700c6-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="700c6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="700c6-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="700c6-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="700c6-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="700c6-118">Library</span></span><br/> | <dl> <span data-ttu-id="700c6-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="700c6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="700c6-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="700c6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700c6-121">**Classe CImageSample**</span><span class="sxs-lookup"><span data-stu-id="700c6-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




