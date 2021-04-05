---
title: Classe MicrosoftDNS_MRType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di ridenominazione delle cassette postali (Sig.).
ms.assetid: fa5da18f-121b-477b-8876-6e337382e9b8
keywords:
- DNS della classe MicrosoftDNS_MRType
- MicrosoftDNS_MRType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
- MicrosoftDNS_MRType.Modify
- MicrosoftDNS_MRType.MRMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732f0e6f51963f5ae810e4730406a94264fdde47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120822"
---
# <a name="microsoftdns_mrtype-class"></a><span data-ttu-id="5e2fe-105">\_Classe MicrosoftDNS MRType</span><span class="sxs-lookup"><span data-stu-id="5e2fe-105">MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="5e2fe-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di ridenominazione delle cassette postali (Sig.).</span><span class="sxs-lookup"><span data-stu-id="5e2fe-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox Rename (MR) record.</span></span>

<span data-ttu-id="5e2fe-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="5e2fe-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e2fe-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e2fe-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MRType : MicrosoftDNS_ResourceRecord
{
  string MRMailbox;
};
```

## <a name="members"></a><span data-ttu-id="5e2fe-109">Members</span><span class="sxs-lookup"><span data-stu-id="5e2fe-109">Members</span></span>

<span data-ttu-id="5e2fe-110">La **classe \_ MRType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5e2fe-110">The **MicrosoftDNS\_MRType** class has these types of members:</span></span>

-   [<span data-ttu-id="5e2fe-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="5e2fe-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="5e2fe-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e2fe-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5e2fe-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="5e2fe-113">Methods</span></span>

<span data-ttu-id="5e2fe-114">La **classe \_ MRType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5e2fe-114">The **MicrosoftDNS\_MRType** class has these methods.</span></span>



| <span data-ttu-id="5e2fe-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="5e2fe-115">Method</span></span>                             | <span data-ttu-id="5e2fe-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e2fe-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2fe-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="5e2fe-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="5e2fe-118">Questo metodo crea un'istanza di un tipo "sig" di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario della cassetta postale, la classe (impostazione predefinita = IN), il valore time-to-Live e la ridenominazione della cassetta postale.</span><span class="sxs-lookup"><span data-stu-id="5e2fe-118">This method instantiates an 'MR' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox rename.</span></span> <span data-ttu-id="5e2fe-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="5e2fe-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="5e2fe-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="5e2fe-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="5e2fe-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="5e2fe-121">**Modify**</span></span>                         | <span data-ttu-id="5e2fe-122">Questo metodo aggiorna la cassetta postale TTL e MR ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="5e2fe-122">This method updates the TTL and MR Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="5e2fe-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="5e2fe-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="5e2fe-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="5e2fe-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="5e2fe-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="5e2fe-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="5e2fe-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e2fe-126">Properties</span></span>

<span data-ttu-id="5e2fe-127">La **classe \_ MRType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5e2fe-127">The **MicrosoftDNS\_MRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e2fe-128">**MRMailbox**</span><span class="sxs-lookup"><span data-stu-id="5e2fe-128">**MRMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e2fe-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e2fe-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e2fe-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e2fe-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e2fe-131">FQDN che specifica una cassetta postale che è la ridenominazione corretta della cassetta postale specificata nel nome del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="5e2fe-131">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e2fe-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e2fe-132">Requirements</span></span>



| <span data-ttu-id="5e2fe-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e2fe-133">Requirement</span></span> | <span data-ttu-id="5e2fe-134">Valore</span><span class="sxs-lookup"><span data-stu-id="5e2fe-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2fe-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e2fe-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5e2fe-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5e2fe-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5e2fe-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e2fe-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5e2fe-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e2fe-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5e2fe-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5e2fe-139">Namespace</span></span><br/>                | <span data-ttu-id="5e2fe-140">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="5e2fe-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5e2fe-141">MOF</span><span class="sxs-lookup"><span data-stu-id="5e2fe-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e2fe-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e2fe-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e2fe-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e2fe-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e2fe-144">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="5e2fe-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="5e2fe-145">**Metodo Modify della \_ classe MRType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5e2fe-145">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="5e2fe-146">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5e2fe-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





