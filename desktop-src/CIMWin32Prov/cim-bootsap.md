---
description: La \_ classe CIM BootSAP rappresenta i punti di accesso di un servizio di avvio.
ms.assetid: eea6d6c5-3930-4e20-b7d3-b6d5722662cd
ms.tgt_platform: multiple
title: Classe CIM_BootSAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootSAP
- CIM_BootSAP.Caption
- CIM_BootSAP.Description
- CIM_BootSAP.InstallDate
- CIM_BootSAP.Status
- CIM_BootSAP.CreationClassName
- CIM_BootSAP.Name
- CIM_BootSAP.SystemCreationClassName
- CIM_BootSAP.SystemName
- CIM_BootSAP.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4868497c2d604457a45273b1c0cc609ae361ad9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304989"
---
# <a name="cim_bootsap-class"></a><span data-ttu-id="3da34-103">CIM \_ BootSAP (classe)</span><span class="sxs-lookup"><span data-stu-id="3da34-103">CIM\_BootSAP class</span></span>

<span data-ttu-id="3da34-104">La classe **CIM \_ BootSAP** rappresenta i punti di accesso di un servizio di avvio.</span><span class="sxs-lookup"><span data-stu-id="3da34-104">The **CIM\_BootSAP** class represents the access points of a boot service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3da34-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="3da34-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3da34-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3da34-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3da34-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3da34-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3da34-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3da34-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da34-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3da34-109">Syntax</span></span>

``` syntax
[UUID("{F6FEF20A-E3D2-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootSAP : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="3da34-110">Members</span><span class="sxs-lookup"><span data-stu-id="3da34-110">Members</span></span>

<span data-ttu-id="3da34-111">La classe **CIM \_ BootSAP** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3da34-111">The **CIM\_BootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="3da34-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3da34-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3da34-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3da34-113">Properties</span></span>

<span data-ttu-id="3da34-114">La classe **CIM \_ BootSAP** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3da34-114">The **CIM\_BootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3da34-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="3da34-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3da34-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3da34-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3da34-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3da34-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3da34-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3da34-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3da34-119">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3da34-119">A short textual description of the object.</span></span>

<span data-ttu-id="3da34-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3da34-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3da34-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3da34-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3da34-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3da34-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3da34-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3da34-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3da34-124">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3da34-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3da34-125">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="3da34-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3da34-126">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="3da34-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3da34-127">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="3da34-127">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="3da34-128">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3da34-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3da34-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3da34-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3da34-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3da34-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3da34-131">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="3da34-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3da34-132">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3da34-132">A textual description of the object.</span></span>

<span data-ttu-id="3da34-133">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3da34-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3da34-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3da34-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3da34-135">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3da34-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3da34-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3da34-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3da34-137">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="3da34-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3da34-138">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="3da34-138">Indicates when the object was installed.</span></span> <span data-ttu-id="3da34-139">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="3da34-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3da34-140">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3da34-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3da34-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3da34-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3da34-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3da34-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3da34-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3da34-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3da34-144">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3da34-144">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3da34-145">Identifica in modo univoco il punto di accesso al servizio e fornisce un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="3da34-145">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="3da34-146">Questa funzionalità è descritta più dettagliatamente nella proprietà Description dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3da34-146">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="3da34-147">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="3da34-147">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="3da34-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="3da34-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3da34-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3da34-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3da34-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3da34-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3da34-151">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="3da34-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3da34-152">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3da34-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="3da34-153">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="3da34-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="3da34-154">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="3da34-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="3da34-155">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="3da34-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="3da34-156">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="3da34-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3da34-157">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="3da34-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3da34-158">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="3da34-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3da34-159">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3da34-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3da34-160">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3da34-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3da34-161">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3da34-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3da34-162">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="3da34-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3da34-163">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="3da34-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3da34-164">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="3da34-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3da34-165">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="3da34-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3da34-166">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="3da34-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3da34-167">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="3da34-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3da34-168">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="3da34-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3da34-169">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="3da34-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3da34-170">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="3da34-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3da34-171">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="3da34-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3da34-172">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="3da34-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3da34-173">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3da34-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3da34-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3da34-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3da34-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3da34-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3da34-176">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3da34-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3da34-177">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="3da34-177">The scoping system's creation class name.</span></span>

<span data-ttu-id="3da34-178">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="3da34-178">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="3da34-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3da34-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3da34-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3da34-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3da34-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3da34-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3da34-182">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3da34-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3da34-183">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="3da34-183">The scoping system's name.</span></span>

<span data-ttu-id="3da34-184">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="3da34-184">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="3da34-185">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3da34-185">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3da34-186">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3da34-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3da34-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3da34-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3da34-188">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3da34-188">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3da34-189">Tipo di SAP, ad esempio collegato o reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="3da34-189">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="3da34-190">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="3da34-190">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="3da34-191">**Scrittura** (1)</span><span class="sxs-lookup"><span data-stu-id="3da34-191">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="3da34-192">**Lettura** (2)</span><span class="sxs-lookup"><span data-stu-id="3da34-192">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="3da34-193">**Reindirizzato** (4)</span><span class="sxs-lookup"><span data-stu-id="3da34-193">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="3da34-194">**Rete \_ Collegato** (8)</span><span class="sxs-lookup"><span data-stu-id="3da34-194">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3da34-195">**sconosciuto** (16)</span><span class="sxs-lookup"><span data-stu-id="3da34-195">**unknown** (16)</span></span>


<span data-ttu-id="3da34-196"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3da34-196"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="3da34-197">Commenti</span><span class="sxs-lookup"><span data-stu-id="3da34-197">Remarks</span></span>

<span data-ttu-id="3da34-198">La classe **CIM \_ BootSAP** è derivata da [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="3da34-198">The **CIM\_BootSAP** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<span data-ttu-id="3da34-199">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="3da34-199">WMI does not implement this class.</span></span>

<span data-ttu-id="3da34-200">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="3da34-200">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3da34-201">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="3da34-201">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da34-202">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3da34-202">Requirements</span></span>



| <span data-ttu-id="3da34-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="3da34-203">Requirement</span></span> | <span data-ttu-id="3da34-204">Valore</span><span class="sxs-lookup"><span data-stu-id="3da34-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3da34-205">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3da34-205">Minimum supported client</span></span><br/> | <span data-ttu-id="3da34-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3da34-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3da34-207">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3da34-207">Minimum supported server</span></span><br/> | <span data-ttu-id="3da34-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3da34-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3da34-209">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3da34-209">Namespace</span></span><br/>                | <span data-ttu-id="3da34-210">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3da34-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3da34-211">MOF</span><span class="sxs-lookup"><span data-stu-id="3da34-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3da34-212"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3da34-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3da34-213">DLL</span><span class="sxs-lookup"><span data-stu-id="3da34-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3da34-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3da34-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3da34-215">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3da34-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da34-216">**\_SERVICEACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="3da34-216">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> </dl>

 

