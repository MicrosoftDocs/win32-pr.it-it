---
title: Classe MicrosoftDNS_MINFOType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di informazioni di posta elettronica (mInfo).
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- DNS della classe MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_MINFOType.Modify
- MicrosoftDNS_MINFOType.ResponsibleMailbox
- MicrosoftDNS_MINFOType.ErrorMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a7d230db9da32ce47cd4cfaf99c4978c4e63385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121275"
---
# <a name="microsoftdns_minfotype-class"></a><span data-ttu-id="b69bc-105">\_Classe MicrosoftDNS MINFOType</span><span class="sxs-lookup"><span data-stu-id="b69bc-105">MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="b69bc-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di informazioni di posta elettronica (mInfo).</span><span class="sxs-lookup"><span data-stu-id="b69bc-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Information (MINFO) record.</span></span>

<span data-ttu-id="b69bc-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="b69bc-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b69bc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b69bc-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MINFOType : MicrosoftDNS_ResourceRecord
{
  string ResponsibleMailbox;
  string ErrorMailbox;
};
```

## <a name="members"></a><span data-ttu-id="b69bc-109">Members</span><span class="sxs-lookup"><span data-stu-id="b69bc-109">Members</span></span>

<span data-ttu-id="b69bc-110">La **classe \_ MINFOType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b69bc-110">The **MicrosoftDNS\_MINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="b69bc-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="b69bc-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b69bc-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b69bc-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b69bc-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="b69bc-113">Methods</span></span>

<span data-ttu-id="b69bc-114">La **classe \_ MINFOType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b69bc-114">The **MicrosoftDNS\_MINFOType** class has these methods.</span></span>



| <span data-ttu-id="b69bc-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="b69bc-115">Method</span></span>                             | <span data-ttu-id="b69bc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b69bc-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b69bc-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="b69bc-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="b69bc-118">Crea un'istanza di un tipo MINFO di RR in base ai dati nei parametri di input del metodo, ovvero il nome del server DNS del record, il nome del contenitore, il nome del proprietario dell'elenco o della casella di posta elettronica, la classe (impostazione predefinita = IN), il valore time-to-Live e le cassette postali di errore e responsabile.</span><span class="sxs-lookup"><span data-stu-id="b69bc-118">Instantiates an MINFO Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail list/box, class (default = IN), time-to-live value and the responsible and error mailboxes.</span></span> <span data-ttu-id="b69bc-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="b69bc-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="b69bc-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="b69bc-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="b69bc-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="b69bc-121">**Modify**</span></span>                         | <span data-ttu-id="b69bc-122">Questo metodo aggiorna la cassetta postale del valore TTL, della cassetta postale responsabile e dell'errore ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="b69bc-122">This method updates the TTL, Responsible Mailbox, and Error Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="b69bc-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="b69bc-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="b69bc-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="b69bc-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="b69bc-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="b69bc-125">Qualifiers: Implemented</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="b69bc-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b69bc-126">Properties</span></span>

<span data-ttu-id="b69bc-127">La **classe \_ MINFOType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b69bc-127">The **MicrosoftDNS\_MINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b69bc-128">**ErrorMailbox**</span><span class="sxs-lookup"><span data-stu-id="b69bc-128">**ErrorMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b69bc-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b69bc-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b69bc-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b69bc-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b69bc-131">FQDN che specifica una cassetta postale per ricevere i messaggi di errore correlati alla lista di distribuzione o alla cassetta postale specificata dal nome del proprietario del record MINFO.</span><span class="sxs-lookup"><span data-stu-id="b69bc-131">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="b69bc-132">**ResponsibleMailbox**</span><span class="sxs-lookup"><span data-stu-id="b69bc-132">**ResponsibleMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b69bc-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b69bc-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b69bc-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b69bc-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b69bc-135">FQDN che specifica una cassetta postale responsabile della lista di distribuzione o della cassetta postale specificata nel nome del proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="b69bc-135">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b69bc-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b69bc-136">Requirements</span></span>



| <span data-ttu-id="b69bc-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b69bc-137">Requirement</span></span> | <span data-ttu-id="b69bc-138">Valore</span><span class="sxs-lookup"><span data-stu-id="b69bc-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b69bc-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b69bc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b69bc-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b69bc-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b69bc-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b69bc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b69bc-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b69bc-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b69bc-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b69bc-143">Namespace</span></span><br/>                | <span data-ttu-id="b69bc-144">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="b69bc-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b69bc-145">MOF</span><span class="sxs-lookup"><span data-stu-id="b69bc-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b69bc-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b69bc-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b69bc-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b69bc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b69bc-148">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="b69bc-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="b69bc-149">**Metodo Modify della \_ classe MINFOType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="b69bc-149">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="b69bc-150">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="b69bc-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





