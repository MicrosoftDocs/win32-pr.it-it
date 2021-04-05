---
title: Metodo Modify della classe MicrosoftDNS_WINSType
description: Il metodo modify aggiorna un record di risorse WINS (Windows Internet Name Service).
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_WINSType classe
- Classe MicrosoftDNS_WINSType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874094"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="7e2b7-106">Metodo Modify della \_ classe WINSType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="7e2b7-106">Modify method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="7e2b7-107">Il metodo **Modify** aggiorna un record di risorse WINS (Windows Internet Name Service).</span><span class="sxs-lookup"><span data-stu-id="7e2b7-107">The **Modify** method updates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e2b7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e2b7-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="7e2b7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e2b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e2b7-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7e2b7-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7e2b7-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="7e2b7-112">*MappingFlag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7e2b7-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7e2b7-113">Flag di mapping WINS che specifica se il record deve essere incluso nella replica della zona.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-113">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="7e2b7-114">Potrebbero essere presenti solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale).</span><span class="sxs-lookup"><span data-stu-id="7e2b7-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="7e2b7-115">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-115">The following values are valid.</span></span>



| <span data-ttu-id="7e2b7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="7e2b7-116">Value</span></span>                                                                                                                                               | <span data-ttu-id="7e2b7-117">Significato</span><span class="sxs-lookup"><span data-stu-id="7e2b7-117">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="7e2b7-118"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="7e2b7-118"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="7e2b7-119">Flag di replica</span><span class="sxs-lookup"><span data-stu-id="7e2b7-119">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="7e2b7-120"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="7e2b7-120"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="7e2b7-121">Flag senza replica (record locale)</span><span class="sxs-lookup"><span data-stu-id="7e2b7-121">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7e2b7-122">*LookupTimeout* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7e2b7-122">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7e2b7-123">Tempo, in secondi, durante il quale un server DNS tenta la risoluzione usando la ricerca di WINS.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-123">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="7e2b7-124">*CacheTimeout* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7e2b7-124">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7e2b7-125">Tempo, in secondi, per cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-125">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="7e2b7-126">*WinsServers* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7e2b7-126">*WinsServers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7e2b7-127">Elenco di indirizzi IP delimitati da virgole dei server WINS utilizzati nelle ricerche WINS.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-127">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="7e2b7-128">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="7e2b7-128">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7e2b7-129">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-129">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e2b7-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e2b7-130">Return value</span></span>

<span data-ttu-id="7e2b7-131">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e2b7-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e2b7-132">Remarks</span></span>

<span data-ttu-id="7e2b7-133">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-133">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e2b7-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e2b7-134">Requirements</span></span>



| <span data-ttu-id="7e2b7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e2b7-135">Requirement</span></span> | <span data-ttu-id="7e2b7-136">Valore</span><span class="sxs-lookup"><span data-stu-id="7e2b7-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e2b7-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e2b7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7e2b7-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7e2b7-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7e2b7-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e2b7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7e2b7-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7e2b7-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7e2b7-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7e2b7-141">Namespace</span></span><br/>                | <span data-ttu-id="7e2b7-142">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="7e2b7-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7e2b7-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7e2b7-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e2b7-144"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e2b7-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e2b7-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e2b7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e2b7-146">**\_WINSType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7e2b7-146">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="7e2b7-147">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WINSType**</span><span class="sxs-lookup"><span data-stu-id="7e2b7-147">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="7e2b7-148">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7e2b7-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





