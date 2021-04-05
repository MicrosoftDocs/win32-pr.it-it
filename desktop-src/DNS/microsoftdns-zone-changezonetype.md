---
title: Metodo ChangeZoneType della classe MicrosoftDNS_Zone
description: Il metodo ChangeZoneType modifica il tipo di una zona.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- DNS del metodo ChangeZoneType
- DNS del metodo ChangeZoneType, classe MicrosoftDNS_Zone
- Classe MicrosoftDNS_Zone DNS, metodo ChangeZoneType
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048242"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="3bf78-106">Metodo ChangeZoneType della classe di \_ zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="3bf78-106">ChangeZoneType method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="3bf78-107">Il metodo **ChangeZoneType** modifica il tipo di una zona.</span><span class="sxs-lookup"><span data-stu-id="3bf78-107">The **ChangeZoneType** method changes the type of a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bf78-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3bf78-108">Syntax</span></span>


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3bf78-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3bf78-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bf78-110">*ZoneType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bf78-110">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bf78-111">Tipo di zona.</span><span class="sxs-lookup"><span data-stu-id="3bf78-111">Type of zone.</span></span> <span data-ttu-id="3bf78-112">Di seguito sono riportati i valori validi:</span><span class="sxs-lookup"><span data-stu-id="3bf78-112">Valid values are the following:</span></span>



| <span data-ttu-id="3bf78-113">Valore</span><span class="sxs-lookup"><span data-stu-id="3bf78-113">Value</span></span>                                                                        | <span data-ttu-id="3bf78-114">Significato</span><span class="sxs-lookup"><span data-stu-id="3bf78-114">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="3bf78-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3bf78-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="3bf78-116">Zona primaria.</span><span class="sxs-lookup"><span data-stu-id="3bf78-116">Primary zone.</span></span><br/>   |
| <dl> <span data-ttu-id="3bf78-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3bf78-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="3bf78-118">Zona secondaria.</span><span class="sxs-lookup"><span data-stu-id="3bf78-118">Secondary zone.</span></span><br/> |
| <dl> <span data-ttu-id="3bf78-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3bf78-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="3bf78-120">Area stub.</span><span class="sxs-lookup"><span data-stu-id="3bf78-120">Stub zone.</span></span><br/>      |
| <dl> <span data-ttu-id="3bf78-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3bf78-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="3bf78-122">Server d'avanzamento della zona.</span><span class="sxs-lookup"><span data-stu-id="3bf78-122">Zone forwarder.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3bf78-123">*DataFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3bf78-123">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3bf78-124">Nome del file di dati associato alla zona.</span><span class="sxs-lookup"><span data-stu-id="3bf78-124">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="3bf78-125">*IpAddr* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3bf78-125">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3bf78-126">Indirizzo IP del server DNS Mater per la zona.</span><span class="sxs-lookup"><span data-stu-id="3bf78-126">IP address of the mater DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="3bf78-127">*AdminEmailName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3bf78-127">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3bf78-128">Indirizzo di posta elettronica dell'amministratore responsabile della zona.</span><span class="sxs-lookup"><span data-stu-id="3bf78-128">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="3bf78-129">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="3bf78-129">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3bf78-130">RR di tipo **\_ zona MicrosoftDns**.</span><span class="sxs-lookup"><span data-stu-id="3bf78-130">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bf78-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3bf78-131">Return value</span></span>

<span data-ttu-id="3bf78-132">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3bf78-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bf78-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bf78-133">Requirements</span></span>



| <span data-ttu-id="3bf78-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bf78-134">Requirement</span></span> | <span data-ttu-id="3bf78-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3bf78-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bf78-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bf78-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3bf78-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3bf78-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3bf78-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bf78-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3bf78-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3bf78-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3bf78-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3bf78-140">Namespace</span></span><br/>                | <span data-ttu-id="3bf78-141">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="3bf78-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3bf78-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3bf78-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bf78-143"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bf78-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bf78-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bf78-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bf78-145">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3bf78-145">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="3bf78-146">**Metodo AgeAllRecords della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3bf78-146">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="3bf78-147">**Metodo CreateZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3bf78-147">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="3bf78-148">**Metodo ForceRefresh della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3bf78-148">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="3bf78-149">**Metodo getdistinguishname della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3bf78-149">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="3bf78-150">**Metodo PauseZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3bf78-150">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="3bf78-151">**Metodo ReloadZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3bf78-151">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="3bf78-152">**Metodo ResetSecondaries della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3bf78-152">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="3bf78-153">**Metodo ResumeZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3bf78-153">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="3bf78-154">**Metodo UpdateFromDS della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3bf78-154">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="3bf78-155">**Metodo WriteBackZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3bf78-155">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





