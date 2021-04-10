---
description: La \_ classe di sistema CIM aggrega un set enumerabile di elementi di sistema gestiti.
ms.assetid: cbfa60d4-36ae-4e0c-a57f-aabf219851d0
ms.tgt_platform: multiple
title: Classe CIM_System (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.Caption
- CIM_System.Description
- CIM_System.InstallDate
- CIM_System.Status
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerContact
- CIM_System.PrimaryOwnerName
- CIM_System.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef04e472e11c848aadb63c98b3dee2ea645a3ce7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966195"
---
# <a name="cim_system-class-cimwin32-wmi-providers"></a><span data-ttu-id="06b80-103">Classe CIM_System (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="06b80-103">CIM_System class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="06b80-104">La classe di **\_ sistema CIM** aggrega un set enumerabile di elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="06b80-104">The **CIM\_System** class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="06b80-105">L'aggregazione funziona come un intero funzionale.</span><span class="sxs-lookup"><span data-stu-id="06b80-105">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="06b80-106">All'interno di una sottoclasse particolare del sistema è presente un elenco ben definito di classi di elementi di sistema gestite le cui istanze devono essere aggregate.</span><span class="sxs-lookup"><span data-stu-id="06b80-106">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

<span data-ttu-id="06b80-107">L'oggetto di **\_ sistema CIM** e i relativi derivati sono oggetti di livello superiore di CIM.</span><span class="sxs-lookup"><span data-stu-id="06b80-107">The **CIM\_System** object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="06b80-108">Forniscono l'ambito per numerosi componenti e devono avere chiavi di sistema univoche.</span><span class="sxs-lookup"><span data-stu-id="06b80-108">They provide the scope for numerous components and are required to have unique system keys.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06b80-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="06b80-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="06b80-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="06b80-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="06b80-111">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="06b80-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="06b80-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="06b80-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b80-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06b80-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C524-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_System : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
};
```

## <a name="members"></a><span data-ttu-id="06b80-114">Members</span><span class="sxs-lookup"><span data-stu-id="06b80-114">Members</span></span>

<span data-ttu-id="06b80-115">La classe di **\_ sistema CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="06b80-115">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="06b80-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06b80-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06b80-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06b80-117">Properties</span></span>

<span data-ttu-id="06b80-118">La classe di **\_ sistema CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="06b80-118">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06b80-119">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="06b80-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b80-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06b80-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06b80-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b80-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06b80-122">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="06b80-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="06b80-123">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06b80-123">A short textual description of the object.</span></span>

<span data-ttu-id="06b80-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06b80-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06b80-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06b80-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b80-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06b80-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06b80-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b80-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06b80-128">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="06b80-128">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="06b80-129">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="06b80-129">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="06b80-130">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="06b80-130">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="06b80-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="06b80-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b80-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06b80-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06b80-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b80-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06b80-134">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="06b80-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="06b80-135">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06b80-135">A textual description of the object.</span></span>

<span data-ttu-id="06b80-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06b80-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06b80-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="06b80-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b80-138">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="06b80-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06b80-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b80-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06b80-140">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="06b80-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="06b80-141">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="06b80-141">Indicates when the object was installed.</span></span> <span data-ttu-id="06b80-142">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="06b80-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="06b80-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06b80-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06b80-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="06b80-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b80-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06b80-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06b80-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b80-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06b80-147">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="06b80-147">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="06b80-148">Definisce l'etichetta in base alla quale l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="06b80-148">Defines the label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="06b80-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="06b80-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b80-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06b80-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06b80-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b80-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06b80-152">Identifica il modo in cui è stato generato il nome di sistema, usando l'euristica della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="06b80-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="06b80-153">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="06b80-153">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b80-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06b80-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06b80-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b80-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06b80-156">Come è possibile raggiungere il proprietario del sistema primario (ad esempio, il numero di telefono o l'indirizzo di posta elettronica).</span><span class="sxs-lookup"><span data-stu-id="06b80-156">How the primary system owner can be reached (for example, phone number or email address).</span></span>

</dd> <dt>

<span data-ttu-id="06b80-157">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="06b80-157">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b80-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06b80-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06b80-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b80-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06b80-160">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="06b80-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="06b80-161">Nome del proprietario del sistema primario.</span><span class="sxs-lookup"><span data-stu-id="06b80-161">Name of the primary system owner.</span></span>

</dd> <dt>

<span data-ttu-id="06b80-162">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="06b80-162">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b80-163">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="06b80-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06b80-164">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="06b80-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="06b80-165">Ruoli riprodotti dal sistema nell'ambiente Information Technology.</span><span class="sxs-lookup"><span data-stu-id="06b80-165">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="06b80-166">Le sottoclassi del sistema possono eseguire l'override di questa proprietà per definire valori di ruolo espliciti.</span><span class="sxs-lookup"><span data-stu-id="06b80-166">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="06b80-167">In alternativa, un gruppo di lavoro può descrivere l'euristica, le convenzioni e le linee guida per specificare i ruoli.</span><span class="sxs-lookup"><span data-stu-id="06b80-167">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="06b80-168">Per un'istanza di un sistema di rete, ad esempio, questa proprietà potrebbe contenere la stringa "switch" o "Bridge".</span><span class="sxs-lookup"><span data-stu-id="06b80-168">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

</dd> <dt>

<span data-ttu-id="06b80-169">**Status**</span><span class="sxs-lookup"><span data-stu-id="06b80-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b80-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06b80-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06b80-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b80-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06b80-172">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="06b80-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="06b80-173">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06b80-173">String that indicates the current status of the object.</span></span> <span data-ttu-id="06b80-174">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="06b80-174">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="06b80-175">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="06b80-175">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="06b80-176">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="06b80-176">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="06b80-177">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="06b80-177">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="06b80-178">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="06b80-178">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="06b80-179">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="06b80-179">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="06b80-180">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06b80-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="06b80-181">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="06b80-181">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="06b80-182">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="06b80-182">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="06b80-183">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="06b80-183">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="06b80-184">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="06b80-184">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06b80-185">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="06b80-185">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="06b80-186">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="06b80-186">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="06b80-187">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="06b80-187">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="06b80-188">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="06b80-188">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="06b80-189">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="06b80-189">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="06b80-190">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="06b80-190">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="06b80-191">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="06b80-191">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="06b80-192">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="06b80-192">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="06b80-193">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="06b80-193">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="06b80-194"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="06b80-194"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="06b80-195">Commenti</span><span class="sxs-lookup"><span data-stu-id="06b80-195">Remarks</span></span>

<span data-ttu-id="06b80-196">La classe di **\_ sistema CIM** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="06b80-196">The **CIM\_System** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="06b80-197">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="06b80-197">WMI does not implement this class.</span></span> <span data-ttu-id="06b80-198">Per le classi WMI derivate dal **\_ sistema CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="06b80-198">For WMI classes derived from **CIM\_System**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="06b80-199">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="06b80-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="06b80-200">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="06b80-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b80-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06b80-201">Requirements</span></span>



| <span data-ttu-id="06b80-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="06b80-202">Requirement</span></span> | <span data-ttu-id="06b80-203">Valore</span><span class="sxs-lookup"><span data-stu-id="06b80-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06b80-204">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06b80-204">Minimum supported client</span></span><br/> | <span data-ttu-id="06b80-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06b80-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06b80-206">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06b80-206">Minimum supported server</span></span><br/> | <span data-ttu-id="06b80-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06b80-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06b80-208">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06b80-208">Namespace</span></span><br/>                | <span data-ttu-id="06b80-209">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="06b80-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06b80-210">MOF</span><span class="sxs-lookup"><span data-stu-id="06b80-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06b80-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06b80-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06b80-212">DLL</span><span class="sxs-lookup"><span data-stu-id="06b80-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06b80-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06b80-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06b80-214">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06b80-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b80-215">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="06b80-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

