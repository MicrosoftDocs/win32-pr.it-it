---
title: Classe MicrosoftDNS_Zone
description: La \_ classe della zona MicrosoftDNS descrive una zona DNS. Ogni istanza della classe della \_ zona MicrosoftDNS deve essere assegnata esattamente a un server DNS. Le zone possono essere associate a più istanze di MicrosoftDNS \_ Domain o MicrosoftDNS \_ ResourceRecord.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- DNS della classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15119c7a5cdc1dba2998e17b5c69a4d0e15c6ca
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048862"
---
# <a name="microsoftdns_zone-class"></a><span data-ttu-id="33e50-107">\_Classe della zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="33e50-107">MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="33e50-108">Questo articolo contiene riferimenti al termine slave, che Microsoft non usa più.</span><span class="sxs-lookup"><span data-stu-id="33e50-108">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="33e50-109">Quando il termine verrà rimosso dal software, verrà rimosso anche dall'articolo.</span><span class="sxs-lookup"><span data-stu-id="33e50-109">When the term is removed from the software, we’ll remove it from this article.</span></span>

> [!NOTE]
> <span data-ttu-id="33e50-110">Questo articolo contiene riferimenti al termine server master, un termine che Microsoft non usa più.</span><span class="sxs-lookup"><span data-stu-id="33e50-110">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="33e50-111">Quando il termine verrà rimosso dal software, verrà rimosso anche dall'articolo.</span><span class="sxs-lookup"><span data-stu-id="33e50-111">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="33e50-112">La classe della **\_ zona MicrosoftDNS** descrive una zona DNS.</span><span class="sxs-lookup"><span data-stu-id="33e50-112">The **MicrosoftDNS\_Zone** class describes a DNS Zone.</span></span> <span data-ttu-id="33e50-113">Ogni istanza della classe **della \_ zona MicrosoftDNS** deve essere assegnata esattamente a un server DNS.</span><span class="sxs-lookup"><span data-stu-id="33e50-113">Every instance of the **MicrosoftDNS\_Zone** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="33e50-114">Le zone possono essere associate a più istanze di [**MicrosoftDNS \_ Domain**](microsoftdns-domain.md) o [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="33e50-114">Zones may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="33e50-115">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="33e50-115">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e50-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33e50-116">Syntax</span></span>

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a><span data-ttu-id="33e50-117">Members</span><span class="sxs-lookup"><span data-stu-id="33e50-117">Members</span></span>

<span data-ttu-id="33e50-118">La classe della **\_ zona MicrosoftDNS** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="33e50-118">The **MicrosoftDNS\_Zone** class has these types of members:</span></span>

-   [<span data-ttu-id="33e50-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="33e50-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="33e50-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33e50-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="33e50-121">Metodi</span><span class="sxs-lookup"><span data-stu-id="33e50-121">Methods</span></span>

<span data-ttu-id="33e50-122">La classe della **\_ zona MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="33e50-122">The **MicrosoftDNS\_Zone** class has these methods.</span></span>



| <span data-ttu-id="33e50-123">Metodo</span><span class="sxs-lookup"><span data-stu-id="33e50-123">Method</span></span>                   | <span data-ttu-id="33e50-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33e50-124">Description</span></span>                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33e50-125">**AgeAllRecords**</span><span class="sxs-lookup"><span data-stu-id="33e50-125">**AgeAllRecords**</span></span>        | <span data-ttu-id="33e50-126">Abilita la durata per alcuni o tutti i record non NS e non SOA.</span><span class="sxs-lookup"><span data-stu-id="33e50-126">Enables aging for some or all non-NS and non-SOA records.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="33e50-127">**ChangeZoneType**</span><span class="sxs-lookup"><span data-stu-id="33e50-127">**ChangeZoneType**</span></span>       | <span data-ttu-id="33e50-128">Modifica i tipi di zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-128">Changes zone types.</span></span> <br/> <span data-ttu-id="33e50-129">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="33e50-129">Qualifiers: Implemented</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="33e50-130">**CreateZone**</span><span class="sxs-lookup"><span data-stu-id="33e50-130">**CreateZone**</span></span>           | <span data-ttu-id="33e50-131">Crea una nuova zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-131">Creates a new zone.</span></span> <br/> <span data-ttu-id="33e50-132">Qualificatori: nessuno.</span><span class="sxs-lookup"><span data-stu-id="33e50-132">Qualifiers: None.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="33e50-133">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="33e50-133">**ForceRefresh**</span></span>         | <span data-ttu-id="33e50-134">Impone un aggiornamento del database secondario dal server DNS master.</span><span class="sxs-lookup"><span data-stu-id="33e50-134">Forces an update of the secondary from the Master DNS Server.</span></span> <br/> <span data-ttu-id="33e50-135">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="33e50-135">Qualifiers: Implemented</span></span><br/>                                                                                               |
| <span data-ttu-id="33e50-136">**Getdistinguishname**</span><span class="sxs-lookup"><span data-stu-id="33e50-136">**GetDistinguishedName**</span></span> | <span data-ttu-id="33e50-137">Ottiene il nome distinto DS per la zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-137">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="33e50-138">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="33e50-138">Qualifiers: Implemented</span></span><br/>                                                                                                                 |
| <span data-ttu-id="33e50-139">**PauseZone**</span><span class="sxs-lookup"><span data-stu-id="33e50-139">**PauseZone**</span></span>            | <span data-ttu-id="33e50-140">Sospende la zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-140">Pauses the Zone.</span></span> <br/> <span data-ttu-id="33e50-141">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="33e50-141">Qualifiers: Implemented</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="33e50-142">**ReloadZone**</span><span class="sxs-lookup"><span data-stu-id="33e50-142">**ReloadZone**</span></span>           | <span data-ttu-id="33e50-143">Ricarica la zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-143">Reloads the Zone.</span></span> <br/> <span data-ttu-id="33e50-144">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="33e50-144">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="33e50-145">**ResetSecondaries**</span><span class="sxs-lookup"><span data-stu-id="33e50-145">**ResetSecondaries**</span></span>     | <span data-ttu-id="33e50-146">Reimposta la matrice di indirizzi IP secondaria.</span><span class="sxs-lookup"><span data-stu-id="33e50-146">Resets the secondary ip address array.</span></span> <br/> <span data-ttu-id="33e50-147">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="33e50-147">Qualifiers: Implemented</span></span><br/>                                                                                                                      |
| <span data-ttu-id="33e50-148">**ResumeZone**</span><span class="sxs-lookup"><span data-stu-id="33e50-148">**ResumeZone**</span></span>           | <span data-ttu-id="33e50-149">Riprende la zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-149">Resumes the Zone.</span></span> <br/> <span data-ttu-id="33e50-150">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="33e50-150">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="33e50-151">**UpdateFromDS**</span><span class="sxs-lookup"><span data-stu-id="33e50-151">**UpdateFromDS**</span></span>         | <span data-ttu-id="33e50-152">Impone un aggiornamento della zona dal servizio directory (DS).</span><span class="sxs-lookup"><span data-stu-id="33e50-152">Forces an update of the Zone from the Directory Service (DS).</span></span> <span data-ttu-id="33e50-153">Affinché questo metodo sia valido, il valore di ZoneType deve essere 0 perché la zona deve essere effettivamente archiviata nel servizio DS.</span><span class="sxs-lookup"><span data-stu-id="33e50-153">For this method to be valid, the ZoneType must be 0 the Zone must indeed be stored in the DS.</span></span> <br/> <span data-ttu-id="33e50-154">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="33e50-154">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="33e50-155">**WriteBackZone**</span><span class="sxs-lookup"><span data-stu-id="33e50-155">**WriteBackZone**</span></span>        | <span data-ttu-id="33e50-156">Salva i dati della zona nel relativo file di zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-156">Saves Zone data to its zone file.</span></span> <br/> <span data-ttu-id="33e50-157">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="33e50-157">Qualifiers: Implemented, static</span></span><br/>                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="33e50-158">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33e50-158">Properties</span></span>

<span data-ttu-id="33e50-159">La classe della **\_ zona MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="33e50-159">The **MicrosoftDNS\_Zone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33e50-160">**Invecchiamento**</span><span class="sxs-lookup"><span data-stu-id="33e50-160">**Aging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-161">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33e50-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-163">Specifica il comportamento di invecchiamento e scavenging della zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-163">Specifies the aging and scavenging behavior of the zone.</span></span> <span data-ttu-id="33e50-164">Zero indica che lo scavenging è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="33e50-164">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="33e50-165">Quando lo scavenging è disabilitato, i timestamp dei record della zona non vengono aggiornati e i record non sono soggetti a scavenging.</span><span class="sxs-lookup"><span data-stu-id="33e50-165">When scavenging is disabled, the timestamps of records in the zone are not refreshed, and the records are not subjected to scavenging.</span></span> <span data-ttu-id="33e50-166">Se impostata su uno, i record vengono sottoposti a scavenging e i relativi timestamp vengono aggiornati quando il server riceve la richiesta di aggiornamento dinamico per i record.</span><span class="sxs-lookup"><span data-stu-id="33e50-166">When set to one, records are subjected to scavenging and their timestamps are refreshed when the server receives the dynamic update request for the records.</span></span> <span data-ttu-id="33e50-167">Per le zone integrate Active Directory, questo valore viene impostato sulla proprietà *DefaultAgingState* del server DNS in cui viene creata la zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-167">For Active Directory-integrated zones, this value is set to the *DefaultAgingState* property of the DNS Server where the zone is created.</span></span> <span data-ttu-id="33e50-168">Per le zone primarie standard, il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="33e50-168">For standard primary zones, the default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-169">**AllowUpdate**</span><span class="sxs-lookup"><span data-stu-id="33e50-169">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33e50-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-172">Indica se la zona accetta richieste di aggiornamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="33e50-172">Indicates whether the Zone accepts dynamic update requests.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-173">**Creato automaticamente**</span><span class="sxs-lookup"><span data-stu-id="33e50-173">**AutoCreated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-174">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33e50-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-176">Indica se la zona è stata creata in autocreazione.</span><span class="sxs-lookup"><span data-stu-id="33e50-176">Indicates whether the Zone is autocreated.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-177">**AvailForScavengeTime**</span><span class="sxs-lookup"><span data-stu-id="33e50-177">**AvailForScavengeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-178">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33e50-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-180">Specifica l'ora in cui il server può tentare di eseguire lo scavenging della zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-180">Specifies the time when the server may attempt scavenging the zone.</span></span> <span data-ttu-id="33e50-181">Anche se la zona è configurata per consentire lo scavenging, il server DNS non tenterà di eseguire lo scavenging di questa zona fino a dopo questo momento.</span><span class="sxs-lookup"><span data-stu-id="33e50-181">Even if the zone is configured to enable scavenging the DNS server will not attempt scavenging this zone until after this moment.</span></span> <span data-ttu-id="33e50-182">Questo valore viene impostato sull'ora corrente più l'intervallo di aggiornamento della zona ogni volta che viene caricata la zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-182">This value is set to the current time plus the Refresh Interval of the zone whenever the zone is loaded.</span></span> <span data-ttu-id="33e50-183">Questo parametro viene archiviato localmente e non viene replicato in altre copie della zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-183">This parameter is stored locally, and is not replicated to other copies of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-184">**DataFile**</span><span class="sxs-lookup"><span data-stu-id="33e50-184">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33e50-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-187">Indica il nome del file di zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-187">Indicates the name of the zone file.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-188">**DisableWINSRecordReplication**</span><span class="sxs-lookup"><span data-stu-id="33e50-188">**DisableWINSRecordReplication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-189">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33e50-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-191">Indica se il record WINS è replicato.</span><span class="sxs-lookup"><span data-stu-id="33e50-191">Indicates whether the WINS record is replicated.</span></span> <span data-ttu-id="33e50-192">Se impostato su TRUE, la replica del record WINS è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="33e50-192">If set to TRUE, WINS record replication is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-193">**DsIntegrated**</span><span class="sxs-lookup"><span data-stu-id="33e50-193">**DsIntegrated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-194">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33e50-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-196">Specifica se la zona è integrata in DS.</span><span class="sxs-lookup"><span data-stu-id="33e50-196">Specifies whether the zone is DS integrated.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-197">**ForwarderSlave**</span><span class="sxs-lookup"><span data-stu-id="33e50-197">**ForwarderSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-198">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33e50-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-200">Indica se il DNS utilizza la ricorsione durante la risoluzione dei nomi per la zona di avanzamento specificata.</span><span class="sxs-lookup"><span data-stu-id="33e50-200">Indicates whether the DNS uses recursion when resolving the names for the specified forward zone.</span></span> <span data-ttu-id="33e50-201">Applicabile solo alle zone di inoltri condizionali.</span><span class="sxs-lookup"><span data-stu-id="33e50-201">Applicable to Conditional Forwarding zones only.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-202">**ForwarderTimeout**</span><span class="sxs-lookup"><span data-stu-id="33e50-202">**ForwarderTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-203">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33e50-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-205">Indica il tempo, in secondi, in cui un server DNS che esegue l'invio di una query per il nome sotto la zona di avanzamento attende la risoluzione dal server d'avvio prima di tentare di risolvere la query stessa.</span><span class="sxs-lookup"><span data-stu-id="33e50-205">Indicates the time, in seconds, a DNS server forwarding a query for the name under the forward zone waits for resolution from the forwarder before attempting to resolve the query itself.</span></span> <span data-ttu-id="33e50-206">Questo parametro è applicabile solo alle zone di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="33e50-206">This parameter is applicable to the Forward zones only.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-207">**LastSuccessfulSoaCheck**</span><span class="sxs-lookup"><span data-stu-id="33e50-207">**LastSuccessfulSoaCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-208">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33e50-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-210">Numero di secondi a partire dall'inizio del 1 gennaio 1970 GMT, perché il numero di serie SOA per la zona è stato selezionato per l'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="33e50-210">Number of seconds since the beginning of January 1, 1970 GMT, since the SOA serial number for the zone was last checked.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-211">**LastSuccessfulXfr**</span><span class="sxs-lookup"><span data-stu-id="33e50-211">**LastSuccessfulXfr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-212">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33e50-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-214">Numero di secondi a partire dall'inizio del 1 gennaio 1970 GMT, dall'ultimo trasferimento della zona da un server master.</span><span class="sxs-lookup"><span data-stu-id="33e50-214">Number of seconds since the beginning of January 1, 1970 GMT, since the zone was last transferred from a master server.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-215">**LocalMasterServers**</span><span class="sxs-lookup"><span data-stu-id="33e50-215">**LocalMasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-216">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="33e50-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33e50-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-218">Indirizzi IP locali dei server DNS master per questa zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-218">Local IP addresses of the master DNS servers for this zone.</span></span> <span data-ttu-id="33e50-219">Se impostate, questi master superano il MasterServers trovato in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="33e50-219">If set, these masters over-ride the MasterServers found in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-220">**MasterServers**</span><span class="sxs-lookup"><span data-stu-id="33e50-220">**MasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-221">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="33e50-221">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33e50-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-223">Indirizzi IP dei server DNS master per questa zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-223">IP addresses of the master DNS servers for this zone.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-224">**NoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="33e50-224">**NoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-225">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33e50-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-227">Specifica l'intervallo di tempo tra l'ultimo aggiornamento del timestamp di un record e il primo momento in cui è possibile aggiornare il timestamp.</span><span class="sxs-lookup"><span data-stu-id="33e50-227">Specifies the time interval between the last update of a record's timestamp and the earliest moment when the timestamp can be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-228">**Notificare**</span><span class="sxs-lookup"><span data-stu-id="33e50-228">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-229">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33e50-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-231">Indica se la zona master notifica i database secondari di eventuali modifiche nel database RRs.</span><span class="sxs-lookup"><span data-stu-id="33e50-231">Indicates whether the master Zone notifies secondaries of any changes in its RRs database.</span></span> <span data-ttu-id="33e50-232">Impostare su 1 per notificare i database secondari.</span><span class="sxs-lookup"><span data-stu-id="33e50-232">Set to 1 to notify secondaries.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-233">**NotifyServers**</span><span class="sxs-lookup"><span data-stu-id="33e50-233">**NotifyServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-234">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="33e50-234">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33e50-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-236">Matrice di stringhe che enumerano gli indirizzi IP dei server DNS per ricevere una notifica delle modifiche in quest'area.</span><span class="sxs-lookup"><span data-stu-id="33e50-236">Array of strings enumerating IP addresses of DNS servers to be notified of changes in this zone.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-237">**Sospeso**</span><span class="sxs-lookup"><span data-stu-id="33e50-237">**Paused**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-238">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33e50-238">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-240">Indica se la zona è sospesa.</span><span class="sxs-lookup"><span data-stu-id="33e50-240">Indicates whether the Zone is paused.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-241">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="33e50-241">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-242">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33e50-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-244">Specifica l'intervallo di aggiornamento, durante il quale si prevede che i record con un timestamp diverso da zero vengano aggiornati in modo che rimangano nella zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-244">Specifies the refresh interval, during which the records with nonzero timestamp are expected to be refreshed to remain in the zone.</span></span> <span data-ttu-id="33e50-245">I record che non sono stati aggiornati entro la scadenza dell'intervallo di aggiornamento potrebbero essere rimossi dal successivo scavenging eseguito da un server.</span><span class="sxs-lookup"><span data-stu-id="33e50-245">Records that have not been refreshed by expiration of the Refresh interval could be removed by the next scavenging performed by a server.</span></span> <span data-ttu-id="33e50-246">Questo valore non deve mai essere inferiore al periodo di aggiornamento più lungo dei record registrati nella zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-246">This value should never be less than the longest refresh period of the records registered in the zone.</span></span> <span data-ttu-id="33e50-247">I valori troppo piccoli possono causare la rimozione di record DNS validi.</span><span class="sxs-lookup"><span data-stu-id="33e50-247">Values that are too small may lead to removal of valid DNS records.</span></span> <span data-ttu-id="33e50-248">i valori troppo grandi prolungano la durata dei record non aggiornati.</span><span class="sxs-lookup"><span data-stu-id="33e50-248">values that are too large prolong the lifetime of stale records.</span></span> <span data-ttu-id="33e50-249">Questo valore viene impostato sulla proprietà *DefaultRefreshInterval-* del server DNS in cui viene creata la zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-249">This value is set to the *DefaultRefreshInterval* property of the DNS server where the zone is created.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-250">**Inverso**</span><span class="sxs-lookup"><span data-stu-id="33e50-250">**Reverse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-251">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33e50-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-253">Indica se la zona è inversa (TRUE) o in poi (FALSE).</span><span class="sxs-lookup"><span data-stu-id="33e50-253">Indicates whether the Zone is reverse (TRUE) or forward (FALSE).</span></span>

</dd> <dt>

<span data-ttu-id="33e50-254">**ScavengeServers**</span><span class="sxs-lookup"><span data-stu-id="33e50-254">**ScavengeServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-255">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="33e50-255">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33e50-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-257">Matrice di stringhe che enumera l'elenco di indirizzi IP dei server DNS a cui è consentito eseguire lo scavenging dei record non aggiornati di questa zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-257">Array of strings that enumerates the list of IP addresses of DNS servers that are allowed to perform scavenging of stale records of this zone.</span></span> <span data-ttu-id="33e50-258">Se l'elenco non è specificato, il server DNS primario autorevole per la zona può eseguire lo scavenging della zona quando vengono soddisfatti altri prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="33e50-258">If the list is not specified, any primary DNS server authoritative for the zone is allowed to scavenge the zone when other prerequisites are met.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-259">**SecondaryServers**</span><span class="sxs-lookup"><span data-stu-id="33e50-259">**SecondaryServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-260">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="33e50-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33e50-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-262">Matrice di stringhe che enumerano gli indirizzi IP dei server DNS che possono ricevere questa zona tramite la replica della zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-262">Array of strings enumerating IP addresses of DNS servers allowed to receive this zone through zone replication.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-263">**SecureSecondaries**</span><span class="sxs-lookup"><span data-stu-id="33e50-263">**SecureSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-264">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33e50-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-266">Indica se il trasferimento di zona può essere solo designato come secondari.</span><span class="sxs-lookup"><span data-stu-id="33e50-266">Indicates whether zone transfer is allowed to designated secondaries only.</span></span> <span data-ttu-id="33e50-267">I database secondari designati sono server DNS i cui indirizzi IP sono elencati in SecondariesIPAddressesArray.</span><span class="sxs-lookup"><span data-stu-id="33e50-267">Designated secondaries are DNS Servers whose IP addresses are listed in SecondariesIPAddressesArray.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-268">**Arresto**</span><span class="sxs-lookup"><span data-stu-id="33e50-268">**Shutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-269">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33e50-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-271">Indica se la copia della zona è scaduta.</span><span class="sxs-lookup"><span data-stu-id="33e50-271">Indicates whether the copy of the Zone is expired.</span></span> <span data-ttu-id="33e50-272">Se TRUE, la zona è scaduta o è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="33e50-272">If TRUE, the Zone is expired, or shut down.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-273">**UseNBStat**</span><span class="sxs-lookup"><span data-stu-id="33e50-273">**UseNBStat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-274">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33e50-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-276">Questo valore booleano indica se la zona usa la ricerca inversa NBStat.</span><span class="sxs-lookup"><span data-stu-id="33e50-276">This Boolean indicates whether the Zone uses NBStat reverse lookup.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-277">**UseWins**</span><span class="sxs-lookup"><span data-stu-id="33e50-277">**UseWins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-278">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33e50-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-280">Indica se la zona usa la ricerca di WINS.</span><span class="sxs-lookup"><span data-stu-id="33e50-280">Indicates whether the Zone uses WINS look up.</span></span>

</dd> <dt>

<span data-ttu-id="33e50-281">**ZoneType**</span><span class="sxs-lookup"><span data-stu-id="33e50-281">**ZoneType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33e50-282">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33e50-282">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33e50-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33e50-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33e50-284">Indica il tipo della zona.</span><span class="sxs-lookup"><span data-stu-id="33e50-284">Indicates the type of the Zone.</span></span> <span data-ttu-id="33e50-285">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="33e50-285">Valid values are:</span></span>

-   <span data-ttu-id="33e50-286">DS integrato</span><span class="sxs-lookup"><span data-stu-id="33e50-286">DS integrated</span></span>
-   <span data-ttu-id="33e50-287">Primaria</span><span class="sxs-lookup"><span data-stu-id="33e50-287">Primary</span></span>
-   <span data-ttu-id="33e50-288">Secondari</span><span class="sxs-lookup"><span data-stu-id="33e50-288">Secondary</span></span>

<span data-ttu-id="33e50-289">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="33e50-289">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="33e50-290">Valori aggiuntivi:</span><span class="sxs-lookup"><span data-stu-id="33e50-290">Additional values:</span></span>

-   <span data-ttu-id="33e50-291">Cache</span><span class="sxs-lookup"><span data-stu-id="33e50-291">Cache</span></span>
-   <span data-ttu-id="33e50-292">Stub</span><span class="sxs-lookup"><span data-stu-id="33e50-292">Stub</span></span>
-   <span data-ttu-id="33e50-293">Server d'inoltro</span><span class="sxs-lookup"><span data-stu-id="33e50-293">Forwarder</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33e50-294">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33e50-294">Requirements</span></span>



| <span data-ttu-id="33e50-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="33e50-295">Requirement</span></span> | <span data-ttu-id="33e50-296">Valore</span><span class="sxs-lookup"><span data-stu-id="33e50-296">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33e50-297">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33e50-297">Minimum supported client</span></span><br/> | <span data-ttu-id="33e50-298">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="33e50-298">None supported</span></span><br/>                                                              |
| <span data-ttu-id="33e50-299">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33e50-299">Minimum supported server</span></span><br/> | <span data-ttu-id="33e50-300">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33e50-300">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="33e50-301">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="33e50-301">Namespace</span></span><br/>                | <span data-ttu-id="33e50-302">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="33e50-302">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="33e50-303">MOF</span><span class="sxs-lookup"><span data-stu-id="33e50-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33e50-304"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33e50-304"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33e50-305">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33e50-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e50-306">**\_Dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-306">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="33e50-307">**Metodo AgeAllRecords della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-307">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="33e50-308">**Metodo ChangeZoneType della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-308">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="33e50-309">**Metodo CreateZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-309">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="33e50-310">**Metodo ForceRefresh della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-310">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="33e50-311">**Metodo getdistinguishname della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-311">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="33e50-312">**Metodo PauseZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-312">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="33e50-313">**Metodo ReloadZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-313">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="33e50-314">**Metodo ResetSecondaries della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-314">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="33e50-315">**Metodo ResumeZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-315">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="33e50-316">**Metodo UpdateFromDS della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-316">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="33e50-317">**Metodo WriteBackZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e50-317">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





