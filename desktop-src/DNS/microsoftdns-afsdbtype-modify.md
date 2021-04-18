---
title: Metodo Modify della classe MicrosoftDNS_AFSDBType
description: Il metodo modify aggiorna un record di risorse del server di database del file System Andrew (AFSDB).
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_AFSDBType classe
- Classe MicrosoftDNS_AFSDBType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4752910ab9e8117bfdaf27f93d32be3377158ba5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301645"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="83429-106">Metodo Modify della \_ classe AFSDBType di MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="83429-106">Modify method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="83429-107">Il metodo **Modify** aggiorna un record di risorse del server di database del file System Andrew (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="83429-107">The **Modify** method updates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="83429-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83429-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="83429-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="83429-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83429-110">Valore *TTL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="83429-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83429-111">Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.</span><span class="sxs-lookup"><span data-stu-id="83429-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="83429-112">*Sottotipo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="83429-112">*Subtype* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83429-113">Sottotipo del server AFS host.</span><span class="sxs-lookup"><span data-stu-id="83429-113">Subtype of the host AFS server.</span></span> <span data-ttu-id="83429-114">Per il sottotipo 1 (valore = 1), l'host dispone di un server del percorso del volume AFS versione 3,0 per la cella AFS denominata.</span><span class="sxs-lookup"><span data-stu-id="83429-114">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="83429-115">Nel caso del sottotipo 2 (valore = 2), l'host dispone di un server dei nomi autenticato che contiene il nodo della directory radice della cella per la cella DCE/autorità di certificazione denominata.</span><span class="sxs-lookup"><span data-stu-id="83429-115">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="83429-116">*Nomeserver* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="83429-116">*ServerName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83429-117">FQDN che specifica un host con un server per la cella AFS specificata nel nome del proprietario.</span><span class="sxs-lookup"><span data-stu-id="83429-117">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="83429-118">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="83429-118">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="83429-119">Riferimento all'oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="83429-119">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83429-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83429-120">Return value</span></span>

<span data-ttu-id="83429-121">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="83429-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83429-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="83429-122">Remarks</span></span>

<span data-ttu-id="83429-123">Tutti i parametri non specificati rimangono invariati nel record modificato.</span><span class="sxs-lookup"><span data-stu-id="83429-123">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="83429-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83429-124">Requirements</span></span>



| <span data-ttu-id="83429-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="83429-125">Requirement</span></span> | <span data-ttu-id="83429-126">Valore</span><span class="sxs-lookup"><span data-stu-id="83429-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83429-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83429-127">Minimum supported client</span></span><br/> | <span data-ttu-id="83429-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="83429-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="83429-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83429-129">Minimum supported server</span></span><br/> | <span data-ttu-id="83429-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="83429-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="83429-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="83429-131">Namespace</span></span><br/>                | <span data-ttu-id="83429-132">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="83429-132">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="83429-133">MOF</span><span class="sxs-lookup"><span data-stu-id="83429-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83429-134"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83429-134"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83429-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83429-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83429-136">**\_AFSDBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="83429-136">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="83429-137">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="83429-137">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="83429-138">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="83429-138">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





