---
description: Classe astratta che rappresenta i dati runtime della porta raccolti da un'estensione del Commuter Ethernet.
ms.assetid: bc41ad1d-e7ab-4d04-96a8-26eb68ea6601
title: Classe Msvm_EthernetPortData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortData
- Msvm_EthernetPortData.InstanceID
- Msvm_EthernetPortData.Caption
- Msvm_EthernetPortData.Description
- Msvm_EthernetPortData.ElementName
- Msvm_EthernetPortData.SystemCreationClassName
- Msvm_EthernetPortData.SystemName
- Msvm_EthernetPortData.DeviceCreationClassName
- Msvm_EthernetPortData.DeviceID
- Msvm_EthernetPortData.CreationClassName
- Msvm_EthernetPortData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36167d4acad3c0da6b96efb9f9cc1fe58bd41a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882181"
---
# <a name="msvm_ethernetportdata-class"></a><span data-ttu-id="75fa1-103">\_Classe MSVM EthernetPortData</span><span class="sxs-lookup"><span data-stu-id="75fa1-103">Msvm\_EthernetPortData class</span></span>

<span data-ttu-id="75fa1-104">Classe astratta che rappresenta i dati runtime della porta raccolti da un'estensione del Commuter Ethernet.</span><span class="sxs-lookup"><span data-stu-id="75fa1-104">An abstract class that represents port runtime data collected by an Ethernet switch extension.</span></span> <span data-ttu-id="75fa1-105">Tutte le classi di dati della porta Ethernet devono derivare da questa classe astratta.</span><span class="sxs-lookup"><span data-stu-id="75fa1-105">All Ethernet port data classes must derive from this abstract class.</span></span>

<span data-ttu-id="75fa1-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="75fa1-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="75fa1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75fa1-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortData : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SystemCreationClassName;
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="75fa1-108">Members</span><span class="sxs-lookup"><span data-stu-id="75fa1-108">Members</span></span>

<span data-ttu-id="75fa1-109">La **classe \_ EthernetPortData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="75fa1-109">The **Msvm\_EthernetPortData** class has these types of members:</span></span>

-   [<span data-ttu-id="75fa1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="75fa1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="75fa1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="75fa1-111">Properties</span></span>

<span data-ttu-id="75fa1-112">La **classe \_ EthernetPortData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="75fa1-112">The **Msvm\_EthernetPortData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="75fa1-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="75fa1-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75fa1-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75fa1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75fa1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="75fa1-116">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="75fa1-116">A short description of the object.</span></span> <span data-ttu-id="75fa1-117">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="75fa1-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="75fa1-118">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="75fa1-118">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75fa1-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75fa1-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75fa1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="75fa1-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="75fa1-122">Nome della sottoclasse utilizzata per la creazione di questa istanza di dati di porta.</span><span class="sxs-lookup"><span data-stu-id="75fa1-122">The name of the subclass used in the creation of this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="75fa1-123">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="75fa1-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75fa1-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75fa1-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75fa1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="75fa1-126">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="75fa1-126">A description of the object.</span></span> <span data-ttu-id="75fa1-127">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="75fa1-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="75fa1-128">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="75fa1-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75fa1-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75fa1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75fa1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-131">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="75fa1-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="75fa1-132">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="75fa1-132">The scoping system's creation class name.</span></span> <span data-ttu-id="75fa1-133">Questa proprietà è sempre impostata su "MSVM \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="75fa1-133">This property is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="75fa1-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="75fa1-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75fa1-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75fa1-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75fa1-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-137">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="75fa1-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="75fa1-138">ID dispositivo della porta che ha come ambito questa istanza di dati di porta.</span><span class="sxs-lookup"><span data-stu-id="75fa1-138">The Device ID of the port that scopes this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="75fa1-139">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="75fa1-139">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75fa1-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75fa1-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75fa1-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="75fa1-142">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="75fa1-142">A display name for the object.</span></span> <span data-ttu-id="75fa1-143">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="75fa1-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="75fa1-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="75fa1-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75fa1-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75fa1-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75fa1-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-147">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="75fa1-147">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="75fa1-148">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="75fa1-148">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="75fa1-149">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="75fa1-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="75fa1-150">**Nome**</span><span class="sxs-lookup"><span data-stu-id="75fa1-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75fa1-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75fa1-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75fa1-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-153">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="75fa1-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="75fa1-154">Stringa che identifica in modo univoco questa istanza di dati di porta nell'ambito dell'opzione e della porta.</span><span class="sxs-lookup"><span data-stu-id="75fa1-154">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span>

</dd> <dt>

<span data-ttu-id="75fa1-155">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="75fa1-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75fa1-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75fa1-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75fa1-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-158">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**propagata**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="75fa1-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="75fa1-159">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="75fa1-159">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="75fa1-160">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="75fa1-160">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75fa1-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75fa1-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75fa1-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75fa1-163">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**propagata**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Nome**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="75fa1-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="75fa1-164">Nome del Commuter virtuale che ha come ambito questa istanza di dati di porta.</span><span class="sxs-lookup"><span data-stu-id="75fa1-164">The name of the virtual switch that scopes this port data instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75fa1-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75fa1-165">Requirements</span></span>



| <span data-ttu-id="75fa1-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="75fa1-166">Requirement</span></span> | <span data-ttu-id="75fa1-167">Valore</span><span class="sxs-lookup"><span data-stu-id="75fa1-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75fa1-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75fa1-168">Minimum supported client</span></span><br/> | <span data-ttu-id="75fa1-169">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="75fa1-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="75fa1-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75fa1-170">Minimum supported server</span></span><br/> | <span data-ttu-id="75fa1-171">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="75fa1-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75fa1-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="75fa1-172">Namespace</span></span><br/>                | <span data-ttu-id="75fa1-173">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="75fa1-173">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="75fa1-174">MOF</span><span class="sxs-lookup"><span data-stu-id="75fa1-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75fa1-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75fa1-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75fa1-176">DLL</span><span class="sxs-lookup"><span data-stu-id="75fa1-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75fa1-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75fa1-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

