---
title: Classe MicrosoftDNS_Server
description: La \_ classe server MicrosoftDNS descrive un server DNS. Ogni istanza di questa classe può essere associata a un'istanza della \_ cache MicrosoftDNS, a un'istanza di MicrosoftDNS \_ RootHints e a più istanze di MicrosoftDNS \_ zone.
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- DNS della classe MicrosoftDNS_Server
- MicrosoftDNS_Server della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854a90f5b0fa4d331bd0478d104e50dd70b0cd65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963829"
---
# <a name="microsoftdns_server-class"></a><span data-ttu-id="dcfe5-106">\_Classe server MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="dcfe5-106">MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="dcfe5-107">La **classe \_ Server MicrosoftDNS** descrive un server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-107">The **MicrosoftDNS\_Server** class describes a DNS Server.</span></span> <span data-ttu-id="dcfe5-108">Ogni istanza di questa classe può essere associata a un'istanza della [**\_ cache MicrosoftDNS**](microsoftdns-cache.md), a un'istanza di [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)e a più istanze di [**MicrosoftDNS \_ zone**](microsoftdns-zone.md).</span><span class="sxs-lookup"><span data-stu-id="dcfe5-108">Every instance of this class may be associated with one instance of [**MicrosoftDNS\_Cache**](microsoftdns-cache.md), one instance of [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md), and multiple instances of [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

<span data-ttu-id="dcfe5-109">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcfe5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcfe5-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a><span data-ttu-id="dcfe5-111">Members</span><span class="sxs-lookup"><span data-stu-id="dcfe5-111">Members</span></span>

<span data-ttu-id="dcfe5-112">La **classe \_ Server MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dcfe5-112">The **MicrosoftDNS\_Server** class has these types of members:</span></span>

-   [<span data-ttu-id="dcfe5-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="dcfe5-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="dcfe5-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dcfe5-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dcfe5-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="dcfe5-115">Methods</span></span>

<span data-ttu-id="dcfe5-116">La **classe \_ Server MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-116">The **MicrosoftDNS\_Server** class has these methods.</span></span>



| <span data-ttu-id="dcfe5-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="dcfe5-117">Method</span></span>                   | <span data-ttu-id="dcfe5-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcfe5-118">Description</span></span>                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| <span data-ttu-id="dcfe5-119">**Getdistinguishname**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-119">**GetDistinguishedName**</span></span> | <span data-ttu-id="dcfe5-120">Recupera il nome distinto DNS per la zona.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-120">Retrieves DNS distinguished name for the zone.</span></span><br/>                        |
| <span data-ttu-id="dcfe5-121">**StartScavenging**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-121">**StartScavenging**</span></span>      | <span data-ttu-id="dcfe5-122">Avvia lo scavenging dei record non aggiornati nelle zone soggette allo scavenging.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-122">Starts scavenging stale records in the zones subjected to scavenging.</span></span><br/> |
| <span data-ttu-id="dcfe5-123">**StartService**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-123">**StartService**</span></span>         | <span data-ttu-id="dcfe5-124">Avvia il server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-124">Starts the DNS Server.</span></span><br/>                                                |
| <span data-ttu-id="dcfe5-125">**StopService**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-125">**StopService**</span></span>          | <span data-ttu-id="dcfe5-126">Arresta il server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-126">Stops the DNS Server.</span></span><br/>                                                 |



 

### <a name="properties"></a><span data-ttu-id="dcfe5-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dcfe5-127">Properties</span></span>

<span data-ttu-id="dcfe5-128">La **classe \_ Server MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-128">The **MicrosoftDNS\_Server** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dcfe5-129">**AddressAnswerLimit**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-129">**AddressAnswerLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-132">Numero massimo di record host restituiti in risposta a una richiesta di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-132">Maximum number of host records returned in response to an address request.</span></span> <span data-ttu-id="dcfe5-133">I valori compresi tra 5 e 28 sono validi.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-133">Values between 5 and 28 are valid.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-134">**AllowUpdate**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-134">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-137">Specifica se il server DNS accetta richieste di aggiornamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-137">Specifies whether the DNS Server accepts dynamic update requests.</span></span> <span data-ttu-id="dcfe5-138">I valori validi sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-138">Valid values are as shown in the following table.</span></span>



| <span data-ttu-id="dcfe5-139">Valore</span><span class="sxs-lookup"><span data-stu-id="dcfe5-139">Value</span></span>                                                                                                | <span data-ttu-id="dcfe5-140">Significato</span><span class="sxs-lookup"><span data-stu-id="dcfe5-140">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="dcfe5-141"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-141"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-142">Nessuna restrizione.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-142">No Restrictions.</span></span><br/>                                                                           |
| <span id="1"></span><dl> <span data-ttu-id="dcfe5-143"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-143"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-144">Non consente aggiornamenti dinamici dei record SOA.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-144">Does not allow dynamic updates of SOA records.</span></span><br/>                                             |
| <span id="2"></span><dl> <span data-ttu-id="dcfe5-145"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-145"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-146">Non consente aggiornamenti dinamici di record NS nella radice della zona.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-146">Does not allow dynamic updates of NS records at the zone root.</span></span><br/>                             |
| <span id="4"></span><dl> <span data-ttu-id="dcfe5-147"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-147"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-148">Non consente aggiornamenti dinamici di record NS non nella radice della zona (record NS di delega).</span><span class="sxs-lookup"><span data-stu-id="dcfe5-148">Does not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span><br/> |



 

<span data-ttu-id="dcfe5-149">Sommare questi valori per determinare il valore dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-149">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-150">**AutoCacheUpdate**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-150">**AutoCacheUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-151">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-153">Indica se il server DNS tenta di aggiornare le voci della cache utilizzando i dati dei server radice.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-153">Indicates whether the DNS Server attempts to update its cache entries using data from root servers.</span></span> <span data-ttu-id="dcfe5-154">All'avvio di un server DNS, è necessario un elenco di NS "hint" del server radice e di record A per i server che storicamente chiamano il file di cache.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-154">When a DNS Server boots, it needs a list of root server 'hints' NS and A records for the servers historically called the cache file.</span></span> <span data-ttu-id="dcfe5-155">I server DNS Microsoft dispongono di una funzionalità che consente di provare a eseguire il writeback di un nuovo file di cache in base alle risposte dei server radice.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-155">Microsoft DNS Servers have a feature that enables them to attempt to write back a new cache file based on the responses from root servers.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-156">**AutoConfigFileZones**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-156">**AutoConfigFileZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-159">Indica quali zone primarie standard autorevoli per il nome del server DNS devono essere aggiornate quando il server dei nomi viene modificato.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-159">Indicates which standard primary zones that are authoritative for the name of the DNS Server must be updated when the name server changes.</span></span> <span data-ttu-id="dcfe5-160">I valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="dcfe5-160">Valid values are as follows:</span></span>



| <span data-ttu-id="dcfe5-161">Valore</span><span class="sxs-lookup"><span data-stu-id="dcfe5-161">Value</span></span>                                                                                                | <span data-ttu-id="dcfe5-162">Significato</span><span class="sxs-lookup"><span data-stu-id="dcfe5-162">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="dcfe5-163"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-163"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-164">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-164">None.</span></span><br/>                                           |
| <span id="1"></span><dl> <span data-ttu-id="dcfe5-165"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-165"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-166">Solo i server che consentono aggiornamenti dinamici.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-166">Only servers that allow dynamic updates.</span></span><br/>        |
| <span id="2"></span><dl> <span data-ttu-id="dcfe5-167"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-167"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-168">Solo i server che non consentono aggiornamenti dinamici.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-168">Only servers that do not allow dynamic updates.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="dcfe5-169"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-169"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-170">Tutti i server.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-170">All servers.</span></span><br/>                                    |



 

<span data-ttu-id="dcfe5-171">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-171">The default value is 1.</span></span>

<span data-ttu-id="dcfe5-172">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="dcfe5-172">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="dcfe5-173">Il numero 3 rappresenta tutti i server.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-173">The number 3 represents All servers.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-174">**BindSecondaries**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-174">**BindSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-175">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-176">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-176">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-177">Determina il formato del messaggio AXFR durante l'invio a database secondari del server DNS non Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-177">Determines the AXFR message format when sending to non-Microsoft DNS Server secondaries.</span></span> <span data-ttu-id="dcfe5-178">Se impostato su TRUE, il server DNS invia i trasferimenti a database secondari del server DNS non Microsoft nel formato non compresso.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-178">When set to TRUE, the DNS Server sends transfers to non-Microsoft DNS Server secondaries in the uncompressed format.</span></span> <span data-ttu-id="dcfe5-179">Se FALSE, tutti i trasferimenti vengono inviati nel formato Fast.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-179">When FALSE, all transfers are sent in the fast format.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-180">**Metodo avvio**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-180">**BootMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-181">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-182">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-183">Metodo di inizializzazione per il server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-183">Initialization method for the DNS Server.</span></span> <span data-ttu-id="dcfe5-184">Nella tabella che segue sono riportati i valori validi.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-184">Valid values are shown in the following table.</span></span>



| <span data-ttu-id="dcfe5-185">Valore</span><span class="sxs-lookup"><span data-stu-id="dcfe5-185">Value</span></span>                                                                                                | <span data-ttu-id="dcfe5-186">Significato</span><span class="sxs-lookup"><span data-stu-id="dcfe5-186">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="dcfe5-187"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-187"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-188">Non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-188">Uninitialized.</span></span><br/>                    |
| <span id="1"></span><dl> <span data-ttu-id="dcfe5-189"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-189"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-190">Avvio dal file.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-190">Boot from file.</span></span><br/>                   |
| <span id="2"></span><dl> <span data-ttu-id="dcfe5-191"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-191"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-192">Avvio dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-192">Boot from registry.</span></span><br/>               |
| <span id="3"></span><dl> <span data-ttu-id="dcfe5-193"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-193"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-194">Avvio da directory e registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-194">Boot from directory and registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dcfe5-195">**DefaultAgingState**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-195">**DefaultAgingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-196">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-197">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-198">Valore predefinito di **ScavengingInterval** impostato per tutte le zone integrate Active Directory create in questo server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-198">Default **ScavengingInterval** value set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="dcfe5-199">Il valore predefinito è zero, che indica che lo scavenging è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-199">The default value is zero, indicating scavenging is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-200">**DefaultNoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-200">**DefaultNoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-201">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-202">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-202">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-203">Nessun intervallo di aggiornamento, in ore, impostato per tutte le zone integrate Active Directory create in questo server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-203">No-refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="dcfe5-204">Il valore predefinito è 168 ore (sette giorni).</span><span class="sxs-lookup"><span data-stu-id="dcfe5-204">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-205">**DefaultRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-205">**DefaultRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-206">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-207">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-207">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-208">Intervallo di aggiornamento, in ore, impostato per tutte le zone integrate Active Directory create in questo server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-208">Refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="dcfe5-209">Il valore predefinito è 168 ore (sette giorni).</span><span class="sxs-lookup"><span data-stu-id="dcfe5-209">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-210">**DisableAutoReverseZones**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-210">**DisableAutoReverseZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-211">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-212">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-213">Indica se il server DNS crea automaticamente le zone di ricerca inversa standard.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-213">Indicates whether the DNS Server automatically creates standard reverse look up zones.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-214">**DisjointNets**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-214">**DisjointNets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-215">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-216">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-217">Indica se è possibile eseguire l'override del binding di porta predefinito per un socket utilizzato per inviare query a server DNS remoti.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-217">Indicates whether the default port binding for a socket used to send queries to remote DNS Servers can be overridden.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-218">**DsAvailable**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-218">**DsAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-219">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-221">Indica se esiste un DS disponibile nel server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-221">Indicates whether there is an available DS on the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-222">**DsPollingInterval**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-222">**DsPollingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-223">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-224">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-224">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-225">Intervallo, in secondi, per il polling delle zone integrate in DS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-225">Interval, in seconds, to poll the DS-integrated zones.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-226">**DsTombstoneInterval**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-226">**DsTombstoneInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-227">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-228">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-229">Durata dei record contrassegnati per la rimozione definitiva nelle zone integrate del servizio directory, espressa in secondi.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-229">Lifetime of tombstoned records in Directory Service integrated zones, expressed in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-230">**EDnsCacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-230">**EDnsCacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-231">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-231">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-232">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-233">Durata, in secondi, delle informazioni memorizzate nella cache che descrivono la versione di EDNS supportata da altri server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-233">Lifetime, in seconds, of the cached information describing the EDNS version supported by other DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-234">**EnableDirectoryPartitions**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-234">**EnableDirectoryPartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-235">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-236">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-237">Specifica se il supporto per le partizioni di directory applicative è abilitato nel server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-237">Specifies whether support for application directory partitions is enabled on the DNS Server.</span></span>

<span data-ttu-id="dcfe5-238">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="dcfe5-238">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="dcfe5-239">Questo metodo è denominato EnableDirectoryPartitionSupport.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-239">This method is named EnableDirectoryPartitionSupport.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-240">**EnableDnsSec**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-240">**EnableDnsSec**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-241">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-242">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-243">Specifica se il server DNS include RRs, KEY, SIG e NXT specifici per DNSSEC in una risposta, nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="dcfe5-243">Specifies whether the DNS Server includes DNSSEC-specific RRs, KEY, SIG, and NXT in a response, per the following table:</span></span>



| <span data-ttu-id="dcfe5-244">Valore</span><span class="sxs-lookup"><span data-stu-id="dcfe5-244">Value</span></span>                                                                                                | <span data-ttu-id="dcfe5-245">Significato</span><span class="sxs-lookup"><span data-stu-id="dcfe5-245">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="dcfe5-246"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-246"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-247">Nessun record DNSSEC viene incluso nella risposta a meno che la query non abbia richiesto un set di record di risorse del tipo di record DNSSEC.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-247">No DNSSEC records are included in the response unless the query requested a resource record set of the DNSSEC record type.</span></span><br/>          |
| <span id="1"></span><dl> <span data-ttu-id="dcfe5-248"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-248"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-249">I record DNSSEC sono inclusi nella risposta in base allo standard RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-249">DNSSEC records are included in the response according to RFC 2535.</span></span><br/>                                                                  |
| <span id="2"></span><dl> <span data-ttu-id="dcfe5-250"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-250"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-251">I record DNSSEC sono inclusi in una risposta solo se la query client originale conteneva il record di risorse OPT in base allo standard RFC 2671</span><span class="sxs-lookup"><span data-stu-id="dcfe5-251">DNSSEC records are included in a response only if the original client query contained the OPT resource record according to RFC 2671</span></span><br/> |



 

<span data-ttu-id="dcfe5-252">Se una query richiede un set di record di risorse del tipo DNSSEC, il server DNS risponde sempre con tali record, se disponibili.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-252">If a query requests a resource record set of the DNSSEC type, the DNS Server always responds with such records, if available.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-253">**EnableEDnsProbes**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-253">**EnableEDnsProbes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-254">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-254">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-255">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-255">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-256">Specifica il comportamento del server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-256">Specifies the behavior of the DNS Server.</span></span> <span data-ttu-id="dcfe5-257">Se il valore è TRUE, il server DNS risponde sempre con i record di risorse OPT in base allo standard RFC 2671, a meno che il server remoto non abbia indicato che non supporta EDNS in uno scambio precedente.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-257">When TRUE, the DNS Server always responds with OPT resource records according to RFC 2671, unless the remote server has indicated it does not support EDNS in a prior exchange.</span></span> <span data-ttu-id="dcfe5-258">Se FALSE, il server DNS risponde alle query con opz solo se le opz vengono inviate nella query originale.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-258">If FALSE, the DNS Server responds to queries with OPTs only if OPTs are sent in the original query.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-259">**EventLogLevel**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-259">**EventLogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-260">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-260">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-261">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-261">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-262">Indica gli eventi registrati dal server DNS nel registro di sistema Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-262">Indicates which events the DNS Server records in the Event Viewer system log.</span></span> <span data-ttu-id="dcfe5-263">Vengono utilizzati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-263">The following values are used.</span></span>



| <span data-ttu-id="dcfe5-264">Valore</span><span class="sxs-lookup"><span data-stu-id="dcfe5-264">Value</span></span>                                                                                                | <span data-ttu-id="dcfe5-265">Significato</span><span class="sxs-lookup"><span data-stu-id="dcfe5-265">Meaning</span></span>                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="dcfe5-266"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-266"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-267">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-267">None.</span></span><br/>                         |
| <span id="1"></span><dl> <span data-ttu-id="dcfe5-268"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-268"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-269">Registra solo gli errori.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-269">Log only errors.</span></span><br/>              |
| <span id="2"></span><dl> <span data-ttu-id="dcfe5-270"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-270"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-271">Registra solo avvisi ed errori.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-271">Log only warnings and errors.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="dcfe5-272"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-272"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-273">Registra tutti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-273">Log all events.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="dcfe5-274">**ForwardDelegations**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-274">**ForwardDelegations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-275">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-276">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-276">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-277">Specifica se le query nelle sottozone delegate vengono trasmesse.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-277">Specifies whether queries to delegated sub-zones are forwarded.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-278">**Server d'inoltro**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-278">**Forwarders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-279">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-279">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-280">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-280">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-281">Enumera l'elenco di indirizzi IP dei server d'indirizzamento a cui il server DNS esegue l'inoltri.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-281">Enumerates the list of IP addresses of Forwarders to which the DNS Server forwards queries.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-282">**ForwardingTimeout**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-282">**ForwardingTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-283">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-284">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-284">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-285">Tempo, in secondi, in cui un server DNS che invia una query attenderà la risoluzione dal server d' [*avvio prima di*](f-gly.md) tentare di risolvere la query stessa.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-285">Time, in seconds, a DNS Server forwarding a query will wait for resolution from the [*forwarder*](f-gly.md) before attempting to resolve the query itself.</span></span>

<span data-ttu-id="dcfe5-286">Questo valore non è significativo se il server di inoltri non è impostato per utilizzare la ricorsione.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-286">This value is meaningless if the forwarding server is not set to use recursion.</span></span> <span data-ttu-id="dcfe5-287">Per determinare questo problema, controllare la proprietà booleana slave.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-287">To determine this, check the IsSlave Boolean property.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-288">**Slave**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-288">**IsSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-289">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-290">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-291">**True** se il server DNS non utilizza la ricorsione quando la risoluzione dei nomi tramite i server d'avanzamento ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-291">**TRUE** if the DNS server does not use recursion when name-resolution through forwarders fails.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-292">**ListenAddresses**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-292">**ListenAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-293">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-294">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-294">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-295">Enumera l'elenco di indirizzi IP su cui il server DNS può ricevere le query.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-295">Enumerates the list of IP addresses on which the DNS Server can receive queries.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-296">**LocalNetPriority**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-296">**LocalNetPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-297">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-298">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-298">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-299">Indica se il server DNS assegna la priorità all'indirizzo di rete locale quando viene restituito un record.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-299">Indicates whether the DNS Server gives priority to the local net address when returning A records.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-300">**LogFileMaxSize**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-300">**LogFileMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-301">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-302">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-302">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-303">Dimensioni in byte del log di debug del server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-303">Size of the DNS Server debug log, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-304">**LogFilePath**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-304">**LogFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-305">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-306">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-306">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-307">Nome file e percorso del log di debug del server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-307">File name and path for the DNS Server debug log.</span></span> <span data-ttu-id="dcfe5-308">Il valore predefinito è% system32% \\ DNS \\ . log.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-308">Default is %system32%\\dns\\dns.log.</span></span> <span data-ttu-id="dcfe5-309">I percorsi relativi sono relativi a% SystemRoot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-309">Relative paths are relative to %Systemroot%\\System32.</span></span> <span data-ttu-id="dcfe5-310">È possibile utilizzare i percorsi assoluti, ma i percorsi UNC non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-310">Absolute paths may be used, but UNC paths are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-311">**LogIPFilterList**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-311">**LogIPFilterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-312">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-312">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-313">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-313">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-314">Elenco di indirizzi IP utilizzati per filtrare gli eventi DNS scritti nel log di debug.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-314">List of IP addresses used to filter DNS events written to the debug log.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-315">**LogLevel**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-315">**LogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-316">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-317">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-317">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-318">Indica i criteri attivati nel registro di sistema Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-318">Indicates which policies are activated in the Event Viewer system log.</span></span>

<span data-ttu-id="dcfe5-319">Deve essere impostato su valori specifici in base all'algoritmo seguente: ogni criterio (da attivare nel registro di sistema Visualizzatore eventi) viene assegnato a un valore specifico.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-319">Should be set to specific values based on the following algorithm: Every policy (to be activated in the Event Viewer system log) is assigned a specific value.</span></span>



| <span data-ttu-id="dcfe5-320">Valore</span><span class="sxs-lookup"><span data-stu-id="dcfe5-320">Value</span></span>                                                                                                                  | <span data-ttu-id="dcfe5-321">Significato</span><span class="sxs-lookup"><span data-stu-id="dcfe5-321">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="dcfe5-322"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-322"><dt>**1**</dt></span></span> </dl>                   | <span data-ttu-id="dcfe5-323">Query.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-323">Query.</span></span><br/>                                   |
| <span id="16"></span><dl> <span data-ttu-id="dcfe5-324"><dt>**16**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-324"><dt>**16**</dt></span></span> </dl>                 | <span data-ttu-id="dcfe5-325">Comunica.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-325">Notify.</span></span><br/>                                  |
| <span id="32"></span><dl> <span data-ttu-id="dcfe5-326"><dt>**32**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-326"><dt>**32**</dt></span></span> </dl>                 | <span data-ttu-id="dcfe5-327">Aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-327">Update.</span></span><br/>                                  |
| <span id="254"></span><dl> <span data-ttu-id="dcfe5-328"><dt>**254**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-328"><dt>**254**</dt></span></span> </dl>               | <span data-ttu-id="dcfe5-329">Transazioni non query.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-329">Nonquery transactions.</span></span><br/>                   |
| <span id="256"></span><dl> <span data-ttu-id="dcfe5-330"><dt>**256**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-330"><dt>**256**</dt></span></span> </dl>               | <span data-ttu-id="dcfe5-331">Domande.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-331">Questions.</span></span><br/>                               |
| <span id="512"></span><dl> <span data-ttu-id="dcfe5-332"><dt>**512**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-332"><dt>**512**</dt></span></span> </dl>               | <span data-ttu-id="dcfe5-333">Risposte.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-333">Answers.</span></span><br/>                                 |
| <span id="4096"></span><dl> <span data-ttu-id="dcfe5-334"><dt>**4096**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-334"><dt>**4096**</dt></span></span> </dl>             | <span data-ttu-id="dcfe5-335">Trasmissione.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-335">Send.</span></span><br/>                                    |
| <span id="8192"></span><dl> <span data-ttu-id="dcfe5-336"><dt>**8192**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-336"><dt>**8192**</dt></span></span> </dl>             | <span data-ttu-id="dcfe5-337">Ricezione.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-337">Receive.</span></span><br/>                                 |
| <span id="16384"></span><dl> <span data-ttu-id="dcfe5-338"><dt>**16384**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-338"><dt>**16384**</dt></span></span> </dl>           | <span data-ttu-id="dcfe5-339">UDP.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-339">UDP.</span></span><br/>                                     |
| <span id="32768"></span><dl> <span data-ttu-id="dcfe5-340"><dt>**32768**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-340"><dt>**32768**</dt></span></span> </dl>           | <span data-ttu-id="dcfe5-341">TCP.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-341">TCP.</span></span><br/>                                     |
| <span id="65535"></span><dl> <span data-ttu-id="dcfe5-342"><dt>**65535**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-342"><dt>**65535**</dt></span></span> </dl>           | <span data-ttu-id="dcfe5-343">Tutti i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-343">All packets.</span></span><br/>                             |
| <span id="65536"></span><dl> <span data-ttu-id="dcfe5-344"><dt>**65536**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-344"><dt>**65536**</dt></span></span> </dl>           | <span data-ttu-id="dcfe5-345">Transazione di scrittura del servizio directory NT.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-345">NT Directory Service write transaction.</span></span><br/>  |
| <span id="131072"></span><dl> <span data-ttu-id="dcfe5-346"><dt>**131072**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-346"><dt>**131072**</dt></span></span> </dl>         | <span data-ttu-id="dcfe5-347">Transazione di aggiornamento del servizio directory NT.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-347">NT Directory Service update transaction.</span></span><br/> |
| <span id="16777216"></span><dl> <span data-ttu-id="dcfe5-348"><dt>**16777216**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-348"><dt>**16777216**</dt></span></span> </dl>     | <span data-ttu-id="dcfe5-349">Pacchetti completi.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-349">Full packets.</span></span><br/>                            |
| <span id="2147483648"></span><dl> <span data-ttu-id="dcfe5-350"><dt>**2147483648**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-350"><dt>**2147483648**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-351">Scrivere.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-351">Write through.</span></span><br/>                           |



 

<span data-ttu-id="dcfe5-352">La somma dei valori corrispondenti a tutti i criteri da attivare è indicata in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-352">The sum of the values corresponding to all the policies to be activated is indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-353">**LooseWildcarding**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-353">**LooseWildcarding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-354">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-355">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-355">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-356">Indica se il server DNS esegue caratteri jolly separati.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-356">Indicates whether the DNS Server performs loose wildcarding.</span></span> <span data-ttu-id="dcfe5-357">Se non è definito o zero, il server segue il comportamento dei caratteri jolly specificato nella RFC DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-357">If undefined or zero, the server follows the wildcarding behavior specified in the DNS RFC.</span></span> <span data-ttu-id="dcfe5-358">In questo caso, è consigliabile che un amministratore includa i record MX per tutti gli host che non sono in grado di ricevere messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-358">In this case, an administrator is advised to include MX records for all hosts incapable of receiving mail.</span></span> <span data-ttu-id="dcfe5-359">Se è diverso da zero, il server cerca il nodo con caratteri jolly più vicino; in questo caso, un amministratore deve inserire i record MX nella radice della zona e in un nodo con caratteri jolly (' \* ') direttamente sotto la radice della zona.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-359">If nonzero, the server seeks the closest wildcard node; in this case, an administrator should put MX records at the zone root and in a wildcard node ('\*') directly below the zone root.</span></span> <span data-ttu-id="dcfe5-360">Inoltre, gli amministratori devono inserire record MX autoreferenziali negli host che ricevono la propria posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-360">Also, administrators should put self-referencing MX records on hosts that receive their own mail.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-361">**MaxCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-361">**MaxCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-362">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-363">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-363">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-364">Tempo massimo, in secondi, per cui il record di una query con nome ricorsivo può rimanere nella cache del server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-364">Maximum time, in seconds, the record of a recursive name query may remain in the DNS Server cache.</span></span> <span data-ttu-id="dcfe5-365">Il server DNS elimina i record dalla cache quando il valore di questa voce scade, anche se il valore del campo TTL nel record è maggiore.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-365">The DNS Server deletes records from the cache when the value of this entry expires, even if the value of the TTL field in the record is greater.</span></span>

<span data-ttu-id="dcfe5-366">Il valore predefinito di questa proprietà è 86.400 secondi (1 giorno).</span><span class="sxs-lookup"><span data-stu-id="dcfe5-366">The default value of this property is 86,400 seconds (1 day).</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-367">**MaxNegativeCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-367">**MaxNegativeCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-368">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-369">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-369">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-370">Tempo massimo, in secondi, in cui un errore di nome deriva da una query ricorsiva può rimanere nella cache del server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-370">Maximum time, in seconds, a name error result from a recursive query may remain in the DNS Server cache.</span></span> <span data-ttu-id="dcfe5-371">DNS elimina i record dalla cache quando questo timer scade, anche se il campo TTL è maggiore.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-371">DNS deletes records from the cache when this timer expires, even if the TTL field is greater.</span></span> <span data-ttu-id="dcfe5-372">Il valore predefinito è 86.400 (un giorno).</span><span class="sxs-lookup"><span data-stu-id="dcfe5-372">Default value is 86,400 (one day).</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-373">**Nome**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-374">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-376">Nome di dominio completo (FQDN) o indirizzo IP del server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-376">Fully qualified domain name (FQDN) or IP address of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-377">**NameCheckFlag**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-377">**NameCheckFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-378">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-379">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-379">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-380">Indica il set di caratteri idonei da usare nei nomi DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-380">Indicates the set of eligible characters to be used in DNS names.</span></span> <span data-ttu-id="dcfe5-381">Vengono utilizzati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-381">The following values are used.</span></span>



| <span data-ttu-id="dcfe5-382">Valore</span><span class="sxs-lookup"><span data-stu-id="dcfe5-382">Value</span></span>                                                                                                | <span data-ttu-id="dcfe5-383">Significato</span><span class="sxs-lookup"><span data-stu-id="dcfe5-383">Meaning</span></span>                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="dcfe5-384"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-384"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-385">RFC rigoroso (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dcfe5-385">Strict RFC (ANSI)</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="dcfe5-386"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-386"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-387">Non RFC (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dcfe5-387">Non RFC (ANSI)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="dcfe5-388"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-388"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-389">Multibyte (UTF8)</span><span class="sxs-lookup"><span data-stu-id="dcfe5-389">Multibyte (UTF8)</span></span><br/>  |



 

<span data-ttu-id="dcfe5-390">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="dcfe5-390">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="dcfe5-391">Il valore "2" indica "any".</span><span class="sxs-lookup"><span data-stu-id="dcfe5-391">A value of "2" indicates "Any."</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-392">**NoRecursion**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-392">**NoRecursion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-393">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-393">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-394">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-394">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-395">Indica se il server DNS esegue ricerche ricorsive.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-395">Indicates whether the DNS Server performs recursive look ups.</span></span> <span data-ttu-id="dcfe5-396">TRUE indica che le ricerche ricorsive non vengono eseguite.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-396">TRUE indicates recursive look ups are not performed.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-397">**RecursionRetry**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-397">**RecursionRetry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-398">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-399">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-399">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-400">Secondi trascorsi prima di riprovare a eseguire una ricerca ricorsiva.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-400">Elapsed seconds before retrying a recursive look up.</span></span> <span data-ttu-id="dcfe5-401">Se la proprietà è undefined o zero, i tentativi vengono eseguiti dopo tre secondi.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-401">If the property is undefined or zero, retries are made after three seconds.</span></span> <span data-ttu-id="dcfe5-402">Gli utenti sono sconsigliati di modificare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-402">Users are discouraged from altering this property.</span></span> <span data-ttu-id="dcfe5-403">In alcune situazioni la proprietà deve essere modificata. un esempio è quando il server DNS Contatta i server remoti tramite un collegamento lento e il server DNS viene ritentato prima di ricevere la risposta dal DNS remoto.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-403">There are certain situations when the property should be changed; one example is when the DNS Server contacts remote servers over a slow link, and the DNS Server is retrying before receiving response from the remote DNS.</span></span> <span data-ttu-id="dcfe5-404">In questo caso, l'aumento del timeout per un tempo leggermente superiore rispetto al tempo di risposta osservato dal DNS remoto sarebbe ragionevole.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-404">In this case, raising the time out to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-405">**RecursionTimeout**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-405">**RecursionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-406">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-406">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-407">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-407">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-408">Secondi trascorsi i quali il server DNS assegna una query ricorsiva.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-408">Elapsed seconds before the DNS Server gives up recursive query.</span></span> <span data-ttu-id="dcfe5-409">Se la proprietà è indefinita o zero, il server DNS si concede dopo 15 secondi.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-409">If the property is undefined or zero, the DNS Server gives up after 15 seconds.</span></span> <span data-ttu-id="dcfe5-410">In generale, il timeout di 15 secondi è sufficiente per consentire a qualsiasi risposta in attesa di tornare al server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-410">In general, the 15-second time out is sufficient to allow any outstanding response to get back to the DNS Server.</span></span>

<span data-ttu-id="dcfe5-411">Gli utenti sono sconsigliati di modificare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-411">Users are discouraged from altering this property.</span></span> <span data-ttu-id="dcfe5-412">Uno scenario in cui la proprietà deve essere modificata è quando il server DNS Contatta i server remoti tramite un collegamento lento e il server DNS rileva il rifiuto delle query (con errore del SERVER \_ ) prima della ricezione delle risposte.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-412">One scenario where the property should be changed is when the DNS Server contacts remote servers over a slow link, and the DNS Server is observed rejecting queries (with SERVER\_FAILURE) before responses are received.</span></span>

<span data-ttu-id="dcfe5-413">I resolver client ritentano anche le query, quindi è necessaria un'attenta analisi per determinare se le risposte remote sono effettivamente associate alla query che ha raggiunto il timeout. In questo caso, l'aumento del valore di timeout leggermente superiore al tempo di risposta osservato dal DNS remoto sarebbe ragionevole.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-413">Client resolvers also retry queries, so careful investigation is required to determine whether remote responses are actually associated with the query that timed out. In this case, raising the time out value to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-414">**RoundRobin**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-414">**RoundRobin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-415">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-416">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-416">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-417">Indica se il server DNS round robin ha più record A.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-417">Indicates whether the DNS Server round robins multiple A records.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-418">**RpcProtocol**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-418">**RpcProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-419">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-419">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-420">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-420">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-421">Protocollo o protocolli RPC su cui viene eseguita la RPC amministrativa.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-421">RPC protocol or protocols over which administrative RPC runs.</span></span> <span data-ttu-id="dcfe5-422">Per assegnare un valore specifico, viene usato l'algoritmo seguente:</span><span class="sxs-lookup"><span data-stu-id="dcfe5-422">The following algorithm is used to assign a specific value:</span></span>



| <span data-ttu-id="dcfe5-423">Valore</span><span class="sxs-lookup"><span data-stu-id="dcfe5-423">Value</span></span>                                                                                                | <span data-ttu-id="dcfe5-424">Significato</span><span class="sxs-lookup"><span data-stu-id="dcfe5-424">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="dcfe5-425"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-425"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-426">nessuno</span><span class="sxs-lookup"><span data-stu-id="dcfe5-426">None</span></span><br/>        |
| <span id="1"></span><dl> <span data-ttu-id="dcfe5-427"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-427"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-428">TCP</span><span class="sxs-lookup"><span data-stu-id="dcfe5-428">TCP</span></span><br/>         |
| <span id="2"></span><dl> <span data-ttu-id="dcfe5-429"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-429"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-430">Named Pipe</span><span class="sxs-lookup"><span data-stu-id="dcfe5-430">Named Pipes</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="dcfe5-431"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-431"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="dcfe5-432">LPC</span><span class="sxs-lookup"><span data-stu-id="dcfe5-432">LPC</span></span><br/>         |



 

<span data-ttu-id="dcfe5-433">La somma dei valori indica i protocolli utilizzati.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-433">The sum of the values indicates the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-434">**ScavengingInterval**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-434">**ScavengingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-435">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-435">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-436">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-436">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-437">Intervallo, in ore, tra due operazioni di scavenging consecutive eseguite dal server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-437">Interval, in hours, between two consecutive scavenging operations performed by the DNS Server.</span></span> <span data-ttu-id="dcfe5-438">Zero indica che lo scavenging è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-438">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="dcfe5-439">Il valore predefinito è 168 ore (sette giorni).</span><span class="sxs-lookup"><span data-stu-id="dcfe5-439">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-440">**SecureResponses**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-440">**SecureResponses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-441">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-441">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-442">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-442">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-443">Indica se il server DNS Salva esclusivamente i record di nomi nello stesso sottoalbero del server in cui sono stati forniti.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-443">Indicates whether the DNS Server exclusively saves records of names in the same subtree as the server that provided them.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-444">**SendPort**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-444">**SendPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-445">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-446">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-446">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-447">Porta su cui il server DNS invia query UDP ad altri server.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-447">Port on which the DNS Server sends UDP queries to other servers.</span></span> <span data-ttu-id="dcfe5-448">Per impostazione predefinita, il server DNS invia query su un socket associato alla porta DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-448">By default, the DNS Server sends queries on a socket bound to the DNS port.</span></span>

<span data-ttu-id="dcfe5-449">In determinate situazioni, questa non è la configurazione migliore.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-449">Under certain situations, this is not the best configuration.</span></span> <span data-ttu-id="dcfe5-450">Un caso ovvio è quando un amministratore blocca la porta DNS con un firewall per impedire l'accesso esterno al server DNS, ma vuole comunque che il server sia in grado di contattare i server DNS Internet per fornire la risoluzione dei nomi per i client interni.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-450">One obvious case is when an administrator blocks the DNS port with a firewall to prevent outside access to the DNS Server, but still wants the server to be able to contact Internet DNS Servers to provide name resolution for internal clients.</span></span> <span data-ttu-id="dcfe5-451">Un altro caso è quello in cui il server DNS supporta le reti non contigue (la proprietà **DisjointNets** impostata su true identifica questo scenario).</span><span class="sxs-lookup"><span data-stu-id="dcfe5-451">Another case is when the DNS Server is supporting disjoint nets (the property **DisjointNets** set to TRUE identifies this scenario).</span></span> <span data-ttu-id="dcfe5-452">In questi casi, l'impostazione della proprietà **SendOnNonDnsPort** su un valore diverso da zero indica al server DNS di eseguire l'associazione a una porta arbitraria per l'invio a server DNS remoti.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-452">In these cases, setting the **SendOnNonDnsPort** property to a nonzero value directs the DNS Server to bind to an arbitrary port for sending to remote DNS Servers.</span></span>

<span data-ttu-id="dcfe5-453">Se il valore di **SendOnNonDnsPort** è maggiore di 1024, il server DNS viene associato in modo esplicito al valore della porta specificato.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-453">If the **SendOnNonDnsPort** value is greater than 1024, the DNS Server binds explicitly to the port value given.</span></span> <span data-ttu-id="dcfe5-454">Questa opzione di configurazione è utile quando un amministratore deve correggere la porta di query DNS per finalità del firewall.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-454">This configuration option is useful when an administrator needs to fix the DNS query port for firewall purposes.</span></span>

<span data-ttu-id="dcfe5-455">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="dcfe5-455">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="dcfe5-456">Se si imposta la proprietà SendPort su un valore diverso da zero, il server DNS eseguirà l'associazione a una porta arbitraria per l'invio a server DNS remoti.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-456">Setting the SendPort property to a non-zero value causes the DNS server to bind to an arbitrary port for sending to remote DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-457">**ServerAddresses**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-457">**ServerAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-458">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-458">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-459">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-460">Enumera l'elenco di indirizzi IP per il server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-460">Enumerates the list of IP addresses for the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-461">**StrictFileParsing**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-461">**StrictFileParsing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-462">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-462">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-463">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-463">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-464">Indica se il server DNS analizza rigorosamente [*i file di zona*](z-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="dcfe5-464">Indicates whether the DNS Server parses [*zone files*](z-gly.md) strictly.</span></span> <span data-ttu-id="dcfe5-465">Se non è definito o zero, il server registrerà e ignorerà i dati non validi nel file di zona e continuerà a essere caricato.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-465">If undefined or zero, the server will log and ignore bad data in the zone file and continue to load.</span></span> <span data-ttu-id="dcfe5-466">Se è diverso da zero, il server registrerà e non riuscirà in caso di errori nel file di zona.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-466">If nonzero, the server will log and fail on zone file errors.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-467">**UpdateOptions**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-467">**UpdateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-468">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-469">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-470">Limita il tipo di record che possono essere aggiornati dinamicamente sul server, usati in aggiunta alle impostazioni di **AllowUpdate** negli oggetti server e zona.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-470">Restricts the type of records that can be dynamically updated on the server, used in addition to the **AllowUpdate** settings on Server and Zone objects.</span></span>

<span data-ttu-id="dcfe5-471">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="dcfe5-471">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="dcfe5-472">0: nessuna restrizione.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-472">0: No restrictions.</span></span>

<span data-ttu-id="dcfe5-473">1: non consente aggiornamenti dinamici di record SOA.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-473">1: Do not allow dynamic updates of SOA records.</span></span>

<span data-ttu-id="dcfe5-474">2: non consentire aggiornamenti dinamici di record NS nella radice della zona.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-474">2: Do not allow dynamic updates of NS records at the zone root.</span></span>

<span data-ttu-id="dcfe5-475">4: non consentire aggiornamenti dinamici di record NS non nella radice della zona (record NS di delega).</span><span class="sxs-lookup"><span data-stu-id="dcfe5-475">4: Do not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span>

<span data-ttu-id="dcfe5-476">Sommare questi valori per determinare il valore dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-476">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-477">**Versione**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-477">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-478">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-479">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-480">Versione del server DNS.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-480">Version of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-481">**WriteAuthorityNS**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-481">**WriteAuthorityNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-482">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-483">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-483">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-484">Specifica se il server DNS scrive i record NS e SOA nella sezione Authority in seguito alla risposta corretta.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-484">Specifies whether the DNS Server writes NS and SOA records to the authority section on successful response.</span></span>

</dd> <dt>

<span data-ttu-id="dcfe5-485">**XfrConnectTimeout**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-485">**XfrConnectTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfe5-486">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcfe5-487">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dcfe5-487">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dcfe5-488">Tempo, in secondi, in cui il server DNS attende una connessione TCP riuscita a un server remoto durante il tentativo di trasferimento di zona.</span><span class="sxs-lookup"><span data-stu-id="dcfe5-488">Time, in seconds, the DNS Server waits for a successful TCP connection to a remote server when attempting a zone transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dcfe5-489">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcfe5-489">Requirements</span></span>



| <span data-ttu-id="dcfe5-490">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcfe5-490">Requirement</span></span> | <span data-ttu-id="dcfe5-491">Valore</span><span class="sxs-lookup"><span data-stu-id="dcfe5-491">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfe5-492">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcfe5-492">Minimum supported client</span></span><br/> | <span data-ttu-id="dcfe5-493">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dcfe5-493">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dcfe5-494">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcfe5-494">Minimum supported server</span></span><br/> | <span data-ttu-id="dcfe5-495">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dcfe5-495">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dcfe5-496">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dcfe5-496">Namespace</span></span><br/>                | <span data-ttu-id="dcfe5-497">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="dcfe5-497">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dcfe5-498">MOF</span><span class="sxs-lookup"><span data-stu-id="dcfe5-498">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcfe5-499"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcfe5-499"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcfe5-500">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcfe5-500">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcfe5-501">**Metodo StartService della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-501">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="dcfe5-502">**Metodo StopService della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-502">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="dcfe5-503">**Metodo StartScavenging della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-503">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="dcfe5-504">**Metodo getdistinguishname della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dcfe5-504">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





