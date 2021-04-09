---
title: Metodo Modify della classe MicrosoftDNS_PTRType
description: Il metodo modify aggiorna un record di risorse puntatore (PTR).
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_PTRType classe
- Classe MicrosoftDNS_PTRType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 840bf100ea5cdbbb606837e90d8fa9fcebab57fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964375"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a><span data-ttu-id="527a4-106">Metodo Modify della \_ classe PTRType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="527a4-106">Modify method of the MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="527a4-107">Il metodo **Modify** aggiorna un record di risorse puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="527a4-107">The **Modify** method updates a Pointer (PTR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="527a4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="527a4-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="527a4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="527a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="527a4-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="527a4-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="527a4-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="527a4-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="527a4-112">*PTRDomainName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="527a4-112">*PTRDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="527a4-113">Indirizzo del nome di dominio del record PTR.</span><span class="sxs-lookup"><span data-stu-id="527a4-113">Domain name address of the PTR record.</span></span>

</dd> <dt>

<span data-ttu-id="527a4-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="527a4-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="527a4-115">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="527a4-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="527a4-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="527a4-116">Return value</span></span>

<span data-ttu-id="527a4-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="527a4-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="527a4-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="527a4-118">Remarks</span></span>

<span data-ttu-id="527a4-119">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="527a4-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="527a4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="527a4-120">Requirements</span></span>



| <span data-ttu-id="527a4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="527a4-121">Requirement</span></span> | <span data-ttu-id="527a4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="527a4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="527a4-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="527a4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="527a4-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="527a4-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="527a4-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="527a4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="527a4-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="527a4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="527a4-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="527a4-127">Namespace</span></span><br/>                | <span data-ttu-id="527a4-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="527a4-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="527a4-129">MOF</span><span class="sxs-lookup"><span data-stu-id="527a4-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="527a4-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="527a4-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="527a4-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="527a4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="527a4-132">**\_PTRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="527a4-132">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="527a4-133">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="527a4-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="527a4-134">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="527a4-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





