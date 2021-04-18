---
description: 'Il metodo getCapabilities recupera tutte le funzionalità di ricerca del flusso. Questo metodo implementa il metodo IMediaSeeking:: GetCapabilities.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Metodo CSourceSeeking. GetCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda23944fd039576bb5de74fbb7c32e375415670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329513"
---
# <a name="csourceseekinggetcapabilities-method"></a><span data-ttu-id="e9828-104">Metodo CSourceSeeking. GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="e9828-104">CSourceSeeking.GetCapabilities method</span></span>

<span data-ttu-id="e9828-105">Il `GetCapabilities` metodo recupera tutte le funzionalità di ricerca del flusso.</span><span class="sxs-lookup"><span data-stu-id="e9828-105">The `GetCapabilities` method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="e9828-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="e9828-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9828-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9828-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="e9828-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9828-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9828-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="e9828-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="e9828-110">Puntatore a una variabile che riceve una combinazione bit per bit dei flag di ricerca delle [**\_ \_ \_ funzionalità di ricerca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="e9828-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9828-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9828-111">Return value</span></span>

<span data-ttu-id="e9828-112">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e9828-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="e9828-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e9828-113">Return code</span></span>                                                                               | <span data-ttu-id="e9828-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9828-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="e9828-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e9828-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="e9828-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="e9828-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="e9828-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="e9828-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="e9828-118">Valore del puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="e9828-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e9828-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9828-119">Remarks</span></span>

<span data-ttu-id="e9828-120">Le funzionalità di ricerca sono specificate dalla variabile membro [**CSourceSeeking:: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="e9828-120">The seeking capabilities are specified by the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9828-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9828-121">Requirements</span></span>



| <span data-ttu-id="e9828-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9828-122">Requirement</span></span> | <span data-ttu-id="e9828-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e9828-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9828-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9828-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e9828-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9828-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9828-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9828-126">Library</span></span><br/> | <dl> <span data-ttu-id="e9828-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e9828-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9828-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9828-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9828-129">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="e9828-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




