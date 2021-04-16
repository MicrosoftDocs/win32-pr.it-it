---
title: Metodo Modify della classe MicrosoftDNS_MFType
description: Il metodo modify aggiorna un record di risorse dell'agente di invio della posta elettronica per il dominio (MF).
ms.assetid: b4bc43a5-6f43-487d-ad6c-3e01d5b2b6b8
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_MFType classe
- Classe MicrosoftDNS_MFType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0a363290580c7cecf47dbe00c6dd7895d23dbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477842"
---
# <a name="modify-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="d2c90-106">Metodo Modify della \_ classe MFType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="d2c90-106">Modify method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="d2c90-107">Il metodo **Modify** aggiorna un record di risorse dell'agente di invio della posta elettronica per il dominio (MF).</span><span class="sxs-lookup"><span data-stu-id="d2c90-107">The **Modify** method updates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c90-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2c90-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d2c90-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2c90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2c90-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="d2c90-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c90-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="d2c90-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d2c90-112">*MFHost* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="d2c90-112">*MFHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c90-113">Nome dell'host che fornisce l'agente di invio della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="d2c90-113">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="d2c90-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="d2c90-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c90-115">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="d2c90-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2c90-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2c90-116">Return value</span></span>

<span data-ttu-id="d2c90-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d2c90-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2c90-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2c90-118">Remarks</span></span>

<span data-ttu-id="d2c90-119">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="d2c90-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2c90-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2c90-120">Requirements</span></span>



| <span data-ttu-id="d2c90-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2c90-121">Requirement</span></span> | <span data-ttu-id="d2c90-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d2c90-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c90-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2c90-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c90-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d2c90-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d2c90-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2c90-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c90-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2c90-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d2c90-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2c90-127">Namespace</span></span><br/>                | <span data-ttu-id="d2c90-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="d2c90-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d2c90-129">MOF</span><span class="sxs-lookup"><span data-stu-id="d2c90-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2c90-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2c90-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2c90-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2c90-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2c90-132">**\_MFType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d2c90-132">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="d2c90-133">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="d2c90-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d2c90-134">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d2c90-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





