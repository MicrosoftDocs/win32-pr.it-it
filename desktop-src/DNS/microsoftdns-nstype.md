---
title: Classe MicrosoftDNS_NSType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record del server dei nomi (NS).
ms.assetid: 8d229acd-bc47-4a32-b6f1-b784a48dc91a
keywords:
- DNS della classe MicrosoftDNS_NSType
- MicrosoftDNS_NSType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType
- MicrosoftDNS_NSType.CreateInstanceFromPropertyData
- MicrosoftDNS_NSType.Modify
- MicrosoftDNS_NSType.NSHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07155c36089e60b12aeea214b19cb8aca146005a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964993"
---
# <a name="microsoftdns_nstype-class"></a><span data-ttu-id="bdd3e-105">\_Classe MicrosoftDNS NSType</span><span class="sxs-lookup"><span data-stu-id="bdd3e-105">MicrosoftDNS\_NSType class</span></span>

<span data-ttu-id="bdd3e-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record del server dei nomi (NS).</span><span class="sxs-lookup"><span data-stu-id="bdd3e-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Name Server (NS) record.</span></span>

<span data-ttu-id="bdd3e-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="bdd3e-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd3e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdd3e-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_NSType : MicrosoftDNS_ResourceRecord
{
  string NSHost;
};
```

## <a name="members"></a><span data-ttu-id="bdd3e-109">Members</span><span class="sxs-lookup"><span data-stu-id="bdd3e-109">Members</span></span>

<span data-ttu-id="bdd3e-110">La **classe \_ NSType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bdd3e-110">The **MicrosoftDNS\_NSType** class has these types of members:</span></span>

-   [<span data-ttu-id="bdd3e-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="bdd3e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="bdd3e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bdd3e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bdd3e-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="bdd3e-113">Methods</span></span>

<span data-ttu-id="bdd3e-114">La **classe \_ NSType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bdd3e-114">The **MicrosoftDNS\_NSType** class has these methods.</span></span>



| <span data-ttu-id="bdd3e-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="bdd3e-115">Method</span></span>                             | <span data-ttu-id="bdd3e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdd3e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd3e-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="bdd3e-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="bdd3e-118">Crea un'istanza di un record di risorse NS DNS basato sui dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata e l'host con autorità per il dominio.</span><span class="sxs-lookup"><span data-stu-id="bdd3e-118">Instantiates a DNS NS Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the host with authority for the domain.</span></span> <span data-ttu-id="bdd3e-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="bdd3e-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="bdd3e-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="bdd3e-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="bdd3e-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="bdd3e-121">**Modify**</span></span>                         | <span data-ttu-id="bdd3e-122">Aggiorna l'host TTL e NS ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="bdd3e-122">Updates the TTL and NS Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="bdd3e-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="bdd3e-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="bdd3e-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="bdd3e-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="bdd3e-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="bdd3e-125">Qualifiers: Implemented</span></span><br/>                               |



 

### <a name="properties"></a><span data-ttu-id="bdd3e-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bdd3e-126">Properties</span></span>

<span data-ttu-id="bdd3e-127">La **classe \_ NSType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bdd3e-127">The **MicrosoftDNS\_NSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bdd3e-128">**NSHost**</span><span class="sxs-lookup"><span data-stu-id="bdd3e-128">**NSHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bdd3e-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bdd3e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bdd3e-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bdd3e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bdd3e-131">Host autorevole per il dominio.</span><span class="sxs-lookup"><span data-stu-id="bdd3e-131">Authoritative host for the domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdd3e-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdd3e-132">Requirements</span></span>



| <span data-ttu-id="bdd3e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdd3e-133">Requirement</span></span> | <span data-ttu-id="bdd3e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="bdd3e-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd3e-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdd3e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bdd3e-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bdd3e-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bdd3e-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdd3e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bdd3e-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bdd3e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bdd3e-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bdd3e-139">Namespace</span></span><br/>                | <span data-ttu-id="bdd3e-140">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="bdd3e-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="bdd3e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="bdd3e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bdd3e-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bdd3e-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdd3e-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdd3e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdd3e-144">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ NSType**</span><span class="sxs-lookup"><span data-stu-id="bdd3e-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NSType Class**</span></span>](microsoftdns-nstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="bdd3e-145">**Metodo Modify della \_ classe NSType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bdd3e-145">**Modify Method of the MicrosoftDNS\_NSType Class**</span></span>](microsoftdns-nstype-modify.md)
</dt> <dt>

[<span data-ttu-id="bdd3e-146">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bdd3e-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





