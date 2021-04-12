---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_RTType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di una route tramite un record di risorse (RT).
ms.assetid: 1ebb0543-d031-4430-acbe-708c4931b7a4
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_RTType
- Classe MicrosoftDNS_RTType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c3b8d71c41fefa9b78aa9a469ee1426c553e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517943"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="9ac23-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ RTType</span><span class="sxs-lookup"><span data-stu-id="9ac23-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="9ac23-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di una route tramite un record di risorse (RT).</span><span class="sxs-lookup"><span data-stu-id="9ac23-107">The **CreateInstanceFromPropertyData** method instantiates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ac23-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ac23-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9ac23-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ac23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ac23-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac23-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="9ac23-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9ac23-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac23-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="9ac23-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9ac23-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac23-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="9ac23-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="9ac23-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac23-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="9ac23-117">Class of the RR.</span></span> <span data-ttu-id="9ac23-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="9ac23-118">Default value is 1.</span></span> <span data-ttu-id="9ac23-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="9ac23-119">The following values are valid.</span></span>



| <span data-ttu-id="9ac23-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9ac23-120">Value</span></span>                                                                                                | <span data-ttu-id="9ac23-121">Significato</span><span class="sxs-lookup"><span data-stu-id="9ac23-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="9ac23-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9ac23-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9ac23-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="9ac23-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="9ac23-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9ac23-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9ac23-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="9ac23-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="9ac23-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="9ac23-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="9ac23-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="9ac23-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="9ac23-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="9ac23-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="9ac23-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="9ac23-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="9ac23-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac23-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="9ac23-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="9ac23-132">*Preferenza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac23-133">Preferenza assegnata a questo RR tra gli altri nello stesso proprietario.</span><span class="sxs-lookup"><span data-stu-id="9ac23-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="9ac23-134">Sono preferibili valori inferiori.</span><span class="sxs-lookup"><span data-stu-id="9ac23-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="9ac23-135">*IntermediateHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-135">*IntermediateHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac23-136">FQDN che specifica un host che funge da intermediario per raggiungere l'host specificato dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="9ac23-136">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="9ac23-137">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac23-138">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="9ac23-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ac23-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ac23-139">Return value</span></span>

<span data-ttu-id="9ac23-140">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9ac23-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ac23-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ac23-141">Requirements</span></span>



| <span data-ttu-id="9ac23-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ac23-142">Requirement</span></span> | <span data-ttu-id="9ac23-143">Valore</span><span class="sxs-lookup"><span data-stu-id="9ac23-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac23-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ac23-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9ac23-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9ac23-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9ac23-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ac23-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9ac23-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9ac23-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9ac23-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9ac23-148">Namespace</span></span><br/>                | <span data-ttu-id="9ac23-149">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="9ac23-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9ac23-150">MOF</span><span class="sxs-lookup"><span data-stu-id="9ac23-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ac23-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ac23-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ac23-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ac23-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ac23-153">**\_RTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9ac23-153">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="9ac23-154">**Metodo Modify della \_ classe RTType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9ac23-154">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="9ac23-155">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9ac23-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





