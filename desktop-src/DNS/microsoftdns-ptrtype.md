---
title: Classe MicrosoftDNS_PTRType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record puntatore (PTR).
ms.assetid: 2cb0f13b-e683-473b-9cdd-bc5d805b919d
keywords:
- DNS della classe MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
- MicrosoftDNS_PTRType.Modify
- MicrosoftDNS_PTRType.PTRDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65dc434eb751ed925ab9efcdaf29f04741b749ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517950"
---
# <a name="microsoftdns_ptrtype-class"></a><span data-ttu-id="a0bb0-105">\_Classe MicrosoftDNS PTRType</span><span class="sxs-lookup"><span data-stu-id="a0bb0-105">MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="a0bb0-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="a0bb0-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Pointer (PTR) record.</span></span>

<span data-ttu-id="a0bb0-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="a0bb0-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0bb0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0bb0-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_PTRType : MicrosoftDNS_ResourceRecord
{
  string PTRDomainName;
};
```

## <a name="members"></a><span data-ttu-id="a0bb0-109">Members</span><span class="sxs-lookup"><span data-stu-id="a0bb0-109">Members</span></span>

<span data-ttu-id="a0bb0-110">La **classe \_ PTRType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a0bb0-110">The **MicrosoftDNS\_PTRType** class has these types of members:</span></span>

-   [<span data-ttu-id="a0bb0-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a0bb0-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0bb0-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a0bb0-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a0bb0-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="a0bb0-113">Methods</span></span>

<span data-ttu-id="a0bb0-114">La **classe \_ PTRType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a0bb0-114">The **MicrosoftDNS\_PTRType** class has these methods.</span></span>



| <span data-ttu-id="a0bb0-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="a0bb0-115">Method</span></span>                             | <span data-ttu-id="a0bb0-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0bb0-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bb0-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a0bb0-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="a0bb0-118">Crea un'istanza di un record di risorsa PTR DNS basato sui dati nei parametri di input del metodo, ovvero il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata (TTL) e il nome di dominio completo (FQDN) del record PTR.</span><span class="sxs-lookup"><span data-stu-id="a0bb0-118">Instantiates a DNS PTR Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the FQDN of the PTR record.</span></span> <span data-ttu-id="a0bb0-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="a0bb0-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="a0bb0-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="a0bb0-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="a0bb0-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="a0bb0-121">**Modify**</span></span>                         | <span data-ttu-id="a0bb0-122">Aggiorna il nome di dominio TTL e PTR ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="a0bb0-122">Updates the TTL and PTR Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="a0bb0-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="a0bb0-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="a0bb0-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="a0bb0-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="a0bb0-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="a0bb0-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="a0bb0-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a0bb0-126">Properties</span></span>

<span data-ttu-id="a0bb0-127">La **classe \_ PTRType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a0bb0-127">The **MicrosoftDNS\_PTRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0bb0-128">**PTRDomainName**</span><span class="sxs-lookup"><span data-stu-id="a0bb0-128">**PTRDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bb0-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0bb0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0bb0-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0bb0-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0bb0-131">FQDN dei dati del record PTR.</span><span class="sxs-lookup"><span data-stu-id="a0bb0-131">FQDN of the PTR record data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0bb0-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0bb0-132">Requirements</span></span>



| <span data-ttu-id="a0bb0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0bb0-133">Requirement</span></span> | <span data-ttu-id="a0bb0-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a0bb0-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bb0-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0bb0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a0bb0-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a0bb0-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a0bb0-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0bb0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a0bb0-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0bb0-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a0bb0-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a0bb0-139">Namespace</span></span><br/>                | <span data-ttu-id="a0bb0-140">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="a0bb0-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a0bb0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a0bb0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0bb0-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0bb0-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0bb0-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0bb0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0bb0-144">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="a0bb0-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a0bb0-145">**Metodo Modify della \_ classe PTRType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a0bb0-145">**Modify Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="a0bb0-146">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a0bb0-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





