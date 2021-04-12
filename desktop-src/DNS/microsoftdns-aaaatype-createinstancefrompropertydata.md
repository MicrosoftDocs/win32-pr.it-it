---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_AAAAType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse di indirizzi IPv6 (AAAA).
ms.assetid: 3f2774d8-1eb6-4300-95e2-f918fc6612e0
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_AAAAType
- Classe MicrosoftDNS_AAAAType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9232506b52795521300e827701f685e351d8ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517782"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="35831-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ AAAAType</span><span class="sxs-lookup"><span data-stu-id="35831-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="35831-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse di indirizzi IPv6 (aaaa).</span><span class="sxs-lookup"><span data-stu-id="35831-107">The **CreateInstanceFromPropertyData** method instantiates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="35831-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35831-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="35831-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="35831-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35831-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35831-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35831-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="35831-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="35831-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35831-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35831-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="35831-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="35831-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35831-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35831-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="35831-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="35831-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="35831-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35831-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="35831-117">Class of the RR.</span></span> <span data-ttu-id="35831-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="35831-118">Default value is 1.</span></span> <span data-ttu-id="35831-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="35831-119">The following values are valid.</span></span>



| <span data-ttu-id="35831-120">Valore</span><span class="sxs-lookup"><span data-stu-id="35831-120">Value</span></span>                                                                                                | <span data-ttu-id="35831-121">Significato</span><span class="sxs-lookup"><span data-stu-id="35831-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="35831-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="35831-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="35831-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="35831-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="35831-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="35831-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="35831-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="35831-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="35831-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="35831-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="35831-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="35831-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="35831-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="35831-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="35831-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="35831-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="35831-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="35831-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35831-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="35831-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="35831-132">*IPV6Address* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35831-132">*IPv6Address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35831-133">Indirizzo IPv6 per l'host.</span><span class="sxs-lookup"><span data-stu-id="35831-133">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="35831-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="35831-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="35831-135">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="35831-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35831-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35831-136">Return value</span></span>

<span data-ttu-id="35831-137">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="35831-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="35831-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35831-138">Requirements</span></span>



| <span data-ttu-id="35831-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="35831-139">Requirement</span></span> | <span data-ttu-id="35831-140">Valore</span><span class="sxs-lookup"><span data-stu-id="35831-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35831-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35831-141">Minimum supported client</span></span><br/> | <span data-ttu-id="35831-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="35831-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="35831-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35831-143">Minimum supported server</span></span><br/> | <span data-ttu-id="35831-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="35831-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="35831-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35831-145">Namespace</span></span><br/>                | <span data-ttu-id="35831-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="35831-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="35831-147">MOF</span><span class="sxs-lookup"><span data-stu-id="35831-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35831-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35831-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35831-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35831-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35831-150">**\_AAAAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="35831-150">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="35831-151">**Metodo Modify della \_ classe AAAAType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="35831-151">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="35831-152">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="35831-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





