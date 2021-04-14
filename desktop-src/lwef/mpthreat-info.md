---
title: Struttura MPTHREAT_INFO (MpClient. h)
description: Contiene informazioni su una minaccia.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- Struttura MPTHREAT_INFO le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_INFO
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478737"
---
# <a name="mpthreat_info-structure"></a><span data-ttu-id="3e496-105">Struttura delle informazioni di MPTHREAT \_</span><span class="sxs-lookup"><span data-stu-id="3e496-105">MPTHREAT\_INFO structure</span></span>

<span data-ttu-id="3e496-106">Contiene informazioni su una minaccia.</span><span class="sxs-lookup"><span data-stu-id="3e496-106">Contains information about a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e496-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e496-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a><span data-ttu-id="3e496-108">Members</span><span class="sxs-lookup"><span data-stu-id="3e496-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3e496-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="3e496-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-110">Tipo: **MPTHREAT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="3e496-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-111">Identificatore della minaccia.</span><span class="sxs-lookup"><span data-stu-id="3e496-111">Threat identifier.</span></span> <span data-ttu-id="3e496-112">Il bit superiore è impostato in modo da identificare le minacce correlate all'antivirus.</span><span class="sxs-lookup"><span data-stu-id="3e496-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-113">**DetectionID**</span><span class="sxs-lookup"><span data-stu-id="3e496-113">**DetectionID**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-114">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="3e496-114">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-115">ID rilevamento.</span><span class="sxs-lookup"><span data-stu-id="3e496-115">Detection ID.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-116">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3e496-116">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-117">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="3e496-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-118">Nome della minaccia.</span><span class="sxs-lookup"><span data-stu-id="3e496-118">Threat name.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-119">**ThreatType**</span><span class="sxs-lookup"><span data-stu-id="3e496-119">**ThreatType**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-120">Tipo: **[ **MPTHREAT \_**](mpthreat-type.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-120">Type: **[**MPTHREAT\_TYPE**](mpthreat-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-121">Tipo di minaccia.</span><span class="sxs-lookup"><span data-stu-id="3e496-121">Threat type.</span></span> <span data-ttu-id="3e496-122">Usato per distinguere tra tipi di minacce diversi, ad esempio noti non validi, sconosciuti o noti.</span><span class="sxs-lookup"><span data-stu-id="3e496-122">Used to differentiate among different threat types such as known bad, unknown, or known good.</span></span> <span data-ttu-id="3e496-123">Vedere [**MPTHREAT \_ Type**](mpthreat-type.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-123">See [**MPTHREAT\_TYPE**](mpthreat-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-124">**ThreatCriticality**</span><span class="sxs-lookup"><span data-stu-id="3e496-124">**ThreatCriticality**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-125">Tipo: **[ **\_ gravità MPTHREAT**](mpthreat-severity.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-125">Type: **[**MPTHREAT\_SEVERITY**](mpthreat-severity.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-126">Criticità della minaccia.</span><span class="sxs-lookup"><span data-stu-id="3e496-126">Threat criticality.</span></span> <span data-ttu-id="3e496-127">Vedere [**\_ gravità MPTHREAT**](mpthreat-severity.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-127">See [**MPTHREAT\_SEVERITY**](mpthreat-severity.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-128">**ThreatCategory**</span><span class="sxs-lookup"><span data-stu-id="3e496-128">**ThreatCategory**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-129">Tipo: **[ **MPTHREAT \_ categoria**](mpthreat-category.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-129">Type: **[**MPTHREAT\_CATEGORY**](mpthreat-category.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-130">Categoria di minacce, ad esempio un Trojan o un keylogger.</span><span class="sxs-lookup"><span data-stu-id="3e496-130">Threat category, such as a trojan or a keylogger.</span></span> <span data-ttu-id="3e496-131">Vedere [**la \_ categoria MPTHREAT**](mpthreat-category.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-131">See [**MPTHREAT\_CATEGORY**](mpthreat-category.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-132">**ThreatShortDescriptionID**</span><span class="sxs-lookup"><span data-stu-id="3e496-132">**ThreatShortDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-133">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e496-133">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-134">ID breve della descrizione della minaccia.</span><span class="sxs-lookup"><span data-stu-id="3e496-134">Threat short description ID.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-135">**ThreatAdviseDescriptionID**</span><span class="sxs-lookup"><span data-stu-id="3e496-135">**ThreatAdviseDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-136">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e496-136">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-137">ID descrizione della notifica di minaccia.</span><span class="sxs-lookup"><span data-stu-id="3e496-137">Threat advise description ID.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-138">**ThreatStatus**</span><span class="sxs-lookup"><span data-stu-id="3e496-138">**ThreatStatus**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-139">Tipo: **[ **\_ stato MPTHREAT**](mpthreat-status.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-139">Type: **[**MPTHREAT\_STATUS**](mpthreat-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-140">Stato della minaccia, ad esempio rilevato, pulito o in quarantena.</span><span class="sxs-lookup"><span data-stu-id="3e496-140">Threat status such as detected, cleaned, or quarantined.</span></span> <span data-ttu-id="3e496-141">Vedere [**\_ lo stato di MPTHREAT**](mpthreat-status.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-141">See [**MPTHREAT\_STATUS**](mpthreat-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-142">**SuggestedActionCount**</span><span class="sxs-lookup"><span data-stu-id="3e496-142">**SuggestedActionCount**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-143">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e496-143">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-144">Conteggio delle azioni suggerite in **SuggestedActionArray**.</span><span class="sxs-lookup"><span data-stu-id="3e496-144">Count of suggested actions in **SuggestedActionArray**.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-145">**SuggestedActionArray**</span><span class="sxs-lookup"><span data-stu-id="3e496-145">**SuggestedActionArray**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-146">Tipo: **[**MPTHREAT \_ Action**](mpthreat-action.md) \[ MP \_ Max \_ suggestions\]**</span><span class="sxs-lookup"><span data-stu-id="3e496-146">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)\[MP\_MAX\_SUGGESTIONS\]**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-147">Matrice di azioni suggerite.</span><span class="sxs-lookup"><span data-stu-id="3e496-147">Array of suggested actions.</span></span> <span data-ttu-id="3e496-148">Vedere [**\_ azione MPTHREAT**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-148">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-149">**ResourceCount**</span><span class="sxs-lookup"><span data-stu-id="3e496-149">**ResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-150">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e496-150">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-151">Numero di risorse in **Resources**.</span><span class="sxs-lookup"><span data-stu-id="3e496-151">Count of resources in **ResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-152">**ResourceList**</span><span class="sxs-lookup"><span data-stu-id="3e496-152">**ResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-153">Tipo: \**PMPRESOURCE \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="3e496-153">Type: \**PMPRESOURCE\_INFO\** _</span></span>

</dd> <dd>

<span data-ttu-id="3e496-154">Elenco di risorse identificato con la minaccia.</span><span class="sxs-lookup"><span data-stu-id="3e496-154">List of resources identified with the threat.</span></span> <span data-ttu-id="3e496-155">Vedere [_ *MPRESOURCE \_ info* \*](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-155">See [_ *MPRESOURCE\_INFO*\*](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-156">**ThreatStatusTime**</span><span class="sxs-lookup"><span data-stu-id="3e496-156">**ThreatStatusTime**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-157">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="3e496-157">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-158">Ora dell'Ultima modifica dello stato della minaccia.</span><span class="sxs-lookup"><span data-stu-id="3e496-158">Time when threat status last changed.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-159">**ThreatStatusCode**</span><span class="sxs-lookup"><span data-stu-id="3e496-159">**ThreatStatusCode**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-160">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3e496-160">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-161">Codice di stato associato allo stato della minaccia.</span><span class="sxs-lookup"><span data-stu-id="3e496-161">Status code associated with the threat status.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-162">**ThreatDetection**</span><span class="sxs-lookup"><span data-stu-id="3e496-162">**ThreatDetection**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-163">Tipo: **[ **\_ rilevamento MPTHREAT**](mpthreat-detection.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-163">Type: **[**MPTHREAT\_DETECTION**](mpthreat-detection.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-164">Tipo di rilevamento delle minacce, ad esempio concreto, sospetto o generico.</span><span class="sxs-lookup"><span data-stu-id="3e496-164">Threat detection type, such as concrete, suspicious, or generic.</span></span> <span data-ttu-id="3e496-165">Vedere [**\_ rilevamento MPTHREAT**](mpthreat-detection.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-165">See [**MPTHREAT\_DETECTION**](mpthreat-detection.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-166">**QuarantineGuid**</span><span class="sxs-lookup"><span data-stu-id="3e496-166">**QuarantineGuid**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-167">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="3e496-167">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-168">GUID di quarantena.</span><span class="sxs-lookup"><span data-stu-id="3e496-168">Quarantine guid.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-169">**ExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="3e496-169">**ExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-170">Tipo: **[ **\_ stato MPEXECUTION**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-170">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-171">Stato di esecuzione della minaccia, ad esempio non noto, bloccato o attivo.</span><span class="sxs-lookup"><span data-stu-id="3e496-171">Execution status of the threat, such as not known, blocked, or active.</span></span> <span data-ttu-id="3e496-172">Vedere [**\_ lo stato di MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-172">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-173">**Dati**</span><span class="sxs-lookup"><span data-stu-id="3e496-173">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-174">Informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="3e496-174">Extra information.</span></span> <span data-ttu-id="3e496-175">Il puntatore alla struttura appropriata dipende dal valore di **ThreatType**.</span><span class="sxs-lookup"><span data-stu-id="3e496-175">The pointer to the appropriate structure depends on the value of **ThreatType**.</span></span>

<dl> <dt>

<span data-ttu-id="3e496-176">**pKnownBad**</span><span class="sxs-lookup"><span data-stu-id="3e496-176">**pKnownBad**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-177">Tipo: **PMPTHREAT \_ INFOEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="3e496-177">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-178">Quando **ThreatType**  ==  **MPTHREAT \_ digitare \_ KNOWNBAD**.</span><span class="sxs-lookup"><span data-stu-id="3e496-178">When **ThreatType** == **MPTHREAT\_TYPE\_KNOWNBAD**.</span></span> <span data-ttu-id="3e496-179">Vedere [**MPTHREAT \_ INFOEX \_ inutilizzato**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-179">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-180">**pBehavior**</span><span class="sxs-lookup"><span data-stu-id="3e496-180">**pBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-181">Tipo: **PMPTHREAT \_ INFOEX \_ Behavior**</span><span class="sxs-lookup"><span data-stu-id="3e496-181">Type: **PMPTHREAT\_INFOEX\_BEHAVIOR**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-182">Quando **ThreatType**  ==  **MPTHREAT \_ il \_ comportamento del tipo**.</span><span class="sxs-lookup"><span data-stu-id="3e496-182">When **ThreatType** == **MPTHREAT\_TYPE\_BEHAVIOR**.</span></span> <span data-ttu-id="3e496-183">Vedere [**MPTHREAT \_ INFOEX \_ Behavior**](mpthreat-infoex-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-183">See [**MPTHREAT\_INFOEX\_BEHAVIOR**](mpthreat-infoex-behavior.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-184">**pUnknown**</span><span class="sxs-lookup"><span data-stu-id="3e496-184">**pUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-185">Tipo: **PMPTHREAT \_ INFOEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="3e496-185">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-186">Quando **ThreatType**  ==  **MPTHREAT \_ tipo \_ sconosciuto**.</span><span class="sxs-lookup"><span data-stu-id="3e496-186">When **ThreatType** == **MPTHREAT\_TYPE\_UNKNOWN**.</span></span> <span data-ttu-id="3e496-187">Vedere [**MPTHREAT \_ INFOEX \_ inutilizzato**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-187">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-188">**pKnownGood**</span><span class="sxs-lookup"><span data-stu-id="3e496-188">**pKnownGood**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-189">Tipo: **PMPTHREAT \_ INFOEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="3e496-189">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-190">Quando **ThreatType** = = MPTHREAT \_ \_ , digitare KNOWNGOOD.</span><span class="sxs-lookup"><span data-stu-id="3e496-190">When **ThreatType** == MPTHREAT\_TYPE\_KNOWNGOOD.</span></span> <span data-ttu-id="3e496-191">Vedere [**MPTHREAT \_ INFOEX \_ inutilizzato**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-191">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-192">**pNis**</span><span class="sxs-lookup"><span data-stu-id="3e496-192">**pNis**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-193">Tipo: **PMPTHREAT \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="3e496-193">Type: **PMPTHREAT\_INFOEX\_NIS**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-194">Quando **ThreatType**  ==  **MPTHREAT \_ digitare \_ NIS**.</span><span class="sxs-lookup"><span data-stu-id="3e496-194">When **ThreatType** == **MPTHREAT\_TYPE\_NIS**.</span></span> <span data-ttu-id="3e496-195">Vedere [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-195">See [**MPTHREAT\_INFOEX\_NIS**](mpthreat-infoex-nis.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3e496-196">**State**</span><span class="sxs-lookup"><span data-stu-id="3e496-196">**State**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-197">Tipo: **[ **\_ stato MPDETECTION**](mpdetection-state.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-197">Type: **[**MPDETECTION\_STATE**](mpdetection-state.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-198">Stato corrente del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="3e496-198">The current state of the detection.</span></span> <span data-ttu-id="3e496-199">Vedere [**MPDETECTION \_ state**](mpdetection-state.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-199">See [**MPDETECTION\_STATE**](mpdetection-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-200">**DetectionUser**</span><span class="sxs-lookup"><span data-stu-id="3e496-200">**DetectionUser**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-201">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="3e496-201">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-202">Utente associato al rilevamento, nel formato "dominio/utente".</span><span class="sxs-lookup"><span data-stu-id="3e496-202">The user associated with the detection, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="3e496-203">**DetectionSource**</span><span class="sxs-lookup"><span data-stu-id="3e496-203">**DetectionSource**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-204">Tipo: **[ **MPSOURCE**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-204">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-205">Origine del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="3e496-205">The source of the detection.</span></span> <span data-ttu-id="3e496-206">Vedere [**MPSOURCE**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-206">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-207">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="3e496-207">**ProcessName**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-208">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="3e496-208">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-209">Nome del processo associato al rilevamento.</span><span class="sxs-lookup"><span data-stu-id="3e496-209">Process name associated with the detection.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-210">**DetectionOrigin**</span><span class="sxs-lookup"><span data-stu-id="3e496-210">**DetectionOrigin**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-211">Tipo: **[ **MPDETECTION \_ Origin**](mpdetection-origin.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-211">Type: **[**MPDETECTION\_ORIGIN**](mpdetection-origin.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-212">Origine del rilevamento, ad esempio locale o rete.</span><span class="sxs-lookup"><span data-stu-id="3e496-212">The origin of the detection, such as local or network.</span></span> <span data-ttu-id="3e496-213">Vedere [**MPDETECTION \_ Origin**](mpdetection-origin.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-213">See [**MPDETECTION\_ORIGIN**](mpdetection-origin.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-214">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="3e496-214">**reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-215">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e496-215">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-216">Metadati riservati sul rilevamento.</span><span class="sxs-lookup"><span data-stu-id="3e496-216">Reserved metadata about the detection.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-217">**DetectionTime**</span><span class="sxs-lookup"><span data-stu-id="3e496-217">**DetectionTime**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-218">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="3e496-218">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-219">Ora del rilevamento iniziale.</span><span class="sxs-lookup"><span data-stu-id="3e496-219">The time of the initial detection.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-220">**PreExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="3e496-220">**PreExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-221">Tipo: **[ **\_ stato MPEXECUTION**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-221">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-222">Stato di esecuzione immediatamente prima della correzione.</span><span class="sxs-lookup"><span data-stu-id="3e496-222">Execution status right before remediation.</span></span> <span data-ttu-id="3e496-223">Vedere [**\_ lo stato di MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-223">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-224">**RemediationTime**</span><span class="sxs-lookup"><span data-stu-id="3e496-224">**RemediationTime**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-225">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="3e496-225">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-226">È stata eseguita la correzione dell'ora.</span><span class="sxs-lookup"><span data-stu-id="3e496-226">The time remediation occured.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-227">**PostExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="3e496-227">**PostExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-228">Tipo: **[ **\_ stato MPEXECUTION**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-228">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-229">Stato di esecuzione dopo la correzione.</span><span class="sxs-lookup"><span data-stu-id="3e496-229">Execution status after remediation.</span></span> <span data-ttu-id="3e496-230">Vedere [**\_ lo stato di MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-230">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-231">**CriticalFailure**</span><span class="sxs-lookup"><span data-stu-id="3e496-231">**CriticalFailure**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-232">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="3e496-232">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-233">True se l'errore di correzione è stato critico.</span><span class="sxs-lookup"><span data-stu-id="3e496-233">True if the remediation failure was critical.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-234">**NonCriticalReason**</span><span class="sxs-lookup"><span data-stu-id="3e496-234">**NonCriticalReason**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-235">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e496-235">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-236">Il motivo per cui l'errore di correzione non è critico.</span><span class="sxs-lookup"><span data-stu-id="3e496-236">The reason the remediation failure is not critical.</span></span> <span data-ttu-id="3e496-237">Questa operazione non è garantita per essere supportata in futuro.</span><span class="sxs-lookup"><span data-stu-id="3e496-237">This is not guaranteed to be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-238">**RemediationUser**</span><span class="sxs-lookup"><span data-stu-id="3e496-238">**RemediationUser**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-239">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="3e496-239">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-240">Utente che ha richiesto la correzione, nel formato "dominio/utente".</span><span class="sxs-lookup"><span data-stu-id="3e496-240">User that requested the remediation, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="3e496-241">**RemediationResourceCount**</span><span class="sxs-lookup"><span data-stu-id="3e496-241">**RemediationResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-242">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e496-242">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-243">Numero di risorse in **RemediationResourceList**.</span><span class="sxs-lookup"><span data-stu-id="3e496-243">Count of resources in **RemediationResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-244">**RemediationResourceList**</span><span class="sxs-lookup"><span data-stu-id="3e496-244">**RemediationResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-245">Tipo: **PMPRESOURCE \_ info \[ RemediationResourceCount \]**</span><span class="sxs-lookup"><span data-stu-id="3e496-245">Type: **PMPRESOURCE\_INFO\[RemediationResourceCount\]**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-246">Elenco di risorse non riuscite durante la correzione.</span><span class="sxs-lookup"><span data-stu-id="3e496-246">List of resources that failed during remediation.</span></span> <span data-ttu-id="3e496-247">Vedere [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-247">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-248">**FailureResolved**</span><span class="sxs-lookup"><span data-stu-id="3e496-248">**FailureResolved**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-249">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="3e496-249">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-250">True se l'errore di monitoraggio e aggiornamento è stato risolto.</span><span class="sxs-lookup"><span data-stu-id="3e496-250">True if remediation failure been resolved.</span></span> <span data-ttu-id="3e496-251">Il bucket verrà spostato in modo da essere completato o da un'altra azione.</span><span class="sxs-lookup"><span data-stu-id="3e496-251">This will move the bucket to either complete or an additional action.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-252">**ResolvedReason**</span><span class="sxs-lookup"><span data-stu-id="3e496-252">**ResolvedReason**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-253">Tipo: **[ **MPRESOLVED \_ reason**](mpresolved-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="3e496-253">Type: **[**MPRESOLVED\_REASON**](mpresolved-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-254">Motivo per cui è stato risolto un errore di correzione.</span><span class="sxs-lookup"><span data-stu-id="3e496-254">Reason for remediation failure being resolved.</span></span> <span data-ttu-id="3e496-255">Questo è il motivo per cui il rilevamento è stato spostato da un'azione non riuscita o completata.</span><span class="sxs-lookup"><span data-stu-id="3e496-255">This is the reason the detection moved from failed to additional action or finished.</span></span> <span data-ttu-id="3e496-256">Vedere [**MPRESOLVED \_ reason**](mpresolved-reason.md).</span><span class="sxs-lookup"><span data-stu-id="3e496-256">See [**MPRESOLVED\_REASON**](mpresolved-reason.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e496-257">**AdditionalActions**</span><span class="sxs-lookup"><span data-stu-id="3e496-257">**AdditionalActions**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-258">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e496-258">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-259">Sono necessarie azioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="3e496-259">Are additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-260">**ResolvedActions**</span><span class="sxs-lookup"><span data-stu-id="3e496-260">**ResolvedActions**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-261">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e496-261">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-262">Eventuali azioni aggiuntive eseguite.</span><span class="sxs-lookup"><span data-stu-id="3e496-262">Any additional actions that have been performed.</span></span>

</dd> <dt>

<span data-ttu-id="3e496-263">**dwThreatStatusFlag**</span><span class="sxs-lookup"><span data-stu-id="3e496-263">**dwThreatStatusFlag**</span></span>
</dt> <dd>

<span data-ttu-id="3e496-264">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e496-264">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e496-265">Aggiuntivi Informazioni sul rilevamento delle minacce.</span><span class="sxs-lookup"><span data-stu-id="3e496-265">Additonal information about the threat detection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e496-266">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e496-266">Requirements</span></span>



| <span data-ttu-id="3e496-267">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e496-267">Requirement</span></span> | <span data-ttu-id="3e496-268">Valore</span><span class="sxs-lookup"><span data-stu-id="3e496-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e496-269">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e496-269">Minimum supported client</span></span><br/> | <span data-ttu-id="3e496-270">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3e496-270">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3e496-271">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e496-271">Minimum supported server</span></span><br/> | <span data-ttu-id="3e496-272">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3e496-272">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e496-273">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e496-273">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e496-274"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e496-274"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e496-275">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e496-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e496-276">**MpFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="3e496-276">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="3e496-277">**MpThreatEnumerate**</span><span class="sxs-lookup"><span data-stu-id="3e496-277">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> <dt>

[<span data-ttu-id="3e496-278">**MpThreatQuery**</span><span class="sxs-lookup"><span data-stu-id="3e496-278">**MpThreatQuery**</span></span>](mpthreatquery.md)
</dt> <dt>

[<span data-ttu-id="3e496-279">**\_origine MPDETECTION**</span><span class="sxs-lookup"><span data-stu-id="3e496-279">**MPDETECTION\_ORIGIN**</span></span>](mpdetection-origin.md)
</dt> <dt>

[<span data-ttu-id="3e496-280">**\_stato MPDETECTION**</span><span class="sxs-lookup"><span data-stu-id="3e496-280">**MPDETECTION\_STATE**</span></span>](mpdetection-state.md)
</dt> <dt>

[<span data-ttu-id="3e496-281">**\_stato MPEXECUTION**</span><span class="sxs-lookup"><span data-stu-id="3e496-281">**MPEXECUTION\_STATUS**</span></span>](mpexecution-status.md)
</dt> <dt>

[<span data-ttu-id="3e496-282">**\_motivo MPRESOLVED**</span><span class="sxs-lookup"><span data-stu-id="3e496-282">**MPRESOLVED\_REASON**</span></span>](mpresolved-reason.md)
</dt> <dt>

[<span data-ttu-id="3e496-283">**\_informazioni MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="3e496-283">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="3e496-284">**MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="3e496-284">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="3e496-285">**\_azione MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="3e496-285">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> <dt>

[<span data-ttu-id="3e496-286">**\_categoria MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="3e496-286">**MPTHREAT\_CATEGORY**</span></span>](mpthreat-category.md)
</dt> <dt>

[<span data-ttu-id="3e496-287">**\_rilevamento MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="3e496-287">**MPTHREAT\_DETECTION**</span></span>](mpthreat-detection.md)
</dt> <dt>

[<span data-ttu-id="3e496-288">**\_comportamento INFOEX \_ MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="3e496-288">**MPTHREAT\_INFOEX\_BEHAVIOR**</span></span>](mpthreat-infoex-behavior.md)
</dt> <dt>

[<span data-ttu-id="3e496-289">**MPTHREAT \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="3e496-289">**MPTHREAT\_INFOEX\_NIS**</span></span>](mpthreat-infoex-nis.md)
</dt> <dt>

[<span data-ttu-id="3e496-290">**MPTHREAT \_ INFOEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="3e496-290">**MPTHREAT\_INFOEX\_UNUSED**</span></span>](mpthreat-infoex-unused.md)
</dt> <dt>

[<span data-ttu-id="3e496-291">**\_gravità MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="3e496-291">**MPTHREAT\_SEVERITY**</span></span>](mpthreat-severity.md)
</dt> <dt>

[<span data-ttu-id="3e496-292">**\_stato MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="3e496-292">**MPTHREAT\_STATUS**</span></span>](mpthreat-status.md)
</dt> <dt>

[<span data-ttu-id="3e496-293">**\_tipo MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="3e496-293">**MPTHREAT\_TYPE**</span></span>](mpthreat-type.md)
</dt> </dl>

 

 





