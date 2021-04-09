---
description: La \_ classe CIM UnitaryComputerSystem rappresenta un computer desktop, mobile, di rete, un server o un altro tipo di computer a nodo singolo.
ms.assetid: c696050d-c921-4056-adc7-e4a2e9f4e119
ms.tgt_platform: multiple
title: Classe CIM_UnitaryComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem
- CIM_UnitaryComputerSystem.Caption
- CIM_UnitaryComputerSystem.CreationClassName
- CIM_UnitaryComputerSystem.Description
- CIM_UnitaryComputerSystem.InitialLoadInfo
- CIM_UnitaryComputerSystem.InstallDate
- CIM_UnitaryComputerSystem.LastLoadInfo
- CIM_UnitaryComputerSystem.Name
- CIM_UnitaryComputerSystem.NameFormat
- CIM_UnitaryComputerSystem.PowerManagementCapabilities
- CIM_UnitaryComputerSystem.PowerManagementSupported
- CIM_UnitaryComputerSystem.PowerState
- CIM_UnitaryComputerSystem.PrimaryOwnerContact
- CIM_UnitaryComputerSystem.PrimaryOwnerName
- CIM_UnitaryComputerSystem.ResetCapability
- CIM_UnitaryComputerSystem.Roles
- CIM_UnitaryComputerSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e14812fda7971ffe045e8e36752c983cf5350402
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965994"
---
# <a name="cim_unitarycomputersystem-class"></a><span data-ttu-id="4e14f-103">CIM \_ UnitaryComputerSystem (classe)</span><span class="sxs-lookup"><span data-stu-id="4e14f-103">CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="4e14f-104">La classe **CIM \_ UnitaryComputerSystem** rappresenta un computer desktop, mobile, di rete, un server o un altro tipo di computer a nodo singolo.</span><span class="sxs-lookup"><span data-stu-id="4e14f-104">The **CIM\_UnitaryComputerSystem** class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e14f-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4e14f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4e14f-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4e14f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4e14f-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4e14f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4e14f-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="4e14f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e14f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e14f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C526-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UnitaryComputerSystem : CIM_ComputerSystem
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  string   InitialLoadInfo[];
  datetime InstallDate;
  string   LastLoadInfo;
  string   Name;
  string   NameFormat;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  string   Roles[];
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="4e14f-110">Members</span><span class="sxs-lookup"><span data-stu-id="4e14f-110">Members</span></span>

<span data-ttu-id="4e14f-111">La classe **CIM \_ UnitaryComputerSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4e14f-111">The **CIM\_UnitaryComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="4e14f-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="4e14f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4e14f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e14f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4e14f-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="4e14f-114">Methods</span></span>

<span data-ttu-id="4e14f-115">La classe **CIM \_ UnitaryComputerSystem** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4e14f-115">The **CIM\_UnitaryComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="4e14f-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="4e14f-116">Method</span></span>                                                                           | <span data-ttu-id="4e14f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e14f-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e14f-118">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4e14f-118">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md) | <span data-ttu-id="4e14f-119">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="4e14f-119">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="4e14f-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="4e14f-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4e14f-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e14f-121">Properties</span></span>

<span data-ttu-id="4e14f-122">La classe **CIM \_ UnitaryComputerSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4e14f-122">The **CIM\_UnitaryComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e14f-123">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="4e14f-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e14f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-126">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4e14f-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-127">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4e14f-127">Short textual description of the object.</span></span>

<span data-ttu-id="4e14f-128">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e14f-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4e14f-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e14f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-132">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4e14f-132">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-133">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="4e14f-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4e14f-134">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="4e14f-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4e14f-135">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-135">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e14f-136">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="4e14f-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e14f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-139">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4e14f-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-140">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4e14f-140">Textual description of the object.</span></span>

<span data-ttu-id="4e14f-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e14f-142">**InitialLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="4e14f-142">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-143">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4e14f-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-145">Dati necessari per trovare il dispositivo di caricamento iniziale (la relativa chiave) o il servizio di avvio per richiedere l'avvio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e14f-145">Data needed to find either the initial load device (its key) or the boot service to request the operating system to start.</span></span> <span data-ttu-id="4e14f-146">Inoltre, è possibile specificare i parametri Load, ovvero un nome di percorso e i parametri.</span><span class="sxs-lookup"><span data-stu-id="4e14f-146">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="4e14f-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4e14f-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-148">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4e14f-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-150">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="4e14f-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-151">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4e14f-151">Date and time the object was installed.</span></span> <span data-ttu-id="4e14f-152">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="4e14f-152">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4e14f-153">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e14f-154">**LastLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="4e14f-154">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e14f-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-157">Dati che identificano il dispositivo di caricamento iniziale (chiave) o il servizio di avvio che ha richiesto l'ultimo caricamento del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e14f-157">Data that identifies either the initial load device (its key) or the boot service that requested the last operating system load.</span></span> <span data-ttu-id="4e14f-158">Inoltre, è possibile specificare i parametri Load, ovvero un nome di percorso e i parametri.</span><span class="sxs-lookup"><span data-stu-id="4e14f-158">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="4e14f-159">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4e14f-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e14f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-162">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4e14f-162">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-163">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="4e14f-163">Label by which the object is known.</span></span> <span data-ttu-id="4e14f-164">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="4e14f-164">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4e14f-165">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e14f-166">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="4e14f-166">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e14f-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-169">L'oggetto [**CIM \_ ComputerSystem**](cim-computersystem.md) e i relativi derivati sono oggetti di livello superiore di CIM che forniscono l'ambito per numerosi componenti e richiedono chiavi di [**\_ sistema CIM**](cim-system.md) univoche.</span><span class="sxs-lookup"><span data-stu-id="4e14f-169">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of CIM that provide the scope for numerous components and require unique [**CIM\_System**](cim-system.md) keys.</span></span> <span data-ttu-id="4e14f-170">Viene definita una euristica per creare il nome del **\_ ComputerSystem CIM** nel tentativo di generare sempre lo stesso nome di sistema, indipendentemente dal protocollo di individuazione.</span><span class="sxs-lookup"><span data-stu-id="4e14f-170">A heuristic is defined to create the **CIM\_ComputerSystem** name in an attempt to always generate the same system name, independent of discovery protocol.</span></span> <span data-ttu-id="4e14f-171">In questo modo si evitano problemi di inventario e gestione quando lo stesso asset o entità viene individuato più volte, ma non può essere risolto in un singolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="4e14f-171">This prevents inventory and management problems where the same asset or entity is discovered multiple times, but cannot be resolved to a single object.</span></span> <span data-ttu-id="4e14f-172">Questa proprietà identifica il modo in cui è stato generato il nome di sistema utilizzando l'euristica della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="4e14f-172">This property identifies how the system name was generated by using the subclass heuristic.</span></span> <span data-ttu-id="4e14f-173">L'euristica è illustrata nella specifica del modello comune CIM V2 e presuppone che le regole documentate vengano attraversate per determinare e assegnare un nome.</span><span class="sxs-lookup"><span data-stu-id="4e14f-173">The heuristic is outlined in the CIM V2 Common Model specification and assumes that the documented rules are traversed to determine and assign a name.</span></span> <span data-ttu-id="4e14f-174">L'elenco di valori **NameFormat** definisce l'ordine di precedenza per l'assegnazione del nome di sistema con diverse regole di mapping allo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="4e14f-174">The **NameFormat** values list defines the precedence order for assigning the system name with several rules mapping to the same value.</span></span> <span data-ttu-id="4e14f-175">Si noti che il nome **CIM \_ ComputerSystem** calcolato mediante l'euristica è il valore della chiave del sistema.</span><span class="sxs-lookup"><span data-stu-id="4e14f-175">Note that the **CIM\_ComputerSystem** name that is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="4e14f-176">Gli altri nomi possono essere assegnati e usati per **la \_ ComputerSystem CIM** che meglio soddisfano le esigenze aziendali, usando gli alias.</span><span class="sxs-lookup"><span data-stu-id="4e14f-176">Other names can be assigned and used for the **CIM\_ComputerSystem** that better suit the business, using aliases.</span></span>

<span data-ttu-id="4e14f-177">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-177">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="4e14f-178">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e14f-178">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="4e14f-179">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="4e14f-179">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="4e14f-180">**Dial** ("dial")</span><span class="sxs-lookup"><span data-stu-id="4e14f-180">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="4e14f-181">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="4e14f-181">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="4e14f-182">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="4e14f-182">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="4e14f-183">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="4e14f-183">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="4e14f-184">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="4e14f-184">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="4e14f-185">**ISDN** ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="4e14f-185">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="4e14f-186">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="4e14f-186">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="4e14f-187">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="4e14f-187">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="4e14f-188">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="4e14f-188">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="4e14f-189">**E. 164** ("e. 164")</span><span class="sxs-lookup"><span data-stu-id="4e14f-189">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="4e14f-190">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="4e14f-190">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="4e14f-191">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="4e14f-191">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4e14f-192">**Altro** ("altro")</span><span class="sxs-lookup"><span data-stu-id="4e14f-192">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e14f-193">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4e14f-193">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-194">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e14f-194">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-196">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controlli di alimentazione del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="4e14f-196">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-197">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="4e14f-197">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="4e14f-198">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="4e14f-198">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e14f-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="4e14f-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4e14f-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="4e14f-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4e14f-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="4e14f-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4e14f-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="4e14f-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-203">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="4e14f-203">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4e14f-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="4e14f-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-205">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="4e14f-205">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4e14f-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="4e14f-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-207">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="4e14f-207">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="4e14f-208">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="4e14f-208">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="4e14f-209">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="4e14f-209">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4e14f-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="4e14f-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-211">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="4e14f-211">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4e14f-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="4e14f-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-213">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="4e14f-213">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e14f-214">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4e14f-214">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-215">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4e14f-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-217">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="4e14f-217">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="4e14f-218">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="4e14f-218">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="4e14f-219">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="4e14f-219">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="4e14f-220">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="4e14f-220">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="4e14f-221">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="4e14f-221">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-222">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e14f-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-224">Stato di alimentazione corrente del computer e del sistema operativo associato.</span><span class="sxs-lookup"><span data-stu-id="4e14f-224">Current power state of the computer system and its associated operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e14f-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="4e14f-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-226">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4e14f-226">Unknown.</span></span>

</dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="4e14f-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Potenza completa** (1)</span><span class="sxs-lookup"><span data-stu-id="4e14f-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-228">Potenza piena.</span><span class="sxs-lookup"><span data-stu-id="4e14f-228">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4e14f-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (2)</span><span class="sxs-lookup"><span data-stu-id="4e14f-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-230">Il sistema è in uno stato di risparmio energia e funziona ancora, ma può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="4e14f-230">System is in a power-save state and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4e14f-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (3)</span><span class="sxs-lookup"><span data-stu-id="4e14f-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-232">Il sistema non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="4e14f-232">System is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4e14f-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (4)</span><span class="sxs-lookup"><span data-stu-id="4e14f-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-234">Il sistema è noto come in modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4e14f-234">System is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4e14f-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (5)</span><span class="sxs-lookup"><span data-stu-id="4e14f-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-236">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="4e14f-236">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4e14f-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (6** )</span><span class="sxs-lookup"><span data-stu-id="4e14f-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-238">Spegnimento.</span><span class="sxs-lookup"><span data-stu-id="4e14f-238">Power off.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4e14f-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (7)</span><span class="sxs-lookup"><span data-stu-id="4e14f-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-240">Il sistema è in uno stato di avviso e anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="4e14f-240">System is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="4e14f-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Risparmio energia-ibernazione** (8)</span><span class="sxs-lookup"><span data-stu-id="4e14f-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-242">Ibernazione risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="4e14f-242">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="4e14f-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Risparmio energia-soft off** (9)</span><span class="sxs-lookup"><span data-stu-id="4e14f-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="4e14f-244">Risparmio energia Soft disattivato.</span><span class="sxs-lookup"><span data-stu-id="4e14f-244">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e14f-245">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="4e14f-245">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e14f-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-248">Stringa che fornisce informazioni su come raggiungere il proprietario del sistema primario, ad esempio il numero di telefono, l'indirizzo di posta elettronica e così via.</span><span class="sxs-lookup"><span data-stu-id="4e14f-248">String that provides information on how to reach the primary system owner (for example, phone number, email address, and so on).</span></span>

<span data-ttu-id="4e14f-249">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-249">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e14f-250">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="4e14f-250">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e14f-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-253">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4e14f-253">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-254">Nome del proprietario del sistema primario.</span><span class="sxs-lookup"><span data-stu-id="4e14f-254">Name of the primary system owner.</span></span>

<span data-ttu-id="4e14f-255">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-255">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e14f-256">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="4e14f-256">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-257">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e14f-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-259">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sicurezza hardware del sistema DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="4e14f-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-260">Se abilitata, il sistema informatico può essere reimpostato con hardware, ad esempio con i pulsanti di accensione e ripristino.</span><span class="sxs-lookup"><span data-stu-id="4e14f-260">If enabled, the unitary computer system can be reset with hardware (for example, with the power and reset buttons).</span></span> <span data-ttu-id="4e14f-261">Se disabilitata, la reimpostazione dell'hardware non è consentita.</span><span class="sxs-lookup"><span data-stu-id="4e14f-261">If disabled, hardware reset is not allowed.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4e14f-262">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="4e14f-262">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e14f-263">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="4e14f-263">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4e14f-264">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="4e14f-264">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4e14f-265">**Abilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="4e14f-265">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="4e14f-266">**Non implementato** (5)</span><span class="sxs-lookup"><span data-stu-id="4e14f-266">**Not Implemented** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e14f-267">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="4e14f-267">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-268">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4e14f-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-269">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e14f-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-270">Ruoli riprodotti dal sistema nell'ambiente Information Technology.</span><span class="sxs-lookup"><span data-stu-id="4e14f-270">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="4e14f-271">Le sottoclassi del sistema possono eseguire l'override di questa proprietà per definire valori di ruolo espliciti.</span><span class="sxs-lookup"><span data-stu-id="4e14f-271">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="4e14f-272">In alternativa, un gruppo di lavoro può descrivere l'euristica, le convenzioni e le linee guida per specificare i ruoli.</span><span class="sxs-lookup"><span data-stu-id="4e14f-272">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="4e14f-273">Per un'istanza di un sistema di rete, ad esempio, questa proprietà potrebbe contenere la stringa "switch" o "Bridge".</span><span class="sxs-lookup"><span data-stu-id="4e14f-273">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="4e14f-274">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-274">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e14f-275">**Status**</span><span class="sxs-lookup"><span data-stu-id="4e14f-275">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e14f-276">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e14f-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e14f-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e14f-278">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="4e14f-278">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4e14f-279">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4e14f-279">Current status of the object.</span></span> <span data-ttu-id="4e14f-280">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4e14f-281">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e14f-281">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4e14f-282">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="4e14f-282">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4e14f-283">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="4e14f-283">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4e14f-284">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="4e14f-284">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e14f-285">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="4e14f-285">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4e14f-286">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="4e14f-286">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4e14f-287">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="4e14f-287">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4e14f-288">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="4e14f-288">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4e14f-289">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="4e14f-289">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4e14f-290">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="4e14f-290">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4e14f-291">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="4e14f-291">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4e14f-292">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="4e14f-292">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4e14f-293">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="4e14f-293">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="4e14f-294"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4e14f-294"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="4e14f-295">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e14f-295">Remarks</span></span>

<span data-ttu-id="4e14f-296">La classe **CIM \_ UnitaryComputerSystem** è derivata da [**CIM \_ ComputerSystem**](cim-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-296">The **CIM\_UnitaryComputerSystem** class is derived from [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="4e14f-297">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="4e14f-297">WMI does not implement this class.</span></span> <span data-ttu-id="4e14f-298">Per le classi WMI derivate da **CIM \_ UnitaryComputerSystem**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4e14f-298">For WMI classes derived from **CIM\_UnitaryComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4e14f-299">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4e14f-299">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4e14f-300">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4e14f-300">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e14f-301">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e14f-301">Requirements</span></span>



| <span data-ttu-id="4e14f-302">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e14f-302">Requirement</span></span> | <span data-ttu-id="4e14f-303">Valore</span><span class="sxs-lookup"><span data-stu-id="4e14f-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e14f-304">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e14f-304">Minimum supported client</span></span><br/> | <span data-ttu-id="4e14f-305">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e14f-305">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e14f-306">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e14f-306">Minimum supported server</span></span><br/> | <span data-ttu-id="4e14f-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e14f-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e14f-308">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e14f-308">Namespace</span></span><br/>                | <span data-ttu-id="4e14f-309">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4e14f-309">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e14f-310">MOF</span><span class="sxs-lookup"><span data-stu-id="4e14f-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e14f-311"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e14f-311"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e14f-312">DLL</span><span class="sxs-lookup"><span data-stu-id="4e14f-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e14f-313"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e14f-313"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e14f-314">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e14f-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e14f-315">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="4e14f-315">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

