---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_WINSType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse WINS (Windows Internet Name Service).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_WINSType
- Classe MicrosoftDNS_WINSType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf584bd34f59391a49fd5f7ec13cb49e18ef68fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742247"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="c1d10-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WINSType</span><span class="sxs-lookup"><span data-stu-id="c1d10-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="c1d10-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse WINS (Windows Internet Name Service).</span><span class="sxs-lookup"><span data-stu-id="c1d10-107">The **CreateInstanceFromPropertyData** method instantiates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d10-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1d10-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c1d10-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1d10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1d10-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d10-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d10-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="c1d10-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c1d10-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d10-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d10-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="c1d10-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c1d10-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d10-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d10-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="c1d10-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="c1d10-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c1d10-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d10-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="c1d10-117">Class of the RR.</span></span> <span data-ttu-id="c1d10-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="c1d10-118">Default value is 1.</span></span> <span data-ttu-id="c1d10-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="c1d10-119">The following values are valid.</span></span>



| <span data-ttu-id="c1d10-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c1d10-120">Value</span></span>                                                                                                | <span data-ttu-id="c1d10-121">Significato</span><span class="sxs-lookup"><span data-stu-id="c1d10-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c1d10-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d10-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c1d10-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="c1d10-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="c1d10-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d10-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c1d10-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="c1d10-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="c1d10-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d10-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c1d10-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="c1d10-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="c1d10-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d10-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c1d10-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="c1d10-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c1d10-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c1d10-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d10-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="c1d10-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c1d10-132">*MappingFlag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d10-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d10-133">Flag di mapping WINS che specifica se il record deve essere incluso nella replica della zona.</span><span class="sxs-lookup"><span data-stu-id="c1d10-133">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="c1d10-134">Potrebbero essere presenti solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale).</span><span class="sxs-lookup"><span data-stu-id="c1d10-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="c1d10-135">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="c1d10-135">The following values are valid.</span></span>



| <span data-ttu-id="c1d10-136">Valore</span><span class="sxs-lookup"><span data-stu-id="c1d10-136">Value</span></span>                                                                                                                                               | <span data-ttu-id="c1d10-137">Significato</span><span class="sxs-lookup"><span data-stu-id="c1d10-137">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="c1d10-138"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d10-138"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="c1d10-139">Flag di replica</span><span class="sxs-lookup"><span data-stu-id="c1d10-139">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="c1d10-140"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d10-140"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="c1d10-141">Flag senza replica (record locale)</span><span class="sxs-lookup"><span data-stu-id="c1d10-141">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c1d10-142">*LookupTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d10-142">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d10-143">Tempo, in secondi, durante il quale un server DNS tenta la risoluzione usando la ricerca di WINS.</span><span class="sxs-lookup"><span data-stu-id="c1d10-143">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="c1d10-144">*CacheTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d10-144">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d10-145">Tempo, in secondi, per cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.</span><span class="sxs-lookup"><span data-stu-id="c1d10-145">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="c1d10-146">*WinsServers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d10-146">*WinsServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d10-147">Elenco di indirizzi IP delimitati da virgole dei server WINS utilizzati nelle ricerche WINS.</span><span class="sxs-lookup"><span data-stu-id="c1d10-147">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="c1d10-148">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c1d10-148">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d10-149">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c1d10-149">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1d10-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1d10-150">Return value</span></span>

<span data-ttu-id="c1d10-151">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c1d10-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d10-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1d10-152">Requirements</span></span>



| <span data-ttu-id="c1d10-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1d10-153">Requirement</span></span> | <span data-ttu-id="c1d10-154">Valore</span><span class="sxs-lookup"><span data-stu-id="c1d10-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d10-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1d10-155">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d10-156">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c1d10-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c1d10-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1d10-157">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d10-158">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1d10-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c1d10-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c1d10-159">Namespace</span></span><br/>                | <span data-ttu-id="c1d10-160">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="c1d10-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c1d10-161">MOF</span><span class="sxs-lookup"><span data-stu-id="c1d10-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1d10-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1d10-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1d10-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1d10-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d10-164">**\_WINSType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1d10-164">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="c1d10-165">**Metodo Modify della \_ classe WINSType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1d10-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="c1d10-166">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1d10-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





