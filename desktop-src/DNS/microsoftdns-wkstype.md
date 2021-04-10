---
title: Classe MicrosoftDNS_WKSType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di Well-Known Services (WKS).
ms.assetid: 7bbfd518-d473-4127-949b-9133a43ac7a7
keywords:
- DNS della classe MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WKSType.Modify
- MicrosoftDNS_WKSType.InternetAddress
- MicrosoftDNS_WKSType.IPProtocol
- MicrosoftDNS_WKSType.Services
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7fde08721bb8bb62b93f72b792060b06c15dad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964459"
---
# <a name="microsoftdns_wkstype-class"></a><span data-ttu-id="9e7ad-105">\_Classe MicrosoftDNS WKSType</span><span class="sxs-lookup"><span data-stu-id="9e7ad-105">MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="9e7ad-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di Well-Known Services (WKS).</span><span class="sxs-lookup"><span data-stu-id="9e7ad-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Well-Known Services (WKS) record.</span></span>

<span data-ttu-id="9e7ad-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="9e7ad-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e7ad-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e7ad-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WKSType : MicrosoftDNS_ResourceRecord
{
  string InternetAddress;
  string IPProtocol;
  string Services;
};
```

## <a name="members"></a><span data-ttu-id="9e7ad-109">Members</span><span class="sxs-lookup"><span data-stu-id="9e7ad-109">Members</span></span>

<span data-ttu-id="9e7ad-110">La **classe \_ WKSType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9e7ad-110">The **MicrosoftDNS\_WKSType** class has these types of members:</span></span>

-   [<span data-ttu-id="9e7ad-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="9e7ad-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9e7ad-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e7ad-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9e7ad-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="9e7ad-113">Methods</span></span>

<span data-ttu-id="9e7ad-114">La **classe \_ WKSType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9e7ad-114">The **MicrosoftDNS\_WKSType** class has these methods.</span></span>



| <span data-ttu-id="9e7ad-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="9e7ad-115">Method</span></span>                             | <span data-ttu-id="9e7ad-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e7ad-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7ad-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="9e7ad-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="9e7ad-118">Crea un'istanza di un tipo WKS di RR in base ai dati nei parametri di input del metodo, ovvero il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata (TTL) e l'indirizzo Internet, il protocollo IP e la maschera di bit della porta del proprietario.</span><span class="sxs-lookup"><span data-stu-id="9e7ad-118">Instantiates a WKS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the owner's Internet Address, IP protocol and port bit mask.</span></span> <span data-ttu-id="9e7ad-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="9e7ad-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="9e7ad-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="9e7ad-120">Qualifiers: Implemented, static</span></span><br/>  |
| <span data-ttu-id="9e7ad-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="9e7ad-121">**Modify**</span></span>                         | <span data-ttu-id="9e7ad-122">Questo metodo aggiorna la durata (TTL), l'indirizzo Internet, il protocollo IP e i servizi ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="9e7ad-122">This method updates the TTL, Internet Address, IP Protocol, and Services to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="9e7ad-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="9e7ad-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="9e7ad-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="9e7ad-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="9e7ad-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="9e7ad-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9e7ad-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e7ad-126">Properties</span></span>

<span data-ttu-id="9e7ad-127">La **classe \_ WKSType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9e7ad-127">The **MicrosoftDNS\_WKSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e7ad-128">**InternetAddress**</span><span class="sxs-lookup"><span data-stu-id="9e7ad-128">**InternetAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7ad-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e7ad-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7ad-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e7ad-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e7ad-131">Indirizzo IP Internet per il proprietario del record.</span><span class="sxs-lookup"><span data-stu-id="9e7ad-131">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="9e7ad-132">**IPProtocol**</span><span class="sxs-lookup"><span data-stu-id="9e7ad-132">**IPProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7ad-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e7ad-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7ad-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e7ad-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e7ad-135">Stringa che rappresenta il protocollo IP per questo record.</span><span class="sxs-lookup"><span data-stu-id="9e7ad-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="9e7ad-136">I valori validi sono UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="9e7ad-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="9e7ad-137">**Services**</span><span class="sxs-lookup"><span data-stu-id="9e7ad-137">**Services**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7ad-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e7ad-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7ad-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e7ad-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e7ad-140">Stringa contenente tutti i servizi utilizzati dal record del servizio noto (WKS).</span><span class="sxs-lookup"><span data-stu-id="9e7ad-140">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e7ad-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e7ad-141">Requirements</span></span>



| <span data-ttu-id="9e7ad-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e7ad-142">Requirement</span></span> | <span data-ttu-id="9e7ad-143">Valore</span><span class="sxs-lookup"><span data-stu-id="9e7ad-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7ad-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e7ad-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9e7ad-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9e7ad-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9e7ad-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e7ad-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9e7ad-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9e7ad-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9e7ad-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9e7ad-148">Namespace</span></span><br/>                | <span data-ttu-id="9e7ad-149">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="9e7ad-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9e7ad-150">MOF</span><span class="sxs-lookup"><span data-stu-id="9e7ad-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e7ad-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e7ad-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e7ad-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e7ad-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e7ad-153">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="9e7ad-153">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="9e7ad-154">**Metodo Modify della \_ classe WKSType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9e7ad-154">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="9e7ad-155">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9e7ad-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





