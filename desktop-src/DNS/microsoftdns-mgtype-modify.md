---
title: Metodo Modify della classe MicrosoftDNS_MGType
description: Il metodo modify aggiorna un record di risorse del gruppo di posta (MG).
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_MGType classe
- Classe MicrosoftDNS_MGType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706502569687a3c035c943e0a9dcc04aa1732492
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120475"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="ffb30-106">Metodo Modify della \_ classe MGType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ffb30-106">Modify method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="ffb30-107">Il metodo **Modify** aggiorna un record di risorse del gruppo di posta (mg).</span><span class="sxs-lookup"><span data-stu-id="ffb30-107">The **Modify** method updates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb30-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffb30-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ffb30-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffb30-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffb30-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ffb30-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb30-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="ffb30-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ffb30-112">*MGMailbox* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ffb30-112">*MGMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb30-113">FQDN che specifica una cassetta postale che è un membro del gruppo di posta elettronica specificato dal nome del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="ffb30-113">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="ffb30-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ffb30-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb30-115">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="ffb30-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffb30-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffb30-116">Return value</span></span>

<span data-ttu-id="ffb30-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ffb30-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffb30-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffb30-118">Remarks</span></span>

<span data-ttu-id="ffb30-119">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="ffb30-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffb30-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffb30-120">Requirements</span></span>



| <span data-ttu-id="ffb30-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffb30-121">Requirement</span></span> | <span data-ttu-id="ffb30-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ffb30-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb30-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffb30-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ffb30-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ffb30-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ffb30-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffb30-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ffb30-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ffb30-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ffb30-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ffb30-127">Namespace</span></span><br/>                | <span data-ttu-id="ffb30-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="ffb30-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ffb30-129">MOF</span><span class="sxs-lookup"><span data-stu-id="ffb30-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffb30-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffb30-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffb30-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffb30-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb30-132">**\_MGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ffb30-132">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="ffb30-133">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="ffb30-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ffb30-134">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ffb30-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





