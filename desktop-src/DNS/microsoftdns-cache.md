---
title: Classe MicrosoftDNS_Cache
description: La \_ classe cache MicrosoftDNS descrive una cache esistente in un server DNS.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- DNS della classe MicrosoftDNS_Cache
- MicrosoftDNS_Cache della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048374"
---
# <a name="microsoftdns_cache-class"></a><span data-ttu-id="a5d51-105">\_Classe della cache MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="a5d51-105">MicrosoftDNS\_Cache class</span></span>

<span data-ttu-id="a5d51-106">La **classe \_ cache MicrosoftDNS** descrive una cache esistente in un server DNS.</span><span class="sxs-lookup"><span data-stu-id="a5d51-106">The **MicrosoftDNS\_Cache** class describes a cache existing on a DNS Server.</span></span> <span data-ttu-id="a5d51-107">Questa classe semplifica la visualizzazione dell'indipendenza degli oggetti DNS anziché la rappresentazione di un oggetto reale.</span><span class="sxs-lookup"><span data-stu-id="a5d51-107">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span> <span data-ttu-id="a5d51-108">La classe della **\_ cache MicrosoftDNS** è un contenitore per i record di risorse memorizzati nella cache dal server DNS.</span><span class="sxs-lookup"><span data-stu-id="a5d51-108">The **MicrosoftDNS\_Cache** class is a container for the resource records cached by the DNS Server.</span></span> <span data-ttu-id="a5d51-109">Non confondere questo oggetto con un file di cache che contiene parametri radice.</span><span class="sxs-lookup"><span data-stu-id="a5d51-109">Do not confuse this with a Cache file that contains root hints.</span></span>

<span data-ttu-id="a5d51-110">Ogni istanza della **\_ cache MicrosoftDNS** della classe deve essere assegnata esattamente a un server DNS.</span><span class="sxs-lookup"><span data-stu-id="a5d51-110">Every instance of the class **MicrosoftDNS\_Cache** must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="a5d51-111">Può essere associato a più istanze del [**\_ dominio MicrosoftDNS**](microsoftdns-domain.md) o alle classi [**\_ ResourceRecord di MicrosoftDNS**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="a5d51-111">It may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="a5d51-112">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="a5d51-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d51-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5d51-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="a5d51-114">Members</span><span class="sxs-lookup"><span data-stu-id="a5d51-114">Members</span></span>

<span data-ttu-id="a5d51-115">La classe della **\_ cache MicrosoftDNS** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a5d51-115">The **MicrosoftDNS\_Cache** class has these types of members:</span></span>

-   [<span data-ttu-id="a5d51-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="a5d51-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a5d51-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="a5d51-117">Methods</span></span>

<span data-ttu-id="a5d51-118">La classe della **\_ cache MicrosoftDNS** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a5d51-118">The **MicrosoftDNS\_Cache** class has these methods.</span></span>



| <span data-ttu-id="a5d51-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="a5d51-119">Method</span></span>                   | <span data-ttu-id="a5d51-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5d51-120">Description</span></span>                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d51-121">**ClearCache**</span><span class="sxs-lookup"><span data-stu-id="a5d51-121">**ClearCache**</span></span>           | <span data-ttu-id="a5d51-122">Cancella la cache del server DNS dei record di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5d51-122">Clears the DNS Server cache of resource records.</span></span> <br/> <span data-ttu-id="a5d51-123">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="a5d51-123">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="a5d51-124">**Getdistinguishname**</span><span class="sxs-lookup"><span data-stu-id="a5d51-124">**GetDistinguishedName**</span></span> | <span data-ttu-id="a5d51-125">Recupera il nome distinto per la zona.</span><span class="sxs-lookup"><span data-stu-id="a5d51-125">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="a5d51-126">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="a5d51-126">Qualifiers: Implemented</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="a5d51-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5d51-127">Requirements</span></span>



| <span data-ttu-id="a5d51-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d51-128">Requirement</span></span> | <span data-ttu-id="a5d51-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a5d51-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d51-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5d51-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d51-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a5d51-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a5d51-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5d51-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d51-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a5d51-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a5d51-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a5d51-134">Namespace</span></span><br/>                | <span data-ttu-id="a5d51-135">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="a5d51-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a5d51-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a5d51-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5d51-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5d51-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5d51-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5d51-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d51-139">**\_Dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a5d51-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="a5d51-140">**Metodo ClearCache della \_ classe cache MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a5d51-140">**ClearCache Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-clearcache.md)
</dt> <dt>

[<span data-ttu-id="a5d51-141">**Metodo getdistinguishname della \_ classe cache MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a5d51-141">**GetDistinguishedName Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





