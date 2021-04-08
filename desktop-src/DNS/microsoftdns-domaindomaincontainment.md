---
title: Classe MicrosoftDNS_DomainDomainContainment
description: La \_ classe MicrosoftDNS DomainDomainContainment viene usata per l'indipendenza del dominio; I domini DNS possono contenere altri domini DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- DNS della classe MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048609"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a><span data-ttu-id="500f6-105">\_Classe MicrosoftDNS DomainDomainContainment</span><span class="sxs-lookup"><span data-stu-id="500f6-105">MicrosoftDNS\_DomainDomainContainment class</span></span>

<span data-ttu-id="500f6-106">La classe **MicrosoftDNS \_ DomainDomainContainment** viene usata per l'indipendenza del dominio; I domini DNS possono contenere altri domini DNS.</span><span class="sxs-lookup"><span data-stu-id="500f6-106">The **MicrosoftDNS\_DomainDomainContainment** class is used for domain containment; DNS domains may contain other DNS domains.</span></span> <span data-ttu-id="500f6-107">Ogni istanza della classe [**di \_ dominio MicrosoftDNS**](microsoftdns-domain.md) può contenere più istanze del **\_ dominio MicrosoftDNS**.</span><span class="sxs-lookup"><span data-stu-id="500f6-107">Every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class may contain multiple other instances of **MicrosoftDNS\_Domain**.</span></span> <span data-ttu-id="500f6-108">Un'istanza di un oggetto di **\_ dominio MicrosoftDNS** è contenuta direttamente in non più di un **\_ dominio MicrosoftDNS** di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="500f6-108">An instance of a **MicrosoftDNS\_Domain** object is directly contained in no more than one higher level **MicrosoftDNS\_Domain**.</span></span>

<span data-ttu-id="500f6-109">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="500f6-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="500f6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="500f6-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="500f6-111">Members</span><span class="sxs-lookup"><span data-stu-id="500f6-111">Members</span></span>

<span data-ttu-id="500f6-112">La **classe \_ DomainDomainContainment di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="500f6-112">The **MicrosoftDNS\_DomainDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="500f6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="500f6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="500f6-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="500f6-114">Properties</span></span>

<span data-ttu-id="500f6-115">La **classe \_ DomainDomainContainment di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="500f6-115">The **MicrosoftDNS\_DomainDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="500f6-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="500f6-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="500f6-117">Tipo di dati **: \_ dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="500f6-117">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="500f6-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="500f6-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="500f6-119">Qualificatori: chiave, Max (1), override ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="500f6-119">Qualifiers: Key, Max(1), Override("GroupComponent")</span></span>

<span data-ttu-id="500f6-120">Descrizione: un dominio di livello superiore, una zona, una cache o un RootHints.</span><span class="sxs-lookup"><span data-stu-id="500f6-120">Description: A higher level Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="500f6-121">Ereditato dal \_ componente CIM</span><span class="sxs-lookup"><span data-stu-id="500f6-121">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="500f6-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="500f6-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="500f6-123">Tipo di dati **: \_ dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="500f6-123">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="500f6-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="500f6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="500f6-125">Qualificatori: chiave, override ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="500f6-125">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="500f6-126">Descrizione: dominio contenuto da un dominio di livello superiore, una zona, una cache o un RootHints.</span><span class="sxs-lookup"><span data-stu-id="500f6-126">Description: The Domain contained by a higher level Domain, Zone, Cache or RootHints.</span></span>

<span data-ttu-id="500f6-127">Ereditato dal \_ componente CIM.</span><span class="sxs-lookup"><span data-stu-id="500f6-127">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="500f6-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="500f6-128">Requirements</span></span>



| <span data-ttu-id="500f6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="500f6-129">Requirement</span></span> | <span data-ttu-id="500f6-130">Valore</span><span class="sxs-lookup"><span data-stu-id="500f6-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="500f6-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="500f6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="500f6-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="500f6-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="500f6-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="500f6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="500f6-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="500f6-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="500f6-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="500f6-135">Namespace</span></span><br/>                | <span data-ttu-id="500f6-136">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="500f6-136">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="500f6-137">MOF</span><span class="sxs-lookup"><span data-stu-id="500f6-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="500f6-138"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="500f6-138"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="500f6-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="500f6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="500f6-140">**\_DomainResourceRecordContainment MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="500f6-140">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="500f6-141">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="500f6-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="500f6-142">**\_ServerDomainContainment MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="500f6-142">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





