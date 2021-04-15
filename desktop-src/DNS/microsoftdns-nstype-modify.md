---
title: Metodo Modify della classe MicrosoftDNS_NSType
description: Il metodo modify aggiorna un record di risorse del server dei nomi (NS).
ms.assetid: da625231-cf4e-4526-b713-737e6b9f5831
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_NSType classe
- Classe MicrosoftDNS_NSType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3dd26b7c0f1c31ef3ea742f20f70df8646a087b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479402"
---
# <a name="modify-method-of-the-microsoftdns_nstype-class"></a><span data-ttu-id="43533-106">Metodo Modify della \_ classe NSType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="43533-106">Modify method of the MicrosoftDNS\_NSType class</span></span>

<span data-ttu-id="43533-107">Il metodo **Modify** aggiorna un record di risorse del server dei nomi (NS).</span><span class="sxs-lookup"><span data-stu-id="43533-107">The **Modify** method updates a Name Server (NS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="43533-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43533-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              NSHost,
  [out, ref]     MicrosoftDNS_NSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="43533-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="43533-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43533-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="43533-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43533-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="43533-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="43533-112">*NSHost* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="43533-112">*NSHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43533-113">Host autorevole per il dominio.</span><span class="sxs-lookup"><span data-stu-id="43533-113">Authoritative host for the domain.</span></span>

</dd> <dt>

<span data-ttu-id="43533-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="43533-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="43533-115">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="43533-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43533-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43533-116">Return value</span></span>

<span data-ttu-id="43533-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="43533-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43533-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="43533-118">Remarks</span></span>

<span data-ttu-id="43533-119">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="43533-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="43533-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43533-120">Requirements</span></span>



| <span data-ttu-id="43533-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="43533-121">Requirement</span></span> | <span data-ttu-id="43533-122">Valore</span><span class="sxs-lookup"><span data-stu-id="43533-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43533-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43533-123">Minimum supported client</span></span><br/> | <span data-ttu-id="43533-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="43533-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="43533-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43533-125">Minimum supported server</span></span><br/> | <span data-ttu-id="43533-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="43533-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="43533-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43533-127">Namespace</span></span><br/>                | <span data-ttu-id="43533-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="43533-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="43533-129">MOF</span><span class="sxs-lookup"><span data-stu-id="43533-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43533-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43533-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43533-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43533-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43533-132">**\_PTRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="43533-132">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="43533-133">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="43533-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="43533-134">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="43533-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





