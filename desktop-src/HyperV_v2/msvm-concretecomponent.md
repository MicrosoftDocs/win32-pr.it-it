---
description: Associazione generica utilizzata per stabilire parte delle relazioni tra gli elementi gestiti.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Classe Msvm_ConcreteComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2ef9e286f4c7ca296ee6b3638ffb9511ccea4115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314340"
---
# <a name="msvm_concretecomponent-class"></a><span data-ttu-id="30d3e-103">\_Classe MSVM ConcreteComponent</span><span class="sxs-lookup"><span data-stu-id="30d3e-103">Msvm\_ConcreteComponent class</span></span>

<span data-ttu-id="30d3e-104">Associazione generica utilizzata per stabilire le relazioni ' parte di ' tra gli elementi gestiti.</span><span class="sxs-lookup"><span data-stu-id="30d3e-104">A generic association used to establish 'part of' relationships between managed elements.</span></span> <span data-ttu-id="30d3e-105">[**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) è definito come una sottoclasse concreta della classe del [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component) astratta, da usare al posto di molte sottoclassi specifiche del componente che non aggiungono alcuna semantica (ovvero sottoclassi che non chiariscono il tipo di composizione, aggiornano le cardinalità o aggiungono o rimuovono i qualificatori).</span><span class="sxs-lookup"><span data-stu-id="30d3e-105">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) is defined as a concrete subclass of the abstract [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component) class, to be used in place of many specific subclasses of component that add no semantics (that is subclasses that do not clarify the type of composition, update cardinalities, or add or remove qualifiers.)</span></span>

<span data-ttu-id="30d3e-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="30d3e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="30d3e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30d3e-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="30d3e-108">Members</span><span class="sxs-lookup"><span data-stu-id="30d3e-108">Members</span></span>

<span data-ttu-id="30d3e-109">La **classe \_ ConcreteComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="30d3e-109">The **Msvm\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="30d3e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="30d3e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30d3e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="30d3e-111">Properties</span></span>

<span data-ttu-id="30d3e-112">La **classe \_ ConcreteComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="30d3e-112">The **Msvm\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30d3e-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="30d3e-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30d3e-114">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="30d3e-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="30d3e-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30d3e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30d3e-116">Elemento padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="30d3e-116">The parent element in the association.</span></span> <span data-ttu-id="30d3e-117">Questa proprietà viene ereditata da [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="30d3e-117">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="30d3e-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="30d3e-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30d3e-119">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="30d3e-119">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="30d3e-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30d3e-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30d3e-121">Elemento figlio nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="30d3e-121">The child element in the association.</span></span> <span data-ttu-id="30d3e-122">Questa proprietà viene ereditata da [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="30d3e-122">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30d3e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="30d3e-123">Remarks</span></span>

<span data-ttu-id="30d3e-124">L'accesso alla **classe \_ ConcreteComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="30d3e-124">Access to the **Msvm\_ConcreteComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="30d3e-125">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="30d3e-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="30d3e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30d3e-126">Requirements</span></span>



| <span data-ttu-id="30d3e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="30d3e-127">Requirement</span></span> | <span data-ttu-id="30d3e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="30d3e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30d3e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30d3e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="30d3e-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="30d3e-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="30d3e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30d3e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="30d3e-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="30d3e-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30d3e-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="30d3e-133">Namespace</span></span><br/>                | <span data-ttu-id="30d3e-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="30d3e-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="30d3e-135">MOF</span><span class="sxs-lookup"><span data-stu-id="30d3e-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30d3e-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30d3e-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="30d3e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="30d3e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30d3e-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="30d3e-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="30d3e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30d3e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30d3e-140">**\_CONCRETECOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="30d3e-140">**CIM\_ConcreteComponent**</span></span>](cim-concretecomponent.md)
</dt> <dt>

<span data-ttu-id="30d3e-141">[**\_CONCRETECOMPONENT CIM**](/previous-versions//cc150665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="30d3e-141">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="30d3e-142">Classi di sistema virtuali</span><span class="sxs-lookup"><span data-stu-id="30d3e-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

