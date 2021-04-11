---
title: Metodo Modify della classe MicrosoftDNS_MDType
description: Il metodo modify aggiorna un record di risorse di un agente di posta elettronica per il dominio (MD).
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_MDType classe
- Classe MicrosoftDNS_MDType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ed5e3a8d7f819447d256ba3bce31f4eaa6986a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119715"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a><span data-ttu-id="fc1d9-106">Metodo Modify della \_ classe MDType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="fc1d9-106">Modify method of the MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="fc1d9-107">Il metodo **Modify** aggiorna un record di risorse di un agente di posta elettronica per il dominio (MD).</span><span class="sxs-lookup"><span data-stu-id="fc1d9-107">The **Modify** method updates a Mail Agent for Domain (MD) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc1d9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc1d9-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="fc1d9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc1d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc1d9-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fc1d9-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fc1d9-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="fc1d9-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="fc1d9-112">*MDHost* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fc1d9-112">*MDHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fc1d9-113">Stringa che rappresenta l'host di recapito della posta.</span><span class="sxs-lookup"><span data-stu-id="fc1d9-113">String representing the mail delivery host.</span></span>

</dd> <dt>

<span data-ttu-id="fc1d9-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="fc1d9-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="fc1d9-115">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="fc1d9-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc1d9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc1d9-116">Return value</span></span>

<span data-ttu-id="fc1d9-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fc1d9-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc1d9-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc1d9-118">Remarks</span></span>

<span data-ttu-id="fc1d9-119">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="fc1d9-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc1d9-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc1d9-120">Requirements</span></span>



| <span data-ttu-id="fc1d9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc1d9-121">Requirement</span></span> | <span data-ttu-id="fc1d9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fc1d9-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1d9-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc1d9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fc1d9-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fc1d9-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fc1d9-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc1d9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fc1d9-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fc1d9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fc1d9-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fc1d9-127">Namespace</span></span><br/>                | <span data-ttu-id="fc1d9-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="fc1d9-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fc1d9-129">MOF</span><span class="sxs-lookup"><span data-stu-id="fc1d9-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc1d9-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc1d9-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc1d9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc1d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc1d9-132">**\_MDType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="fc1d9-132">**MicrosoftDNS\_MDType**</span></span>](microsoftdns-mdtype.md)
</dt> <dt>

[<span data-ttu-id="fc1d9-133">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MDType**</span><span class="sxs-lookup"><span data-stu-id="fc1d9-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fc1d9-134">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="fc1d9-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





