---
title: Metodo Modify della classe MicrosoftDNS_WINSRType
description: Il metodo modify aggiorna un record di risorse WINS reverse look up (WINSr).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_WINSRType classe
- Classe MicrosoftDNS_WINSRType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02d89c3cd191262136035f9006853e2f1a7f7dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121274"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="35a5e-106">Metodo Modify della \_ classe WINSRType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="35a5e-106">Modify method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="35a5e-107">Il metodo **Modify** aggiorna un record di risorse WINS reverse look up (WINSR).</span><span class="sxs-lookup"><span data-stu-id="35a5e-107">The **Modify** method updates a WINS Reverse Look up (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a5e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35a5e-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="35a5e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="35a5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a5e-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="35a5e-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35a5e-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="35a5e-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="35a5e-112">*MappingFlag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="35a5e-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35a5e-113">Flag di mapping WINSr che specifica se il record deve essere incluso nella replica della zona.</span><span class="sxs-lookup"><span data-stu-id="35a5e-113">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="35a5e-114">Potrebbero essere presenti solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale).</span><span class="sxs-lookup"><span data-stu-id="35a5e-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="35a5e-115">*LookupTimeout* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="35a5e-115">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35a5e-116">Timeout, in secondi, per un server DNS che utilizza la ricerca inversa WINS.</span><span class="sxs-lookup"><span data-stu-id="35a5e-116">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="35a5e-117">*CacheTimeout* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="35a5e-117">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35a5e-118">Tempo, in secondi, in cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.</span><span class="sxs-lookup"><span data-stu-id="35a5e-118">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="35a5e-119">*ResultDomain* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="35a5e-119">*ResultDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35a5e-120">Nome di dominio da aggiungere ai nomi NetBIOS restituiti.</span><span class="sxs-lookup"><span data-stu-id="35a5e-120">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="35a5e-121">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="35a5e-121">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="35a5e-122">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="35a5e-122">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a5e-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35a5e-123">Return value</span></span>

<span data-ttu-id="35a5e-124">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="35a5e-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a5e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="35a5e-125">Remarks</span></span>

<span data-ttu-id="35a5e-126">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="35a5e-126">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="35a5e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35a5e-127">Requirements</span></span>



| <span data-ttu-id="35a5e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="35a5e-128">Requirement</span></span> | <span data-ttu-id="35a5e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="35a5e-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35a5e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a5e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="35a5e-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="35a5e-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="35a5e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a5e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="35a5e-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="35a5e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="35a5e-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35a5e-134">Namespace</span></span><br/>                | <span data-ttu-id="35a5e-135">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="35a5e-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="35a5e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="35a5e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35a5e-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35a5e-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a5e-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35a5e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a5e-139">**\_WINSRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="35a5e-139">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="35a5e-140">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="35a5e-140">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="35a5e-141">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="35a5e-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





