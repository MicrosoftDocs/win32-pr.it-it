---
title: Metodo Modify della classe MicrosoftDNS_SRVType
description: Il metodo modify aggiorna un record di risorse del servizio (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_SRVType classe
- Classe MicrosoftDNS_SRVType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048695"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="deb50-106">Metodo Modify della \_ classe SRVType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="deb50-106">Modify method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="deb50-107">Il metodo **Modify** aggiorna un record di risorse del servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="deb50-107">The **Modify** method updates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb50-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="deb50-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="deb50-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="deb50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb50-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="deb50-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="deb50-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="deb50-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="deb50-112">*Priorità* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="deb50-112">*Priority* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="deb50-113">Priorità dell'host di destinazione specificato nel nome del proprietario.</span><span class="sxs-lookup"><span data-stu-id="deb50-113">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="deb50-114">I numeri più bassi implicano priorità più elevate.</span><span class="sxs-lookup"><span data-stu-id="deb50-114">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="deb50-115">*Peso* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="deb50-115">*Weight* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="deb50-116">Peso dell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="deb50-116">Weight of the target host.</span></span> <span data-ttu-id="deb50-117">Questa operazione è utile quando si seleziona tra gli host con la stessa priorità.</span><span class="sxs-lookup"><span data-stu-id="deb50-117">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="deb50-118">La possibilità di utilizzare questo host deve essere proporzionale al suo peso.</span><span class="sxs-lookup"><span data-stu-id="deb50-118">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="deb50-119">*Porta* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="deb50-119">*Port* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="deb50-120">Porta utilizzata nell'host di destinazione di un servizio del protocollo.</span><span class="sxs-lookup"><span data-stu-id="deb50-120">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="deb50-121">*SRVDomainName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="deb50-121">*SRVDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="deb50-122">FQDN dell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="deb50-122">FQDN of the target host.</span></span> <span data-ttu-id="deb50-123">Destinazione di \\ . \\ indica che il servizio non è disponibile in questo dominio.</span><span class="sxs-lookup"><span data-stu-id="deb50-123">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="deb50-124">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="deb50-124">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="deb50-125">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="deb50-125">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb50-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="deb50-126">Return value</span></span>

<span data-ttu-id="deb50-127">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="deb50-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="deb50-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="deb50-128">Remarks</span></span>

<span data-ttu-id="deb50-129">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="deb50-129">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="deb50-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="deb50-130">Requirements</span></span>



| <span data-ttu-id="deb50-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="deb50-131">Requirement</span></span> | <span data-ttu-id="deb50-132">Valore</span><span class="sxs-lookup"><span data-stu-id="deb50-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="deb50-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="deb50-133">Minimum supported client</span></span><br/> | <span data-ttu-id="deb50-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="deb50-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="deb50-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="deb50-135">Minimum supported server</span></span><br/> | <span data-ttu-id="deb50-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="deb50-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="deb50-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="deb50-137">Namespace</span></span><br/>                | <span data-ttu-id="deb50-138">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="deb50-138">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="deb50-139">MOF</span><span class="sxs-lookup"><span data-stu-id="deb50-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="deb50-140"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="deb50-140"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deb50-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="deb50-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb50-142">**\_SRVType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="deb50-142">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="deb50-143">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="deb50-143">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="deb50-144">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="deb50-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





