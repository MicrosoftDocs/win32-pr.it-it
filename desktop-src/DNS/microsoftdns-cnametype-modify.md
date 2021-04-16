---
title: Metodo Modify della classe MicrosoftDNS_CNAMEType
description: Il metodo modify aggiorna un record di risorse di nome canonico (CNAME).
ms.assetid: 7e550026-d901-44a0-86ac-520682232ccb
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_CNAMEType classe
- Classe MicrosoftDNS_CNAMEType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ddbe1e1592c4331be808340c216954cd8d7b14f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476762"
---
# <a name="modify-method-of-the-microsoftdns_cnametype-class"></a><span data-ttu-id="a07f3-106">Metodo Modify della \_ classe CNAMEType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="a07f3-106">Modify method of the MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="a07f3-107">Il metodo **Modify** aggiorna un record di risorse di nome canonico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="a07f3-107">The **Modify** method updates a Canonical Name (CNAME) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a07f3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a07f3-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="a07f3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a07f3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a07f3-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a07f3-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a07f3-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="a07f3-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="a07f3-112">*PrimaryName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a07f3-112">*PrimaryName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a07f3-113">Stringa che rappresenta il nome primario per il record CNAME.</span><span class="sxs-lookup"><span data-stu-id="a07f3-113">String representing the primary name for the CNAME record.</span></span>

</dd> <dt>

<span data-ttu-id="a07f3-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="a07f3-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a07f3-115">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="a07f3-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a07f3-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a07f3-116">Return value</span></span>

<span data-ttu-id="a07f3-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a07f3-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a07f3-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a07f3-118">Remarks</span></span>

<span data-ttu-id="a07f3-119">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="a07f3-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="a07f3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a07f3-120">Requirements</span></span>



| <span data-ttu-id="a07f3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a07f3-121">Requirement</span></span> | <span data-ttu-id="a07f3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a07f3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a07f3-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a07f3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a07f3-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a07f3-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a07f3-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a07f3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a07f3-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a07f3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a07f3-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a07f3-127">Namespace</span></span><br/>                | <span data-ttu-id="a07f3-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="a07f3-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a07f3-129">MOF</span><span class="sxs-lookup"><span data-stu-id="a07f3-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a07f3-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a07f3-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a07f3-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a07f3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a07f3-132">**\_CNAMEType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a07f3-132">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md)
</dt> <dt>

[<span data-ttu-id="a07f3-133">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="a07f3-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a07f3-134">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a07f3-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





