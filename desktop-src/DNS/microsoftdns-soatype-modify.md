---
title: Metodo Modify della classe MicrosoftDNS_SOAType
description: Il metodo modify aggiorna un record di risorse di inizio di autorità (SOA).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_SOAType classe
- Classe MicrosoftDNS_SOAType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff40abc7f4e93b7122a1c48889c17f9efc4f625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047983"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a><span data-ttu-id="e4298-106">Metodo Modify della \_ classe SOAType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="e4298-106">Modify method of the MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="e4298-107">Il metodo **Modify** aggiorna un record di risorse di inizio di autorità (SOA).</span><span class="sxs-lookup"><span data-stu-id="e4298-107">The **Modify** method updates a Start Of Authority (SOA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4298-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4298-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e4298-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4298-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4298-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e4298-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4298-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="e4298-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e4298-112">*SerialNumber* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e4298-112">*SerialNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4298-113">Numero di serie SOA che rappresenta il numero di volte in cui la zona è stata aggiornata, usata dai [*server secondari*](s-gly.md) per determinare se è necessario il trasferimento di zona.</span><span class="sxs-lookup"><span data-stu-id="e4298-113">SOA serial number representing the number of times the zone has been updated, used by [*secondary servers*](s-gly.md) to determine whether zone transfer is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="e4298-114">*PrimaryServer* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e4298-114">*PrimaryServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4298-115">Nome del server primario.</span><span class="sxs-lookup"><span data-stu-id="e4298-115">Name of the primary server.</span></span>

</dd> <dt>

<span data-ttu-id="e4298-116">*Qualcunoresponsabile* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e4298-116">*ResponsibleParty* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4298-117">Indirizzo della cassetta postale della parte responsabile, nel formato alias. dominio, ad esempio xyz.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="e4298-117">Mailbox address of the responsible party, in the form of alias.domain, such as xyz.microsoft.com.</span></span> <span data-ttu-id="e4298-118">Si noti l'uso di un punto anziché un simbolo di chiocciola (@).</span><span class="sxs-lookup"><span data-stu-id="e4298-118">Note the use of a period rather than an at symbol (@).</span></span>

</dd> <dt>

<span data-ttu-id="e4298-119">*RefreshInterval* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e4298-119">*RefreshInterval* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4298-120">Tempo, in secondi, prima che sia necessario aggiornare la zona contenente questo record.</span><span class="sxs-lookup"><span data-stu-id="e4298-120">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="e4298-121">*RetryDelay* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e4298-121">*RetryDelay* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4298-122">Tempo, in secondi, per cui il server DNS deve ritardare tra i tentativi di risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e4298-122">Time, in seconds, the DNS Server should delay between name resolution attempts.</span></span>

</dd> <dt>

<span data-ttu-id="e4298-123">*ExpireLimit* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e4298-123">*ExpireLimit* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4298-124">Tempo, in secondi, durante il quale i server secondari devono attendere una risposta dal server primario prima di rimuovere le copie del file di zona come non valide.</span><span class="sxs-lookup"><span data-stu-id="e4298-124">Time, in seconds, that secondary servers should wait for a response from the primary server before discarding their copies of the zone file as invalid.</span></span>

</dd> <dt>

<span data-ttu-id="e4298-125">*MinimumTTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e4298-125">*MinimumTTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4298-126">Tempo TTL, in secondi, applicato ai record di risorse nella zona che non specificano un valore TTL specifico.</span><span class="sxs-lookup"><span data-stu-id="e4298-126">TTL time, in seconds, applied to resource records in the zone that do not specify their own TTL.</span></span>

</dd> <dt>

<span data-ttu-id="e4298-127">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e4298-127">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e4298-128">Riferimento all'oggetto modificato</span><span class="sxs-lookup"><span data-stu-id="e4298-128">Reference to the modified object</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4298-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4298-129">Return value</span></span>

<span data-ttu-id="e4298-130">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e4298-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4298-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4298-131">Remarks</span></span>

<span data-ttu-id="e4298-132">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="e4298-132">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4298-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4298-133">Requirements</span></span>



| <span data-ttu-id="e4298-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4298-134">Requirement</span></span> | <span data-ttu-id="e4298-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e4298-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4298-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4298-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e4298-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e4298-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e4298-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4298-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e4298-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e4298-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e4298-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e4298-140">Namespace</span></span><br/>                | <span data-ttu-id="e4298-141">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="e4298-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e4298-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e4298-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4298-143"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4298-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4298-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4298-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4298-145">**\_SOAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e4298-145">**MicrosoftDNS\_SOAType**</span></span>](microsoftdns-soatype.md)
</dt> <dt>

[<span data-ttu-id="e4298-146">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e4298-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





