---
title: Classe MicrosoftDNS_AAAAType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di indirizzo IPv6 (aaaa). Il record AAAA è comunemente pronunciato \ 0034; quad-a record \ 0034;.
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- DNS della classe MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0131177c342730c08868946c29356554cbfb9cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301646"
---
# <a name="microsoftdns_aaaatype-class"></a><span data-ttu-id="e801e-106">\_Classe MicrosoftDNS AAAAType</span><span class="sxs-lookup"><span data-stu-id="e801e-106">MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="e801e-107">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di indirizzo IPv6 (aaaa).</span><span class="sxs-lookup"><span data-stu-id="e801e-107">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an IPv6 Address (AAAA) record.</span></span> <span data-ttu-id="e801e-108">Il record AAAA viene comunemente pronunciato "record quad-a".</span><span class="sxs-lookup"><span data-stu-id="e801e-108">The AAAA record is commonly pronounced "quad-a record".</span></span>

<span data-ttu-id="e801e-109">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="e801e-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e801e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e801e-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a><span data-ttu-id="e801e-111">Members</span><span class="sxs-lookup"><span data-stu-id="e801e-111">Members</span></span>

<span data-ttu-id="e801e-112">La **classe \_ AAAAType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e801e-112">The **MicrosoftDNS\_AAAAType** class has these types of members:</span></span>

-   [<span data-ttu-id="e801e-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="e801e-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="e801e-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e801e-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e801e-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="e801e-115">Methods</span></span>

<span data-ttu-id="e801e-116">La **classe \_ AAAAType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e801e-116">The **MicrosoftDNS\_AAAAType** class has these methods.</span></span>



| <span data-ttu-id="e801e-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="e801e-117">Method</span></span>                             | <span data-ttu-id="e801e-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e801e-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e801e-119">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e801e-119">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="e801e-120">Crea un'istanza di un tipo ' AAAA ' di RR in base ai dati nei parametri di input del metodo, ovvero il nome del server DNS del record, il nome del contenitore, il nome del proprietario o dell'host, la classe (impostazione predefinita = IN), il valore di durata (TTL) e l'indirizzo IPv6.</span><span class="sxs-lookup"><span data-stu-id="e801e-120">Instantiates an 'AAAA' type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Host Name, class (default = IN), time-to-live value, and the IPv6 address.</span></span> <span data-ttu-id="e801e-121">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="e801e-121">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="e801e-122">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="e801e-122">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="e801e-123">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="e801e-123">**Modify**</span></span>                         | <span data-ttu-id="e801e-124">Aggiorna l'indirizzo TTL e IPv6 ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e801e-124">Updates the TTL and IPv6 address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="e801e-125">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="e801e-125">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="e801e-126">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="e801e-126">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="e801e-127">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="e801e-127">Qualifiers: Implemented</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="e801e-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e801e-128">Properties</span></span>

<span data-ttu-id="e801e-129">La **classe \_ AAAAType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e801e-129">The **MicrosoftDNS\_AAAAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e801e-130">**IPv6Address**</span><span class="sxs-lookup"><span data-stu-id="e801e-130">**IPv6Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e801e-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e801e-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e801e-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e801e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e801e-133">Indirizzo IPv6 per l'host.</span><span class="sxs-lookup"><span data-stu-id="e801e-133">IPv6 address for the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e801e-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e801e-134">Requirements</span></span>



| <span data-ttu-id="e801e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e801e-135">Requirement</span></span> | <span data-ttu-id="e801e-136">Valore</span><span class="sxs-lookup"><span data-stu-id="e801e-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e801e-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e801e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e801e-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e801e-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e801e-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e801e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e801e-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e801e-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e801e-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e801e-141">Namespace</span></span><br/>                | <span data-ttu-id="e801e-142">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="e801e-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e801e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="e801e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e801e-144"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e801e-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e801e-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e801e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e801e-146">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ AAAAType**</span><span class="sxs-lookup"><span data-stu-id="e801e-146">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e801e-147">**Metodo Modify della \_ classe AAAAType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e801e-147">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="e801e-148">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e801e-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





