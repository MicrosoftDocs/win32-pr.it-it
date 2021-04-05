---
title: Classe MicrosoftDNS_RPType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di persona responsabile (RP).
ms.assetid: 2b1c1bbc-a69f-4480-a7f2-6420240d4ad8
keywords:
- DNS della classe MicrosoftDNS_RPType
- MicrosoftDNS_RPType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
- MicrosoftDNS_RPType.Modify
- MicrosoftDNS_RPType.RPMailbox
- MicrosoftDNS_RPType.TXTDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aae8686016d26cb9007b21a06c125d56ed5207f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873993"
---
# <a name="microsoftdns_rptype-class"></a><span data-ttu-id="e48c3-105">\_Classe MicrosoftDNS RPType</span><span class="sxs-lookup"><span data-stu-id="e48c3-105">MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="e48c3-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di persona responsabile (RP).</span><span class="sxs-lookup"><span data-stu-id="e48c3-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Responsible Person (RP) record.</span></span>

<span data-ttu-id="e48c3-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="e48c3-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e48c3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e48c3-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RPType : MicrosoftDNS_ResourceRecord
{
  string RPMailbox;
  string TXTDomainName;
};
```

## <a name="members"></a><span data-ttu-id="e48c3-109">Members</span><span class="sxs-lookup"><span data-stu-id="e48c3-109">Members</span></span>

<span data-ttu-id="e48c3-110">La **classe \_ RPType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e48c3-110">The **MicrosoftDNS\_RPType** class has these types of members:</span></span>

-   [<span data-ttu-id="e48c3-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e48c3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e48c3-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e48c3-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e48c3-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="e48c3-113">Methods</span></span>

<span data-ttu-id="e48c3-114">La **classe \_ RPType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e48c3-114">The **MicrosoftDNS\_RPType** class has these methods.</span></span>



| <span data-ttu-id="e48c3-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="e48c3-115">Method</span></span>                             | <span data-ttu-id="e48c3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e48c3-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e48c3-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e48c3-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="e48c3-118">Crea un'istanza di un tipo RP di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario/responsabile della persona, la classe (impostazione predefinita = IN), il valore time-to-Live e i nomi di dominio per la cassetta postale dell'utente e i percorsi TXT RR.</span><span class="sxs-lookup"><span data-stu-id="e48c3-118">Instantiates an RP Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/responsible person Name, class (default = IN), time-to-live value and the domain names for the person's mailbox and TXT RR locations.</span></span> <span data-ttu-id="e48c3-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="e48c3-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="e48c3-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="e48c3-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="e48c3-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="e48c3-121">**Modify**</span></span>                         | <span data-ttu-id="e48c3-122">Questo metodo aggiorna il nome di dominio TTL, cassetta postale RP e TXT ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e48c3-122">This method updates the TTL, RP Mailbox and TXT Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="e48c3-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="e48c3-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="e48c3-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="e48c3-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="e48c3-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="e48c3-125">Qualifiers: Implemented</span></span><br/>                                  |



 

### <a name="properties"></a><span data-ttu-id="e48c3-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e48c3-126">Properties</span></span>

<span data-ttu-id="e48c3-127">La **classe \_ RPType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e48c3-127">The **MicrosoftDNS\_RPType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e48c3-128">**RPMailbox**</span><span class="sxs-lookup"><span data-stu-id="e48c3-128">**RPMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e48c3-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e48c3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e48c3-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e48c3-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e48c3-131">FQDN che specifica la cassetta postale per la persona responsabile.</span><span class="sxs-lookup"><span data-stu-id="e48c3-131">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="e48c3-132">**TXTDomainName**</span><span class="sxs-lookup"><span data-stu-id="e48c3-132">**TXTDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e48c3-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e48c3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e48c3-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e48c3-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e48c3-135">FQDN per cui sono presenti record di risorse TXT.</span><span class="sxs-lookup"><span data-stu-id="e48c3-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e48c3-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e48c3-136">Requirements</span></span>



| <span data-ttu-id="e48c3-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e48c3-137">Requirement</span></span> | <span data-ttu-id="e48c3-138">Valore</span><span class="sxs-lookup"><span data-stu-id="e48c3-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e48c3-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e48c3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e48c3-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e48c3-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e48c3-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e48c3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e48c3-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e48c3-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e48c3-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e48c3-143">Namespace</span></span><br/>                | <span data-ttu-id="e48c3-144">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="e48c3-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e48c3-145">MOF</span><span class="sxs-lookup"><span data-stu-id="e48c3-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e48c3-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e48c3-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e48c3-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e48c3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e48c3-148">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="e48c3-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e48c3-149">**Metodo Modify della \_ classe RPType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e48c3-149">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="e48c3-150">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e48c3-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





