---
description: Utilizzato per associare una macchina virtuale al relativo BIOS.
ms.assetid: 494E9D9F-64D5-49D5-A6C7-ABE469ABA4CA
title: Classe Msvm_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemBIOS
- Msvm_SystemBIOS.GroupComponent
- Msvm_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e1ad159a3ac0b86abd8b01e5c38105590ea8db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128422"
---
# <a name="msvm_systembios-class"></a><span data-ttu-id="a8ceb-103">\_Classe MSVM SystemBIOS</span><span class="sxs-lookup"><span data-stu-id="a8ceb-103">Msvm\_SystemBIOS class</span></span>

<span data-ttu-id="a8ceb-104">Utilizzato per associare una macchina virtuale al relativo BIOS.</span><span class="sxs-lookup"><span data-stu-id="a8ceb-104">Used to associate a virtual machine with its BIOS.</span></span>

<span data-ttu-id="a8ceb-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a8ceb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ceb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8ceb-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemBIOS : CIM_SystemBIOS
{
  CIM_ComputerSystem REF GroupComponent;
  Msvm_BIOSElement   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a8ceb-107">Members</span><span class="sxs-lookup"><span data-stu-id="a8ceb-107">Members</span></span>

<span data-ttu-id="a8ceb-108">La **classe \_ SystemBIOS di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a8ceb-108">The **Msvm\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="a8ceb-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a8ceb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8ceb-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a8ceb-110">Properties</span></span>

<span data-ttu-id="a8ceb-111">La **classe \_ SystemBIOS di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a8ceb-111">The **Msvm\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8ceb-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a8ceb-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8ceb-113">Tipo di dati: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="a8ceb-113">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a8ceb-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8ceb-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8ceb-115">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="a8ceb-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="a8ceb-116">Macchina virtuale che inizia dal BIOS.</span><span class="sxs-lookup"><span data-stu-id="a8ceb-116">The virtual machine that starts from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="a8ceb-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a8ceb-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8ceb-118">Tipo di dati: **[ **MSVM \_ bioselement**](msvm-bioselement.md)**</span><span class="sxs-lookup"><span data-stu-id="a8ceb-118">Data type: **[**Msvm\_BIOSElement**](msvm-bioselement.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a8ceb-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8ceb-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8ceb-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="a8ceb-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a8ceb-121">Il BIOS associato alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a8ceb-121">The BIOS associated with the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8ceb-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8ceb-122">Remarks</span></span>

<span data-ttu-id="a8ceb-123">L'accesso alla **classe \_ SystemBIOS di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="a8ceb-123">Access to the **Msvm\_SystemBIOS** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a8ceb-124">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a8ceb-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ceb-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8ceb-125">Requirements</span></span>



| <span data-ttu-id="a8ceb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8ceb-126">Requirement</span></span> | <span data-ttu-id="a8ceb-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a8ceb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ceb-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8ceb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a8ceb-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a8ceb-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a8ceb-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8ceb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a8ceb-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a8ceb-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a8ceb-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a8ceb-132">Namespace</span></span><br/>                | <span data-ttu-id="a8ceb-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a8ceb-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a8ceb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a8ceb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8ceb-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8ceb-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8ceb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a8ceb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8ceb-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a8ceb-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a8ceb-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8ceb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ceb-139">**\_SYSTEMBIOS CIM**</span><span class="sxs-lookup"><span data-stu-id="a8ceb-139">**CIM\_SystemBIOS**</span></span>](cim-systembios.md)
</dt> <dt>

[<span data-ttu-id="a8ceb-140">Classi BIOS</span><span class="sxs-lookup"><span data-stu-id="a8ceb-140">BIOS Classes</span></span>](bios-classes.md)
</dt> </dl>

 

