---
title: Classe MicrosoftDNS_Domain
description: La \_ classe di dominio MicrosoftDNS rappresenta un dominio in una gerarchia DNS.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- DNS della classe MicrosoftDNS_Domain
- MicrosoftDNS_Domain della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119790"
---
# <a name="microsoftdns_domain-class"></a><span data-ttu-id="d3b58-105">\_Classe di dominio MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="d3b58-105">MicrosoftDNS\_Domain class</span></span>

<span data-ttu-id="d3b58-106">La classe di **\_ dominio MicrosoftDNS** rappresenta un dominio in una gerarchia DNS.</span><span class="sxs-lookup"><span data-stu-id="d3b58-106">The **MicrosoftDNS\_Domain** class represents a Domain in a DNS hierarchy.</span></span>

<span data-ttu-id="d3b58-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="d3b58-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b58-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3b58-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="d3b58-109">Members</span><span class="sxs-lookup"><span data-stu-id="d3b58-109">Members</span></span>

<span data-ttu-id="d3b58-110">La classe di **\_ dominio MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d3b58-110">The **MicrosoftDNS\_Domain** class has these types of members:</span></span>

-   [<span data-ttu-id="d3b58-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="d3b58-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d3b58-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d3b58-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d3b58-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="d3b58-113">Methods</span></span>

<span data-ttu-id="d3b58-114">La classe di **\_ dominio MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d3b58-114">The **MicrosoftDNS\_Domain** class has these methods.</span></span>



| <span data-ttu-id="d3b58-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="d3b58-115">Method</span></span>                   | <span data-ttu-id="d3b58-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3b58-116">Description</span></span>                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b58-117">**Getdistinguishname**</span><span class="sxs-lookup"><span data-stu-id="d3b58-117">**GetDistinguishedName**</span></span> | <span data-ttu-id="d3b58-118">Ottiene il nome distinto DS per la zona.</span><span class="sxs-lookup"><span data-stu-id="d3b58-118">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="d3b58-119">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="d3b58-119">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d3b58-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d3b58-120">Properties</span></span>

<span data-ttu-id="d3b58-121">La classe di **\_ dominio MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3b58-121">The **MicrosoftDNS\_Domain** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3b58-122">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="d3b58-122">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3b58-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d3b58-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3b58-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3b58-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3b58-125">Nome del contenitore del dominio, che può essere una zona, una cache o un RootHints.</span><span class="sxs-lookup"><span data-stu-id="d3b58-125">Name of the container of the domain, which could be a Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="d3b58-126">Nei casi in cui il contenitore è una zona (un'istanza della classe di [**\_ zona MicrosoftDNS**](microsoftdns-zone.md) ), questa proprietà contiene il nome di dominio completo della zona.</span><span class="sxs-lookup"><span data-stu-id="d3b58-126">In cases where the Container is a Zone (an instance of the [**MicrosoftDNS\_Zone**](microsoftdns-zone.md) class), this property contains the FQDN of the Zone.</span></span>

<span data-ttu-id="d3b58-127">Quando il contenitore è la zona radice, la stringa \\ \\ deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d3b58-127">When the Container is the root zone, the string \\.\\ should be used.</span></span>

<span data-ttu-id="d3b58-128">Nei casi in cui il contenitore è la cache DNS dei record di risorse (un'istanza della classe della [**\_ cache MicrosoftDNS**](microsoftdns-cache.md) ), questa proprietà viene impostata sulla stringa \\ .. Cache \\ .</span><span class="sxs-lookup"><span data-stu-id="d3b58-128">In cases where the Container is the DNS cache of resource records (an instance of the [**MicrosoftDNS\_Cache**](microsoftdns-cache.md) class), this property is set to the string \\..Cache\\.</span></span>

<span data-ttu-id="d3b58-129">Se il contenitore è RootHints (un'istanza della classe [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md) ), questa proprietà deve essere impostata su \\ . RootHints \\ .</span><span class="sxs-lookup"><span data-stu-id="d3b58-129">If the Container is RootHints (an instance of the [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md) class), this property should be set to \\..RootHints\\.</span></span>

</dd> <dt>

<span data-ttu-id="d3b58-130">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="d3b58-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3b58-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d3b58-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3b58-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3b58-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3b58-133">FQDN o indirizzo IP del server DNS che contiene il dominio.</span><span class="sxs-lookup"><span data-stu-id="d3b58-133">FQDN or IP address of the DNS Server that contains the domain.</span></span>

</dd> <dt>

<span data-ttu-id="d3b58-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d3b58-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3b58-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d3b58-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3b58-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3b58-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3b58-137">FQDN del dominio.</span><span class="sxs-lookup"><span data-stu-id="d3b58-137">FQDN of the domain.</span></span>

<span data-ttu-id="d3b58-138">Per le istanze della cache DNS o RootHints, le stringhe \\ .. Memorizza nella cache \\ e \\ .. \\ È necessario usare RootHints, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="d3b58-138">For instances of DNS Cache or RootHints, the strings \\..Cache\\ and \\..RootHints\\ should be used, respectively.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3b58-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3b58-139">Requirements</span></span>



| <span data-ttu-id="d3b58-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3b58-140">Requirement</span></span> | <span data-ttu-id="d3b58-141">Valore</span><span class="sxs-lookup"><span data-stu-id="d3b58-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b58-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3b58-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b58-143">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d3b58-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d3b58-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3b58-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b58-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d3b58-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d3b58-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d3b58-146">Namespace</span></span><br/>                | <span data-ttu-id="d3b58-147">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="d3b58-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d3b58-148">MOF</span><span class="sxs-lookup"><span data-stu-id="d3b58-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3b58-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3b58-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3b58-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3b58-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b58-151">**Metodo getdistinguishname della classe di \_ dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d3b58-151">**GetDistinguishedName Method of the MicrosoftDNS\_Domain Class**</span></span>](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





