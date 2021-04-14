---
title: Metodo AgeAllRecords della classe MicrosoftDNS_Zone
description: Il metodo AgeAllRecords consente la durata per alcuni o tutti i record non NS e non SOA in una zona.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- DNS del metodo AgeAllRecords
- DNS del metodo AgeAllRecords, classe MicrosoftDNS_Zone
- Classe MicrosoftDNS_Zone DNS, metodo AgeAllRecords
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478478"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="eaee6-106">Metodo AgeAllRecords della classe di \_ zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="eaee6-106">AgeAllRecords method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="eaee6-107">Il metodo **AgeAllRecords** consente la durata per alcuni o tutti i record non NS e non SOA in una zona.</span><span class="sxs-lookup"><span data-stu-id="eaee6-107">The **AgeAllRecords** method enables aging for some or all non-NS and non-SOA records in a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaee6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eaee6-108">Syntax</span></span>


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a><span data-ttu-id="eaee6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="eaee6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaee6-110">*NodeName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="eaee6-110">*NodeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eaee6-111">Nome del nodo da Age.</span><span class="sxs-lookup"><span data-stu-id="eaee6-111">Name of the node to age.</span></span>

</dd> <dt>

<span data-ttu-id="eaee6-112">*ApplyToSubtree* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="eaee6-112">*ApplyToSubtree* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eaee6-113">Specifica se la durata deve essere applicata a tutti i record nel sottoalbero.</span><span class="sxs-lookup"><span data-stu-id="eaee6-113">Specifies whether aging should apply to all records in the subtree.</span></span> <span data-ttu-id="eaee6-114">Impostare su TRUE per applicare l'invecchiamento a tutti i record nel sottoalbero, iniziando con nodeName.</span><span class="sxs-lookup"><span data-stu-id="eaee6-114">Set to TRUE to apply aging to all records in the subtree, beginning with NodeName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaee6-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eaee6-115">Return value</span></span>

<span data-ttu-id="eaee6-116">ERRORE \_ indica che la durata è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="eaee6-116">ERROR\_SUCCESS indicates the aging was successfully completed.</span></span> <span data-ttu-id="eaee6-117">Qualsiasi altro valore è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="eaee6-117">Any other value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaee6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="eaee6-118">Remarks</span></span>

<span data-ttu-id="eaee6-119">Se *NodeName* non è specificato, tutti i record saranno soggetti a durata e scavenging.</span><span class="sxs-lookup"><span data-stu-id="eaee6-119">If *NodeName* is not specified, all records will be subject to aging and scavenging.</span></span>

<span data-ttu-id="eaee6-120">Se si specifica *NodeName* e *ApplyToSubtree* non è specificato o è impostato su zero, i record nel nodo specificato verranno sottoposti a tempo e scavenging.</span><span class="sxs-lookup"><span data-stu-id="eaee6-120">If *NodeName* is specified and *ApplyToSubtree* is not specified or set to zero, records at the specified node will be subjected to aging and scavenging.</span></span>

<span data-ttu-id="eaee6-121">Se si specifica *NodeName* e *ApplyToSubtree* è impostato su 1, tutti i record del sottoalbero a partire da *NodeName* verranno sottoposti a invecchiamento e scavenging.</span><span class="sxs-lookup"><span data-stu-id="eaee6-121">If *NodeName* is specified and *ApplyToSubtree* is set to 1, all records of the subtree starting at *NodeName* will be subjected to aging and scavenging.</span></span> <span data-ttu-id="eaee6-122">Il timestamp è impostato sull'ora corrente per tutti i record non NS e non SOA con i nomi del proprietario identificati dai parametri di input.</span><span class="sxs-lookup"><span data-stu-id="eaee6-122">The time stamp is set to the current time for all non-NS and non-SOA RRs with the owner name(s) identified by the input parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaee6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eaee6-123">Requirements</span></span>



| <span data-ttu-id="eaee6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaee6-124">Requirement</span></span> | <span data-ttu-id="eaee6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="eaee6-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaee6-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eaee6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eaee6-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="eaee6-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eaee6-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eaee6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eaee6-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eaee6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="eaee6-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eaee6-130">Namespace</span></span><br/>                | <span data-ttu-id="eaee6-131">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="eaee6-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="eaee6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="eaee6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaee6-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaee6-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaee6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eaee6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaee6-135">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaee6-135">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="eaee6-136">**Metodo ChangeZoneType della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaee6-136">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="eaee6-137">**Metodo CreateZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaee6-137">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="eaee6-138">**Metodo ForceRefresh della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaee6-138">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="eaee6-139">**Metodo getdistinguishname della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaee6-139">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="eaee6-140">**Metodo PauseZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaee6-140">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="eaee6-141">**Metodo ReloadZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaee6-141">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="eaee6-142">**Metodo ResetSecondaries della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaee6-142">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="eaee6-143">**Metodo ResumeZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaee6-143">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="eaee6-144">**Metodo UpdateFromDS della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaee6-144">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="eaee6-145">**Metodo WriteBackZone della classe di \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaee6-145">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





