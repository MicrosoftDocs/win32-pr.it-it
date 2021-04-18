---
description: Il metodo SetDIBData specifica informazioni sulla bitmap indipendente dal dispositivo (DIB) GDI gestita da questo oggetto. Chiamare questo metodo per inizializzare l'oggetto CImageSample.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Metodo CImageSample. SetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325048"
---
# <a name="cimagesamplesetdibdata-method"></a><span data-ttu-id="85bff-104">CImageSample. SetDIBData, metodo</span><span class="sxs-lookup"><span data-stu-id="85bff-104">CImageSample.SetDIBData method</span></span>

<span data-ttu-id="85bff-105">Il `SetDIBData` metodo specifica informazioni sulla bitmap indipendente dal dispositivo (DIB) GDI gestita da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="85bff-105">The `SetDIBData` method specifies information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span> <span data-ttu-id="85bff-106">Chiamare questo metodo per inizializzare l'oggetto **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="85bff-106">Call this method to initialize the **CImageSample** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="85bff-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85bff-107">Syntax</span></span>


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a><span data-ttu-id="85bff-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="85bff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85bff-109">*pDibData*</span><span class="sxs-lookup"><span data-stu-id="85bff-109">*pDibData*</span></span> 
</dt> <dd>

<span data-ttu-id="85bff-110">Puntatore a una struttura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="85bff-110">Pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85bff-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85bff-111">Return value</span></span>

<span data-ttu-id="85bff-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="85bff-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="85bff-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85bff-113">Requirements</span></span>



| <span data-ttu-id="85bff-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="85bff-114">Requirement</span></span> | <span data-ttu-id="85bff-115">Valore</span><span class="sxs-lookup"><span data-stu-id="85bff-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85bff-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85bff-116">Header</span></span><br/>  | <dl> <span data-ttu-id="85bff-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85bff-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85bff-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="85bff-118">Library</span></span><br/> | <dl> <span data-ttu-id="85bff-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="85bff-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85bff-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85bff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85bff-121">**Classe CImageSample**</span><span class="sxs-lookup"><span data-stu-id="85bff-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




