---
description: 'Metodo CPosPassThru.GetDuration: il metodo GetDuration recupera la durata del flusso. Questo metodo implementa il metodo IMediaSeeking::GetDuration.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Metodo CPosPassThru.GetDuration (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b0af7bfaca405ed52a4e3c5a63c18b4bc087ba3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085579"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="b7723-104">Metodo CPosPassThru.GetDuration</span><span class="sxs-lookup"><span data-stu-id="b7723-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="b7723-105">Il `GetDuration` metodo recupera la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="b7723-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="b7723-106">Questo metodo implementa il [**metodo IMediaSeeking::GetDuration.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)</span><span class="sxs-lookup"><span data-stu-id="b7723-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7723-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7723-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="b7723-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7723-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7723-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="b7723-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="b7723-110">Puntatore a una variabile che riceve la durata, in unità del formato di ora corrente.</span><span class="sxs-lookup"><span data-stu-id="b7723-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7723-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7723-111">Return value</span></span>

<span data-ttu-id="b7723-112">Restituisce il **valore HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="b7723-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7723-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7723-113">Requirements</span></span>



| <span data-ttu-id="b7723-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7723-114">Requirement</span></span> | <span data-ttu-id="b7723-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b7723-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7723-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7723-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b7723-117"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7723-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b7723-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7723-118">Library</span></span><br/> | <dl> <span data-ttu-id="b7723-119"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b7723-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7723-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7723-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7723-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="b7723-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




