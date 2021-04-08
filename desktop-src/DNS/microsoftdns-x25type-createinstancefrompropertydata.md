---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_X25Type
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse X. 25 (x25).
ms.assetid: fe89f829-79b9-457e-b455-899b2706ef04
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_X25Type
- Classe MicrosoftDNS_X25Type DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f198bf7b843b5633acd0b1515e9e3573f5ebb55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048511"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_x25type-class"></a><span data-ttu-id="e9e81-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ X25Type</span><span class="sxs-lookup"><span data-stu-id="e9e81-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="e9e81-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse X. 25 (x25).</span><span class="sxs-lookup"><span data-stu-id="e9e81-107">The **CreateInstanceFromPropertyData** method instantiates an X.25 (X25) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9e81-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9e81-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e9e81-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9e81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9e81-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9e81-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e81-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="e9e81-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="e9e81-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9e81-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e81-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="e9e81-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="e9e81-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9e81-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e81-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="e9e81-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="e9e81-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e9e81-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e81-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="e9e81-117">Class of the RR.</span></span> <span data-ttu-id="e9e81-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="e9e81-118">Default value is 1.</span></span> <span data-ttu-id="e9e81-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="e9e81-119">The following values are valid.</span></span>



| <span data-ttu-id="e9e81-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e81-120">Value</span></span>                                                                                                | <span data-ttu-id="e9e81-121">Significato</span><span class="sxs-lookup"><span data-stu-id="e9e81-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="e9e81-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e81-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="e9e81-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="e9e81-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="e9e81-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e81-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="e9e81-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="e9e81-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="e9e81-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e81-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="e9e81-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="e9e81-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="e9e81-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e81-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="e9e81-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="e9e81-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="e9e81-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e9e81-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e81-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="e9e81-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e9e81-132">*PSDNAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9e81-132">*PSDNAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e81-133">Indirizzo PSDN del proprietario dell'RR.</span><span class="sxs-lookup"><span data-stu-id="e9e81-133">PSDN address of the owner of the RR.</span></span>

</dd> <dt>

<span data-ttu-id="e9e81-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e9e81-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e81-135">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9e81-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9e81-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9e81-136">Return value</span></span>

<span data-ttu-id="e9e81-137">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e9e81-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9e81-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9e81-138">Requirements</span></span>



| <span data-ttu-id="e9e81-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9e81-139">Requirement</span></span> | <span data-ttu-id="e9e81-140">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e81-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9e81-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9e81-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e9e81-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e9e81-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e9e81-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9e81-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e9e81-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9e81-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e9e81-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e9e81-145">Namespace</span></span><br/>                | <span data-ttu-id="e9e81-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="e9e81-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e9e81-147">MOF</span><span class="sxs-lookup"><span data-stu-id="e9e81-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9e81-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9e81-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9e81-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9e81-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e81-150">**\_X25Type MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e9e81-150">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)
</dt> <dt>

[<span data-ttu-id="e9e81-151">**Metodo Modify della \_ classe X25Type di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e9e81-151">**Modify Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-modify.md)
</dt> <dt>

[<span data-ttu-id="e9e81-152">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e9e81-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





