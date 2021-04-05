---
title: Classe MicrosoftDNS_SIGType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di risorse di firma (SIG).
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- DNS della classe MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172869e90664f88e53fc4cfc89f23b8adbf1e3a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740263"
---
# <a name="microsoftdns_sigtype-class"></a><span data-ttu-id="71a22-105">\_Classe MicrosoftDNS SIGType</span><span class="sxs-lookup"><span data-stu-id="71a22-105">MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="71a22-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di risorse di firma (SIG).</span><span class="sxs-lookup"><span data-stu-id="71a22-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Signature (SIG) Resource Record.</span></span>

<span data-ttu-id="71a22-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="71a22-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="71a22-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71a22-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a><span data-ttu-id="71a22-109">Members</span><span class="sxs-lookup"><span data-stu-id="71a22-109">Members</span></span>

<span data-ttu-id="71a22-110">La **classe \_ SIGType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="71a22-110">The **MicrosoftDNS\_SIGType** class has these types of members:</span></span>

-   [<span data-ttu-id="71a22-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="71a22-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="71a22-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="71a22-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="71a22-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="71a22-113">Methods</span></span>

<span data-ttu-id="71a22-114">La **classe \_ SIGType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="71a22-114">The **MicrosoftDNS\_SIGType** class has these methods.</span></span>



| <span data-ttu-id="71a22-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="71a22-115">Method</span></span>                             | <span data-ttu-id="71a22-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71a22-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71a22-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="71a22-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="71a22-118">Crea un'istanza di un RR SIG in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore time-to-Live e il flag di mapping WINS, il timeout della ricerca inversa, il timeout della cache WINS e il nome di dominio da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="71a22-118">Instantiates an SIG RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="71a22-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="71a22-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="71a22-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="71a22-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="71a22-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="71a22-121">**Modify**</span></span>                         | <span data-ttu-id="71a22-122">Aggiorna il valore TTL, il flag di mapping, il timeout di ricerca, il timeout della cache e il dominio dei risultati ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="71a22-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="71a22-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="71a22-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="71a22-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="71a22-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="71a22-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="71a22-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="71a22-126">**Windows Server 2003:** Questo metodo aggiorna anche TypeCovered, Algorithm, labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName e Signature ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="71a22-126">**Windows Server 2003:** This method also updates the TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName and Signature to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="71a22-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="71a22-127">Properties</span></span>

<span data-ttu-id="71a22-128">La **classe \_ SIGType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="71a22-128">The **MicrosoftDNS\_SIGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71a22-129">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="71a22-129">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71a22-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71a22-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71a22-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="71a22-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71a22-132">Algoritmo utilizzato con la chiave specificata nel record di risorse.</span><span class="sxs-lookup"><span data-stu-id="71a22-132">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="71a22-133">I valori assegnati sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="71a22-133">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="71a22-134">Valore</span><span class="sxs-lookup"><span data-stu-id="71a22-134">Value</span></span>                                                                                                | <span data-ttu-id="71a22-135">Significato</span><span class="sxs-lookup"><span data-stu-id="71a22-135">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="71a22-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="71a22-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="71a22-137">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="71a22-137">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="71a22-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="71a22-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="71a22-139">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="71a22-139">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="71a22-140"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="71a22-140"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="71a22-141">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="71a22-141">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="71a22-142"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="71a22-142"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="71a22-143">Crittografia a curva ellittica</span><span class="sxs-lookup"><span data-stu-id="71a22-143">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="71a22-144">**KeyTag**</span><span class="sxs-lookup"><span data-stu-id="71a22-144">**KeyTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71a22-145">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71a22-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71a22-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="71a22-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71a22-147">Metodo usato per scegliere una chiave che verifica un SIG.</span><span class="sxs-lookup"><span data-stu-id="71a22-147">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="71a22-148">Vedere RFC 2535, Appendice C per il metodo usato per calcolare un KeyTag.</span><span class="sxs-lookup"><span data-stu-id="71a22-148">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="71a22-149">**Etichette**</span><span class="sxs-lookup"><span data-stu-id="71a22-149">**Labels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71a22-150">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71a22-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71a22-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="71a22-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71a22-152">Conteggio senza segno delle etichette nel nome originale del proprietario del record di firma.</span><span class="sxs-lookup"><span data-stu-id="71a22-152">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="71a22-153">Il conteggio non include l'etichetta NULL per la radice, né i caratteri jolly iniziali.</span><span class="sxs-lookup"><span data-stu-id="71a22-153">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="71a22-154">**OriginalTTL**</span><span class="sxs-lookup"><span data-stu-id="71a22-154">**OriginalTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71a22-155">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71a22-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71a22-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="71a22-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71a22-157">TTL del set di RR firmato dal SIG.</span><span class="sxs-lookup"><span data-stu-id="71a22-157">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="71a22-158">**Firma**</span><span class="sxs-lookup"><span data-stu-id="71a22-158">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71a22-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="71a22-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71a22-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="71a22-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71a22-161">Firma, rappresentata in base 64, formattata come definito nella RFC 2535, Appendice A.</span><span class="sxs-lookup"><span data-stu-id="71a22-161">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="71a22-162">**SignatureExpiration**</span><span class="sxs-lookup"><span data-stu-id="71a22-162">**SignatureExpiration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71a22-163">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71a22-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71a22-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="71a22-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71a22-165">Data di scadenza della firma, espressa in secondi dall'inizio del 1 gennaio 1970, ora di Greenwich (GMT), esclusi i secondi intercalari.</span><span class="sxs-lookup"><span data-stu-id="71a22-165">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="71a22-166">**SignatureInception**</span><span class="sxs-lookup"><span data-stu-id="71a22-166">**SignatureInception**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71a22-167">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71a22-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71a22-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="71a22-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71a22-169">Data e ora in cui la firma diventa valida, espressa in secondi a partire dall'inizio del 1 ° gennaio 1970, ora di Greenwich (GMT), esclusi i secondi intercalari.</span><span class="sxs-lookup"><span data-stu-id="71a22-169">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="71a22-170">**SignerName**</span><span class="sxs-lookup"><span data-stu-id="71a22-170">**SignerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71a22-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="71a22-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71a22-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="71a22-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71a22-173">Nome di dominio del firmatario che ha generato il record SIG.</span><span class="sxs-lookup"><span data-stu-id="71a22-173">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="71a22-174">**TypeCovered**</span><span class="sxs-lookup"><span data-stu-id="71a22-174">**TypeCovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71a22-175">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71a22-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71a22-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="71a22-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71a22-177">Tipo di RR coperto da questo SIG.</span><span class="sxs-lookup"><span data-stu-id="71a22-177">Type of RR covered by this SIG.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71a22-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71a22-178">Requirements</span></span>



| <span data-ttu-id="71a22-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="71a22-179">Requirement</span></span> | <span data-ttu-id="71a22-180">Valore</span><span class="sxs-lookup"><span data-stu-id="71a22-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71a22-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71a22-181">Minimum supported client</span></span><br/> | <span data-ttu-id="71a22-182">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="71a22-182">None supported</span></span><br/>                                                              |
| <span data-ttu-id="71a22-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71a22-183">Minimum supported server</span></span><br/> | <span data-ttu-id="71a22-184">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="71a22-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="71a22-185">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="71a22-185">Namespace</span></span><br/>                | <span data-ttu-id="71a22-186">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="71a22-186">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="71a22-187">MOF</span><span class="sxs-lookup"><span data-stu-id="71a22-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71a22-188"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71a22-188"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71a22-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71a22-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a22-190">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="71a22-190">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="71a22-191">**Metodo Modify della \_ classe SIGType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="71a22-191">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="71a22-192">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="71a22-192">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





