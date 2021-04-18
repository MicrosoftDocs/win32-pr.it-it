---
title: Struttura TSMF_SUPPORT_NODEDATA_IN
description: Usati all'interno del TSMF \_ supportano i \_ dati \_ nella struttura per contenere informazioni sui formati multimediali supportati.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- Struttura TSMF_SUPPORT_NODEDATA_IN Servizi Desktop remoto
- Puntatore alla struttura PTSMF_SUPPORT_NODEDATA_IN Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301854"
---
# <a name="tsmf_support_nodedata_in-structure"></a><span data-ttu-id="09144-105">TSMF \_ supporta \_ NODEDATA \_ nella struttura</span><span class="sxs-lookup"><span data-stu-id="09144-105">TSMF\_SUPPORT\_NODEDATA\_IN structure</span></span>

<span data-ttu-id="09144-106">Usati all'interno del [**TSMF \_ supportano i \_ dati \_ nella**](tsmf-support-data-in.md) struttura per contenere informazioni sui formati multimediali supportati.</span><span class="sxs-lookup"><span data-stu-id="09144-106">Used inside the [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="09144-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09144-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a><span data-ttu-id="09144-108">Members</span><span class="sxs-lookup"><span data-stu-id="09144-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="09144-109">**byteCount**</span><span class="sxs-lookup"><span data-stu-id="09144-109">**byteCount**</span></span>
</dt> <dd>

<span data-ttu-id="09144-110">Dimensioni in byte della struttura.</span><span class="sxs-lookup"><span data-stu-id="09144-110">The size of the structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="09144-111">**nodeId**</span><span class="sxs-lookup"><span data-stu-id="09144-111">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="09144-112">Nodo.</span><span class="sxs-lookup"><span data-stu-id="09144-112">The node.</span></span>

</dd> <dt>

<span data-ttu-id="09144-113">**numMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="09144-113">**numMediaTypes**</span></span>
</dt> <dd>

<span data-ttu-id="09144-114">Il numero di strutture di formato multimediale.</span><span class="sxs-lookup"><span data-stu-id="09144-114">The number of media format structures.</span></span>

</dd> <dt>

<span data-ttu-id="09144-115">**...**</span><span class="sxs-lookup"><span data-stu-id="09144-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="09144-116">Numero variabile di strutture che definiscono formati di supporti audio o video.</span><span class="sxs-lookup"><span data-stu-id="09144-116">A variable number of structures defining audio or video media formats.</span></span> <span data-ttu-id="09144-117">**FormatType** è **formato \_ WAVEFORMATEX** per l'audio o il **formato \_ MFVideoFormat** per il video.</span><span class="sxs-lookup"><span data-stu-id="09144-117">The **FormatType** is either **FORMAT\_WaveFormatEx** for audio or **FORMAT\_MFVideoFormat** for video.</span></span>

<span data-ttu-id="09144-118">Per informazioni dettagliate su questa struttura, [vedere \_ struttura \_ del \_ tipo di supporto di Servizi terminal](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span><span class="sxs-lookup"><span data-stu-id="09144-118">For details of this structure, see [TS\_AM\_MEDIA\_TYPE Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09144-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09144-119">Requirements</span></span>



| <span data-ttu-id="09144-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="09144-120">Requirement</span></span> | <span data-ttu-id="09144-121">Valore</span><span class="sxs-lookup"><span data-stu-id="09144-121">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="09144-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09144-122">Minimum supported client</span></span><br/> | <span data-ttu-id="09144-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="09144-123">None supported</span></span><br/>         |
| <span data-ttu-id="09144-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09144-124">Minimum supported server</span></span><br/> | <span data-ttu-id="09144-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09144-125">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09144-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09144-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09144-127">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="09144-127">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="09144-128">**TSMF \_ supporta \_ i dati \_ in**</span><span class="sxs-lookup"><span data-stu-id="09144-128">**TSMF\_SUPPORT\_DATA\_IN**</span></span>](tsmf-support-data-in.md)
</dt> </dl>

 

