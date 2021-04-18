---
description: La \_ classe CIM BOOTSERVICE rappresenta la funzionalità fornita da un dispositivo o un software, o da una rete, per caricare un sistema operativo in un computer di sistema.
ms.assetid: d9c969bb-0f54-4e94-8e19-7ccd6f5adfb3
ms.tgt_platform: multiple
title: Classe CIM_BootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService
- CIM_BootService.Caption
- CIM_BootService.Description
- CIM_BootService.InstallDate
- CIM_BootService.Status
- CIM_BootService.CreationClassName
- CIM_BootService.Name
- CIM_BootService.Started
- CIM_BootService.StartMode
- CIM_BootService.SystemCreationClassName
- CIM_BootService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d32a8fdfe61e02e6ffe3a8dd2f115e57f338aec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304986"
---
# <a name="cim_bootservice-class"></a><span data-ttu-id="cd894-103">CIM \_ BOOTSERVICE (classe)</span><span class="sxs-lookup"><span data-stu-id="cd894-103">CIM\_BootService class</span></span>

<span data-ttu-id="cd894-104">La classe **CIM \_ BOOTSERVICE** rappresenta la funzionalità fornita da un dispositivo o un software, o da una rete, per caricare un sistema operativo in un computer di sistema.</span><span class="sxs-lookup"><span data-stu-id="cd894-104">The **CIM\_BootService** class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd894-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="cd894-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cd894-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cd894-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cd894-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cd894-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cd894-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="cd894-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd894-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd894-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FE-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_BootService : CIM_Service
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="cd894-110">Members</span><span class="sxs-lookup"><span data-stu-id="cd894-110">Members</span></span>

<span data-ttu-id="cd894-111">La classe **CIM \_ BOOTSERVICE** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cd894-111">The **CIM\_BootService** class has these types of members:</span></span>

-   [<span data-ttu-id="cd894-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="cd894-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="cd894-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd894-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cd894-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="cd894-114">Methods</span></span>

<span data-ttu-id="cd894-115">La classe **CIM \_ BOOTSERVICE** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cd894-115">The **CIM\_BootService** class has these methods.</span></span>



| <span data-ttu-id="cd894-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="cd894-116">Method</span></span>                                                               | <span data-ttu-id="cd894-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd894-117">Description</span></span>                                                               |
|:---------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="cd894-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="cd894-118">**StartService**</span></span>](startservice-method-in-class-cim-bootservice.md) | <span data-ttu-id="cd894-119">Inserisce il servizio nello stato avviato.</span><span class="sxs-lookup"><span data-stu-id="cd894-119">Puts the service in the started state.</span></span> <span data-ttu-id="cd894-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="cd894-120">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="cd894-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="cd894-121">**StopService**</span></span>](stopservice-method-in-class-cim-bootservice.md)   | <span data-ttu-id="cd894-122">Inserisce il servizio nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="cd894-122">Puts the service in the stopped state.</span></span> <span data-ttu-id="cd894-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="cd894-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cd894-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd894-124">Properties</span></span>

<span data-ttu-id="cd894-125">La classe **CIM \_ BOOTSERVICE** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cd894-125">The **CIM\_BootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd894-126">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="cd894-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd894-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd894-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd894-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd894-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd894-129">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cd894-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cd894-130">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd894-130">A short textual description of the object.</span></span>

<span data-ttu-id="cd894-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd894-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd894-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd894-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd894-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd894-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd894-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd894-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd894-135">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="cd894-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd894-136">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="cd894-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cd894-137">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="cd894-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cd894-138">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cd894-138">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd894-139">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="cd894-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd894-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd894-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd894-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd894-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd894-142">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="cd894-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cd894-143">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd894-143">A textual description of the object.</span></span>

<span data-ttu-id="cd894-144">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd894-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd894-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cd894-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd894-146">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd894-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd894-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd894-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd894-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="cd894-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cd894-149">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="cd894-149">Indicates when the object was installed.</span></span> <span data-ttu-id="cd894-150">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="cd894-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="cd894-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd894-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd894-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cd894-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd894-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd894-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd894-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd894-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd894-155">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cd894-155">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cd894-156">La proprietà Name identifica in modo univoco il servizio e fornisce un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="cd894-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="cd894-157">Questa funzionalità è descritta più dettagliatamente nella proprietà **Description** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd894-157">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="cd894-158">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cd894-158">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd894-159">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="cd894-159">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd894-160">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cd894-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd894-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd894-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd894-162">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="cd894-162">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="cd894-163">Se **true**, il servizio è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="cd894-163">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="cd894-164">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cd894-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd894-165">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="cd894-165">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd894-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd894-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd894-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd894-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd894-168">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modalità di avvio")</span><span class="sxs-lookup"><span data-stu-id="cd894-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="cd894-169">Indica se il servizio viene avviato automaticamente, ad esempio da un sistema operativo, o se è stato avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="cd894-169">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="cd894-170">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cd894-170">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="cd894-171">**Automatico** ("automatico")</span><span class="sxs-lookup"><span data-stu-id="cd894-171">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="cd894-172">**Manuale** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="cd894-172">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd894-173">**Status**</span><span class="sxs-lookup"><span data-stu-id="cd894-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd894-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd894-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd894-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd894-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd894-176">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="cd894-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cd894-177">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd894-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="cd894-178">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="cd894-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="cd894-179">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="cd894-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="cd894-180">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="cd894-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="cd894-181">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="cd894-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cd894-182">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="cd894-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cd894-183">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="cd894-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cd894-184">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd894-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cd894-185">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd894-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cd894-186">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="cd894-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cd894-187">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="cd894-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cd894-188">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="cd894-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cd894-189">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="cd894-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cd894-190">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="cd894-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cd894-191">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="cd894-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cd894-192">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="cd894-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cd894-193">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="cd894-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cd894-194">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="cd894-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cd894-195">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="cd894-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cd894-196">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="cd894-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cd894-197">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="cd894-197">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd894-198">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd894-198">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd894-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd894-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd894-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd894-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd894-201">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema ")</span><span class="sxs-lookup"><span data-stu-id="cd894-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd894-202">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="cd894-202">Scoping system's creation class name.</span></span>

<span data-ttu-id="cd894-203">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cd894-203">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd894-204">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cd894-204">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd894-205">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd894-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd894-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd894-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd894-207">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema ")</span><span class="sxs-lookup"><span data-stu-id="cd894-207">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd894-208">Nome del sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="cd894-208">Name of the system that hosts the service.</span></span>

<span data-ttu-id="cd894-209">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cd894-209">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd894-210">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd894-210">Remarks</span></span>

<span data-ttu-id="cd894-211">La classe **CIM \_ BOOTSERVICE** deriva dal [**\_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cd894-211">The **CIM\_BootService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="cd894-212">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="cd894-212">WMI does not implement this class.</span></span>

<span data-ttu-id="cd894-213">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="cd894-213">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cd894-214">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="cd894-214">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd894-215">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd894-215">Requirements</span></span>



| <span data-ttu-id="cd894-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd894-216">Requirement</span></span> | <span data-ttu-id="cd894-217">Valore</span><span class="sxs-lookup"><span data-stu-id="cd894-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd894-218">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd894-218">Minimum supported client</span></span><br/> | <span data-ttu-id="cd894-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd894-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd894-220">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd894-220">Minimum supported server</span></span><br/> | <span data-ttu-id="cd894-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd894-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd894-222">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd894-222">Namespace</span></span><br/>                | <span data-ttu-id="cd894-223">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="cd894-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd894-224">MOF</span><span class="sxs-lookup"><span data-stu-id="cd894-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd894-225"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd894-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd894-226">DLL</span><span class="sxs-lookup"><span data-stu-id="cd894-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd894-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd894-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd894-228">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd894-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd894-229">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="cd894-229">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

