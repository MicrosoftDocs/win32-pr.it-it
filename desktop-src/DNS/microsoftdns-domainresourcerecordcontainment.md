---
title: Classe MicrosoftDNS_DomainResourceRecordContainment
description: La \_ classe MicrosoftDNS DomainResourceRecordContainment viene usata per il contenimento del record RR. ogni istanza del \_ dominio MicrosoftDNS può contenere più istanze della \_ classe MicrosoftDNS ResourceRecord.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- DNS della classe MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476756"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a><span data-ttu-id="934ba-105">\_Classe MicrosoftDNS DomainResourceRecordContainment</span><span class="sxs-lookup"><span data-stu-id="934ba-105">MicrosoftDNS\_DomainResourceRecordContainment class</span></span>

<span data-ttu-id="934ba-106">La classe **MicrosoftDNS \_ DomainResourceRecordContainment** viene usata per il contenimento del record RR. ogni istanza del [**\_ dominio MicrosoftDNS**](microsoftdns-domain.md) può contenere più istanze della classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="934ba-106">The **MicrosoftDNS\_DomainResourceRecordContainment** class is used for RR containment; every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) may contain multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span> <span data-ttu-id="934ba-107">Ogni istanza della classe **MicrosoftDNS \_ ResourceRecord** appartiene a una singola istanza della classe di **\_ dominio MicrosoftDNS** e viene definita debole per tale istanza.</span><span class="sxs-lookup"><span data-stu-id="934ba-107">Every instance of the **MicrosoftDNS\_ResourceRecord** class belongs to a single instance of the **MicrosoftDNS\_Domain** class, and is defined to be weak to that instance.</span></span>

<span data-ttu-id="934ba-108">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="934ba-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="934ba-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="934ba-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="934ba-110">Members</span><span class="sxs-lookup"><span data-stu-id="934ba-110">Members</span></span>

<span data-ttu-id="934ba-111">La **classe \_ DomainResourceRecordContainment di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="934ba-111">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="934ba-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="934ba-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="934ba-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="934ba-113">Properties</span></span>

<span data-ttu-id="934ba-114">La **classe \_ DomainResourceRecordContainment di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="934ba-114">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="934ba-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="934ba-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934ba-116">Tipo di dati **: \_ dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="934ba-116">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="934ba-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="934ba-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934ba-118">Qualificatori: chiave, override ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="934ba-118">Qualifiers: Key, Override("GroupComponent")</span></span>

<span data-ttu-id="934ba-119">Descrizione: la zona, la cache, RootHints o il dominio contenente direttamente il record di risorse.</span><span class="sxs-lookup"><span data-stu-id="934ba-119">Description: The Zone, Cache, RootHints or Domain directly containing the Resource Record.</span></span>

<span data-ttu-id="934ba-120">Ereditato dal \_ componente CIM</span><span class="sxs-lookup"><span data-stu-id="934ba-120">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="934ba-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="934ba-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934ba-122">Tipo di dati: **MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="934ba-122">Data type: **MicrosoftDNS\_ResourceRecord**</span></span>
</dt> <dt>

<span data-ttu-id="934ba-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="934ba-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934ba-124">Qualificatori: chiave, override ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="934ba-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="934ba-125">Descrizione: il record di risorse contenuto in un dominio, una zona, una cache o un RootHints.</span><span class="sxs-lookup"><span data-stu-id="934ba-125">Description: The resource record contained in a Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="934ba-126">Ereditato dal \_ componente CIM.</span><span class="sxs-lookup"><span data-stu-id="934ba-126">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="934ba-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="934ba-127">Requirements</span></span>



| <span data-ttu-id="934ba-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="934ba-128">Requirement</span></span> | <span data-ttu-id="934ba-129">Valore</span><span class="sxs-lookup"><span data-stu-id="934ba-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="934ba-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="934ba-130">Minimum supported client</span></span><br/> | <span data-ttu-id="934ba-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="934ba-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="934ba-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="934ba-132">Minimum supported server</span></span><br/> | <span data-ttu-id="934ba-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="934ba-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="934ba-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="934ba-134">Namespace</span></span><br/>                | <span data-ttu-id="934ba-135">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="934ba-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="934ba-136">MOF</span><span class="sxs-lookup"><span data-stu-id="934ba-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="934ba-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="934ba-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="934ba-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="934ba-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="934ba-139">**\_ServerDomainContainment MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="934ba-139">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="934ba-140">**\_DomainDomainContainment MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="934ba-140">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="934ba-141">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="934ba-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





