---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_ATMAType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un indirizzo ATM per il nome (ATMA) del record di risorse.
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_ATMAType
- Classe MicrosoftDNS_ATMAType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fada3759e6384ae6f42a78bd132b9b8ad16f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301643"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="f79a2-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ ATMAType</span><span class="sxs-lookup"><span data-stu-id="f79a2-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="f79a2-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un indirizzo ATM per il nome (ATMA) del record di risorse.</span><span class="sxs-lookup"><span data-stu-id="f79a2-107">The **CreateInstanceFromPropertyData** method instantiates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f79a2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f79a2-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f79a2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f79a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f79a2-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f79a2-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a2-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="f79a2-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f79a2-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f79a2-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a2-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="f79a2-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f79a2-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f79a2-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a2-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="f79a2-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="f79a2-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f79a2-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a2-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="f79a2-117">Class of the RR.</span></span> <span data-ttu-id="f79a2-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="f79a2-118">Default value is 1.</span></span> <span data-ttu-id="f79a2-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="f79a2-119">The following values are valid.</span></span>



| <span data-ttu-id="f79a2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f79a2-120">Value</span></span>                                                                                                | <span data-ttu-id="f79a2-121">Significato</span><span class="sxs-lookup"><span data-stu-id="f79a2-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f79a2-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f79a2-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f79a2-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="f79a2-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="f79a2-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f79a2-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f79a2-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="f79a2-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="f79a2-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f79a2-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f79a2-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="f79a2-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="f79a2-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="f79a2-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f79a2-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="f79a2-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f79a2-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f79a2-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a2-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="f79a2-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f79a2-132">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f79a2-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a2-133">Formato dell'indirizzo ATM.</span><span class="sxs-lookup"><span data-stu-id="f79a2-133">ATM address format.</span></span> <span data-ttu-id="f79a2-134">Due valori possibili per FORMAT sono: 0 che indica il formato AESA (ATM End System Address) e 1 indica il formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="f79a2-134">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="f79a2-135">*ATMAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f79a2-135">*ATMAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a2-136">Stringa di lunghezza variabile di ottetti che contiene l'indirizzo ATM del nodo/proprietario a cui si riferisce questo RR.</span><span class="sxs-lookup"><span data-stu-id="f79a2-136">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="f79a2-137">I primi quattro byte della matrice vengono usati per archiviare le dimensioni della stringa di ottetto.</span><span class="sxs-lookup"><span data-stu-id="f79a2-137">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="f79a2-138">Il byte più significativo viene archiviato nel byte 0.</span><span class="sxs-lookup"><span data-stu-id="f79a2-138">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="f79a2-139">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f79a2-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a2-140">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="f79a2-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f79a2-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f79a2-141">Return value</span></span>

<span data-ttu-id="f79a2-142">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f79a2-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f79a2-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f79a2-143">Requirements</span></span>



| <span data-ttu-id="f79a2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f79a2-144">Requirement</span></span> | <span data-ttu-id="f79a2-145">Valore</span><span class="sxs-lookup"><span data-stu-id="f79a2-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f79a2-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f79a2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f79a2-147">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f79a2-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f79a2-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f79a2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f79a2-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f79a2-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f79a2-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f79a2-150">Namespace</span></span><br/>                | <span data-ttu-id="f79a2-151">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="f79a2-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f79a2-152">MOF</span><span class="sxs-lookup"><span data-stu-id="f79a2-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f79a2-153"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f79a2-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f79a2-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f79a2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79a2-155">**\_ATMAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f79a2-155">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="f79a2-156">**Metodo Modify della \_ classe ATMAType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f79a2-156">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="f79a2-157">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f79a2-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





