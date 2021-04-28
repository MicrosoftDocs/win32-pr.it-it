---
description: 'AM_RATE_ResetOnTimeDisc proprietà : si applica a Windows Vista e versioni successive.'
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e867bff1f344e80ffd06c9c40276515f2cd4920c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096609"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="f0dd5-103">Am \_ RATE \_ ResetOnTimeDisc - proprietà</span><span class="sxs-lookup"><span data-stu-id="f0dd5-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="f0dd5-104">Si applica a Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="f0dd5-105">Questa proprietà esegue una query se il decodificatore risincronizza i timestamp di output nei timestamp di input quando il decodificatore riceve un campione con il flag di discontinuità.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="f0dd5-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-106">This property is read/write.</span></span>



| <span data-ttu-id="f0dd5-107">Label</span><span class="sxs-lookup"><span data-stu-id="f0dd5-107">Label</span></span> | <span data-ttu-id="f0dd5-108">Valore</span><span class="sxs-lookup"><span data-stu-id="f0dd5-108">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="f0dd5-109">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="f0dd5-109">Property Set GUID</span></span> | <span data-ttu-id="f0dd5-110">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="f0dd5-110">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="f0dd5-111">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="f0dd5-111">Property ID</span></span>       | <span data-ttu-id="f0dd5-112">AM \_ RATE \_ ResetOnTimeDisc</span><span class="sxs-lookup"><span data-stu-id="f0dd5-112">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="f0dd5-113">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f0dd5-113">Data Type</span></span>         | <span data-ttu-id="f0dd5-114">**Dword**</span><span class="sxs-lookup"><span data-stu-id="f0dd5-114">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="f0dd5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0dd5-115">Remarks</span></span>

<span data-ttu-id="f0dd5-116">Questa proprietà supporta le modifiche della velocità uniforme.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-116">This property supports smooth rate changes.</span></span> <span data-ttu-id="f0dd5-117">Se il valore di questa proprietà è **TRUE** e il decodificatore riceve un esempio di input con il flag AM \_ SAMPLE TIMEDISCONTINUITY, il frame decodificato deve avere lo stesso timestamp del \_ frame di input.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-117">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="f0dd5-118">Per recuperare il flag AM \_ SAMPLE \_ TIMEDISCONTINUITY, chiamare [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="f0dd5-118">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="f0dd5-119">Il flag viene impostato nel **membro dwSampleFlags** della [**struttura AM \_ SAMPLE2 \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)</span><span class="sxs-lookup"><span data-stu-id="f0dd5-119">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="f0dd5-120">Per altre informazioni, vedere [Miglioramenti della riproduzione DVD in Windows Vista.](dvd-playback-enhancements-in-windows-vista.md)</span><span class="sxs-lookup"><span data-stu-id="f0dd5-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0dd5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0dd5-121">Requirements</span></span>



| <span data-ttu-id="f0dd5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0dd5-122">Requirement</span></span> | <span data-ttu-id="f0dd5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f0dd5-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0dd5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0dd5-124">Header</span></span><br/> | <dl> <span data-ttu-id="f0dd5-125"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="f0dd5-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0dd5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0dd5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0dd5-127">**Impostare le proprietà di modifica della frequenza**</span><span class="sxs-lookup"><span data-stu-id="f0dd5-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




