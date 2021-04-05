---
title: Metodo Modify della classe MicrosoftDNS_WKSType
description: Il metodo modify aggiorna un record di risorse di Well-Known Services (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_WKSType classe
- Classe MicrosoftDNS_WKSType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874089"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="49170-106">Metodo Modify della \_ classe WKSType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="49170-106">Modify method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="49170-107">Il metodo **Modify** aggiorna un record di risorse di Well-Known Services (WKS).</span><span class="sxs-lookup"><span data-stu-id="49170-107">The **Modify** method updates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="49170-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49170-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="49170-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="49170-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49170-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="49170-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49170-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="49170-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="49170-112">*InternetAddress* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="49170-112">*InternetAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49170-113">Indirizzo IP Internet per il proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="49170-113">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="49170-114">*IPProtocol* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="49170-114">*IPProtocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49170-115">Stringa che rappresenta il protocollo IP per questo record.</span><span class="sxs-lookup"><span data-stu-id="49170-115">String representing the IP protocol for this record.</span></span> <span data-ttu-id="49170-116">I valori validi sono UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="49170-116">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="49170-117">*Servizi* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="49170-117">*Services* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49170-118">Stringa contenente tutti i servizi utilizzati dal record del servizio noto (WKS).</span><span class="sxs-lookup"><span data-stu-id="49170-118">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="49170-119">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="49170-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="49170-120">Riferimento al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="49170-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49170-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49170-121">Return value</span></span>

<span data-ttu-id="49170-122">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="49170-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49170-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="49170-123">Remarks</span></span>

<span data-ttu-id="49170-124">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="49170-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="49170-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49170-125">Requirements</span></span>



| <span data-ttu-id="49170-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="49170-126">Requirement</span></span> | <span data-ttu-id="49170-127">Valore</span><span class="sxs-lookup"><span data-stu-id="49170-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49170-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49170-128">Minimum supported client</span></span><br/> | <span data-ttu-id="49170-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="49170-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="49170-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49170-130">Minimum supported server</span></span><br/> | <span data-ttu-id="49170-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49170-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="49170-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="49170-132">Namespace</span></span><br/>                | <span data-ttu-id="49170-133">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="49170-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="49170-134">MOF</span><span class="sxs-lookup"><span data-stu-id="49170-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49170-135"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49170-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49170-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49170-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49170-137">**\_WKSType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="49170-137">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="49170-138">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="49170-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="49170-139">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="49170-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





