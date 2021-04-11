---
title: Classe MicrosoftDNS_MFType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di agente di invio della posta elettronica per il dominio (MF).
ms.assetid: 0ba0fddd-c316-4a5b-ad65-6344dbe949c1
keywords:
- DNS della classe MicrosoftDNS_MFType
- MicrosoftDNS_MFType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
- MicrosoftDNS_MFType.Modify
- MicrosoftDNS_MFType.MFHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e030f695e95ee736b1c53a345201e0bd1addfe3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120478"
---
# <a name="microsoftdns_mftype-class"></a><span data-ttu-id="fe8c8-105">\_Classe MicrosoftDNS MFType</span><span class="sxs-lookup"><span data-stu-id="fe8c8-105">MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="fe8c8-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di agente di invio della posta elettronica per il dominio (MF).</span><span class="sxs-lookup"><span data-stu-id="fe8c8-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Forwarding Agent for Domain (MF) record.</span></span>

<span data-ttu-id="fe8c8-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="fe8c8-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe8c8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe8c8-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MFType : MicrosoftDNS_ResourceRecord
{
  string MFHost;
};
```

## <a name="members"></a><span data-ttu-id="fe8c8-109">Members</span><span class="sxs-lookup"><span data-stu-id="fe8c8-109">Members</span></span>

<span data-ttu-id="fe8c8-110">La **classe \_ MFType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fe8c8-110">The **MicrosoftDNS\_MFType** class has these types of members:</span></span>

-   [<span data-ttu-id="fe8c8-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="fe8c8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fe8c8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fe8c8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fe8c8-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="fe8c8-113">Methods</span></span>

<span data-ttu-id="fe8c8-114">La **classe \_ MFType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="fe8c8-114">The **MicrosoftDNS\_MFType** class has these methods.</span></span>



| <span data-ttu-id="fe8c8-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="fe8c8-115">Method</span></span>                             | <span data-ttu-id="fe8c8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe8c8-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8c8-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="fe8c8-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fe8c8-118">Questo metodo crea un'istanza di un tipo MF di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario del dominio, la classe (impostazione predefinita = IN), il valore time-to-Live e l'host dell'agente di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="fe8c8-118">This method instantiates an MF Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="fe8c8-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="fe8c8-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fe8c8-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="fe8c8-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fe8c8-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="fe8c8-121">**Modify**</span></span>                         | <span data-ttu-id="fe8c8-122">Questo metodo aggiorna l'host TTL e MF ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fe8c8-122">This method updates the TTL and MF Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fe8c8-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="fe8c8-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fe8c8-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="fe8c8-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fe8c8-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="fe8c8-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="fe8c8-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fe8c8-126">Properties</span></span>

<span data-ttu-id="fe8c8-127">La **classe \_ MFType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe8c8-127">The **MicrosoftDNS\_MFType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe8c8-128">**MFHost**</span><span class="sxs-lookup"><span data-stu-id="fe8c8-128">**MFHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe8c8-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe8c8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe8c8-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe8c8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe8c8-131">FQDN che specifica un host con un agente di posta elettronica che accetterà la posta elettronica per l'invio al dominio specificato.</span><span class="sxs-lookup"><span data-stu-id="fe8c8-131">FQDN specifying a host with a mail agent that will accept mail for forwarding to the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe8c8-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe8c8-132">Requirements</span></span>



| <span data-ttu-id="fe8c8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe8c8-133">Requirement</span></span> | <span data-ttu-id="fe8c8-134">Valore</span><span class="sxs-lookup"><span data-stu-id="fe8c8-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8c8-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe8c8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8c8-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fe8c8-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fe8c8-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe8c8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8c8-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe8c8-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fe8c8-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fe8c8-139">Namespace</span></span><br/>                | <span data-ttu-id="fe8c8-140">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="fe8c8-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fe8c8-141">MOF</span><span class="sxs-lookup"><span data-stu-id="fe8c8-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe8c8-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe8c8-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe8c8-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe8c8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe8c8-144">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="fe8c8-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fe8c8-145">**Metodo Modify della \_ classe MFType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="fe8c8-145">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="fe8c8-146">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="fe8c8-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





