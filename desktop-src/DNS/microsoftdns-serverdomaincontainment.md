---
title: Classe MicrosoftDNS_ServerDomainContainment
description: Ogni istanza della \_ classe WMI dell'associazione al server MicrosoftDNS può contenere più istanze della \_ classe di dominio MicrosoftDNS.
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- DNS della classe MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740266"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a><span data-ttu-id="19c93-105">\_Classe MicrosoftDNS ServerDomainContainment</span><span class="sxs-lookup"><span data-stu-id="19c93-105">MicrosoftDNS\_ServerDomainContainment class</span></span>

<span data-ttu-id="19c93-106">Ogni istanza della classe WMI dell'associazione al [**\_ Server MicrosoftDNS**](microsoftdns-server.md) può contenere più istanze della classe di [**\_ dominio MicrosoftDNS**](microsoftdns-domain.md) .</span><span class="sxs-lookup"><span data-stu-id="19c93-106">Every instance of the [**MicrosoftDNS\_Server**](microsoftdns-server.md) association WMI class may contain multiple instances of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class.</span></span> <span data-ttu-id="19c93-107">Ogni istanza della classe **di \_ dominio MicrosoftDNS** appartiene a una singola istanza della classe **\_ Server MicrosoftDNS** e viene definita debole per tale server.</span><span class="sxs-lookup"><span data-stu-id="19c93-107">Every instance of the **MicrosoftDNS\_Domain** class belongs to a single instance of the **MicrosoftDNS\_Server** class, and is defined to be weak to that server.</span></span>

<span data-ttu-id="19c93-108">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="19c93-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c93-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19c93-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="19c93-110">Members</span><span class="sxs-lookup"><span data-stu-id="19c93-110">Members</span></span>

<span data-ttu-id="19c93-111">La **classe \_ ServerDomainContainment di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="19c93-111">The **MicrosoftDNS\_ServerDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="19c93-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19c93-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19c93-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19c93-113">Properties</span></span>

<span data-ttu-id="19c93-114">La **classe \_ ServerDomainContainment di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="19c93-114">The **MicrosoftDNS\_ServerDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19c93-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="19c93-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19c93-116">Tipo di dati: **MicrosoftDNS \_ Server**</span><span class="sxs-lookup"><span data-stu-id="19c93-116">Data type: **MicrosoftDNS\_Server**</span></span>
</dt> <dt>

<span data-ttu-id="19c93-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19c93-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19c93-118">Qualificatori: chiave, override ("GroupComponent"), min (1), Max (1)</span><span class="sxs-lookup"><span data-stu-id="19c93-118">Qualifiers: Key, Override ("GroupComponent"), Min (1), Max (1)</span></span>

<span data-ttu-id="19c93-119">Descrizione: il server DNS.</span><span class="sxs-lookup"><span data-stu-id="19c93-119">Description: The DNS Server.</span></span>

<span data-ttu-id="19c93-120">Ereditato dal **\_ componente CIM**.</span><span class="sxs-lookup"><span data-stu-id="19c93-120">Inherited from **CIM\_Component**.</span></span>

</dd> <dt>

<span data-ttu-id="19c93-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="19c93-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19c93-122">Tipo di dati **: \_ dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="19c93-122">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="19c93-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19c93-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19c93-124">Qualificatori: chiave, override ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="19c93-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="19c93-125">Descrizione: dominio, zona, cache o RootHints gestito dal server DNS.</span><span class="sxs-lookup"><span data-stu-id="19c93-125">Description: A Domain, Zone, Cache, or RootHints managed by the DNS Server.</span></span>

<span data-ttu-id="19c93-126">Ereditato dal **\_ componente CIM**.</span><span class="sxs-lookup"><span data-stu-id="19c93-126">Inherited from **CIM\_Component**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19c93-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="19c93-127">Remarks</span></span>

<span data-ttu-id="19c93-128">La classe **MicrosoftDNS \_ ServerDomainContainment** è derivata dalla classe **del \_ componente CIM** .</span><span class="sxs-lookup"><span data-stu-id="19c93-128">The **MicrosoftDNS\_ServerDomainContainment** class is derived from the **CIM\_Component** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="19c93-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19c93-129">Requirements</span></span>



| <span data-ttu-id="19c93-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="19c93-130">Requirement</span></span> | <span data-ttu-id="19c93-131">Valore</span><span class="sxs-lookup"><span data-stu-id="19c93-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19c93-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19c93-132">Minimum supported client</span></span><br/> | <span data-ttu-id="19c93-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="19c93-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="19c93-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19c93-134">Minimum supported server</span></span><br/> | <span data-ttu-id="19c93-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="19c93-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="19c93-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="19c93-136">Namespace</span></span><br/>                | <span data-ttu-id="19c93-137">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="19c93-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="19c93-138">MOF</span><span class="sxs-lookup"><span data-stu-id="19c93-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19c93-139"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19c93-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19c93-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19c93-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c93-141">**\_DomainDomainContainment MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="19c93-141">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="19c93-142">**\_DomainResourceRecordContainment MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="19c93-142">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="19c93-143">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="19c93-143">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





