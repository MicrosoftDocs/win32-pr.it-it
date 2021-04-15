---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_MDType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un agente di posta elettronica per il record di risorse di dominio (MD).
ms.assetid: 23155a49-e2b3-4a69-8572-5dee61019d8f
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_MDType
- Classe MicrosoftDNS_MDType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b2e2cfdf3d2bb4b853a8e32716e51ca8e4c5b8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476601"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mdtype-class"></a><span data-ttu-id="76520-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MDType</span><span class="sxs-lookup"><span data-stu-id="76520-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="76520-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un agente di posta elettronica per il record di risorse di dominio (MD).</span><span class="sxs-lookup"><span data-stu-id="76520-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Agent for Domain (MD) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="76520-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76520-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="76520-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="76520-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76520-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76520-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76520-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="76520-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="76520-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76520-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76520-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="76520-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="76520-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76520-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76520-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="76520-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="76520-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="76520-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76520-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="76520-117">Class of the RR.</span></span> <span data-ttu-id="76520-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="76520-118">Default value is 1.</span></span> <span data-ttu-id="76520-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="76520-119">The following values are valid.</span></span>



| <span data-ttu-id="76520-120">Valore</span><span class="sxs-lookup"><span data-stu-id="76520-120">Value</span></span>                                                                                                | <span data-ttu-id="76520-121">Significato</span><span class="sxs-lookup"><span data-stu-id="76520-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="76520-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="76520-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="76520-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="76520-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="76520-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="76520-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="76520-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="76520-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="76520-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="76520-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="76520-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="76520-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="76520-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="76520-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="76520-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="76520-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="76520-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="76520-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76520-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="76520-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="76520-132">*MDHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76520-132">*MDHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76520-133">Nome host per il recapito della posta.</span><span class="sxs-lookup"><span data-stu-id="76520-133">Mail delivery host name.</span></span>

</dd> <dt>

<span data-ttu-id="76520-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="76520-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="76520-135">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="76520-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76520-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76520-136">Return value</span></span>

<span data-ttu-id="76520-137">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="76520-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="76520-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76520-138">Requirements</span></span>



| <span data-ttu-id="76520-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="76520-139">Requirement</span></span> | <span data-ttu-id="76520-140">Valore</span><span class="sxs-lookup"><span data-stu-id="76520-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76520-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76520-141">Minimum supported client</span></span><br/> | <span data-ttu-id="76520-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="76520-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="76520-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76520-143">Minimum supported server</span></span><br/> | <span data-ttu-id="76520-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="76520-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="76520-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="76520-145">Namespace</span></span><br/>                | <span data-ttu-id="76520-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="76520-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="76520-147">MOF</span><span class="sxs-lookup"><span data-stu-id="76520-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76520-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76520-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76520-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76520-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76520-150">**\_MDType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="76520-150">**MicrosoftDNS\_MDType**</span></span>](microsoftdns-mdtype.md)
</dt> <dt>

[<span data-ttu-id="76520-151">**Metodo Modify della \_ classe MDType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="76520-151">**Modify Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-modify.md)
</dt> <dt>

[<span data-ttu-id="76520-152">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="76520-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





