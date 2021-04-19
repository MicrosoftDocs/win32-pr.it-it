---
description: Definisce i mezzi mediante i quali un client può individuare l'intervallo valido di impostazioni predefinite per una funzionalità del comcambio Ethernet.
ms.assetid: 84ae7656-2cc4-4ca7-b4ae-95d9905c9aad
title: Classe Msvm_EthernetSwitchFeatureCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureCapabilities
- Msvm_EthernetSwitchFeatureCapabilities.InstanceID
- Msvm_EthernetSwitchFeatureCapabilities.Caption
- Msvm_EthernetSwitchFeatureCapabilities.Description
- Msvm_EthernetSwitchFeatureCapabilities.ElementName
- Msvm_EthernetSwitchFeatureCapabilities.FeatureId
- Msvm_EthernetSwitchFeatureCapabilities.Applicability
- Msvm_EthernetSwitchFeatureCapabilities.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ba145ca6a43a2031a676e565f38210dc6771f40e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320035"
---
# <a name="msvm_ethernetswitchfeaturecapabilities-class"></a><span data-ttu-id="1c576-103">\_Classe MSVM EthernetSwitchFeatureCapabilities</span><span class="sxs-lookup"><span data-stu-id="1c576-103">Msvm\_EthernetSwitchFeatureCapabilities class</span></span>

<span data-ttu-id="1c576-104">Definisce i mezzi mediante i quali un client può individuare l'intervallo valido di impostazioni predefinite per una funzionalità del comcambio Ethernet.</span><span class="sxs-lookup"><span data-stu-id="1c576-104">Defines the means by which a client can discover the valid range of default settings for an Ethernet switch feature.</span></span> <span data-ttu-id="1c576-105">Un oggetto **MSVM \_ EthernetSwitchFeatureCapabilities** è associato a ogni Commuter Ethernet virtuale, per ogni funzionalità supportata dal Commuter.</span><span class="sxs-lookup"><span data-stu-id="1c576-105">An **Msvm\_EthernetSwitchFeatureCapabilities** object is associated with each virtual Ethernet switch, for each feature that the switch supports.</span></span> <span data-ttu-id="1c576-106">Quattro [**oggetti \_ EthernetSwitchFeatureSettingData di MSVM**](msvm-ethernetswitchfeaturesettingdata.md) sono associati all'oggetto **MSVM \_ EthernetSwitchFeatureCapabilities** per descrivere i valori minimo, massimo, predefinito e incrementale per le funzionalità della funzionalità dell'opzione specificata.</span><span class="sxs-lookup"><span data-stu-id="1c576-106">Four [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) objects are associated with the **Msvm\_EthernetSwitchFeatureCapabilities** object to describe the minimum, maximum, default, and incremental values for the given switch's feature capabilities.</span></span>

<span data-ttu-id="1c576-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1c576-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c576-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c576-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = " Ethernet Switch Feature Capabilities";
  string Description = "Microsoft Virtual Ethernet Switch Feature Capabilities";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  string FeatureId;
  uint16 Applicability;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="1c576-109">Members</span><span class="sxs-lookup"><span data-stu-id="1c576-109">Members</span></span>

<span data-ttu-id="1c576-110">La **classe \_ EthernetSwitchFeatureCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1c576-110">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="1c576-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1c576-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c576-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1c576-112">Properties</span></span>

<span data-ttu-id="1c576-113">La **classe \_ EthernetSwitchFeatureCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c576-113">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c576-114">**Applicabilità**</span><span class="sxs-lookup"><span data-stu-id="1c576-114">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c576-115">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c576-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c576-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c576-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c576-117">Descrive se questa funzionalità viene applicata a un compartitore Ethernet o a una porta di commutazione Ethernet particolare.</span><span class="sxs-lookup"><span data-stu-id="1c576-117">Describes whether this feature is applied to an Ethernet switch or a particular Ethernet switch port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c576-118">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="1c576-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Port"></span><span id="port"></span><span id="PORT"></span>

<span data-ttu-id="1c576-119">**Porta** (1)</span><span class="sxs-lookup"><span data-stu-id="1c576-119">**Port** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="1c576-120">**Switch** (2)</span><span class="sxs-lookup"><span data-stu-id="1c576-120">**Switch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c576-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="1c576-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c576-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1c576-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c576-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c576-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c576-124">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="1c576-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="1c576-125">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1c576-125">A short description of the object.</span></span> <span data-ttu-id="1c576-126">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1c576-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c576-127">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1c576-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c576-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1c576-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c576-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c576-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c576-130">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="1c576-130">A description of the object.</span></span> <span data-ttu-id="1c576-131">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1c576-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c576-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1c576-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c576-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1c576-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c576-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c576-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c576-135">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1c576-135">A display name for the object.</span></span> <span data-ttu-id="1c576-136">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1c576-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c576-137">**FeatureId**</span><span class="sxs-lookup"><span data-stu-id="1c576-137">**FeatureId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c576-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1c576-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c576-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c576-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c576-140">Identificatore della funzionalità per cui questo oggetto fornisce informazioni sulle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1c576-140">The identifier of the feature this object provides capabilities information for.</span></span>

</dd> <dt>

<span data-ttu-id="1c576-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1c576-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c576-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1c576-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c576-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c576-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c576-144">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="1c576-144">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1c576-145">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="1c576-145">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1c576-146">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1c576-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c576-147">**Versione**</span><span class="sxs-lookup"><span data-stu-id="1c576-147">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c576-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1c576-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c576-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c576-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c576-150">Versione della funzionalità in un formato "Major. minor", ad esempio "2,0".</span><span class="sxs-lookup"><span data-stu-id="1c576-150">The version of the feature in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c576-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c576-151">Requirements</span></span>



| <span data-ttu-id="1c576-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c576-152">Requirement</span></span> | <span data-ttu-id="1c576-153">Valore</span><span class="sxs-lookup"><span data-stu-id="1c576-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c576-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c576-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1c576-155">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1c576-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1c576-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c576-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1c576-157">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1c576-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c576-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1c576-158">Namespace</span></span><br/>                | <span data-ttu-id="1c576-159">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1c576-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1c576-160">MOF</span><span class="sxs-lookup"><span data-stu-id="1c576-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c576-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c576-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c576-162">DLL</span><span class="sxs-lookup"><span data-stu-id="1c576-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c576-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1c576-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

