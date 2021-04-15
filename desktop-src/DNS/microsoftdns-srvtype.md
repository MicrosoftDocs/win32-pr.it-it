---
title: Classe MicrosoftDNS_SRVType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di servizio (SRV).
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- DNS della classe MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea955cad281e9361b4fa1ca5b033a4ca0d39719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477266"
---
# <a name="microsoftdns_srvtype-class"></a><span data-ttu-id="c1995-105">\_Classe MicrosoftDNS SRVType</span><span class="sxs-lookup"><span data-stu-id="c1995-105">MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="c1995-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="c1995-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Service (SRV) record.</span></span>

<span data-ttu-id="c1995-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="c1995-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1995-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1995-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a><span data-ttu-id="c1995-109">Members</span><span class="sxs-lookup"><span data-stu-id="c1995-109">Members</span></span>

<span data-ttu-id="c1995-110">La **classe \_ SRVType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c1995-110">The **MicrosoftDNS\_SRVType** class has these types of members:</span></span>

-   [<span data-ttu-id="c1995-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="c1995-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c1995-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c1995-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c1995-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="c1995-113">Methods</span></span>

<span data-ttu-id="c1995-114">La **classe \_ SRVType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c1995-114">The **MicrosoftDNS\_SRVType** class has these methods.</span></span>



| <span data-ttu-id="c1995-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="c1995-115">Method</span></span>                             | <span data-ttu-id="c1995-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1995-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1995-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c1995-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="c1995-118">Crea un'istanza di un tipo SRV di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario/destinazione, la classe (impostazione predefinita = IN), il valore di durata (TTL) e la priorità, il peso, la porta e il nome di dominio dell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c1995-118">Instantiates an SRV Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/target Name, class (default = IN), time-to-live value, and target host's priority, weight, port, and domain name.</span></span> <span data-ttu-id="c1995-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="c1995-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="c1995-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="c1995-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="c1995-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="c1995-121">**Modify**</span></span>                         | <span data-ttu-id="c1995-122">Aggiorna i valori TTL, Priority, Weight, Port e Domain Name con i valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c1995-122">Updates the TTL, Priority, Weight, Port, and Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="c1995-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="c1995-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="c1995-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="c1995-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="c1995-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="c1995-125">Qualifiers: Implemented</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="c1995-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c1995-126">Properties</span></span>

<span data-ttu-id="c1995-127">La **classe \_ SRVType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c1995-127">The **MicrosoftDNS\_SRVType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1995-128">**Porta**</span><span class="sxs-lookup"><span data-stu-id="c1995-128">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1995-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1995-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1995-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c1995-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1995-131">Porta utilizzata nell'host di destinazione di un servizio del protocollo.</span><span class="sxs-lookup"><span data-stu-id="c1995-131">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="c1995-132">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="c1995-132">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1995-133">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1995-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1995-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c1995-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1995-135">Priorità dell'host di destinazione specificato nel nome del proprietario.</span><span class="sxs-lookup"><span data-stu-id="c1995-135">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="c1995-136">I numeri più bassi implicano priorità più elevate.</span><span class="sxs-lookup"><span data-stu-id="c1995-136">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="c1995-137">**SRVDomainName**</span><span class="sxs-lookup"><span data-stu-id="c1995-137">**SRVDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1995-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c1995-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1995-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c1995-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1995-140">FQDN dell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c1995-140">FQDN of the target host.</span></span> <span data-ttu-id="c1995-141">Destinazione di \\ . \\ indica che il servizio non è disponibile in questo dominio.</span><span class="sxs-lookup"><span data-stu-id="c1995-141">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="c1995-142">**Weight**</span><span class="sxs-lookup"><span data-stu-id="c1995-142">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1995-143">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1995-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1995-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c1995-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1995-145">Peso dell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c1995-145">Weight of the target host.</span></span> <span data-ttu-id="c1995-146">Questa operazione è utile quando si seleziona tra gli host con la stessa priorità.</span><span class="sxs-lookup"><span data-stu-id="c1995-146">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="c1995-147">La possibilità di utilizzare questo host deve essere proporzionale al suo peso.</span><span class="sxs-lookup"><span data-stu-id="c1995-147">The chances of using this host should be proportional to its weight.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1995-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1995-148">Requirements</span></span>



| <span data-ttu-id="c1995-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1995-149">Requirement</span></span> | <span data-ttu-id="c1995-150">Valore</span><span class="sxs-lookup"><span data-stu-id="c1995-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1995-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1995-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c1995-152">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c1995-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c1995-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1995-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c1995-154">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1995-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c1995-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c1995-155">Namespace</span></span><br/>                | <span data-ttu-id="c1995-156">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="c1995-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c1995-157">MOF</span><span class="sxs-lookup"><span data-stu-id="c1995-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1995-158"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1995-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1995-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1995-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1995-160">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="c1995-160">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c1995-161">**Metodo Modify della \_ classe SRVType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1995-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="c1995-162">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1995-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





