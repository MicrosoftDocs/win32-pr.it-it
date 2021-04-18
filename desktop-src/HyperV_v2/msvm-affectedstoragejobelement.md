---
description: Rappresenta l'associazione tra un processo e gli elementi gestiti che potrebbero essere interessati dalla relativa esecuzione.
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Classe Msvm_AffectedStorageJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d900f42e5022301a08ebeee0036400be3a2f1bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305656"
---
# <a name="msvm_affectedstoragejobelement-class"></a><span data-ttu-id="b1c3b-103">\_Classe MSVM AffectedStorageJobElement</span><span class="sxs-lookup"><span data-stu-id="b1c3b-103">Msvm\_AffectedStorageJobElement class</span></span>

<span data-ttu-id="b1c3b-104">Rappresenta l'associazione tra un processo e gli elementi gestiti che potrebbero essere interessati dalla relativa esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-104">Represents the association between a job and the managed elements that may be affected by its execution.</span></span>

<span data-ttu-id="b1c3b-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1c3b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1c3b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="b1c3b-107">Members</span><span class="sxs-lookup"><span data-stu-id="b1c3b-107">Members</span></span>

<span data-ttu-id="b1c3b-108">La **classe \_ AffectedStorageJobElement di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b1c3b-108">The **Msvm\_AffectedStorageJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="b1c3b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1c3b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1c3b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1c3b-110">Properties</span></span>

<span data-ttu-id="b1c3b-111">La **classe \_ AffectedStorageJobElement di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-111">The **Msvm\_AffectedStorageJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1c3b-112">**Interessato**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1c3b-113">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="b1c3b-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1c3b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1c3b-115">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b1c3b-116">Elemento gestito interessato dall'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-116">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="b1c3b-117">Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b1c3b-117">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b1c3b-118">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1c3b-119">Tipo di dati: **[ **MSVM \_ StorageJob**](msvm-storagejob.md)**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-119">Data type: **[**Msvm\_StorageJob**](msvm-storagejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b1c3b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1c3b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1c3b-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ AffectedJobElement. AffectingElement")</span><span class="sxs-lookup"><span data-stu-id="b1c3b-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_AffectedJobElement.AffectingElement")</span></span>
</dt> </dl>

<span data-ttu-id="b1c3b-122">Processo che influisce sull'elemento interessato.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-122">The job that is affecting the affected element.</span></span> <span data-ttu-id="b1c3b-123">Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b1c3b-123">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b1c3b-124">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-124">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1c3b-125">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b1c3b-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1c3b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1c3b-127">Enumerazione che descrive l'effetto sull'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-127">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="b1c3b-128">Questa matrice corrisponde alla matrice di proprietà **OtherElementEffectsDescriptions** , in cui quest'ultimo fornisce dettagli correlati agli effetti di alto livello enumerati da questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-128">This array corresponds to the **OtherElementEffectsDescriptions** property array, where the latter provides details related to the high-level effects enumerated by this property.</span></span> <span data-ttu-id="b1c3b-129">Sono necessari ulteriori dettagli se la matrice di proprietà **ElementEffects** contiene il valore 1, (other).</span><span class="sxs-lookup"><span data-stu-id="b1c3b-129">Additional detail is required if the **ElementEffects** property array contains the value 1, (Other).</span></span> <span data-ttu-id="b1c3b-130">Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b1c3b-130">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b1c3b-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b1c3b-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b1c3b-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b1c3b-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b1c3b-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Utilizzo esclusivo** (2)</span><span class="sxs-lookup"><span data-stu-id="b1c3b-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Exclusive Use** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b1c3b-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Effetti sulle prestazioni** (3)</span><span class="sxs-lookup"><span data-stu-id="b1c3b-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Performance Impact** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b1c3b-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Integrità elementi** (4)</span><span class="sxs-lookup"><span data-stu-id="b1c3b-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Element Integrity** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b1c3b-136">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-136">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1c3b-137">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b1c3b-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1c3b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1c3b-139">Fornisce informazioni dettagliate sull'effetto in corrispondenza della posizione della matrice corrispondente nella matrice di proprietà **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="b1c3b-139">Provides details for the effect at the corresponding array position in the **ElementEffects** property array.</span></span> <span data-ttu-id="b1c3b-140">Queste informazioni sono necessarie ogni volta che l'elemento corrispondente nella matrice di proprietà **ElementEffects** contiene il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="b1c3b-140">This information is required whenever the corresponding element in the **ElementEffects** property array contains the value 1 (Other).</span></span> <span data-ttu-id="b1c3b-141">Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b1c3b-141">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1c3b-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1c3b-142">Remarks</span></span>

<span data-ttu-id="b1c3b-143">L'accesso alla **classe \_ AffectedStorageJobElement di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="b1c3b-143">Access to the **Msvm\_AffectedStorageJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b1c3b-144">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b1c3b-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1c3b-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1c3b-145">Requirements</span></span>



| <span data-ttu-id="b1c3b-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1c3b-146">Requirement</span></span> | <span data-ttu-id="b1c3b-147">Valore</span><span class="sxs-lookup"><span data-stu-id="b1c3b-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1c3b-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1c3b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b1c3b-149">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b1c3b-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b1c3b-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1c3b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b1c3b-151">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b1c3b-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b1c3b-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1c3b-152">Namespace</span></span><br/>                | <span data-ttu-id="b1c3b-153">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b1c3b-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b1c3b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="b1c3b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1c3b-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1c3b-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1c3b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="b1c3b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1c3b-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b1c3b-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b1c3b-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1c3b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1c3b-159">**\_AFFECTEDJOBELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b1c3b-159">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="b1c3b-160">[**\_AFFECTEDJOBELEMENT CIM**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1c3b-160">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b1c3b-161">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b1c3b-161">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

