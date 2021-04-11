---
title: Classe MicrosoftDNS_ISDNType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record ISDN.
ms.assetid: 8925042c-65d3-465f-aedd-9f7c862620b5
keywords:
- DNS della classe MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
- MicrosoftDNS_ISDNType.Modify
- MicrosoftDNS_ISDNType.ISDNNumber
- MicrosoftDNS_ISDNType.SubAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e8b50d75f7b6d57226247c978ced45e07b1acc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119063"
---
# <a name="microsoftdns_isdntype-class"></a><span data-ttu-id="ec20b-105">\_Classe MicrosoftDNS ISDNType</span><span class="sxs-lookup"><span data-stu-id="ec20b-105">MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="ec20b-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record ISDN.</span><span class="sxs-lookup"><span data-stu-id="ec20b-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ISDN record.</span></span>

<span data-ttu-id="ec20b-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="ec20b-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec20b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec20b-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ISDNType : MicrosoftDNS_ResourceRecord
{
  string ISDNNumber;
  string SubAddress;
};
```

## <a name="members"></a><span data-ttu-id="ec20b-109">Members</span><span class="sxs-lookup"><span data-stu-id="ec20b-109">Members</span></span>

<span data-ttu-id="ec20b-110">La **classe \_ ISDNType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ec20b-110">The **MicrosoftDNS\_ISDNType** class has these types of members:</span></span>

-   [<span data-ttu-id="ec20b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="ec20b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ec20b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ec20b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ec20b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="ec20b-113">Methods</span></span>

<span data-ttu-id="ec20b-114">La **classe \_ ISDNType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ec20b-114">The **MicrosoftDNS\_ISDNType** class has these methods.</span></span>



| <span data-ttu-id="ec20b-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="ec20b-115">Method</span></span>                             | <span data-ttu-id="ec20b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec20b-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec20b-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ec20b-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ec20b-118">Crea un'istanza di un record di risorse ISDN basato sui dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata (TTL) e il numero ISDN e il sottoindirizzo del proprietario.</span><span class="sxs-lookup"><span data-stu-id="ec20b-118">Instantiates an ISDN Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the ISDN number and subaddress of the owner.</span></span> <span data-ttu-id="ec20b-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="ec20b-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ec20b-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="ec20b-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ec20b-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="ec20b-121">**Modify**</span></span>                         | <span data-ttu-id="ec20b-122">Aggiorna la durata (TTL), il numero ISDN e il sottoindirizzo ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ec20b-122">Updates the TTL, ISDN Number, and Subaddress to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ec20b-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="ec20b-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ec20b-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="ec20b-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ec20b-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="ec20b-125">Qualifiers: Implemented</span></span><br/>                   |



 

### <a name="properties"></a><span data-ttu-id="ec20b-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ec20b-126">Properties</span></span>

<span data-ttu-id="ec20b-127">La **classe \_ ISDNType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ec20b-127">The **MicrosoftDNS\_ISDNType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec20b-128">**ISDNNumber**</span><span class="sxs-lookup"><span data-stu-id="ec20b-128">**ISDNNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec20b-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec20b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec20b-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec20b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec20b-131">Numero ISDN e DDI del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="ec20b-131">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="ec20b-132">**Sottoindirizzo**</span><span class="sxs-lookup"><span data-stu-id="ec20b-132">**SubAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec20b-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec20b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec20b-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec20b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec20b-135">Sottoindirizzo del proprietario, se definito.</span><span class="sxs-lookup"><span data-stu-id="ec20b-135">Subaddress of the owner, if defined.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec20b-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec20b-136">Requirements</span></span>



| <span data-ttu-id="ec20b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec20b-137">Requirement</span></span> | <span data-ttu-id="ec20b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="ec20b-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec20b-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec20b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ec20b-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ec20b-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ec20b-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec20b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ec20b-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ec20b-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ec20b-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ec20b-143">Namespace</span></span><br/>                | <span data-ttu-id="ec20b-144">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="ec20b-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ec20b-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ec20b-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec20b-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec20b-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec20b-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec20b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec20b-148">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ ISDNType**</span><span class="sxs-lookup"><span data-stu-id="ec20b-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ec20b-149">**Metodo Modify della \_ classe ISDNType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ec20b-149">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="ec20b-150">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ec20b-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





