---
title: Classe MicrosoftDNS_Statistic
description: La \_ classe statistica MicrosoftDNS rappresenta una singola statistica del server DNS.
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- DNS della classe MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e26f1738c046e446fa898c4fdff2f6e8855730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048640"
---
# <a name="microsoftdns_statistic-class"></a><span data-ttu-id="b5434-105">\_Classe statistica MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="b5434-105">MicrosoftDNS\_Statistic class</span></span>

<span data-ttu-id="b5434-106">La **classe \_ statistica MicrosoftDNS** rappresenta una singola statistica del server DNS.</span><span class="sxs-lookup"><span data-stu-id="b5434-106">The **MicrosoftDNS\_Statistic** class represents a single DNS Server statistic.</span></span>

<span data-ttu-id="b5434-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="b5434-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5434-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5434-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a><span data-ttu-id="b5434-109">Members</span><span class="sxs-lookup"><span data-stu-id="b5434-109">Members</span></span>

<span data-ttu-id="b5434-110">La **classe \_ statistica MicrosoftDNS** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b5434-110">The **MicrosoftDNS\_Statistic** class has these types of members:</span></span>

-   [<span data-ttu-id="b5434-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b5434-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5434-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b5434-112">Properties</span></span>

<span data-ttu-id="b5434-113">La **classe \_ statistica MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b5434-113">The **MicrosoftDNS\_Statistic** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5434-114">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="b5434-114">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5434-115">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5434-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5434-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5434-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5434-117">Rappresentazione numerica di **CollectionName**.</span><span class="sxs-lookup"><span data-stu-id="b5434-117">Numeric representation of **CollectionName**.</span></span>

</dd> <dt>

<span data-ttu-id="b5434-118">**CollectionName**</span><span class="sxs-lookup"><span data-stu-id="b5434-118">**CollectionName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5434-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5434-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5434-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5434-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5434-121">Nome della raccolta a cui appartiene la statistica.</span><span class="sxs-lookup"><span data-stu-id="b5434-121">Name of the collection to which the statistic belongs.</span></span>

</dd> <dt>

<span data-ttu-id="b5434-122">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="b5434-122">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5434-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5434-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5434-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5434-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5434-125">Indica il nome di dominio completo o l'indirizzo IP del server DNS che contiene la statistica.</span><span class="sxs-lookup"><span data-stu-id="b5434-125">Indicates the FQDN or IP address of the DNS Server that contains the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="b5434-126">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b5434-126">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5434-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5434-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5434-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5434-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5434-129">Nome della statistica.</span><span class="sxs-lookup"><span data-stu-id="b5434-129">Name of the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="b5434-130">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="b5434-130">**StringValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5434-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5434-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5434-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5434-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5434-133">Valore stringa della statistica, utilizzato solo quando il valore statistico non è rappresentato come DWORD.</span><span class="sxs-lookup"><span data-stu-id="b5434-133">String value of the statistic, used only when the statistic value is not represented as a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="b5434-134">**Valore**</span><span class="sxs-lookup"><span data-stu-id="b5434-134">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5434-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5434-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5434-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5434-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5434-137">Valore numerico della statistica, rappresentato come DWORD.</span><span class="sxs-lookup"><span data-stu-id="b5434-137">Numeric value of the statistic, represented as a DWORD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5434-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5434-138">Requirements</span></span>



| <span data-ttu-id="b5434-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5434-139">Requirement</span></span> | <span data-ttu-id="b5434-140">Valore</span><span class="sxs-lookup"><span data-stu-id="b5434-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5434-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5434-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b5434-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b5434-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b5434-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5434-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b5434-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5434-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b5434-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b5434-145">Namespace</span></span><br/>                | <span data-ttu-id="b5434-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="b5434-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b5434-147">MOF</span><span class="sxs-lookup"><span data-stu-id="b5434-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5434-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5434-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5434-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5434-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5434-150">MicrosoftDNS \_ StatisticCollection</span><span class="sxs-lookup"><span data-stu-id="b5434-150">MicrosoftDNS\_StatisticCollection</span></span>](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





