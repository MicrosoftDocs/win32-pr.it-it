---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_ISDNType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse ISDN.
ms.assetid: cd3b98e3-a804-473e-8831-5f045d43a54f
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_ISDNType
- Classe MicrosoftDNS_ISDNType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f6adaaf374cac56d7d29d04d83c8765b0080ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518256"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="8fda3-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ ISDNType</span><span class="sxs-lookup"><span data-stu-id="8fda3-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="8fda3-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse ISDN.</span><span class="sxs-lookup"><span data-stu-id="8fda3-107">The **CreateInstanceFromPropertyData** method instantiates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fda3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fda3-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                ISDNNumber,
  [in]           string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8fda3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fda3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fda3-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fda3-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fda3-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="8fda3-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8fda3-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fda3-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fda3-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="8fda3-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8fda3-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fda3-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fda3-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="8fda3-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="8fda3-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8fda3-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8fda3-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="8fda3-117">Class of the RR.</span></span> <span data-ttu-id="8fda3-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="8fda3-118">Default value is 1.</span></span> <span data-ttu-id="8fda3-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="8fda3-119">The following values are valid.</span></span>



| <span data-ttu-id="8fda3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8fda3-120">Value</span></span>                                                                                                | <span data-ttu-id="8fda3-121">Significato</span><span class="sxs-lookup"><span data-stu-id="8fda3-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8fda3-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8fda3-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8fda3-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="8fda3-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="8fda3-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8fda3-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8fda3-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="8fda3-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="8fda3-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8fda3-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8fda3-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="8fda3-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="8fda3-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="8fda3-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8fda3-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="8fda3-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8fda3-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8fda3-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8fda3-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="8fda3-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8fda3-132">*ISDNNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fda3-132">*ISDNNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fda3-133">Numero ISDN e DDI del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="8fda3-133">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="8fda3-134">*Sottoindirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fda3-134">*SubAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fda3-135">Sottoindirizzo del proprietario, se definito.</span><span class="sxs-lookup"><span data-stu-id="8fda3-135">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="8fda3-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="8fda3-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8fda3-137">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="8fda3-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fda3-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fda3-138">Return value</span></span>

<span data-ttu-id="8fda3-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8fda3-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fda3-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fda3-140">Requirements</span></span>



| <span data-ttu-id="8fda3-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fda3-141">Requirement</span></span> | <span data-ttu-id="8fda3-142">Valore</span><span class="sxs-lookup"><span data-stu-id="8fda3-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fda3-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fda3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8fda3-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8fda3-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8fda3-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fda3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8fda3-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8fda3-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8fda3-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8fda3-147">Namespace</span></span><br/>                | <span data-ttu-id="8fda3-148">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="8fda3-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8fda3-149">MOF</span><span class="sxs-lookup"><span data-stu-id="8fda3-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fda3-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fda3-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fda3-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fda3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fda3-152">**\_ISDNType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8fda3-152">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="8fda3-153">**Metodo Modify della \_ classe ISDNType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8fda3-153">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="8fda3-154">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8fda3-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





