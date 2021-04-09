---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_WINSRType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse di ricerca inversa WINS (WINSr).
ms.assetid: e14e81be-fc5c-4a6f-b6d1-cb3ce5005e00
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_WINSRType
- Classe MicrosoftDNS_WINSRType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c35863e00ace6c0772383604d0fbdfd7915cd02c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120471"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="faab2-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WINSRType</span><span class="sxs-lookup"><span data-stu-id="faab2-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="faab2-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse di ricerca inversa WINS (WINSR).</span><span class="sxs-lookup"><span data-stu-id="faab2-107">The **CreateInstanceFromPropertyData** method instantiates a WINS Reverse Lookup (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="faab2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="faab2-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint32                 MappingFlag,
  [in]           uint32                 LookupTimeout,
  [in]           uint32                 CacheTimeout,
  [in]           string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="faab2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="faab2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faab2-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faab2-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faab2-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="faab2-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="faab2-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faab2-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faab2-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="faab2-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="faab2-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faab2-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faab2-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="faab2-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="faab2-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="faab2-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="faab2-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="faab2-117">Class of the RR.</span></span> <span data-ttu-id="faab2-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="faab2-118">Default value is 1.</span></span> <span data-ttu-id="faab2-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="faab2-119">The following values are valid.</span></span>



| <span data-ttu-id="faab2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="faab2-120">Value</span></span>                                                                                                | <span data-ttu-id="faab2-121">Significato</span><span class="sxs-lookup"><span data-stu-id="faab2-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="faab2-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="faab2-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="faab2-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="faab2-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="faab2-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="faab2-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="faab2-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="faab2-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="faab2-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="faab2-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="faab2-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="faab2-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="faab2-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="faab2-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="faab2-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="faab2-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="faab2-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="faab2-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="faab2-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="faab2-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="faab2-132">*MappingFlag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faab2-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faab2-133">Flag di mapping WINSr che specifica se il record deve essere incluso nella replica della zona.</span><span class="sxs-lookup"><span data-stu-id="faab2-133">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="faab2-134">Potrebbero essere presenti solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale).</span><span class="sxs-lookup"><span data-stu-id="faab2-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="faab2-135">*LookupTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faab2-135">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faab2-136">Timeout, in secondi, per un server DNS che utilizza la ricerca inversa WINS.</span><span class="sxs-lookup"><span data-stu-id="faab2-136">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="faab2-137">*CacheTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faab2-137">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faab2-138">Tempo, in secondi, in cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.</span><span class="sxs-lookup"><span data-stu-id="faab2-138">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="faab2-139">*ResultDomain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faab2-139">*ResultDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faab2-140">Nome di dominio da aggiungere ai nomi NetBIOS restituiti.</span><span class="sxs-lookup"><span data-stu-id="faab2-140">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="faab2-141">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="faab2-141">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="faab2-142">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="faab2-142">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faab2-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="faab2-143">Return value</span></span>

<span data-ttu-id="faab2-144">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="faab2-144">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="faab2-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="faab2-145">Requirements</span></span>



| <span data-ttu-id="faab2-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="faab2-146">Requirement</span></span> | <span data-ttu-id="faab2-147">Valore</span><span class="sxs-lookup"><span data-stu-id="faab2-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="faab2-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="faab2-148">Minimum supported client</span></span><br/> | <span data-ttu-id="faab2-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="faab2-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="faab2-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="faab2-150">Minimum supported server</span></span><br/> | <span data-ttu-id="faab2-151">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="faab2-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="faab2-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="faab2-152">Namespace</span></span><br/>                | <span data-ttu-id="faab2-153">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="faab2-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="faab2-154">MOF</span><span class="sxs-lookup"><span data-stu-id="faab2-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faab2-155"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="faab2-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faab2-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="faab2-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faab2-157">**\_WINSRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faab2-157">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="faab2-158">**Metodo Modify della \_ classe WINSRType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faab2-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="faab2-159">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faab2-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





