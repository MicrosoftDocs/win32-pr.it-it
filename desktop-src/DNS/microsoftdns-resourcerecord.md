---
title: Classe MicrosoftDNS_ResourceRecord
description: La \_ classe MicrosoftDNS ResourceRecord rappresenta le proprietà generali di un RR DNS. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- DNS della classe MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe546ceabb5590ccd4907448af5efd5e2d4fe2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964374"
---
# <a name="microsoftdns_resourcerecord-class"></a><span data-ttu-id="15b09-105">\_Classe MicrosoftDNS ResourceRecord</span><span class="sxs-lookup"><span data-stu-id="15b09-105">MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="15b09-106">La classe **MicrosoftDNS \_ ResourceRecord** rappresenta le proprietà generali di un RR DNS.</span><span class="sxs-lookup"><span data-stu-id="15b09-106">The **MicrosoftDNS\_ResourceRecord** class represents the general properties of a DNS RR.</span></span>

<span data-ttu-id="15b09-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="15b09-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="15b09-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15b09-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a><span data-ttu-id="15b09-109">Members</span><span class="sxs-lookup"><span data-stu-id="15b09-109">Members</span></span>

<span data-ttu-id="15b09-110">La **classe \_ ResourceRecord di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="15b09-110">The **MicrosoftDNS\_ResourceRecord** class has these types of members:</span></span>

-   [<span data-ttu-id="15b09-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="15b09-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="15b09-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15b09-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="15b09-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="15b09-113">Methods</span></span>

<span data-ttu-id="15b09-114">La **classe \_ ResourceRecord di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="15b09-114">The **MicrosoftDNS\_ResourceRecord** class has these methods.</span></span>



| <span data-ttu-id="15b09-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="15b09-115">Method</span></span>                                   | <span data-ttu-id="15b09-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15b09-116">Description</span></span>                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15b09-117">**CreateInstanceFromTextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="15b09-117">**CreateInstanceFromTextRepresentation**</span></span> | <span data-ttu-id="15b09-118">Analizza l'RR nella stringa TextRepresentation e con i nomi del server e del contenitore DNS di input, definisce e crea un'istanza di un oggetto ResourceRecord.</span><span class="sxs-lookup"><span data-stu-id="15b09-118">Parses the RR in the TextRepresentation string, and with the input DNS Server and Container Names, defines, and instantiates a ResourceRecord object.</span></span> <span data-ttu-id="15b09-119">Il metodo restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="15b09-119">The method returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="15b09-120">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="15b09-120">Qualifiers: None</span></span><br/> |
| <span data-ttu-id="15b09-121">**GetObjectByTextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="15b09-121">**GetObjectByTextRepresentation**</span></span>        | <span data-ttu-id="15b09-122">Recupera un'istanza esistente della \_ sottoclasse MicrosoftDns ResourceRecord, rappresentata dalla stringa TextRepresentation insieme al server DNS e al nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="15b09-122">Retrieves an existing instance of the MicrosoftDns\_ResourceRecord subclass, represented by the TextRepresentation string along with the DNS Server and Container Name.</span></span> <br/> <span data-ttu-id="15b09-123">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="15b09-123">Qualifiers: None</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="15b09-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15b09-124">Properties</span></span>

<span data-ttu-id="15b09-125">La **classe \_ ResourceRecord di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="15b09-125">The **MicrosoftDNS\_ResourceRecord** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15b09-126">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="15b09-126">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b09-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="15b09-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b09-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15b09-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b09-129">Indica il nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene l'RR.</span><span class="sxs-lookup"><span data-stu-id="15b09-129">Indicates the name of the Container for the Zone, Cache, or RootHints instance that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="15b09-130">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="15b09-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b09-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="15b09-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b09-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15b09-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b09-133">Indica il nome di dominio completo o l'indirizzo IP del server DNS che contiene l'RR.</span><span class="sxs-lookup"><span data-stu-id="15b09-133">Indicates the FQDN or IP address of the DNS Server that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="15b09-134">**NomeDominio**</span><span class="sxs-lookup"><span data-stu-id="15b09-134">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b09-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="15b09-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b09-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15b09-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b09-137">Rappresenta il nome FQDN del dominio che contiene l'RR.</span><span class="sxs-lookup"><span data-stu-id="15b09-137">Represents the FQDN of the Domain that contains the RR.</span></span> <span data-ttu-id="15b09-138">Questa proprietà può contenere le stringhe \\ . Cache \\ o \\ .. RootHints \\ se la cache interna o RootHints contengono rispettivamente l'RR.</span><span class="sxs-lookup"><span data-stu-id="15b09-138">This property may contain the strings \\..Cache\\ or \\..RootHints\\ if the internal cache or RootHints contain the RR, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="15b09-139">**OwnerName**</span><span class="sxs-lookup"><span data-stu-id="15b09-139">**OwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b09-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="15b09-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b09-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15b09-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b09-142">Nome del proprietario per l'RR.</span><span class="sxs-lookup"><span data-stu-id="15b09-142">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="15b09-143">**RecordClass = 1**</span><span class="sxs-lookup"><span data-stu-id="15b09-143">**RecordClass=1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b09-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15b09-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15b09-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15b09-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b09-146">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="15b09-146">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="15b09-147">Questa stringa rappresenta la classe del record di risorse.</span><span class="sxs-lookup"><span data-stu-id="15b09-147">This string represents the class of the Resource Record.</span></span> <span data-ttu-id="15b09-148">I valori validi includono:</span><span class="sxs-lookup"><span data-stu-id="15b09-148">Valid values include:</span></span>

<span data-ttu-id="15b09-149">1: IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="15b09-149">1: IN (Internet)</span></span>

<span data-ttu-id="15b09-150">2: CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="15b09-150">2: CS (CSNET)</span></span>

<span data-ttu-id="15b09-151">3: CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="15b09-151">3: CH (CHAOS)</span></span>

<span data-ttu-id="15b09-152">4: HS (Esiodo)</span><span class="sxs-lookup"><span data-stu-id="15b09-152">4: HS (Hesiod)</span></span>

</dd> <dt>

<span data-ttu-id="15b09-153">**RecordData**</span><span class="sxs-lookup"><span data-stu-id="15b09-153">**RecordData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b09-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="15b09-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b09-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15b09-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b09-156">Dati del record di risorse.</span><span class="sxs-lookup"><span data-stu-id="15b09-156">Resource record data.</span></span>

</dd> <dt>

<span data-ttu-id="15b09-157">**TextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="15b09-157">**TextRepresentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b09-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="15b09-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b09-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15b09-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b09-160">Rappresentazione testuale dell'intero RR.</span><span class="sxs-lookup"><span data-stu-id="15b09-160">Text representation of the entire RR.</span></span>

</dd> <dt>

<span data-ttu-id="15b09-161">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="15b09-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b09-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15b09-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15b09-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15b09-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b09-164">Ora dell'ultimo aggiornamento dell'RR, espressa in ore trascorse dal 1 gennaio 1601, ora di Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="15b09-164">Time at which the RR was last refreshed, expressed in elapsed hours since January 1, 1601, Greenwich Mean Time (GMT).</span></span>

</dd> <dt>

<span data-ttu-id="15b09-165">**TTL**</span><span class="sxs-lookup"><span data-stu-id="15b09-165">**TTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b09-166">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15b09-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15b09-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15b09-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b09-168">Tempo, in secondi, che l'RR può memorizzare nella cache da un [*resolver*](r-gly.md)DNS.</span><span class="sxs-lookup"><span data-stu-id="15b09-168">Time, in seconds, that the RR can be cached by a DNS [*resolver*](r-gly.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15b09-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15b09-169">Requirements</span></span>



| <span data-ttu-id="15b09-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="15b09-170">Requirement</span></span> | <span data-ttu-id="15b09-171">Valore</span><span class="sxs-lookup"><span data-stu-id="15b09-171">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15b09-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15b09-172">Minimum supported client</span></span><br/> | <span data-ttu-id="15b09-173">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="15b09-173">None supported</span></span><br/>                                                              |
| <span data-ttu-id="15b09-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15b09-174">Minimum supported server</span></span><br/> | <span data-ttu-id="15b09-175">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="15b09-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="15b09-176">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="15b09-176">Namespace</span></span><br/>                | <span data-ttu-id="15b09-177">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="15b09-177">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="15b09-178">MOF</span><span class="sxs-lookup"><span data-stu-id="15b09-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15b09-179"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15b09-179"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15b09-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15b09-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b09-181">**Metodo CreateInstanceFromTextRepresentation della classe MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="15b09-181">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[<span data-ttu-id="15b09-182">**Metodo GetObjectByTextRepresentation della classe MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="15b09-182">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





