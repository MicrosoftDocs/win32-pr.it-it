---
title: Metodo Modify della classe MicrosoftDNS_HINFOType
description: Il metodo modify aggiorna un record di risorse host Information (HINFO).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_HINFOType classe
- Classe MicrosoftDNS_HINFOType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29a01eb94d82d080142d3496bab5f7f0b9acac8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741546"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="2de71-106">Metodo Modify della \_ classe HINFOType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="2de71-106">Modify method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="2de71-107">Il metodo **Modify** aggiorna un record di risorse host Information (HINFO).</span><span class="sxs-lookup"><span data-stu-id="2de71-107">The **Modify** method updates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de71-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2de71-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="2de71-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2de71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2de71-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2de71-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2de71-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="2de71-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="2de71-112">*CPU* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2de71-112">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2de71-113">Tipo di CPU del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="2de71-113">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="2de71-114">*Sistema operativo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2de71-114">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2de71-115">Sistema operativo del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="2de71-115">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="2de71-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="2de71-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2de71-117">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="2de71-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2de71-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2de71-118">Return value</span></span>

<span data-ttu-id="2de71-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2de71-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2de71-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="2de71-120">Remarks</span></span>

<span data-ttu-id="2de71-121">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="2de71-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="2de71-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2de71-122">Requirements</span></span>



| <span data-ttu-id="2de71-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2de71-123">Requirement</span></span> | <span data-ttu-id="2de71-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2de71-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2de71-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2de71-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2de71-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2de71-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2de71-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2de71-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2de71-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2de71-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2de71-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2de71-129">Namespace</span></span><br/>                | <span data-ttu-id="2de71-130">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="2de71-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2de71-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2de71-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2de71-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2de71-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2de71-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2de71-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de71-134">**\_HINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="2de71-134">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="2de71-135">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="2de71-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="2de71-136">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="2de71-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





