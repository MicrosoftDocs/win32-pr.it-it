---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_NSType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse del server dei nomi (NS).
ms.assetid: f2399a9d-840d-4392-86c4-610894e60f8e
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_NSType
- Classe MicrosoftDNS_NSType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37b21323da53c592375a00be9303c321d270f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517776"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nstype-class"></a><span data-ttu-id="7b848-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ NSType</span><span class="sxs-lookup"><span data-stu-id="7b848-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_NSType class</span></span>

<span data-ttu-id="7b848-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse del server dei nomi (NS).</span><span class="sxs-lookup"><span data-stu-id="7b848-107">The **CreateInstanceFromPropertyData** method instantiates a Name Server (NS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b848-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b848-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              NSHost,
  [out, ref]     MicrosoftDNS_NSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="7b848-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b848-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b848-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b848-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b848-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="7b848-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="7b848-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b848-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b848-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="7b848-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="7b848-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b848-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b848-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="7b848-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="7b848-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7b848-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7b848-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="7b848-117">Class of the RR.</span></span> <span data-ttu-id="7b848-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="7b848-118">Default value is 1.</span></span> <span data-ttu-id="7b848-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="7b848-119">The following values are valid.</span></span>



| <span data-ttu-id="7b848-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7b848-120">Value</span></span>                                                                                                | <span data-ttu-id="7b848-121">Significato</span><span class="sxs-lookup"><span data-stu-id="7b848-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="7b848-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="7b848-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="7b848-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="7b848-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="7b848-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="7b848-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="7b848-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="7b848-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="7b848-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="7b848-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="7b848-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="7b848-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="7b848-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="7b848-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="7b848-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="7b848-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="7b848-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7b848-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7b848-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="7b848-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="7b848-132">*NSHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b848-132">*NSHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b848-133">Host autorevole per il dominio.</span><span class="sxs-lookup"><span data-stu-id="7b848-133">Authoritative host for the domain.</span></span>

</dd> <dt>

<span data-ttu-id="7b848-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="7b848-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7b848-135">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b848-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b848-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b848-136">Return value</span></span>

<span data-ttu-id="7b848-137">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7b848-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b848-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b848-138">Requirements</span></span>



| <span data-ttu-id="7b848-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b848-139">Requirement</span></span> | <span data-ttu-id="7b848-140">Valore</span><span class="sxs-lookup"><span data-stu-id="7b848-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b848-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b848-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7b848-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7b848-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7b848-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b848-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7b848-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7b848-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7b848-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b848-145">Namespace</span></span><br/>                | <span data-ttu-id="7b848-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="7b848-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7b848-147">MOF</span><span class="sxs-lookup"><span data-stu-id="7b848-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b848-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b848-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b848-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b848-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b848-150">**\_NSType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7b848-150">**MicrosoftDNS\_NSType**</span></span>](microsoftdns-nstype.md)
</dt> <dt>

[<span data-ttu-id="7b848-151">**Metodo Modify della \_ classe NSType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7b848-151">**Modify Method of the MicrosoftDNS\_NSType Class**</span></span>](microsoftdns-nstype-modify.md)
</dt> <dt>

[<span data-ttu-id="7b848-152">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7b848-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





