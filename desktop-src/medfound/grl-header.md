---
description: Contiene l'intestazione dell'elenco di revoche globale (GRL).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: Struttura GRL_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305368"
---
# <a name="grl_header-structure"></a><span data-ttu-id="9e2e8-103">\_Struttura dell'intestazione GRL</span><span class="sxs-lookup"><span data-stu-id="9e2e8-103">GRL\_HEADER structure</span></span>

<span data-ttu-id="9e2e8-104">Contiene l'intestazione dell'elenco di revoche globale (GRL).</span><span class="sxs-lookup"><span data-stu-id="9e2e8-104">Contains the global revocation list (GRL) header.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e2e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e2e8-105">Syntax</span></span>


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a><span data-ttu-id="9e2e8-106">Members</span><span class="sxs-lookup"><span data-stu-id="9e2e8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9e2e8-107">**wszIdentifier**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-107">**wszIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-108">Identificatore GRL.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-108">The GRL identifier.</span></span> <span data-ttu-id="9e2e8-109">Il valore è sempre L "MSGRL".</span><span class="sxs-lookup"><span data-stu-id="9e2e8-109">The value is always L"MSGRL".</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-110">**wFormatMajor**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-110">**wFormatMajor**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-111">Numero di versione principale.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-111">The major version number.</span></span> <span data-ttu-id="9e2e8-112">Attualmente, il valore deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-112">Currently the value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-113">**wFormatMinor**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-113">**wFormatMinor**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-114">Numero di versione secondario.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-114">The minor version number.</span></span> <span data-ttu-id="9e2e8-115">Attualmente, il valore deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-115">Currently the value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-116">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-116">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-117">Valore **FILETIME** che specifica quando è stato creato il file.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-117">A **FILETIME** value that specifies when the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-118">**dwSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-118">**dwSequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-119">Numero di versione di GRL.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-119">The GRL version number.</span></span> <span data-ttu-id="9e2e8-120">Attualmente, il valore deve essere almeno 3</span><span class="sxs-lookup"><span data-stu-id="9e2e8-120">Currently the value must be at least 3</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-121">**dwForceRebootVersion**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-121">**dwForceRebootVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-123">**dwForceProcessRestartVersion**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-123">**dwForceProcessRestartVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-124">Riservato.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-125">**cbRevocationSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-125">**cbRevocationSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-126">Offset, in byte, dall'inizio del GRL alla sezione di base.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-126">The offset, in bytes, from the start of the GRL to the Core section.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-127">**cRevokedKernelBinaries**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-127">**cRevokedKernelBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-128">Numero di file binari del kernel revocati elencati in GRL.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-128">The number of revoked kernel binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-129">**cRevokedUserBinaries**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-129">**cRevokedUserBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-130">Numero di file binari revocati in modalità utente elencati in GRL.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-130">The number of revoked user-mode binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-131">**cRevokedCertificates**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-131">**cRevokedCertificates**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-132">Numero di certificati revocati elencati in GRL.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-132">The number of revoked certificates listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-133">**cTrustedRoots**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-133">**cTrustedRoots**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-134">Il numero di radici attendibili elencate in GRL.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-134">The number of trusted roots listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-135">**cbExtensibleSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-135">**cbExtensibleSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-136">Offset, in byte, dall'inizio di GRL alla sezione estendibile.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-136">The offset, in bytes, from the start of the GRL to the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-137">**cExtensibleEntries**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-137">**cExtensibleEntries**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-138">Numero di voci nella sezione estendibile.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-138">The number of entries in the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-139">**cbRenewalSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-139">**cbRenewalSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-140">Offset, in byte, dall'inizio del GRL alla sezione rinnovi.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-140">The offset, in bytes, from the start of the GRL to the Renewals section.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-141">**cRevokedKernelBinaryRenewals**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-141">**cRevokedKernelBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-142">Il numero di rinnovi binari del kernel elencati in GRL.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-142">The number of kernel binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-143">**cRevokedUserBinaryRenewals**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-143">**cRevokedUserBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-144">Il numero di rinnovi binari in modalità utente elencati in GRL.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-144">The number of user-mode binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-145">**cRevokedCertificateRenewals**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-145">**cRevokedCertificateRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-146">Il numero di rinnovi certificati elencati in GRL.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-146">The number of certificate renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-147">**cbSignatureCoreOffset**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-147">**cbSignatureCoreOffset**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-148">Offset, in byte, dall'inizio di GRL alla firma della sezione di base.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-148">The offset, in bytes, from the start of the GRL to the Core section signature.</span></span>

</dd> <dt>

<span data-ttu-id="9e2e8-149">**cbSignatureExtOffset**</span><span class="sxs-lookup"><span data-stu-id="9e2e8-149">**cbSignatureExtOffset**</span></span>
</dt> <dd>

<span data-ttu-id="9e2e8-150">Offset, in byte, dall'inizio del GRL alla firma della sezione estendibile.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-150">The offset, in bytes, from the start of the GRL to the Extensible section signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e2e8-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e2e8-151">Remarks</span></span>

<span data-ttu-id="9e2e8-152">Tutti i numeri interi in GRL hanno un ordine di byte little-endian.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-152">All integers in the GRL have little-endian byte ordering.</span></span> <span data-ttu-id="9e2e8-153">Tutte le strutture sono allineate ai limiti di 1 byte.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-153">All structures are aligned to 1-byte boundaries.</span></span>

<span data-ttu-id="9e2e8-154">Questa struttura non è dichiarata in un'intestazione SDK.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-154">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="9e2e8-155">Per usare questa struttura, aggiungere la dichiarazione mostrata qui al codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="9e2e8-155">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e2e8-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e2e8-156">Requirements</span></span>



| <span data-ttu-id="9e2e8-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e2e8-157">Requirement</span></span> | <span data-ttu-id="9e2e8-158">Valore</span><span class="sxs-lookup"><span data-stu-id="9e2e8-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e2e8-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e2e8-159">Minimum supported client</span></span><br/> | <span data-ttu-id="9e2e8-160">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e2e8-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9e2e8-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e2e8-161">Minimum supported server</span></span><br/> | <span data-ttu-id="9e2e8-162">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9e2e8-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e2e8-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e2e8-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e2e8-164">Revoca del certificato OPM</span><span class="sxs-lookup"><span data-stu-id="9e2e8-164">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="9e2e8-165">Strutture OPM</span><span class="sxs-lookup"><span data-stu-id="9e2e8-165">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




