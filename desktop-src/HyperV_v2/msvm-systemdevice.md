---
description: Associa un dispositivo logico al sistema padre.
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Classe Msvm_SystemDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemDevice
- Msvm_SystemDevice.GroupComponent
- Msvm_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be31a51ad4e24bd31785e64400bf5b266624d8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306023"
---
# <a name="msvm_systemdevice-class"></a><span data-ttu-id="040ae-103">\_Classe MSVM SystemDevice</span><span class="sxs-lookup"><span data-stu-id="040ae-103">Msvm\_SystemDevice class</span></span>

<span data-ttu-id="040ae-104">I dispositivi logici possono essere aggregati da un sistema.</span><span class="sxs-lookup"><span data-stu-id="040ae-104">Logical devices can be aggregated by a system.</span></span> <span data-ttu-id="040ae-105">Questa relazione viene resa esplicita dall'associazione di dispositivi di sistema.</span><span class="sxs-lookup"><span data-stu-id="040ae-105">This relationship is made explicit by the system device association.</span></span>

<span data-ttu-id="040ae-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="040ae-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="040ae-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="040ae-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="040ae-108">Members</span><span class="sxs-lookup"><span data-stu-id="040ae-108">Members</span></span>

<span data-ttu-id="040ae-109">La **classe \_ SystemDevice di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="040ae-109">The **Msvm\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="040ae-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="040ae-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="040ae-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="040ae-111">Properties</span></span>

<span data-ttu-id="040ae-112">La **classe \_ SystemDevice di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="040ae-112">The **Msvm\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="040ae-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="040ae-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="040ae-114">Tipo di dati: **[ **\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="040ae-114">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="040ae-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="040ae-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="040ae-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="040ae-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="040ae-117">Sistema padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="040ae-117">The parent system in the association.</span></span> <span data-ttu-id="040ae-118">Questa proprietà viene ereditata [**dal \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="040ae-118">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="040ae-119">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="040ae-119">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="040ae-120">Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="040ae-120">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="040ae-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="040ae-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="040ae-122">Il dispositivo logico che è un elemento di un sistema.</span><span class="sxs-lookup"><span data-stu-id="040ae-122">The logical device that is an element of a system.</span></span> <span data-ttu-id="040ae-123">Questa proprietà viene ereditata [**dal \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="040ae-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="040ae-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="040ae-124">Remarks</span></span>

<span data-ttu-id="040ae-125">L'accesso alla **classe \_ SystemDevice di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="040ae-125">Access to the **Msvm\_SystemDevice** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="040ae-126">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="040ae-126">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="040ae-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="040ae-127">Requirements</span></span>



| <span data-ttu-id="040ae-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="040ae-128">Requirement</span></span> | <span data-ttu-id="040ae-129">Valore</span><span class="sxs-lookup"><span data-stu-id="040ae-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="040ae-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="040ae-130">Minimum supported client</span></span><br/> | <span data-ttu-id="040ae-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="040ae-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="040ae-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="040ae-132">Minimum supported server</span></span><br/> | <span data-ttu-id="040ae-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="040ae-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="040ae-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="040ae-134">Namespace</span></span><br/>                | <span data-ttu-id="040ae-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="040ae-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="040ae-136">MOF</span><span class="sxs-lookup"><span data-stu-id="040ae-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="040ae-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="040ae-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="040ae-138">DLL</span><span class="sxs-lookup"><span data-stu-id="040ae-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="040ae-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="040ae-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="040ae-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="040ae-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="040ae-141">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="040ae-141">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="040ae-142">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="040ae-142">**CIM\_SystemDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[<span data-ttu-id="040ae-143">Classi di sistema virtuali</span><span class="sxs-lookup"><span data-stu-id="040ae-143">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

