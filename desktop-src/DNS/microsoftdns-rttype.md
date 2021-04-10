---
title: Classe MicrosoftDNS_RTType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record route through (RT).
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- DNS della classe MicrosoftDNS_RTType
- MicrosoftDNS_RTType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d867185d8ce07a54a47eb5ea7591ec8d68a11059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964371"
---
# <a name="microsoftdns_rttype-class"></a><span data-ttu-id="54f17-105">\_Classe MicrosoftDNS RTType</span><span class="sxs-lookup"><span data-stu-id="54f17-105">MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="54f17-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record route through (RT).</span><span class="sxs-lookup"><span data-stu-id="54f17-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Route Through (RT) record.</span></span>

<span data-ttu-id="54f17-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="54f17-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="54f17-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54f17-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a><span data-ttu-id="54f17-109">Members</span><span class="sxs-lookup"><span data-stu-id="54f17-109">Members</span></span>

<span data-ttu-id="54f17-110">La **classe \_ RTType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="54f17-110">The **MicrosoftDNS\_RTType** class has these types of members:</span></span>

-   [<span data-ttu-id="54f17-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="54f17-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="54f17-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54f17-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="54f17-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="54f17-113">Methods</span></span>

<span data-ttu-id="54f17-114">La **classe \_ RTType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="54f17-114">The **MicrosoftDNS\_RTType** class has these methods.</span></span>



| <span data-ttu-id="54f17-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="54f17-115">Method</span></span>                             | <span data-ttu-id="54f17-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54f17-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54f17-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="54f17-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="54f17-118">Crea un'istanza di un tipo RT di RR in base ai dati nei parametri di input del metodo, ovvero il nome del server DNS del record, il nome del contenitore, il nome del proprietario o dell'host, la classe (impostazione predefinita = IN), il valore time-to-Live, la preferenza di record e il nome host intermedio.</span><span class="sxs-lookup"><span data-stu-id="54f17-118">Instantiates an RT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/host Name, class (default = IN), time-to-live value, record preference and intermediate host name.</span></span> <span data-ttu-id="54f17-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="54f17-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="54f17-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="54f17-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="54f17-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="54f17-121">**Modify**</span></span>                         | <span data-ttu-id="54f17-122">Aggiorna la durata (TTL), la preferenza e l'host intermedio ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="54f17-122">Updates the TTL, Preference, and Intermediate Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="54f17-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="54f17-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="54f17-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="54f17-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="54f17-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="54f17-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="54f17-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54f17-126">Properties</span></span>

<span data-ttu-id="54f17-127">La **classe \_ RTType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="54f17-127">The **MicrosoftDNS\_RTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54f17-128">**IntermediateHost**</span><span class="sxs-lookup"><span data-stu-id="54f17-128">**IntermediateHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f17-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54f17-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54f17-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54f17-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f17-131">FQDN che specifica un host che funge da intermediario per raggiungere l'host specificato dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="54f17-131">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="54f17-132">**Preferenza**</span><span class="sxs-lookup"><span data-stu-id="54f17-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f17-133">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54f17-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54f17-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54f17-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f17-135">Preferenza assegnata a questo RR tra gli altri nello stesso proprietario.</span><span class="sxs-lookup"><span data-stu-id="54f17-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="54f17-136">Sono preferibili valori inferiori.</span><span class="sxs-lookup"><span data-stu-id="54f17-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54f17-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54f17-137">Requirements</span></span>



| <span data-ttu-id="54f17-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="54f17-138">Requirement</span></span> | <span data-ttu-id="54f17-139">Valore</span><span class="sxs-lookup"><span data-stu-id="54f17-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54f17-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54f17-140">Minimum supported client</span></span><br/> | <span data-ttu-id="54f17-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="54f17-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="54f17-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54f17-142">Minimum supported server</span></span><br/> | <span data-ttu-id="54f17-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54f17-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="54f17-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="54f17-144">Namespace</span></span><br/>                | <span data-ttu-id="54f17-145">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="54f17-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="54f17-146">MOF</span><span class="sxs-lookup"><span data-stu-id="54f17-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54f17-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54f17-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54f17-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54f17-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f17-149">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="54f17-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="54f17-150">**Metodo Modify della \_ classe RTType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="54f17-150">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="54f17-151">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="54f17-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





