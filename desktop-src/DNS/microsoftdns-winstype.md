---
title: Classe MicrosoftDNS_WINSType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record WINS (Windows Internet Name Service).
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- DNS della classe MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSType.Modify
- MicrosoftDNS_WINSType.MappingFlag
- MicrosoftDNS_WINSType.LookupTimeout
- MicrosoftDNS_WINSType.CacheTimeout
- MicrosoftDNS_WINSType.WinsServers
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce23132073305142948518327ea5b6c7e46f1289
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874093"
---
# <a name="microsoftdns_winstype-class"></a><span data-ttu-id="df135-105">\_Classe MicrosoftDNS WINSType</span><span class="sxs-lookup"><span data-stu-id="df135-105">MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="df135-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record WINS (Windows Internet Name Service).</span><span class="sxs-lookup"><span data-stu-id="df135-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Windows Internet Name Service (WINS) record.</span></span>

<span data-ttu-id="df135-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="df135-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="df135-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df135-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string WinsServers;
};
```

## <a name="members"></a><span data-ttu-id="df135-109">Members</span><span class="sxs-lookup"><span data-stu-id="df135-109">Members</span></span>

<span data-ttu-id="df135-110">La **classe \_ WINSType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="df135-110">The **MicrosoftDNS\_WINSType** class has these types of members:</span></span>

-   [<span data-ttu-id="df135-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="df135-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="df135-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="df135-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="df135-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="df135-113">Methods</span></span>

<span data-ttu-id="df135-114">La **classe \_ WINSType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="df135-114">The **MicrosoftDNS\_WINSType** class has these methods.</span></span>



| <span data-ttu-id="df135-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="df135-115">Method</span></span>                             | <span data-ttu-id="df135-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df135-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df135-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="df135-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="df135-118">Crea un'istanza di un tipo WINS di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata (TTL) e il flag di mapping WINS, il timeout di ricerca, il timeout della cache e l'elenco degli indirizzi IP per la ricerca</span><span class="sxs-lookup"><span data-stu-id="df135-118">Instantiates a WINS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, look-up time out, cache time out and list of IP addresses for look up.</span></span> <span data-ttu-id="df135-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="df135-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="df135-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="df135-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="df135-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="df135-121">**Modify**</span></span>                         | <span data-ttu-id="df135-122">Aggiorna il valore TTL, il flag di mapping, il timeout di ricerca, il timeout della cache e i server WINS ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="df135-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Wins Servers to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="df135-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="df135-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="df135-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="df135-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="df135-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="df135-125">Qualifiers: Implemented</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="df135-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="df135-126">Properties</span></span>

<span data-ttu-id="df135-127">La **classe \_ WINSType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="df135-127">The **MicrosoftDNS\_WINSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df135-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="df135-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df135-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df135-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df135-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df135-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df135-131">Tempo, in secondi, per cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.</span><span class="sxs-lookup"><span data-stu-id="df135-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="df135-132">**LookupTimeout**</span><span class="sxs-lookup"><span data-stu-id="df135-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df135-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df135-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df135-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df135-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df135-135">Tempo, in secondi, durante il quale un server DNS tenta la risoluzione usando la ricerca di WINS.</span><span class="sxs-lookup"><span data-stu-id="df135-135">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="df135-136">**MappingFlag**</span><span class="sxs-lookup"><span data-stu-id="df135-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df135-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df135-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df135-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df135-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df135-139">Flag di mapping WINS che specifica se il record deve essere incluso nella replica della zona.</span><span class="sxs-lookup"><span data-stu-id="df135-139">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="df135-140">Potrebbero essere presenti solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale).</span><span class="sxs-lookup"><span data-stu-id="df135-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="df135-141">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="df135-141">The following values are valid.</span></span>



| <span data-ttu-id="df135-142">Valore</span><span class="sxs-lookup"><span data-stu-id="df135-142">Value</span></span>                                                                                                                                               | <span data-ttu-id="df135-143">Significato</span><span class="sxs-lookup"><span data-stu-id="df135-143">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="df135-144"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="df135-144"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="df135-145">Flag di replica</span><span class="sxs-lookup"><span data-stu-id="df135-145">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="df135-146"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="df135-146"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="df135-147">Flag senza replica (record locale)</span><span class="sxs-lookup"><span data-stu-id="df135-147">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="df135-148">**WinsServers**</span><span class="sxs-lookup"><span data-stu-id="df135-148">**WinsServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df135-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df135-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df135-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df135-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df135-151">Elenco di indirizzi IP delimitati da virgole dei server WINS utilizzati nelle ricerche WINS.</span><span class="sxs-lookup"><span data-stu-id="df135-151">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df135-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df135-152">Requirements</span></span>



| <span data-ttu-id="df135-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="df135-153">Requirement</span></span> | <span data-ttu-id="df135-154">Valore</span><span class="sxs-lookup"><span data-stu-id="df135-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df135-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df135-155">Minimum supported client</span></span><br/> | <span data-ttu-id="df135-156">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="df135-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="df135-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df135-157">Minimum supported server</span></span><br/> | <span data-ttu-id="df135-158">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df135-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="df135-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="df135-159">Namespace</span></span><br/>                | <span data-ttu-id="df135-160">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="df135-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="df135-161">MOF</span><span class="sxs-lookup"><span data-stu-id="df135-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df135-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df135-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df135-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df135-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df135-164">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WINSType**</span><span class="sxs-lookup"><span data-stu-id="df135-164">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="df135-165">**Metodo Modify della \_ classe WINSType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="df135-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="df135-166">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="df135-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





