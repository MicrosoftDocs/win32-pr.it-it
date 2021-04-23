---
description: La struttura MPEG2 \_ TRANSPORT STRIDE descrive il formato dei pacchetti \_ TS (Transport Stream) MPEG-2.
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: MPEG2_TRANSPORT_STRIDE struttura (Bdatypes.h)
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
ms.openlocfilehash: 5153f6f79c2807634149222a126a7256a65ffe8a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908489"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="7d10c-103">Struttura STRIDE DEL TRASPORTO MPEG2 \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d10c-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="7d10c-104">La `MPEG2_TRANSPORT_STRIDE` struttura descrive il formato dei pacchetti TS (Transport Stream) MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="7d10c-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="7d10c-105">Questa struttura consente flussi di trasporto in cui i pacchetti di trasporto a 188 byte non sono contigui.</span><span class="sxs-lookup"><span data-stu-id="7d10c-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="7d10c-106">Ai fini di questa documentazione, tali pacchetti vengono definiti pacchetti *stride*.</span><span class="sxs-lookup"><span data-stu-id="7d10c-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="7d10c-107">I pacchetti Stride sono identificati dal tipo di supporto seguente:</span><span class="sxs-lookup"><span data-stu-id="7d10c-107">Stride packets are identified by the following media type:</span></span>



| <span data-ttu-id="7d10c-108">Label</span><span class="sxs-lookup"><span data-stu-id="7d10c-108">Label</span></span> | <span data-ttu-id="7d10c-109">Valore</span><span class="sxs-lookup"><span data-stu-id="7d10c-109">Value</span></span> |
|-------------|----------------------------------------|
| <span data-ttu-id="7d10c-110">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="7d10c-110">Major Type</span></span>  | <span data-ttu-id="7d10c-111">Flusso \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="7d10c-111">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="7d10c-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="7d10c-112">Subtype</span></span>     | <span data-ttu-id="7d10c-113">MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="7d10c-113">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="7d10c-114">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="7d10c-114">Format Type</span></span> | <span data-ttu-id="7d10c-115">FORMAT \_ None</span><span class="sxs-lookup"><span data-stu-id="7d10c-115">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="7d10c-116">Il blocco di formato (**pbFormat**) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7d10c-116">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="7d10c-117">Se il blocco di formato è incluso, deve iniziare con una **struttura \_ MPEG2 TRANSPORT \_ STRIDE.**</span><span class="sxs-lookup"><span data-stu-id="7d10c-117">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="7d10c-118">Questa struttura definisce il layout del pacchetto di trasporto all'interno del pacchetto stride.</span><span class="sxs-lookup"><span data-stu-id="7d10c-118">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="7d10c-119">Se il blocco di formato **è NULL,** si presuppone che i pacchetti usino un set di valori predefiniti. Per informazioni dettagliate, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="7d10c-119">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d10c-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d10c-120">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="7d10c-121">Members</span><span class="sxs-lookup"><span data-stu-id="7d10c-121">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d10c-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="7d10c-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7d10c-123">Specifica l'offset, in byte, dall'inizio del pacchetto al primo byte del pacchetto di trasporto incorporato.</span><span class="sxs-lookup"><span data-stu-id="7d10c-123">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="7d10c-124">Il valore deve essere compreso tra zero e `(dwStride - dwPacketLength)` , inclusi.</span><span class="sxs-lookup"><span data-stu-id="7d10c-124">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="7d10c-125">**dwPacketLength**</span><span class="sxs-lookup"><span data-stu-id="7d10c-125">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="7d10c-126">Specifica la lunghezza in byte del pacchetto di trasporto incorporato.</span><span class="sxs-lookup"><span data-stu-id="7d10c-126">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="7d10c-127">Per i pacchetti di trasporto MPEG-2 standard, il valore deve essere 188 byte.</span><span class="sxs-lookup"><span data-stu-id="7d10c-127">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7d10c-128">**dwStride**</span><span class="sxs-lookup"><span data-stu-id="7d10c-128">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="7d10c-129">Specifica la lunghezza in byte dell'intero pacchetto stride.</span><span class="sxs-lookup"><span data-stu-id="7d10c-129">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="7d10c-130">Il valore deve essere almeno `(dwOffset + dwPacketLength)` .</span><span class="sxs-lookup"><span data-stu-id="7d10c-130">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d10c-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d10c-131">Remarks</span></span>

<span data-ttu-id="7d10c-132">Il diagramma seguente illustra le relazioni tra i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="7d10c-132">The following diagram illustrates the relations between the structure members.</span></span>

![Pacchetto mpeg-2 stride](images/mpeg2-stride-packet.png)

<span data-ttu-id="7d10c-134">I buffer di input che contengono pacchetti stride multiplexed hanno alcune restrizioni:</span><span class="sxs-lookup"><span data-stu-id="7d10c-134">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="7d10c-135">I pacchetti Stride devono essere imballati in modo contiguo all'interno del buffer.</span><span class="sxs-lookup"><span data-stu-id="7d10c-135">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="7d10c-136">Nessun byte può precedere il primo pacchetto stride o seguire l'ultimo pacchetto stride.</span><span class="sxs-lookup"><span data-stu-id="7d10c-136">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="7d10c-137">Un numero integrale di pacchetti stride deve essere contenuto nel buffer. in altri, la lunghezza del buffer % dwStride è uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="7d10c-137">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="7d10c-138">Non esiste alcuna restrizione sul numero di pacchetti stride per buffer.</span><span class="sxs-lookup"><span data-stu-id="7d10c-138">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="7d10c-139">Se il tipo di supporto non contiene un blocco di formato (**pbFormat** è **NULL),** vengono usati i valori predefiniti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7d10c-139">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="7d10c-140">**dwOffset**: 0</span><span class="sxs-lookup"><span data-stu-id="7d10c-140">**dwOffset**: 0</span></span>
-   <span data-ttu-id="7d10c-141">**dwPacketLength**: 188</span><span class="sxs-lookup"><span data-stu-id="7d10c-141">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="7d10c-142">**dwStride**: 188</span><span class="sxs-lookup"><span data-stu-id="7d10c-142">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="7d10c-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d10c-143">Requirements</span></span>



| <span data-ttu-id="7d10c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d10c-144">Requirement</span></span> | <span data-ttu-id="7d10c-145">Valore</span><span class="sxs-lookup"><span data-stu-id="7d10c-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d10c-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d10c-146">Header</span></span><br/> | <dl> <span data-ttu-id="7d10c-147"><dt>Bdatypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="7d10c-147"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d10c-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d10c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d10c-149">Strutture DirectShow</span><span class="sxs-lookup"><span data-stu-id="7d10c-149">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="7d10c-150">Tipi di supporti MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7d10c-150">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




