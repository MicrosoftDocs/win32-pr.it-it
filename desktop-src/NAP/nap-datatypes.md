---
title: Tipi di tipo di protezione accesso alla rete (NapTypes. h)
description: Nota la piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10 i tipi di dati per l'API di protezione accesso alla rete (NAP) sono i seguenti.
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- ProbationTime
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- Percentuale
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964718"
---
# <a name="nap-datatypes"></a><span data-ttu-id="fd745-114">Tipi di tipo di protezione accesso alla rete</span><span class="sxs-lookup"><span data-stu-id="fd745-114">NAP Datatypes</span></span>

> [!Note]  
> <span data-ttu-id="fd745-115">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="fd745-115">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fd745-116">Di seguito sono riportati i tipi di dati per l'API di protezione accesso alla rete (NAP).</span><span class="sxs-lookup"><span data-stu-id="fd745-116">The datatypes for the Network Access Protection (NAP) API are as follows.</span></span>


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

<span data-ttu-id="fd745-117">**ProbationTime**</span><span class="sxs-lookup"><span data-stu-id="fd745-117">**ProbationTime**</span></span>
</dt> <dd>

<span data-ttu-id="fd745-118">Struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) che contiene un'ora relativa alla prova di un computer client.</span><span class="sxs-lookup"><span data-stu-id="fd745-118">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains a time related to a client machine's probation.</span></span>

</dd> <dt>

<span data-ttu-id="fd745-119">**ProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="fd745-119">**ProtocolMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="fd745-120">Valore che specifica l'intervallo di valori possibili per la dimensione massima, in byte, di un pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) definito dall'intervallo ([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="fd745-120">A value that specifies the range of possible values for the maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet as defined by range([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="fd745-121">**NapComponentId**</span><span class="sxs-lookup"><span data-stu-id="fd745-121">**NapComponentId**</span></span>
</dt> <dd>

<span data-ttu-id="fd745-122">Identificatore univoco a 4 byte utilizzato da SHAs, SHV e client di imposizione per identificarsi autonomamente.</span><span class="sxs-lookup"><span data-stu-id="fd745-122">A unique 4-byte identifier used by SHAs, SHVs and enforcement clients to identify themselves.</span></span> <span data-ttu-id="fd745-123">I primi tre byte sono il codice SMI assegnato dall'IETF del fornitore e l'ultimo byte identifica il componente stesso.</span><span class="sxs-lookup"><span data-stu-id="fd745-123">The first three bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="fd745-124">**SystemHealthEntityId**</span><span class="sxs-lookup"><span data-stu-id="fd745-124">**SystemHealthEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="fd745-125">Valore **NapComponentId** utilizzato per identificare le coppie Sha/di convalida integrità.</span><span class="sxs-lookup"><span data-stu-id="fd745-125">A **NapComponentId** value used to identify SHA/SHV pairs.</span></span>

</dd> <dt>

<span data-ttu-id="fd745-126">**EnforcementEntityId**</span><span class="sxs-lookup"><span data-stu-id="fd745-126">**EnforcementEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="fd745-127">Valore **NapComponentId** usato per identificare i client di imposizione.</span><span class="sxs-lookup"><span data-stu-id="fd745-127">A **NapComponentId** value used to identify enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="fd745-128">**SystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="fd745-128">**SystemHealthEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="fd745-129">Valore che specifica il numero di SHAs registrati nel sistema NAP nell'intervallo compreso tra 0 (zero) e [**maxSystemHealthEntityCount**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fd745-129">A value that specifies the number of registered SHAs in the NAP system in the range 0 (zero) to [**maxSystemHealthEntityCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd745-130">**EnforcementEntityCount**</span><span class="sxs-lookup"><span data-stu-id="fd745-130">**EnforcementEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="fd745-131">Valore che specifica il numero di client di imposizione nel sistema NAP nell'intervallo compreso tra 0 (zero) e [**maxEnforcerCount**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fd745-131">A value that specifies the number of enforcement clients in the NAP system in the range 0 (zero) to [**maxEnforcerCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd745-132">**StringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="fd745-132">**StringCorrelationId**</span></span>
</dt> <dd>

<span data-ttu-id="fd745-133">Versione [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) di una struttura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) utilizzata per associare [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) a **SoHResponses**.</span><span class="sxs-lookup"><span data-stu-id="fd745-133">The [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) version of a [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure used to pair [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) to **SoHResponses**.</span></span>

</dd> <dt>

<span data-ttu-id="fd745-134">**ConnectionId**</span><span class="sxs-lookup"><span data-stu-id="fd745-134">**ConnectionId**</span></span>
</dt> <dd>

<span data-ttu-id="fd745-135">Identificatore univoco globale (GUID) univoco utilizzato per identificare le connessioni NAP gestite dai client di imposizione.</span><span class="sxs-lookup"><span data-stu-id="fd745-135">A unique Globally Unique Identifier (GUID) used to identify a NAP connections maintained by enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="fd745-136">**Percentuale**</span><span class="sxs-lookup"><span data-stu-id="fd745-136">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="fd745-137">Valore che contiene la percentuale compresa tra 0 (zero) e 100 di monitoraggio e aggiornamento completato</span><span class="sxs-lookup"><span data-stu-id="fd745-137">A value that contains the percentage between 0 (zero) and 100 of remediation that is complete</span></span>

</dd> <dt>

<span data-ttu-id="fd745-138">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="fd745-138">**MessageId**</span></span>
</dt> <dd>

<span data-ttu-id="fd745-139">Valore univoco utilizzato per identificare i messaggi di sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="fd745-139">A unique value used to identify NAP system messages.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd745-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd745-140">Requirements</span></span>



| <span data-ttu-id="fd745-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd745-141">Requirement</span></span> | <span data-ttu-id="fd745-142">Valore</span><span class="sxs-lookup"><span data-stu-id="fd745-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd745-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd745-143">Minimum supported client</span></span><br/> | <span data-ttu-id="fd745-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd745-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="fd745-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd745-145">Minimum supported server</span></span><br/> | <span data-ttu-id="fd745-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd745-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="fd745-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd745-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd745-148"><dt>NapTypes. h; </dt> <dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd745-148"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



 

