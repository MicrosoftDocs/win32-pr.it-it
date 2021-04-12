---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_RPType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse della persona responsabile (RP).
ms.assetid: 6d9366c3-fc82-4c1f-8fa3-c107f6a1ff74
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_RPType
- Classe MicrosoftDNS_RPType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c150a8a91a7a94fbea8492faea08b61d437a4c9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225213"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="8bb61-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ RPType</span><span class="sxs-lookup"><span data-stu-id="8bb61-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="8bb61-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse della persona responsabile (RP).</span><span class="sxs-lookup"><span data-stu-id="8bb61-107">The **CreateInstanceFromPropertyData** method instantiates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb61-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bb61-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              RPMailbox,
  [in]           string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8bb61-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bb61-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bb61-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bb61-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb61-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="8bb61-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8bb61-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bb61-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb61-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="8bb61-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8bb61-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bb61-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb61-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="8bb61-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="8bb61-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8bb61-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb61-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="8bb61-117">Class of the RR.</span></span> <span data-ttu-id="8bb61-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="8bb61-118">Default value is 1.</span></span> <span data-ttu-id="8bb61-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="8bb61-119">The following values are valid.</span></span>



| <span data-ttu-id="8bb61-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8bb61-120">Value</span></span>                                                                                                | <span data-ttu-id="8bb61-121">Significato</span><span class="sxs-lookup"><span data-stu-id="8bb61-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8bb61-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8bb61-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8bb61-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="8bb61-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="8bb61-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8bb61-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8bb61-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="8bb61-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="8bb61-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8bb61-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8bb61-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="8bb61-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="8bb61-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="8bb61-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8bb61-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="8bb61-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8bb61-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8bb61-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb61-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="8bb61-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8bb61-132">*RPMailbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bb61-132">*RPMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb61-133">FQDN che specifica la cassetta postale per la persona responsabile.</span><span class="sxs-lookup"><span data-stu-id="8bb61-133">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="8bb61-134">*TXTDomainName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bb61-134">*TXTDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb61-135">FQDN per cui sono presenti record di risorse TXT.</span><span class="sxs-lookup"><span data-stu-id="8bb61-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="8bb61-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="8bb61-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb61-137">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="8bb61-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bb61-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bb61-138">Return value</span></span>

<span data-ttu-id="8bb61-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8bb61-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb61-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bb61-140">Requirements</span></span>



| <span data-ttu-id="8bb61-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bb61-141">Requirement</span></span> | <span data-ttu-id="8bb61-142">Valore</span><span class="sxs-lookup"><span data-stu-id="8bb61-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb61-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bb61-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb61-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8bb61-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8bb61-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bb61-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb61-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8bb61-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8bb61-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8bb61-147">Namespace</span></span><br/>                | <span data-ttu-id="8bb61-148">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="8bb61-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8bb61-149">MOF</span><span class="sxs-lookup"><span data-stu-id="8bb61-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bb61-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bb61-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb61-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bb61-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb61-152">**\_RPType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8bb61-152">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="8bb61-153">**Metodo Modify della \_ classe RPType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8bb61-153">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="8bb61-154">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8bb61-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





