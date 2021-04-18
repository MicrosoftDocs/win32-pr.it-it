---
Description: Il \_ processo Win32&\# 32; La classe WMI rappresenta un processo in un sistema operativo.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Classe Win32_Process
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327251"
---
# <a name="win32_process-class"></a><span data-ttu-id="ceb4c-103">\_Classe processo Win32</span><span class="sxs-lookup"><span data-stu-id="ceb4c-103">Win32\_Process class</span></span>

<span data-ttu-id="ceb4c-104">La [classe WMI](../wmisdk/retrieving-a-class.md) del **\_ processo Win32** rappresenta un processo in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-104">The **Win32\_Process** [WMI class](../wmisdk/retrieving-a-class.md) represents a process on an operating system.</span></span>

<span data-ttu-id="ceb4c-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

> [!NOTE]
> <span data-ttu-id="ceb4c-106">Per una discussione generale su processi e thread in Windows, vedere l'argomento [processi e thread](/ProcThread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-106">For a general discussion on Processes and Threads within Windows, please see the topic [Processes and Threads](/ProcThread/processes-and-threads.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ceb4c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ceb4c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a><span data-ttu-id="ceb4c-108">Members</span><span class="sxs-lookup"><span data-stu-id="ceb4c-108">Members</span></span>

<span data-ttu-id="ceb4c-109">La classe di **\_ processo Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ceb4c-109">The **Win32\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="ceb4c-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ceb4c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ceb4c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ceb4c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ceb4c-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="ceb4c-112">Methods</span></span>

<span data-ttu-id="ceb4c-113">La classe di **\_ processo Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-113">The **Win32\_Process** class has these methods.</span></span>



| <span data-ttu-id="ceb4c-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="ceb4c-114">Method</span></span>                                                                   | <span data-ttu-id="ceb4c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ceb4c-115">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceb4c-116">**AttachDebugger**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-116">**AttachDebugger**</span></span>](attachdebugger-method-in-class-win32-process.md)   | <span data-ttu-id="ceb4c-117">Avvia il debugger attualmente registrato per un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-117">Launches the currently registered debugger for a process.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="ceb4c-118">**Creare**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-118">**Create**</span></span>](create-method-in-class-win32-process.md)                   | <span data-ttu-id="ceb4c-119">Crea un nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-119">Creates a new process.</span></span><br/>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="ceb4c-120">**GetAvailableVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-120">**GetAvailableVirtualSize**</span></span>](getavailablevirtualsize-win32-process.md) | <span data-ttu-id="ceb4c-121">Recupera le dimensioni correnti, in byte, dello spazio degli indirizzi virtuali libero disponibile per il processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-121">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span><br/> <span data-ttu-id="ceb4c-122">**Windows server 2012, Windows 8, Windows 7, Windows server 2008 e Windows Vista:** Questo metodo non è supportato prima di Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-122">**Windows Server 2012, Windows 8, Windows 7, Windows Server 2008 and Windows Vista:** This method is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="ceb4c-123">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-123">**GetOwner**</span></span>](getowner-method-in-class-win32-process.md)               | <span data-ttu-id="ceb4c-124">Recupera il nome utente e il nome di dominio in cui è in esecuzione il processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-124">Retrieves the user name and domain name under which the process is running.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="ceb4c-125">**GetOwnerSid**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-125">**GetOwnerSid**</span></span>](getownersid-method-in-class-win32-process.md)         | <span data-ttu-id="ceb4c-126">Recupera l'ID di sicurezza (SID) per il proprietario di un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-126">Retrieves the security identifier (SID) for the owner of a process.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="ceb4c-127">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-127">**SetPriority**</span></span>](setpriority-method-in-class-win32-process.md)         | <span data-ttu-id="ceb4c-128">Modifica la priorità di esecuzione di un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-128">Changes the execution priority of a process.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="ceb4c-129">**Terminare**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-129">**Terminate**</span></span>](terminate-method-in-class-win32-process.md)             | <span data-ttu-id="ceb4c-130">Termina un processo e tutti i relativi thread.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-130">Terminates a process and all of its threads.</span></span><br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="ceb4c-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ceb4c-131">Properties</span></span>

<span data-ttu-id="ceb4c-132">La classe di **\_ processo Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-132">The **Win32\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ceb4c-133">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-136">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-136">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-137">Breve descrizione di un oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-137">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="ceb4c-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-139">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-139">**CommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-142">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("riga di comando per avviare il processo")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-142">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Command Line To Start Process")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-143">Riga di comando usata per avviare un processo specifico, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-143">Command line used to start a specific process, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-144">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-144">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-147">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-147">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-148">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ceb4c-149">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ceb4c-150">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-150">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-151">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-151">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-152">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-154">Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-154">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-155">Data di inizio dell'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-155">Date the process begins executing.</span></span>

<span data-ttu-id="ceb4c-156">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-156">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-157">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-157">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-160">Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe di sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-160">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-161">Nome della classe di creazione del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-161">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="ceb4c-162">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-162">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-163">**CSName**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-163">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-166">Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-166">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-167">Nome del sistema di ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-167">Name of the scoping computer system.</span></span>

<span data-ttu-id="ceb4c-168">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-168">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-169">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-172">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-172">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-173">Descrizione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-173">Description of an object.</span></span>

<span data-ttu-id="ceb4c-174">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-175">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-175">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-178">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tool Help Structures \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("percorso eseguibile")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-178">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)\|szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Executable Path")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-179">Percorso del file eseguibile del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-179">Path to the executable file of the process.</span></span>

<span data-ttu-id="ceb4c-180">Esempio: "C: \\ Windows \\ System \\Explorer.Exe"</span><span class="sxs-lookup"><span data-stu-id="ceb4c-180">Example: "C:\\Windows\\System\\Explorer.Exe"</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-181">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-181">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-182">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-184">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("stato esecuzione")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-185">Condizione operativa corrente del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-185">Current operating condition of the process.</span></span>

<span data-ttu-id="ceb4c-186">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-186">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ceb4c-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ceb4c-188">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="ceb4c-188">Unknown</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ceb4c-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ceb4c-190">Altro</span><span class="sxs-lookup"><span data-stu-id="ceb4c-190">Other</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="ceb4c-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Pronto** (2)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="ceb4c-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="ceb4c-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloccato** (4)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ceb4c-194">Bloccato</span><span class="sxs-lookup"><span data-stu-id="ceb4c-194">Blocked</span></span>

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="ceb4c-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Sospeso bloccato** (5)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="ceb4c-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Pronto per sospensione** (6)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="ceb4c-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminato** (7)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="ceb4c-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (8)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="ceb4c-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>In **crescita** (9)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ceb4c-200">**Handle**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-200">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-203">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("handle")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-203">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-204">Identificatore del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-204">Process identifier.</span></span>

<span data-ttu-id="ceb4c-205">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-205">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-206">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-206">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-207">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-209">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("handle count")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle Count")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-210">Numero totale di handle aperti di proprietà del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-210">Total number of open handles owned by the process.</span></span> <span data-ttu-id="ceb4c-211">**HandleCount** è la somma degli handle attualmente aperti da ogni thread di questo processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-211">**HandleCount** is the sum of the handles currently open by each thread in this process.</span></span> <span data-ttu-id="ceb4c-212">Viene utilizzato un handle per esaminare o modificare le risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-212">A handle is used to examine or modify the system resources.</span></span> <span data-ttu-id="ceb4c-213">Ogni handle include una voce in una tabella gestita internamente.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-213">Each handle has an entry in a table that is maintained internally.</span></span> <span data-ttu-id="ceb4c-214">Le voci contengono gli indirizzi delle risorse e dei dati per identificare il tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-214">Entries contain the addresses of the resources and data to identify the resource type.</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-216">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-218">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-219">Data di installazione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-219">Date an object is installed.</span></span> <span data-ttu-id="ceb4c-220">L'oggetto può essere installato senza che venga scritto un valore in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-220">The object may be installed without a value being written to this property.</span></span>

<span data-ttu-id="ceb4c-221">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-222">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-222">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-223">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-225">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**unità**](../wmisdk/standard-qualifiers.md) ("100 nanosecondi")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-225">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-226">Tempo in modalità kernel, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-226">Time in kernel mode, in milliseconds.</span></span> <span data-ttu-id="ceb4c-227">Se queste informazioni non sono disponibili, usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-227">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="ceb4c-228">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-228">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-229">**MaximumWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-229">**MaximumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-230">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-232">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| \_ limiti \| di quota MaximumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" dimensioni massime working set "), [**unità**](../wmisdk/standard-qualifiers.md) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-232">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MaximumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Maximum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-233">Dimensioni massime working set del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-233">Maximum working set size of the process.</span></span> <span data-ttu-id="ceb4c-234">Il working set di un processo è il set di pagine di memoria visibile al processo nella RAM fisica.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-234">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="ceb4c-235">Queste pagine sono residenti e disponibili per l'uso da un'applicazione senza attivare un errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-235">These pages are resident, and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="ceb4c-236">Esempio: 1413120</span><span class="sxs-lookup"><span data-stu-id="ceb4c-236">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-237">**MinimumWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-237">**MinimumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-238">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-238">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-240">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| limiti di quota \_ \| MinimumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" dimensioni minime working set "), [**unità**](../wmisdk/standard-qualifiers.md) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-240">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MinimumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Minimum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-241">Dimensioni minime working set del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-241">Minimum working set size of the process.</span></span> <span data-ttu-id="ceb4c-242">Il working set di un processo è il set di pagine di memoria visibile al processo nella RAM fisica.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-242">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="ceb4c-243">Queste pagine sono residenti e disponibili per l'uso da un'applicazione senza attivare un errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-243">These pages are resident and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="ceb4c-244">Esempio: 20480</span><span class="sxs-lookup"><span data-stu-id="ceb4c-244">Example: 20480</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-245">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-245">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-248">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-249">Nome del file eseguibile responsabile del processo, equivalente alla proprietà nome immagine in Gestione attività.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-249">Name of the executable file responsible for the process, equivalent to the Image Name property in Task Manager.</span></span>

<span data-ttu-id="ceb4c-250">Se ereditato da una sottoclasse, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-250">When inherited by a subclass, the property can be overridden to be a key property.</span></span> <span data-ttu-id="ceb4c-251">Il nome è hardcoded nell'applicazione stessa e non è interessato dalla modifica del nome del file.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-251">The name is hard-coded into the application itself and is not affected by changing the file name.</span></span> <span data-ttu-id="ceb4c-252">Ad esempio, anche se si rinomina Calc.exe, il nome Calc.exe verrà comunque visualizzato in Gestione attività e in tutti gli script WMI che recuperano il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-252">For example, even if you rename Calc.exe, the name Calc.exe will still appear in Task Manager and in any WMI scripts that retrieve the process name.</span></span>

<span data-ttu-id="ceb4c-253">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-254">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-254">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-257">Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe sistema operativo ")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-257">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-258">Nome della classe di creazione del sistema operativo di ambito.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-258">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="ceb4c-259">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-259">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-260">**OSName**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-260">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-263">Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome sistema operativo ")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-263">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-264">Nome del sistema operativo di ambito.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-264">Name of the scoping operating system.</span></span>

<span data-ttu-id="ceb4c-265">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-265">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-266">**OtherOperationCount**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-266">**OtherOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-267">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-269">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("altro conteggio operazioni")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-270">Numero di operazioni di I/O eseguite che non sono operazioni di lettura o scrittura.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-270">Number of I/O operations performed that are not read or write operations.</span></span>

<span data-ttu-id="ceb4c-271">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-271">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-272">**OtherTransferCount**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-272">**OtherTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-273">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-273">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-275">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("other Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-276">Quantità di dati trasferiti durante le operazioni che non sono operazioni di lettura o scrittura.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-276">Amount of data transferred during operations that are not read or write operations.</span></span>

<span data-ttu-id="ceb4c-277">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-277">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-278">**PageFaults**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-278">**PageFaults**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-279">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-281">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("numero di errori di pagina")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Number Of Page Faults")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-282">Numero di errori di pagina generati da un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-282">Number of page faults that a process generates.</span></span>

<span data-ttu-id="ceb4c-283">Esempio: 10</span><span class="sxs-lookup"><span data-stu-id="ceb4c-283">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-284">**PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-284">**PageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-285">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-287">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Page file Usage"), [**unità**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-288">Quantità di spazio del file di paging attualmente utilizzata da un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-288">Amount of page file space that a process is using currently.</span></span> <span data-ttu-id="ceb4c-289">Questo valore è coerente con il valore **vmsize** in TaskMgr.exe.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-289">This value is consistent with the **VMSize** value in TaskMgr.exe.</span></span>

<span data-ttu-id="ceb4c-290">Esempio: 102435</span><span class="sxs-lookup"><span data-stu-id="ceb4c-290">Example: 102435</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-291">**ParentProcessId**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-291">**ParentProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-292">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-294">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API process \| status \| System \_ Process \_ Information \| InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID processo padre")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Parent Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-295">Identificatore univoco del processo di creazione di un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-295">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="ceb4c-296">I numeri degli identificatori di processo vengono riutilizzati, in modo che identifichino solo un processo per la durata di tale processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-296">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="ceb4c-297">È possibile che il processo identificato da **ParentProcessId** venga terminato, quindi **ParentProcessId** potrebbe non fare riferimento a un processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-297">It is possible that the process identified by **ParentProcessId** is terminated, so **ParentProcessId** may not refer to a running process.</span></span> <span data-ttu-id="ceb4c-298">È anche possibile che **ParentProcessId** si riferisca erroneamente a un processo che riutilizza un identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-298">It is also possible that **ParentProcessId** incorrectly refers to a process that reuses a process identifier.</span></span> <span data-ttu-id="ceb4c-299">È possibile utilizzare la proprietà **CreationDate** per determinare se l'elemento padre specificato è stato creato dopo che è stato creato il processo rappresentato da questa istanza del **\_ processo Win32** .</span><span class="sxs-lookup"><span data-stu-id="ceb4c-299">You can use the **CreationDate** property to determine whether the specified parent was created after the process represented by this **Win32\_Process** instance was created.</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-300">**PeakPageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-300">**PeakPageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-301">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-303">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak page file Usage"), [**unità**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-304">Quantità massima di spazio per i file di paging utilizzata durante il ciclo di vita di un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-304">Maximum amount of page file space used during the life of a process.</span></span>

<span data-ttu-id="ceb4c-305">Esempio: 102367</span><span class="sxs-lookup"><span data-stu-id="ceb4c-305">Example: 102367</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-306">**PeakVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-306">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-307">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-309">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak virual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Virual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-310">Spazio degli indirizzi virtuali massimo usato da un processo in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-310">Maximum virtual address space a process uses at any one time.</span></span> <span data-ttu-id="ceb4c-311">L'utilizzo dello spazio degli indirizzi virtuali non implica necessariamente l'utilizzo corrispondente di pagine del disco o della memoria principale.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-311">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="ceb4c-312">Tuttavia, lo spazio virtuale è finito e l'uso di un numero eccessivo di processi potrebbe non essere in grado di caricare le librerie.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-312">However, virtual space is finite, and by using too much the process might not be able to load libraries.</span></span>

<span data-ttu-id="ceb4c-313">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-313">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-314">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-314">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-315">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-317">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("picco working set size"), [**unità**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-318">Picco working set dimensioni di un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-318">Peak working set size of a process.</span></span>

<span data-ttu-id="ceb4c-319">Esempio: 1413120</span><span class="sxs-lookup"><span data-stu-id="ceb4c-319">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-320">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-320">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-321">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-323">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| relativa BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-323">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-324">Priorità di pianificazione di un processo all'interno di un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-324">Scheduling priority of a process within an operating system.</span></span> <span data-ttu-id="ceb4c-325">Maggiore è il valore, maggiore è la priorità che un processo riceve.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-325">The higher the value, the higher priority a process receives.</span></span> <span data-ttu-id="ceb4c-326">I valori di priorità possono variare da 0 (zero), ovvero la priorità più bassa a 31, che corrisponde alla priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-326">Priority values can range from 0 (zero), which is the lowest priority to 31, which is highest priority.</span></span>

<span data-ttu-id="ceb4c-327">Esempio: 7</span><span class="sxs-lookup"><span data-stu-id="ceb4c-327">Example: 7</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-328">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-328">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-329">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-331">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("conteggio pagine private")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Private Page Count")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-332">Numero corrente di pagine allocate accessibili solo al processo rappresentato da questa istanza del **\_ processo Win32** .</span><span class="sxs-lookup"><span data-stu-id="ceb4c-332">Current number of pages allocated that are only accessible to the process represented by this **Win32\_Process** instance.</span></span>

<span data-ttu-id="ceb4c-333">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-334">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-334">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-335">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-337">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API processi \| e strutture thread \| [**Process \_ Information**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| DwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID processo")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-337">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)\|dwProcessId "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-338">Identificatore numerico usato per distinguere un processo da un altro.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-338">Numeric identifier used to distinguish one process from another.</span></span> <span data-ttu-id="ceb4c-339">ProcessIDs sono validi dalla fase di creazione del processo per la terminazione del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-339">ProcessIDs are valid from process creation time to process termination.</span></span> <span data-ttu-id="ceb4c-340">Alla chiusura, lo stesso identificatore numerico può essere applicato a un nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-340">Upon termination, that same numeric identifier can be applied to a new process.</span></span>

<span data-ttu-id="ceb4c-341">Ciò significa che non è possibile utilizzare solo ProcessId per monitorare un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-341">This means that you cannot use ProcessID alone to monitor a particular process.</span></span> <span data-ttu-id="ceb4c-342">Ad esempio, un'applicazione può avere un ProcessId pari a 7 e quindi avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-342">For example, an application could have a ProcessID of 7, and then fail.</span></span> <span data-ttu-id="ceb4c-343">Quando viene avviato un nuovo processo, il nuovo processo può essere assegnato come ProcessId 7.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-343">When a new process is started, the new process could be assigned ProcessID 7.</span></span> <span data-ttu-id="ceb4c-344">Uno script controllato solo per un determinato ProcessId potrebbe quindi essere "ingannato" nel pensare che l'applicazione originale era ancora in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-344">A script that checked only for a specified ProcessID could thus be "fooled" into thinking that the original application was still running.</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-345">**QuotaNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-345">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-346">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-348">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("quota di utilizzo del pool non di paging")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-349">Importo della quota di utilizzo del pool non di paging per un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-349">Quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="ceb4c-350">Esempio: 15</span><span class="sxs-lookup"><span data-stu-id="ceb4c-350">Example: 15</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-351">**QuotaPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-351">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-352">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-354">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("quota di utilizzo del pool di paging")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-354">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-355">Importo della quota di utilizzo del pool di paging per un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-355">Quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="ceb4c-356">Esempio: 22</span><span class="sxs-lookup"><span data-stu-id="ceb4c-356">Example: 22</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-357">**QuotaPeakNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-357">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-358">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-360">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak non-paging pool Usage quota")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-361">Importo massimo della quota di utilizzo del pool non di paging per un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-361">Peak quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="ceb4c-362">Esempio: 31</span><span class="sxs-lookup"><span data-stu-id="ceb4c-362">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-363">**QuotaPeakPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-363">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-364">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-366">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("picco di utilizzo pool di paging")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-366">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-367">Importo massimo della quota di utilizzo del pool di paging per un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-367">Peak quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="ceb4c-368">Esempio: 31</span><span class="sxs-lookup"><span data-stu-id="ceb4c-368">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-369">**ReadOperationCount**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-369">**ReadOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-370">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-372">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read operation count")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-373">Numero di operazioni di lettura eseguite.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-373">Number of read operations performed.</span></span>

<span data-ttu-id="ceb4c-374">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-374">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-375">**ReadTransferCount**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-375">**ReadTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-376">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-376">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-378">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-379">Quantità di dati letti.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-379">Amount of data read.</span></span>

<span data-ttu-id="ceb4c-380">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-381">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-381">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-382">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-384">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| SessionID"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID sessione")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-384">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|SessionId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Session Id")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-385">Identificatore univoco generato da un sistema operativo al momento della creazione di una sessione.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-385">Unique identifier that an operating system generates when a session is created.</span></span> <span data-ttu-id="ceb4c-386">Una sessione si estende a un periodo di tempo dall'accesso fino alla disconnessione da un sistema specifico.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-386">A session spans a period of time from logon until logoff from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-387">**Status**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-388">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-389">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-390">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-390">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-391">Questa proprietà non viene implementata e non viene popolata per nessuna istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-391">This property is not implemented and does not get populated for any instance of this class.</span></span> <span data-ttu-id="ceb4c-392">È sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-392">It is always **NULL**.</span></span>

<span data-ttu-id="ceb4c-393">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-393">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ceb4c-394">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ceb4c-394">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ceb4c-395">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-395">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ceb4c-396">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-396">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ceb4c-397">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="ceb4c-397">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ceb4c-398">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-398">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ceb4c-399">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-399">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ceb4c-400">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-400">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ceb4c-401">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-401">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ceb4c-402">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-402">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ceb4c-403">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-403">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ceb4c-404">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-404">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ceb4c-405">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-405">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ceb4c-406">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-406">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ceb4c-407">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-407">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-408">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-408">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-410">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("data di terminazione")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-410">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-411">Il processo è stato interrotto o terminato.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-411">Process was stopped or terminated.</span></span> <span data-ttu-id="ceb4c-412">Per ottenere il tempo di chiusura, è necessario che venga mantenuto aperto un handle per il processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-412">To get the termination time, a handle to the process must be held open.</span></span> <span data-ttu-id="ceb4c-413">In caso contrario, la proprietà restituirà **null**.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-413">Otherwise, this property returns **NULL**.</span></span>

<span data-ttu-id="ceb4c-414">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-414">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-415">**ThreadCount**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-415">**ThreadCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-416">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-417">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-418">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("conteggio thread")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-418">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Thread Count")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-419">Numero di thread attivi in un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-419">Number of active threads in a process.</span></span> <span data-ttu-id="ceb4c-420">Un'istruzione è l'unità di base di esecuzione in un processore e un thread è l'oggetto che esegue un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-420">An instruction is the basic unit of execution in a processor, and a thread is the object that executes an instruction.</span></span> <span data-ttu-id="ceb4c-421">Ogni processo in esecuzione ha almeno un thread.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-421">Each running process has at least one thread.</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-422">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-422">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-423">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-423">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-424">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-425">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**unità**](../wmisdk/standard-qualifiers.md) ("100 nanosecondi")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-425">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-426">Tempo in modalità utente, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-426">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="ceb4c-427">Se queste informazioni non sono disponibili, usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-427">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="ceb4c-428">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-428">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-429">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-429">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-430">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-431">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-432">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("utilizzo spazio indirizzi virtuali"), [**unità**](../wmisdk/standard-qualifiers.md) ("byte")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-432">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Virtual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-433">Dimensioni correnti dello spazio degli indirizzi virtuali usato da un processo, non della memoria fisica o virtuale effettivamente utilizzata dal processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-433">Current size of the virtual address space that a process is using, not the physical or virtual memory actually used by the process.</span></span> <span data-ttu-id="ceb4c-434">L'utilizzo dello spazio degli indirizzi virtuali non implica necessariamente l'utilizzo corrispondente di pagine del disco o della memoria principale.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-434">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="ceb4c-435">Lo spazio virtuale è finito e, usando un numero eccessivo di operazioni, il processo potrebbe non essere in grado di caricare le librerie.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-435">Virtual space is finite, and by using too much, the process might not be able to load libraries.</span></span> <span data-ttu-id="ceb4c-436">Questo valore è coerente con quello visualizzato in Perfmon.exe.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-436">This value is consistent with what you see in Perfmon.exe.</span></span>

<span data-ttu-id="ceb4c-437">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-437">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-438">**WindowsVersion**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-438">**WindowsVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-439">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-441">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and thread Functions \| GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("versione di Windows")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Windows Version")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-442">Versione di Windows in cui è in esecuzione il processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-442">Version of Windows in which the process is running.</span></span>

<span data-ttu-id="ceb4c-443">Esempio: 4,0</span><span class="sxs-lookup"><span data-stu-id="ceb4c-443">Example: 4.0</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-444">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-444">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-445">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-447">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("working set size"), [**unità**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-447">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-448">Quantità di memoria in byte che un processo deve eseguire in modo efficiente, per un sistema operativo che utilizza la gestione della memoria basata su pagine.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-448">Amount of memory in bytes that a process needs to execute efficiently—for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="ceb4c-449">Se il sistema non dispone di memoria sufficiente (inferiore alla dimensione working set), si verifica il thrashing.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-449">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="ceb4c-450">Se la dimensione dell'working set non è nota, utilizzare **null** o 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-450">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="ceb4c-451">Se vengono forniti working set dati, è possibile monitorare le informazioni per comprendere i requisiti di memoria modificabili di un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-451">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="ceb4c-452">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-452">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="ceb4c-453">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-453">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-454">**WriteOperationCount**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-454">**WriteOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-455">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-455">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-456">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-456">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-457">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("write operation count")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-457">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-458">Numero di operazioni di scrittura eseguite.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-458">Number of write operations performed.</span></span>

<span data-ttu-id="ceb4c-459">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-459">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb4c-460">**WriteTransferCount**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-460">**WriteTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb4c-461">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-462">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb4c-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb4c-463">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="ceb4c-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ceb4c-464">Quantità di dati scritti.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-464">Amount of data written.</span></span>

<span data-ttu-id="ceb4c-465">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-465">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ceb4c-466">Commenti</span><span class="sxs-lookup"><span data-stu-id="ceb4c-466">Remarks</span></span>

<span data-ttu-id="ceb4c-467">La classe di **\_ processo Win32** è derivata [**dal \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-467">The **Win32\_Process** class is derived from [**CIM\_Process**](cim-process.md).</span></span> <span data-ttu-id="ceb4c-468">Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-468">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="ceb4c-469">Per altre informazioni, vedere [esecuzione di operazioni con privilegi](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-469">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

### <a name="overview"></a><span data-ttu-id="ceb4c-470">Panoramica</span><span class="sxs-lookup"><span data-stu-id="ceb4c-470">Overview</span></span>

<span data-ttu-id="ceb4c-471">I processi sono sottostanti quasi tutto ciò che accade in un computer.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-471">Processes underlie almost everything that happens on a computer.</span></span> <span data-ttu-id="ceb4c-472">Infatti, la causa principale della maggior parte dei problemi del computer può essere tracciata ai processi; è possibile, ad esempio, che un numero eccessivo di processi sia in esecuzione in un computer (e che contenda un set limitato di risorse) oppure che un singolo processo stia usando più della relativa condivisione di risorse.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-472">In fact, the root cause of most computer problems can be traced to processes; for example, too many processes might be running on a computer (and contending for a finite set of resources), or a single process might be using more than its share of resources.</span></span> <span data-ttu-id="ceb4c-473">Questi fattori rendono importante tenere sotto controllo i processi in esecuzione in un computer.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-473">These factors make it important to keep a close watch on the processes running on a computer.</span></span> <span data-ttu-id="ceb4c-474">Il monitoraggio dei processi, l'attività principale nella gestione dei processi, consente di determinare le operazioni effettivamente eseguite da un computer, le applicazioni eseguite dal computer e il modo in cui tali applicazioni sono interessate dalle modifiche apportate all'ambiente informatico.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-474">Process monitoring, the main activity in process management, allows you to determine what a computer actually does, what applications the computer runs, and how those applications are affected by changes in the computing environment.</span></span>

### <a name="monitoring-a-process"></a><span data-ttu-id="ceb4c-475">Monitoraggio di un processo</span><span class="sxs-lookup"><span data-stu-id="ceb4c-475">Monitoring a Process</span></span>

<span data-ttu-id="ceb4c-476">Il monitoraggio dei processi a intervalli regolari consente di garantire che un computer venga eseguito a picco di efficienza e che esegua le attività designate come previsto.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-476">Monitoring processes on a regular basis helps you ensure that a computer runs at peak efficiency and that it carries out its appointed tasks as expected.</span></span> <span data-ttu-id="ceb4c-477">Tramite il monitoraggio dei processi, ad esempio, è possibile ricevere notifiche immediate di qualsiasi applicazione che ha smesso di rispondere e quindi eseguire le operazioni necessarie per terminare il processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-477">For example, by monitoring processes you can be notified immediately of any application that has stopped responding, and then take steps to end that process.</span></span> <span data-ttu-id="ceb4c-478">Inoltre, il monitoraggio dei processi consente di identificare i problemi prima che si verifichino.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-478">In addition, process monitoring enables you to identify problems before they occur.</span></span> <span data-ttu-id="ceb4c-479">Ad esempio, controllando ripetutamente la quantità di memoria usata da un processo, è possibile identificare una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-479">For example, by repeatedly checking the amount of memory used by a process, you can identify a memory leak.</span></span> <span data-ttu-id="ceb4c-480">È quindi possibile arrestare il processo prima che l'applicazione errata utilizzi tutta la memoria disponibile e riporti un arresto del computer.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-480">You can then stop the process before the errant application uses all of the available memory and brings the computer to a halt.</span></span>

<span data-ttu-id="ceb4c-481">Il monitoraggio dei processi consente inoltre di ridurre al minimo le interruzioni dovute a interruzioni pianificate per aggiornamenti e manutenzione.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-481">Process monitoring also helps minimize the disruptions caused by planned outages for upgrades and maintenance.</span></span> <span data-ttu-id="ceb4c-482">Se ad esempio si controlla lo stato di un'applicazione di database in esecuzione nei computer client, è possibile determinare l'effetto della disconnessione del database per l'aggiornamento del software.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-482">For example, by checking the status of a database application running on client computers, you can determine the impact of taking the database offline in order to upgrade the software.</span></span>

<span data-ttu-id="ceb4c-483">Monitoraggio della disponibilità del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-483">Monitoring process availability.</span></span> <span data-ttu-id="ceb4c-484">Misura la percentuale di tempo disponibile per un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-484">Measures the percentage of time that a process is available.</span></span> <span data-ttu-id="ceb4c-485">La disponibilità viene in genere monitorata usando un probe semplice, che indica se il processo è ancora in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-485">Availability is typically monitored by use of a simple probe, which reports whether the process is still running.</span></span> <span data-ttu-id="ceb4c-486">Tenendo traccia dei risultati di ogni Probe, è possibile calcolare la disponibilità del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-486">By keeping track of the results of each probe, you can calculate the availability of the process.</span></span> <span data-ttu-id="ceb4c-487">Ad esempio, un processo con Probe 100 volte e risponde in 95 di tali occasioni ha una disponibilità pari al 95%.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-487">For example, a process that is probed 100 times and responds on 95 of those occasions has an availability of 95 percent.</span></span> <span data-ttu-id="ceb4c-488">Questo tipo di monitoraggio è in genere riservato per database, programmi di posta elettronica e altre applicazioni che dovrebbero essere eseguite in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-488">This type of monitoring is typically reserved for databases, mail programs, and other applications that are expected to run at all times.</span></span> <span data-ttu-id="ceb4c-489">Non è appropriato per i programmi di elaborazione testi, i fogli di calcolo o altre applicazioni che vengono regolarmente avviate e arrestate più volte al giorno.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-489">It is not appropriate for word processing programs, spreadsheets, or other applications that are routinely started and stopped several times a day.</span></span>

<span data-ttu-id="ceb4c-490">Per configurare il processo, è possibile creare un'istanza della classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="ceb4c-490">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process.</span></span>

<span data-ttu-id="ceb4c-491">È possibile monitorare le prestazioni del processo con la classe di [**\_ \_ \_ processo Win32 PerfFormattedData PerfProc**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) e un oggetto di aggiornamento WMI, ad esempio [**SWbemRefresher**](../wmisdk/swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-491">You can monitor process performance with the [**Win32\_PerfFormattedData\_PerfProc\_Process**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) class and a WMI refresher object, such as [**SWbemRefresher**](../wmisdk/swbemrefresher.md).</span></span> <span data-ttu-id="ceb4c-492">Per ulteriori informazioni, vedere [monitoraggio dei dati sulle prestazioni](../wmisdk/monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4c-492">For more information, see [Monitoring Performance Data](../wmisdk/monitoring-performance-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ceb4c-493">Esempio</span><span class="sxs-lookup"><span data-stu-id="ceb4c-493">Examples</span></span>

<span data-ttu-id="ceb4c-494">L' [elenco delle proprietà delle classi WMI esempio di](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) codice PowerShell nella raccolta TechNet descrive la classe di **\_ processo Win32** e restituisce i risultati in formato Excel.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-494">The [List the Properties of WMI Classes](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) PowerShell code sample on TechNet Gallery describes the **Win32\_Process** class, and outputs the results in Excel format.</span></span>

<span data-ttu-id="ceb4c-495">Il [processo termina in esecuzione su più server](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) termina un processo in esecuzione in uno o più computer.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-495">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="ceb4c-496">Nell'argomento [esempio: chiamata a un metodo del provider](../wmisdk/example--calling-a-provider-method.md) , il codice USA C++ per chiamare il **\_ processo Win32** per creare un processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-496">In the [Example: Calling a Provider Method](../wmisdk/example--calling-a-provider-method.md) topic, the code uses C++ to call **Win32\_Process** to create a process.</span></span>

<span data-ttu-id="ceb4c-497">La disponibilità è la forma più semplice di monitoraggio dei processi: con questo approccio è sufficiente assicurarsi che il processo sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-497">Availability is the simplest form of process monitoring: with this approach, you simply ensure that the process is running.</span></span> <span data-ttu-id="ceb4c-498">Quando si monitora la disponibilità dei processi, in genere si recupera un elenco di processi in esecuzione in un computer e quindi si verifica che un determinato processo sia ancora attivo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-498">When you monitor for process availability, you typically retrieve a list of processes running on a computer and then verify that a particular process is still active.</span></span> <span data-ttu-id="ceb4c-499">Se il processo è attivo, viene considerato disponibile.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-499">If the process is active, it is considered available.</span></span> <span data-ttu-id="ceb4c-500">Se il processo non è attivo, non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-500">If the process is not active, it is not available.</span></span> <span data-ttu-id="ceb4c-501">Nell'esempio VBScript seguente viene monitorata la disponibilità del processo controllando l'elenco dei processi in esecuzione in un computer e inviando una notifica se il processo di Database.exe non viene trovato.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-501">The following VBScript sample monitors process availability by checking the list of processes running on a computer and issuing a notification if the Database.exe process is not found.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



<span data-ttu-id="ceb4c-502">Nell'esempio VBScript seguente viene monitorata la creazione di processi utilizzando un consumer di eventi temporaneo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-502">The following VBScript sample monitors process creation using a temporary event consumer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



<span data-ttu-id="ceb4c-503">Il codice VBScript seguente monitora le informazioni sulle prestazioni del processo.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-503">The following VBScript monitors process performance information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



<span data-ttu-id="ceb4c-504">Nell'esempio di codice VBScript riportato di seguito viene illustrato come ottenere il proprietario di ogni processo in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-504">The following VBScript code example shows how to obtain the owner of each process on a local computer.</span></span> <span data-ttu-id="ceb4c-505">È possibile utilizzare questo script per ottenere i dati da un computer remoto, ad esempio, per determinare quali utenti dispongono di processi che eseguono Terminal Server, sostituire il nome del computer remoto con "." nella prima riga.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-505">You can use this script to obtain data from a remote computer, for example, to determine which users have processes running terminal server, substitute the name of the remote computer for "." in the first line.</span></span> <span data-ttu-id="ceb4c-506">È anche necessario essere un amministratore nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-506">You must also be an administrator on the remote machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



<span data-ttu-id="ceb4c-507">Nell'esempio di codice VBScript riportato di seguito viene illustrato come ottenere la sessione di accesso associata a un processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-507">The following VBScript code example shows how to obtain the logon session associated with a running process.</span></span> <span data-ttu-id="ceb4c-508">Un processo deve essere in esecuzione Notepad.exe prima dell'avvio dello script.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-508">A process must be running Notepad.exe before the script starts.</span></span> <span data-ttu-id="ceb4c-509">Nell'esempio vengono individuate le istanze [**di \_ LogonSession Win32**](win32-logonsession.md) associate al **\_ processo Win32** che rappresenta Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-509">The example locates the instances of [**Win32\_LogonSession**](win32-logonsession.md) associated with the **Win32\_Process** that represents Notepad.exe.</span></span> <span data-ttu-id="ceb4c-510">[**Win32 \_ SessionProcess**](win32-sessionprocess.md) viene specificato come classe Association.</span><span class="sxs-lookup"><span data-stu-id="ceb4c-510">[**Win32\_SessionProcess**](win32-sessionprocess.md) is specified as the association class.</span></span> <span data-ttu-id="ceb4c-511">Per ulteriori informazioni, vedere [ASSOCIATORS of Statement.](../wmisdk/associators-of-statement.md)</span><span class="sxs-lookup"><span data-stu-id="ceb4c-511">For more information, see [ASSOCIATORS OF Statement.](../wmisdk/associators-of-statement.md).</span></span>


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
```



## <a name="requirements"></a><span data-ttu-id="ceb4c-512">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ceb4c-512">Requirements</span></span>



| <span data-ttu-id="ceb4c-513">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceb4c-513">Requirement</span></span> | <span data-ttu-id="ceb4c-514">Valore</span><span class="sxs-lookup"><span data-stu-id="ceb4c-514">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb4c-515">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ceb4c-515">Minimum supported client</span></span><br/> | <span data-ttu-id="ceb4c-516">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ceb4c-516">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ceb4c-517">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ceb4c-517">Minimum supported server</span></span><br/> | <span data-ttu-id="ceb4c-518">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ceb4c-518">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ceb4c-519">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ceb4c-519">Namespace</span></span><br/>                | <span data-ttu-id="ceb4c-520">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ceb4c-520">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ceb4c-521">MOF</span><span class="sxs-lookup"><span data-stu-id="ceb4c-521">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ceb4c-522"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ceb4c-522"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ceb4c-523">DLL</span><span class="sxs-lookup"><span data-stu-id="ceb4c-523">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ceb4c-524"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ceb4c-524"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceb4c-525">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ceb4c-525">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb4c-526">**\_Processo CIM**</span><span class="sxs-lookup"><span data-stu-id="ceb4c-526">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dt>

[<span data-ttu-id="ceb4c-527">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ceb4c-527">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="ceb4c-528">Attività WMI: processi</span><span class="sxs-lookup"><span data-stu-id="ceb4c-528">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
