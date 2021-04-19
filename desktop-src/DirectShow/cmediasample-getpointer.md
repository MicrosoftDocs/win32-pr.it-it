---
description: 'Il metodo getpointer recupera un puntatore di lettura/scrittura nel buffer. Questo metodo implementa il metodo IMediaSample:: getpointer.'
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Metodo CMediaSample. getpointer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe8d8785bd52fbe601d9980f8fc146a2c6f41e40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326560"
---
# <a name="cmediasamplegetpointer-method"></a><span data-ttu-id="8dec0-104">Metodo CMediaSample. getpointer</span><span class="sxs-lookup"><span data-stu-id="8dec0-104">CMediaSample.GetPointer method</span></span>

<span data-ttu-id="8dec0-105">Il `GetPointer` metodo recupera un puntatore di lettura/scrittura nel buffer.</span><span class="sxs-lookup"><span data-stu-id="8dec0-105">The `GetPointer` method retrieves a read/write pointer to the buffer.</span></span> <span data-ttu-id="8dec0-106">Questo metodo implementa il metodo [**IMediaSample:: Getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) .</span><span class="sxs-lookup"><span data-stu-id="8dec0-106">This method implements the [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dec0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8dec0-107">Syntax</span></span>


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="8dec0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8dec0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dec0-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="8dec0-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="8dec0-110">Indirizzo di una variabile che riceve un puntatore al buffer.</span><span class="sxs-lookup"><span data-stu-id="8dec0-110">Address of a variable that receives a pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dec0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8dec0-111">Return value</span></span>

<span data-ttu-id="8dec0-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8dec0-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dec0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8dec0-113">Requirements</span></span>



| <span data-ttu-id="8dec0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dec0-114">Requirement</span></span> | <span data-ttu-id="8dec0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8dec0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dec0-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8dec0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8dec0-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8dec0-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8dec0-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="8dec0-118">Library</span></span><br/> | <dl> <span data-ttu-id="8dec0-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8dec0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dec0-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8dec0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dec0-121">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="8dec0-121">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




