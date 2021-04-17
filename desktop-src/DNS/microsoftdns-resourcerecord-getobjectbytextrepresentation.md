---
title: Metodo GetObjectByTextRepresentation della classe MicrosoftDNS_ResourceRecord
description: Il metodo GetObjectByTextRepresentation recupera un'istanza esistente della \_ classe ResourceRecord di MicrosoftDNS.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- DNS del metodo GetObjectByTextRepresentation
- DNS del metodo GetObjectByTextRepresentation, classe MicrosoftDNS_ResourceRecord
- Classe MicrosoftDNS_ResourceRecord DNS, metodo GetObjectByTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477278"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="780e7-106">Metodo GetObjectByTextRepresentation della classe MicrosoftDNS \_ ResourceRecord</span><span class="sxs-lookup"><span data-stu-id="780e7-106">GetObjectByTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="780e7-107">Il metodo **GetObjectByTextRepresentation** recupera un'istanza esistente della classe [**\_ ResourceRecord di MicrosoftDNS**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="780e7-107">The **GetObjectByTextRepresentation** method retrieves an existing instance of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="780e7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="780e7-108">Syntax</span></span>


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a><span data-ttu-id="780e7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="780e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="780e7-110">*DnsServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="780e7-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="780e7-111">Nome del server DNS da cui recuperare l'RR.</span><span class="sxs-lookup"><span data-stu-id="780e7-111">Name of the DNS Server from which the RR should be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="780e7-112">*ContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="780e7-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="780e7-113">Nome del contenitore da cui ottenere l'RR.</span><span class="sxs-lookup"><span data-stu-id="780e7-113">Name of the container from which the RR should be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="780e7-114">*TextRepresentation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="780e7-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="780e7-115">Rappresentazione testuale dell'RR da recuperare.</span><span class="sxs-lookup"><span data-stu-id="780e7-115">Text representation of the RR to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="780e7-116">*RR* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="780e7-116">*RR* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="780e7-117">Riferimento all'RR di cui è stata creata un'istanza.</span><span class="sxs-lookup"><span data-stu-id="780e7-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="780e7-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="780e7-118">Return value</span></span>

<span data-ttu-id="780e7-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="780e7-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="780e7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="780e7-120">Requirements</span></span>



| <span data-ttu-id="780e7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="780e7-121">Requirement</span></span> | <span data-ttu-id="780e7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="780e7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="780e7-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="780e7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="780e7-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="780e7-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="780e7-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="780e7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="780e7-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="780e7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="780e7-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="780e7-127">Namespace</span></span><br/>                | <span data-ttu-id="780e7-128">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="780e7-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="780e7-129">MOF</span><span class="sxs-lookup"><span data-stu-id="780e7-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="780e7-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="780e7-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="780e7-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="780e7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="780e7-132">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="780e7-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="780e7-133">**Metodo CreateInstanceFromTextRepresentation della classe MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="780e7-133">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





