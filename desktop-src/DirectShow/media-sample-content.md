---
description: Descrive il contenuto di un flusso elementare all'interno di un flusso di trasporto MPEG-2. Questa enumerazione viene utilizzata nell'interfaccia IMPEG2PIDMap, implementata nei pin di output del Demultiplexer MPEG-2.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: Enumerazione MEDIA_SAMPLE_CONTENT (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SAMPLE_CONTENT
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 9065f2af948ff28d181b24842673b086882837bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325920"
---
# <a name="media_sample_content-enumeration"></a><span data-ttu-id="94464-104">Enumerazione del contenuto di \_ esempio multimediale \_</span><span class="sxs-lookup"><span data-stu-id="94464-104">MEDIA\_SAMPLE\_CONTENT enumeration</span></span>

<span data-ttu-id="94464-105">Descrive il contenuto di un flusso elementare all'interno di un flusso di trasporto MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="94464-105">Describes the contents of an elementary stream within an MPEG-2 transport stream.</span></span> <span data-ttu-id="94464-106">Questa enumerazione viene utilizzata nell'interfaccia [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) , implementata nei pin di output del [Demultiplexer MPEG-2](mpeg-2-demultiplexer.md).</span><span class="sxs-lookup"><span data-stu-id="94464-106">This enumeration is used in the [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) interface, which is implemented on the output pins of the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="94464-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94464-107">Syntax</span></span>


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a><span data-ttu-id="94464-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="94464-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="94464-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**\_pacchetto di trasporto multimediale \_**</span><span class="sxs-lookup"><span data-stu-id="94464-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**MEDIA\_TRANSPORT\_PACKET**</span></span>
</dt> <dd>

<span data-ttu-id="94464-110">Specifica un pacchetto del flusso di trasporto completo da passare senza elaborazione.</span><span class="sxs-lookup"><span data-stu-id="94464-110">Specifies a complete transport stream packet to be passed through without processing.</span></span>

</dd> <dt>

<span data-ttu-id="94464-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**\_flusso elementare \_ multimediale**</span><span class="sxs-lookup"><span data-stu-id="94464-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**MEDIA\_ELEMENTARY\_STREAM**</span></span>
</dt> <dd>

<span data-ttu-id="94464-112">Specifica il payload di un file audio o video.</span><span class="sxs-lookup"><span data-stu-id="94464-112">Specifies an audio or video PES payload.</span></span>

</dd> <dt>

<span data-ttu-id="94464-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA \_ MPEG2 \_ PSI**</span><span class="sxs-lookup"><span data-stu-id="94464-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA\_MPEG2\_PSI**</span></span>
</dt> <dd>

<span data-ttu-id="94464-114">Specifica un flusso di dati PAT, PMT, CAT o private.</span><span class="sxs-lookup"><span data-stu-id="94464-114">Specifies a PAT, PMT, CAT, or Private data stream.</span></span> <span data-ttu-id="94464-115">Si tratta di sezioni PSI complete che non è necessario riassemblare.</span><span class="sxs-lookup"><span data-stu-id="94464-115">These are complete PSI sections which do not need to be reassembled.</span></span>

</dd> <dt>

<span data-ttu-id="94464-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**\_payload del trasporto multimediale \_**</span><span class="sxs-lookup"><span data-stu-id="94464-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**MEDIA\_TRANSPORT\_PAYLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="94464-117">Specifica i payload di pacchetti TS raccolti, ad esempio i pacchetti PES.</span><span class="sxs-lookup"><span data-stu-id="94464-117">Specifies gathered TS packet payloads, such as PES packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94464-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94464-118">Requirements</span></span>



| <span data-ttu-id="94464-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="94464-119">Requirement</span></span> | <span data-ttu-id="94464-120">Valore</span><span class="sxs-lookup"><span data-stu-id="94464-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94464-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94464-121">Header</span></span><br/> | <dl> <span data-ttu-id="94464-122"><dt>Bdatypes. h (include Bdaiface. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94464-122"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94464-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94464-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94464-124">Tipi enumerati DirectShow</span><span class="sxs-lookup"><span data-stu-id="94464-124">DirectShow Enumerated Types</span></span>](directshow-enumerated-types.md)
</dt> </dl>

 

 




