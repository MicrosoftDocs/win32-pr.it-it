---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_CNAMEType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse di nome canonico (CNAME).
ms.assetid: b5a5e14a-fb30-4cdf-90d0-7ef446350ac6
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_CNAMEType
- Classe MicrosoftDNS_CNAMEType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceb65a76002651e98dd8751e0a5c0c56aca3e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964224"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_cnametype-class"></a><span data-ttu-id="8c088-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ CNAMEType</span><span class="sxs-lookup"><span data-stu-id="8c088-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="8c088-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse di nome canonico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="8c088-107">The **CreateInstanceFromPropertyData** method instantiates a Canonical Name (CNAME) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c088-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c088-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8c088-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c088-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c088-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c088-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c088-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="8c088-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8c088-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c088-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c088-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="8c088-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8c088-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c088-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c088-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="8c088-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="8c088-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8c088-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c088-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="8c088-117">Class of the RR.</span></span> <span data-ttu-id="8c088-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="8c088-118">Default value is 1.</span></span> <span data-ttu-id="8c088-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="8c088-119">The following values are valid.</span></span>



| <span data-ttu-id="8c088-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8c088-120">Value</span></span>                                                                                                | <span data-ttu-id="8c088-121">Significato</span><span class="sxs-lookup"><span data-stu-id="8c088-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8c088-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8c088-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8c088-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="8c088-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="8c088-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8c088-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8c088-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="8c088-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="8c088-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8c088-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8c088-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="8c088-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="8c088-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="8c088-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8c088-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="8c088-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8c088-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8c088-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c088-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="8c088-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8c088-132">*PrimaryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c088-132">*PrimaryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c088-133">Nome primario del record CNAME CNAME.</span><span class="sxs-lookup"><span data-stu-id="8c088-133">Primary name of the CNAME RR.</span></span>

</dd> <dt>

<span data-ttu-id="8c088-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="8c088-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8c088-135">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="8c088-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c088-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c088-136">Return value</span></span>

<span data-ttu-id="8c088-137">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8c088-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c088-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c088-138">Requirements</span></span>



| <span data-ttu-id="8c088-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c088-139">Requirement</span></span> | <span data-ttu-id="8c088-140">Valore</span><span class="sxs-lookup"><span data-stu-id="8c088-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c088-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c088-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8c088-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8c088-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8c088-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c088-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8c088-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8c088-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8c088-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c088-145">Namespace</span></span><br/>                | <span data-ttu-id="8c088-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="8c088-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8c088-147">MOF</span><span class="sxs-lookup"><span data-stu-id="8c088-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c088-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c088-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c088-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c088-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c088-150">**\_CNAMEType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8c088-150">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md)
</dt> <dt>

[<span data-ttu-id="8c088-151">**Metodo Modify della \_ classe CNAMEType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8c088-151">**Modify Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-modify.md)
</dt> <dt>

[<span data-ttu-id="8c088-152">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8c088-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





