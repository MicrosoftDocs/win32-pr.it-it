---
title: Metodo ResetSecondaries della classe MicrosoftDNS_Zone
description: Il metodo ResetSecondaries Reimposta gli indirizzi IP per i server DNS secondari nella zona.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- DNS del metodo ResetSecondaries
- DNS del metodo ResetSecondaries, classe MicrosoftDNS_Zone
- Classe MicrosoftDNS_Zone DNS, metodo ResetSecondaries
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964539"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="81f6f-106">Metodo ResetSecondaries della classe di \_ zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="81f6f-106">ResetSecondaries method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="81f6f-107">Il metodo **ResetSecondaries** Reimposta gli indirizzi IP per i server DNS secondari nella zona.</span><span class="sxs-lookup"><span data-stu-id="81f6f-107">The **ResetSecondaries** method resets the IP addresses for secondary DNS Servers in the zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="81f6f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81f6f-108">Syntax</span></span>


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="81f6f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="81f6f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81f6f-110">*SecondaryServers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81f6f-110">*SecondaryServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f6f-111">Matrice di indirizzi IP per i server DNS secondari.</span><span class="sxs-lookup"><span data-stu-id="81f6f-111">Array of IP addresses for secondary DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="81f6f-112">*SecureSecondaries* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81f6f-112">*SecureSecondaries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f6f-113">Specifica la sicurezza da applicare e deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="81f6f-113">Specifies the security to be applied and must be one of the following:</span></span>

-   <span data-ttu-id="81f6f-114">SECSECURE della zona \_ \_ senza \_ sicurezza</span><span class="sxs-lookup"><span data-stu-id="81f6f-114">ZONE\_SECSECURE\_NO\_SECURITY</span></span>
-   <span data-ttu-id="81f6f-115">ZONA \_ \_ solo NS \_ SECSECURE</span><span class="sxs-lookup"><span data-stu-id="81f6f-115">ZONE\_SECSECURE\_NS\_ONLY</span></span>
-   <span data-ttu-id="81f6f-116">\_ \_ solo elenco SECSECURE \_ zona</span><span class="sxs-lookup"><span data-stu-id="81f6f-116">ZONE\_SECSECURE\_LIST\_ONLY</span></span>
-   <span data-ttu-id="81f6f-117">AREA \_ SECSECURE \_ No \_ XFR</span><span class="sxs-lookup"><span data-stu-id="81f6f-117">ZONE\_SECSECURE\_NO\_XFR</span></span>

</dd> <dt>

<span data-ttu-id="81f6f-118">*NotifyServers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81f6f-118">*NotifyServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f6f-119">Indirizzo IP dei server DNS a cui ricevere una notifica in caso di modifica della zona.</span><span class="sxs-lookup"><span data-stu-id="81f6f-119">IP address of DNS Servers to be notified when the zone changes.</span></span>

</dd> <dt>

<span data-ttu-id="81f6f-120">*Invia notifica* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81f6f-120">*Notify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f6f-121">L'impostazione di notifica deve essere una delle seguenti:</span><span class="sxs-lookup"><span data-stu-id="81f6f-121">Notification setting and must be one of the following:</span></span>

-   <span data-ttu-id="81f6f-122">\_notifica zona \_ disattivata</span><span class="sxs-lookup"><span data-stu-id="81f6f-122">ZONE\_NOTIFY\_OFF</span></span>
-   <span data-ttu-id="81f6f-123">notifica zona a \_ \_ tutti i database \_ secondari</span><span class="sxs-lookup"><span data-stu-id="81f6f-123">ZONE\_NOTIFY\_ALL\_SECONDARIES</span></span>
-   <span data-ttu-id="81f6f-124">\_ \_ solo elenco notifiche \_ zone</span><span class="sxs-lookup"><span data-stu-id="81f6f-124">ZONE\_NOTIFY\_LIST\_ONLY</span></span>

</dd> <dt>

<span data-ttu-id="81f6f-125">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="81f6f-125">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="81f6f-126">RR di tipo [**\_ zona MicrosoftDNS**](microsoftdns-zone.md).</span><span class="sxs-lookup"><span data-stu-id="81f6f-126">RR of type [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81f6f-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81f6f-127">Return value</span></span>

<span data-ttu-id="81f6f-128">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="81f6f-128">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="81f6f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81f6f-129">Requirements</span></span>



| <span data-ttu-id="81f6f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="81f6f-130">Requirement</span></span> | <span data-ttu-id="81f6f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="81f6f-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81f6f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81f6f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="81f6f-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="81f6f-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="81f6f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81f6f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="81f6f-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81f6f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="81f6f-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="81f6f-136">Namespace</span></span><br/>                | <span data-ttu-id="81f6f-137">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="81f6f-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="81f6f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="81f6f-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81f6f-139"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81f6f-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81f6f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81f6f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81f6f-141">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="81f6f-141">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="81f6f-142">**Metodo AgeAllRecords della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="81f6f-142">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="81f6f-143">**Metodo ChangeZoneType della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="81f6f-143">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="81f6f-144">**Metodo CreateZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="81f6f-144">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="81f6f-145">**Metodo ForceRefresh della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="81f6f-145">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="81f6f-146">**Metodo getdistinguishname della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="81f6f-146">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="81f6f-147">**Metodo PauseZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="81f6f-147">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="81f6f-148">**Metodo ReloadZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="81f6f-148">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="81f6f-149">**Metodo ResumeZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="81f6f-149">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="81f6f-150">**Metodo UpdateFromDS della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="81f6f-150">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="81f6f-151">**Metodo WriteBackZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="81f6f-151">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





