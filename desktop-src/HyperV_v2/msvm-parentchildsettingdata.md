---
description: Associazione tra un'istanza di MSVM \_ VirtualSystemSettingData e l'istanza di MSVM \_ VirtualSystemSettingData che rappresenta lo snapshot più recente su cui si basa questo oggetto.
ms.assetid: F779775B-9AB3-4495-B6FF-9985FCDF63E4
title: Classe Msvm_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentChildSettingData
- Msvm_ParentChildSettingData.Antecedent
- Msvm_ParentChildSettingData.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 083de5f5d162f32fc9499a67b2ec991c6d3b398a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318321"
---
# <a name="msvm_parentchildsettingdata-class"></a><span data-ttu-id="88074-103">\_Classe MSVM ParentChildSettingData</span><span class="sxs-lookup"><span data-stu-id="88074-103">Msvm\_ParentChildSettingData class</span></span>

<span data-ttu-id="88074-104">Associazione tra un'istanza di [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) e l'istanza di **MSVM \_ VirtualSystemSettingData** che rappresenta lo snapshot più recente su cui si basa questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="88074-104">An association between an instance of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) and the **Msvm\_VirtualSystemSettingData** instance that represents the most recent snapshot upon which this object is based.</span></span>

<span data-ttu-id="88074-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="88074-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="88074-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88074-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentChildSettingData : CIM_Dependency
{
  Msvm_VirtualSystemSettingData REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="88074-107">Members</span><span class="sxs-lookup"><span data-stu-id="88074-107">Members</span></span>

<span data-ttu-id="88074-108">La **classe \_ ParentChildSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="88074-108">The **Msvm\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="88074-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="88074-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88074-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="88074-110">Properties</span></span>

<span data-ttu-id="88074-111">La **classe \_ ParentChildSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="88074-111">The **Msvm\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88074-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="88074-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88074-113">Tipo di dati: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="88074-113">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="88074-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="88074-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88074-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="88074-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="88074-116">I dati di impostazione dello snapshot su cui si basano i dati delle impostazioni figlio.</span><span class="sxs-lookup"><span data-stu-id="88074-116">The snapshot setting data upon which the child setting data is based.</span></span>

</dd> <dt>

<span data-ttu-id="88074-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="88074-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88074-118">Tipo di dati: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="88074-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="88074-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="88074-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88074-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. dependent")</span><span class="sxs-lookup"><span data-stu-id="88074-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="88074-121">Dati di impostazione per la macchina virtuale che rappresenta l'elemento figlio dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="88074-121">The setting data for the virtual machine that represents the child of the parent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88074-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="88074-122">Remarks</span></span>

<span data-ttu-id="88074-123">L'accesso alla **classe \_ ParentChildSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="88074-123">Access to the **Msvm\_ParentChildSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="88074-124">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="88074-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="88074-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88074-125">Requirements</span></span>



| <span data-ttu-id="88074-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="88074-126">Requirement</span></span> | <span data-ttu-id="88074-127">Valore</span><span class="sxs-lookup"><span data-stu-id="88074-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88074-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88074-128">Minimum supported client</span></span><br/> | <span data-ttu-id="88074-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="88074-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="88074-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88074-130">Minimum supported server</span></span><br/> | <span data-ttu-id="88074-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="88074-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88074-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88074-132">Namespace</span></span><br/>                | <span data-ttu-id="88074-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="88074-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="88074-134">MOF</span><span class="sxs-lookup"><span data-stu-id="88074-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88074-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88074-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="88074-136">DLL</span><span class="sxs-lookup"><span data-stu-id="88074-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88074-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88074-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="88074-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88074-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88074-139">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="88074-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="88074-140">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="88074-140">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> <dt>

[<span data-ttu-id="88074-141">Classi di sistema virtuali</span><span class="sxs-lookup"><span data-stu-id="88074-141">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

