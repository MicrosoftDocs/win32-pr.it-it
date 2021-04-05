---
title: Metodo Modify della classe MicrosoftDNS_AAAAType
description: Il metodo modify aggiorna un record di risorse di indirizzo IPv6 (AAAA).
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_AAAAType classe
- Classe MicrosoftDNS_AAAAType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc216233fe3d41e4f1e31fe0d471e766c4dc8476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873825"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="6a14a-106">Metodo Modify della \_ classe AAAAType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="6a14a-106">Modify method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="6a14a-107">Il metodo **Modify** aggiorna un record di risorse di indirizzo IPv6 (aaaa).</span><span class="sxs-lookup"><span data-stu-id="6a14a-107">The **Modify** method updates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a14a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a14a-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="6a14a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a14a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a14a-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6a14a-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a14a-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="6a14a-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="6a14a-112">*IPV6Address* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6a14a-112">*IPv6Address* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a14a-113">Indirizzo IPv6 per l'host.</span><span class="sxs-lookup"><span data-stu-id="6a14a-113">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="6a14a-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="6a14a-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6a14a-115">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="6a14a-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a14a-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a14a-116">Return value</span></span>

<span data-ttu-id="6a14a-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6a14a-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a14a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a14a-118">Remarks</span></span>

<span data-ttu-id="6a14a-119">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="6a14a-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a14a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a14a-120">Requirements</span></span>



| <span data-ttu-id="6a14a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a14a-121">Requirement</span></span> | <span data-ttu-id="6a14a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6a14a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a14a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a14a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6a14a-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6a14a-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6a14a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a14a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6a14a-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6a14a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6a14a-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a14a-127">Namespace</span></span><br/>                | <span data-ttu-id="6a14a-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="6a14a-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6a14a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="6a14a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a14a-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a14a-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a14a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a14a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a14a-132">**\_AAAAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6a14a-132">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="6a14a-133">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ AAAAType**</span><span class="sxs-lookup"><span data-stu-id="6a14a-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6a14a-134">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6a14a-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





