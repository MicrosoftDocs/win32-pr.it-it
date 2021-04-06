---
title: Classe MicrosoftDNS_MDType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di agente di posta elettronica per il dominio (MD).
ms.assetid: 11242372-65fe-44ee-845b-2430aec59127
keywords:
- DNS della classe MicrosoftDNS_MDType
- MicrosoftDNS_MDType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
- MicrosoftDNS_MDType.Modify
- MicrosoftDNS_MDType.MDHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7641fda7a223fed7c2dc9229c5a3449c575e84ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873765"
---
# <a name="microsoftdns_mdtype-class"></a><span data-ttu-id="fe586-105">\_Classe MicrosoftDNS MDType</span><span class="sxs-lookup"><span data-stu-id="fe586-105">MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="fe586-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di agente di posta elettronica per il dominio (MD).</span><span class="sxs-lookup"><span data-stu-id="fe586-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Agent for Domain (MD) record.</span></span>

<span data-ttu-id="fe586-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="fe586-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe586-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe586-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MDType : MicrosoftDNS_ResourceRecord
{
  string MDHost;
};
```

## <a name="members"></a><span data-ttu-id="fe586-109">Members</span><span class="sxs-lookup"><span data-stu-id="fe586-109">Members</span></span>

<span data-ttu-id="fe586-110">La **classe \_ MDType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fe586-110">The **MicrosoftDNS\_MDType** class has these types of members:</span></span>

-   [<span data-ttu-id="fe586-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="fe586-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fe586-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fe586-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fe586-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="fe586-113">Methods</span></span>

<span data-ttu-id="fe586-114">La **classe \_ MDType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="fe586-114">The **MicrosoftDNS\_MDType** class has these methods.</span></span>



| <span data-ttu-id="fe586-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="fe586-115">Method</span></span>                             | <span data-ttu-id="fe586-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe586-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe586-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="fe586-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fe586-118">Crea un'istanza di un record di risorse MD DNS in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario del dominio, la classe (impostazione predefinita = IN), il valore time-to-Live e l'host dell'agente di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="fe586-118">Instantiates a DNS MD Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="fe586-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="fe586-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fe586-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="fe586-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fe586-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="fe586-121">**Modify**</span></span>                         | <span data-ttu-id="fe586-122">Aggiorna l'host TTL e MD ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fe586-122">Updates the TTL and MD host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fe586-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="fe586-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fe586-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="fe586-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fe586-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="fe586-125">Qualifiers: Implemented</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="fe586-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fe586-126">Properties</span></span>

<span data-ttu-id="fe586-127">La **classe \_ MDType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe586-127">The **MicrosoftDNS\_MDType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe586-128">**MDHost**</span><span class="sxs-lookup"><span data-stu-id="fe586-128">**MDHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe586-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe586-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe586-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe586-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe586-131">FQDN che specifica un host con un agente di posta elettronica in grado di consegnare la posta per il dominio specificato.</span><span class="sxs-lookup"><span data-stu-id="fe586-131">FQDN that specifies a host with a mail agent capable of delivering mail for the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe586-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe586-132">Requirements</span></span>



| <span data-ttu-id="fe586-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe586-133">Requirement</span></span> | <span data-ttu-id="fe586-134">Valore</span><span class="sxs-lookup"><span data-stu-id="fe586-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe586-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe586-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fe586-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fe586-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fe586-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe586-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fe586-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe586-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fe586-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fe586-139">Namespace</span></span><br/>                | <span data-ttu-id="fe586-140">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="fe586-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fe586-141">MOF</span><span class="sxs-lookup"><span data-stu-id="fe586-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe586-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe586-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe586-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe586-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe586-144">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MDType**</span><span class="sxs-lookup"><span data-stu-id="fe586-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fe586-145">**Metodo Modify della \_ classe MDType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="fe586-145">**Modify Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-modify.md)
</dt> <dt>

[<span data-ttu-id="fe586-146">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="fe586-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





