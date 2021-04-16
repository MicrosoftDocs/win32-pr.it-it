---
title: Classe MicrosoftDNS_MGType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record del gruppo di posta (mg).
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- DNS della classe MicrosoftDNS_MGType
- MicrosoftDNS_MGType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4772f8841977fbeae1f0bf609a65a9511bc704a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518970"
---
# <a name="microsoftdns_mgtype-class"></a><span data-ttu-id="a6efe-105">\_Classe MicrosoftDNS MGType</span><span class="sxs-lookup"><span data-stu-id="a6efe-105">MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="a6efe-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record del gruppo di posta (mg).</span><span class="sxs-lookup"><span data-stu-id="a6efe-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Group (MG) record.</span></span>

<span data-ttu-id="a6efe-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="a6efe-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6efe-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6efe-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a><span data-ttu-id="a6efe-109">Members</span><span class="sxs-lookup"><span data-stu-id="a6efe-109">Members</span></span>

<span data-ttu-id="a6efe-110">La **classe \_ MGType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a6efe-110">The **MicrosoftDNS\_MGType** class has these types of members:</span></span>

-   [<span data-ttu-id="a6efe-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a6efe-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a6efe-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6efe-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a6efe-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="a6efe-113">Methods</span></span>

<span data-ttu-id="a6efe-114">La **classe \_ MGType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a6efe-114">The **MicrosoftDNS\_MGType** class has these methods.</span></span>



| <span data-ttu-id="a6efe-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="a6efe-115">Method</span></span>                             | <span data-ttu-id="a6efe-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6efe-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6efe-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a6efe-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="a6efe-118">Questo metodo crea un'istanza di un tipo MG di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario del gruppo di posta elettronica, la classe (impostazione predefinita = IN), il valore time-to-Live e il nome della cassetta postale.</span><span class="sxs-lookup"><span data-stu-id="a6efe-118">This method instantiates an MG Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail group, class (default = IN), time-to-live value and the mailbox name.</span></span> <span data-ttu-id="a6efe-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="a6efe-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="a6efe-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="a6efe-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="a6efe-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="a6efe-121">**Modify**</span></span>                         | <span data-ttu-id="a6efe-122">Questo metodo aggiorna la cassetta postale TTL e MG ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="a6efe-122">This method updates the TTL and MG Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="a6efe-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="a6efe-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="a6efe-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="a6efe-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="a6efe-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="a6efe-125">Qualifiers: Implemented</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="a6efe-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6efe-126">Properties</span></span>

<span data-ttu-id="a6efe-127">La **classe \_ MGType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a6efe-127">The **MicrosoftDNS\_MGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6efe-128">**MGMailbox**</span><span class="sxs-lookup"><span data-stu-id="a6efe-128">**MGMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6efe-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6efe-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6efe-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6efe-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6efe-131">FQDN che specifica una cassetta postale che è un membro del gruppo di posta elettronica specificato dal nome del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="a6efe-131">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6efe-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6efe-132">Requirements</span></span>



| <span data-ttu-id="a6efe-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6efe-133">Requirement</span></span> | <span data-ttu-id="a6efe-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a6efe-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6efe-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6efe-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a6efe-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a6efe-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a6efe-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6efe-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a6efe-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a6efe-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a6efe-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6efe-139">Namespace</span></span><br/>                | <span data-ttu-id="a6efe-140">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="a6efe-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a6efe-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a6efe-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6efe-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6efe-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6efe-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6efe-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6efe-144">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="a6efe-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a6efe-145">**Metodo Modify della \_ classe MGType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a6efe-145">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="a6efe-146">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a6efe-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





