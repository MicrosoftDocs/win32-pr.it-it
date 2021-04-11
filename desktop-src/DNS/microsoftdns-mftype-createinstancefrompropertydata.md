---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_MFType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse dell'agente di invio della posta elettronica per il dominio (MF).
ms.assetid: e669d065-bfba-4a86-8519-2317e03ed4ee
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_MFType
- Classe MicrosoftDNS_MFType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26cafc766a6ea6419432b279f5389721f6572b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964196"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="90345-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MFType</span><span class="sxs-lookup"><span data-stu-id="90345-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="90345-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse dell'agente di invio della posta elettronica per il dominio (MF).</span><span class="sxs-lookup"><span data-stu-id="90345-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="90345-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90345-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="90345-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="90345-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90345-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90345-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90345-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="90345-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="90345-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90345-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90345-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="90345-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="90345-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90345-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90345-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="90345-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="90345-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="90345-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90345-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="90345-117">Class of the RR.</span></span> <span data-ttu-id="90345-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="90345-118">Default value is 1.</span></span> <span data-ttu-id="90345-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="90345-119">The following values are valid.</span></span>



| <span data-ttu-id="90345-120">Valore</span><span class="sxs-lookup"><span data-stu-id="90345-120">Value</span></span>                                                                                                | <span data-ttu-id="90345-121">Significato</span><span class="sxs-lookup"><span data-stu-id="90345-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="90345-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="90345-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="90345-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="90345-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="90345-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="90345-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="90345-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="90345-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="90345-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="90345-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="90345-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="90345-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="90345-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="90345-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="90345-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="90345-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="90345-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="90345-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90345-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="90345-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="90345-132">*MFHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90345-132">*MFHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90345-133">Nome dell'host che fornisce l'agente di invio della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="90345-133">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="90345-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="90345-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="90345-135">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="90345-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90345-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90345-136">Return value</span></span>

<span data-ttu-id="90345-137">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="90345-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="90345-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90345-138">Requirements</span></span>



| <span data-ttu-id="90345-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="90345-139">Requirement</span></span> | <span data-ttu-id="90345-140">Valore</span><span class="sxs-lookup"><span data-stu-id="90345-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90345-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90345-141">Minimum supported client</span></span><br/> | <span data-ttu-id="90345-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="90345-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="90345-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90345-143">Minimum supported server</span></span><br/> | <span data-ttu-id="90345-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90345-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="90345-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="90345-145">Namespace</span></span><br/>                | <span data-ttu-id="90345-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="90345-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="90345-147">MOF</span><span class="sxs-lookup"><span data-stu-id="90345-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90345-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90345-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90345-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90345-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90345-150">**\_MFType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="90345-150">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="90345-151">**Metodo Modify della \_ classe MFType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="90345-151">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="90345-152">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="90345-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





