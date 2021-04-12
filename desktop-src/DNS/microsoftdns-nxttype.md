---
title: Classe MicrosoftDNS_NXTType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un RR successivo (NXT).
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- DNS della classe MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79db82b3ae760c31d4e6fef80eb01469cb2bb41d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120094"
---
# <a name="microsoftdns_nxttype-class"></a><span data-ttu-id="59c09-105">\_Classe MicrosoftDNS NXTType</span><span class="sxs-lookup"><span data-stu-id="59c09-105">MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="59c09-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un RR successivo (NXT).</span><span class="sxs-lookup"><span data-stu-id="59c09-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Next (NXT) RR.</span></span>

<span data-ttu-id="59c09-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="59c09-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c09-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59c09-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a><span data-ttu-id="59c09-109">Members</span><span class="sxs-lookup"><span data-stu-id="59c09-109">Members</span></span>

<span data-ttu-id="59c09-110">La **classe \_ NXTType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="59c09-110">The **MicrosoftDNS\_NXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="59c09-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="59c09-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="59c09-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="59c09-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="59c09-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="59c09-113">Methods</span></span>

<span data-ttu-id="59c09-114">La **classe \_ NXTType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="59c09-114">The **MicrosoftDNS\_NXTType** class has these methods.</span></span>



| <span data-ttu-id="59c09-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="59c09-115">Method</span></span>                             | <span data-ttu-id="59c09-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59c09-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59c09-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="59c09-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="59c09-118">Crea un'istanza di un record di risorse NXT basato sui dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata e il flag di mapping WINS, il timeout della ricerca inversa, il timeout della cache WINS e il nome di dominio da accodare.</span><span class="sxs-lookup"><span data-stu-id="59c09-118">Instantiates an NXT Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out, and domain name to append.</span></span> <span data-ttu-id="59c09-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="59c09-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="59c09-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="59c09-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="59c09-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="59c09-121">**Modify**</span></span>                         | <span data-ttu-id="59c09-122">Aggiorna il valore TTL, il flag di mapping, il timeout di ricerca, il timeout della cache e il dominio dei risultati ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="59c09-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="59c09-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="59c09-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="59c09-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="59c09-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="59c09-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="59c09-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="59c09-126">**Windows Server 2003:** Questo metodo aggiorna inoltre i NextDomainName e i tipi ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="59c09-126">**Windows Server 2003:** This method also updates the NextDomainName and Types to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="59c09-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="59c09-127">Properties</span></span>

<span data-ttu-id="59c09-128">La **classe \_ NXTType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="59c09-128">The **MicrosoftDNS\_NXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59c09-129">**NextDomainName**</span><span class="sxs-lookup"><span data-stu-id="59c09-129">**NextDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c09-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59c09-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59c09-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59c09-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59c09-132">Nome di dominio successivo.</span><span class="sxs-lookup"><span data-stu-id="59c09-132">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="59c09-133">**Tipi**</span><span class="sxs-lookup"><span data-stu-id="59c09-133">**Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c09-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59c09-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59c09-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59c09-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59c09-136">Elenco separato da spazi dei tasti di scelta del tipo RR per il nome del proprietario del record di risorse NXT.</span><span class="sxs-lookup"><span data-stu-id="59c09-136">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59c09-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59c09-137">Requirements</span></span>



| <span data-ttu-id="59c09-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="59c09-138">Requirement</span></span> | <span data-ttu-id="59c09-139">Valore</span><span class="sxs-lookup"><span data-stu-id="59c09-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59c09-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59c09-140">Minimum supported client</span></span><br/> | <span data-ttu-id="59c09-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="59c09-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="59c09-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59c09-142">Minimum supported server</span></span><br/> | <span data-ttu-id="59c09-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="59c09-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="59c09-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59c09-144">Namespace</span></span><br/>                | <span data-ttu-id="59c09-145">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="59c09-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="59c09-146">MOF</span><span class="sxs-lookup"><span data-stu-id="59c09-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59c09-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59c09-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59c09-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59c09-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c09-149">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="59c09-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="59c09-150">**Metodo Modify della \_ classe NXTType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="59c09-150">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="59c09-151">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="59c09-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





