---
title: Metodo Modify della classe MicrosoftDNS_MRType
description: Il metodo modify aggiorna un record di risorse di ridenominazione delle cassette postali.
ms.assetid: eb833735-d485-4603-9976-305244537acd
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_MRType classe
- Classe MicrosoftDNS_MRType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996692301e8446b3fd67e20eca036cd085e83b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476594"
---
# <a name="modify-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="e2b19-106">Metodo Modify della \_ classe MRType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="e2b19-106">Modify method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="e2b19-107">Il metodo **Modify** aggiorna un record di risorse di ridenominazione delle cassette postali.</span><span class="sxs-lookup"><span data-stu-id="e2b19-107">The **Modify** method updates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b19-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2b19-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e2b19-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2b19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2b19-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e2b19-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b19-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="e2b19-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e2b19-112">*MRMailbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2b19-112">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b19-113">FQDN che specifica una cassetta postale che è la ridenominazione corretta della cassetta postale specificata nel nome del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="e2b19-113">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="e2b19-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e2b19-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b19-115">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="e2b19-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2b19-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2b19-116">Return value</span></span>

<span data-ttu-id="e2b19-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e2b19-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2b19-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2b19-118">Remarks</span></span>

<span data-ttu-id="e2b19-119">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="e2b19-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b19-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2b19-120">Requirements</span></span>



| <span data-ttu-id="e2b19-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2b19-121">Requirement</span></span> | <span data-ttu-id="e2b19-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e2b19-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b19-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2b19-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b19-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e2b19-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e2b19-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2b19-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b19-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e2b19-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e2b19-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e2b19-127">Namespace</span></span><br/>                | <span data-ttu-id="e2b19-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="e2b19-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e2b19-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e2b19-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2b19-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2b19-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b19-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2b19-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b19-132">**\_MRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e2b19-132">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="e2b19-133">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="e2b19-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e2b19-134">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e2b19-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





