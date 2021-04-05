---
title: Classe MicrosoftDNS_KEYType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di risorse chiave.
ms.assetid: d3fa1f35-fa0a-47ee-b2be-4464b9b21d80
keywords:
- DNS della classe MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
- MicrosoftDNS_KEYType.Modify
- MicrosoftDNS_KEYType.Flags
- MicrosoftDNS_KEYType.Protocol
- MicrosoftDNS_KEYType.Algorithm
- MicrosoftDNS_KEYType.PublicKey
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1e814af1d22820f1722e5812dd314dd1c7f6e0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874002"
---
# <a name="microsoftdns_keytype-class"></a><span data-ttu-id="4973b-105">\_Classe di tipo MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="4973b-105">MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="4973b-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di risorse chiave.</span><span class="sxs-lookup"><span data-stu-id="4973b-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a KEY Resource Record.</span></span>

<span data-ttu-id="4973b-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="4973b-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4973b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4973b-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_KEYType : MicrosoftDNS_ResourceRecord
{
  uint16 Flags;
  uint16 Protocol;
  uint16 Algorithm;
  string PublicKey;
};
```

## <a name="members"></a><span data-ttu-id="4973b-109">Members</span><span class="sxs-lookup"><span data-stu-id="4973b-109">Members</span></span>

<span data-ttu-id="4973b-110">La classe del **\_ tipo** di codice MicrosoftDNS presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4973b-110">The **MicrosoftDNS\_KEYType** class has these types of members:</span></span>

-   [<span data-ttu-id="4973b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="4973b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4973b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4973b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4973b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="4973b-113">Methods</span></span>

<span data-ttu-id="4973b-114">Questi metodi sono disponibili nella classe di **\_ tipo MicrosoftDNS** .</span><span class="sxs-lookup"><span data-stu-id="4973b-114">The **MicrosoftDNS\_KEYType** class has these methods.</span></span>



| <span data-ttu-id="4973b-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="4973b-115">Method</span></span>                             | <span data-ttu-id="4973b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4973b-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4973b-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="4973b-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="4973b-118">Crea un'istanza di un record di risorse chiave basato sui dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata e il flag di mapping WINS, il timeout della ricerca inversa, il timeout della cache WINS e il nome di dominio da accodare.</span><span class="sxs-lookup"><span data-stu-id="4973b-118">Instantiates a KEY Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="4973b-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="4973b-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="4973b-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="4973b-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="4973b-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="4973b-121">**Modify**</span></span>                         | <span data-ttu-id="4973b-122">Aggiorna il valore TTL, il flag di mapping, il timeout di ricerca, il timeout della cache e il dominio dei risultati ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4973b-122">Updates the TTL, mapping flag, look-up time out, cache time out, and result domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="4973b-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="4973b-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="4973b-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="4973b-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="4973b-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="4973b-125">Qualifiers: Implemented</span></span><br/>                          |



 

### <a name="properties"></a><span data-ttu-id="4973b-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4973b-126">Properties</span></span>

<span data-ttu-id="4973b-127">La classe di **\_ tipo MicrosoftDNS** è dotata di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4973b-127">The **MicrosoftDNS\_KEYType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4973b-128">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="4973b-128">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4973b-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4973b-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4973b-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4973b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4973b-131">Algoritmo utilizzato con la chiave specificata nel record di risorse.</span><span class="sxs-lookup"><span data-stu-id="4973b-131">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="4973b-132">I valori assegnati sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4973b-132">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="4973b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4973b-133">Value</span></span>                                                                                                | <span data-ttu-id="4973b-134">Significato</span><span class="sxs-lookup"><span data-stu-id="4973b-134">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4973b-135"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4973b-135"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4973b-136">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="4973b-136">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="4973b-137"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4973b-137"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4973b-138">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="4973b-138">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="4973b-139"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4973b-139"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="4973b-140">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="4973b-140">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="4973b-141"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4973b-141"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4973b-142">Crittografia a curva ellittica</span><span class="sxs-lookup"><span data-stu-id="4973b-142">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4973b-143">**Flag**</span><span class="sxs-lookup"><span data-stu-id="4973b-143">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4973b-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4973b-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4973b-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4973b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4973b-146">Flag utilizzati per specificare il mapping, come descritto in IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="4973b-146">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="4973b-147">**Protocollo**</span><span class="sxs-lookup"><span data-stu-id="4973b-147">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4973b-148">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4973b-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4973b-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4973b-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4973b-150">Protocollo per il quale è possibile utilizzare la chiave specificata nel record di risorse.</span><span class="sxs-lookup"><span data-stu-id="4973b-150">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="4973b-151">I valori assegnati sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4973b-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="4973b-152">Valore</span><span class="sxs-lookup"><span data-stu-id="4973b-152">Value</span></span>                                                                                                    | <span data-ttu-id="4973b-153">Significato</span><span class="sxs-lookup"><span data-stu-id="4973b-153">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4973b-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4973b-154"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="4973b-155">TLS</span><span class="sxs-lookup"><span data-stu-id="4973b-155">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="4973b-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4973b-156"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="4973b-157">Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="4973b-157">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="4973b-158"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4973b-158"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="4973b-159">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="4973b-159">DNSSEC</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="4973b-160"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4973b-160"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="4973b-161">IPsec</span><span class="sxs-lookup"><span data-stu-id="4973b-161">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="4973b-162"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="4973b-162"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="4973b-163">Tutti i protocolli</span><span class="sxs-lookup"><span data-stu-id="4973b-163">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4973b-164">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="4973b-164">**PublicKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4973b-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4973b-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4973b-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4973b-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4973b-167">Chiave pubblica, rappresentata in base 64 come descritto nell'Appendice A di RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="4973b-167">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4973b-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4973b-168">Requirements</span></span>



| <span data-ttu-id="4973b-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="4973b-169">Requirement</span></span> | <span data-ttu-id="4973b-170">Valore</span><span class="sxs-lookup"><span data-stu-id="4973b-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4973b-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4973b-171">Minimum supported client</span></span><br/> | <span data-ttu-id="4973b-172">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4973b-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4973b-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4973b-173">Minimum supported server</span></span><br/> | <span data-ttu-id="4973b-174">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4973b-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4973b-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4973b-175">Namespace</span></span><br/>                | <span data-ttu-id="4973b-176">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="4973b-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4973b-177">MOF</span><span class="sxs-lookup"><span data-stu-id="4973b-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4973b-178"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4973b-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4973b-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4973b-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4973b-180">**Metodo CreateInstanceFromPropertyData della classe di \_ tipo MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4973b-180">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="4973b-181">**Metodo Modify della classe di \_ tipo MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4973b-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="4973b-182">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4973b-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





