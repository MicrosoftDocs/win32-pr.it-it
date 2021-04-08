---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_SIGType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse di firma (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_SIGType
- Classe MicrosoftDNS_SIGType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21660572d9557e6425b459c5694a7eeee4722cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047985"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="dce75-106">Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SIGType</span><span class="sxs-lookup"><span data-stu-id="dce75-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="dce75-107">Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse di firma (SIG).</span><span class="sxs-lookup"><span data-stu-id="dce75-107">The **CreateInstanceFromPropertyData** method instantiates a Signature (SIG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce75-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dce75-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="dce75-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dce75-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dce75-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-111">FQDN o indirizzo IP del server DNS che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="dce75-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-113">Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.</span><span class="sxs-lookup"><span data-stu-id="dce75-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-114">*Proprietarioname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-115">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="dce75-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-116">*RecordClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="dce75-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-117">Classe dell'RR.</span><span class="sxs-lookup"><span data-stu-id="dce75-117">Class of the RR.</span></span> <span data-ttu-id="dce75-118">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="dce75-118">Default value is 1.</span></span> <span data-ttu-id="dce75-119">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="dce75-119">The following values are valid.</span></span>



| <span data-ttu-id="dce75-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dce75-120">Value</span></span>                                                                                                | <span data-ttu-id="dce75-121">Significato</span><span class="sxs-lookup"><span data-stu-id="dce75-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="dce75-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dce75-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dce75-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="dce75-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="dce75-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dce75-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dce75-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="dce75-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="dce75-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="dce75-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="dce75-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="dce75-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="dce75-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="dce75-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="dce75-129">HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="dce75-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="dce75-130">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="dce75-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-131">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="dce75-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-132">*TypeCovered* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-132">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-133">Tipo di RR coperto da questo SIG.</span><span class="sxs-lookup"><span data-stu-id="dce75-133">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-134">*Algoritmo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-134">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-135">Algoritmo utilizzato con la chiave specificata nel record di risorse.</span><span class="sxs-lookup"><span data-stu-id="dce75-135">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="dce75-136">I valori assegnati sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="dce75-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="dce75-137">Valore</span><span class="sxs-lookup"><span data-stu-id="dce75-137">Value</span></span>                                                                                                | <span data-ttu-id="dce75-138">Significato</span><span class="sxs-lookup"><span data-stu-id="dce75-138">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="dce75-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dce75-139"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dce75-140">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="dce75-140">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="dce75-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dce75-141"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dce75-142">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="dce75-142">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="dce75-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="dce75-143"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="dce75-144">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="dce75-144">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="dce75-145"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="dce75-145"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="dce75-146">Crittografia a curva ellittica</span><span class="sxs-lookup"><span data-stu-id="dce75-146">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dce75-147">*Etichette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-147">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-148">Conteggio senza segno delle etichette nel nome originale del proprietario del record di firma.</span><span class="sxs-lookup"><span data-stu-id="dce75-148">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="dce75-149">Il conteggio non include l'etichetta NULL per la radice, né i caratteri jolly iniziali.</span><span class="sxs-lookup"><span data-stu-id="dce75-149">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-150">*OriginalTTL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-150">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-151">TTL del set di RR firmato dal SIG.</span><span class="sxs-lookup"><span data-stu-id="dce75-151">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-152">*SignatureExpiration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-152">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-153">Data di scadenza della firma, espressa in secondi dall'inizio del 1 gennaio 1970, ora di Greenwich (GMT), esclusi i secondi intercalari.</span><span class="sxs-lookup"><span data-stu-id="dce75-153">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-154">*SignatureInception* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-154">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-155">Data e ora in cui la firma diventa valida, espressa in secondi a partire dall'inizio del 1 ° gennaio 1970, ora di Greenwich (GMT), esclusi i secondi intercalari.</span><span class="sxs-lookup"><span data-stu-id="dce75-155">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-156">*KeyTag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-156">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-157">Metodo usato per scegliere una chiave che verifica un SIG.</span><span class="sxs-lookup"><span data-stu-id="dce75-157">Method used to choose a key that verifies an SIG.</span></span> <span data-ttu-id="dce75-158">Vedere RFC 2535, Appendice C per il metodo usato per calcolare un KeyTag.</span><span class="sxs-lookup"><span data-stu-id="dce75-158">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-159">*SignerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-159">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-160">Nome di dominio del firmatario che ha generato il record SIG.</span><span class="sxs-lookup"><span data-stu-id="dce75-160">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-161">*Firma* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="dce75-161">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-162">Firma, rappresentata in base 64, formattata come definito nella RFC 2535, Appendice A.</span><span class="sxs-lookup"><span data-stu-id="dce75-162">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="dce75-163">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="dce75-163">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dce75-164">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="dce75-164">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dce75-165">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dce75-165">Return value</span></span>

<span data-ttu-id="dce75-166">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="dce75-166">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dce75-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dce75-167">Requirements</span></span>



| <span data-ttu-id="dce75-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="dce75-168">Requirement</span></span> | <span data-ttu-id="dce75-169">Valore</span><span class="sxs-lookup"><span data-stu-id="dce75-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dce75-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dce75-170">Minimum supported client</span></span><br/> | <span data-ttu-id="dce75-171">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dce75-171">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dce75-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dce75-172">Minimum supported server</span></span><br/> | <span data-ttu-id="dce75-173">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dce75-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dce75-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dce75-174">Namespace</span></span><br/>                | <span data-ttu-id="dce75-175">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="dce75-175">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dce75-176">MOF</span><span class="sxs-lookup"><span data-stu-id="dce75-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dce75-177"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dce75-177"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce75-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dce75-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce75-179">**\_SIGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dce75-179">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="dce75-180">**Metodo Modify della \_ classe SIGType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dce75-180">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="dce75-181">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dce75-181">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





