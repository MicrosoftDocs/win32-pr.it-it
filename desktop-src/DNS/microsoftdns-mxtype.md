---
title: Classe MicrosoftDNS_MXType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta uno scambio di posta elettronica (Mr) RR.
ms.assetid: 7c147628-5bda-48dd-beb4-e630d1886da8
keywords:
- DNS della classe MicrosoftDNS_MXType
- MicrosoftDNS_MXType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
- MicrosoftDNS_MXType.Modify
- MicrosoftDNS_MXType.Preference
- MicrosoftDNS_MXType.MailExchange
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652743178b71b2f9fed296ecfa4427f85b5cf1c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964222"
---
# <a name="microsoftdns_mxtype-class"></a><span data-ttu-id="89ac9-105">\_Classe MicrosoftDNS MXType</span><span class="sxs-lookup"><span data-stu-id="89ac9-105">MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="89ac9-106">Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta uno scambio di posta elettronica (Mr) RR.</span><span class="sxs-lookup"><span data-stu-id="89ac9-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Exchanger (MR) RR.</span></span>

<span data-ttu-id="89ac9-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="89ac9-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="89ac9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89ac9-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MXType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string MailExchange;
};
```

## <a name="members"></a><span data-ttu-id="89ac9-109">Members</span><span class="sxs-lookup"><span data-stu-id="89ac9-109">Members</span></span>

<span data-ttu-id="89ac9-110">La **classe \_ MXType di MicrosoftDNS** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="89ac9-110">The **MicrosoftDNS\_MXType** class has these types of members:</span></span>

-   [<span data-ttu-id="89ac9-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="89ac9-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="89ac9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89ac9-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="89ac9-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="89ac9-113">Methods</span></span>

<span data-ttu-id="89ac9-114">La **classe \_ MXType di MicrosoftDNS** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="89ac9-114">The **MicrosoftDNS\_MXType** class has these methods.</span></span>



| <span data-ttu-id="89ac9-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="89ac9-115">Method</span></span>                             | <span data-ttu-id="89ac9-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89ac9-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89ac9-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="89ac9-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="89ac9-118">Crea un'istanza di un tipo MX di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore time-to-Live, la preferenza di record e il nome host disposti come scambio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="89ac9-118">Instantiates an MX Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, record preference, and host name willing to be a mail exchange.</span></span> <span data-ttu-id="89ac9-119">Restituisce un riferimento al nuovo oggetto come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="89ac9-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="89ac9-120">Qualificatori: implementata, statica</span><span class="sxs-lookup"><span data-stu-id="89ac9-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="89ac9-121">**Modifica**</span><span class="sxs-lookup"><span data-stu-id="89ac9-121">**Modify**</span></span>                         | <span data-ttu-id="89ac9-122">Aggiorna la durata (TTL), la preferenza e lo scambio di posta elettronica ai valori specificati come parametri di input di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="89ac9-122">Updates the TTL, Preference, and Mail Exchange to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="89ac9-123">Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="89ac9-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="89ac9-124">Il metodo restituisce un riferimento all'oggetto modificato come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="89ac9-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="89ac9-125">Qualificatori: implementato</span><span class="sxs-lookup"><span data-stu-id="89ac9-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="89ac9-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89ac9-126">Properties</span></span>

<span data-ttu-id="89ac9-127">La **classe \_ MXType di MicrosoftDNS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="89ac9-127">The **MicrosoftDNS\_MXType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89ac9-128">**MailExchange**</span><span class="sxs-lookup"><span data-stu-id="89ac9-128">**MailExchange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89ac9-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89ac9-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89ac9-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89ac9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89ac9-131">FQDN che specifica un host disposto a fungere da scambio di posta elettronica per il nome del proprietario.</span><span class="sxs-lookup"><span data-stu-id="89ac9-131">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="89ac9-132">**Preferenza**</span><span class="sxs-lookup"><span data-stu-id="89ac9-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89ac9-133">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89ac9-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89ac9-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89ac9-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89ac9-135">Preferenza assegnata a questo RR tra gli altri nello stesso proprietario.</span><span class="sxs-lookup"><span data-stu-id="89ac9-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="89ac9-136">Sono preferibili valori inferiori.</span><span class="sxs-lookup"><span data-stu-id="89ac9-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89ac9-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89ac9-137">Requirements</span></span>



| <span data-ttu-id="89ac9-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="89ac9-138">Requirement</span></span> | <span data-ttu-id="89ac9-139">Valore</span><span class="sxs-lookup"><span data-stu-id="89ac9-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89ac9-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89ac9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="89ac9-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="89ac9-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="89ac9-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89ac9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="89ac9-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89ac9-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="89ac9-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89ac9-144">Namespace</span></span><br/>                | <span data-ttu-id="89ac9-145">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="89ac9-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="89ac9-146">MOF</span><span class="sxs-lookup"><span data-stu-id="89ac9-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89ac9-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89ac9-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89ac9-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89ac9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89ac9-149">**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="89ac9-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="89ac9-150">**Metodo Modify della \_ classe MXType di MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="89ac9-150">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="89ac9-151">**\_ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="89ac9-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





