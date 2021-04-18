---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_TXTType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse di testo (TXT).
ms.assetid: f518bb07-e64f-4240-a7b8-9363374b83d6
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_TXTType
- Classe MicrosoftDNS_TXTType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23f9790189ca182cd65d9fe34890c31a90921d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302278"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="03ba6-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ TXTType</span><span class="sxs-lookup"><span data-stu-id="03ba6-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="03ba6-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse di testo (txt).</span><span class="sxs-lookup"><span data-stu-id="03ba6-107">The **CreateInstanceFromPropertyData** method instantiates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ba6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03ba6-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="03ba6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="03ba6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ba6-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03ba6-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ba6-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="03ba6-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="03ba6-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03ba6-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ba6-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="03ba6-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="03ba6-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03ba6-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ba6-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="03ba6-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="03ba6-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="03ba6-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03ba6-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="03ba6-117">Class of the RR.</span></span> <span data-ttu-id="03ba6-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="03ba6-118">Default value is 1.</span></span> <span data-ttu-id="03ba6-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="03ba6-119">The following values are valid.</span></span>



| <span data-ttu-id="03ba6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="03ba6-120">Value</span></span>                                                                                                | <span data-ttu-id="03ba6-121">Significato</span><span class="sxs-lookup"><span data-stu-id="03ba6-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="03ba6-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="03ba6-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="03ba6-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="03ba6-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="03ba6-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="03ba6-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="03ba6-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="03ba6-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="03ba6-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="03ba6-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="03ba6-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="03ba6-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="03ba6-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="03ba6-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="03ba6-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="03ba6-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="03ba6-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="03ba6-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03ba6-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="03ba6-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="03ba6-132">*DescriptiveText* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03ba6-132">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ba6-133">Testo descrittivo, la semantica di che dipende dal dominio proprietario.</span><span class="sxs-lookup"><span data-stu-id="03ba6-133">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="03ba6-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="03ba6-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="03ba6-135">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="03ba6-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ba6-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03ba6-136">Return value</span></span>

<span data-ttu-id="03ba6-137">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="03ba6-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03ba6-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03ba6-138">Requirements</span></span>



| <span data-ttu-id="03ba6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="03ba6-139">Requirement</span></span> | <span data-ttu-id="03ba6-140">Valore</span><span class="sxs-lookup"><span data-stu-id="03ba6-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03ba6-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03ba6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="03ba6-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="03ba6-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="03ba6-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03ba6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="03ba6-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="03ba6-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="03ba6-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03ba6-145">Namespace</span></span><br/>                | <span data-ttu-id="03ba6-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="03ba6-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="03ba6-147">MOF</span><span class="sxs-lookup"><span data-stu-id="03ba6-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03ba6-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03ba6-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03ba6-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03ba6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ba6-150">**\_TXTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="03ba6-150">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="03ba6-151">**Metodo Modify della \_ classe TXTType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="03ba6-151">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="03ba6-152">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="03ba6-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





