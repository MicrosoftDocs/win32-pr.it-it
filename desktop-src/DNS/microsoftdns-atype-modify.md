---
title: Metodo Modify della classe MicrosoftDNS_AType
description: Il metodo modify aggiorna la durata (TTL) e l'indirizzo IP di un record di risorse di indirizzo host (A).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_AType classe
- Classe MicrosoftDNS_AType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffda093ed843cfd655711100321c9876120519c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048375"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="4b9b6-106">Metodo Modify della \_ classe aType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="4b9b6-106">Modify method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="4b9b6-107">Il metodo **Modify** aggiorna la durata (TTL) e l'indirizzo IP di un record di risorse di indirizzo host (a).</span><span class="sxs-lookup"><span data-stu-id="4b9b6-107">The **Modify** method updates the TTL and IP address of a host Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b9b6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b9b6-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4b9b6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b9b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b9b6-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4b9b6-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9b6-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="4b9b6-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="4b9b6-112">*Indirizzo IP* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4b9b6-112">*IPAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9b6-113">Stringa che rappresenta l'indirizzo IP dell'host.</span><span class="sxs-lookup"><span data-stu-id="4b9b6-113">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="4b9b6-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="4b9b6-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9b6-115">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="4b9b6-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b9b6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b9b6-116">Return value</span></span>

<span data-ttu-id="4b9b6-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4b9b6-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b9b6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b9b6-118">Remarks</span></span>

<span data-ttu-id="4b9b6-119">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="4b9b6-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b9b6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b9b6-120">Requirements</span></span>



| <span data-ttu-id="4b9b6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b9b6-121">Requirement</span></span> | <span data-ttu-id="4b9b6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4b9b6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9b6-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b9b6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4b9b6-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4b9b6-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4b9b6-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b9b6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4b9b6-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b9b6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4b9b6-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4b9b6-127">Namespace</span></span><br/>                | <span data-ttu-id="4b9b6-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="4b9b6-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4b9b6-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4b9b6-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b9b6-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b9b6-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b9b6-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b9b6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b9b6-132">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4b9b6-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="4b9b6-133">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ aType**</span><span class="sxs-lookup"><span data-stu-id="4b9b6-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





