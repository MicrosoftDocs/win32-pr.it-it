---
title: Classe MicrosoftDNS_RootHints
description: La \_ classe MicrosoftDNS RootHints descrive il RootHints archiviato in un file di cache in un server DNS. Questa classe semplifica la visualizzazione dell'indipendenza degli oggetti DNS anziché la rappresentazione di un oggetto reale.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- DNS della classe MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120090"
---
# <a name="microsoftdns_roothints-class"></a><span data-ttu-id="72154-106">\_Classe MicrosoftDNS RootHints</span><span class="sxs-lookup"><span data-stu-id="72154-106">MicrosoftDNS\_RootHints class</span></span>

<span data-ttu-id="72154-107">La classe **MicrosoftDNS \_ RootHints** descrive il RootHints archiviato in un file di cache in un server DNS.</span><span class="sxs-lookup"><span data-stu-id="72154-107">The **MicrosoftDNS\_RootHints** class describes the RootHints stored in a Cache file on a DNS Server.</span></span> <span data-ttu-id="72154-108">Questa classe semplifica la visualizzazione dell'indipendenza degli oggetti DNS anziché la rappresentazione di un oggetto reale.</span><span class="sxs-lookup"><span data-stu-id="72154-108">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span>

<span data-ttu-id="72154-109">**MicrosoftDNS \_ RootHints** è un contenitore per i record di risorse archiviati dal server DNS in un file di cache.</span><span class="sxs-lookup"><span data-stu-id="72154-109">**MicrosoftDNS\_RootHints** is a container for the resource records stored by the DNS Server in a Cache file.</span></span> <span data-ttu-id="72154-110">Ogni istanza della classe **\_ RootHints di MicrosoftDNS** deve essere assegnata esattamente a un server DNS.</span><span class="sxs-lookup"><span data-stu-id="72154-110">Every instance of the **MicrosoftDNS\_RootHints** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="72154-111">Può essere associato a più istanze della classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="72154-111">It may be associated with multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

<span data-ttu-id="72154-112">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="72154-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="72154-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72154-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="72154-114">Members</span><span class="sxs-lookup"><span data-stu-id="72154-114">Members</span></span>

<span data-ttu-id="72154-115">La **classe \_ RootHints di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="72154-115">The **MicrosoftDNS\_RootHints** class has these types of members:</span></span>

-   [<span data-ttu-id="72154-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="72154-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="72154-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="72154-117">Methods</span></span>

<span data-ttu-id="72154-118">La **classe \_ RootHints di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="72154-118">The **MicrosoftDNS\_RootHints** class has these methods.</span></span>



| <span data-ttu-id="72154-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="72154-119">Method</span></span>                        | <span data-ttu-id="72154-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72154-120">Description</span></span>                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72154-121">**Getdistinguishname**</span><span class="sxs-lookup"><span data-stu-id="72154-121">**GetDistinguishedName**</span></span>      | <span data-ttu-id="72154-122">Recupera il nome distinto per la zona.</span><span class="sxs-lookup"><span data-stu-id="72154-122">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="72154-123">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="72154-123">Qualifiers: Implemented</span></span><br/>   |
| <span data-ttu-id="72154-124">**WriteBackRootHintDatafile**</span><span class="sxs-lookup"><span data-stu-id="72154-124">**WriteBackRootHintDatafile**</span></span> | <span data-ttu-id="72154-125">Scrive RootHints di nuovo nel file di cache DNS.</span><span class="sxs-lookup"><span data-stu-id="72154-125">Writes the RootHints back to the DNS Cache file.</span></span> <br/> <span data-ttu-id="72154-126">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="72154-126">Qualifiers: Implemented</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="72154-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72154-127">Requirements</span></span>



| <span data-ttu-id="72154-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="72154-128">Requirement</span></span> | <span data-ttu-id="72154-129">Valore</span><span class="sxs-lookup"><span data-stu-id="72154-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72154-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72154-130">Minimum supported client</span></span><br/> | <span data-ttu-id="72154-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="72154-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="72154-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72154-132">Minimum supported server</span></span><br/> | <span data-ttu-id="72154-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="72154-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="72154-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72154-134">Namespace</span></span><br/>                | <span data-ttu-id="72154-135">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="72154-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="72154-136">MOF</span><span class="sxs-lookup"><span data-stu-id="72154-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72154-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72154-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72154-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72154-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72154-139">**\_Dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="72154-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="72154-140">**Metodo WriteBackRootHintDatafile della classe MicrosoftDNS \_ RootHints**</span><span class="sxs-lookup"><span data-stu-id="72154-140">**WriteBackRootHintDatafile Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[<span data-ttu-id="72154-141">**Metodo getdistinguishname della \_ classe RootHints di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="72154-141">**GetDistinguishedName Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





