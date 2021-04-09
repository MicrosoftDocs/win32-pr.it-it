---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_KEYType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse chiave.
ms.assetid: 77d7b800-4077-46da-9199-e2abb5801978
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_KEYType
- Classe MicrosoftDNS_KEYType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16dc8f3f591ba3aaf5ac9883cdd3a15c85146d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048731"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="851a0-106">Metodo CreateInstanceFromPropertyData della classe di \_ tipo MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="851a0-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="851a0-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse chiave.</span><span class="sxs-lookup"><span data-stu-id="851a0-107">The **CreateInstanceFromPropertyData** method instantiates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="851a0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="851a0-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Flags,
  [in]           uint16               Protocol,
  [in]           uint16               Algorithm,
  [in]           string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="851a0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="851a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="851a0-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="851a0-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="851a0-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="851a0-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="851a0-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="851a0-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="851a0-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="851a0-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="851a0-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="851a0-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="851a0-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="851a0-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="851a0-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="851a0-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="851a0-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="851a0-117">Class of the RR.</span></span> <span data-ttu-id="851a0-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="851a0-118">Default value is 1.</span></span> <span data-ttu-id="851a0-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="851a0-119">The following values are valid.</span></span>



| <span data-ttu-id="851a0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="851a0-120">Value</span></span>                                                                                                | <span data-ttu-id="851a0-121">Significato</span><span class="sxs-lookup"><span data-stu-id="851a0-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="851a0-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="851a0-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="851a0-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="851a0-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="851a0-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="851a0-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="851a0-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="851a0-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="851a0-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="851a0-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="851a0-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="851a0-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="851a0-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="851a0-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="851a0-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="851a0-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="851a0-132">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="851a0-132">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="851a0-133">Flag utilizzati per specificare il mapping, come descritto in IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="851a0-133">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="851a0-134">*Protocollo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="851a0-134">*Protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="851a0-135">Protocollo per il quale è possibile utilizzare la chiave specificata nel record di risorse.</span><span class="sxs-lookup"><span data-stu-id="851a0-135">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="851a0-136">I valori assegnati sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="851a0-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="851a0-137">Valore</span><span class="sxs-lookup"><span data-stu-id="851a0-137">Value</span></span>                                                                                                    | <span data-ttu-id="851a0-138">Significato</span><span class="sxs-lookup"><span data-stu-id="851a0-138">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="851a0-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-139"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="851a0-140">TLS</span><span class="sxs-lookup"><span data-stu-id="851a0-140">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="851a0-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-141"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="851a0-142">Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="851a0-142">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="851a0-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-143"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="851a0-144">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="851a0-144">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="851a0-145"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-145"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="851a0-146">IPsec</span><span class="sxs-lookup"><span data-stu-id="851a0-146">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="851a0-147"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-147"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="851a0-148">Tutti i protocolli</span><span class="sxs-lookup"><span data-stu-id="851a0-148">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="851a0-149">*Algoritmo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="851a0-149">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="851a0-150">Algoritmo utilizzato con la chiave specificata nel record di risorse.</span><span class="sxs-lookup"><span data-stu-id="851a0-150">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="851a0-151">I valori assegnati sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="851a0-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="851a0-152">Valore</span><span class="sxs-lookup"><span data-stu-id="851a0-152">Value</span></span>                                                                                                | <span data-ttu-id="851a0-153">Significato</span><span class="sxs-lookup"><span data-stu-id="851a0-153">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="851a0-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-154"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="851a0-155">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="851a0-155">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="851a0-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-156"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="851a0-157">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="851a0-157">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="851a0-158"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-158"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="851a0-159">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="851a0-159">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="851a0-160"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-160"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="851a0-161">Crittografia a curva ellittica</span><span class="sxs-lookup"><span data-stu-id="851a0-161">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="851a0-162">*PublicKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="851a0-162">*PublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="851a0-163">Chiave pubblica, rappresentata in base 64 come descritto nell'Appendice A di RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="851a0-163">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="851a0-164">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="851a0-164">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="851a0-165">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="851a0-165">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="851a0-166">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="851a0-166">Return value</span></span>

<span data-ttu-id="851a0-167">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="851a0-167">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="851a0-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="851a0-168">Requirements</span></span>



| <span data-ttu-id="851a0-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="851a0-169">Requirement</span></span> | <span data-ttu-id="851a0-170">Valore</span><span class="sxs-lookup"><span data-stu-id="851a0-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="851a0-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="851a0-171">Minimum supported client</span></span><br/> | <span data-ttu-id="851a0-172">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="851a0-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="851a0-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="851a0-173">Minimum supported server</span></span><br/> | <span data-ttu-id="851a0-174">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="851a0-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="851a0-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="851a0-175">Namespace</span></span><br/>                | <span data-ttu-id="851a0-176">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="851a0-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="851a0-177">MOF</span><span class="sxs-lookup"><span data-stu-id="851a0-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="851a0-178"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="851a0-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="851a0-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="851a0-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="851a0-180">**Tipo di MicrosoftDNS \_**</span><span class="sxs-lookup"><span data-stu-id="851a0-180">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="851a0-181">**Metodo Modify della classe di \_ tipo MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="851a0-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="851a0-182">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="851a0-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





