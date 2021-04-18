---
title: Classe MicrosoftDNS_HINFOType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di informazioni sull'host (HINFO).
ms.assetid: c6591010-0fe6-45b2-9032-9f847237ecf6
keywords:
- DNS della classe MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_HINFOType.Modify
- MicrosoftDNS_HINFOType.CPU
- MicrosoftDNS_HINFOType.OS
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3298e5a7f90dbaee24e5014b1a3aab76ad6997
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302040"
---
# <a name="microsoftdns_hinfotype-class"></a><span data-ttu-id="56e8e-105">\_Classe MicrosoftDNS HINFOType</span><span class="sxs-lookup"><span data-stu-id="56e8e-105">MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="56e8e-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di informazioni sull'host (HINFO).</span><span class="sxs-lookup"><span data-stu-id="56e8e-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Host Information (HINFO) record.</span></span>

<span data-ttu-id="56e8e-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="56e8e-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e8e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56e8e-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_HINFOType : MicrosoftDNS_ResourceRecord
{
  string CPU;
  string OS;
};
```

## <a name="members"></a><span data-ttu-id="56e8e-109">Members</span><span class="sxs-lookup"><span data-stu-id="56e8e-109">Members</span></span>

<span data-ttu-id="56e8e-110">La **classe \_ HINFOType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="56e8e-110">The **MicrosoftDNS\_HINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="56e8e-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="56e8e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="56e8e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56e8e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="56e8e-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="56e8e-113">Methods</span></span>

<span data-ttu-id="56e8e-114">La **classe \_ HINFOType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="56e8e-114">The **MicrosoftDNS\_HINFOType** class has these methods.</span></span>



| <span data-ttu-id="56e8e-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="56e8e-115">Method</span></span>                             | <span data-ttu-id="56e8e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56e8e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56e8e-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="56e8e-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="56e8e-118">Crea un'istanza di un HINFO di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore time-to-Live e i tipi di CPU e del sistema operativo dell'host.</span><span class="sxs-lookup"><span data-stu-id="56e8e-118">Instantiates an HINFO of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the host's CPU and operating system types.</span></span> <span data-ttu-id="56e8e-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="56e8e-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="56e8e-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="56e8e-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="56e8e-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="56e8e-121">**Modify**</span></span>                         | <span data-ttu-id="56e8e-122">Aggiorna il TTL, la CPU e il sistema operativo ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="56e8e-122">Updates the TTL, CPU, and operating system to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="56e8e-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="56e8e-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="56e8e-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="56e8e-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="56e8e-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="56e8e-125">Qualifiers: Implemented</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="56e8e-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56e8e-126">Properties</span></span>

<span data-ttu-id="56e8e-127">La **classe \_ HINFOType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="56e8e-127">The **MicrosoftDNS\_HINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56e8e-128">**CPU**</span><span class="sxs-lookup"><span data-stu-id="56e8e-128">**CPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56e8e-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="56e8e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56e8e-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56e8e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56e8e-131">Tipo di CPU del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="56e8e-131">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="56e8e-132">**Sistema operativo**</span><span class="sxs-lookup"><span data-stu-id="56e8e-132">**OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56e8e-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="56e8e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56e8e-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56e8e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56e8e-135">Sistema operativo del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="56e8e-135">Operating system of the record owner.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56e8e-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56e8e-136">Requirements</span></span>



| <span data-ttu-id="56e8e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="56e8e-137">Requirement</span></span> | <span data-ttu-id="56e8e-138">Valore</span><span class="sxs-lookup"><span data-stu-id="56e8e-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56e8e-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56e8e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="56e8e-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="56e8e-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="56e8e-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56e8e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="56e8e-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="56e8e-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="56e8e-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="56e8e-143">Namespace</span></span><br/>                | <span data-ttu-id="56e8e-144">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="56e8e-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="56e8e-145">MOF</span><span class="sxs-lookup"><span data-stu-id="56e8e-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56e8e-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56e8e-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56e8e-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56e8e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e8e-148">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="56e8e-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="56e8e-149">**Metodo Modify della \_ classe HINFOType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="56e8e-149">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="56e8e-150">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="56e8e-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





