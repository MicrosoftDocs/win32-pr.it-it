---
description: Specifica i dati del controllo sezionamento.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: Struttura DXVA_Slice_HEVC_Short (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049307"
---
# <a name="dxva_slice_hevc_short-structure"></a><span data-ttu-id="5288b-103">DXVA \_ Slice \_ HEVC \_ breve struttura</span><span class="sxs-lookup"><span data-stu-id="5288b-103">DXVA\_Slice\_HEVC\_Short structure</span></span>

<span data-ttu-id="5288b-104">Specifica i dati del controllo sezionamento.</span><span class="sxs-lookup"><span data-stu-id="5288b-104">Specifies slice control data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5288b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5288b-105">Syntax</span></span>


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a><span data-ttu-id="5288b-106">Members</span><span class="sxs-lookup"><span data-stu-id="5288b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5288b-107">**BSNALunitDataLocation**</span><span class="sxs-lookup"><span data-stu-id="5288b-107">**BSNALunitDataLocation**</span></span>
</dt> <dd>

<span data-ttu-id="5288b-108">Specifica la posizione dell'unità NAL.</span><span class="sxs-lookup"><span data-stu-id="5288b-108">Specifies the location of the NAL unit.</span></span>

</dd> <dt>

<span data-ttu-id="5288b-109">**SliceBytesInBuffer**</span><span class="sxs-lookup"><span data-stu-id="5288b-109">**SliceBytesInBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="5288b-110">Il numero di byte nel buffer di dati Bitstream associato a questa struttura di dati del controllo Slice.</span><span class="sxs-lookup"><span data-stu-id="5288b-110">The number of bytes in the bitstream data buffer that are associated with this slice control data structure.</span></span>

</dd> <dt>

<span data-ttu-id="5288b-111">**wBadSliceChopping**</span><span class="sxs-lookup"><span data-stu-id="5288b-111">**wBadSliceChopping**</span></span>
</dt> <dd>

<span data-ttu-id="5288b-112">Se si usa l'analisi Bitstream fuori host, questo valore indica il sezionamento della sezione non valida e contiene uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5288b-112">If off-host bitstream parsing is used, this value indicates the bad slice chopping and contains one of the following values:</span></span>



| <span data-ttu-id="5288b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5288b-113">Requirement</span></span> | <span data-ttu-id="5288b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5288b-114">Value</span></span> |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5288b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5288b-115">Value</span></span> | <span data-ttu-id="5288b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5288b-116">Description</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="5288b-117">0</span><span class="sxs-lookup"><span data-stu-id="5288b-117">0</span></span>     | <span data-ttu-id="5288b-118">Tutti i bit per la sezione si trovano all'interno del buffer dei dati Bitstream corrispondente.</span><span class="sxs-lookup"><span data-stu-id="5288b-118">All bits for the slice are located within the corresponding bitstream data buffer.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="5288b-119">1</span><span class="sxs-lookup"><span data-stu-id="5288b-119">1</span></span>     | <span data-ttu-id="5288b-120">Il buffer di dati Bitstream contiene l'inizio della sezione, ma non l'intera sezione, perché il buffer è pieno.</span><span class="sxs-lookup"><span data-stu-id="5288b-120">The bitstream data buffer contains the start of the slice, but not the entire slice, because the buffer is full.</span></span>                                                                                                                                        |
| <span data-ttu-id="5288b-121">2</span><span class="sxs-lookup"><span data-stu-id="5288b-121">2</span></span>     | <span data-ttu-id="5288b-122">Il buffer di dati Bitstream contiene la fine della sezione.</span><span class="sxs-lookup"><span data-stu-id="5288b-122">The bitstream data buffer contains the end of the slice.</span></span> <span data-ttu-id="5288b-123">Non contiene l'inizio della sezione, perché l'inizio della sezione si trova nel buffer dei dati Bitstream precedente.</span><span class="sxs-lookup"><span data-stu-id="5288b-123">It does not contain the start of the slice, because the start of the slice was located in the previous bitstream data buffer.</span></span>                                                                  |
| <span data-ttu-id="5288b-124">3</span><span class="sxs-lookup"><span data-stu-id="5288b-124">3</span></span>     | <span data-ttu-id="5288b-125">Il buffer di dati Bitstream non contiene l'inizio della sezione perché l'inizio della sezione si trova nel buffer dei dati Bitstream precedente e non contiene la fine della sezione perché anche il buffer dei dati Bitstream corrente è pieno.</span><span class="sxs-lookup"><span data-stu-id="5288b-125">The bitstream data buffer does not contain the start of the slice because the start of the slice was located in the previous bitstream data buffer and it does not contain the end of the slice becuase the current bitstream data buffer is also full.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5288b-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="5288b-126">Remarks</span></span>

<span data-ttu-id="5288b-127">**DXVA \_ Slice \_ HEVC \_ short** contiene i dati di controllo delle sezioni che vengono passati all'acceleratore hardware dal decodificatore software host.</span><span class="sxs-lookup"><span data-stu-id="5288b-127">**DXVA\_Slice\_HEVC\_Short** contains slice control data which is passed to the hardware accelerator from the host software decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="5288b-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5288b-128">Requirements</span></span>



| <span data-ttu-id="5288b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5288b-129">Requirement</span></span> | <span data-ttu-id="5288b-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5288b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5288b-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5288b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5288b-132">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5288b-132">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5288b-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5288b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5288b-134">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5288b-134">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5288b-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5288b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5288b-136"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5288b-136"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5288b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5288b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5288b-138">Strutture di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5288b-138">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




