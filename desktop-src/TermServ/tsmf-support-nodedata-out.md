---
title: Struttura TSMF_SUPPORT_NODEDATA_OUT
description: Usati all'interno \_ di TSMF supportano la \_ struttura dei dati \_ per contenere informazioni sui formati multimediali supportati.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- Struttura TSMF_SUPPORT_NODEDATA_OUT Servizi Desktop remoto
- Puntatore alla struttura PTSMF_SUPPORT_NODEDATA_OUT Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874069"
---
# <a name="tsmf_support_nodedata_out-structure"></a><span data-ttu-id="e022c-105">TSMF \_ supporta \_ la \_ struttura NODEDATA out</span><span class="sxs-lookup"><span data-stu-id="e022c-105">TSMF\_SUPPORT\_NODEDATA\_OUT structure</span></span>

<span data-ttu-id="e022c-106">Usati all'interno di [**TSMF supportano la struttura \_ \_ dei dati \_**](tsmf-support-data-out.md) per contenere informazioni sui formati multimediali supportati.</span><span class="sxs-lookup"><span data-stu-id="e022c-106">Used inside the [**TSMF\_SUPPORT\_DATA\_OUT**](tsmf-support-data-out.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="e022c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e022c-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a><span data-ttu-id="e022c-108">Members</span><span class="sxs-lookup"><span data-stu-id="e022c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e022c-109">**nodeId**</span><span class="sxs-lookup"><span data-stu-id="e022c-109">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="e022c-110">Nodo.</span><span class="sxs-lookup"><span data-stu-id="e022c-110">The node.</span></span>

</dd> <dt>

<span data-ttu-id="e022c-111">**hrSupportStatus**</span><span class="sxs-lookup"><span data-stu-id="e022c-111">**hrSupportStatus**</span></span>
</dt> <dd>

<span data-ttu-id="e022c-112">Indica se il sink identificato dal parametro *clsidNewSink* è supportato.</span><span class="sxs-lookup"><span data-stu-id="e022c-112">Whether the sink identified by the *clsidNewSink* parameter is supported.</span></span>

<span data-ttu-id="e022c-113">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="e022c-113">The possible values are.</span></span>

<dt>

<span data-ttu-id="e022c-114">0</span><span class="sxs-lookup"><span data-stu-id="e022c-114">0</span></span>
</dt> <dd>

<span data-ttu-id="e022c-115">Non supportato</span><span class="sxs-lookup"><span data-stu-id="e022c-115">Not supported</span></span>

</dd> <dt>

<span data-ttu-id="e022c-116">1</span><span class="sxs-lookup"><span data-stu-id="e022c-116">1</span></span>
</dt> <dd>

<span data-ttu-id="e022c-117">Supportato</span><span class="sxs-lookup"><span data-stu-id="e022c-117">Supported</span></span>

</dd> </dl>

<span data-ttu-id="e022c-118">Altri valori non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="e022c-118">Other values are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="e022c-119">**clsidNewSink**</span><span class="sxs-lookup"><span data-stu-id="e022c-119">**clsidNewSink**</span></span>
</dt> <dd>

<span data-ttu-id="e022c-120">Sink associato al tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e022c-120">The sink associated with the media type.</span></span>

</dd> <dt>

<span data-ttu-id="e022c-121">**supportedMediaTypeIndex**</span><span class="sxs-lookup"><span data-stu-id="e022c-121">**supportedMediaTypeIndex**</span></span>
</dt> <dd>

<span data-ttu-id="e022c-122">Indice in base zero del tipo di supporto supportato dal sink.</span><span class="sxs-lookup"><span data-stu-id="e022c-122">The zero-based index of the media type supported by the sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e022c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e022c-123">Requirements</span></span>



| <span data-ttu-id="e022c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e022c-124">Requirement</span></span> | <span data-ttu-id="e022c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e022c-125">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="e022c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e022c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e022c-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e022c-127">None supported</span></span><br/>         |
| <span data-ttu-id="e022c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e022c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e022c-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e022c-129">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e022c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e022c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e022c-131">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="e022c-131">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="e022c-132">**TSMF \_ supporta \_ i dati in \_ uscita**</span><span class="sxs-lookup"><span data-stu-id="e022c-132">**TSMF\_SUPPORT\_DATA\_OUT**</span></span>](tsmf-support-data-out.md)
</dt> </dl>

 

 





