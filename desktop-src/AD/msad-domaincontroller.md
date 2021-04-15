---
title: Classe MSAD_DomainController
description: Rappresenta il controller di dominio in cui è in esecuzione il provider WMI.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- Classe MSAD_DomainController Active Directory
- Classe MSAD_DomainController Active Directory, descritta
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476847"
---
# <a name="msad_domaincontroller-class"></a><span data-ttu-id="e2b07-105">\_Classe DomainController MSAD</span><span class="sxs-lookup"><span data-stu-id="e2b07-105">MSAD\_DomainController class</span></span>

<span data-ttu-id="e2b07-106">Rappresenta il controller di dominio in cui è in esecuzione il provider WMI.</span><span class="sxs-lookup"><span data-stu-id="e2b07-106">Represents the domain controller (DC) on which the WMI provider is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b07-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2b07-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="e2b07-108">Members</span><span class="sxs-lookup"><span data-stu-id="e2b07-108">Members</span></span>

<span data-ttu-id="e2b07-109">La **classe \_ DomainController MSAD** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e2b07-109">The **MSAD\_DomainController** class has these types of members:</span></span>

-   [<span data-ttu-id="e2b07-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="e2b07-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e2b07-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2b07-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e2b07-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="e2b07-112">Methods</span></span>

<span data-ttu-id="e2b07-113">La **classe \_ DomainController MSAD** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e2b07-113">The **MSAD\_DomainController** class has these methods.</span></span>



| <span data-ttu-id="e2b07-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="e2b07-114">Method</span></span>                                                 | <span data-ttu-id="e2b07-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2b07-115">Description</span></span>                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2b07-116">**ExecuteKCC**</span><span class="sxs-lookup"><span data-stu-id="e2b07-116">**ExecuteKCC**</span></span>](executekcc-msad-domaincontroller.md) | <span data-ttu-id="e2b07-117">Richiama il controllo di coerenza informazioni per verificare la topologia di replica.</span><span class="sxs-lookup"><span data-stu-id="e2b07-117">Invokes the Knowledge Consistency Checker to verify the replication topology.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e2b07-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2b07-118">Properties</span></span>

<span data-ttu-id="e2b07-119">La **classe \_ DomainController MSAD** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e2b07-119">The **MSAD\_DomainController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2b07-120">**CommonName**</span><span class="sxs-lookup"><span data-stu-id="e2b07-120">**CommonName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2b07-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-123">Ottiene il nome comune dell'oggetto server.</span><span class="sxs-lookup"><span data-stu-id="e2b07-123">Gets the common name of the server object.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-124">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="e2b07-124">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2b07-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e2b07-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-128">Ottiene il percorso X. 500 dell'oggetto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) .</span><span class="sxs-lookup"><span data-stu-id="e2b07-128">Gets the X.500 path of the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-129">**IsAdvertisingToLocator**</span><span class="sxs-lookup"><span data-stu-id="e2b07-129">**IsAdvertisingToLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-130">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e2b07-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-132">Ottiene il valore che indica se il servizio localizzatore sul controller di dominio è pubblicizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="e2b07-132">Gets the value that indicates whether the locator service on the DC is advertising correctly.</span></span> <span data-ttu-id="e2b07-133">**True** se il servizio Locator sul controller di dominio viene pubblicizzato correttamente. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e2b07-133">**TRUE** if the locator service on the DC is advertising correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-134">**IsGC**</span><span class="sxs-lookup"><span data-stu-id="e2b07-134">**IsGC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-135">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e2b07-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-137">Ottiene il valore che indica se il controller di dominio è un server di catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="e2b07-137">Gets the value that indicates whether the DC is a Global Catalog server.</span></span> <span data-ttu-id="e2b07-138">**True** se il controller di dominio è un server di catalogo globale; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e2b07-138">**TRUE** if the DC is a Global Catalog server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-139">**IsNextRIDPoolAvailable**</span><span class="sxs-lookup"><span data-stu-id="e2b07-139">**IsNextRIDPoolAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-140">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e2b07-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-142">Ottiene il valore che indica se il controller di dominio ha ottenuto un altro pool di RID.</span><span class="sxs-lookup"><span data-stu-id="e2b07-142">Gets the value that indicates whether the DC has obtained another RID pool.</span></span> <span data-ttu-id="e2b07-143">**True** se il controller di dominio ha ottenuto un altro pool di RID e l'allocazione di RID in questo controller di dominio può continuare anche se il pool corrente di RID è esaurito. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e2b07-143">**TRUE** if the DC has obtained another RID pool and allocation of RIDs on this DC can continue even if the current pool of RIDs is exhausted; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-144">**IsRegisteredInDNS**</span><span class="sxs-lookup"><span data-stu-id="e2b07-144">**IsRegisteredInDNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-145">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e2b07-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-147">Ottiene il valore che indica se il controller di dominio è registrato correttamente in DNS.</span><span class="sxs-lookup"><span data-stu-id="e2b07-147">Gets the value that indicates whether the DC is registered correctly in DNS.</span></span> <span data-ttu-id="e2b07-148">**True** se il controller di dominio è registrato correttamente in DNS; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e2b07-148">**TRUE** if the DC is registered correctly in DNS; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-149">**IsSysVolReady**</span><span class="sxs-lookup"><span data-stu-id="e2b07-149">**IsSysVolReady**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-150">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e2b07-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-152">Ottiene il valore che indica se SysVol è stato pubblicato correttamente.</span><span class="sxs-lookup"><span data-stu-id="e2b07-152">Gets the value that indicates whether the SysVol has published correctly.</span></span> <span data-ttu-id="e2b07-153">**True** se SYSVOL è stato pubblicato correttamente. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e2b07-153">**TRUE** if the SysVol has published correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-154">**NTDsaGUID**</span><span class="sxs-lookup"><span data-stu-id="e2b07-154">**NTDsaGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2b07-155">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-157">Ottiene il GUID associato all'oggetto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) nel contenitore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e2b07-157">Gets the GUID that is associated with the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object in the configuration container.</span></span> <span data-ttu-id="e2b07-158">L'oggetto **NTDS-DSA** rappresenta il processo DSA del servizio dominio di Active Directory nel server.</span><span class="sxs-lookup"><span data-stu-id="e2b07-158">The **NTDS-DSA** object represents the Active Directory Domain Service DSA process on the server.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-159">**PercentOfRIDsLeft**</span><span class="sxs-lookup"><span data-stu-id="e2b07-159">**PercentOfRIDsLeft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-160">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2b07-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-162">Ottiene la percentuale di RID a sinistra nel pool di RID corrente in questo controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="e2b07-162">Gets the percentage of RIDs that are left in the current RID pool on this DC.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-163">**SiteName**</span><span class="sxs-lookup"><span data-stu-id="e2b07-163">**SiteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2b07-164">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-166">Ottiene il sito in cui è presente il controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="e2b07-166">Gets the site in which the DC exists.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-167">**TimeOfOldestReplAdd**</span><span class="sxs-lookup"><span data-stu-id="e2b07-167">**TimeOfOldestReplAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-168">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2b07-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-170">Ottiene il timestamp dell'operazione di aggiunta della replica meno recente che si trova ancora nella coda del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="e2b07-170">Gets the timestamp of the oldest replication add operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-171">**TimeOfOldestReplDel**</span><span class="sxs-lookup"><span data-stu-id="e2b07-171">**TimeOfOldestReplDel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-172">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2b07-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-174">Ottiene il timestamp dell'operazione di eliminazione della replica meno recente che si trova ancora nella coda del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="e2b07-174">Gets the timestamp of the oldest replication delete operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-175">**TimeOfOldestReplMod**</span><span class="sxs-lookup"><span data-stu-id="e2b07-175">**TimeOfOldestReplMod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-176">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2b07-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-178">Ottiene il timestamp dell'operazione di modifica della replica meno recente che si trova ancora nella coda del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="e2b07-178">Gets the timestamp of the oldest replication modify operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-179">**TimeOfOldestReplSync**</span><span class="sxs-lookup"><span data-stu-id="e2b07-179">**TimeOfOldestReplSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-180">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2b07-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-182">Ottiene il timestamp dell'operazione di sincronizzazione della replica meno recente che si trova ancora nella coda del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="e2b07-182">Gets the timestamp of the oldest replication sync operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="e2b07-183">**TimeOfOldestReplUpdRefs**</span><span class="sxs-lookup"><span data-stu-id="e2b07-183">**TimeOfOldestReplUpdRefs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b07-184">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2b07-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2b07-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2b07-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b07-186">Ottiene il timestamp dell'operazione di aggiornamento della replica meno recente che si trova ancora nella coda del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="e2b07-186">Gets the timestamp of the oldest replication update operation that is still in the queue on this domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2b07-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2b07-187">Requirements</span></span>



| <span data-ttu-id="e2b07-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2b07-188">Requirement</span></span> | <span data-ttu-id="e2b07-189">Valore</span><span class="sxs-lookup"><span data-stu-id="e2b07-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b07-190">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2b07-190">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b07-191">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e2b07-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e2b07-192">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2b07-192">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b07-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2b07-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2b07-194">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e2b07-194">Namespace</span></span><br/>                | <span data-ttu-id="e2b07-195">\\MicrosoftActiveDirectory radice</span><span class="sxs-lookup"><span data-stu-id="e2b07-195">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="e2b07-196">MOF</span><span class="sxs-lookup"><span data-stu-id="e2b07-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2b07-197"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2b07-197"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2b07-198">DLL</span><span class="sxs-lookup"><span data-stu-id="e2b07-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2b07-199"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2b07-199"><dt>Replprov.dll</dt></span></span> </dl> |



 

