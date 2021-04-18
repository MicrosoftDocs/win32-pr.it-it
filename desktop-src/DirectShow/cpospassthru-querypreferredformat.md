---
description: 'Il metodo QueryPreferredFormat Recupera il formato di ora preferito per il flusso. Questo metodo implementa il metodo IMediaSeeking:: QueryPreferredFormat.'
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: Metodo CPosPassThru. QueryPreferredFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c22348a10e8b9e5f241e06252c025e2ec9593486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328252"
---
# <a name="cpospassthruquerypreferredformat-method"></a><span data-ttu-id="7f9e2-104">CPosPassThru. QueryPreferredFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="7f9e2-104">CPosPassThru.QueryPreferredFormat method</span></span>

<span data-ttu-id="7f9e2-105">Il `QueryPreferredFormat` metodo recupera il formato di ora preferito per il flusso.</span><span class="sxs-lookup"><span data-stu-id="7f9e2-105">The `QueryPreferredFormat` method retrieves the preferred time format for the stream.</span></span> <span data-ttu-id="7f9e2-106">Questo metodo implementa il metodo [**IMediaSeeking:: QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .</span><span class="sxs-lookup"><span data-stu-id="7f9e2-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9e2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f9e2-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="7f9e2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f9e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f9e2-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="7f9e2-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="7f9e2-110">Puntatore a una variabile che riceve un GUID del formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="7f9e2-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f9e2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f9e2-111">Return value</span></span>

<span data-ttu-id="7f9e2-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="7f9e2-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f9e2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f9e2-113">Requirements</span></span>



| <span data-ttu-id="7f9e2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f9e2-114">Requirement</span></span> | <span data-ttu-id="7f9e2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7f9e2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f9e2-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f9e2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7f9e2-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f9e2-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f9e2-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="7f9e2-118">Library</span></span><br/> | <dl> <span data-ttu-id="7f9e2-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7f9e2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f9e2-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f9e2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f9e2-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="7f9e2-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="7f9e2-122">**GUID del formato dell'ora**</span><span class="sxs-lookup"><span data-stu-id="7f9e2-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




