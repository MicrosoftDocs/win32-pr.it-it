---
description: MSVM \_ GuestService è la classe base astratta per i servizi nel Guest a cui è possibile accedere dall'host.
ms.assetid: F9E6FFE6-B8C5-4F06-BF22-A4BDB20F813A
title: Classe Msvm_GuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService
- Msvm_GuestService.Caption
- Msvm_GuestService.CreationClassName
- Msvm_GuestService.Description
- Msvm_GuestService.InstallDate
- Msvm_GuestService.Name
- Msvm_GuestService.Started
- Msvm_GuestService.StartMode
- Msvm_GuestService.Status
- Msvm_GuestService.SystemCreationClassName
- Msvm_GuestService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99d1936a2678fc2d8357974f9c11a250a1d9bce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401614"
---
# <a name="msvm_guestservice-class"></a><span data-ttu-id="f1c8b-103">\_Classe MSVM GuestService</span><span class="sxs-lookup"><span data-stu-id="f1c8b-103">Msvm\_GuestService class</span></span>

<span data-ttu-id="f1c8b-104">**MSVM \_ GuestService** è la classe di base astratta per i servizi nel Guest a cui è possibile accedere dall'host.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-104">**Msvm\_GuestService** is the abstract base class for services in the guest that can be accessed from the host.</span></span> <span data-ttu-id="f1c8b-105">Questa classe deriva dalla classe del [**\_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service) .</span><span class="sxs-lookup"><span data-stu-id="f1c8b-105">This class derives from the [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service) class.</span></span>

<span data-ttu-id="f1c8b-106">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c8b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1c8b-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_GuestService : CIM_Service
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="f1c8b-108">Members</span><span class="sxs-lookup"><span data-stu-id="f1c8b-108">Members</span></span>

<span data-ttu-id="f1c8b-109">La **classe \_ GuestService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f1c8b-109">The **Msvm\_GuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="f1c8b-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="f1c8b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f1c8b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1c8b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f1c8b-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="f1c8b-112">Methods</span></span>

<span data-ttu-id="f1c8b-113">La **classe \_ GuestService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-113">The **Msvm\_GuestService** class has these methods.</span></span>



| <span data-ttu-id="f1c8b-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="f1c8b-114">Method</span></span>                                                             | <span data-ttu-id="f1c8b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1c8b-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1c8b-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestservice.md) | <span data-ttu-id="f1c8b-117">Richiede che lo stato del servizio Guest venga modificato nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-117">Requests that the state of the guest service be changed to the specified value.</span></span><br/> |
| [<span data-ttu-id="f1c8b-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-118">**StartService**</span></span>](startservice-msvm-guestservice.md)             | <span data-ttu-id="f1c8b-119">Inserisce il servizio Guest in uno stato avviato.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-119">Puts the guest service in a started state.</span></span> <br/>                                     |
| [<span data-ttu-id="f1c8b-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-120">**StopService**</span></span>](stopservice-msvm-guestservice.md)               | <span data-ttu-id="f1c8b-121">Arresta il servizio Guest.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-121">Stops the guest service.</span></span> <br/>                                                       |



 

### <a name="properties"></a><span data-ttu-id="f1c8b-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1c8b-122">Properties</span></span>

<span data-ttu-id="f1c8b-123">La **classe \_ GuestService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-123">The **Msvm\_GuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1c8b-124">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c8b-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1c8b-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1c8b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1c8b-127">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-127">Short textual description of the object.</span></span> <span data-ttu-id="f1c8b-128">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1c8b-128">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1c8b-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c8b-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1c8b-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1c8b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1c8b-132">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-132">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f1c8b-133">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-133">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="f1c8b-134">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c8b-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1c8b-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1c8b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1c8b-137">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-137">Textual description of the object.</span></span> <span data-ttu-id="f1c8b-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1c8b-138">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1c8b-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c8b-140">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1c8b-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1c8b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1c8b-142">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-142">Date and time the object was installed.</span></span> <span data-ttu-id="f1c8b-143">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-143">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="f1c8b-144">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1c8b-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1c8b-145">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c8b-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1c8b-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1c8b-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1c8b-148">Identificatore univoco per il servizio che fornisce anche un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-148">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="f1c8b-149">Per ulteriori informazioni sulla funzionalità, vedere la proprietà **Description** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-149">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="f1c8b-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1c8b-150">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1c8b-151">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-151">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c8b-152">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1c8b-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1c8b-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1c8b-154">Se **true**, il servizio è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-154">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="f1c8b-155">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-155">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c8b-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1c8b-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1c8b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1c8b-158">Indica se il servizio viene avviato automaticamente, ad esempio da un sistema operativo, o se è stato avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-158">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="f1c8b-159">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1c8b-159">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="f1c8b-160">**Automatica**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-160">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="f1c8b-161">**Manuale**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-161">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1c8b-162">**Status**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-162">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c8b-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1c8b-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1c8b-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1c8b-165">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-165">Current status of the object.</span></span> <span data-ttu-id="f1c8b-166">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1c8b-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="f1c8b-167">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1c8b-167">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="f1c8b-168">**OK**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-168">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="f1c8b-169">**Errore**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-169">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="f1c8b-170">**Degradato**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-170">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="f1c8b-171">**Sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-171">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="f1c8b-172">**"Errore di predazione"**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-172">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="f1c8b-173">**Avvio**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-173">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="f1c8b-174">**Arresto**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-174">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="f1c8b-175">**Servizio**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-175">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="f1c8b-176">**Sottolineato**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-176">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="f1c8b-177">**"Non ripristino"**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-177">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="f1c8b-178">**"Nessun contatto"**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-178">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="f1c8b-179">**"Lost comm"**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-179">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1c8b-180">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-180">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c8b-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1c8b-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1c8b-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1c8b-183">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-183">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="f1c8b-184">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-184">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c8b-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1c8b-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1c8b-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1c8b-187">Nome del sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="f1c8b-187">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1c8b-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1c8b-188">Requirements</span></span>



| <span data-ttu-id="f1c8b-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1c8b-189">Requirement</span></span> | <span data-ttu-id="f1c8b-190">Valore</span><span class="sxs-lookup"><span data-stu-id="f1c8b-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c8b-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1c8b-191">Minimum supported client</span></span><br/> | <span data-ttu-id="f1c8b-192">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1c8b-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f1c8b-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1c8b-193">Minimum supported server</span></span><br/> | <span data-ttu-id="f1c8b-194">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1c8b-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f1c8b-195">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f1c8b-195">Namespace</span></span><br/>                | <span data-ttu-id="f1c8b-196">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1c8b-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f1c8b-197">MOF</span><span class="sxs-lookup"><span data-stu-id="f1c8b-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1c8b-198"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1c8b-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1c8b-199">DLL</span><span class="sxs-lookup"><span data-stu-id="f1c8b-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1c8b-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1c8b-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1c8b-201">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1c8b-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c8b-202">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-202">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="f1c8b-203">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="f1c8b-203">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

