---
description: Rappresenta un'associazione tra un processo e l'elemento gestito che può essere influenzato dalla relativa esecuzione.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Classe Msvm_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bef667872a7afa4c726ee1b2c77a36c29649114d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315918"
---
# <a name="msvm_affectedjobelement-class"></a><span data-ttu-id="57a2f-103">\_Classe MSVM AffectedJobElement</span><span class="sxs-lookup"><span data-stu-id="57a2f-103">Msvm\_AffectedJobElement class</span></span>

<span data-ttu-id="57a2f-104">Rappresenta un'associazione tra un processo e l'elemento gestito che può essere influenzato dalla relativa esecuzione.</span><span class="sxs-lookup"><span data-stu-id="57a2f-104">Represents an association between a job and the managed element that may be affected by its execution.</span></span>

<span data-ttu-id="57a2f-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="57a2f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a2f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57a2f-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="57a2f-107">Members</span><span class="sxs-lookup"><span data-stu-id="57a2f-107">Members</span></span>

<span data-ttu-id="57a2f-108">La **classe \_ AffectedJobElement di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="57a2f-108">The **Msvm\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="57a2f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57a2f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57a2f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57a2f-110">Properties</span></span>

<span data-ttu-id="57a2f-111">La **classe \_ AffectedJobElement di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="57a2f-111">The **Msvm\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57a2f-112">**Interessato**</span><span class="sxs-lookup"><span data-stu-id="57a2f-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57a2f-113">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="57a2f-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="57a2f-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57a2f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57a2f-115">Elemento gestito interessato dall'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="57a2f-115">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="57a2f-116">Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57a2f-116">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="57a2f-117">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="57a2f-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57a2f-118">Tipo di dati: **[ **MSVM \_ ConcreteJob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="57a2f-118">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="57a2f-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57a2f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57a2f-120">Processo che influisce sull'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="57a2f-120">The job that is affecting the managed element.</span></span> <span data-ttu-id="57a2f-121">Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57a2f-121">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="57a2f-122">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="57a2f-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57a2f-123">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57a2f-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="57a2f-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57a2f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57a2f-125">Enumerazione che descrive l'effetto sull'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="57a2f-125">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="57a2f-126">Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57a2f-126">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="57a2f-127">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="57a2f-127">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57a2f-128">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="57a2f-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="57a2f-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57a2f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57a2f-130">Fornisce informazioni dettagliate sull'effetto in corrispondenza della posizione della matrice corrispondente in **ElementEffects**.</span><span class="sxs-lookup"><span data-stu-id="57a2f-130">Provides details for the effect at the corresponding array position in **ElementEffects**.</span></span> <span data-ttu-id="57a2f-131">Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57a2f-131">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57a2f-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="57a2f-132">Remarks</span></span>

<span data-ttu-id="57a2f-133">L'accesso alla **classe \_ AffectedJobElement di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="57a2f-133">Access to the **Msvm\_AffectedJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="57a2f-134">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="57a2f-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="57a2f-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57a2f-135">Requirements</span></span>



| <span data-ttu-id="57a2f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a2f-136">Requirement</span></span> | <span data-ttu-id="57a2f-137">Valore</span><span class="sxs-lookup"><span data-stu-id="57a2f-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a2f-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57a2f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="57a2f-139">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="57a2f-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="57a2f-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57a2f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="57a2f-141">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="57a2f-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57a2f-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="57a2f-142">Namespace</span></span><br/>                | <span data-ttu-id="57a2f-143">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="57a2f-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="57a2f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="57a2f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57a2f-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57a2f-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="57a2f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="57a2f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57a2f-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="57a2f-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="57a2f-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57a2f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a2f-149">**\_AFFECTEDJOBELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="57a2f-149">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="57a2f-150">[**\_AFFECTEDJOBELEMENT CIM**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="57a2f-150">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="57a2f-151">Classi di gestione del sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="57a2f-151">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

