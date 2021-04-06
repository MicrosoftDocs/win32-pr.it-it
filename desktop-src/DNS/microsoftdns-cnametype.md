---
title: Classe MicrosoftDNS_CNAMEType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di nome canonico (CNAME).
ms.assetid: 93a972e3-abb1-425f-beb7-32abe7d0b485
keywords:
- DNS della classe MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
- MicrosoftDNS_CNAMEType.Modify
- MicrosoftDNS_CNAMEType.PrimaryName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dca8729c2c750e1cef774b5f0f3eadc3e2f6fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873821"
---
# <a name="microsoftdns_cnametype-class"></a><span data-ttu-id="c012b-105">\_Classe MicrosoftDNS CNAMEType</span><span class="sxs-lookup"><span data-stu-id="c012b-105">MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="c012b-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di nome canonico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="c012b-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Canonical Name (CNAME) record.</span></span>

<span data-ttu-id="c012b-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="c012b-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c012b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c012b-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_CNAMEType : MicrosoftDNS_ResourceRecord
{
  string PrimaryName;
};
```

## <a name="members"></a><span data-ttu-id="c012b-109">Members</span><span class="sxs-lookup"><span data-stu-id="c012b-109">Members</span></span>

<span data-ttu-id="c012b-110">La **classe \_ CNAMEType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c012b-110">The **MicrosoftDNS\_CNAMEType** class has these types of members:</span></span>

-   [<span data-ttu-id="c012b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="c012b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c012b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c012b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c012b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="c012b-113">Methods</span></span>

<span data-ttu-id="c012b-114">La **classe \_ CNAMEType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c012b-114">The **MicrosoftDNS\_CNAMEType** class has these methods.</span></span>



| <span data-ttu-id="c012b-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="c012b-115">Method</span></span>                             | <span data-ttu-id="c012b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c012b-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c012b-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c012b-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="c012b-118">Crea un'istanza di un record di risorse CNAME basato sui dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata (TTL) e il nome primario del record CNAME.</span><span class="sxs-lookup"><span data-stu-id="c012b-118">Instantiates a CNAME Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the primary name of the CNAME record.</span></span> <span data-ttu-id="c012b-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="c012b-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="c012b-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="c012b-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="c012b-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="c012b-121">**Modify**</span></span>                         | <span data-ttu-id="c012b-122">Aggiorna il nome TTL e il nome primario ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c012b-122">Updates the TTL and Primary Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="c012b-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="c012b-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="c012b-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="c012b-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="c012b-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="c012b-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="c012b-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c012b-126">Properties</span></span>

<span data-ttu-id="c012b-127">La **classe \_ CNAMEType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c012b-127">The **MicrosoftDNS\_CNAMEType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c012b-128">**PrimaryName**</span><span class="sxs-lookup"><span data-stu-id="c012b-128">**PrimaryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c012b-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c012b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c012b-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c012b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c012b-131">Nome canonico o primario per il proprietario del record CNAME.</span><span class="sxs-lookup"><span data-stu-id="c012b-131">Canonical, or primary name for the owner of the CNAME record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c012b-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c012b-132">Requirements</span></span>



| <span data-ttu-id="c012b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c012b-133">Requirement</span></span> | <span data-ttu-id="c012b-134">Valore</span><span class="sxs-lookup"><span data-stu-id="c012b-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c012b-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c012b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c012b-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c012b-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c012b-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c012b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c012b-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c012b-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c012b-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c012b-139">Namespace</span></span><br/>                | <span data-ttu-id="c012b-140">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="c012b-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c012b-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c012b-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c012b-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c012b-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c012b-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c012b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c012b-144">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="c012b-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c012b-145">**Metodo Modify della \_ classe CNAMEType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c012b-145">**Modify Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-modify.md)
</dt> <dt>

[<span data-ttu-id="c012b-146">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c012b-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





