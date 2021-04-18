---
title: Classe MicrosoftDNS_AType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di indirizzo host (a).
ms.assetid: c7bd8a26-b0ac-49ef-9068-a0ecddeb6ef4
keywords:
- DNS della classe MicrosoftDNS_AType
- MicrosoftDNS_AType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
- MicrosoftDNS_AType.Modify
- MicrosoftDNS_AType.IPAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e856968e2c3d4e581d69e0ac7bcbddc256424c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301642"
---
# <a name="microsoftdns_atype-class"></a><span data-ttu-id="18d99-105">\_Classe MicrosoftDNS aType</span><span class="sxs-lookup"><span data-stu-id="18d99-105">MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="18d99-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di indirizzo host (a).</span><span class="sxs-lookup"><span data-stu-id="18d99-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a host Address (A) record.</span></span>

<span data-ttu-id="18d99-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="18d99-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d99-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18d99-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AType : MicrosoftDNS_ResourceRecord
{
  string IPAddress;
};
```

## <a name="members"></a><span data-ttu-id="18d99-109">Members</span><span class="sxs-lookup"><span data-stu-id="18d99-109">Members</span></span>

<span data-ttu-id="18d99-110">La **classe \_ aType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="18d99-110">The **MicrosoftDNS\_AType** class has these types of members:</span></span>

-   [<span data-ttu-id="18d99-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="18d99-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="18d99-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="18d99-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18d99-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="18d99-113">Methods</span></span>

<span data-ttu-id="18d99-114">La **classe \_ aType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="18d99-114">The **MicrosoftDNS\_AType** class has these methods.</span></span>



| <span data-ttu-id="18d99-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="18d99-115">Method</span></span>                             | <span data-ttu-id="18d99-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18d99-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d99-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="18d99-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="18d99-118">Crea un'istanza di un indirizzo host (A) RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore time-to-Live e l'indirizzo IP dell'host.</span><span class="sxs-lookup"><span data-stu-id="18d99-118">Instantiates a Host Address (A) RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the IP address of the host.</span></span> <span data-ttu-id="18d99-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="18d99-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="18d99-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="18d99-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="18d99-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="18d99-121">**Modify**</span></span>                         | <span data-ttu-id="18d99-122">Aggiorna il valore TTL e l'indirizzo IP ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="18d99-122">Updates the TTL and IP address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="18d99-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="18d99-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="18d99-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="18d99-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="18d99-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="18d99-125">Qualifiers: Implemented</span></span><br/>             |



 

### <a name="properties"></a><span data-ttu-id="18d99-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="18d99-126">Properties</span></span>

<span data-ttu-id="18d99-127">La **classe \_ aType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="18d99-127">The **MicrosoftDNS\_AType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18d99-128">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="18d99-128">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d99-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18d99-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d99-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18d99-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d99-131">Stringa che rappresenta l'indirizzo IPv4 dell'host.</span><span class="sxs-lookup"><span data-stu-id="18d99-131">String representing the IPv4 address of the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18d99-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18d99-132">Requirements</span></span>



| <span data-ttu-id="18d99-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="18d99-133">Requirement</span></span> | <span data-ttu-id="18d99-134">Valore</span><span class="sxs-lookup"><span data-stu-id="18d99-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18d99-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18d99-135">Minimum supported client</span></span><br/> | <span data-ttu-id="18d99-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="18d99-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="18d99-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18d99-137">Minimum supported server</span></span><br/> | <span data-ttu-id="18d99-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18d99-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="18d99-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="18d99-139">Namespace</span></span><br/>                | <span data-ttu-id="18d99-140">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="18d99-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="18d99-141">MOF</span><span class="sxs-lookup"><span data-stu-id="18d99-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18d99-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18d99-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18d99-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18d99-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d99-144">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="18d99-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="18d99-145">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ aType**</span><span class="sxs-lookup"><span data-stu-id="18d99-145">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="18d99-146">**Metodo Modify della \_ classe aType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="18d99-146">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





