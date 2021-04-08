---
title: Metodo CreateZone della classe MicrosoftDNS_Zone
description: Il Metodo CreateZone crea una zona DNS.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- DNS del Metodo CreateZone
- DNS del Metodo CreateZone, classe MicrosoftDNS_Zone
- Classe MicrosoftDNS_Zone DNS, Metodo CreateZone
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048540"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="f7374-106">Metodo CreateZone della classe di \_ zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="f7374-106">CreateZone method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="f7374-107">Il metodo **CreateZone** crea una zona DNS.</span><span class="sxs-lookup"><span data-stu-id="f7374-107">The **CreateZone** method creates a DNS zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7374-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7374-108">Syntax</span></span>


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f7374-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7374-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7374-110">*Zonename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7374-110">*ZoneName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7374-111">Stringa che rappresenta il nome della zona.</span><span class="sxs-lookup"><span data-stu-id="f7374-111">String representing the name of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="f7374-112">*ZoneType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7374-112">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7374-113">Tipo di zona.</span><span class="sxs-lookup"><span data-stu-id="f7374-113">Type of zone.</span></span> <span data-ttu-id="f7374-114">Di seguito sono riportati i valori validi:</span><span class="sxs-lookup"><span data-stu-id="f7374-114">Valid values are the following:</span></span>



| <span data-ttu-id="f7374-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f7374-115">Value</span></span>                                                                        | <span data-ttu-id="f7374-116">Significato</span><span class="sxs-lookup"><span data-stu-id="f7374-116">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7374-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f7374-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="f7374-118">Integrazione con Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f7374-118">AD integrated.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="f7374-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f7374-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f7374-120">Zona secondaria.</span><span class="sxs-lookup"><span data-stu-id="f7374-120">Secondary zone.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="f7374-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f7374-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="f7374-122">Area stub.</span><span class="sxs-lookup"><span data-stu-id="f7374-122">Stub zone.</span></span><br/> <span data-ttu-id="f7374-123">**Windows Server 2003:** Questo tipo di zona è stato introdotto in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f7374-123">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/>      |
| <dl> <span data-ttu-id="f7374-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f7374-124"><dt>4</dt></span></span> </dl> | <span data-ttu-id="f7374-125">Server d'avanzamento della zona.</span><span class="sxs-lookup"><span data-stu-id="f7374-125">Zone forwarder.</span></span><br/> <span data-ttu-id="f7374-126">**Windows Server 2003:** Questo tipo di zona è stato introdotto in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f7374-126">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f7374-127">*DsIntegrated* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7374-127">*DsIntegrated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7374-128">Indica se i dati della zona vengono archiviati nel Active Directory o nei file.</span><span class="sxs-lookup"><span data-stu-id="f7374-128">Indicates whether zone data is stored in the Active Directory or in files.</span></span> <span data-ttu-id="f7374-129">Se TRUE, i dati vengono archiviati nella Active Directory; Se FALSE, i dati vengono archiviati in file.</span><span class="sxs-lookup"><span data-stu-id="f7374-129">If TRUE, the data is stored in the Active Directory; if FALSE, the data is stored in files.</span></span>

</dd> <dt>

<span data-ttu-id="f7374-130">*DataFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f7374-130">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7374-131">Nome del file di dati associato alla zona.</span><span class="sxs-lookup"><span data-stu-id="f7374-131">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="f7374-132">*IpAddr* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f7374-132">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7374-133">Indirizzo IP del server DNS master per la zona.</span><span class="sxs-lookup"><span data-stu-id="f7374-133">IP address of the master DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="f7374-134">*AdminEmailName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f7374-134">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7374-135">Indirizzo di posta elettronica dell'amministratore responsabile della zona.</span><span class="sxs-lookup"><span data-stu-id="f7374-135">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="f7374-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f7374-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f7374-137">RR di tipo **\_ zona MicrosoftDns**.</span><span class="sxs-lookup"><span data-stu-id="f7374-137">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7374-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7374-138">Return value</span></span>

<span data-ttu-id="f7374-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f7374-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7374-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7374-140">Requirements</span></span>



| <span data-ttu-id="f7374-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7374-141">Requirement</span></span> | <span data-ttu-id="f7374-142">Valore</span><span class="sxs-lookup"><span data-stu-id="f7374-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7374-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7374-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f7374-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f7374-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f7374-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7374-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f7374-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7374-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f7374-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f7374-147">Namespace</span></span><br/>                | <span data-ttu-id="f7374-148">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="f7374-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f7374-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f7374-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7374-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7374-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7374-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7374-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7374-152">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f7374-152">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="f7374-153">**Metodo AgeAllRecords della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f7374-153">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="f7374-154">**Metodo ChangeZoneType della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f7374-154">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="f7374-155">**Metodo ForceRefresh della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f7374-155">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="f7374-156">**Metodo getdistinguishname della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f7374-156">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="f7374-157">**Metodo PauseZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f7374-157">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="f7374-158">**Metodo ReloadZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f7374-158">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="f7374-159">**Metodo ResetSecondaries della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f7374-159">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="f7374-160">**Metodo ResumeZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f7374-160">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="f7374-161">**Metodo UpdateFromDS della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f7374-161">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="f7374-162">**Metodo WriteBackZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f7374-162">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





