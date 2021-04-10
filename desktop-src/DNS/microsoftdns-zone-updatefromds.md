---
title: Metodo UpdateFromDS della classe MicrosoftDNS_Zone
description: Il metodo UpdateFromDS impone un aggiornamento della zona dal servizio directory (DS).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- DNS del metodo UpdateFromDS
- DNS del metodo UpdateFromDS, classe MicrosoftDNS_Zone
- Classe MicrosoftDNS_Zone DNS, metodo UpdateFromDS
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8fd0ba4db9b182379ce2ec93508c7a3bab354a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121698"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="6fd61-106">Metodo UpdateFromDS della classe di \_ zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="6fd61-106">UpdateFromDS method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="6fd61-107">Il metodo **UpdateFromDS** impone un aggiornamento della zona dal servizio directory (DS).</span><span class="sxs-lookup"><span data-stu-id="6fd61-107">The **UpdateFromDS** method forces an update of the zone from the Directory Service (DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd61-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fd61-108">Syntax</span></span>


```mof
void UpdateFromDS();
```



## <a name="parameters"></a><span data-ttu-id="6fd61-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6fd61-109">Parameters</span></span>

<span data-ttu-id="6fd61-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6fd61-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6fd61-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6fd61-111">Return value</span></span>

<span data-ttu-id="6fd61-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6fd61-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fd61-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fd61-113">Remarks</span></span>

<span data-ttu-id="6fd61-114">Per eseguire correttamente questo metodo, ZoneType deve essere zero e la zona deve essere archiviata in DS.</span><span class="sxs-lookup"><span data-stu-id="6fd61-114">In order to successfully execute this method, the ZoneType must be zero, and the zone must be stored on the DS.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd61-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fd61-115">Requirements</span></span>



| <span data-ttu-id="6fd61-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fd61-116">Requirement</span></span> | <span data-ttu-id="6fd61-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6fd61-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd61-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fd61-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6fd61-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6fd61-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6fd61-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fd61-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6fd61-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6fd61-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6fd61-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6fd61-122">Namespace</span></span><br/>                | <span data-ttu-id="6fd61-123">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="6fd61-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6fd61-124">MOF</span><span class="sxs-lookup"><span data-stu-id="6fd61-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fd61-125"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fd61-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fd61-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fd61-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd61-127">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6fd61-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="6fd61-128">**Metodo AgeAllRecords della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6fd61-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="6fd61-129">**Metodo ChangeZoneType della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6fd61-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="6fd61-130">**Metodo CreateZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6fd61-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="6fd61-131">**Metodo ForceRefresh della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6fd61-131">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="6fd61-132">**Metodo getdistinguishname della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6fd61-132">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="6fd61-133">**Metodo PauseZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6fd61-133">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="6fd61-134">**Metodo ReloadZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6fd61-134">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="6fd61-135">**Metodo ResetSecondaries della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6fd61-135">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="6fd61-136">**Metodo ResumeZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6fd61-136">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="6fd61-137">**Metodo WriteBackZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6fd61-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





