---
description: Classe astratta che rappresenta una risorsa per un'istanza specifica di un commutere Ethernet.
ms.assetid: 5ae1be2a-8d59-4efe-a4ae-7cac1727cfa2
title: Classe Msvm_EthernetSwitchData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchData
- Msvm_EthernetSwitchData.InstanceID
- Msvm_EthernetSwitchData.Caption
- Msvm_EthernetSwitchData.Description
- Msvm_EthernetSwitchData.ElementName
- Msvm_EthernetSwitchData.SystemCreationClassName
- Msvm_EthernetSwitchData.SystemName
- Msvm_EthernetSwitchData.CreationClassName
- Msvm_EthernetSwitchData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dca2e4e01266a0a7da0f3ec85a86615406625f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312911"
---
# <a name="msvm_ethernetswitchdata-class"></a><span data-ttu-id="acfa3-103">\_Classe MSVM EthernetSwitchData</span><span class="sxs-lookup"><span data-stu-id="acfa3-103">Msvm\_EthernetSwitchData class</span></span>

<span data-ttu-id="acfa3-104">Classe astratta che rappresenta una risorsa per un'istanza specifica di un commutere Ethernet.</span><span class="sxs-lookup"><span data-stu-id="acfa3-104">Abstract class that represents a resource for a given instance of an Ethernet switch.</span></span>

<span data-ttu-id="acfa3-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="acfa3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="acfa3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="acfa3-106">Syntax</span></span>

``` syntax
[Abstract, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchData : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchBandwidthData";
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="acfa3-107">Members</span><span class="sxs-lookup"><span data-stu-id="acfa3-107">Members</span></span>

<span data-ttu-id="acfa3-108">La **classe \_ EthernetSwitchData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="acfa3-108">The **Msvm\_EthernetSwitchData** class has these types of members:</span></span>

-   [<span data-ttu-id="acfa3-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="acfa3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="acfa3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="acfa3-110">Properties</span></span>

<span data-ttu-id="acfa3-111">La **classe \_ EthernetSwitchData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="acfa3-111">The **Msvm\_EthernetSwitchData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="acfa3-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="acfa3-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acfa3-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acfa3-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acfa3-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="acfa3-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="acfa3-115">A short description of the object.</span></span> <span data-ttu-id="acfa3-116">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="acfa3-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="acfa3-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="acfa3-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acfa3-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acfa3-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acfa3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-120">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="acfa3-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="acfa3-121">Nome della classe o della sottoclasse utilizzata per la creazione di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="acfa3-121">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="acfa3-122">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="acfa3-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acfa3-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acfa3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acfa3-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="acfa3-125">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="acfa3-125">A description of the object.</span></span> <span data-ttu-id="acfa3-126">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="acfa3-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="acfa3-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="acfa3-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acfa3-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acfa3-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acfa3-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="acfa3-130">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="acfa3-130">A display name for the object.</span></span> <span data-ttu-id="acfa3-131">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="acfa3-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="acfa3-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="acfa3-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acfa3-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acfa3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acfa3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-135">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="acfa3-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="acfa3-136">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="acfa3-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="acfa3-137">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="acfa3-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="acfa3-138">**Nome**</span><span class="sxs-lookup"><span data-stu-id="acfa3-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acfa3-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acfa3-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acfa3-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-141">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="acfa3-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="acfa3-142">Nome univoco della risorsa.</span><span class="sxs-lookup"><span data-stu-id="acfa3-142">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="acfa3-143">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="acfa3-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acfa3-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acfa3-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acfa3-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-146">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**propagata**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="acfa3-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="acfa3-147">Nome della classe di creazione del sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="acfa3-147">The hosting system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="acfa3-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="acfa3-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acfa3-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acfa3-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acfa3-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acfa3-151">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**propagata**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Nome**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="acfa3-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="acfa3-152">Nome del commutire virtuale a cui è associata l'istanza della risorsa associata.</span><span class="sxs-lookup"><span data-stu-id="acfa3-152">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="acfa3-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acfa3-153">Requirements</span></span>



| <span data-ttu-id="acfa3-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="acfa3-154">Requirement</span></span> | <span data-ttu-id="acfa3-155">Valore</span><span class="sxs-lookup"><span data-stu-id="acfa3-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acfa3-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acfa3-156">Minimum supported client</span></span><br/> | <span data-ttu-id="acfa3-157">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="acfa3-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="acfa3-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acfa3-158">Minimum supported server</span></span><br/> | <span data-ttu-id="acfa3-159">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="acfa3-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="acfa3-160">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="acfa3-160">Namespace</span></span><br/>                | <span data-ttu-id="acfa3-161">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="acfa3-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="acfa3-162">MOF</span><span class="sxs-lookup"><span data-stu-id="acfa3-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acfa3-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="acfa3-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="acfa3-164">DLL</span><span class="sxs-lookup"><span data-stu-id="acfa3-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acfa3-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="acfa3-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

