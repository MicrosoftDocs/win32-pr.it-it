---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_NXTType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse successivo (NXT).
ms.assetid: d0e4f3bf-f835-4341-a614-539975e6be11
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_NXTType
- Classe MicrosoftDNS_NXTType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee00cd0afdb6ac629a981dbdb586a30252eac1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477524"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="917e3-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ NXTType</span><span class="sxs-lookup"><span data-stu-id="917e3-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="917e3-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse successivo (NXT).</span><span class="sxs-lookup"><span data-stu-id="917e3-107">The **CreateInstanceFromPropertyData** method instantiates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="917e3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="917e3-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="917e3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="917e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="917e3-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="917e3-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917e3-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="917e3-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="917e3-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="917e3-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917e3-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="917e3-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="917e3-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="917e3-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917e3-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="917e3-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="917e3-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="917e3-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="917e3-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="917e3-117">Class of the RR.</span></span> <span data-ttu-id="917e3-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="917e3-118">Default value is 1.</span></span> <span data-ttu-id="917e3-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="917e3-119">The following values are valid.</span></span>



| <span data-ttu-id="917e3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="917e3-120">Value</span></span>                                                                                                | <span data-ttu-id="917e3-121">Significato</span><span class="sxs-lookup"><span data-stu-id="917e3-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="917e3-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="917e3-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="917e3-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="917e3-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="917e3-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="917e3-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="917e3-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="917e3-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="917e3-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="917e3-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="917e3-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="917e3-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="917e3-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="917e3-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="917e3-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="917e3-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="917e3-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="917e3-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="917e3-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="917e3-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="917e3-132">*NextDomainName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="917e3-132">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917e3-133">Nome di dominio successivo.</span><span class="sxs-lookup"><span data-stu-id="917e3-133">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="917e3-134">*Tipi* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="917e3-134">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917e3-135">Elenco separato da spazi dei tasti di scelta del tipo RR per il nome del proprietario del record di risorse NXT.</span><span class="sxs-lookup"><span data-stu-id="917e3-135">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="917e3-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="917e3-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="917e3-137">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="917e3-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="917e3-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="917e3-138">Return value</span></span>

<span data-ttu-id="917e3-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="917e3-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="917e3-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="917e3-140">Requirements</span></span>



| <span data-ttu-id="917e3-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="917e3-141">Requirement</span></span> | <span data-ttu-id="917e3-142">Valore</span><span class="sxs-lookup"><span data-stu-id="917e3-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="917e3-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="917e3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="917e3-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="917e3-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="917e3-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="917e3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="917e3-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="917e3-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="917e3-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="917e3-147">Namespace</span></span><br/>                | <span data-ttu-id="917e3-148">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="917e3-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="917e3-149">MOF</span><span class="sxs-lookup"><span data-stu-id="917e3-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="917e3-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="917e3-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="917e3-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="917e3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917e3-152">**\_NXTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="917e3-152">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="917e3-153">**Metodo Modify della \_ classe NXTType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="917e3-153">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="917e3-154">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="917e3-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





