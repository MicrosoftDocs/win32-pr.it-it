---
title: Classe MicrosoftDNS_ATMAType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un indirizzo ATM per il nome (ATMA) record.
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- DNS della classe MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237dc4ecb657e79e835abcfdacf90844fb05c5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964226"
---
# <a name="microsoftdns_atmatype-class"></a><span data-ttu-id="328a1-105">\_Classe MicrosoftDNS ATMAType</span><span class="sxs-lookup"><span data-stu-id="328a1-105">MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="328a1-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un indirizzo ATM per il nome (ATMA) record.</span><span class="sxs-lookup"><span data-stu-id="328a1-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ATM Address to Name (ATMA) record.</span></span>

<span data-ttu-id="328a1-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="328a1-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="328a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="328a1-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a><span data-ttu-id="328a1-109">Members</span><span class="sxs-lookup"><span data-stu-id="328a1-109">Members</span></span>

<span data-ttu-id="328a1-110">La **classe \_ ATMAType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="328a1-110">The **MicrosoftDNS\_ATMAType** class has these types of members:</span></span>

-   [<span data-ttu-id="328a1-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="328a1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="328a1-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="328a1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="328a1-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="328a1-113">Methods</span></span>

<span data-ttu-id="328a1-114">La **classe \_ ATMAType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="328a1-114">The **MicrosoftDNS\_ATMAType** class has these methods.</span></span>



| <span data-ttu-id="328a1-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="328a1-115">Method</span></span>                             | <span data-ttu-id="328a1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="328a1-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="328a1-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="328a1-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="328a1-118">Crea un'istanza di un record di risorse ATMA basato sui dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario/nodo, la classe (impostazione predefinita = IN), il valore di durata (TTL) e il formato e l'indirizzo ATM.</span><span class="sxs-lookup"><span data-stu-id="328a1-118">Instantiates an ATMA Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Node Name, class (default = IN), time-to-live value, and ATM format and address.</span></span> <span data-ttu-id="328a1-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="328a1-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="328a1-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="328a1-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="328a1-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="328a1-121">**Modify**</span></span>                         | <span data-ttu-id="328a1-122">Aggiorna l'indirizzo TTL, format e ATMA ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="328a1-122">Updates the TTL, Format and ATMA Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="328a1-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="328a1-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="328a1-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="328a1-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="328a1-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="328a1-125">Qualifiers: Implemented</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="328a1-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="328a1-126">Properties</span></span>

<span data-ttu-id="328a1-127">La **classe \_ ATMAType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="328a1-127">The **MicrosoftDNS\_ATMAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="328a1-128">**ATMAddress**</span><span class="sxs-lookup"><span data-stu-id="328a1-128">**ATMAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="328a1-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="328a1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="328a1-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="328a1-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="328a1-131">Stringa di lunghezza variabile di ottetti che contiene l'indirizzo ATM del nodo/proprietario a cui si riferisce questo RR.</span><span class="sxs-lookup"><span data-stu-id="328a1-131">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="328a1-132">I primi 4 byte della matrice vengono usati per archiviare le dimensioni della stringa di ottetto.</span><span class="sxs-lookup"><span data-stu-id="328a1-132">The first 4 bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="328a1-133">Il byte più significativo viene archiviato nel byte 0.</span><span class="sxs-lookup"><span data-stu-id="328a1-133">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="328a1-134">**Formato**</span><span class="sxs-lookup"><span data-stu-id="328a1-134">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="328a1-135">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="328a1-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="328a1-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="328a1-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="328a1-137">Formato dell'indirizzo ATM.</span><span class="sxs-lookup"><span data-stu-id="328a1-137">ATM address format.</span></span> <span data-ttu-id="328a1-138">I valori validi sono: 0 che indica il formato AESA (ATM End System Address) e 1 che indica il formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="328a1-138">Valid values are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="328a1-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="328a1-139">Requirements</span></span>



| <span data-ttu-id="328a1-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="328a1-140">Requirement</span></span> | <span data-ttu-id="328a1-141">Valore</span><span class="sxs-lookup"><span data-stu-id="328a1-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="328a1-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="328a1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="328a1-143">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="328a1-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="328a1-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="328a1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="328a1-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="328a1-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="328a1-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="328a1-146">Namespace</span></span><br/>                | <span data-ttu-id="328a1-147">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="328a1-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="328a1-148">MOF</span><span class="sxs-lookup"><span data-stu-id="328a1-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="328a1-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="328a1-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="328a1-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="328a1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="328a1-151">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="328a1-151">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="328a1-152">**Metodo Modify della \_ classe ATMAType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="328a1-152">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="328a1-153">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="328a1-153">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





