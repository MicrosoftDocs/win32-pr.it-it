---
title: Metodo CreateInstanceFromTextRepresentation della classe MicrosoftDNS_ResourceRecord
description: Il metodo CreateInstanceFromTextRepresentation crea un'istanza di un \_ oggetto ResourceRecord MicrosoftDNS.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- DNS del metodo CreateInstanceFromTextRepresentation
- DNS del metodo CreateInstanceFromTextRepresentation, classe MicrosoftDNS_ResourceRecord
- Classe MicrosoftDNS_ResourceRecord DNS, metodo CreateInstanceFromTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a578d036180ecb1dc8a5e66bf853eec8845583f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048473"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="4a944-106">Metodo CreateInstanceFromTextRepresentation della classe MicrosoftDNS \_ ResourceRecord</span><span class="sxs-lookup"><span data-stu-id="4a944-106">CreateInstanceFromTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="4a944-107">Il metodo **CreateInstanceFromTextRepresentation** crea un'istanza di un oggetto [**\_ ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="4a944-107">The **CreateInstanceFromTextRepresentation** method instantiates a [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a944-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a944-108">Syntax</span></span>


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4a944-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a944-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a944-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a944-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a944-111">Nome del server DNS in cui deve essere creato l'RR.</span><span class="sxs-lookup"><span data-stu-id="4a944-111">Name of the DNS Server on which the RR should be created.</span></span>

</dd> <dt>

<span data-ttu-id="4a944-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a944-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a944-113">Nome del contenitore in cui deve essere inserito il nuovo RR.</span><span class="sxs-lookup"><span data-stu-id="4a944-113">Name of the container into which the new RR should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="4a944-114">*TextRepresentation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a944-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a944-115">Rappresentazione testo dell'istanza di RR da creare.</span><span class="sxs-lookup"><span data-stu-id="4a944-115">Text representation of the RR instance to be created.</span></span>

</dd> <dt>

<span data-ttu-id="4a944-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="4a944-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4a944-117">Riferimento all'RR di cui è stata creata un'istanza.</span><span class="sxs-lookup"><span data-stu-id="4a944-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a944-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a944-118">Return value</span></span>

<span data-ttu-id="4a944-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4a944-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a944-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a944-120">Requirements</span></span>



| <span data-ttu-id="4a944-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a944-121">Requirement</span></span> | <span data-ttu-id="4a944-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4a944-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a944-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a944-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4a944-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4a944-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4a944-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a944-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4a944-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4a944-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4a944-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4a944-127">Namespace</span></span><br/>                | <span data-ttu-id="4a944-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="4a944-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4a944-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4a944-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a944-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a944-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a944-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a944-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a944-132">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4a944-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="4a944-133">**Metodo GetObjectByTextRepresentation della classe MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="4a944-133">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





