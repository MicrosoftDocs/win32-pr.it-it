---
description: La \_ struttura dello stride del trasporto MPEG2 \_ descrive il formato dei pacchetti di flusso di trasporto MPEG-2.
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: Struttura MPEG2_TRANSPORT_STRIDE (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 4a0cdc21bdd8c320728da0c0af8c0af023de68eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325167"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="748d3-103">\_ \_ Struttura stride trasporto MPEG2</span><span class="sxs-lookup"><span data-stu-id="748d3-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="748d3-104">La `MPEG2_TRANSPORT_STRIDE` struttura descrive il formato dei pacchetti MPEG-2 Transport Stream (TS).</span><span class="sxs-lookup"><span data-stu-id="748d3-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="748d3-105">Questa struttura consente flussi di trasporto in cui i pacchetti di trasporto da 188 byte non sono contigui.</span><span class="sxs-lookup"><span data-stu-id="748d3-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="748d3-106">Ai fini di questa documentazione, questi pacchetti sono detti *pacchetti stride*.</span><span class="sxs-lookup"><span data-stu-id="748d3-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="748d3-107">I pacchetti stride sono identificati dal seguente tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="748d3-107">Stride packets are identified by the following media type:</span></span>



|             |                                        |
|-------------|----------------------------------------|
| <span data-ttu-id="748d3-108">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="748d3-108">Major Type</span></span>  | <span data-ttu-id="748d3-109">\_Flusso MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="748d3-109">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="748d3-110">Subtype</span><span class="sxs-lookup"><span data-stu-id="748d3-110">Subtype</span></span>     | <span data-ttu-id="748d3-111">\_ \_ Stride trasporto MPEG2 \_ MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="748d3-111">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="748d3-112">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="748d3-112">Format Type</span></span> | <span data-ttu-id="748d3-113">FORMATO \_ None</span><span class="sxs-lookup"><span data-stu-id="748d3-113">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="748d3-114">Il formato del blocco (**pbFormat**) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="748d3-114">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="748d3-115">Se il blocco di formato è incluso, deve iniziare con una struttura dello **\_ \_ stride del trasporto MPEG2** .</span><span class="sxs-lookup"><span data-stu-id="748d3-115">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="748d3-116">Questa struttura definisce il layout del pacchetto di trasporto all'interno del pacchetto stride.</span><span class="sxs-lookup"><span data-stu-id="748d3-116">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="748d3-117">Se il blocco di formato è **null**, si presuppone che i pacchetti usino un set di valori predefiniti. per informazioni dettagliate, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="748d3-117">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="748d3-118">Sintassi</span><span class="sxs-lookup"><span data-stu-id="748d3-118">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="748d3-119">Members</span><span class="sxs-lookup"><span data-stu-id="748d3-119">Members</span></span>

<dl> <dt>

<span data-ttu-id="748d3-120">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="748d3-120">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="748d3-121">Specifica l'offset, in byte, dall'inizio del pacchetto al primo byte del pacchetto di trasporto incorporato.</span><span class="sxs-lookup"><span data-stu-id="748d3-121">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="748d3-122">Il valore deve essere compreso tra zero e `(dwStride - dwPacketLength)` , inclusi.</span><span class="sxs-lookup"><span data-stu-id="748d3-122">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="748d3-123">**dwPacketLength**</span><span class="sxs-lookup"><span data-stu-id="748d3-123">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="748d3-124">Specifica la lunghezza, in byte, del pacchetto di trasporto incorporato.</span><span class="sxs-lookup"><span data-stu-id="748d3-124">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="748d3-125">Per i pacchetti di trasporto MPEG-2 standard, il valore deve essere pari a 188 byte.</span><span class="sxs-lookup"><span data-stu-id="748d3-125">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="748d3-126">**dwStride**</span><span class="sxs-lookup"><span data-stu-id="748d3-126">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="748d3-127">Specifica la lunghezza in byte dell'intero pacchetto stride.</span><span class="sxs-lookup"><span data-stu-id="748d3-127">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="748d3-128">Il valore deve essere almeno `(dwOffset + dwPacketLength)` .</span><span class="sxs-lookup"><span data-stu-id="748d3-128">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="748d3-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="748d3-129">Remarks</span></span>

<span data-ttu-id="748d3-130">Il diagramma seguente illustra le relazioni tra i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="748d3-130">The following diagram illustrates the relations between the structure members.</span></span>

![pacchetto MPEG-2 stride](images/mpeg2-stride-packet.png)

<span data-ttu-id="748d3-132">I buffer di input che contengono pacchetti stride in multiplex presentano alcune restrizioni:</span><span class="sxs-lookup"><span data-stu-id="748d3-132">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="748d3-133">I pacchetti stride devono essere compressi in modo contiguo all'interno del buffer.</span><span class="sxs-lookup"><span data-stu-id="748d3-133">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="748d3-134">Nessun byte può precedere il primo pacchetto stride o seguire l'ultimo pacchetto stride.</span><span class="sxs-lookup"><span data-stu-id="748d3-134">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="748d3-135">Un numero integrale di pacchetti stride deve rientrare nel buffer; ovvero la lunghezza del buffer% dwStride è uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="748d3-135">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="748d3-136">Non esiste alcuna restrizione per il numero di pacchetti stride per buffer.</span><span class="sxs-lookup"><span data-stu-id="748d3-136">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="748d3-137">Se il tipo di supporto non contiene un blocco di formato (**pbFormat** è **null**), vengono usati i valori predefiniti seguenti:</span><span class="sxs-lookup"><span data-stu-id="748d3-137">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="748d3-138">**dwOffset**: 0</span><span class="sxs-lookup"><span data-stu-id="748d3-138">**dwOffset**: 0</span></span>
-   <span data-ttu-id="748d3-139">**dwPacketLength**: 188</span><span class="sxs-lookup"><span data-stu-id="748d3-139">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="748d3-140">**dwStride**: 188</span><span class="sxs-lookup"><span data-stu-id="748d3-140">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="748d3-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="748d3-141">Requirements</span></span>



| <span data-ttu-id="748d3-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="748d3-142">Requirement</span></span> | <span data-ttu-id="748d3-143">Valore</span><span class="sxs-lookup"><span data-stu-id="748d3-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="748d3-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="748d3-144">Header</span></span><br/> | <dl> <span data-ttu-id="748d3-145"><dt>Bdatypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="748d3-145"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="748d3-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="748d3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="748d3-147">Strutture DirectShow</span><span class="sxs-lookup"><span data-stu-id="748d3-147">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="748d3-148">Tipi di supporti MPEG-2</span><span class="sxs-lookup"><span data-stu-id="748d3-148">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




