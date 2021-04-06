---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_HINFOType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse di informazioni host (HINFO).
ms.assetid: dfc11ae8-5013-4b48-a1e9-78566dc32297
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_HINFOType
- Classe MicrosoftDNS_HINFOType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2c8386a9c66ec94436fe4ae4c886ec62ff5b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743159"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="54134-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ HINFOType</span><span class="sxs-lookup"><span data-stu-id="54134-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="54134-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse di informazioni host (HINFO).</span><span class="sxs-lookup"><span data-stu-id="54134-107">The **CreateInstanceFromPropertyData** method instantiates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="54134-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54134-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="54134-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="54134-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54134-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54134-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54134-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="54134-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="54134-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54134-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54134-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="54134-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="54134-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54134-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54134-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="54134-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="54134-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="54134-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="54134-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="54134-117">Class of the RR.</span></span> <span data-ttu-id="54134-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="54134-118">Default value is 1.</span></span> <span data-ttu-id="54134-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="54134-119">The following values are valid.</span></span>



| <span data-ttu-id="54134-120">Valore</span><span class="sxs-lookup"><span data-stu-id="54134-120">Value</span></span>                                                                                                | <span data-ttu-id="54134-121">Significato</span><span class="sxs-lookup"><span data-stu-id="54134-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="54134-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="54134-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="54134-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="54134-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="54134-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="54134-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="54134-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="54134-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="54134-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="54134-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="54134-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="54134-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="54134-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="54134-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="54134-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="54134-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="54134-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="54134-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="54134-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="54134-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="54134-132">*CPU* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="54134-132">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="54134-133">Tipo di CPU del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="54134-133">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="54134-134">*Sistema operativo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="54134-134">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="54134-135">Sistema operativo del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="54134-135">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="54134-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="54134-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="54134-137">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="54134-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54134-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54134-138">Return value</span></span>

<span data-ttu-id="54134-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="54134-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="54134-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54134-140">Requirements</span></span>



| <span data-ttu-id="54134-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="54134-141">Requirement</span></span> | <span data-ttu-id="54134-142">Valore</span><span class="sxs-lookup"><span data-stu-id="54134-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54134-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54134-143">Minimum supported client</span></span><br/> | <span data-ttu-id="54134-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="54134-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="54134-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54134-145">Minimum supported server</span></span><br/> | <span data-ttu-id="54134-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54134-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="54134-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="54134-147">Namespace</span></span><br/>                | <span data-ttu-id="54134-148">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="54134-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="54134-149">MOF</span><span class="sxs-lookup"><span data-stu-id="54134-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54134-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54134-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54134-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54134-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54134-152">**\_HINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="54134-152">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="54134-153">**Metodo Modify della \_ classe HINFOType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="54134-153">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="54134-154">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="54134-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





