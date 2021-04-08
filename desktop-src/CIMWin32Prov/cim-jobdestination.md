---
description: La \_ classe CIM JobDestination rappresenta il punto in cui un processo viene inviato per l'elaborazione.
ms.assetid: ad2a037d-a5d3-4422-972d-8ef10699bb60
ms.tgt_platform: multiple
title: Classe CIM_JobDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestination
- CIM_JobDestination.Caption
- CIM_JobDestination.Description
- CIM_JobDestination.InstallDate
- CIM_JobDestination.Name
- CIM_JobDestination.Status
- CIM_JobDestination.CreationClassName
- CIM_JobDestination.SystemCreationClassName
- CIM_JobDestination.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d01fbe3b6025795084bf0af4cca3d644fd3cf4a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877885"
---
# <a name="cim_jobdestination-class"></a><span data-ttu-id="c2434-103">CIM \_ JobDestination (classe)</span><span class="sxs-lookup"><span data-stu-id="c2434-103">CIM\_JobDestination class</span></span>

<span data-ttu-id="c2434-104">La classe **CIM \_ JobDestination** rappresenta il punto in cui un processo viene inviato per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="c2434-104">The **CIM\_JobDestination** class represents where a job is submitted for processing.</span></span> <span data-ttu-id="c2434-105">Può fare riferimento a una coda che contiene zero o più processi, ad esempio una coda di stampa contenente processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="c2434-105">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="c2434-106">Le destinazioni dei processi sono ospitate in sistemi, in modo analogo al modo in cui i servizi sono ospitati nei sistemi.</span><span class="sxs-lookup"><span data-stu-id="c2434-106">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2434-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c2434-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c2434-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c2434-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c2434-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c2434-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c2434-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c2434-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2434-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2434-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{673E0A2C-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestination : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="c2434-112">Members</span><span class="sxs-lookup"><span data-stu-id="c2434-112">Members</span></span>

<span data-ttu-id="c2434-113">La classe **CIM \_ JobDestination** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c2434-113">The **CIM\_JobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="c2434-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c2434-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2434-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c2434-115">Properties</span></span>

<span data-ttu-id="c2434-116">La classe **CIM \_ JobDestination** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c2434-116">The **CIM\_JobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2434-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c2434-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2434-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2434-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2434-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2434-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2434-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c2434-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c2434-121">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2434-121">A short textual description of the object.</span></span>

<span data-ttu-id="c2434-122">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2434-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2434-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c2434-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2434-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2434-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2434-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2434-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2434-126">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c2434-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c2434-127">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="c2434-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c2434-128">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="c2434-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="c2434-129">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c2434-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2434-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2434-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2434-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2434-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2434-132">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c2434-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c2434-133">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2434-133">A textual description of the object.</span></span>

<span data-ttu-id="c2434-134">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2434-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2434-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c2434-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2434-136">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c2434-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c2434-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2434-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2434-138">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="c2434-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c2434-139">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="c2434-139">Indicates when the object was installed.</span></span> <span data-ttu-id="c2434-140">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="c2434-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c2434-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2434-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2434-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c2434-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2434-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2434-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2434-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2434-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2434-145">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c2434-145">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c2434-146">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="c2434-146">Label by which the object is known.</span></span> <span data-ttu-id="c2434-147">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="c2434-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c2434-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2434-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2434-149">**Status**</span><span class="sxs-lookup"><span data-stu-id="c2434-149">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2434-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2434-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2434-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2434-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2434-152">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c2434-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c2434-153">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2434-153">String that indicates the current status of the object.</span></span> <span data-ttu-id="c2434-154">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="c2434-154">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c2434-155">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="c2434-155">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c2434-156">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="c2434-156">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c2434-157">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="c2434-157">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c2434-158">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="c2434-158">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c2434-159">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="c2434-159">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c2434-160">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2434-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c2434-161">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2434-161">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c2434-162">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c2434-162">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c2434-163">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="c2434-163">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c2434-164">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="c2434-164">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c2434-165">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="c2434-165">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c2434-166">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="c2434-166">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c2434-167">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="c2434-167">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c2434-168">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="c2434-168">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c2434-169">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="c2434-169">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c2434-170">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="c2434-170">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c2434-171">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="c2434-171">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c2434-172">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="c2434-172">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c2434-173">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="c2434-173">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c2434-174">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c2434-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2434-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2434-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2434-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2434-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2434-177">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="c2434-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="c2434-178">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="c2434-178">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="c2434-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c2434-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2434-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2434-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2434-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2434-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2434-182">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="c2434-182">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="c2434-183">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="c2434-183">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2434-184">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2434-184">Remarks</span></span>

<span data-ttu-id="c2434-185">La classe **CIM \_ JobDestination** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2434-185">The **CIM\_JobDestination** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="c2434-186">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="c2434-186">WMI does not implement this class.</span></span>

<span data-ttu-id="c2434-187">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c2434-187">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c2434-188">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c2434-188">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2434-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2434-189">Requirements</span></span>



| <span data-ttu-id="c2434-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2434-190">Requirement</span></span> | <span data-ttu-id="c2434-191">Valore</span><span class="sxs-lookup"><span data-stu-id="c2434-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2434-192">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2434-192">Minimum supported client</span></span><br/> | <span data-ttu-id="c2434-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2434-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2434-194">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2434-194">Minimum supported server</span></span><br/> | <span data-ttu-id="c2434-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2434-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2434-196">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c2434-196">Namespace</span></span><br/>                | <span data-ttu-id="c2434-197">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c2434-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c2434-198">MOF</span><span class="sxs-lookup"><span data-stu-id="c2434-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2434-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2434-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2434-200">DLL</span><span class="sxs-lookup"><span data-stu-id="c2434-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2434-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2434-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2434-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2434-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2434-203">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="c2434-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

