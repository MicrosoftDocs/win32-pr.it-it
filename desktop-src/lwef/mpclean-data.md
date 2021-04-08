---
title: Struttura MPCLEAN_DATA (MpClient. h)
description: Dati di notifica passati alla funzione di callback pulita.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- Struttura MPCLEAN_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCLEAN_DATA
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741026"
---
# <a name="mpclean_data-structure"></a><span data-ttu-id="8d12c-105">\_Struttura dei dati MPCLEAN</span><span class="sxs-lookup"><span data-stu-id="8d12c-105">MPCLEAN\_DATA structure</span></span>

<span data-ttu-id="8d12c-106">Dati di notifica passati alla funzione di callback pulita.</span><span class="sxs-lookup"><span data-stu-id="8d12c-106">Notification data passed to clean callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d12c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d12c-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a><span data-ttu-id="8d12c-108">Members</span><span class="sxs-lookup"><span data-stu-id="8d12c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8d12c-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="8d12c-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="8d12c-110">Tipo: **MPTHREAT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="8d12c-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="8d12c-111">Identificatore di minaccia per **MPNOTIFY \_ Clean \_ Threat \_ Start** / **MPNOTIFY \_ Clean \_ Threat \_ succeeded** / **MPNOTIFY \_ Clean \_ Threat \_ failed** Events.</span><span class="sxs-lookup"><span data-stu-id="8d12c-111">Threat identifier for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="8d12c-112">Il bit superiore è impostato in modo da identificare le minacce correlate all'antivirus.</span><span class="sxs-lookup"><span data-stu-id="8d12c-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="8d12c-113">**ThreatAction**</span><span class="sxs-lookup"><span data-stu-id="8d12c-113">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="8d12c-114">Tipo: **[ **\_ azione MPTHREAT**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="8d12c-114">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8d12c-115">Azione di minaccia per **MPNOTIFY \_ Clean \_ Threat \_ Start** / **MPNOTIFY \_ Clean \_ Threat \_ succeeded** / **MPNOTIFY \_ Clean \_ Threat \_ failed** Events.</span><span class="sxs-lookup"><span data-stu-id="8d12c-115">Threat action for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="8d12c-116">Vedere [**\_ azione MPTHREAT**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="8d12c-116">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d12c-117">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="8d12c-117">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="8d12c-118">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d12c-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d12c-119">Stato o azioni aggiuntive associate all'azione eseguita.</span><span class="sxs-lookup"><span data-stu-id="8d12c-119">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="8d12c-120">Si tratta di una combinazione di flag di bit del [**\_ flag MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="8d12c-120">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d12c-121">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="8d12c-121">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8d12c-122">Tipo: **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="8d12c-122">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="8d12c-123">Informazioni sulle risorse per la **MPNOTIFY \_ Clean \_ Threat \_ Start** / **MPNOTIFY \_ Clean \_ Threat \_ succeeded** / **MPNOTIFY \_ Clean \_ Threat \_ failed** Events.</span><span class="sxs-lookup"><span data-stu-id="8d12c-123">Resource information for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="8d12c-124">Vedere [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="8d12c-124">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d12c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d12c-125">Requirements</span></span>



| <span data-ttu-id="8d12c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d12c-126">Requirement</span></span> | <span data-ttu-id="8d12c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8d12c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d12c-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d12c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8d12c-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8d12c-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8d12c-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d12c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8d12c-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8d12c-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d12c-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d12c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d12c-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d12c-133"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d12c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d12c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d12c-135">**\_informazioni MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="8d12c-135">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="8d12c-136">**\_flag MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="8d12c-136">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="8d12c-137">**\_azione MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="8d12c-137">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





