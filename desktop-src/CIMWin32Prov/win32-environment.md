---
description: Rappresenta un ambiente o un'impostazione dell'ambiente di sistema in un computer Windows.
ms.assetid: da7ee891-c759-4046-a9d8-d3caf66ab5a9
ms.tgt_platform: multiple
title: Classe Win32_Environment
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Environment
- Win32_Environment.Caption
- Win32_Environment.Description
- Win32_Environment.InstallDate
- Win32_Environment.Status
- Win32_Environment.Name
- Win32_Environment.SystemVariable
- Win32_Environment.UserName
- Win32_Environment.VariableValue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b7267e3ac03c14cfc6ad6ca73ede42cc8478b41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878358"
---
# <a name="win32_environment-class"></a><span data-ttu-id="8b090-103">\_Classe ambiente Win32</span><span class="sxs-lookup"><span data-stu-id="8b090-103">Win32\_Environment class</span></span>

<span data-ttu-id="8b090-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ dell'ambiente Win32** rappresenta un ambiente o un'impostazione dell'ambiente di sistema in un computer Windows.</span><span class="sxs-lookup"><span data-stu-id="8b090-104">The **Win32\_Environment** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an environment or system environment setting on a Windows computer system.</span></span> <span data-ttu-id="8b090-105">L'esecuzione di query su questa classe restituisce le variabili di ambiente disponibili in:</span><span class="sxs-lookup"><span data-stu-id="8b090-105">Querying this class returns environment variables found in:</span></span>

<span data-ttu-id="8b090-106">**HKEY \_ Ambiente \_ del** \\ **sistema** di \\  \\ **controllo** CurrentControlSet \\  \\  del sistema del computer locale sessionmanager</span><span class="sxs-lookup"><span data-stu-id="8b090-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="8b090-107">e</span><span class="sxs-lookup"><span data-stu-id="8b090-107">and</span></span>

<span data-ttu-id="8b090-108">**HKEY \_** \\ Ambiente **< utente >** utenti \\ </span><span class="sxs-lookup"><span data-stu-id="8b090-108">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="8b090-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8b090-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8b090-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="8b090-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b090-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b090-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4D2-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_Environment : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  boolean  SystemVariable;
  string   UserName;
  string   VariableValue;
};
```

## <a name="members"></a><span data-ttu-id="8b090-112">Members</span><span class="sxs-lookup"><span data-stu-id="8b090-112">Members</span></span>

<span data-ttu-id="8b090-113">La classe di **\_ ambiente Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8b090-113">The **Win32\_Environment** class has these types of members:</span></span>

-   [<span data-ttu-id="8b090-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8b090-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b090-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8b090-115">Properties</span></span>

<span data-ttu-id="8b090-116">La classe dell' **\_ ambiente Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8b090-116">The **Win32\_Environment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b090-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="8b090-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b090-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8b090-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b090-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8b090-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b090-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8b090-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8b090-121">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8b090-121">A short textual description of the object.</span></span>

<span data-ttu-id="8b090-122">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8b090-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b090-123">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8b090-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b090-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8b090-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b090-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8b090-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b090-126">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8b090-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8b090-127">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8b090-127">A textual description of the object.</span></span>

<span data-ttu-id="8b090-128">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8b090-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b090-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8b090-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b090-130">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b090-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b090-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8b090-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b090-132">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="8b090-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8b090-133">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="8b090-133">Indicates when the object was installed.</span></span> <span data-ttu-id="8b090-134">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="8b090-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8b090-135">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8b090-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b090-136">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8b090-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b090-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8b090-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b090-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8b090-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b090-139">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="8b090-139">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="8b090-140">Stringa di caratteri che specifica il nome di una variabile di ambiente basata su Windows.</span><span class="sxs-lookup"><span data-stu-id="8b090-140">Character string that specifies the name of a Windows-based environment variable.</span></span> <span data-ttu-id="8b090-141">Specificando il nome di una variabile che non esiste ancora, un'applicazione crea una nuova variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="8b090-141">By specifying the name of a variable that does not yet exist, an application creates a new environment variable.</span></span>

<span data-ttu-id="8b090-142">Esempio: "Path"</span><span class="sxs-lookup"><span data-stu-id="8b090-142">Example: "Path"</span></span>

</dd> <dt>

<span data-ttu-id="8b090-143">**Status**</span><span class="sxs-lookup"><span data-stu-id="8b090-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b090-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8b090-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b090-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8b090-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b090-146">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="8b090-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8b090-147">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8b090-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="8b090-148">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="8b090-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8b090-149">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="8b090-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8b090-150">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="8b090-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8b090-151">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="8b090-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8b090-152">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="8b090-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8b090-153">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="8b090-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8b090-154">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8b090-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8b090-155">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8b090-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8b090-156">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8b090-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8b090-157">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="8b090-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8b090-158">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="8b090-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8b090-159">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="8b090-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8b090-160">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="8b090-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8b090-161">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="8b090-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8b090-162">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="8b090-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8b090-163">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="8b090-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8b090-164">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="8b090-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8b090-165">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="8b090-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8b090-166">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="8b090-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8b090-167">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="8b090-167">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8b090-168">**SystemVariable**</span><span class="sxs-lookup"><span data-stu-id="8b090-168">**SystemVariable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b090-169">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8b090-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b090-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8b090-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b090-171">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="8b090-171">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="8b090-172">Indica se la variabile è una variabile di sistema.</span><span class="sxs-lookup"><span data-stu-id="8b090-172">Indicates whether the variable is a system variable.</span></span> <span data-ttu-id="8b090-173">Una variabile di sistema viene impostata dal sistema operativo ed è indipendente dalle impostazioni dell'ambiente utente.</span><span class="sxs-lookup"><span data-stu-id="8b090-173">A system variable is set by the operating system, and is independent from user environment settings.</span></span>

</dd> <dt>

<span data-ttu-id="8b090-174">**UserName**</span><span class="sxs-lookup"><span data-stu-id="8b090-174">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b090-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8b090-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b090-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8b090-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b090-177">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="8b090-177">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="8b090-178">Nome del proprietario dell'impostazione dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="8b090-178">Name of the owner of the environment setting.</span></span> <span data-ttu-id="8b090-179">Viene impostato su <SYSTEM> per le impostazioni specifiche del sistema basato su Windows (in contrapposizione a un utente specifico) e <DEFAULT> per le impostazioni utente predefinite.</span><span class="sxs-lookup"><span data-stu-id="8b090-179">It is set to <SYSTEM> for settings that are specific to the Windows-based system (as opposed to a specific user) and <DEFAULT> for default user settings.</span></span>

<span data-ttu-id="8b090-180">Esempio: "JSmith"</span><span class="sxs-lookup"><span data-stu-id="8b090-180">Example: "JSmith"</span></span>

</dd> <dt>

<span data-ttu-id="8b090-181">**VariableValue**</span><span class="sxs-lookup"><span data-stu-id="8b090-181">**VariableValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b090-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8b090-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b090-183">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8b090-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b090-184">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="8b090-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="8b090-185">Variabile segnaposto di una variabile di ambiente basata su Windows.</span><span class="sxs-lookup"><span data-stu-id="8b090-185">Placeholder variable of a Windows-based environment variable.</span></span> <span data-ttu-id="8b090-186">Informazioni come la directory file system possono variare da computer a computer.</span><span class="sxs-lookup"><span data-stu-id="8b090-186">Information like the file system directory can change from computer to computer.</span></span> <span data-ttu-id="8b090-187">Il sistema operativo sostituisce i segnaposto per questi.</span><span class="sxs-lookup"><span data-stu-id="8b090-187">The operating system substitutes placeholders for these.</span></span>

<span data-ttu-id="8b090-188">Esempio: "% SystemRoot%"</span><span class="sxs-lookup"><span data-stu-id="8b090-188">Example: "%SystemRoot%"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b090-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b090-189">Remarks</span></span>

<span data-ttu-id="8b090-190">La classe di **\_ ambiente Win32** è derivata da [**CIM \_ SystemResource**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="8b090-190">The **Win32\_Environment** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span> <span data-ttu-id="8b090-191">È possibile usare questa classe per trovare i percorsi di cartelle speciali, ad esempio la cartella di sistema o i file di programma in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="8b090-191">You can use this class to find the paths of special folders such as the System folder or Program files on a remote machine.</span></span> <span data-ttu-id="8b090-192">Di seguito sono riportati alcuni esempi: windir, SystemRoot, ProgramFiles e UserProfile.</span><span class="sxs-lookup"><span data-stu-id="8b090-192">Some examples are: windir, systemroot, programfiles, and userprofile.</span></span> <span data-ttu-id="8b090-193">**Win32 \_ L'ambiente** restituisce sostanzialmente le informazioni disponibili in:</span><span class="sxs-lookup"><span data-stu-id="8b090-193">**Win32\_Environment** basically returns what can be found in:</span></span>

<span data-ttu-id="8b090-194">**HKEY \_ Ambiente \_ del** \\ **sistema** di \\  \\ **controllo** CurrentControlSet \\  \\  del sistema del computer locale sessionmanager</span><span class="sxs-lookup"><span data-stu-id="8b090-194">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="8b090-195">e</span><span class="sxs-lookup"><span data-stu-id="8b090-195">and</span></span>

<span data-ttu-id="8b090-196">**HKEY \_** \\ Ambiente **< utente >** utenti \\ </span><span class="sxs-lookup"><span data-stu-id="8b090-196">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="8b090-197">Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8b090-197">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="8b090-198">Se ad esempio si enumera questa classe nel computer locale, l'account con cui viene eseguita l'applicazione deve disporre di questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="8b090-198">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="8b090-199">Per altre informazioni, vedere [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="8b090-199">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="8b090-200">Esempio</span><span class="sxs-lookup"><span data-stu-id="8b090-200">Examples</span></span>

<span data-ttu-id="8b090-201">Nell'esempio [relativo all'elenco delle variabili di ambiente in un computer](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl viene utilizzato WMI per restituire informazioni su tutte le variabili di ambiente in un computer.</span><span class="sxs-lookup"><span data-stu-id="8b090-201">The [List Environment Variables on a Computer](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl sample uses WMI to return information about all the environment variables on a computer.</span></span>

<span data-ttu-id="8b090-202">Nell'esempio di codice VBScript riportato di seguito vengono enumerate le variabili di ambiente nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="8b090-202">The following VBScript code example enumerates the environment variables on the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colVar = objWMIService.ExecQuery("Select * from Win32_Environment")
For Each objVar in colVar
    Wscript.Echo "Description: " & objVar.Description & VBNewLine _
               & "Name: " & objVar.Name & VBNewLine _
               & "System Variable: " & objVar.SystemVariable & VBNewLine _
               & "User Name: " & objVar.UserName & VBNewLine _
               & "Variable Value: " & objVar.VariableValue 
Next
```



<span data-ttu-id="8b090-203">Nell'esempio di codice VBScript seguente viene modificata una variabile di ambiente denominata BUILD \_ Type in un valore di input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8b090-203">The following VBScript code example changes an environment variable named BUILD\_TYPE to a value input by the user.</span></span> <span data-ttu-id="8b090-204">Lo script presuppone che la variabile del tipo di compilazione \_ esista già.</span><span class="sxs-lookup"><span data-stu-id="8b090-204">The script assumes that the BUILD\_TYPE variable already exists.</span></span> <span data-ttu-id="8b090-205">Se non esiste, lo script termina.</span><span class="sxs-lookup"><span data-stu-id="8b090-205">If it does not exist then the script ends.</span></span> <span data-ttu-id="8b090-206">Il valore di input è selezionato: deve essere "Build1", "Build2" o "build3" e non viene accettato alcun altro valore.</span><span class="sxs-lookup"><span data-stu-id="8b090-206">The input value is checked: it must be either "Build1", "Build2", or "Build3", and no other value is accepted.</span></span> <span data-ttu-id="8b090-207">La funzione [UCase](https://msdn.microsoft.com/library/aa902519.aspx) di VBScript rende l'input senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8b090-207">The VBScript [UCase](https://msdn.microsoft.com/library/aa902519.aspx) function makes the input case-insensitive.</span></span> <span data-ttu-id="8b090-208">Se ciò che è digitato non è uno dei tre valori accettabili, lo script termina.</span><span class="sxs-lookup"><span data-stu-id="8b090-208">If what is typed in is not one of the three acceptable values, the script ends.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_Environment")
Found = False
For Each objItem in colItems
    If objItem.Name = "BUILD_TYPE" Then
    Found = True
    Change = UCase(InputBox("BUILD_TYPE currently = " & objItem.VariableValue & VBNewLine _
                          & "Change options are Build1, Build2, Build3 "))
        If UCase(Change) = "BUILD1" OR Change = "BUILD2" OR Change = "BUILD3" Then
            objItem.VariableValue = Change
            objItem.Put_
        WScript.Echo "BUILD_TYPE changed to " & objItem.VariableValue
        Else 
        WScript.Echo "No input or unacceptable input." & " No change to BUILD_TYPE"
        End If
    End If
Next
If Found = False Then
    WScript.Echo "User-defined environment variable BUILD_TYPE not found."
End If
```



## <a name="requirements"></a><span data-ttu-id="8b090-209">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b090-209">Requirements</span></span>



| <span data-ttu-id="8b090-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b090-210">Requirement</span></span> | <span data-ttu-id="8b090-211">Valore</span><span class="sxs-lookup"><span data-stu-id="8b090-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b090-212">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b090-212">Minimum supported client</span></span><br/> | <span data-ttu-id="8b090-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b090-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b090-214">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b090-214">Minimum supported server</span></span><br/> | <span data-ttu-id="8b090-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b090-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b090-216">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8b090-216">Namespace</span></span><br/>                | <span data-ttu-id="8b090-217">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8b090-217">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8b090-218">MOF</span><span class="sxs-lookup"><span data-stu-id="8b090-218">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b090-219"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b090-219"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b090-220">DLL</span><span class="sxs-lookup"><span data-stu-id="8b090-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b090-221"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b090-221"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b090-222">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b090-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b090-223">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="8b090-223">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dt>

<span data-ttu-id="8b090-224">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b090-224">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

