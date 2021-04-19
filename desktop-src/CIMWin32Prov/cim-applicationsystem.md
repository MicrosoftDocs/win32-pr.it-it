---
description: La \_ classe CIM ApplicationSystem rappresenta un'applicazione o un sistema software che supporta una particolare funzione di business che può essere gestita come unità indipendente.
ms.assetid: 42471863-ff6c-4464-8b0a-7dad2fd11934
ms.tgt_platform: multiple
title: Classe CIM_ApplicationSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystem
- CIM_ApplicationSystem.Caption
- CIM_ApplicationSystem.Description
- CIM_ApplicationSystem.InstallDate
- CIM_ApplicationSystem.Status
- CIM_ApplicationSystem.CreationClassName
- CIM_ApplicationSystem.Name
- CIM_ApplicationSystem.NameFormat
- CIM_ApplicationSystem.PrimaryOwnerContact
- CIM_ApplicationSystem.PrimaryOwnerName
- CIM_ApplicationSystem.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a69c05b11c5f3c623824783ed13f42c0a3eab801
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305042"
---
# <a name="cim_applicationsystem-class"></a><span data-ttu-id="724ad-103">CIM \_ ApplicationSystem (classe)</span><span class="sxs-lookup"><span data-stu-id="724ad-103">CIM\_ApplicationSystem class</span></span>

<span data-ttu-id="724ad-104">La classe **CIM \_ ApplicationSystem** rappresenta un'applicazione o un sistema software che supporta una particolare funzione di business che può essere gestita come unità indipendente.</span><span class="sxs-lookup"><span data-stu-id="724ad-104">The **CIM\_ApplicationSystem** class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="724ad-105">Un sistema di questo tipo può essere scomposto nei componenti funzionali usando la classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="724ad-105">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="724ad-106">Le funzionalità software per una particolare applicazione o sistema software si trovano usando l'associazione [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="724ad-106">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="724ad-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="724ad-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="724ad-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="724ad-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="724ad-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="724ad-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="724ad-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="724ad-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="724ad-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="724ad-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{120BB700-DB2B-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ApplicationSystem : CIM_System
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

## <a name="members"></a><span data-ttu-id="724ad-112">Members</span><span class="sxs-lookup"><span data-stu-id="724ad-112">Members</span></span>

<span data-ttu-id="724ad-113">La classe **CIM \_ ApplicationSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="724ad-113">The **CIM\_ApplicationSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="724ad-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="724ad-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="724ad-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="724ad-115">Properties</span></span>

<span data-ttu-id="724ad-116">La classe **CIM \_ ApplicationSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="724ad-116">The **CIM\_ApplicationSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="724ad-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="724ad-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="724ad-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="724ad-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="724ad-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="724ad-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="724ad-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="724ad-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="724ad-121">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="724ad-121">A short textual description of the object.</span></span>

<span data-ttu-id="724ad-122">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="724ad-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="724ad-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="724ad-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="724ad-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="724ad-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="724ad-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="724ad-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="724ad-126">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="724ad-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="724ad-127">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="724ad-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="724ad-128">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="724ad-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="724ad-129">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="724ad-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="724ad-130">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="724ad-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="724ad-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="724ad-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="724ad-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="724ad-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="724ad-133">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="724ad-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="724ad-134">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="724ad-134">A textual description of the object.</span></span>

<span data-ttu-id="724ad-135">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="724ad-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="724ad-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="724ad-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="724ad-137">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="724ad-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="724ad-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="724ad-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="724ad-139">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="724ad-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="724ad-140">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="724ad-140">Indicates when the object was installed.</span></span> <span data-ttu-id="724ad-141">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="724ad-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="724ad-142">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="724ad-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="724ad-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="724ad-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="724ad-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="724ad-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="724ad-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="724ad-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="724ad-146">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="724ad-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="724ad-147">Definisce l'etichetta in base alla quale l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="724ad-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="724ad-148">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="724ad-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="724ad-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="724ad-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="724ad-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="724ad-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="724ad-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="724ad-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="724ad-152">Identifica il modo in cui è stato generato il nome di sistema, usando l'euristica della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="724ad-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

<span data-ttu-id="724ad-153">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="724ad-153">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="724ad-154">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="724ad-154">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="724ad-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="724ad-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="724ad-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="724ad-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="724ad-157">Come è possibile raggiungere il proprietario del sistema primario (ad esempio, il numero di telefono o l'indirizzo di posta elettronica).</span><span class="sxs-lookup"><span data-stu-id="724ad-157">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="724ad-158">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="724ad-158">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="724ad-159">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="724ad-159">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="724ad-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="724ad-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="724ad-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="724ad-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="724ad-162">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="724ad-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="724ad-163">Nome del proprietario del sistema primario.</span><span class="sxs-lookup"><span data-stu-id="724ad-163">Name of the primary system owner.</span></span>

<span data-ttu-id="724ad-164">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="724ad-164">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="724ad-165">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="724ad-165">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="724ad-166">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="724ad-166">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="724ad-167">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="724ad-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="724ad-168">Ruoli riprodotti dal sistema nell'ambiente Information Technology.</span><span class="sxs-lookup"><span data-stu-id="724ad-168">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="724ad-169">Le sottoclassi del sistema possono eseguire l'override di questa proprietà per definire valori di ruolo espliciti.</span><span class="sxs-lookup"><span data-stu-id="724ad-169">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="724ad-170">In alternativa, un gruppo di lavoro può descrivere l'euristica, le convenzioni e le linee guida per specificare i ruoli.</span><span class="sxs-lookup"><span data-stu-id="724ad-170">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="724ad-171">Per un'istanza di un sistema di rete, ad esempio, questa proprietà potrebbe contenere la stringa "switch" o "Bridge".</span><span class="sxs-lookup"><span data-stu-id="724ad-171">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="724ad-172">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="724ad-172">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="724ad-173">**Status**</span><span class="sxs-lookup"><span data-stu-id="724ad-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="724ad-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="724ad-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="724ad-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="724ad-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="724ad-176">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="724ad-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="724ad-177">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="724ad-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="724ad-178">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="724ad-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="724ad-179">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="724ad-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="724ad-180">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="724ad-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="724ad-181">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="724ad-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="724ad-182">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="724ad-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="724ad-183">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="724ad-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="724ad-184">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="724ad-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="724ad-185">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="724ad-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="724ad-186">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="724ad-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="724ad-187">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="724ad-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="724ad-188">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="724ad-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="724ad-189">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="724ad-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="724ad-190">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="724ad-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="724ad-191">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="724ad-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="724ad-192">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="724ad-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="724ad-193">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="724ad-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="724ad-194">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="724ad-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="724ad-195">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="724ad-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="724ad-196">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="724ad-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="724ad-197">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="724ad-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="724ad-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="724ad-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="724ad-199">Commenti</span><span class="sxs-lookup"><span data-stu-id="724ad-199">Remarks</span></span>

<span data-ttu-id="724ad-200">La classe **CIM \_ ApplicationSystem** è derivata dal [**\_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="724ad-200">The **CIM\_ApplicationSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="724ad-201">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="724ad-201">WMI does not implement this class.</span></span>

<span data-ttu-id="724ad-202">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="724ad-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="724ad-203">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="724ad-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="724ad-204">Requisiti</span><span class="sxs-lookup"><span data-stu-id="724ad-204">Requirements</span></span>



| <span data-ttu-id="724ad-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="724ad-205">Requirement</span></span> | <span data-ttu-id="724ad-206">Valore</span><span class="sxs-lookup"><span data-stu-id="724ad-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="724ad-207">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="724ad-207">Minimum supported client</span></span><br/> | <span data-ttu-id="724ad-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="724ad-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="724ad-209">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="724ad-209">Minimum supported server</span></span><br/> | <span data-ttu-id="724ad-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="724ad-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="724ad-211">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="724ad-211">Namespace</span></span><br/>                | <span data-ttu-id="724ad-212">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="724ad-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="724ad-213">MOF</span><span class="sxs-lookup"><span data-stu-id="724ad-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="724ad-214"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="724ad-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="724ad-215">DLL</span><span class="sxs-lookup"><span data-stu-id="724ad-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="724ad-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="724ad-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="724ad-217">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="724ad-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="724ad-218">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="724ad-218">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

