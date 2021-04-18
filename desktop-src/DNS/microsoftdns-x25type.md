---
title: Classe MicrosoftDNS_X25Type
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record X. 25 (x25).
ms.assetid: 1213dfd7-30b3-413e-b723-f4284fa0b416
keywords:
- DNS della classe MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
- MicrosoftDNS_X25Type.Modify
- MicrosoftDNS_X25Type.PSDNAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584119dbd45d5d6c7fae347c506c42fcda4fff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302038"
---
# <a name="microsoftdns_x25type-class"></a><span data-ttu-id="bc063-105">\_Classe MicrosoftDNS X25Type</span><span class="sxs-lookup"><span data-stu-id="bc063-105">MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="bc063-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record X. 25 (x25).</span><span class="sxs-lookup"><span data-stu-id="bc063-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an X.25 (X25) record.</span></span>

<span data-ttu-id="bc063-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="bc063-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc063-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc063-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_X25Type : MicrosoftDNS_ResourceRecord
{
  string PSDNAddress;
};
```

## <a name="members"></a><span data-ttu-id="bc063-109">Members</span><span class="sxs-lookup"><span data-stu-id="bc063-109">Members</span></span>

<span data-ttu-id="bc063-110">La **classe \_ X25Type di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bc063-110">The **MicrosoftDNS\_X25Type** class has these types of members:</span></span>

-   [<span data-ttu-id="bc063-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="bc063-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="bc063-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc063-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bc063-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="bc063-113">Methods</span></span>

<span data-ttu-id="bc063-114">La **classe \_ X25Type di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bc063-114">The **MicrosoftDNS\_X25Type** class has these methods.</span></span>



| <span data-ttu-id="bc063-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="bc063-115">Method</span></span>                             | <span data-ttu-id="bc063-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc063-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc063-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="bc063-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="bc063-118">Crea un'istanza di un tipo ' x25' di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore time-to-Live e l'indirizzo PSDN.</span><span class="sxs-lookup"><span data-stu-id="bc063-118">Instantiates an 'X25' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the PSDN address.</span></span> <span data-ttu-id="bc063-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="bc063-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="bc063-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="bc063-120">Qualifiers: Implemented, static</span></span><br/>              |
| <span data-ttu-id="bc063-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="bc063-121">**Modify**</span></span>                         | <span data-ttu-id="bc063-122">Questo metodo aggiorna l'indirizzo TTL e PSDN ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="bc063-122">This method updates the TTL and PSDN Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="bc063-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="bc063-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="bc063-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="bc063-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="bc063-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="bc063-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bc063-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc063-126">Properties</span></span>

<span data-ttu-id="bc063-127">La **classe \_ X25Type di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bc063-127">The **MicrosoftDNS\_X25Type** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc063-128">**PSDNAddress**</span><span class="sxs-lookup"><span data-stu-id="bc063-128">**PSDNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc063-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc063-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc063-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc063-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc063-131">Indirizzo PSDN del proprietario dell'RR.</span><span class="sxs-lookup"><span data-stu-id="bc063-131">PSDN address of the owner of the RR.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc063-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc063-132">Requirements</span></span>



| <span data-ttu-id="bc063-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc063-133">Requirement</span></span> | <span data-ttu-id="bc063-134">Valore</span><span class="sxs-lookup"><span data-stu-id="bc063-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc063-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc063-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bc063-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bc063-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bc063-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc063-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bc063-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc063-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bc063-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bc063-139">Namespace</span></span><br/>                | <span data-ttu-id="bc063-140">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="bc063-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="bc063-141">MOF</span><span class="sxs-lookup"><span data-stu-id="bc063-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc063-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc063-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc063-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc063-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc063-144">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="bc063-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="bc063-145">**Metodo Modify della \_ classe X25Type di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bc063-145">**Modify Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-modify.md)
</dt> <dt>

[<span data-ttu-id="bc063-146">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bc063-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





