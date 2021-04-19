---
description: 'Il metodo GetPreroll recupera la quantità di dati che verranno accodati prima della posizione iniziale. Questo metodo implementa il metodo IMediaSeeking:: GetPreroll.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Metodo CPosPassThru. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329756"
---
# <a name="cpospassthrugetpreroll-method"></a><span data-ttu-id="0c5a0-104">CPosPassThru. GetPreroll, metodo</span><span class="sxs-lookup"><span data-stu-id="0c5a0-104">CPosPassThru.GetPreroll method</span></span>

<span data-ttu-id="0c5a0-105">Il `GetPreroll` metodo recupera la quantità di dati che verranno accodati prima della posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="0c5a0-105">The `GetPreroll` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="0c5a0-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .</span><span class="sxs-lookup"><span data-stu-id="0c5a0-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c5a0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c5a0-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="0c5a0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c5a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c5a0-109">*pllPreroll*</span><span class="sxs-lookup"><span data-stu-id="0c5a0-109">*pllPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="0c5a0-110">Puntatore a una variabile che riceve l'ora di preregistrazione, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="0c5a0-110">Pointer to a variable that receives the preroll time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c5a0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c5a0-111">Return value</span></span>

<span data-ttu-id="0c5a0-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="0c5a0-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c5a0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c5a0-113">Requirements</span></span>



| <span data-ttu-id="0c5a0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c5a0-114">Requirement</span></span> | <span data-ttu-id="0c5a0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0c5a0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c5a0-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c5a0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0c5a0-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c5a0-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0c5a0-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="0c5a0-118">Library</span></span><br/> | <dl> <span data-ttu-id="0c5a0-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0c5a0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c5a0-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c5a0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c5a0-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="0c5a0-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




