---
title: Metodo Modify della classe MicrosoftDNS_NXTType
description: Il metodo modify aggiorna un record di risorse successivo (NXT).
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_NXTType classe
- Classe MicrosoftDNS_NXTType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bab7bf8480c7e18914cac4f7ae0deb8a608090f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475880"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="af062-106">Metodo Modify della \_ classe NXTType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="af062-106">Modify method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="af062-107">Il metodo **Modify** aggiorna un record di risorse successivo (NXT).</span><span class="sxs-lookup"><span data-stu-id="af062-107">The **Modify** method updates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="af062-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af062-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="af062-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="af062-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af062-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="af062-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="af062-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="af062-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="af062-112">*NextDomainName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af062-112">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af062-113">Nome di dominio successivo.</span><span class="sxs-lookup"><span data-stu-id="af062-113">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="af062-114">*Tipi* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="af062-114">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af062-115">Elenco separato da spazi dei tasti di scelta del tipo RR per il nome del proprietario del record di risorse NXT.</span><span class="sxs-lookup"><span data-stu-id="af062-115">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="af062-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="af062-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="af062-117">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="af062-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af062-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af062-118">Return value</span></span>

<span data-ttu-id="af062-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="af062-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af062-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="af062-120">Remarks</span></span>

<span data-ttu-id="af062-121">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="af062-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="af062-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af062-122">Requirements</span></span>



| <span data-ttu-id="af062-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="af062-123">Requirement</span></span> | <span data-ttu-id="af062-124">Valore</span><span class="sxs-lookup"><span data-stu-id="af062-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af062-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af062-125">Minimum supported client</span></span><br/> | <span data-ttu-id="af062-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="af062-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="af062-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af062-127">Minimum supported server</span></span><br/> | <span data-ttu-id="af062-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="af062-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="af062-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af062-129">Namespace</span></span><br/>                | <span data-ttu-id="af062-130">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="af062-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="af062-131">MOF</span><span class="sxs-lookup"><span data-stu-id="af062-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af062-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af062-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af062-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af062-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af062-134">**\_NXTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="af062-134">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="af062-135">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="af062-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="af062-136">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="af062-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





