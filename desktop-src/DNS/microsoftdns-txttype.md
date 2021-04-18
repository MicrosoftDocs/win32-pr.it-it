---
title: Classe MicrosoftDNS_TXTType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di testo (txt).
ms.assetid: e4bd445f-71c4-48dc-b210-e3ad4452d2e5
keywords:
- DNS della classe MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_TXTType.Modify
- MicrosoftDNS_TXTType.DescriptiveText
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d89563240b8e6d6bedb51cbe802180cd7577b57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302358"
---
# <a name="microsoftdns_txttype-class"></a><span data-ttu-id="b1296-105">\_Classe MicrosoftDNS TXTType</span><span class="sxs-lookup"><span data-stu-id="b1296-105">MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="b1296-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di testo (txt).</span><span class="sxs-lookup"><span data-stu-id="b1296-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Text (TXT) record.</span></span>

<span data-ttu-id="b1296-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="b1296-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1296-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1296-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_TXTType : MicrosoftDNS_ResourceRecord
{
  string DescriptiveText;
};
```

## <a name="members"></a><span data-ttu-id="b1296-109">Members</span><span class="sxs-lookup"><span data-stu-id="b1296-109">Members</span></span>

<span data-ttu-id="b1296-110">La **classe \_ TXTType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b1296-110">The **MicrosoftDNS\_TXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="b1296-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="b1296-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b1296-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1296-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b1296-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="b1296-113">Methods</span></span>

<span data-ttu-id="b1296-114">La **classe \_ TXTType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b1296-114">The **MicrosoftDNS\_TXTType** class has these methods.</span></span>



| <span data-ttu-id="b1296-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="b1296-115">Method</span></span>                             | <span data-ttu-id="b1296-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1296-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1296-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="b1296-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="b1296-118">Crea un'istanza di un tipo TXT di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata (TTL) e il testo del record.</span><span class="sxs-lookup"><span data-stu-id="b1296-118">Instantiates a TXT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the record's text.</span></span> <span data-ttu-id="b1296-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="b1296-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="b1296-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="b1296-120">Qualifiers: Implemented, static</span></span><br/>        |
| <span data-ttu-id="b1296-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="b1296-121">**Modify**</span></span>                         | <span data-ttu-id="b1296-122">Aggiorna il valore TTL e il testo descrittivo ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="b1296-122">Updates the TTL and Descriptive Text to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="b1296-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="b1296-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="b1296-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="b1296-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="b1296-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="b1296-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b1296-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1296-126">Properties</span></span>

<span data-ttu-id="b1296-127">La **classe \_ TXTType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b1296-127">The **MicrosoftDNS\_TXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1296-128">**DescriptiveText**</span><span class="sxs-lookup"><span data-stu-id="b1296-128">**DescriptiveText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1296-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b1296-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1296-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1296-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1296-131">Testo descrittivo, la semantica di che dipende dal dominio proprietario.</span><span class="sxs-lookup"><span data-stu-id="b1296-131">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1296-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1296-132">Requirements</span></span>



| <span data-ttu-id="b1296-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1296-133">Requirement</span></span> | <span data-ttu-id="b1296-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b1296-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1296-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1296-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b1296-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b1296-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b1296-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1296-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b1296-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1296-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b1296-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1296-139">Namespace</span></span><br/>                | <span data-ttu-id="b1296-140">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="b1296-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b1296-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b1296-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1296-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1296-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1296-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1296-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1296-144">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="b1296-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="b1296-145">**Metodo Modify della \_ classe TXTType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="b1296-145">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="b1296-146">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="b1296-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





