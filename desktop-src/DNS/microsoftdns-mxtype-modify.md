---
title: Metodo Modify della classe MicrosoftDNS_MXType
description: Il metodo modify aggiorna un record di risorse di Mail Exchanger (Sig.).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_MXType classe
- Classe MicrosoftDNS_MXType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a665d0673e048eff684b4c985b54a1c57e030a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964895"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="029f6-106">Metodo Modify della \_ classe MXType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="029f6-106">Modify method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="029f6-107">Il metodo **Modify** aggiorna un record di risorse di Mail Exchanger (Sig.).</span><span class="sxs-lookup"><span data-stu-id="029f6-107">The **Modify** method updates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="029f6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="029f6-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="029f6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="029f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="029f6-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="029f6-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="029f6-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="029f6-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="029f6-112">*Preferenza* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="029f6-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="029f6-113">Preferenza assegnata a questo RR tra gli altri nello stesso proprietario.</span><span class="sxs-lookup"><span data-stu-id="029f6-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="029f6-114">Sono preferibili valori inferiori.</span><span class="sxs-lookup"><span data-stu-id="029f6-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="029f6-115">*MailExchange* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="029f6-115">*MailExchange* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="029f6-116">FQDN che specifica un host disposto a fungere da scambio di posta elettronica per il nome del proprietario.</span><span class="sxs-lookup"><span data-stu-id="029f6-116">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="029f6-117">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="029f6-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="029f6-118">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="029f6-118">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="029f6-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="029f6-119">Return value</span></span>

<span data-ttu-id="029f6-120">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="029f6-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="029f6-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="029f6-121">Remarks</span></span>

<span data-ttu-id="029f6-122">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="029f6-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="029f6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="029f6-123">Requirements</span></span>



| <span data-ttu-id="029f6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="029f6-124">Requirement</span></span> | <span data-ttu-id="029f6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="029f6-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="029f6-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="029f6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="029f6-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="029f6-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="029f6-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="029f6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="029f6-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="029f6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="029f6-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="029f6-130">Namespace</span></span><br/>                | <span data-ttu-id="029f6-131">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="029f6-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="029f6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="029f6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="029f6-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="029f6-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="029f6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="029f6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029f6-135">**\_MXType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="029f6-135">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="029f6-136">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="029f6-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="029f6-137">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="029f6-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





