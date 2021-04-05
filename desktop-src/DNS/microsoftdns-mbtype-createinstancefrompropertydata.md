---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_MBType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse della cassetta postale (MB).
ms.assetid: ac160a4d-2af7-428e-9cbd-bdd28f7c0910
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_MBType
- Classe MicrosoftDNS_MBType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e340d78057c12e58159a293468598da7dbf53e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874001"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="88f60-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MBType</span><span class="sxs-lookup"><span data-stu-id="88f60-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="88f60-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse della cassetta postale (MB).</span><span class="sxs-lookup"><span data-stu-id="88f60-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="88f60-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88f60-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]       string              DnsServerName,
  [in]       string              ContainerName,
  [in]       string              OwnerName,
  [in]       uint32              RecordClass = 1,
  [in]       uint32              TTL,
  [in]       string              MBHost,
  [out, ref] MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="88f60-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="88f60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88f60-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88f60-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88f60-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="88f60-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="88f60-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88f60-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88f60-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="88f60-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="88f60-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88f60-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88f60-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="88f60-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="88f60-116">*RecordClass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88f60-116">*RecordClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88f60-117">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="88f60-117">Optional.</span></span> <span data-ttu-id="88f60-118">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="88f60-118">Class of the RR.</span></span> <span data-ttu-id="88f60-119">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="88f60-119">Default value is 1.</span></span> <span data-ttu-id="88f60-120">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="88f60-120">The following values are valid.</span></span>



| <span data-ttu-id="88f60-121">Valore</span><span class="sxs-lookup"><span data-stu-id="88f60-121">Value</span></span>                                                                                                | <span data-ttu-id="88f60-122">Significato</span><span class="sxs-lookup"><span data-stu-id="88f60-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="88f60-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="88f60-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="88f60-124">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="88f60-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="88f60-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="88f60-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="88f60-126">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="88f60-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="88f60-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="88f60-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="88f60-128">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="88f60-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="88f60-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="88f60-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="88f60-130">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="88f60-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="88f60-131">Valore *TTL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88f60-131">*TTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88f60-132">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="88f60-132">Optional.</span></span> <span data-ttu-id="88f60-133">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="88f60-133">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="88f60-134">*MBHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88f60-134">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88f60-135">Nome host della cassetta postale per l'RR.</span><span class="sxs-lookup"><span data-stu-id="88f60-135">Mailbox host name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="88f60-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="88f60-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="88f60-137">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="88f60-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88f60-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88f60-138">Return value</span></span>

<span data-ttu-id="88f60-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="88f60-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="88f60-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88f60-140">Requirements</span></span>



| <span data-ttu-id="88f60-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="88f60-141">Requirement</span></span> | <span data-ttu-id="88f60-142">Valore</span><span class="sxs-lookup"><span data-stu-id="88f60-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88f60-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88f60-143">Minimum supported client</span></span><br/> | <span data-ttu-id="88f60-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="88f60-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="88f60-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88f60-145">Minimum supported server</span></span><br/> | <span data-ttu-id="88f60-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="88f60-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="88f60-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88f60-147">Namespace</span></span><br/>                | <span data-ttu-id="88f60-148">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="88f60-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="88f60-149">MOF</span><span class="sxs-lookup"><span data-stu-id="88f60-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88f60-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88f60-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88f60-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88f60-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f60-152">**\_MBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="88f60-152">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="88f60-153">**Metodo Modify della \_ classe MBType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="88f60-153">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="88f60-154">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="88f60-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





