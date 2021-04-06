---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_SRVType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse del servizio (SRV).
ms.assetid: ef55faa8-1109-4c96-98ac-2b01b940fa5c
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_SRVType
- Classe MicrosoftDNS_SRVType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 607ed606bf12e9e2a6f90a6e7f309aa708b7f230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743383"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="3c063-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SRVType</span><span class="sxs-lookup"><span data-stu-id="3c063-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="3c063-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse del servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="3c063-107">The **CreateInstanceFromPropertyData** method instantiates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c063-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c063-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Priority,
  [in]           uint16               Weight,
  [in]           uint16               Port,
  [in]           string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3c063-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c063-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c063-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c063-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c063-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="3c063-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="3c063-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c063-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c063-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="3c063-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="3c063-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c063-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c063-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="3c063-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="3c063-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3c063-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c063-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="3c063-117">Class of the RR.</span></span> <span data-ttu-id="3c063-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="3c063-118">Default value is 1.</span></span> <span data-ttu-id="3c063-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="3c063-119">The following values are valid.</span></span>



| <span data-ttu-id="3c063-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3c063-120">Value</span></span>                                                                                                | <span data-ttu-id="3c063-121">Significato</span><span class="sxs-lookup"><span data-stu-id="3c063-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="3c063-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="3c063-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="3c063-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="3c063-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="3c063-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3c063-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="3c063-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="3c063-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="3c063-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="3c063-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="3c063-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="3c063-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="3c063-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="3c063-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="3c063-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="3c063-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="3c063-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3c063-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c063-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="3c063-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3c063-132">*Priorità* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3c063-132">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c063-133">Priorità dell'host di destinazione specificato nel nome del proprietario.</span><span class="sxs-lookup"><span data-stu-id="3c063-133">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="3c063-134">I numeri più bassi implicano priorità più elevate.</span><span class="sxs-lookup"><span data-stu-id="3c063-134">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="3c063-135">*Peso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c063-135">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c063-136">Peso dell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3c063-136">Weight of the target host.</span></span> <span data-ttu-id="3c063-137">Questa operazione è utile quando si seleziona tra gli host con la stessa priorità.</span><span class="sxs-lookup"><span data-stu-id="3c063-137">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="3c063-138">La possibilità di utilizzare questo host deve essere proporzionale al suo peso.</span><span class="sxs-lookup"><span data-stu-id="3c063-138">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="3c063-139">*Porta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c063-139">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c063-140">Porta utilizzata nell'host di destinazione di un servizio del protocollo.</span><span class="sxs-lookup"><span data-stu-id="3c063-140">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="3c063-141">*SRVDomainName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c063-141">*SRVDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c063-142">FQDN dell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3c063-142">FQDN of the target host.</span></span> <span data-ttu-id="3c063-143">Destinazione di \\ . \\ indica che il servizio non è disponibile in questo dominio.</span><span class="sxs-lookup"><span data-stu-id="3c063-143">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="3c063-144">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="3c063-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3c063-145">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="3c063-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c063-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c063-146">Return value</span></span>

<span data-ttu-id="3c063-147">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3c063-147">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c063-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c063-148">Requirements</span></span>



| <span data-ttu-id="3c063-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c063-149">Requirement</span></span> | <span data-ttu-id="3c063-150">Valore</span><span class="sxs-lookup"><span data-stu-id="3c063-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c063-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c063-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3c063-152">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3c063-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3c063-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c063-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3c063-154">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c063-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3c063-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3c063-155">Namespace</span></span><br/>                | <span data-ttu-id="3c063-156">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="3c063-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3c063-157">MOF</span><span class="sxs-lookup"><span data-stu-id="3c063-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c063-158"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c063-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c063-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c063-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c063-160">**\_SRVType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3c063-160">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="3c063-161">**Metodo Modify della \_ classe SRVType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3c063-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="3c063-162">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3c063-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





