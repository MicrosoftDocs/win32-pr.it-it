---
title: Metodo Modify della classe MicrosoftDNS_MINFOType
description: Il metodo modify aggiorna un record di risorse MINFO (mail Information).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_MINFOType classe
- Classe MicrosoftDNS_MINFOType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b59d7d1231ed88e61a0ecf94cef50041ca772f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475881"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="e5714-106">Metodo Modify della \_ classe MINFOType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="e5714-106">Modify method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="e5714-107">Il metodo **Modify** aggiorna un record di risorse MINFO (mail Information).</span><span class="sxs-lookup"><span data-stu-id="e5714-107">The **Modify** method updates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5714-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5714-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e5714-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5714-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5714-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e5714-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5714-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="e5714-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e5714-112">*ResponsibleMailbox* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e5714-112">*ResponsibleMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5714-113">FQDN che specifica una cassetta postale responsabile della lista di distribuzione o della cassetta postale specificata nel nome del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="e5714-113">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="e5714-114">*ErrorMailbox* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e5714-114">*ErrorMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5714-115">FQDN che specifica una cassetta postale per ricevere i messaggi di errore correlati alla lista di distribuzione o alla cassetta postale specificata dal nome del proprietario del record MINFO.</span><span class="sxs-lookup"><span data-stu-id="e5714-115">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="e5714-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e5714-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e5714-117">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="e5714-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5714-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5714-118">Return value</span></span>

<span data-ttu-id="e5714-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e5714-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5714-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5714-120">Remarks</span></span>

<span data-ttu-id="e5714-121">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="e5714-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5714-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5714-122">Requirements</span></span>



| <span data-ttu-id="e5714-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5714-123">Requirement</span></span> | <span data-ttu-id="e5714-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e5714-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5714-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5714-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e5714-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e5714-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e5714-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5714-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e5714-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e5714-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e5714-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e5714-129">Namespace</span></span><br/>                | <span data-ttu-id="e5714-130">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="e5714-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e5714-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e5714-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5714-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5714-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5714-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5714-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5714-134">**\_MINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e5714-134">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="e5714-135">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="e5714-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e5714-136">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e5714-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





