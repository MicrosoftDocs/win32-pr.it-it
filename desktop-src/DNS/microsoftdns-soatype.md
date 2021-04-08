---
title: Classe MicrosoftDNS_SOAType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di inizio di autorità (SOA).
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- DNS della classe MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType.Modify
- MicrosoftDNS_SOAType.SerialNumber
- MicrosoftDNS_SOAType.PrimaryServer
- MicrosoftDNS_SOAType.ResponsibleParty
- MicrosoftDNS_SOAType.RefreshInterval
- MicrosoftDNS_SOAType.RetryDelay
- MicrosoftDNS_SOAType.ExpireLimit
- MicrosoftDNS_SOAType.MinimumTTL
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3e7cb617514e2ed7c8692a866cc80dfc639391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047982"
---
# <a name="microsoftdns_soatype-class"></a><span data-ttu-id="4f302-105">\_Classe MicrosoftDNS SOAType</span><span class="sxs-lookup"><span data-stu-id="4f302-105">MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="4f302-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di inizio di autorità (SOA).</span><span class="sxs-lookup"><span data-stu-id="4f302-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Start Of Authority (SOA) record.</span></span>

<span data-ttu-id="4f302-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="4f302-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f302-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f302-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SOAType : MicrosoftDNS_ResourceRecord
{
  uint32 SerialNumber;
  string PrimaryServer;
  string ResponsibleParty;
  uint32 RefreshInterval;
  uint32 RetryDelay;
  uint32 ExpireLimit;
  uint32 MinimumTTL;
};
```

## <a name="members"></a><span data-ttu-id="4f302-109">Members</span><span class="sxs-lookup"><span data-stu-id="4f302-109">Members</span></span>

<span data-ttu-id="4f302-110">La **classe \_ SOAType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4f302-110">The **MicrosoftDNS\_SOAType** class has these types of members:</span></span>

-   [<span data-ttu-id="4f302-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="4f302-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4f302-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f302-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4f302-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="4f302-113">Methods</span></span>

<span data-ttu-id="4f302-114">La **classe \_ SOAType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4f302-114">The **MicrosoftDNS\_SOAType** class has these methods.</span></span>



| <span data-ttu-id="4f302-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="4f302-115">Method</span></span>     | <span data-ttu-id="4f302-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f302-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f302-117">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="4f302-117">**Modify**</span></span> | <span data-ttu-id="4f302-118">Aggiorna il valore TTL, il numero di serie SOA, il server primario, la parte responsabile, l'intervallo di aggiornamento, il ritardo tra tentativi, il limite di scadenza e il valore TTL minimo (per la zona) ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4f302-118">Updates the TTL, SOA Serial Number, Primary Server, Responsible Party, Refresh Interval, Retry Delay, Expire Limit and Minimum TTL (for the zone) to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="4f302-119">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="4f302-119">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="4f302-120">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="4f302-120">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="4f302-121">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="4f302-121">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4f302-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f302-122">Properties</span></span>

<span data-ttu-id="4f302-123">La **classe \_ SOAType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4f302-123">The **MicrosoftDNS\_SOAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f302-124">**ExpireLimit**</span><span class="sxs-lookup"><span data-stu-id="4f302-124">**ExpireLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f302-125">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f302-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f302-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f302-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f302-127">Tempo, in secondi, prima che una zona che non risponde non sia più autorevole.</span><span class="sxs-lookup"><span data-stu-id="4f302-127">Time, in seconds, before an unresponsive zone is no longer authoritative.</span></span>

</dd> <dt>

<span data-ttu-id="4f302-128">**MinimumTTL**</span><span class="sxs-lookup"><span data-stu-id="4f302-128">**MinimumTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f302-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f302-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f302-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f302-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f302-131">Limite inferiore per il tempo, in secondi, consentito a un server DNS o a un resolver di memorizzazione nella cache di qualsiasi record di risorse dalla zona a cui appartiene il record.</span><span class="sxs-lookup"><span data-stu-id="4f302-131">Lower limit on the time, in seconds, that a DNS Server or Caching resolver are allowed to cache any resource record from the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="4f302-132">**PrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="4f302-132">**PrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f302-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4f302-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f302-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f302-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f302-135">Server DNS autorevole per la zona a cui appartiene il record.</span><span class="sxs-lookup"><span data-stu-id="4f302-135">Authoritative DNS Server for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="4f302-136">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="4f302-136">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f302-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f302-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f302-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f302-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f302-139">Tempo, in secondi, prima che sia necessario aggiornare la zona contenente questo record.</span><span class="sxs-lookup"><span data-stu-id="4f302-139">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="4f302-140">**Qualcunoresponsabile**</span><span class="sxs-lookup"><span data-stu-id="4f302-140">**ResponsibleParty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f302-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4f302-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f302-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f302-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f302-143">Nome della parte responsabile della zona a cui appartiene il record.</span><span class="sxs-lookup"><span data-stu-id="4f302-143">Name of the responsible party for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="4f302-144">**RetryDelay**</span><span class="sxs-lookup"><span data-stu-id="4f302-144">**RetryDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f302-145">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f302-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f302-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f302-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f302-147">Tempo, in secondi, prima di riprovare a eseguire un aggiornamento non riuscito della zona a cui appartiene il record.</span><span class="sxs-lookup"><span data-stu-id="4f302-147">Time, in seconds, before retrying a failed refresh of the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="4f302-148">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="4f302-148">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f302-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f302-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f302-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f302-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f302-151">Numero di serie del record SOA.</span><span class="sxs-lookup"><span data-stu-id="4f302-151">Serial number of the SOA record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f302-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f302-152">Requirements</span></span>



| <span data-ttu-id="4f302-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f302-153">Requirement</span></span> | <span data-ttu-id="4f302-154">Valore</span><span class="sxs-lookup"><span data-stu-id="4f302-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f302-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f302-155">Minimum supported client</span></span><br/> | <span data-ttu-id="4f302-156">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4f302-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4f302-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f302-157">Minimum supported server</span></span><br/> | <span data-ttu-id="4f302-158">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f302-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4f302-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f302-159">Namespace</span></span><br/>                | <span data-ttu-id="4f302-160">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="4f302-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4f302-161">MOF</span><span class="sxs-lookup"><span data-stu-id="4f302-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f302-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f302-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f302-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f302-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f302-164">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4f302-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="4f302-165">**Metodo Modify della \_ classe SOAType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4f302-165">**Modify Method of the MicrosoftDNS\_SOAType Class**</span></span>](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 





