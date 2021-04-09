---
description: Associa un'istanza di macchina virtuale al servizio di gestione che ne controlla lo stato.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Classe Msvm_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129999"
---
# <a name="msvm_serviceaffectselement-class"></a><span data-ttu-id="2def3-103">\_Classe MSVM ServiceAffectsElement</span><span class="sxs-lookup"><span data-stu-id="2def3-103">Msvm\_ServiceAffectsElement class</span></span>

<span data-ttu-id="2def3-104">Associa un'istanza di macchina virtuale al servizio di gestione che ne controlla lo stato.</span><span class="sxs-lookup"><span data-stu-id="2def3-104">Associates a virtual machine instance with the management service that controls its state.</span></span>

<span data-ttu-id="2def3-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2def3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2def3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2def3-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="2def3-107">Members</span><span class="sxs-lookup"><span data-stu-id="2def3-107">Members</span></span>

<span data-ttu-id="2def3-108">La **classe \_ ServiceAffectsElement di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2def3-108">The **Msvm\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="2def3-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2def3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2def3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2def3-110">Properties</span></span>

<span data-ttu-id="2def3-111">La **classe \_ ServiceAffectsElement di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2def3-111">The **Msvm\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2def3-112">**Interessato**</span><span class="sxs-lookup"><span data-stu-id="2def3-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2def3-113">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="2def3-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="2def3-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2def3-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2def3-115">Riferimento alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2def3-115">A reference to the virtual machine.</span></span> <span data-ttu-id="2def3-116">Questa proprietà viene ereditata da [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2def3-116">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2def3-117">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="2def3-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2def3-118">Tipo di dati: **[ **\_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="2def3-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="2def3-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2def3-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2def3-120">Riferimento al servizio che controlla la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2def3-120">A reference to the service that controls the virtual machine.</span></span> <span data-ttu-id="2def3-121">Questa proprietà viene ereditata da [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2def3-121">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2def3-122">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="2def3-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2def3-123">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2def3-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2def3-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2def3-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2def3-125">Specifica il tipo di controllo rappresentato dall'associazione.</span><span class="sxs-lookup"><span data-stu-id="2def3-125">Specifies the type of control that the association represents.</span></span> <span data-ttu-id="2def3-126">Questa proprietà viene ereditata da [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))ed è sempre impostata sul valore seguente.</span><span class="sxs-lookup"><span data-stu-id="2def3-126">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to the following value.</span></span>



| <span data-ttu-id="2def3-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2def3-127">Value</span></span>                                                                        | <span data-ttu-id="2def3-128">Significato</span><span class="sxs-lookup"><span data-stu-id="2def3-128">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="2def3-129"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2def3-129"><dt>5</dt></span></span> </dl> | <span data-ttu-id="2def3-130">Gestisce</span><span class="sxs-lookup"><span data-stu-id="2def3-130">Manages</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2def3-131">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2def3-131">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2def3-132">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2def3-132">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2def3-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2def3-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2def3-134">Dettagli per il tipo di associazione nella posizione della matrice corrispondente nella matrice di proprietà **ElementAffects** .</span><span class="sxs-lookup"><span data-stu-id="2def3-134">The details for the type of association at the corresponding array position in the **ElementAffects** property array.</span></span> <span data-ttu-id="2def3-135">Queste informazioni sono obbligatorie se **ElementAffects** è impostato su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="2def3-135">This information is required if **ElementAffects** is set to 1 (Other).</span></span> <span data-ttu-id="2def3-136">Questa proprietà viene ereditata da [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="2def3-136">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2def3-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="2def3-137">Remarks</span></span>

<span data-ttu-id="2def3-138">L'accesso alla **classe \_ ServiceAffectsElement di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="2def3-138">Access to the **Msvm\_ServiceAffectsElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2def3-139">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2def3-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2def3-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2def3-140">Requirements</span></span>



| <span data-ttu-id="2def3-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2def3-141">Requirement</span></span> | <span data-ttu-id="2def3-142">Valore</span><span class="sxs-lookup"><span data-stu-id="2def3-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2def3-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2def3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2def3-144">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2def3-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2def3-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2def3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2def3-146">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2def3-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2def3-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2def3-147">Namespace</span></span><br/>                | <span data-ttu-id="2def3-148">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2def3-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2def3-149">MOF</span><span class="sxs-lookup"><span data-stu-id="2def3-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2def3-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2def3-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2def3-151">DLL</span><span class="sxs-lookup"><span data-stu-id="2def3-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2def3-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2def3-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2def3-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2def3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2def3-154">**\_SERVICEAFFECTSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="2def3-154">**CIM\_ServiceAffectsElement**</span></span>](cim-serviceaffectselement.md)
</dt> <dt>

<span data-ttu-id="2def3-155">[**\_SERVICEAFFECTSELEMENT CIM**](/previous-versions//cc136907(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2def3-155">[**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))</span></span>
</dt> </dl>

 

