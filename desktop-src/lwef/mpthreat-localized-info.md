---
title: Struttura MPTHREAT_LOCALIZED_INFO (MpClient. h)
description: Informazioni localizzate per una minaccia.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- Struttura MPTHREAT_LOCALIZED_INFO le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_LOCALIZED_INFO
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400595"
---
# <a name="mpthreat_localized_info-structure"></a><span data-ttu-id="dd555-105">\_Struttura delle informazioni localizzate MPTHREAT \_</span><span class="sxs-lookup"><span data-stu-id="dd555-105">MPTHREAT\_LOCALIZED\_INFO structure</span></span>

<span data-ttu-id="dd555-106">Informazioni localizzate per una minaccia.</span><span class="sxs-lookup"><span data-stu-id="dd555-106">Localized information for a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd555-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd555-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a><span data-ttu-id="dd555-108">Members</span><span class="sxs-lookup"><span data-stu-id="dd555-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dd555-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="dd555-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="dd555-110">Tipo: **MPTHREAT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="dd555-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="dd555-111">Identificatore della minaccia.</span><span class="sxs-lookup"><span data-stu-id="dd555-111">Threat identifier.</span></span> <span data-ttu-id="dd555-112">Il bit superiore è impostato in modo da identificare le minacce correlate all'antivirus.</span><span class="sxs-lookup"><span data-stu-id="dd555-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-113">**CategoryName**</span><span class="sxs-lookup"><span data-stu-id="dd555-113">**CategoryName**</span></span>
</dt> <dd>

<span data-ttu-id="dd555-114">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="dd555-114">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="dd555-115">Classificazione delle minacce, ad esempio un Trojan o un keylogger.</span><span class="sxs-lookup"><span data-stu-id="dd555-115">Threat classification, such as a trojan or a keylogger.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-116">**CategoryDescription**</span><span class="sxs-lookup"><span data-stu-id="dd555-116">**CategoryDescription**</span></span>
</dt> <dd>

<span data-ttu-id="dd555-117">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="dd555-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="dd555-118">Descrizione della categoria di minacce.</span><span class="sxs-lookup"><span data-stu-id="dd555-118">Description of threat category.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-119">**Gravitàname**</span><span class="sxs-lookup"><span data-stu-id="dd555-119">**SeverityName**</span></span>
</dt> <dd>

<span data-ttu-id="dd555-120">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="dd555-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="dd555-121">Livello di gravità della minaccia, ad esempio grave o moderato.</span><span class="sxs-lookup"><span data-stu-id="dd555-121">Threat severity level, such as severe or moderate.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-122">**SeverityDescription**</span><span class="sxs-lookup"><span data-stu-id="dd555-122">**SeverityDescription**</span></span>
</dt> <dd>

<span data-ttu-id="dd555-123">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="dd555-123">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="dd555-124">Descrizione del livello di gravità della minaccia.</span><span class="sxs-lookup"><span data-stu-id="dd555-124">Description of threat severity level.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-125">**ShortDescription**</span><span class="sxs-lookup"><span data-stu-id="dd555-125">**ShortDescription**</span></span>
</dt> <dd>

<span data-ttu-id="dd555-126">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="dd555-126">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="dd555-127">Breve descrizione della minaccia.</span><span class="sxs-lookup"><span data-stu-id="dd555-127">Short description of threat.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-128">**DefaultActionName;**</span><span class="sxs-lookup"><span data-stu-id="dd555-128">**DefaultActionName;**</span></span>
</dt> <dd>

<span data-ttu-id="dd555-129">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="dd555-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="dd555-130">Nome dell'azione predefinita, ad esempio Remove o Quarantine, suggerito dal motore.</span><span class="sxs-lookup"><span data-stu-id="dd555-130">Name of default action, such as remove or quarantine, suggested by engine.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-131">**Advice**</span><span class="sxs-lookup"><span data-stu-id="dd555-131">**Advice**</span></span>
</dt> <dd>

<span data-ttu-id="dd555-132">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="dd555-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="dd555-133">Suggerimenti per la minaccia particolare.</span><span class="sxs-lookup"><span data-stu-id="dd555-133">Advice for the particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-134">**ThreatUrl**</span><span class="sxs-lookup"><span data-stu-id="dd555-134">**ThreatUrl**</span></span>
</dt> <dd>

<span data-ttu-id="dd555-135">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="dd555-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="dd555-136">URL di una pagina Web contenente informazioni sulla minaccia.</span><span class="sxs-lookup"><span data-stu-id="dd555-136">A URL to a webpage containing information about the threat.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd555-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd555-137">Requirements</span></span>



| <span data-ttu-id="dd555-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd555-138">Requirement</span></span> | <span data-ttu-id="dd555-139">Valore</span><span class="sxs-lookup"><span data-stu-id="dd555-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd555-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd555-140">Minimum supported client</span></span><br/> | <span data-ttu-id="dd555-141">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dd555-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dd555-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd555-142">Minimum supported server</span></span><br/> | <span data-ttu-id="dd555-143">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dd555-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd555-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd555-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd555-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd555-145"><dt>MpClient.h</dt></span></span> </dl> |



 

 





