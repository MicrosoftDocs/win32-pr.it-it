---
description: 'Metodo CPosPassThru.GetCapabilities: il metodo GetCapabilities recupera tutte le funzionalità di ricerca del flusso. Questo metodo implementa il metodo IMediaSeeking::GetCapabilities.'
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: Metodo CPosPassThru.GetCapabilities (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c21838d3df72d52255d0a2e35dd0b7d34ef55411
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085569"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="e4176-104">Metodo CPosPassThru.GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="e4176-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="e4176-105">Il **metodo GetCapabilities** recupera tutte le funzionalità di ricerca del flusso.</span><span class="sxs-lookup"><span data-stu-id="e4176-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="e4176-106">Questo metodo implementa il [**metodo IMediaSeeking::GetCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities)</span><span class="sxs-lookup"><span data-stu-id="e4176-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4176-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4176-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="e4176-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4176-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4176-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="e4176-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="e4176-110">Puntatore a una variabile che riceve una combinazione bit per bit di [**flag AM \_ \_ SEEKING SEEKING \_ CAPABILITIES.**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities)</span><span class="sxs-lookup"><span data-stu-id="e4176-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4176-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4176-111">Return value</span></span>

<span data-ttu-id="e4176-112">Restituisce il **valore HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="e4176-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4176-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4176-113">Requirements</span></span>



| <span data-ttu-id="e4176-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4176-114">Requirement</span></span> | <span data-ttu-id="e4176-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e4176-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4176-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4176-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e4176-117"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4176-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e4176-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="e4176-118">Library</span></span><br/> | <dl> <span data-ttu-id="e4176-119"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e4176-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4176-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4176-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4176-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="e4176-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




