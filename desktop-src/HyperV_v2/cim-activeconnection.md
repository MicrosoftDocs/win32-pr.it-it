---
description: Definisce una connessione attualmente attivata e configurata per fornire la comunicazione tra due \_ oggetti CIM ServiceAccessPoint.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: Classe CIM_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActiveConnection
- CIM_ActiveConnection.Antecedent
- CIM_ActiveConnection.Dependent
- CIM_ActiveConnection.TrafficType
- CIM_ActiveConnection.OtherTrafficDescription
- CIM_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 644e8aaae1368e4164ceca7f7db29e343116c93c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308912"
---
# <a name="cim_activeconnection-class"></a><span data-ttu-id="dd6b7-103">CIM \_ ActiveConnection (classe)</span><span class="sxs-lookup"><span data-stu-id="dd6b7-103">CIM\_ActiveConnection class</span></span>

<span data-ttu-id="dd6b7-104">Definisce una connessione attualmente attivata e configurata per fornire la comunicazione tra due oggetti **CIM \_ serviceAccessPoint** .</span><span class="sxs-lookup"><span data-stu-id="dd6b7-104">Defines a connection that is currently turned on and configured to provide communication between two **CIM\_ServiceAccessPoint** objects.</span></span> <span data-ttu-id="dd6b7-105">**CIM \_ ActiveConnection** viene usato quando la connessione non viene trattata come un oggetto **CIM \_ managementelement** .</span><span class="sxs-lookup"><span data-stu-id="dd6b7-105">**CIM\_ActiveConnection** is used when the connection is not treated as a **CIM\_ManagedElement** object.</span></span> <span data-ttu-id="dd6b7-106">I punti di accesso al servizio connessi tramite una connessione attiva si trovano in genere nello stesso livello di rete o di applicazione.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-106">Service access points that are connected by an active connection are typically at the same networking or application layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd6b7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd6b7-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ActiveConnection : CIM_SAPSAPDependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     TrafficType;
  string                     OtherTrafficDescription;
  boolean                    IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="dd6b7-108">Members</span><span class="sxs-lookup"><span data-stu-id="dd6b7-108">Members</span></span>

<span data-ttu-id="dd6b7-109">La classe **CIM \_ ActiveConnection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dd6b7-109">The **CIM\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="dd6b7-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd6b7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd6b7-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd6b7-111">Properties</span></span>

<span data-ttu-id="dd6b7-112">La classe **CIM \_ ActiveConnection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-112">The **CIM\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd6b7-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="dd6b7-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6b7-114">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="dd6b7-114">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="dd6b7-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd6b7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6b7-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="dd6b7-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="dd6b7-117">Il punto di accesso al servizio connesso all'altro punto di accesso al servizio tramite la connessione attiva.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-117">The service access point that is connected to the other service access point through the active connection.</span></span> <span data-ttu-id="dd6b7-118">**CIM \_ Oggetto ServiceAccessPoint** .</span><span class="sxs-lookup"><span data-stu-id="dd6b7-118">**CIM\_ServiceAccessPoint** object.</span></span> <span data-ttu-id="dd6b7-119">In una connessione unidirezionale, questo punto di accesso è quello che trasmette i dati.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-119">In a unidirectional connection, this access point is the one that is transmitting data.</span></span>

</dd> <dt>

<span data-ttu-id="dd6b7-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="dd6b7-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6b7-121">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="dd6b7-121">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="dd6b7-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd6b7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6b7-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="dd6b7-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="dd6b7-124">Il punto di accesso al servizio configurato per comunicare o sta comunicando attivamente con il punto di accesso al servizio specificato nella proprietà **precedente** .</span><span class="sxs-lookup"><span data-stu-id="dd6b7-124">The service access point that is configured to communicate or is actively communicating with the service access point specified in the **Antecedent** property.</span></span> <span data-ttu-id="dd6b7-125">In una connessione unidirezionale, questo punto di accesso è quello che riceve i dati.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-125">In a unidirectional connection, this access point is the one that is receiving data.</span></span>

</dd> <dt>

<span data-ttu-id="dd6b7-126">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="dd6b7-126">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6b7-127">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dd6b7-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd6b7-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd6b7-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd6b7-129">True se la connessione è unidirezionale. false se la connessione è bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-129">True if the connection is unidirectional; false if the connection is bidirectional.</span></span> <span data-ttu-id="dd6b7-130">Quando la connessione è unidirezionale, la proprietà **antecedente** specifica il punto di accesso che trasmette i dati.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-130">When the connection is unidirectional, the **Antecedent** property specifies the access point that is transmitting data.</span></span> <span data-ttu-id="dd6b7-131">In una connessione bidirezionale, l'attività **precedente** può specificare uno dei punti di accesso assegnati alla connessione.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-131">In a bidirectional connection, **Antecedent** can specify either access point assigned to the connection.</span></span>

</dd> <dt>

<span data-ttu-id="dd6b7-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="dd6b7-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6b7-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd6b7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd6b7-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd6b7-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6b7-135">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**TrafficType**")</span><span class="sxs-lookup"><span data-stu-id="dd6b7-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**TrafficType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="dd6b7-136">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-136">This property is deprecated.</span></span> <span data-ttu-id="dd6b7-137">È invece consigliabile specificare queste informazioni nell'indirizzamento, nel protocollo e nella funzionalità di base degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-137">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="dd6b7-138">Descrizione del tipo di traffico specificato quando la proprietà **TrafficType** è impostata su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="dd6b7-138">A description of the traffic type that is specified when the **TrafficType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="dd6b7-139">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="dd6b7-139">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd6b7-140">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd6b7-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd6b7-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd6b7-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd6b7-142">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**OtherTrafficDescription**")</span><span class="sxs-lookup"><span data-stu-id="dd6b7-142">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**OtherTrafficDescription**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="dd6b7-143">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-143">This property is deprecated.</span></span> <span data-ttu-id="dd6b7-144">È invece consigliabile specificare queste informazioni nell'indirizzamento, nel protocollo e nella funzionalità di base degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-144">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="dd6b7-145">Tipo di traffico trasmesso sulla connessione.</span><span class="sxs-lookup"><span data-stu-id="dd6b7-145">The type of traffic that is transmitted over this connection.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd6b7-146">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="dd6b7-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd6b7-147">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="dd6b7-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

<span data-ttu-id="dd6b7-148">**Unicast** (2)</span><span class="sxs-lookup"><span data-stu-id="dd6b7-148">**Unicast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

<span data-ttu-id="dd6b7-149">**Broadcast** (3)</span><span class="sxs-lookup"><span data-stu-id="dd6b7-149">**Broadcast** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

<span data-ttu-id="dd6b7-150">**Multicast** (4)</span><span class="sxs-lookup"><span data-stu-id="dd6b7-150">**Multicast** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

<span data-ttu-id="dd6b7-151">**Anycast** (5)</span><span class="sxs-lookup"><span data-stu-id="dd6b7-151">**Anycast** (5)</span></span>


<span data-ttu-id="dd6b7-152"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dd6b7-152"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="dd6b7-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd6b7-153">Requirements</span></span>



| <span data-ttu-id="dd6b7-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd6b7-154">Requirement</span></span> | <span data-ttu-id="dd6b7-155">Valore</span><span class="sxs-lookup"><span data-stu-id="dd6b7-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd6b7-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd6b7-156">Minimum supported client</span></span><br/> | <span data-ttu-id="dd6b7-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dd6b7-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="dd6b7-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd6b7-158">Minimum supported server</span></span><br/> | <span data-ttu-id="dd6b7-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd6b7-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="dd6b7-160">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dd6b7-160">Namespace</span></span><br/>                | <span data-ttu-id="dd6b7-161">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="dd6b7-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd6b7-162">MOF</span><span class="sxs-lookup"><span data-stu-id="dd6b7-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd6b7-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd6b7-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd6b7-164">DLL</span><span class="sxs-lookup"><span data-stu-id="dd6b7-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd6b7-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd6b7-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd6b7-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd6b7-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd6b7-167">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="dd6b7-167">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

