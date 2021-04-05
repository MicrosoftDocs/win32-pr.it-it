---
title: Metodo Modify della classe MicrosoftDNS_MBType
description: Il metodo modify aggiorna un record di risorse della cassetta postale (MB).
ms.assetid: ee76031c-ac1b-4ebb-9fb2-3b64553867cc
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_MBType classe
- Classe MicrosoftDNS_MBType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135d6f0fcb0faf5c1e8da152798863c8cecc8641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741991"
---
# <a name="modify-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="745f4-106">Metodo Modify della \_ classe MBType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="745f4-106">Modify method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="745f4-107">Il metodo **Modify** aggiorna un record di risorse della cassetta postale (MB).</span><span class="sxs-lookup"><span data-stu-id="745f4-107">The **Modify** method updates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="745f4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="745f4-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MBHost,
  [out, ref]     MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="745f4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="745f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="745f4-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="745f4-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="745f4-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="745f4-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="745f4-112">*MBHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="745f4-112">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745f4-113">Stringa che rappresenta il nome host della cassetta postale per il record MB.</span><span class="sxs-lookup"><span data-stu-id="745f4-113">String representing the mailbox host name for the MB record.</span></span>

</dd> <dt>

<span data-ttu-id="745f4-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="745f4-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="745f4-115">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="745f4-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="745f4-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="745f4-116">Return value</span></span>

<span data-ttu-id="745f4-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="745f4-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="745f4-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="745f4-118">Remarks</span></span>

<span data-ttu-id="745f4-119">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="745f4-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="745f4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="745f4-120">Requirements</span></span>



| <span data-ttu-id="745f4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="745f4-121">Requirement</span></span> | <span data-ttu-id="745f4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="745f4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="745f4-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="745f4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="745f4-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="745f4-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="745f4-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="745f4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="745f4-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="745f4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="745f4-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="745f4-127">Namespace</span></span><br/>                | <span data-ttu-id="745f4-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="745f4-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="745f4-129">MOF</span><span class="sxs-lookup"><span data-stu-id="745f4-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="745f4-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="745f4-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="745f4-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="745f4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="745f4-132">**\_MBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="745f4-132">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="745f4-133">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="745f4-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="745f4-134">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="745f4-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





