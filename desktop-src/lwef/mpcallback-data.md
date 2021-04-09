---
title: Struttura MPCALLBACK_DATA (MpClient. h)
description: Dati passati alla funzione di callback.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- Struttura MPCALLBACK_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCALLBACK_DATA
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9741ca479eeb9770a3ae8c2aedbc51a8a2643033
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119674"
---
# <a name="mpcallback_data-structure"></a><span data-ttu-id="89df2-105">\_Struttura dei dati MPCALLBACK</span><span class="sxs-lookup"><span data-stu-id="89df2-105">MPCALLBACK\_DATA structure</span></span>

<span data-ttu-id="89df2-106">Dati passati alla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="89df2-106">Data passed to the callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="89df2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89df2-107">Syntax</span></span>


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a><span data-ttu-id="89df2-108">Members</span><span class="sxs-lookup"><span data-stu-id="89df2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="89df2-109">**Notificare**</span><span class="sxs-lookup"><span data-stu-id="89df2-109">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-110">Tipo: **[ **MPNOTIFY**](mpnotify.md)**</span><span class="sxs-lookup"><span data-stu-id="89df2-110">Type: **[**MPNOTIFY**](mpnotify.md)**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-111">Notifica di modifica per il report.</span><span class="sxs-lookup"><span data-stu-id="89df2-111">Change notification to report.</span></span>

</dd> <dt>

<span data-ttu-id="89df2-112">**hResult**</span><span class="sxs-lookup"><span data-stu-id="89df2-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="89df2-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-114">Codice di errore, in caso di errore interno.</span><span class="sxs-lookup"><span data-stu-id="89df2-114">Error code, in case of an internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="89df2-115">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="89df2-115">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-116">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="89df2-116">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-117">Timestamp corrente.</span><span class="sxs-lookup"><span data-stu-id="89df2-117">Current timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="89df2-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="89df2-118">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-119">Tipo: **[ **MPCALLBACK \_**](mpcallback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="89df2-119">Type: **[**MPCALLBACK\_TYPE**](mpcallback-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-120">Tipo di dati speciale di callback.</span><span class="sxs-lookup"><span data-stu-id="89df2-120">Callback special data type.</span></span>

</dd> <dt>

<span data-ttu-id="89df2-121">**Dati**</span><span class="sxs-lookup"><span data-stu-id="89df2-121">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-122">Richiamata di dati speciali.</span><span class="sxs-lookup"><span data-stu-id="89df2-122">Callback special data.</span></span> <span data-ttu-id="89df2-123">Il puntatore alla struttura appropriata dipende dal valore di **tipo**.</span><span class="sxs-lookup"><span data-stu-id="89df2-123">The pointer to the appropriate structure depends on the value of **Type**.</span></span>

<dl> <dt>

<span data-ttu-id="89df2-124">**pStatusData**</span><span class="sxs-lookup"><span data-stu-id="89df2-124">**pStatusData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-125">Tipo: **PMPSTATUS \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-125">Type: **PMPSTATUS\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-126">Quando **digitare**  ==  **MPCALLBACK \_ status**.</span><span class="sxs-lookup"><span data-stu-id="89df2-126">When **Type** == **MPCALLBACK\_STATUS**.</span></span> <span data-ttu-id="89df2-127">Vedere [**MPSTATUS \_ Data**](mpstatus-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-127">See [**MPSTATUS\_DATA**](mpstatus-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-128">**pScanData**</span><span class="sxs-lookup"><span data-stu-id="89df2-128">**pScanData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-129">Tipo: **PMPSCAN \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-129">Type: **PMPSCAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-130">Quando si **digita**  ==  **MPCALLBACK \_ Scan**.</span><span class="sxs-lookup"><span data-stu-id="89df2-130">When **Type** == **MPCALLBACK\_SCAN**.</span></span> <span data-ttu-id="89df2-131">Vedere [**MPSCAN \_ Data**](mpscan-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-131">See [**MPSCAN\_DATA**](mpscan-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-132">**pCleanData**</span><span class="sxs-lookup"><span data-stu-id="89df2-132">**pCleanData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-133">Tipo: **PMPCLEAN \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-133">Type: **PMPCLEAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-134">Quando il **tipo**  ==  **MPCALLBACK è \_ Clean**.</span><span class="sxs-lookup"><span data-stu-id="89df2-134">When **Type** == **MPCALLBACK\_CLEAN**.</span></span> <span data-ttu-id="89df2-135">Vedere [**MPCLEAN \_ Data**](mpclean-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-135">See [**MPCLEAN\_DATA**](mpclean-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-136">**pPrecheckData**</span><span class="sxs-lookup"><span data-stu-id="89df2-136">**pPrecheckData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-137">Tipo: **PMPCLEAN \_ Precheck \_ dati**</span><span class="sxs-lookup"><span data-stu-id="89df2-137">Type: **PMPCLEAN\_PRECHECK\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-138">Quando il **tipo**  ==  **MPCALLBACK è \_ Precheck**.</span><span class="sxs-lookup"><span data-stu-id="89df2-138">When **Type** == **MPCALLBACK\_PRECHECK**.</span></span> <span data-ttu-id="89df2-139">Vedere [**MPCLEAN \_ Precheck \_ Data**](mpclean-precheck-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-139">See [**MPCLEAN\_PRECHECK\_DATA**](mpclean-precheck-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-140">**pThreatData**</span><span class="sxs-lookup"><span data-stu-id="89df2-140">**pThreatData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-141">Tipo: **PMPTHREAT \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-141">Type: **PMPTHREAT\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-142">Quando **digitare**  ==  **MPCALLBACK \_ Threat**.</span><span class="sxs-lookup"><span data-stu-id="89df2-142">When **Type** == **MPCALLBACK\_THREAT**.</span></span> <span data-ttu-id="89df2-143">Vedere [**MPTHREAT \_ Data**](mpthreat-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-143">See [**MPTHREAT\_DATA**](mpthreat-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-144">**pSigUpdateData**</span><span class="sxs-lookup"><span data-stu-id="89df2-144">**pSigUpdateData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-145">Tipo: **PMPSIGUPDATE \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-145">Type: **PMPSIGUPDATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-146">Quando il **tipo** è  ==  **MPCALLBACK \_ SIGUPDATE**.</span><span class="sxs-lookup"><span data-stu-id="89df2-146">When **Type** == **MPCALLBACK\_SIGUPDATE**.</span></span> <span data-ttu-id="89df2-147">Vedere [**MPSIGUPDATE \_ Data**](mpsigupdate-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-147">See [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-148">**pSampleData**</span><span class="sxs-lookup"><span data-stu-id="89df2-148">**pSampleData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-149">Tipo: **PMPSAMPLE \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-149">Type: **PMPSAMPLE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-150">Quando si **digita**  ==  **MPCALLBACK \_ Sample**.</span><span class="sxs-lookup"><span data-stu-id="89df2-150">When **Type** == **MPCALLBACK\_SAMPLE**.</span></span> <span data-ttu-id="89df2-151">Vedere [**MPSAMPLE \_ Data**](mpsample-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-151">See [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-152">**pReservedData**</span><span class="sxs-lookup"><span data-stu-id="89df2-152">**pReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-153">Tipo: **PMPRESERVED \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-153">Type: **PMPRESERVED\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-154">Quando il **tipo**  ==  **MPCALLBACK è \_ riservato**.</span><span class="sxs-lookup"><span data-stu-id="89df2-154">When **Type** == **MPCALLBACK\_RESERVED**.</span></span> <span data-ttu-id="89df2-155">Vedere [**MPRESERVED \_ Data**](mpreserved-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-155">See [**MPRESERVED\_DATA**](mpreserved-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-156">**pConfigurationData**</span><span class="sxs-lookup"><span data-stu-id="89df2-156">**pConfigurationData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-157">Tipo: **PMPCONFIGURATION \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-157">Type: **PMPCONFIGURATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-158">Quando si **digita** la  ==  **\_ \_ notifica di configurazione MPCALLBACK**.</span><span class="sxs-lookup"><span data-stu-id="89df2-158">When **Type** == **MPCALLBACK\_CONFIGURATION\_NOTIFICATION**.</span></span> <span data-ttu-id="89df2-159">Vedere [**MPCONFIGURATION \_ Data**](mpconfiguration-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-159">See [**MPCONFIGURATION\_DATA**](mpconfiguration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-160">**pFastPathData**</span><span class="sxs-lookup"><span data-stu-id="89df2-160">**pFastPathData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-161">Tipo: **PMPFASTPATH \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-161">Type: **PMPFASTPATH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-162">Quando il **tipo** è  ==  **MPCALLBACK \_ FastPath**.</span><span class="sxs-lookup"><span data-stu-id="89df2-162">When **Type** == **MPCALLBACK\_FASTPATH**.</span></span> <span data-ttu-id="89df2-163">Vedere [**MPFASTPATH \_ Data**](mpfastpath-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-163">See [**MPFASTPATH\_DATA**](mpfastpath-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-164">**pExpirationData**</span><span class="sxs-lookup"><span data-stu-id="89df2-164">**pExpirationData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-165">Tipo: **PMPEXPIRATION \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-165">Type: **PMPEXPIRATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-166">Quando il **tipo**  ==  **MPCALLBACK \_ \_ scadenza del prodotto**.</span><span class="sxs-lookup"><span data-stu-id="89df2-166">When **Type** == **MPCALLBACK\_PRODUCT\_EXPIRATION**.</span></span> <span data-ttu-id="89df2-167">Vedere [**MPEXPIRATION \_ Data**](mpexpiration-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-167">See [**MPEXPIRATION\_DATA**](mpexpiration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-168">**pNISPrivateData**</span><span class="sxs-lookup"><span data-stu-id="89df2-168">**pNISPrivateData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-169">Tipo: **PMPNIS \_ private \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-169">Type: **PMPNIS\_PRIVATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-170">Quando il **tipo**  ==  **MPCALLBACK \_ NIS è \_ privato**.</span><span class="sxs-lookup"><span data-stu-id="89df2-170">When **Type** == **MPCALLBACK\_NIS\_PRIVATE**.</span></span> <span data-ttu-id="89df2-171">Vedere [**MPNIS \_ private \_ Data**](mpnis-private-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-171">See [**MPNIS\_PRIVATE\_DATA**](mpnis-private-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-172">**pHealthData**</span><span class="sxs-lookup"><span data-stu-id="89df2-172">**pHealthData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-173">Tipo: **PMPHEALTH \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-173">Type: **PMPHEALTH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-174">Quando **digitare**  ==  **MPCALLBACK \_ Health**.</span><span class="sxs-lookup"><span data-stu-id="89df2-174">When **Type** == **MPCALLBACK\_HEALTH**.</span></span> <span data-ttu-id="89df2-175">Vedere [**MPHEALTH \_ Data**](mphealth-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-175">See [**MPHEALTH\_DATA**](mphealth-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-176">**pEndOfLifeData**</span><span class="sxs-lookup"><span data-stu-id="89df2-176">**pEndOfLifeData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-177">Tipo: **PMPENDOFLIFE \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-177">Type: **PMPENDOFLIFE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-178">Quando il **tipo** è  ==  **MPCALLBACK \_ ENDOFLIFE**.</span><span class="sxs-lookup"><span data-stu-id="89df2-178">When **Type** == **MPCALLBACK\_ENDOFLIFE**.</span></span> <span data-ttu-id="89df2-179">Vedere [**MPENDOFLIFE \_ Data**](mpendoflife-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-179">See [**MPENDOFLIFE\_DATA**](mpendoflife-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="89df2-180">**pMalwareToastData**</span><span class="sxs-lookup"><span data-stu-id="89df2-180">**pMalwareToastData**</span></span>
</dt> <dd>

<span data-ttu-id="89df2-181">Tipo: **PMPMALWARETOAST \_ Data**</span><span class="sxs-lookup"><span data-stu-id="89df2-181">Type: **PMPMALWARETOAST\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="89df2-182">Quando il **tipo** è  ==  **MPCALLBACK \_ MALWARETOAST**.</span><span class="sxs-lookup"><span data-stu-id="89df2-182">When **Type** == **MPCALLBACK\_MALWARETOAST**.</span></span> <span data-ttu-id="89df2-183">Vedere [**MPMALWARETOAST \_ Data**](mpmalwaretoast-data.md).</span><span class="sxs-lookup"><span data-stu-id="89df2-183">See [**MPMALWARETOAST\_DATA**](mpmalwaretoast-data.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89df2-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89df2-184">Requirements</span></span>



| <span data-ttu-id="89df2-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="89df2-185">Requirement</span></span> | <span data-ttu-id="89df2-186">Valore</span><span class="sxs-lookup"><span data-stu-id="89df2-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89df2-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89df2-187">Minimum supported client</span></span><br/> | <span data-ttu-id="89df2-188">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="89df2-188">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="89df2-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89df2-189">Minimum supported server</span></span><br/> | <span data-ttu-id="89df2-190">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="89df2-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89df2-191">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89df2-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="89df2-192"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="89df2-192"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89df2-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89df2-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89df2-194">**\_tipo MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="89df2-194">**MPCALLBACK\_TYPE**</span></span>](mpcallback-type.md)
</dt> <dt>

[<span data-ttu-id="89df2-195">**\_dati MPCLEAN**</span><span class="sxs-lookup"><span data-stu-id="89df2-195">**MPCLEAN\_DATA**</span></span>](mpclean-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-196">**MPCLEAN \_ i dati di PREverifica \_**</span><span class="sxs-lookup"><span data-stu-id="89df2-196">**MPCLEAN\_PRECHECK\_DATA**</span></span>](mpclean-precheck-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-197">**\_dati MPCONFIGURATION**</span><span class="sxs-lookup"><span data-stu-id="89df2-197">**MPCONFIGURATION\_DATA**</span></span>](mpconfiguration-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-198">**\_dati MPENDOFLIFE**</span><span class="sxs-lookup"><span data-stu-id="89df2-198">**MPENDOFLIFE\_DATA**</span></span>](mpendoflife-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-199">**\_dati MPEXPIRATION**</span><span class="sxs-lookup"><span data-stu-id="89df2-199">**MPEXPIRATION\_DATA**</span></span>](mpexpiration-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-200">**\_dati MPFASTPATH**</span><span class="sxs-lookup"><span data-stu-id="89df2-200">**MPFASTPATH\_DATA**</span></span>](mpfastpath-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-201">**\_dati MPHEALTH**</span><span class="sxs-lookup"><span data-stu-id="89df2-201">**MPHEALTH\_DATA**</span></span>](mphealth-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-202">**\_dati MPMALWARETOAST**</span><span class="sxs-lookup"><span data-stu-id="89df2-202">**MPMALWARETOAST\_DATA**</span></span>](mpmalwaretoast-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-203">**MPNIS \_ \_ dati privati**</span><span class="sxs-lookup"><span data-stu-id="89df2-203">**MPNIS\_PRIVATE\_DATA**</span></span>](mpnis-private-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-204">**MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="89df2-204">**MPNOTIFY**</span></span>](mpnotify.md)
</dt> <dt>

[<span data-ttu-id="89df2-205">**\_dati MPRESERVED**</span><span class="sxs-lookup"><span data-stu-id="89df2-205">**MPRESERVED\_DATA**</span></span>](mpreserved-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-206">**\_dati MPSAMPLE**</span><span class="sxs-lookup"><span data-stu-id="89df2-206">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-207">**\_dati MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="89df2-207">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-208">**\_dati MPSIGUPDATE**</span><span class="sxs-lookup"><span data-stu-id="89df2-208">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-209">**\_dati MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="89df2-209">**MPSTATUS\_DATA**</span></span>](mpstatus-data.md)
</dt> <dt>

[<span data-ttu-id="89df2-210">**\_dati MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="89df2-210">**MPTHREAT\_DATA**</span></span>](mpthreat-data.md)
</dt> </dl>

 

 





