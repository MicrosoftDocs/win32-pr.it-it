---
description: Archivia le informazioni sulle sezioni della memoria condivisa.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: Struttura SHAREDMEMORY_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314898"
---
# <a name="sharedmemory_header-structure"></a><span data-ttu-id="a7c88-103">\_Struttura dell'intestazione SHAREDMEMORY</span><span class="sxs-lookup"><span data-stu-id="a7c88-103">SHAREDMEMORY\_HEADER structure</span></span>

<span data-ttu-id="a7c88-104">Archivia le informazioni sulle sezioni della memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="a7c88-104">Stores information about shared memory sections.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c88-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7c88-105">Syntax</span></span>


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a><span data-ttu-id="a7c88-106">Members</span><span class="sxs-lookup"><span data-stu-id="a7c88-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a7c88-107">**cbTotal**</span><span class="sxs-lookup"><span data-stu-id="a7c88-107">**cbTotal**</span></span>
</dt> <dd>

<span data-ttu-id="a7c88-108">Dimensione, in byte, dei dati a cui fa riferimento questa struttura di intestazione.</span><span class="sxs-lookup"><span data-stu-id="a7c88-108">The size, in bytes, of the data referenced by this header structure.</span></span>

</dd> <dt>

<span data-ttu-id="a7c88-109">**cbOffsetSns**</span><span class="sxs-lookup"><span data-stu-id="a7c88-109">**cbOffsetSns**</span></span>
</dt> <dd>

<span data-ttu-id="a7c88-110">Dimensioni, in byte, di offset dei numeri di serie rispetto alla struttura dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="a7c88-110">The size, in bytes, that the serial numbers are offset from the header structure.</span></span>

</dd> <dt>

<span data-ttu-id="a7c88-111">**idxEvent**</span><span class="sxs-lookup"><span data-stu-id="a7c88-111">**idxEvent**</span></span>
</dt> <dd>

<span data-ttu-id="a7c88-112">Indice dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a7c88-112">The event index.</span></span> <span data-ttu-id="a7c88-113">Questo valore viene incrementato con gli eventi successivi.</span><span class="sxs-lookup"><span data-stu-id="a7c88-113">This value is incremented with successive events.</span></span>

</dd> <dt>

<span data-ttu-id="a7c88-114">**dwEvent**</span><span class="sxs-lookup"><span data-stu-id="a7c88-114">**dwEvent**</span></span>
</dt> <dd>

<span data-ttu-id="a7c88-115">Evento associato a questa intestazione.</span><span class="sxs-lookup"><span data-stu-id="a7c88-115">The event associated with this header.</span></span>

</dd> <dt>

<span data-ttu-id="a7c88-116">**CID**</span><span class="sxs-lookup"><span data-stu-id="a7c88-116">**cid**</span></span>
</dt> <dd>

<span data-ttu-id="a7c88-117">Identificatore di cursore a cui fa riferimento l'intestazione Shared Memory.</span><span class="sxs-lookup"><span data-stu-id="a7c88-117">The cursor identifier referenced by the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="a7c88-118">**sn**</span><span class="sxs-lookup"><span data-stu-id="a7c88-118">**sn**</span></span>
</dt> <dd>

<span data-ttu-id="a7c88-119">Numero di serie per l'intestazione Shared Memory.</span><span class="sxs-lookup"><span data-stu-id="a7c88-119">The serial number for the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="a7c88-120">**sysEvt**</span><span class="sxs-lookup"><span data-stu-id="a7c88-120">**sysEvt**</span></span>
</dt> <dd>

<span data-ttu-id="a7c88-121">Evento di sistema, con prefisso SE \_ \* , associato a questa intestazione.</span><span class="sxs-lookup"><span data-stu-id="a7c88-121">The system event, prefixed SE\_\*, associated with this header.</span></span> <span data-ttu-id="a7c88-122">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a7c88-122">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="a7c88-123">**sysEvtData**</span><span class="sxs-lookup"><span data-stu-id="a7c88-123">**sysEvtData**</span></span>
</dt> <dd>

<span data-ttu-id="a7c88-124">Struttura [**\_ \_ dei dati dell'evento di sistema**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) associata all'evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="a7c88-124">The [**SYSTEM\_EVENT\_DATA**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) structure associated with the system event.</span></span>

</dd> <dt>

<span data-ttu-id="a7c88-125">**cPackets**</span><span class="sxs-lookup"><span data-stu-id="a7c88-125">**cPackets**</span></span>
</dt> <dd>

<span data-ttu-id="a7c88-126">Conteggio dei pacchetti associati alla sezione della memoria condivisa corrente.</span><span class="sxs-lookup"><span data-stu-id="a7c88-126">A count of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="a7c88-127">**cbPackets**</span><span class="sxs-lookup"><span data-stu-id="a7c88-127">**cbPackets**</span></span>
</dt> <dd>

<span data-ttu-id="a7c88-128">Dimensione, in byte, dei pacchetti associati alla sezione della memoria condivisa corrente.</span><span class="sxs-lookup"><span data-stu-id="a7c88-128">The size, in bytes, of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="a7c88-129">**fSnsPresent**</span><span class="sxs-lookup"><span data-stu-id="a7c88-129">**fSnsPresent**</span></span>
</dt> <dd>

<span data-ttu-id="a7c88-130">Flag che indica se i numeri di serie sono presenti nella sezione della memoria condivisa corrente.</span><span class="sxs-lookup"><span data-stu-id="a7c88-130">A flag indicating whether serial numbers are present in the current shared memory section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7c88-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7c88-131">Remarks</span></span>

<span data-ttu-id="a7c88-132">I valori seguenti sono definiti per il membro **sysEvt** .</span><span class="sxs-lookup"><span data-stu-id="a7c88-132">The following values are defined for the **sysEvt** member.</span></span>


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a><span data-ttu-id="a7c88-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7c88-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7c88-134">**\_dati degli eventi di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="a7c88-134">**SYSTEM\_EVENT\_DATA**</span></span>](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



