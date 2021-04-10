---
title: Struttura MPSIGUPDATE_DATA (MpClient. h)
description: Dati di notifica passati alla funzione di callback dell'aggiornamento della firma.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- Struttura MPSIGUPDATE_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSIGUPDATE_DATA
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120343"
---
# <a name="mpsigupdate_data-structure"></a><span data-ttu-id="2e49e-105">\_Struttura dei dati MPSIGUPDATE</span><span class="sxs-lookup"><span data-stu-id="2e49e-105">MPSIGUPDATE\_DATA structure</span></span>

<span data-ttu-id="2e49e-106">Dati di notifica passati alla funzione di callback dell'aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="2e49e-106">Notification data passed to the signature update callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e49e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e49e-107">Syntax</span></span>


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a><span data-ttu-id="2e49e-108">Members</span><span class="sxs-lookup"><span data-stu-id="2e49e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e49e-109">**dwPercentComplete**</span><span class="sxs-lookup"><span data-stu-id="2e49e-109">**dwPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="2e49e-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2e49e-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2e49e-111">Stima della percentuale in tutti gli aggiornamenti scaricati e/o installati.</span><span class="sxs-lookup"><span data-stu-id="2e49e-111">An estimate of the percentage across all the updates that have been downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="2e49e-112">**dwTotalUpdates**</span><span class="sxs-lookup"><span data-stu-id="2e49e-112">**dwTotalUpdates**</span></span>
</dt> <dd>

<span data-ttu-id="2e49e-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2e49e-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2e49e-114">Numero totale di aggiornamenti da scaricare e/o installare.</span><span class="sxs-lookup"><span data-stu-id="2e49e-114">Total number of updates to download and/or install.</span></span>

</dd> <dt>

<span data-ttu-id="2e49e-115">**dwCurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="2e49e-115">**dwCurrentUpdateIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2e49e-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2e49e-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2e49e-117">Valore di indice in base zero che specifica quale aggiornamento tra quelli richiesti è attualmente in fase di download e/o di installazione.</span><span class="sxs-lookup"><span data-stu-id="2e49e-117">Zero-based index value that specifies which update among those required is currently being downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="2e49e-118">**eType**</span><span class="sxs-lookup"><span data-stu-id="2e49e-118">**eType**</span></span>
</dt> <dd>

<span data-ttu-id="2e49e-119">Tipo: **MPSIGUPDATE \_**</span><span class="sxs-lookup"><span data-stu-id="2e49e-119">Type: **MPSIGUPDATE\_TYPE**</span></span>

</dd> <dd>

<span data-ttu-id="2e49e-120">Tipo di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2e49e-120">Update type.</span></span> <span data-ttu-id="2e49e-121">Uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="2e49e-121">One of the following possible values:</span></span>



| <span data-ttu-id="2e49e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2e49e-122">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="2e49e-123">Significato</span><span class="sxs-lookup"><span data-stu-id="2e49e-123">Meaning</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <span data-ttu-id="2e49e-124"><dt>**\_tipo MPSIGUPDATE \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-124"><dt>**MPSIGUPDATE\_TYPE\_NONE**</dt></span></span> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <span data-ttu-id="2e49e-125"><dt>**\_tipo MPSIGUPDATE \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-125"><dt>**MPSIGUPDATE\_TYPE\_MANAGED**</dt></span></span> </dl>                                   | <span data-ttu-id="2e49e-126">Aggiornamento WSUS.</span><span class="sxs-lookup"><span data-stu-id="2e49e-126">WSUS update.</span></span> <span data-ttu-id="2e49e-127">Annulla è necessario disporre dei diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="2e49e-127">Cancel requires administrator rights.</span></span><br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <span data-ttu-id="2e49e-128"><dt>**MPSIGUPDATE \_ tipo \_ http**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-128"><dt>**MPSIGUPDATE\_TYPE\_HTTP**</dt></span></span> </dl>                                            | <span data-ttu-id="2e49e-129">Aggiornamento HTTP.</span><span class="sxs-lookup"><span data-stu-id="2e49e-129">HTTP update.</span></span> <span data-ttu-id="2e49e-130">Diritti di amministratore non necessari per l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="2e49e-130">Administrator rights not needed to cancel.</span></span><br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <span data-ttu-id="2e49e-131"><dt>**MPSIGUPDATE \_ digitare \_ http \_ SRV**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-131"><dt>**MPSIGUPDATE\_TYPE\_HTTP\_SRV**</dt></span></span> </dl>                               | <span data-ttu-id="2e49e-132">HTTP dal servizio.</span><span class="sxs-lookup"><span data-stu-id="2e49e-132">HTTP from service.</span></span> <span data-ttu-id="2e49e-133">Annulla è necessario disporre dei diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="2e49e-133">Cancel requires administrator rights.</span></span><br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <span data-ttu-id="2e49e-134"><dt>**\_UNC di tipo MPSIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-134"><dt>**MPSIGUPDATE\_TYPE\_UNC**</dt></span></span> </dl>                                               | <span data-ttu-id="2e49e-135">Condivisione UNC.</span><span class="sxs-lookup"><span data-stu-id="2e49e-135">UNC share.</span></span> <span data-ttu-id="2e49e-136">Diritti di amministratore non necessari per l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="2e49e-136">Administrator rights not needed to cancel.</span></span><br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <span data-ttu-id="2e49e-137"><dt>**tipo di MPSIGUPDATE \_ \_ non gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-137"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED**</dt></span></span> </dl>                             | <span data-ttu-id="2e49e-138">Aggiornamento di MU/WU.</span><span class="sxs-lookup"><span data-stu-id="2e49e-138">MU/WU update.</span></span> <span data-ttu-id="2e49e-139">Annulla è necessario disporre dei diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="2e49e-139">Cancel requires administrator rights.</span></span><br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <span data-ttu-id="2e49e-140"><dt>**\_ \_ piattaforma gestita di tipo MPSIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-140"><dt>**MPSIGUPDATE\_TYPE\_MANAGED\_PLATFORM**</dt></span></span> </dl>       | <span data-ttu-id="2e49e-141">Aggiornamento WSUS per la piattaforma.</span><span class="sxs-lookup"><span data-stu-id="2e49e-141">WSUS update for PLATFORM.</span></span> <span data-ttu-id="2e49e-142">Annulla è necessario disporre dei diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="2e49e-142">Cancel requires administrator rights.</span></span><br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <span data-ttu-id="2e49e-143"><dt>**MPSIGUPDATE \_ tipo \_ piattaforma non gestita \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-143"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED\_PLATFORM**</dt></span></span> </dl> | <span data-ttu-id="2e49e-144">Aggiornamento di MU/WU per la piattaforma.</span><span class="sxs-lookup"><span data-stu-id="2e49e-144">MU/WU update for PLATFORM.</span></span> <span data-ttu-id="2e49e-145">Annulla è necessario disporre dei diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="2e49e-145">Cancel requires administrator rights.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2e49e-146">**Fase**</span><span class="sxs-lookup"><span data-stu-id="2e49e-146">**Stage**</span></span>
</dt> <dd>

<span data-ttu-id="2e49e-147">Tipo: **\_ \_ fase di aggiornamento MP**</span><span class="sxs-lookup"><span data-stu-id="2e49e-147">Type: **MP\_UPDATE\_STAGE**</span></span>

</dd> <dd>

<span data-ttu-id="2e49e-148">Fase di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2e49e-148">Update stage.</span></span> <span data-ttu-id="2e49e-149">Uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="2e49e-149">One of the following possible values:</span></span>



| <span data-ttu-id="2e49e-150">Valore</span><span class="sxs-lookup"><span data-stu-id="2e49e-150">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="2e49e-151">Significato</span><span class="sxs-lookup"><span data-stu-id="2e49e-151">Meaning</span></span>                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <span data-ttu-id="2e49e-152"><dt>**\_fase MP \_ sconosciuta**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-152"><dt>**MP\_STAGE\_UNKNOWN**</dt></span></span> </dl>       | <span data-ttu-id="2e49e-153">La fase di aggiornamento è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="2e49e-153">Update stage unknown.</span></span><br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <span data-ttu-id="2e49e-154"><dt>**\_aggiornamento ricerca \_ MP**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-154"><dt>**MP\_SEARCH\_UPDATE**</dt></span></span> </dl>       | <span data-ttu-id="2e49e-155">Fase di ricerca dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2e49e-155">Update search stage.</span></span><br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <span data-ttu-id="2e49e-156"><dt>**\_aggiornamento del download MP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-156"><dt>**MP\_DOWNLOAD\_UPDATE**</dt></span></span> </dl> | <span data-ttu-id="2e49e-157">Fase di download dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2e49e-157">Update download stage.</span></span><br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <span data-ttu-id="2e49e-158"><dt>**\_aggiornamento installazione \_ MP**</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-158"><dt>**MP\_INSTALL\_UPDATE**</dt></span></span> </dl>    | <span data-ttu-id="2e49e-159">Aggiornare la fase di installazione.</span><span class="sxs-lookup"><span data-stu-id="2e49e-159">Update install stage.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="2e49e-160">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="2e49e-160">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="2e49e-161">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="2e49e-161">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="2e49e-162">Percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2e49e-162">Update path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e49e-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e49e-163">Requirements</span></span>



| <span data-ttu-id="2e49e-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e49e-164">Requirement</span></span> | <span data-ttu-id="2e49e-165">Valore</span><span class="sxs-lookup"><span data-stu-id="2e49e-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e49e-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e49e-166">Minimum supported client</span></span><br/> | <span data-ttu-id="2e49e-167">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2e49e-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2e49e-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e49e-168">Minimum supported server</span></span><br/> | <span data-ttu-id="2e49e-169">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2e49e-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e49e-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e49e-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e49e-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e49e-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





