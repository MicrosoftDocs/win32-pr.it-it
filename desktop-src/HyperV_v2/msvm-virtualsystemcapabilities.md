---
description: Descrive le funzionalità del ComputerSystem MSVM associato \_ .
ms.assetid: 7e3b51ba-f85d-4b83-abc6-a094d412eca1
title: Classe Msvm_VirtualSystemCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCapabilities
- Msvm_VirtualSystemCapabilities.InstanceID
- Msvm_VirtualSystemCapabilities.Caption
- Msvm_VirtualSystemCapabilities.Description
- Msvm_VirtualSystemCapabilities.ElementName
- Msvm_VirtualSystemCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemCapabilities.MaxElementNameLen
- Msvm_VirtualSystemCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9fbd9b747e85ec1c9a1b7754f99282a7d913994e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225910"
---
# <a name="msvm_virtualsystemcapabilities-class"></a><span data-ttu-id="9d248-103">\_Classe MSVM VirtualSystemCapabilities</span><span class="sxs-lookup"><span data-stu-id="9d248-103">Msvm\_VirtualSystemCapabilities class</span></span>

<span data-ttu-id="9d248-104">Descrive le funzionalità del [**\_ ComputerSystem MSVM**](msvm-computersystem.md)associato.</span><span class="sxs-lookup"><span data-stu-id="9d248-104">Describes the capabilities of the associated [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="9d248-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9d248-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d248-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d248-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Capabilities";
  string  Description = "Defines Virtual System Capabilities";
  string  ElementName = "Hyper-V Virtual System Capabilities";
  boolean ElementNameEditSupported = True;
  unit16  MaxElementNameLen = 100;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="9d248-107">Members</span><span class="sxs-lookup"><span data-stu-id="9d248-107">Members</span></span>

<span data-ttu-id="9d248-108">La **classe \_ VirtualSystemCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9d248-108">The **Msvm\_VirtualSystemCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="9d248-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d248-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d248-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d248-110">Properties</span></span>

<span data-ttu-id="9d248-111">La **classe \_ VirtualSystemCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9d248-111">The **Msvm\_VirtualSystemCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d248-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="9d248-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d248-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d248-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d248-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d248-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d248-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9d248-115">A short description of the object.</span></span> <span data-ttu-id="9d248-116">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d248-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d248-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9d248-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d248-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d248-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d248-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d248-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d248-120">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="9d248-120">A description of the object.</span></span> <span data-ttu-id="9d248-121">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d248-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d248-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9d248-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d248-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d248-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d248-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d248-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d248-125">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9d248-125">A display name for the object.</span></span> <span data-ttu-id="9d248-126">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d248-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d248-127">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="9d248-127">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d248-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9d248-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d248-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d248-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d248-130">Indica se la proprietà **ElementName** può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="9d248-130">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="9d248-131">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="9d248-131">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="9d248-132">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="9d248-132">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d248-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d248-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d248-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d248-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d248-135">Specifica le restrizioni per **ElementName**, espresse come espressione regolare.</span><span class="sxs-lookup"><span data-stu-id="9d248-135">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="9d248-136">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="9d248-136">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="9d248-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9d248-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d248-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d248-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d248-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d248-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d248-140">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="9d248-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9d248-141">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="9d248-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9d248-142">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d248-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d248-143">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="9d248-143">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d248-144">Tipo di dati: **unit16**</span><span class="sxs-lookup"><span data-stu-id="9d248-144">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="9d248-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d248-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d248-146">Qualificatori: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="9d248-146">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="9d248-147">Specifica la lunghezza massima supportata della proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="9d248-147">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="9d248-148">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="9d248-148">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="9d248-149">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="9d248-149">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d248-150">Tipo di dati: matrice **unit16**</span><span class="sxs-lookup"><span data-stu-id="9d248-150">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="9d248-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d248-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d248-152">Indica gli stati possibili che è possibile richiedere quando si utilizza il metodo **RequestStateChange** sull'elemento logico Enabled.</span><span class="sxs-lookup"><span data-stu-id="9d248-152">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="9d248-153">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="9d248-153">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="9d248-154">Valore</span><span class="sxs-lookup"><span data-stu-id="9d248-154">Value</span></span>                                                                         | <span data-ttu-id="9d248-155">Significato</span><span class="sxs-lookup"><span data-stu-id="9d248-155">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="9d248-156"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9d248-156"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="9d248-157">Abilitato</span><span class="sxs-lookup"><span data-stu-id="9d248-157">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="9d248-158"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9d248-158"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="9d248-159">Disabilita</span><span class="sxs-lookup"><span data-stu-id="9d248-159">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="9d248-160"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9d248-160"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="9d248-161">Arresta</span><span class="sxs-lookup"><span data-stu-id="9d248-161">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="9d248-162"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9d248-162"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="9d248-163">Offline</span><span class="sxs-lookup"><span data-stu-id="9d248-163">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="9d248-164"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9d248-164"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="9d248-165">Test</span><span class="sxs-lookup"><span data-stu-id="9d248-165">Test</span></span><br/>      |
| <dl> <span data-ttu-id="9d248-166"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9d248-166"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="9d248-167">Rinviare</span><span class="sxs-lookup"><span data-stu-id="9d248-167">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="9d248-168"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9d248-168"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="9d248-169">Disattivazione</span><span class="sxs-lookup"><span data-stu-id="9d248-169">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="9d248-170"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9d248-170"><dt>10</dt></span></span> </dl> | <span data-ttu-id="9d248-171">Riavvio</span><span class="sxs-lookup"><span data-stu-id="9d248-171">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="9d248-172"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="9d248-172"><dt>11</dt></span></span> </dl> | <span data-ttu-id="9d248-173">Reset</span><span class="sxs-lookup"><span data-stu-id="9d248-173">Reset</span></span><br/>     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d248-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d248-174">Requirements</span></span>



| <span data-ttu-id="9d248-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d248-175">Requirement</span></span> | <span data-ttu-id="9d248-176">Valore</span><span class="sxs-lookup"><span data-stu-id="9d248-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d248-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d248-177">Minimum supported client</span></span><br/> | <span data-ttu-id="9d248-178">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9d248-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9d248-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d248-179">Minimum supported server</span></span><br/> | <span data-ttu-id="9d248-180">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9d248-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d248-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d248-181">Namespace</span></span><br/>                | <span data-ttu-id="9d248-182">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9d248-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9d248-183">MOF</span><span class="sxs-lookup"><span data-stu-id="9d248-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d248-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d248-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d248-185">DLL</span><span class="sxs-lookup"><span data-stu-id="9d248-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d248-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d248-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

