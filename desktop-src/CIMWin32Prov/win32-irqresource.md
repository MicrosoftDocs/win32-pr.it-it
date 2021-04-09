---
description: Win32 \_ IRQResource &\# 160; La classe WMI rappresenta un numero di riga di richiesta di interrupt (IRQ) in un sistema di computer che esegue Windows.
ms.assetid: bae0c28e-2b66-40ac-9679-b2dfe9269306
ms.tgt_platform: multiple
title: Classe Win32_IRQResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IRQResource
- Win32_IRQResource.Availability
- Win32_IRQResource.Caption
- Win32_IRQResource.CreationClassName
- Win32_IRQResource.CSCreationClassName
- Win32_IRQResource.CSName
- Win32_IRQResource.Description
- Win32_IRQResource.Hardware
- Win32_IRQResource.InstallDate
- Win32_IRQResource.IRQNumber
- Win32_IRQResource.Name
- Win32_IRQResource.Shareable
- Win32_IRQResource.Status
- Win32_IRQResource.TriggerLevel
- Win32_IRQResource.TriggerType
- Win32_IRQResource.Vector
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd02487fe166cd7ce55482eaca1339c8701f2b62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126255"
---
# <a name="win32_irqresource-class"></a><span data-ttu-id="38b15-103">Win32 \_ IRQResource (classe)</span><span class="sxs-lookup"><span data-stu-id="38b15-103">Win32\_IRQResource class</span></span>

<span data-ttu-id="38b15-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ IRQResource Win32** rappresenta un numero di riga di richiesta di interrupt (IRQ) in un sistema di computer che esegue Windows.  </span><span class="sxs-lookup"><span data-stu-id="38b15-104">The **Win32\_IRQResource**  [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an interrupt request line (IRQ) number on a computer system running Windows.</span></span> <span data-ttu-id="38b15-105">Una richiesta di interrupt è un segnale inviato alla CPU da un dispositivo o un programma per gli eventi critici temporali.</span><span class="sxs-lookup"><span data-stu-id="38b15-105">An interrupt request is a signal sent to the CPU by a device or program for time critical events.</span></span> <span data-ttu-id="38b15-106">IRQ può essere basato su hardware o software.</span><span class="sxs-lookup"><span data-stu-id="38b15-106">IRQ can be hardware-based or software-based.</span></span>

<span data-ttu-id="38b15-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="38b15-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="38b15-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="38b15-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="38b15-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38b15-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_IRQResource : CIM_IRQ
{
  uint16   Availability;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  boolean  Hardware;
  datetime InstallDate;
  uint32   IRQNumber;
  string   Name;
  boolean  Shareable;
  string   Status;
  uint16   TriggerLevel;
  uint16   TriggerType;
  uint32   Vector;
};
```

## <a name="members"></a><span data-ttu-id="38b15-110">Members</span><span class="sxs-lookup"><span data-stu-id="38b15-110">Members</span></span>

<span data-ttu-id="38b15-111">La classe **Win32 \_ IRQResource** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="38b15-111">The **Win32\_IRQResource** class has these types of members:</span></span>

-   [<span data-ttu-id="38b15-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="38b15-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38b15-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="38b15-113">Properties</span></span>

<span data-ttu-id="38b15-114">La classe **Win32 \_ IRQResource** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="38b15-114">The **Win32\_IRQResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38b15-115">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="38b15-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38b15-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-118">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="38b15-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="38b15-119">Disponibilità dell'IRQ.</span><span class="sxs-lookup"><span data-stu-id="38b15-119">Availability of the IRQ.</span></span>

<span data-ttu-id="38b15-120">Questa proprietà viene ereditata [**da \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-120">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="38b15-121"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="38b15-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="38b15-122">Altro</span><span class="sxs-lookup"><span data-stu-id="38b15-122">Other</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="38b15-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="38b15-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="38b15-124">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="38b15-124">Unknown</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="38b15-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="38b15-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="38b15-126">Disponibile</span><span class="sxs-lookup"><span data-stu-id="38b15-126">Available</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="38b15-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponibile** (3)</span><span class="sxs-lookup"><span data-stu-id="38b15-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="38b15-128">In uso o non disponibile</span><span class="sxs-lookup"><span data-stu-id="38b15-128">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="38b15-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In uso/non disponibile** (4)</span><span class="sxs-lookup"><span data-stu-id="38b15-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="38b15-130">In uso e disponibile o condivisibile</span><span class="sxs-lookup"><span data-stu-id="38b15-130">In Use and Available or Sharable</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="38b15-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In uso e disponibile/condivisibile** (5)</span><span class="sxs-lookup"><span data-stu-id="38b15-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="38b15-132">In uso e disponibile/condivisibile</span><span class="sxs-lookup"><span data-stu-id="38b15-132">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="38b15-133">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="38b15-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38b15-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-136">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="38b15-136">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="38b15-137">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="38b15-137">Short description of the object a one-line string.</span></span>

<span data-ttu-id="38b15-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="38b15-139">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="38b15-139">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38b15-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-142">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="38b15-142">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="38b15-143">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="38b15-143">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="38b15-144">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="38b15-144">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="38b15-145">Questa proprietà viene ereditata [**da \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-145">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="38b15-146">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="38b15-146">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38b15-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-149">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="38b15-149">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="38b15-150">Nome della classe di creazione dell'ambito del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="38b15-150">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="38b15-151">Questa proprietà viene ereditata [**da \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-151">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="38b15-152">**CSName**</span><span class="sxs-lookup"><span data-stu-id="38b15-152">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38b15-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-155">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="38b15-155">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="38b15-156">Nome del sistema di ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="38b15-156">Name of the scoping computer system.</span></span>

<span data-ttu-id="38b15-157">Questa proprietà viene ereditata [**da \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-157">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="38b15-158">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="38b15-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38b15-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-161">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="38b15-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="38b15-162">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="38b15-162">Textual description of the object.</span></span>

<span data-ttu-id="38b15-163">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="38b15-164">**Hardware**</span><span class="sxs-lookup"><span data-stu-id="38b15-164">**Hardware**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-165">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="38b15-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-167">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Structures \| Resource \_ Descriptor \| InterfaceType")</span><span class="sxs-lookup"><span data-stu-id="38b15-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|RESOURCE\_DESCRIPTOR\|InterfaceType")</span></span>
</dt> </dl>

<span data-ttu-id="38b15-168">Se **true**, l'interrupt è basato su hardware o software.</span><span class="sxs-lookup"><span data-stu-id="38b15-168">If **TRUE**, the interrupt is hardware or software based.</span></span> <span data-ttu-id="38b15-169">Un IRQ hardware è un cablaggio fisico dal dispositivo periferico al chip del controller di interrupt programmabile (PIC) attraverso il quale la CPU può ricevere notifiche di eventi critici per il tempo.</span><span class="sxs-lookup"><span data-stu-id="38b15-169">A hardware IRQ is a physical wire from the peripheral to the programmable interrupt controller (PIC) chip through which the CPU can be notified of time-critical events.</span></span> <span data-ttu-id="38b15-170">Alcune linee IRQ sono riservate per i dispositivi standard, ad esempio la tastiera, le unità disco floppy e l'orologio di sistema.</span><span class="sxs-lookup"><span data-stu-id="38b15-170">Some IRQ lines are reserved for standard devices, such as the keyboard, floppy disk drives, and the system clock.</span></span> <span data-ttu-id="38b15-171">Un interrupt software consente alle applicazioni di ottenere l'attenzione del processore.</span><span class="sxs-lookup"><span data-stu-id="38b15-171">A software interrupt allows applications to get the attention of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="38b15-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="38b15-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-173">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="38b15-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-175">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="38b15-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="38b15-176">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="38b15-176">Date and time the object was installed.</span></span> <span data-ttu-id="38b15-177">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="38b15-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="38b15-178">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="38b15-179">**IRQNumber**</span><span class="sxs-lookup"><span data-stu-id="38b15-179">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-180">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38b15-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-182">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,1 "), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="38b15-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="38b15-183">Parte del valore della chiave dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="38b15-183">Part of the object's key value.</span></span>

<span data-ttu-id="38b15-184">Questa proprietà viene ereditata [**da \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-184">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="38b15-185">**Nome**</span><span class="sxs-lookup"><span data-stu-id="38b15-185">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38b15-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-188">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="38b15-188">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="38b15-189">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="38b15-189">Label by which the object is known.</span></span> <span data-ttu-id="38b15-190">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="38b15-190">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="38b15-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="38b15-192">**Condivisibile**</span><span class="sxs-lookup"><span data-stu-id="38b15-192">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-193">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="38b15-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-195">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="38b15-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="38b15-196">Se **true**, l'IRQ può essere condiviso.</span><span class="sxs-lookup"><span data-stu-id="38b15-196">If **TRUE**, the IRQ can be shared.</span></span>

<span data-ttu-id="38b15-197">Questa proprietà viene ereditata [**da \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-197">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="38b15-198">**Status**</span><span class="sxs-lookup"><span data-stu-id="38b15-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38b15-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-201">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="38b15-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="38b15-202">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="38b15-202">Current status of the object.</span></span> <span data-ttu-id="38b15-203">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="38b15-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="38b15-204">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="38b15-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="38b15-205">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="38b15-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="38b15-206">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="38b15-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="38b15-207">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="38b15-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="38b15-208">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="38b15-209">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="38b15-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="38b15-210">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="38b15-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="38b15-211">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="38b15-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="38b15-212">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="38b15-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="38b15-213">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="38b15-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="38b15-214">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="38b15-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="38b15-215">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="38b15-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="38b15-216">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="38b15-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="38b15-217">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="38b15-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="38b15-218">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="38b15-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="38b15-219">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="38b15-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="38b15-220">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="38b15-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="38b15-221">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="38b15-221">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38b15-222">**TriggerLevel**</span><span class="sxs-lookup"><span data-stu-id="38b15-222">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-223">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38b15-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-225">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni sull'IRQ delle risorse di sistema \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="38b15-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="38b15-226">Livello di trigger IRQ che indica se l'interrupt viene attivato dal segnale hardware in alto (4) o basso (3).</span><span class="sxs-lookup"><span data-stu-id="38b15-226">IRQ trigger level indicating whether the interrupt is triggered by the hardware signal going high (4) or low (3).</span></span>

<span data-ttu-id="38b15-227">Questa proprietà viene ereditata [**da \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-227">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="38b15-228">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="38b15-228">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="38b15-229">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="38b15-229">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="38b15-230">**Attivo basso** (3)</span><span class="sxs-lookup"><span data-stu-id="38b15-230">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="38b15-231">**Attivo alto** (4)</span><span class="sxs-lookup"><span data-stu-id="38b15-231">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38b15-232">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="38b15-232">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-233">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38b15-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-235">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,3 "," MIF. DMTF \| informazioni sull'IRQ delle risorse di sistema \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="38b15-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="38b15-236">Tipo di trigger IRQ che indica se si verificano gli interrupt con trigger Edge (4) o a livello (3).</span><span class="sxs-lookup"><span data-stu-id="38b15-236">IRQ trigger type indicating whether edge-triggered (4) or level-triggered (3) interrupts occur.</span></span>

<span data-ttu-id="38b15-237">Questa proprietà viene ereditata [**da \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-237">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="38b15-238">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="38b15-238">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="38b15-239">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="38b15-239">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="38b15-240">**Livello** (3)</span><span class="sxs-lookup"><span data-stu-id="38b15-240">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="38b15-241">**Edge** (4)</span><span class="sxs-lookup"><span data-stu-id="38b15-241">**Edge** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38b15-242">**Vettore**</span><span class="sxs-lookup"><span data-stu-id="38b15-242">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b15-243">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38b15-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38b15-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b15-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b15-245">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| strutture di sistema Win32API \| cm livello di interrupt del [**\_ \_ \_ descrittore di risorse parziali**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor) \| \| ")</span><span class="sxs-lookup"><span data-stu-id="38b15-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Interrupt\|Level")</span></span>
</dt> </dl>

<span data-ttu-id="38b15-246">Vettore della risorsa IRQ di Windows.</span><span class="sxs-lookup"><span data-stu-id="38b15-246">Vector of the Windows IRQ resource.</span></span> <span data-ttu-id="38b15-247">Un vettore contiene l'indirizzo di memoria per la funzione che verrà eseguita dopo che la richiesta di interrupt viene riconosciuta dalla CPU.</span><span class="sxs-lookup"><span data-stu-id="38b15-247">A vector contains the memory address to the function that will execute once the interrupt request is acknowledged by the CPU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38b15-248">Commenti</span><span class="sxs-lookup"><span data-stu-id="38b15-248">Remarks</span></span>

<span data-ttu-id="38b15-249">La classe **Win32 \_ IRQResource** è derivata da [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="38b15-249">The **Win32\_IRQResource** class is derived from [**CIM\_IRQ**](cim-irq.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38b15-250">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38b15-250">Requirements</span></span>



| <span data-ttu-id="38b15-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="38b15-251">Requirement</span></span> | <span data-ttu-id="38b15-252">Valore</span><span class="sxs-lookup"><span data-stu-id="38b15-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38b15-253">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38b15-253">Minimum supported client</span></span><br/> | <span data-ttu-id="38b15-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38b15-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38b15-255">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38b15-255">Minimum supported server</span></span><br/> | <span data-ttu-id="38b15-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38b15-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38b15-257">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="38b15-257">Namespace</span></span><br/>                | <span data-ttu-id="38b15-258">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="38b15-258">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38b15-259">MOF</span><span class="sxs-lookup"><span data-stu-id="38b15-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38b15-260"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38b15-260"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38b15-261">DLL</span><span class="sxs-lookup"><span data-stu-id="38b15-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38b15-262"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38b15-262"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38b15-263">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38b15-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b15-264">**\_IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="38b15-264">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dt>

[<span data-ttu-id="38b15-265">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="38b15-265">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

