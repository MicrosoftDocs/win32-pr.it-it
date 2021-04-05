---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_WKSType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse di Well-Known Services (WKS).
ms.assetid: 6d910716-74f9-48a0-b43c-3243f5518caf
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_WKSType
- Classe MicrosoftDNS_WKSType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e27b62bd2008c58d283d0e7564fa7821c452cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874090"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="d9f77-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WKSType</span><span class="sxs-lookup"><span data-stu-id="d9f77-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="d9f77-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse di Well-Known Services (WKS).</span><span class="sxs-lookup"><span data-stu-id="d9f77-107">The **CreateInstanceFromPropertyData** method instantiates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f77-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9f77-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               InternetAddress,
  [in]           string               IPProtocol,
  [in]           string               Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d9f77-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9f77-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9f77-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9f77-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9f77-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="d9f77-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d9f77-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9f77-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9f77-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="d9f77-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d9f77-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9f77-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9f77-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="d9f77-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="d9f77-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="d9f77-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d9f77-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="d9f77-117">Class of the RR.</span></span> <span data-ttu-id="d9f77-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="d9f77-118">Default value is 1.</span></span> <span data-ttu-id="d9f77-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="d9f77-119">The following values are valid.</span></span>



| <span data-ttu-id="d9f77-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d9f77-120">Value</span></span>                                                                                                | <span data-ttu-id="d9f77-121">Significato</span><span class="sxs-lookup"><span data-stu-id="d9f77-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="d9f77-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d9f77-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d9f77-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="d9f77-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="d9f77-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d9f77-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d9f77-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="d9f77-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="d9f77-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="d9f77-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="d9f77-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="d9f77-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="d9f77-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="d9f77-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="d9f77-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="d9f77-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="d9f77-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="d9f77-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d9f77-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="d9f77-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d9f77-132">*InternetAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9f77-132">*InternetAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9f77-133">Indirizzo IP Internet per il proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="d9f77-133">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="d9f77-134">*IPProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9f77-134">*IPProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9f77-135">Stringa che rappresenta il protocollo IP per questo record.</span><span class="sxs-lookup"><span data-stu-id="d9f77-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="d9f77-136">I valori validi sono UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="d9f77-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="d9f77-137">*Servizi* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d9f77-137">*Services* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9f77-138">Stringa contenente tutti i servizi utilizzati dal record del servizio noto (WKS).</span><span class="sxs-lookup"><span data-stu-id="d9f77-138">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="d9f77-139">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="d9f77-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d9f77-140">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d9f77-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9f77-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9f77-141">Return value</span></span>

<span data-ttu-id="d9f77-142">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d9f77-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f77-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9f77-143">Requirements</span></span>



| <span data-ttu-id="d9f77-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9f77-144">Requirement</span></span> | <span data-ttu-id="d9f77-145">Valore</span><span class="sxs-lookup"><span data-stu-id="d9f77-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f77-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9f77-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d9f77-147">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d9f77-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d9f77-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9f77-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d9f77-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d9f77-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d9f77-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d9f77-150">Namespace</span></span><br/>                | <span data-ttu-id="d9f77-151">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="d9f77-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d9f77-152">MOF</span><span class="sxs-lookup"><span data-stu-id="d9f77-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9f77-153"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9f77-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f77-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9f77-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f77-155">**\_WKSType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d9f77-155">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="d9f77-156">**Metodo Modify della \_ classe WKSType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d9f77-156">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="d9f77-157">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d9f77-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





