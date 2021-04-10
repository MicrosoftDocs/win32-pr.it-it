---
title: Classe MicrosoftDNS_MBType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di risorse cassetta postale (MB).
ms.assetid: b8f3b106-58f4-44b8-b2db-b00f1a495641
keywords:
- DNS della classe MicrosoftDNS_MBType
- MicrosoftDNS_MBType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
- MicrosoftDNS_MBType.Modify
- MicrosoftDNS_MBType.MBHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ad6599ad058f65beba961f00c1bd6c43663487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964377"
---
# <a name="microsoftdns_mbtype-class"></a><span data-ttu-id="ee3e3-105">\_Classe MicrosoftDNS MBType</span><span class="sxs-lookup"><span data-stu-id="ee3e3-105">MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="ee3e3-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di risorse cassetta postale (MB).</span><span class="sxs-lookup"><span data-stu-id="ee3e3-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox (MB) resource record.</span></span>

<span data-ttu-id="ee3e3-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee3e3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee3e3-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MBType : MicrosoftDNS_ResourceRecord
{
  string MBHost;
};
```

## <a name="members"></a><span data-ttu-id="ee3e3-109">Members</span><span class="sxs-lookup"><span data-stu-id="ee3e3-109">Members</span></span>

<span data-ttu-id="ee3e3-110">La **classe \_ MBType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ee3e3-110">The **MicrosoftDNS\_MBType** class has these types of members:</span></span>

-   [<span data-ttu-id="ee3e3-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="ee3e3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ee3e3-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee3e3-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ee3e3-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="ee3e3-113">Methods</span></span>

<span data-ttu-id="ee3e3-114">La **classe \_ MBType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-114">The **MicrosoftDNS\_MBType** class has these methods.</span></span>



| <span data-ttu-id="ee3e3-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="ee3e3-115">Method</span></span>                             | <span data-ttu-id="ee3e3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee3e3-116">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3e3-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ee3e3-118">Crea un'istanza di un RR MB in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario della cassetta postale, la classe (impostazione predefinita = IN), il valore time-to-Live e l'host della cassetta postale.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-118">Instantiates an MB RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox host.</span></span> <span data-ttu-id="ee3e3-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ee3e3-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="ee3e3-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ee3e3-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-121">**Modify**</span></span>                         | <span data-ttu-id="ee3e3-122">Aggiorna l'host TTL e MB ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-122">Updates the TTL and MB host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ee3e3-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ee3e3-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ee3e3-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="ee3e3-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="ee3e3-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee3e3-126">Properties</span></span>

<span data-ttu-id="ee3e3-127">La **classe \_ MBType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-127">The **MicrosoftDNS\_MBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee3e3-128">**MBHost**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-128">**MBHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3e3-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3e3-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee3e3-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee3e3-131">FQDN che specifica un host della cassetta postale specificata nel nome del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-131">FQDN that specifies a host of the mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee3e3-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee3e3-132">Requirements</span></span>



| <span data-ttu-id="ee3e3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee3e3-133">Requirement</span></span> | <span data-ttu-id="ee3e3-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ee3e3-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3e3-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee3e3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ee3e3-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ee3e3-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ee3e3-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee3e3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ee3e3-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ee3e3-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ee3e3-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ee3e3-139">Namespace</span></span><br/>                | <span data-ttu-id="ee3e3-140">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="ee3e3-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ee3e3-141">MOF</span><span class="sxs-lookup"><span data-stu-id="ee3e3-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee3e3-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee3e3-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee3e3-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee3e3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee3e3-144">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ee3e3-145">**Metodo Modify della \_ classe MBType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-145">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="ee3e3-146">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





