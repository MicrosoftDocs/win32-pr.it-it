---
title: Metodo Modify della classe MicrosoftDNS_RTType
description: Il metodo modify aggiorna una route tramite un record di risorse (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_RTType classe
- Classe MicrosoftDNS_RTType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8267bf1dc256ec95a456978643226ab5c01af93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517938"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="c956c-106">Metodo Modify della \_ classe RTType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c956c-106">Modify method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="c956c-107">Il metodo **Modify** aggiorna una route tramite un record di risorse (RT).</span><span class="sxs-lookup"><span data-stu-id="c956c-107">The **Modify** method updates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c956c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c956c-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c956c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c956c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c956c-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c956c-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c956c-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="c956c-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c956c-112">*Preferenza* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c956c-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c956c-113">Preferenza assegnata a questo RR tra gli altri nello stesso proprietario.</span><span class="sxs-lookup"><span data-stu-id="c956c-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="c956c-114">Sono preferibili valori inferiori.</span><span class="sxs-lookup"><span data-stu-id="c956c-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="c956c-115">*IntermediateHost* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c956c-115">*IntermediateHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c956c-116">FQDN che specifica un host che funge da intermediario per raggiungere l'host specificato dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="c956c-116">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="c956c-117">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c956c-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c956c-118">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c956c-118">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c956c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c956c-119">Return value</span></span>

<span data-ttu-id="c956c-120">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c956c-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c956c-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="c956c-121">Remarks</span></span>

<span data-ttu-id="c956c-122">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="c956c-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="c956c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c956c-123">Requirements</span></span>



| <span data-ttu-id="c956c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c956c-124">Requirement</span></span> | <span data-ttu-id="c956c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c956c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c956c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c956c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c956c-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c956c-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c956c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c956c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c956c-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c956c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c956c-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c956c-130">Namespace</span></span><br/>                | <span data-ttu-id="c956c-131">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="c956c-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c956c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c956c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c956c-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c956c-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c956c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c956c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c956c-135">**\_RTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c956c-135">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="c956c-136">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="c956c-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c956c-137">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c956c-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





