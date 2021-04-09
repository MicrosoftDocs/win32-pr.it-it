---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_AFSDBType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse del server di database di file System Andrew (AFSDB).
ms.assetid: 2cd0434d-0c18-468f-95f3-7a77375596a3
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_AFSDBType
- Classe MicrosoftDNS_AFSDBType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04efd6e18ef4267d9887252f91e8a215fcf3ee88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964230"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="26671-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ AFSDBType</span><span class="sxs-lookup"><span data-stu-id="26671-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="26671-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse del server di database di file System Andrew (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="26671-107">The **CreateInstanceFromPropertyData** method instantiates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="26671-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26671-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint16                 Subtype,
  [in]           string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="26671-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="26671-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26671-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26671-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26671-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="26671-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="26671-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26671-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26671-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="26671-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="26671-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26671-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26671-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="26671-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="26671-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="26671-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26671-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="26671-117">Class of the RR.</span></span> <span data-ttu-id="26671-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="26671-118">Default value is 1.</span></span> <span data-ttu-id="26671-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="26671-119">The following values are valid.</span></span>



| <span data-ttu-id="26671-120">Valore</span><span class="sxs-lookup"><span data-stu-id="26671-120">Value</span></span>                                                                                                | <span data-ttu-id="26671-121">Significato</span><span class="sxs-lookup"><span data-stu-id="26671-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="26671-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="26671-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="26671-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="26671-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="26671-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="26671-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="26671-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="26671-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="26671-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="26671-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="26671-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="26671-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="26671-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="26671-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="26671-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="26671-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="26671-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="26671-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26671-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="26671-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="26671-132">*Sottotipo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26671-132">*Subtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26671-133">Sottotipo del server AFS host.</span><span class="sxs-lookup"><span data-stu-id="26671-133">Subtype of the host AFS server.</span></span> <span data-ttu-id="26671-134">Per il sottotipo 1 (valore = 1), l'host dispone di un server del percorso del volume AFS versione 3,0 per la cella AFS denominata.</span><span class="sxs-lookup"><span data-stu-id="26671-134">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="26671-135">Nel caso del sottotipo 2 (valore = 2), l'host dispone di un server dei nomi autenticato che contiene il nodo della directory radice della cella per la cella DCE/autorità di certificazione denominata.</span><span class="sxs-lookup"><span data-stu-id="26671-135">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="26671-136">*Nomeserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26671-136">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26671-137">FQDN che specifica un host con un server per la cella AFS specificata nel nome del proprietario.</span><span class="sxs-lookup"><span data-stu-id="26671-137">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="26671-138">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="26671-138">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="26671-139">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="26671-139">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26671-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26671-140">Return value</span></span>

<span data-ttu-id="26671-141">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="26671-141">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="26671-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26671-142">Requirements</span></span>



| <span data-ttu-id="26671-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="26671-143">Requirement</span></span> | <span data-ttu-id="26671-144">Valore</span><span class="sxs-lookup"><span data-stu-id="26671-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26671-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26671-145">Minimum supported client</span></span><br/> | <span data-ttu-id="26671-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="26671-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="26671-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26671-147">Minimum supported server</span></span><br/> | <span data-ttu-id="26671-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26671-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="26671-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="26671-149">Namespace</span></span><br/>                | <span data-ttu-id="26671-150">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="26671-150">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="26671-151">MOF</span><span class="sxs-lookup"><span data-stu-id="26671-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26671-152"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26671-152"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26671-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26671-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26671-154">**\_AFSDBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="26671-154">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="26671-155">**Metodo Modify della \_ classe AFSDBType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="26671-155">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="26671-156">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="26671-156">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





