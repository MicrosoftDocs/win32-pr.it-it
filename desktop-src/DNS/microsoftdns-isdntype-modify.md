---
title: Metodo Modify della classe MicrosoftDNS_ISDNType
description: Il metodo modify aggiorna un record di risorse ISDN.
ms.assetid: 09e23853-ca92-43a3-8bd9-7de10eb5eddc
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_ISDNType classe
- Classe MicrosoftDNS_ISDNType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c369a6650c834ff9f35af6389c346daec86a954
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963787"
---
# <a name="modify-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="88bfd-106">Metodo Modify della \_ classe ISDNType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="88bfd-106">Modify method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="88bfd-107">Il metodo **Modify** aggiorna un record di risorse ISDN.</span><span class="sxs-lookup"><span data-stu-id="88bfd-107">The **Modify** method updates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="88bfd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88bfd-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                ISDNNumber,
  [in, optional] string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="88bfd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="88bfd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88bfd-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="88bfd-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88bfd-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="88bfd-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="88bfd-112">*ISDNNumber* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="88bfd-112">*ISDNNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88bfd-113">Numero ISDN e DDI del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="88bfd-113">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="88bfd-114">*Sottoindirizzo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="88bfd-114">*SubAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88bfd-115">Sottoindirizzo del proprietario, se definito.</span><span class="sxs-lookup"><span data-stu-id="88bfd-115">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="88bfd-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="88bfd-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="88bfd-117">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="88bfd-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88bfd-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88bfd-118">Return value</span></span>

<span data-ttu-id="88bfd-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="88bfd-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88bfd-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="88bfd-120">Remarks</span></span>

<span data-ttu-id="88bfd-121">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="88bfd-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="88bfd-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88bfd-122">Requirements</span></span>



| <span data-ttu-id="88bfd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="88bfd-123">Requirement</span></span> | <span data-ttu-id="88bfd-124">Valore</span><span class="sxs-lookup"><span data-stu-id="88bfd-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88bfd-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88bfd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="88bfd-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="88bfd-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="88bfd-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88bfd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="88bfd-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="88bfd-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="88bfd-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88bfd-129">Namespace</span></span><br/>                | <span data-ttu-id="88bfd-130">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="88bfd-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="88bfd-131">MOF</span><span class="sxs-lookup"><span data-stu-id="88bfd-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88bfd-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88bfd-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88bfd-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88bfd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88bfd-134">**\_ISDNType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="88bfd-134">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="88bfd-135">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ ISDNType**</span><span class="sxs-lookup"><span data-stu-id="88bfd-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="88bfd-136">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="88bfd-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





