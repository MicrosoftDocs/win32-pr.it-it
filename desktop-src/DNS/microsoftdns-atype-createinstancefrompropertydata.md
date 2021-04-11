---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_AType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse Address (A).
ms.assetid: 81d67eba-f2c6-49c0-af29-be3f3724a973
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_AType
- Classe MicrosoftDNS_AType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d8d3e5c9d0ad4302da2243a3ef9611e295c86e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119794"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="3a427-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ aType</span><span class="sxs-lookup"><span data-stu-id="3a427-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="3a427-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse Address (A).</span><span class="sxs-lookup"><span data-stu-id="3a427-107">The **CreateInstanceFromPropertyData** method instantiates an Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a427-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a427-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string             DnsServerName,
  [in]           string             ContainerName,
  [in]           string             OwnerName,
  [in, optional] uint32             RecordClass = 1,
  [in, optional] uint32             TTL,
  [in]           string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3a427-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a427-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a427-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a427-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a427-111">Nome di dominio completo (FQDN) o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="3a427-111">Fully Qualified Domain Name (FQDN) or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="3a427-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a427-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a427-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="3a427-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="3a427-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a427-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a427-115">FQDN del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="3a427-115">Owner FQDN for the RR.</span></span>

> [!Note]  
> <span data-ttu-id="3a427-116">Non usare il nome NetBIOS del proprietario.</span><span class="sxs-lookup"><span data-stu-id="3a427-116">Do not use the owner NetBIOS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="3a427-117">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3a427-117">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a427-118">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="3a427-118">Class of the RR.</span></span> <span data-ttu-id="3a427-119">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="3a427-119">Default value is 1.</span></span> <span data-ttu-id="3a427-120">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="3a427-120">The following values are valid.</span></span>



| <span data-ttu-id="3a427-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3a427-121">Value</span></span>                                                                                                | <span data-ttu-id="3a427-122">Significato</span><span class="sxs-lookup"><span data-stu-id="3a427-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="3a427-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="3a427-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="3a427-124">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="3a427-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="3a427-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3a427-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="3a427-126">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="3a427-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="3a427-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="3a427-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="3a427-128">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="3a427-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="3a427-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="3a427-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="3a427-130">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="3a427-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="3a427-131">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3a427-131">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a427-132">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="3a427-132">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3a427-133">*Indirizzo IP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a427-133">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a427-134">Stringa che rappresenta l'indirizzo IP dell'host.</span><span class="sxs-lookup"><span data-stu-id="3a427-134">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="3a427-135">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="3a427-135">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3a427-136">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="3a427-136">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a427-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a427-137">Return value</span></span>

<span data-ttu-id="3a427-138">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3a427-138">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a427-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a427-139">Requirements</span></span>



| <span data-ttu-id="3a427-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a427-140">Requirement</span></span> | <span data-ttu-id="3a427-141">Valore</span><span class="sxs-lookup"><span data-stu-id="3a427-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a427-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a427-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3a427-143">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3a427-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3a427-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a427-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3a427-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a427-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3a427-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3a427-146">Namespace</span></span><br/>                | <span data-ttu-id="3a427-147">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="3a427-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3a427-148">MOF</span><span class="sxs-lookup"><span data-stu-id="3a427-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a427-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a427-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a427-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a427-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a427-151">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3a427-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="3a427-152">**Metodo Modify della \_ classe aType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3a427-152">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





