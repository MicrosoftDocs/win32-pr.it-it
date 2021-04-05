---
title: Struttura MPCONFIGURATION_DATA (MpClient. h)
description: Contiene i dati sulle modifiche di configurazione, inclusi i vecchi e i nuovi valori.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- Struttura MPCONFIGURATION_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCONFIGURATION_DATA
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048215"
---
# <a name="mpconfiguration_data-structure"></a><span data-ttu-id="0862f-105">\_Struttura dei dati MPCONFIGURATION</span><span class="sxs-lookup"><span data-stu-id="0862f-105">MPCONFIGURATION\_DATA structure</span></span>

<span data-ttu-id="0862f-106">Contiene i dati sulle modifiche di configurazione, inclusi i vecchi e i nuovi valori.</span><span class="sxs-lookup"><span data-stu-id="0862f-106">Contains data about configuration changes, including the old and new values.</span></span>

## <a name="syntax"></a><span data-ttu-id="0862f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0862f-107">Syntax</span></span>


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a><span data-ttu-id="0862f-108">Members</span><span class="sxs-lookup"><span data-stu-id="0862f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0862f-109">**ConfigurationName**</span><span class="sxs-lookup"><span data-stu-id="0862f-109">**ConfigurationName**</span></span>
</dt> <dd>

<span data-ttu-id="0862f-110">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="0862f-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="0862f-111">Nome della configurazione modificata.</span><span class="sxs-lookup"><span data-stu-id="0862f-111">Name of the configuration that changed.</span></span>

</dd> <dt>

<span data-ttu-id="0862f-112">**DataType**</span><span class="sxs-lookup"><span data-stu-id="0862f-112">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="0862f-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0862f-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0862f-114">Tipo di dati utilizzati.</span><span class="sxs-lookup"><span data-stu-id="0862f-114">The type of data used.</span></span>

</dd> <dt>

<span data-ttu-id="0862f-115">**PreviousDataSize**</span><span class="sxs-lookup"><span data-stu-id="0862f-115">**PreviousDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="0862f-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0862f-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0862f-117">Dimensioni in byte dei dati precedenti.</span><span class="sxs-lookup"><span data-stu-id="0862f-117">Size of previous data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0862f-118">**pPreviousData**</span><span class="sxs-lookup"><span data-stu-id="0862f-118">**pPreviousData**</span></span>
</dt> <dd>

<span data-ttu-id="0862f-119">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="0862f-119">Type: \**BYTE\** _</span></span>

</dd> <dd>

<span data-ttu-id="0862f-120">Puntatore ai dati precedenti.</span><span class="sxs-lookup"><span data-stu-id="0862f-120">Pointer to previous data.</span></span>

</dd> <dt>

<span data-ttu-id="0862f-121">_ *CurrentDataSize*\*</span><span class="sxs-lookup"><span data-stu-id="0862f-121">_ *CurrentDataSize*\*</span></span>
</dt> <dd>

<span data-ttu-id="0862f-122">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0862f-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0862f-123">Dimensioni dei nuovi dati in byte.</span><span class="sxs-lookup"><span data-stu-id="0862f-123">Size of new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0862f-124">**pCurrentData**</span><span class="sxs-lookup"><span data-stu-id="0862f-124">**pCurrentData**</span></span>
</dt> <dd>

<span data-ttu-id="0862f-125">Tipo: **byte \***</span><span class="sxs-lookup"><span data-stu-id="0862f-125">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="0862f-126">Puntatore ai nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="0862f-126">Pointer to new data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0862f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0862f-127">Requirements</span></span>



| <span data-ttu-id="0862f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0862f-128">Requirement</span></span> | <span data-ttu-id="0862f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0862f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0862f-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0862f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0862f-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0862f-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0862f-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0862f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0862f-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0862f-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0862f-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0862f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0862f-135"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0862f-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





