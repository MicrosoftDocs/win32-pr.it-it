---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_PTRType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse puntatore (PTR).
ms.assetid: ff8beaca-fa0d-4294-8dab-3aa62baa3fe3
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_PTRType
- Classe MicrosoftDNS_PTRType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6123b503fff1548b7fee3f643920b49ebacf636c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119714"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_ptrtype-class"></a><span data-ttu-id="c6ffe-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ PTRType</span><span class="sxs-lookup"><span data-stu-id="c6ffe-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="c6ffe-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="c6ffe-107">The **CreateInstanceFromPropertyData** method instantiates a Pointer (PTR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ffe-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6ffe-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c6ffe-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6ffe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6ffe-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6ffe-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6ffe-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c6ffe-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6ffe-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6ffe-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c6ffe-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6ffe-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6ffe-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="c6ffe-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c6ffe-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6ffe-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-117">Class of the RR.</span></span> <span data-ttu-id="c6ffe-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-118">Default value is 1.</span></span> <span data-ttu-id="c6ffe-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-119">The following values are valid.</span></span>



| <span data-ttu-id="c6ffe-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c6ffe-120">Value</span></span>                                                                                                | <span data-ttu-id="c6ffe-121">Significato</span><span class="sxs-lookup"><span data-stu-id="c6ffe-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c6ffe-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c6ffe-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c6ffe-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="c6ffe-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="c6ffe-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c6ffe-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c6ffe-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="c6ffe-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="c6ffe-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c6ffe-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c6ffe-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="c6ffe-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="c6ffe-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c6ffe-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c6ffe-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="c6ffe-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c6ffe-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c6ffe-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6ffe-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c6ffe-132">*PTRDomainName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6ffe-132">*PTRDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6ffe-133">Stringa che rappresenta l'indirizzo del nome di dominio del record PTR.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-133">String representing the domain name address of the PTR record.</span></span>

</dd> <dt>

<span data-ttu-id="c6ffe-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c6ffe-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c6ffe-135">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6ffe-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6ffe-136">Return value</span></span>

<span data-ttu-id="c6ffe-137">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c6ffe-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6ffe-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6ffe-138">Requirements</span></span>



| <span data-ttu-id="c6ffe-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6ffe-139">Requirement</span></span> | <span data-ttu-id="c6ffe-140">Valore</span><span class="sxs-lookup"><span data-stu-id="c6ffe-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ffe-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6ffe-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ffe-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c6ffe-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c6ffe-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6ffe-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ffe-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c6ffe-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c6ffe-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c6ffe-145">Namespace</span></span><br/>                | <span data-ttu-id="c6ffe-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="c6ffe-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c6ffe-147">MOF</span><span class="sxs-lookup"><span data-stu-id="c6ffe-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6ffe-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6ffe-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6ffe-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6ffe-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ffe-150">**\_PTRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-150">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="c6ffe-151">**Metodo Modify della \_ classe PTRType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-151">**Modify Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="c6ffe-152">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c6ffe-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





