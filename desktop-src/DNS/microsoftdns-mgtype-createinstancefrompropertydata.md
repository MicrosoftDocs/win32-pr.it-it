---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_MGType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse del gruppo di posta (MG).
ms.assetid: 98e2ecb3-bf2f-42db-8a8b-de10a29f5a5a
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_MGType
- Classe MicrosoftDNS_MGType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 313f6d14a10b1de9bc1d3b3b8042020ea5b0a522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120474"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="b78ae-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MGType</span><span class="sxs-lookup"><span data-stu-id="b78ae-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="b78ae-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse del gruppo di posta (mg).</span><span class="sxs-lookup"><span data-stu-id="b78ae-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b78ae-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b78ae-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="b78ae-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b78ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b78ae-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b78ae-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b78ae-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="b78ae-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="b78ae-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b78ae-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b78ae-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="b78ae-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="b78ae-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b78ae-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b78ae-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="b78ae-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="b78ae-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b78ae-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b78ae-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="b78ae-117">Class of the RR.</span></span> <span data-ttu-id="b78ae-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="b78ae-118">Default value is 1.</span></span> <span data-ttu-id="b78ae-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="b78ae-119">The following values are valid.</span></span>



| <span data-ttu-id="b78ae-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b78ae-120">Value</span></span>                                                                                                | <span data-ttu-id="b78ae-121">Significato</span><span class="sxs-lookup"><span data-stu-id="b78ae-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="b78ae-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b78ae-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="b78ae-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="b78ae-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="b78ae-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="b78ae-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="b78ae-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="b78ae-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="b78ae-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="b78ae-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="b78ae-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="b78ae-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="b78ae-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="b78ae-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="b78ae-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="b78ae-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="b78ae-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b78ae-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b78ae-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="b78ae-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="b78ae-132">*MGMailbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b78ae-132">*MGMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b78ae-133">FQDN che specifica una cassetta postale che è un membro del gruppo di posta elettronica specificato dal nome del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="b78ae-133">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="b78ae-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="b78ae-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b78ae-135">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="b78ae-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b78ae-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b78ae-136">Return value</span></span>

<span data-ttu-id="b78ae-137">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b78ae-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b78ae-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b78ae-138">Requirements</span></span>



| <span data-ttu-id="b78ae-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b78ae-139">Requirement</span></span> | <span data-ttu-id="b78ae-140">Valore</span><span class="sxs-lookup"><span data-stu-id="b78ae-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b78ae-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b78ae-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b78ae-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b78ae-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b78ae-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b78ae-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b78ae-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b78ae-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b78ae-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b78ae-145">Namespace</span></span><br/>                | <span data-ttu-id="b78ae-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="b78ae-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b78ae-147">MOF</span><span class="sxs-lookup"><span data-stu-id="b78ae-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b78ae-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b78ae-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b78ae-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b78ae-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78ae-150">**\_MGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="b78ae-150">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="b78ae-151">**Metodo Modify della \_ classe MGType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="b78ae-151">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="b78ae-152">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="b78ae-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





