---
title: Classe MicrosoftDNS_AFSDBType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record del server di database del file System Andrew (AFSDB).
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- DNS della classe MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 836de50f4da9e613fb3e940b90971f38a634c804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048380"
---
# <a name="microsoftdns_afsdbtype-class"></a><span data-ttu-id="fec8a-105">\_Classe MicrosoftDNS AFSDBType</span><span class="sxs-lookup"><span data-stu-id="fec8a-105">MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="fec8a-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record del server di database del file System Andrew (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="fec8a-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an Andrew File System Database Server (AFSDB) record.</span></span>

<span data-ttu-id="fec8a-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="fec8a-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fec8a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fec8a-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a><span data-ttu-id="fec8a-109">Members</span><span class="sxs-lookup"><span data-stu-id="fec8a-109">Members</span></span>

<span data-ttu-id="fec8a-110">La **classe \_ AFSDBType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fec8a-110">The **MicrosoftDNS\_AFSDBType** class has these types of members:</span></span>

-   [<span data-ttu-id="fec8a-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="fec8a-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fec8a-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fec8a-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fec8a-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="fec8a-113">Methods</span></span>

<span data-ttu-id="fec8a-114">La **classe \_ AFSDBType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="fec8a-114">The **MicrosoftDNS\_AFSDBType** class has these methods.</span></span>



| <span data-ttu-id="fec8a-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="fec8a-115">Method</span></span>                             | <span data-ttu-id="fec8a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fec8a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec8a-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="fec8a-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fec8a-118">Crea un'istanza di un record di risorse AFSDB in base ai dati nei parametri di input del metodo, ovvero il nome del server DNS del record, il nome del contenitore, il nome della cella e del proprietario, la classe (impostazione predefinita = IN), il valore time-to-Live e il sottotipo e il nome del server AFS host.</span><span class="sxs-lookup"><span data-stu-id="fec8a-118">Instantiates an AFSDB Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Cell Name, class (default = IN), time-to-live value, and host AFS server subtype and name.</span></span> <span data-ttu-id="fec8a-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="fec8a-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fec8a-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="fec8a-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fec8a-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="fec8a-121">**Modify**</span></span>                         | <span data-ttu-id="fec8a-122">Questo metodo aggiorna il nome del server e del sottotipo TTL ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fec8a-122">This method updates the TTL, Subtype and Server Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fec8a-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="fec8a-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fec8a-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="fec8a-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fec8a-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="fec8a-125">Qualifiers: Implemented</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="fec8a-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fec8a-126">Properties</span></span>

<span data-ttu-id="fec8a-127">La **classe \_ AFSDBType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fec8a-127">The **MicrosoftDNS\_AFSDBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fec8a-128">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="fec8a-128">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec8a-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fec8a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fec8a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fec8a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fec8a-131">FQDN che specifica un host con un server per la cella AFS specificata nel nome del proprietario.</span><span class="sxs-lookup"><span data-stu-id="fec8a-131">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="fec8a-132">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="fec8a-132">**Subtype**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec8a-133">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fec8a-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fec8a-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fec8a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fec8a-135">Sottotipo del server AFS host.</span><span class="sxs-lookup"><span data-stu-id="fec8a-135">Subtype of the host AFS server.</span></span> <span data-ttu-id="fec8a-136">Per il sottotipo 1 (valore = 1), l'host dispone di un server del percorso del volume AFS versione 3,0 per la cella AFS denominata.</span><span class="sxs-lookup"><span data-stu-id="fec8a-136">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="fec8a-137">Nel caso del sottotipo 2 (valore = 2), l'host dispone di un server dei nomi autenticato che contiene il nodo della directory radice della cella per la cella DCE/autorità di certificazione denominata.</span><span class="sxs-lookup"><span data-stu-id="fec8a-137">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fec8a-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fec8a-138">Requirements</span></span>



| <span data-ttu-id="fec8a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec8a-139">Requirement</span></span> | <span data-ttu-id="fec8a-140">Valore</span><span class="sxs-lookup"><span data-stu-id="fec8a-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fec8a-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fec8a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fec8a-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fec8a-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fec8a-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fec8a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fec8a-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fec8a-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fec8a-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fec8a-145">Namespace</span></span><br/>                | <span data-ttu-id="fec8a-146">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="fec8a-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fec8a-147">MOF</span><span class="sxs-lookup"><span data-stu-id="fec8a-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fec8a-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fec8a-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec8a-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fec8a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec8a-150">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="fec8a-150">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fec8a-151">**Metodo Modify della \_ classe AFSDBType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="fec8a-151">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="fec8a-152">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="fec8a-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





