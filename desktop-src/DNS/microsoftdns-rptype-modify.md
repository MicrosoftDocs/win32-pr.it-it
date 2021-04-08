---
title: Metodo Modify della classe MicrosoftDNS_RPType
description: Il metodo modify aggiorna un record di risorse responsabile (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_RPType classe
- Classe MicrosoftDNS_RPType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ec575424e6e26c79f8d6a27e62732cad6ddc57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873994"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="06b98-106">Metodo Modify della \_ classe RPType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="06b98-106">Modify method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="06b98-107">Il metodo **Modify** aggiorna un record di risorse responsabile (RP).</span><span class="sxs-lookup"><span data-stu-id="06b98-107">The **Modify** method updates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b98-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06b98-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="06b98-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="06b98-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06b98-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06b98-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06b98-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="06b98-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="06b98-112">*RPMailbox* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06b98-112">*RPMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06b98-113">FQDN che specifica la cassetta postale per la persona responsabile.</span><span class="sxs-lookup"><span data-stu-id="06b98-113">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="06b98-114">*TXTDomainName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="06b98-114">*TXTDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06b98-115">FQDN per cui sono presenti record di risorse TXT.</span><span class="sxs-lookup"><span data-stu-id="06b98-115">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="06b98-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="06b98-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="06b98-117">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="06b98-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06b98-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06b98-118">Return value</span></span>

<span data-ttu-id="06b98-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="06b98-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06b98-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="06b98-120">Remarks</span></span>

<span data-ttu-id="06b98-121">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="06b98-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b98-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06b98-122">Requirements</span></span>



| <span data-ttu-id="06b98-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="06b98-123">Requirement</span></span> | <span data-ttu-id="06b98-124">Valore</span><span class="sxs-lookup"><span data-stu-id="06b98-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06b98-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06b98-125">Minimum supported client</span></span><br/> | <span data-ttu-id="06b98-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="06b98-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="06b98-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06b98-127">Minimum supported server</span></span><br/> | <span data-ttu-id="06b98-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="06b98-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="06b98-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06b98-129">Namespace</span></span><br/>                | <span data-ttu-id="06b98-130">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="06b98-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="06b98-131">MOF</span><span class="sxs-lookup"><span data-stu-id="06b98-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06b98-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06b98-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06b98-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06b98-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b98-134">**\_RPType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="06b98-134">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="06b98-135">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="06b98-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="06b98-136">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="06b98-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





