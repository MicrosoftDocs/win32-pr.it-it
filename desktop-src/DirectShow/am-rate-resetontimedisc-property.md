---
description: Si applica a Windows Vista e versioni successive.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: Proprietà AM_RATE_ResetOnTimeDisc (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c26763d32513652a08d38b52bf6fb745d3d321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330328"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="39c7e-103">\_Proprietà rate \_ ResetOnTimeDisc</span><span class="sxs-lookup"><span data-stu-id="39c7e-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="39c7e-104">Si applica a Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="39c7e-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="39c7e-105">Questa proprietà esegue una query se il decodificatore risincronizza i timestamp di output ai timestamp di input quando il decodificatore riceve un campione con il flag di discontinuità.</span><span class="sxs-lookup"><span data-stu-id="39c7e-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="39c7e-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="39c7e-106">This property is read/write.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="39c7e-107">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="39c7e-107">Property Set GUID</span></span> | <span data-ttu-id="39c7e-108">\_TSRateChange KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="39c7e-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="39c7e-109">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="39c7e-109">Property ID</span></span>       | <span data-ttu-id="39c7e-110">\_Frequenza \_ ResetOnTimeDisc</span><span class="sxs-lookup"><span data-stu-id="39c7e-110">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="39c7e-111">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="39c7e-111">Data Type</span></span>         | <span data-ttu-id="39c7e-112">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="39c7e-112">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="39c7e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="39c7e-113">Remarks</span></span>

<span data-ttu-id="39c7e-114">Questa proprietà supporta le modifiche alla frequenza uniforme.</span><span class="sxs-lookup"><span data-stu-id="39c7e-114">This property supports smooth rate changes.</span></span> <span data-ttu-id="39c7e-115">Se il valore di questa proprietà è **true** e il decodificatore riceve un esempio di input con il \_ flag AM Sample \_ TIMEDISCONTINUITY, il fotogramma decodificato deve avere lo stesso timestamp del frame di input.</span><span class="sxs-lookup"><span data-stu-id="39c7e-115">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="39c7e-116">Per recuperare il \_ flag TIMEDISCONTINUITY di esempio AM \_ , chiamare [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="39c7e-116">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="39c7e-117">Il flag viene impostato nel membro **dwSampleFlags** della struttura delle [**\_ \_ Proprietà SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="39c7e-117">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="39c7e-118">Per ulteriori informazioni, vedere [miglioramenti della riproduzione DVD in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="39c7e-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39c7e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39c7e-119">Requirements</span></span>



| <span data-ttu-id="39c7e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c7e-120">Requirement</span></span> | <span data-ttu-id="39c7e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="39c7e-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39c7e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39c7e-122">Header</span></span><br/> | <dl> <span data-ttu-id="39c7e-123"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c7e-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c7e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39c7e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c7e-125">**Set di proprietà di modifica della frequenza**</span><span class="sxs-lookup"><span data-stu-id="39c7e-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




