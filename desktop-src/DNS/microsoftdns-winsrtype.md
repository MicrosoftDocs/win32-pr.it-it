---
title: Classe MicrosoftDNS_WINSRType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record WINS di ricerca inversa (WINSR).
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- DNS della classe MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSRType.Modify
- MicrosoftDNS_WINSRType.MappingFlag
- MicrosoftDNS_WINSRType.LookupTimeout
- MicrosoftDNS_WINSRType.CacheTimeout
- MicrosoftDNS_WINSRType.ResultDomain
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9500c6a36a1c3a7cc243f1cbcfbc0edca6cecf2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400896"
---
# <a name="microsoftdns_winsrtype-class"></a><span data-ttu-id="50ff1-105">\_Classe MicrosoftDNS WINSRType</span><span class="sxs-lookup"><span data-stu-id="50ff1-105">MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="50ff1-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record WINS di ricerca INversa (WINSR).</span><span class="sxs-lookup"><span data-stu-id="50ff1-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a WINS Reverse Look-up (WINSR) record.</span></span>

<span data-ttu-id="50ff1-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="50ff1-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="50ff1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50ff1-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSRType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string ResultDomain;
};
```

## <a name="members"></a><span data-ttu-id="50ff1-109">Members</span><span class="sxs-lookup"><span data-stu-id="50ff1-109">Members</span></span>

<span data-ttu-id="50ff1-110">La **classe \_ WINSRType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="50ff1-110">The **MicrosoftDNS\_WINSRType** class has these types of members:</span></span>

-   [<span data-ttu-id="50ff1-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="50ff1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="50ff1-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="50ff1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="50ff1-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="50ff1-113">Methods</span></span>

<span data-ttu-id="50ff1-114">La **classe \_ WINSRType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="50ff1-114">The **MicrosoftDNS\_WINSRType** class has these methods.</span></span>



| <span data-ttu-id="50ff1-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="50ff1-115">Method</span></span>                             | <span data-ttu-id="50ff1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50ff1-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50ff1-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="50ff1-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="50ff1-118">Crea un'istanza di un tipo di record WINS in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata e il flag di mapping WINS, il timeout della ricerca inversa, il timeout della cache WINS e il nome di dominio da accodare.</span><span class="sxs-lookup"><span data-stu-id="50ff1-118">Instantiates a WINSR Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="50ff1-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="50ff1-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="50ff1-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="50ff1-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="50ff1-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="50ff1-121">**Modify**</span></span>                         | <span data-ttu-id="50ff1-122">Aggiorna il valore TTL, il flag di mapping, il timeout di ricerca, il timeout della cache e il dominio dei risultati ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="50ff1-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="50ff1-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="50ff1-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="50ff1-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="50ff1-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="50ff1-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="50ff1-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="50ff1-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="50ff1-126">Properties</span></span>

<span data-ttu-id="50ff1-127">La **classe \_ WINSRType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="50ff1-127">The **MicrosoftDNS\_WINSRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50ff1-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="50ff1-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50ff1-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50ff1-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50ff1-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50ff1-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50ff1-131">Tempo, in secondi, per cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.</span><span class="sxs-lookup"><span data-stu-id="50ff1-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="50ff1-132">**LookupTimeout**</span><span class="sxs-lookup"><span data-stu-id="50ff1-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50ff1-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50ff1-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50ff1-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50ff1-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50ff1-135">Timeout, in secondi, per un server DNS che utilizza la ricerca inversa WINS.</span><span class="sxs-lookup"><span data-stu-id="50ff1-135">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="50ff1-136">**MappingFlag**</span><span class="sxs-lookup"><span data-stu-id="50ff1-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50ff1-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50ff1-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50ff1-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50ff1-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50ff1-139">Flag di mapping WINSr che specifica se il record deve essere incluso nella replica della zona.</span><span class="sxs-lookup"><span data-stu-id="50ff1-139">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="50ff1-140">Potrebbero essere presenti solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale).</span><span class="sxs-lookup"><span data-stu-id="50ff1-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="50ff1-141">**ResultDomain**</span><span class="sxs-lookup"><span data-stu-id="50ff1-141">**ResultDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50ff1-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="50ff1-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50ff1-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50ff1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50ff1-144">Nome di dominio da aggiungere ai nomi NetBIOS restituiti.</span><span class="sxs-lookup"><span data-stu-id="50ff1-144">Domain name to append to returned NetBIOS names.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50ff1-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50ff1-145">Requirements</span></span>



| <span data-ttu-id="50ff1-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="50ff1-146">Requirement</span></span> | <span data-ttu-id="50ff1-147">Valore</span><span class="sxs-lookup"><span data-stu-id="50ff1-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50ff1-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50ff1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="50ff1-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="50ff1-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="50ff1-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50ff1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="50ff1-151">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="50ff1-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="50ff1-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="50ff1-152">Namespace</span></span><br/>                | <span data-ttu-id="50ff1-153">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="50ff1-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="50ff1-154">MOF</span><span class="sxs-lookup"><span data-stu-id="50ff1-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50ff1-155"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50ff1-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50ff1-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50ff1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ff1-157">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="50ff1-157">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="50ff1-158">**Metodo Modify della \_ classe WINSRType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="50ff1-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="50ff1-159">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="50ff1-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





