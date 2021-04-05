---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_MRType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse di ridenominazione delle cassette postali.
ms.assetid: 7dab86e0-bf05-4e98-b1f8-e1daecd4425c
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_MRType
- Classe MicrosoftDNS_MRType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f41478d4ff59ff7999f6f3b052f203aeda78803
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873853"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="cd933-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MRType</span><span class="sxs-lookup"><span data-stu-id="cd933-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="cd933-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse di ridenominazione delle cassette postali.</span><span class="sxs-lookup"><span data-stu-id="cd933-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd933-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd933-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="cd933-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd933-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd933-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd933-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd933-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="cd933-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="cd933-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd933-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd933-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="cd933-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="cd933-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd933-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd933-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="cd933-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="cd933-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="cd933-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd933-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="cd933-117">Class of the RR.</span></span> <span data-ttu-id="cd933-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="cd933-118">Default value is 1.</span></span> <span data-ttu-id="cd933-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="cd933-119">The following values are valid.</span></span>



| <span data-ttu-id="cd933-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cd933-120">Value</span></span>                                                                                                | <span data-ttu-id="cd933-121">Significato</span><span class="sxs-lookup"><span data-stu-id="cd933-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="cd933-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="cd933-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="cd933-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="cd933-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="cd933-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="cd933-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="cd933-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="cd933-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="cd933-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="cd933-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="cd933-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="cd933-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="cd933-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="cd933-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="cd933-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="cd933-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="cd933-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="cd933-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd933-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="cd933-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="cd933-132">*MRMailbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd933-132">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd933-133">FQDN che specifica una cassetta postale che è la ridenominazione corretta della cassetta postale specificata nel nome del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="cd933-133">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="cd933-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="cd933-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cd933-135">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd933-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd933-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd933-136">Return value</span></span>

<span data-ttu-id="cd933-137">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cd933-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd933-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd933-138">Requirements</span></span>



| <span data-ttu-id="cd933-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd933-139">Requirement</span></span> | <span data-ttu-id="cd933-140">Valore</span><span class="sxs-lookup"><span data-stu-id="cd933-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd933-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd933-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cd933-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cd933-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cd933-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd933-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cd933-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd933-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cd933-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd933-145">Namespace</span></span><br/>                | <span data-ttu-id="cd933-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="cd933-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cd933-147">MOF</span><span class="sxs-lookup"><span data-stu-id="cd933-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd933-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd933-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd933-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd933-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd933-150">**\_MRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cd933-150">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="cd933-151">**Metodo Modify della \_ classe MRType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cd933-151">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="cd933-152">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cd933-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





