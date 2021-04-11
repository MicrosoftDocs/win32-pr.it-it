---
description: Associa una macchina virtuale e i relativi dispositivi a istanze di CIM \_ SettingData che rappresentano le impostazioni correnti che si applicano a tali oggetti.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Classe Msvm_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232268"
---
# <a name="msvm_settingsdefinestate-class"></a><span data-ttu-id="112e5-103">\_Classe MSVM SettingsDefineState</span><span class="sxs-lookup"><span data-stu-id="112e5-103">Msvm\_SettingsDefineState class</span></span>

<span data-ttu-id="112e5-104">Associa una macchina virtuale e i relativi dispositivi a istanze di [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) che rappresentano le impostazioni correnti che si applicano a tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="112e5-104">Associates a virtual machine and its devices with instances of [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that represent the current settings that apply to these objects.</span></span> <span data-ttu-id="112e5-105">In particolare, associa [**MSVM \_ ComputerSystem**](msvm-computersystem.md) alle istanze di [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)e associa \**MSVM \_ \** _ derivati di [_ *CIM \_ LogicalDevice* \*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) con \**\_ \* MSVM* _ derivati di [_ *CIM \_ ResourceAllocationSettingData*. \*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)</span><span class="sxs-lookup"><span data-stu-id="112e5-105">More specifically, it associates [**Msvm\_ComputerSystem**](msvm-computersystem.md) with instances of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md), and it associates \**Msvm\_\** _ derivatives of [_ *CIM\_LogicalDevice*\*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) with \**Msvm\_\** _ derivatives of [_ *CIM\_ResourceAllocationSettingData*\*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="112e5-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="112e5-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="112e5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="112e5-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="112e5-108">Members</span><span class="sxs-lookup"><span data-stu-id="112e5-108">Members</span></span>

<span data-ttu-id="112e5-109">La **classe \_ SettingsDefineState di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="112e5-109">The **Msvm\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="112e5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="112e5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="112e5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="112e5-111">Properties</span></span>

<span data-ttu-id="112e5-112">La **classe \_ SettingsDefineState di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="112e5-112">The **Msvm\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="112e5-113">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="112e5-113">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112e5-114">Tipo di dati: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="112e5-114">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="112e5-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="112e5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="112e5-116">Riferimento alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="112e5-116">A reference to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="112e5-117">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="112e5-117">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112e5-118">Tipo di dati: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="112e5-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="112e5-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="112e5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="112e5-120">Un riferimento alle impostazioni attualmente attive per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="112e5-120">A reference to the currently active settings for the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="112e5-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="112e5-121">Remarks</span></span>

<span data-ttu-id="112e5-122">L'accesso alla **classe \_ SettingsDefineState di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="112e5-122">Access to the **Msvm\_SettingsDefineState** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="112e5-123">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="112e5-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="112e5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="112e5-124">Requirements</span></span>



| <span data-ttu-id="112e5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="112e5-125">Requirement</span></span> | <span data-ttu-id="112e5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="112e5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="112e5-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="112e5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="112e5-128">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="112e5-128">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="112e5-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="112e5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="112e5-130">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="112e5-130">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="112e5-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="112e5-131">Namespace</span></span><br/>                | <span data-ttu-id="112e5-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="112e5-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="112e5-133">MOF</span><span class="sxs-lookup"><span data-stu-id="112e5-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="112e5-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="112e5-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="112e5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="112e5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="112e5-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="112e5-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="112e5-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="112e5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112e5-138">**\_SETTINGSDEFINESTATE CIM**</span><span class="sxs-lookup"><span data-stu-id="112e5-138">**CIM\_SettingsDefineState**</span></span>](cim-settingsdefinestate.md)
</dt> <dt>

[<span data-ttu-id="112e5-139">**\_SETTINGSDEFINESTATE CIM**</span><span class="sxs-lookup"><span data-stu-id="112e5-139">**CIM\_SettingsDefineState**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[<span data-ttu-id="112e5-140">Classi di gestione del sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="112e5-140">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

