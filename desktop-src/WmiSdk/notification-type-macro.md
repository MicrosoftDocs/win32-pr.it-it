---
description: La macro del tipo di notifica contiene gli elementi seguenti.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: Macro del tipo di notifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308846"
---
# <a name="notification-type-macro"></a><span data-ttu-id="a7d5b-103">Macro del tipo di notifica</span><span class="sxs-lookup"><span data-stu-id="a7d5b-103">NOTIFICATION-TYPE Macro</span></span>

<span data-ttu-id="a7d5b-104">La macro del tipo di notifica contiene gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-104">The NOTIFICATION-TYPE macro contains the following elements.</span></span>

> [!Note]  
> <span data-ttu-id="a7d5b-105">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a7d5b-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="a7d5b-106">Componenti</span><span class="sxs-lookup"><span data-stu-id="a7d5b-106">Components</span></span>

<dl> <dt>

<span data-ttu-id="a7d5b-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descrittore di oggetto</span><span class="sxs-lookup"><span data-stu-id="a7d5b-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="a7d5b-108">Connette un nome a un evento SNMP in una macro del tipo di notifica.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-108">Attaches a name to an SNMP event in a NOTIFICATION-TYPE macro.</span></span> <span data-ttu-id="a7d5b-109">Nell'elenco seguente sono elencate le regole per il mapping del descrittore di oggetti.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-109">The following list lists the rules for mapping the object descriptor.</span></span>



| <span data-ttu-id="a7d5b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7d5b-110">Type</span></span>                        | <span data-ttu-id="a7d5b-111">Concatenate</span><span class="sxs-lookup"><span data-stu-id="a7d5b-111">Concatenate</span></span>                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d5b-112">Nome classe CIM incapsulato</span><span class="sxs-lookup"><span data-stu-id="a7d5b-112">Encapsulated CIM class name</span></span> | <span data-ttu-id="a7d5b-113">"SNMP \_ "</span><span class="sxs-lookup"><span data-stu-id="a7d5b-113">"SNMP\_"</span></span><br/> <span data-ttu-id="a7d5b-114">Nome identità modulo MIB</span><span class="sxs-lookup"><span data-stu-id="a7d5b-114">MIB module identity name</span></span><br/> <span data-ttu-id="a7d5b-115">carattere di sottolineatura ( \_ )</span><span class="sxs-lookup"><span data-stu-id="a7d5b-115">underscore (\_)</span></span><br/> <span data-ttu-id="a7d5b-116">descrittore di oggetto</span><span class="sxs-lookup"><span data-stu-id="a7d5b-116">object descriptor</span></span><br/> <span data-ttu-id="a7d5b-117">" \_ Notifica"</span><span class="sxs-lookup"><span data-stu-id="a7d5b-117">"\_Notification"</span></span><br/> <span data-ttu-id="a7d5b-118">Esempio: la notifica **vtpServerDisabled** da **Cisco-VTP-MIB** esegue il mapping alla **\_ notifica SNMP Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_**.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-118">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_Notification**.</span></span><br/>                 |
| <span data-ttu-id="a7d5b-119">Nome della classe CIM riferente</span><span class="sxs-lookup"><span data-stu-id="a7d5b-119">Referent CIM class name</span></span>     | <span data-ttu-id="a7d5b-120">"SNMP \_ "</span><span class="sxs-lookup"><span data-stu-id="a7d5b-120">"SNMP\_"</span></span><br/> <span data-ttu-id="a7d5b-121">Nome identità modulo MIB</span><span class="sxs-lookup"><span data-stu-id="a7d5b-121">MIB module identity name</span></span><br/> <span data-ttu-id="a7d5b-122">carattere di sottolineatura ( \_ )</span><span class="sxs-lookup"><span data-stu-id="a7d5b-122">underscore (\_)</span></span><br/> <span data-ttu-id="a7d5b-123">descrittore di oggetto</span><span class="sxs-lookup"><span data-stu-id="a7d5b-123">object descriptor</span></span><br/> <span data-ttu-id="a7d5b-124">" \_ ExtendedNotification"</span><span class="sxs-lookup"><span data-stu-id="a7d5b-124">"\_ExtendedNotification"</span></span><br/> <span data-ttu-id="a7d5b-125">Esempio: la notifica **vtpServerDisabled** da **Cisco-VTP-MIB** viene mappata a **SNMP \_ Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-125">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_ExtendedNotification**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a7d5b-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>Clausola OBJECTs</span><span class="sxs-lookup"><span data-stu-id="a7d5b-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTS clause</span></span>
</dt> <dd>

<span data-ttu-id="a7d5b-127">Enumera il set di oggetti associati all'oggetto notifica.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-127">Enumerates the set of objects associated with the notification object.</span></span>

</dd> <dt>

<span data-ttu-id="a7d5b-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Clausola REFERENCE</span><span class="sxs-lookup"><span data-stu-id="a7d5b-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="a7d5b-129">Fa riferimento a un altro documento che contiene ulteriori informazioni sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-129">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="a7d5b-130">Viene eseguito il mapping al **riferimento** al qualificatore di classe CIM, che è di tipo String.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-130">It maps to the CIM class qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="a7d5b-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Clausola DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a7d5b-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="a7d5b-132">Descrive l'oggetto in questione.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-132">Describes the object in question.</span></span> <span data-ttu-id="a7d5b-133">Esegue il mapping alla **Descrizione** del qualificatore di classe CIM, che è di tipo stringa</span><span class="sxs-lookup"><span data-stu-id="a7d5b-133">It maps to the CIM class qualifier **Description**, which is of type string</span></span>

</dd> <dt>

<span data-ttu-id="a7d5b-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Clausola STATUS</span><span class="sxs-lookup"><span data-stu-id="a7d5b-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="a7d5b-135">Indica se l'oggetto deve essere supportato.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-135">Indicates whether the object must be supported.</span></span> <span data-ttu-id="a7d5b-136">Quando lo stato è **obsoleto** o **deprecato**, la notifica viene eliminata dal mapping.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-136">When the status is either **obsolete** or **deprecated**, the notification is discarded from the mapping.</span></span> <span data-ttu-id="a7d5b-137">In caso contrario, questa clausola esegue il mapping allo **stato** del qualificatore della classe CIM, che è di tipo **String**.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-137">Otherwise, this clause maps to the CIM class qualifier **Status**, which is of type **string**.</span></span>

<span data-ttu-id="a7d5b-138">Per SNMPv1, il valore preferito dello **stato** è **obbligatorio** o **facoltativo**, ma il qualificatore può contenere un altro valore.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-138">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="a7d5b-139">Per SNMPv2C, il valore preferito dello **stato** è **Current** o **deprecato**, ma il qualificatore può contenere un altro valore.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-139">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7d5b-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7d5b-140">Remarks</span></span>

<span data-ttu-id="a7d5b-141">Il provider SNMP esegue il mapping della macro del **tipo di notifica** a una definizione di classe incapsulata o referente.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-141">The SNMP provider maps the **NOTIFICATION-TYPE** macro to either an encapsulated or referent class definition.</span></span>

<span data-ttu-id="a7d5b-142">Una definizione di classe incapsulata non espone le informazioni sull'istanza associate all'oggetto MIB.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-142">An encapsulated class definition does not expose the instance information associated with the MIB object.</span></span> <span data-ttu-id="a7d5b-143">Al contrario, la definizione di classe codifica la clausola OBJECTs come una serie di proprietà della classe di evento CIM.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-143">Instead, the class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="a7d5b-144">Ogni proprietà CIM riflette il nome, il tipo e il valore dell'oggetto MIB corrispondente nella clausola OBJECTs.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-144">Each CIM property reflects the name, type, and value of the corresponding MIB object in the OBJECTS clause.</span></span> <span data-ttu-id="a7d5b-145">Se sono necessarie informazioni sull'istanza, è necessario eseguire il mapping a una classe referente.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-145">If you require instance information, you must map to a referent class.</span></span> <span data-ttu-id="a7d5b-146">Viene eseguito il mapping di una definizione di classe incapsulata alla classe [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="a7d5b-146">An encapsulated class definition maps to the [SnmpNotification](snmpnotification.md) class.</span></span>

<span data-ttu-id="a7d5b-147">Una classe referente definisce un oggetto MIB e le informazioni sull'istanza utilizzate per ottenere l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-147">A referent class defines an MIB object and the instance information used to obtain the object.</span></span> <span data-ttu-id="a7d5b-148">La definizione di classe codifica la clausola OBJECTs come una serie di proprietà della classe di evento CIM.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-148">The class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="a7d5b-149">Ogni proprietà CIM riflette il nome dell'oggetto MIB corrispondente nella clausola OBJECTs e il tipo come oggetto incorporato che riflette un'istanza della classe associata a tale oggetto MIB.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-149">Each CIM property reflects the name of the corresponding MIB object in the OBJECTS clause and the type as an embedded object that reflects an instance of the class associated with that MIB object.</span></span> <span data-ttu-id="a7d5b-150">Il provider genera quindi una classe associata all'oggetto MIB.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-150">The provider then generates a class associated with the MIB object.</span></span> <span data-ttu-id="a7d5b-151">Ad esempio, **ifindex** esegue il mapping a una classe incorporata denominata **SNMP \_ RFC1213 \_ MIB \_ ifindex**.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-151">For example, **ifIndex** maps to an embedded class named **SNMP\_RFC1213\_MIB\_ifIndex**.</span></span> <span data-ttu-id="a7d5b-152">Per ulteriori informazioni su questo tipo di classe, vedere [macro di tipo di oggetto](object-type-macro.md).</span><span class="sxs-lookup"><span data-stu-id="a7d5b-152">For more information about this type of class, see [OBJECT-TYPE Macro](object-type-macro.md).</span></span>

 

 




