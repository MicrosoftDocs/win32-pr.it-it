---
description: MSVM \_ GuestFileService contiene un metodo che può essere usato per copiare un file in una macchina virtuale dall'host Hyper-V.
ms.assetid: 3599d5a8-415f-48f8-b887-00a93b7abb83
title: Classe Msvm_GuestFileService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService
- Msvm_GuestFileService.StartService
- Msvm_GuestFileService.StopService
- Msvm_GuestFileService.Caption
- Msvm_GuestFileService.CreationClassName
- Msvm_GuestFileService.Description
- Msvm_GuestFileService.InstallDate
- Msvm_GuestFileService.Name
- Msvm_GuestFileService.Started
- Msvm_GuestFileService.StartMode
- Msvm_GuestFileService.Status
- Msvm_GuestFileService.SystemCreationClassName
- Msvm_GuestFileService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ee0f235d7549428ecf02e9c758c83bcea33efe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306043"
---
# <a name="msvm_guestfileservice-class"></a><span data-ttu-id="29bef-103">\_Classe MSVM GuestFileService</span><span class="sxs-lookup"><span data-stu-id="29bef-103">Msvm\_GuestFileService class</span></span>

<span data-ttu-id="29bef-104">**MSVM \_ GuestFileService** contiene un metodo che può essere utilizzato per copiare un file in una macchina virtuale dall'host Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="29bef-104">**Msvm\_GuestFileService** contains a method that can be used to copy a file to a virtual machine from the Hyper-V host.</span></span> <span data-ttu-id="29bef-105">Questa classe deriva da [**MSVM \_ GuestService**](msvm-guestservice.md).</span><span class="sxs-lookup"><span data-stu-id="29bef-105">This class derives from [**Msvm\_GuestService**](msvm-guestservice.md).</span></span>

<span data-ttu-id="29bef-106">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="29bef-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="29bef-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29bef-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestFileService : Msvm_GuestService
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

## <a name="members"></a><span data-ttu-id="29bef-108">Members</span><span class="sxs-lookup"><span data-stu-id="29bef-108">Members</span></span>

<span data-ttu-id="29bef-109">La **classe \_ GuestFileService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="29bef-109">The **Msvm\_GuestFileService** class has these types of members:</span></span>

-   [<span data-ttu-id="29bef-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="29bef-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="29bef-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="29bef-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="29bef-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="29bef-112">Methods</span></span>

<span data-ttu-id="29bef-113">La **classe \_ GuestFileService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="29bef-113">The **Msvm\_GuestFileService** class has these methods.</span></span>



| <span data-ttu-id="29bef-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="29bef-114">Method</span></span>                                                             | <span data-ttu-id="29bef-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29bef-115">Description</span></span>                                                                                                                                                                  |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29bef-116">**CopyFilesToGuest**</span><span class="sxs-lookup"><span data-stu-id="29bef-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md) | <span data-ttu-id="29bef-117">Copia i file dall'host Hyper-V alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="29bef-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> <span data-ttu-id="29bef-118">**Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="29bef-118">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| <span data-ttu-id="29bef-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="29bef-119">**StartService**</span></span>                                                   | <span data-ttu-id="29bef-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="29bef-120">This method is not supported.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="29bef-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="29bef-121">**StopService**</span></span>                                                    | <span data-ttu-id="29bef-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="29bef-122">This method is not supported.</span></span><br/>                                                                                                                                     |



 

### <a name="properties"></a><span data-ttu-id="29bef-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="29bef-123">Properties</span></span>

<span data-ttu-id="29bef-124">La **classe \_ GuestFileService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="29bef-124">The **Msvm\_GuestFileService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29bef-125">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="29bef-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bef-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29bef-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bef-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29bef-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bef-128">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="29bef-128">Short textual description of the object.</span></span> <span data-ttu-id="29bef-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="29bef-129">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="29bef-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="29bef-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bef-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29bef-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bef-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29bef-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bef-133">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="29bef-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="29bef-134">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="29bef-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="29bef-135">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="29bef-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bef-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29bef-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bef-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29bef-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bef-138">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="29bef-138">Textual description of the object.</span></span> <span data-ttu-id="29bef-139">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="29bef-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="29bef-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="29bef-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bef-141">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="29bef-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="29bef-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29bef-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bef-143">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="29bef-143">Date and time the object was installed.</span></span> <span data-ttu-id="29bef-144">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="29bef-144">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="29bef-145">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="29bef-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="29bef-146">**Nome**</span><span class="sxs-lookup"><span data-stu-id="29bef-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bef-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29bef-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bef-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29bef-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bef-149">Identificatore univoco per il servizio che fornisce anche un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="29bef-149">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="29bef-150">Per ulteriori informazioni sulla funzionalità, vedere la proprietà **Description** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="29bef-150">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="29bef-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="29bef-151">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="29bef-152">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="29bef-152">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bef-153">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="29bef-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29bef-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29bef-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bef-155">Se **true**, il servizio è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="29bef-155">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="29bef-156">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="29bef-156">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bef-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29bef-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bef-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29bef-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bef-159">Indica se il servizio viene avviato automaticamente, ad esempio da un sistema operativo, o se è stato avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="29bef-159">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="29bef-160">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="29bef-160">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="29bef-161">**Automatica**</span><span class="sxs-lookup"><span data-stu-id="29bef-161">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="29bef-162">**Manuale**</span><span class="sxs-lookup"><span data-stu-id="29bef-162">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="29bef-163">**Status**</span><span class="sxs-lookup"><span data-stu-id="29bef-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bef-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29bef-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bef-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29bef-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bef-166">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="29bef-166">Current status of the object.</span></span> <span data-ttu-id="29bef-167">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="29bef-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="29bef-168">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="29bef-168">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="29bef-169">**OK**</span><span class="sxs-lookup"><span data-stu-id="29bef-169">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="29bef-170">**Errore**</span><span class="sxs-lookup"><span data-stu-id="29bef-170">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="29bef-171">**Degradato**</span><span class="sxs-lookup"><span data-stu-id="29bef-171">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="29bef-172">**Sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="29bef-172">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="29bef-173">**"Errore di predazione"**</span><span class="sxs-lookup"><span data-stu-id="29bef-173">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="29bef-174">**Avvio**</span><span class="sxs-lookup"><span data-stu-id="29bef-174">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="29bef-175">**Arresto**</span><span class="sxs-lookup"><span data-stu-id="29bef-175">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="29bef-176">**Servizio**</span><span class="sxs-lookup"><span data-stu-id="29bef-176">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="29bef-177">**Sottolineato**</span><span class="sxs-lookup"><span data-stu-id="29bef-177">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="29bef-178">**"Non ripristino"**</span><span class="sxs-lookup"><span data-stu-id="29bef-178">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="29bef-179">**"Nessun contatto"**</span><span class="sxs-lookup"><span data-stu-id="29bef-179">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="29bef-180">**"Lost comm"**</span><span class="sxs-lookup"><span data-stu-id="29bef-180">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="29bef-181">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="29bef-181">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bef-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29bef-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bef-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29bef-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bef-184">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="29bef-184">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="29bef-185">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="29bef-185">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bef-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29bef-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bef-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29bef-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bef-188">Nome del sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="29bef-188">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29bef-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29bef-189">Requirements</span></span>



| <span data-ttu-id="29bef-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="29bef-190">Requirement</span></span> | <span data-ttu-id="29bef-191">Valore</span><span class="sxs-lookup"><span data-stu-id="29bef-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29bef-192">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29bef-192">Minimum supported client</span></span><br/> | <span data-ttu-id="29bef-193">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="29bef-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="29bef-194">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29bef-194">Minimum supported server</span></span><br/> | <span data-ttu-id="29bef-195">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="29bef-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="29bef-196">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="29bef-196">Namespace</span></span><br/>                | <span data-ttu-id="29bef-197">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="29bef-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="29bef-198">MOF</span><span class="sxs-lookup"><span data-stu-id="29bef-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29bef-199"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29bef-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="29bef-200">DLL</span><span class="sxs-lookup"><span data-stu-id="29bef-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29bef-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="29bef-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="29bef-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29bef-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29bef-203">**\_GuestService MSVM**</span><span class="sxs-lookup"><span data-stu-id="29bef-203">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

