---
description: La \_ classe CIM IRQ rappresenta un IRQ (Intel Architecture interrupt request line).
ms.assetid: d72d4914-c57b-496d-a9fe-d8f5b522504c
ms.tgt_platform: multiple
title: Classe CIM_IRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_IRQ
- CIM_IRQ.Caption
- CIM_IRQ.Description
- CIM_IRQ.InstallDate
- CIM_IRQ.Name
- CIM_IRQ.Status
- CIM_IRQ.Availability
- CIM_IRQ.CreationClassName
- CIM_IRQ.CSCreationClassName
- CIM_IRQ.CSName
- CIM_IRQ.IRQNumber
- CIM_IRQ.Shareable
- CIM_IRQ.TriggerLevel
- CIM_IRQ.TriggerType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03a336caa02c766160fe6501f91b28f06a872ecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877890"
---
# <a name="cim_irq-class"></a><span data-ttu-id="fd30d-103">\_Classe IRQ CIM</span><span class="sxs-lookup"><span data-stu-id="fd30d-103">CIM\_IRQ class</span></span>

<span data-ttu-id="fd30d-104">La classe **CIM \_ IRQ** rappresenta un IRQ (Intel Architecture interrupt request line).</span><span class="sxs-lookup"><span data-stu-id="fd30d-104">The **CIM\_IRQ** class represents an Intel architecture interrupt request line (IRQ).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd30d-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="fd30d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fd30d-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fd30d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fd30d-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fd30d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fd30d-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="fd30d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd30d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd30d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_IRQ : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint32   IRQNumber;
  boolean  Shareable;
  uint16   TriggerLevel;
  uint16   TriggerType;
};
```

## <a name="members"></a><span data-ttu-id="fd30d-110">Members</span><span class="sxs-lookup"><span data-stu-id="fd30d-110">Members</span></span>

<span data-ttu-id="fd30d-111">La classe **CIM \_ IRQ** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fd30d-111">The **CIM\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="fd30d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd30d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd30d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd30d-113">Properties</span></span>

<span data-ttu-id="fd30d-114">La classe **CIM \_ IRQ** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fd30d-114">The **CIM\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd30d-115">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="fd30d-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd30d-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-118">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="fd30d-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-119">Disponibilità dell'IRQ.</span><span class="sxs-lookup"><span data-stu-id="fd30d-119">Availability of the IRQ.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd30d-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fd30d-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd30d-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fd30d-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="fd30d-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponibile** (3)</span><span class="sxs-lookup"><span data-stu-id="fd30d-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="fd30d-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In uso/non disponibile** (4)</span><span class="sxs-lookup"><span data-stu-id="fd30d-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="fd30d-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In uso e disponibile/condivisibile** (5)</span><span class="sxs-lookup"><span data-stu-id="fd30d-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fd30d-125">In uso e disponibile/condivisibile</span><span class="sxs-lookup"><span data-stu-id="fd30d-125">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd30d-126">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="fd30d-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd30d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-129">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="fd30d-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-130">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fd30d-130">A short textual description of the object.</span></span>

<span data-ttu-id="fd30d-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd30d-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd30d-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fd30d-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd30d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-135">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fd30d-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-136">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="fd30d-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="fd30d-137">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="fd30d-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="fd30d-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fd30d-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd30d-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-141">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fd30d-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-142">Nome della classe di creazione dell'ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="fd30d-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="fd30d-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="fd30d-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd30d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-146">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fd30d-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-147">Nome del sistema del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="fd30d-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="fd30d-148">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="fd30d-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd30d-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-151">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="fd30d-151">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-152">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fd30d-152">A textual description of the object.</span></span>

<span data-ttu-id="fd30d-153">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd30d-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd30d-154">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fd30d-154">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-155">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fd30d-155">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-157">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="fd30d-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-158">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="fd30d-158">Indicates when the object was installed.</span></span> <span data-ttu-id="fd30d-159">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="fd30d-159">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="fd30d-160">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd30d-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd30d-161">**IRQNumber**</span><span class="sxs-lookup"><span data-stu-id="fd30d-161">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd30d-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-164">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,1 "), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd30d-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-165">Parte del valore di chiave dell'oggetto, numero IRQ.</span><span class="sxs-lookup"><span data-stu-id="fd30d-165">Part of the object's key value, IRQ number.</span></span>

</dd> <dt>

<span data-ttu-id="fd30d-166">**Nome**</span><span class="sxs-lookup"><span data-stu-id="fd30d-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd30d-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-169">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="fd30d-169">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-170">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="fd30d-170">Label by which the object is known.</span></span> <span data-ttu-id="fd30d-171">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="fd30d-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="fd30d-172">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd30d-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd30d-173">**Condivisibile**</span><span class="sxs-lookup"><span data-stu-id="fd30d-173">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-174">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fd30d-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-176">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="fd30d-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-177">Se **true**, l'IRQ può essere condiviso.</span><span class="sxs-lookup"><span data-stu-id="fd30d-177">If **TRUE**, the IRQ can be shared.</span></span>

</dd> <dt>

<span data-ttu-id="fd30d-178">**Status**</span><span class="sxs-lookup"><span data-stu-id="fd30d-178">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd30d-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-181">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="fd30d-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-182">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fd30d-182">String that indicates the current status of the object.</span></span> <span data-ttu-id="fd30d-183">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="fd30d-183">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="fd30d-184">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="fd30d-184">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="fd30d-185">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="fd30d-185">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="fd30d-186">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="fd30d-186">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fd30d-187">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="fd30d-187">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fd30d-188">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="fd30d-188">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fd30d-189">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd30d-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fd30d-190">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd30d-190">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fd30d-191">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="fd30d-191">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fd30d-192">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="fd30d-192">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fd30d-193">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="fd30d-193">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd30d-194">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="fd30d-194">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fd30d-195">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="fd30d-195">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fd30d-196">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="fd30d-196">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fd30d-197">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="fd30d-197">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fd30d-198">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="fd30d-198">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fd30d-199">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="fd30d-199">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fd30d-200">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="fd30d-200">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fd30d-201">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="fd30d-201">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fd30d-202">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="fd30d-202">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd30d-203">**TriggerLevel**</span><span class="sxs-lookup"><span data-stu-id="fd30d-203">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-204">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd30d-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-206">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni sull'IRQ delle risorse di sistema \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="fd30d-206">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-207">Indica se l'interruzione viene attivata dal segnale hardware in alto o in basso.</span><span class="sxs-lookup"><span data-stu-id="fd30d-207">Indicates whether the interruption is triggered by the hardware signal going high or low.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd30d-208">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fd30d-208">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd30d-209">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fd30d-209">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="fd30d-210">**Attivo basso** (3)</span><span class="sxs-lookup"><span data-stu-id="fd30d-210">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="fd30d-211">**Attivo alto** (4)</span><span class="sxs-lookup"><span data-stu-id="fd30d-211">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd30d-212">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="fd30d-212">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd30d-213">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd30d-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd30d-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd30d-215">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,3 "," MIF. DMTF \| informazioni sull'IRQ delle risorse di sistema \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="fd30d-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="fd30d-216">Tipo di interruzione che può verificarsi.</span><span class="sxs-lookup"><span data-stu-id="fd30d-216">Type of interruption that can occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd30d-217">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fd30d-217">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd30d-218">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="fd30d-218">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="fd30d-219">**Livello** (3)</span><span class="sxs-lookup"><span data-stu-id="fd30d-219">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="fd30d-220">**Edge** (4)</span><span class="sxs-lookup"><span data-stu-id="fd30d-220">**Edge** (4)</span></span>


<span data-ttu-id="fd30d-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fd30d-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="fd30d-222">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd30d-222">Remarks</span></span>

<span data-ttu-id="fd30d-223">La classe **CIM \_ IRQ** è derivata da [**CIM \_ SystemResource**](cim-systemresource.md). WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="fd30d-223">The **CIM\_IRQ** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).WMI does not implement this class.</span></span> <span data-ttu-id="fd30d-224">Vedere [le classi Win32](win32-provider.md) per le classi derivate da **\_ IRQ CIM**.</span><span class="sxs-lookup"><span data-stu-id="fd30d-224">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_IRQ**.</span></span>

<span data-ttu-id="fd30d-225">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="fd30d-225">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fd30d-226">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="fd30d-226">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd30d-227">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd30d-227">Requirements</span></span>



| <span data-ttu-id="fd30d-228">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd30d-228">Requirement</span></span> | <span data-ttu-id="fd30d-229">Valore</span><span class="sxs-lookup"><span data-stu-id="fd30d-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd30d-230">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd30d-230">Minimum supported client</span></span><br/> | <span data-ttu-id="fd30d-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd30d-231">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd30d-232">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd30d-232">Minimum supported server</span></span><br/> | <span data-ttu-id="fd30d-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd30d-233">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd30d-234">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fd30d-234">Namespace</span></span><br/>                | <span data-ttu-id="fd30d-235">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fd30d-235">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd30d-236">MOF</span><span class="sxs-lookup"><span data-stu-id="fd30d-236">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd30d-237"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd30d-237"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd30d-238">DLL</span><span class="sxs-lookup"><span data-stu-id="fd30d-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd30d-239"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd30d-239"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd30d-240">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd30d-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd30d-241">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="fd30d-241">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

