---
description: La \_ classe WMI astratta Win32 ProcessStartup rappresenta la configurazione di avvio di un processo basato su Windows.
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Classe Win32_ProcessStartup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b0be949b106c1fa88b37e0c7764dbddb0546ded7
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334363"
---
# <a name="win32_processstartup-class"></a><span data-ttu-id="435c4-103">Win32 \_ ProcessStartup (classe)</span><span class="sxs-lookup"><span data-stu-id="435c4-103">Win32\_ProcessStartup class</span></span>

<span data-ttu-id="435c4-104">La [classe WMI](../wmisdk/retrieving-a-class.md) astratta **Win32 \_ ProcessStartup** rappresenta la configurazione di avvio di un processo basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="435c4-104">The **Win32\_ProcessStartup** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the startup configuration of a Windows-based process.</span></span> <span data-ttu-id="435c4-105">La classe viene definita come definizione del tipo di metodo, ovvero viene utilizzata solo per passare informazioni al metodo [**create**](create-method-in-class-win32-process.md) della classe del [**\_ processo Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="435c4-105">The class is defined as a method type definition, which means that it is only used for passing information to the [**Create**](create-method-in-class-win32-process.md) method of the [**Win32\_Process**](win32-process.md) class.</span></span>

<span data-ttu-id="435c4-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="435c4-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="435c4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="435c4-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a><span data-ttu-id="435c4-108">Members</span><span class="sxs-lookup"><span data-stu-id="435c4-108">Members</span></span>

<span data-ttu-id="435c4-109">La classe **Win32 \_ ProcessStartup** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="435c4-109">The **Win32\_ProcessStartup** class has these types of members:</span></span>

-   [<span data-ttu-id="435c4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="435c4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="435c4-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="435c4-111">Properties</span></span>

<span data-ttu-id="435c4-112">La classe **Win32 \_ ProcessStartup** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="435c4-112">The **Win32\_ProcessStartup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="435c4-113">**CreateFlags**</span><span class="sxs-lookup"><span data-stu-id="435c4-113">**CreateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="435c4-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-116">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and thread Functions \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags")</span><span class="sxs-lookup"><span data-stu-id="435c4-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)\|dwCreationFlags")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-117">Valori aggiuntivi che controllano la classe di priorità e la creazione del processo.</span><span class="sxs-lookup"><span data-stu-id="435c4-117">Additional values that control the priority class and the creation of the process.</span></span> <span data-ttu-id="435c4-118">È possibile specificare i valori di creazione seguenti in qualsiasi combinazione, ad eccezione di quanto indicato.</span><span class="sxs-lookup"><span data-stu-id="435c4-118">The following creation values can be specified in any combination, except as noted.</span></span>

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span data-ttu-id="435c4-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Esegui debug \_ Processo** (1)</span><span class="sxs-lookup"><span data-stu-id="435c4-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debug\_Process** (1)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-120">Se questo flag è impostato, il processo chiamante viene considerato come un debugger e viene eseguito il debug del nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="435c4-120">If this flag is set, the calling process is treated as a debugger, and the new process is being debugged.</span></span> <span data-ttu-id="435c4-121">Il sistema notifica al debugger tutti gli eventi di debug che si verificano nel processo di cui è in corso il debug.</span><span class="sxs-lookup"><span data-stu-id="435c4-121">The system notifies the debugger of all debug events that occur in the process being debugged.</span></span>

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span data-ttu-id="435c4-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Esegui debug \_ Solo \_ questo \_ processo** (2)</span><span class="sxs-lookup"><span data-stu-id="435c4-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debug\_Only\_This\_Process** (2)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-123">Se questo flag non è impostato ed è in corso il debug del processo chiamante, il nuovo processo diventa un altro processo di cui è in corso il debug.</span><span class="sxs-lookup"><span data-stu-id="435c4-123">If this flag is not set and the calling process is being debugged, the new process becomes another process being debugged.</span></span> <span data-ttu-id="435c4-124">Se il processo chiamante non è un processo di cui è in corso il debug, non si verificheranno azioni correlate al debug.</span><span class="sxs-lookup"><span data-stu-id="435c4-124">If the calling process is not a process of being debugged, no debugging-related actions occur.</span></span>

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span data-ttu-id="435c4-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Crea \_ Sospeso** (4)</span><span class="sxs-lookup"><span data-stu-id="435c4-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Create\_Suspended** (4)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-126">Il thread principale del nuovo processo viene creato in uno stato sospeso e non viene eseguito fino a quando non viene chiamato il metodo [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .</span><span class="sxs-lookup"><span data-stu-id="435c4-126">The primary thread of the new process is created in a suspended state and does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) method is called.</span></span>

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span data-ttu-id="435c4-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**\_ Scollegato Processo** (8)</span><span class="sxs-lookup"><span data-stu-id="435c4-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Detached\_Process** (8)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-128">Per i processi della console, il nuovo processo non ha accesso alla console del processo padre.</span><span class="sxs-lookup"><span data-stu-id="435c4-128">For console processes, the new process does not have access to the console of the parent process.</span></span> <span data-ttu-id="435c4-129">Non è possibile usare questo flag se è impostato il flag **Crea \_ nuova \_ console** .</span><span class="sxs-lookup"><span data-stu-id="435c4-129">This flag cannot be used if the **Create\_New\_Console** flag is set.</span></span>

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span data-ttu-id="435c4-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Crea \_ Nuova \_ console** (16)</span><span class="sxs-lookup"><span data-stu-id="435c4-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Create\_New\_Console** (16)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-131">Questo nuovo processo ha una nuova console, anziché ereditare la console padre.</span><span class="sxs-lookup"><span data-stu-id="435c4-131">This new process has a new console, instead of inheriting the parent console.</span></span> <span data-ttu-id="435c4-132">Questo flag non può essere utilizzato con il flag di **\_ processo scollegato** .</span><span class="sxs-lookup"><span data-stu-id="435c4-132">This flag cannot be used with the **Detached\_Process** flag.</span></span>

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span data-ttu-id="435c4-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Crea \_ Nuovo \_ \_ gruppo di processi** (512)</span><span class="sxs-lookup"><span data-stu-id="435c4-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Create\_New\_Process\_Group** (512)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-134">Questo nuovo processo è il processo radice di un nuovo gruppo di processi.</span><span class="sxs-lookup"><span data-stu-id="435c4-134">This new process is the root process of a new process group.</span></span> <span data-ttu-id="435c4-135">Il gruppo di processi include tutti i processi discendenti di questo processo radice.</span><span class="sxs-lookup"><span data-stu-id="435c4-135">The process group includes all of the processes that are descendants of this root process.</span></span> <span data-ttu-id="435c4-136">L'identificatore di processo del nuovo gruppo di processi è uguale all'identificatore di processo restituito nella proprietà **ProcessID** della classe del [**\_ processo Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="435c4-136">The process identifier of the new process group is the same as the process identifier that is returned in the **ProcessID** property of the [**Win32\_Process**](win32-process.md) class.</span></span> <span data-ttu-id="435c4-137">I gruppi di processi vengono usati dal metodo [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) per consentire l'invio di un segnale CTRL + C o Ctrl + Break a un gruppo di processi della console.</span><span class="sxs-lookup"><span data-stu-id="435c4-137">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable the sending of either a CTRL+C signal or a CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span data-ttu-id="435c4-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Crea \_ \_Ambiente Unicode** (1024)</span><span class="sxs-lookup"><span data-stu-id="435c4-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Create\_Unicode\_Environment** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-139">Le impostazioni dell'ambiente elencate nella proprietà **EnvironmentVariables** utilizzano caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="435c4-139">The environment settings listed in the **EnvironmentVariables** property use Unicode characters.</span></span> <span data-ttu-id="435c4-140">Se questo flag non è impostato, il blocco dell'ambiente usa caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="435c4-140">If this flag is not set, the environment block uses ANSI characters.</span></span>

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span data-ttu-id="435c4-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Crea \_ \_ \_ Modalità di errore predefinita** (67108864)</span><span class="sxs-lookup"><span data-stu-id="435c4-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Create\_Default\_Error\_Mode** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-142">Ai processi appena creati viene assegnata la modalità di errore predefinita del sistema del processo chiamante anziché ereditare la modalità di errore del processo padre.</span><span class="sxs-lookup"><span data-stu-id="435c4-142">Newly created processes are given the system default error mode of the calling process instead of inheriting the error mode of the parent process.</span></span> <span data-ttu-id="435c4-143">Questo flag è utile per le applicazioni shell multithreading eseguite con errori hardware disabilitati.</span><span class="sxs-lookup"><span data-stu-id="435c4-143">This flag is useful for multithreaded shell applications that run with hard errors disabled.</span></span>

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span data-ttu-id="435c4-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Crea \_ FUGA \_ dal \_ processo** (16777216)</span><span class="sxs-lookup"><span data-stu-id="435c4-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**CREATE\_BREAKAWAY\_FROM\_JOB** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-145">Utilizzato per evitare che il processo creato sia limitato dall'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="435c4-145">Used for the created process not to be limited by the job object.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="435c4-146">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="435c4-146">**EnvironmentVariables**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-147">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="435c4-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="435c4-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-149">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Current \_ User \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="435c4-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_CURRENT\_USER\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-150">Elenco delle impostazioni per la configurazione di un computer.</span><span class="sxs-lookup"><span data-stu-id="435c4-150">List of settings for the configuration of a computer.</span></span> <span data-ttu-id="435c4-151">Le variabili di ambiente specificano i percorsi di ricerca per i file, le directory per i file temporanei, le opzioni specifiche dell'applicazione e altre informazioni simili.</span><span class="sxs-lookup"><span data-stu-id="435c4-151">Environment variables specify search paths for files, directories for temporary files, application-specific options, and other similar information.</span></span> <span data-ttu-id="435c4-152">Il sistema mantiene un blocco di impostazioni di ambiente per ogni utente e uno per il computer.</span><span class="sxs-lookup"><span data-stu-id="435c4-152">The system maintains a block of environment settings for each user and one for the computer.</span></span> <span data-ttu-id="435c4-153">Il blocco dell'ambiente di sistema rappresenta le variabili di ambiente per tutti gli utenti di un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="435c4-153">The system environment block represents environment variables for all of the users of a specific computer.</span></span> <span data-ttu-id="435c4-154">Il blocco dell'ambiente di un utente rappresenta le variabili di ambiente gestite dal sistema per un utente specifico e include il set di variabili di ambiente di sistema.</span><span class="sxs-lookup"><span data-stu-id="435c4-154">A user's environment block represents the environment variables that the system maintains for a specific user, and includes the set of system environment variables.</span></span> <span data-ttu-id="435c4-155">Per impostazione predefinita, ogni processo riceve una copia del blocco di ambiente per il processo padre.</span><span class="sxs-lookup"><span data-stu-id="435c4-155">By default, each process receives a copy of the environment block for its parent process.</span></span> <span data-ttu-id="435c4-156">Si tratta in genere del blocco dell'ambiente per l'utente che ha eseguito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="435c4-156">Typically, this is the environment block for the user who is logged on.</span></span> <span data-ttu-id="435c4-157">Un processo può specificare blocchi di ambiente diversi per i processi figlio.</span><span class="sxs-lookup"><span data-stu-id="435c4-157">A process can specify different environment blocks for its child processes.</span></span>

</dd> <dt>

<span data-ttu-id="435c4-158">**ErrorMode**</span><span class="sxs-lookup"><span data-stu-id="435c4-158">**ErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-159">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="435c4-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-161">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Error Functions \| SetErrorMode")</span><span class="sxs-lookup"><span data-stu-id="435c4-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Error Functions\|SetErrorMode")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-162">In alcuni processori non x86, i riferimenti di memoria non allineati provocano un'eccezione di errore di allineamento.</span><span class="sxs-lookup"><span data-stu-id="435c4-162">On some non-x86 processors, misaligned memory references cause an alignment fault exception.</span></span> <span data-ttu-id="435c4-163">Il flag **nessun \_ errore di allineamento \_ \_ eccetto** consente di controllare se un sistema operativo corregge automaticamente tali errori di allineamento o li rende visibili a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="435c4-163">The **No\_Alignment\_Fault\_Except** flag lets you control whether or not an operating system automatically fixes such alignment faults, or makes them visible to an application.</span></span> <span data-ttu-id="435c4-164">In una piattaforma di milioni di istruzioni al secondo (MIPS), un'applicazione deve chiamare in modo esplicito [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) con il flag **nessun errore di \_ allineamento ad \_ \_ eccezione** che il sistema operativo corregge automaticamente gli errori di allineamento.</span><span class="sxs-lookup"><span data-stu-id="435c4-164">On a millions of instructions per second (MIPS) platform, an application must explicitly call [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) with the **No\_Alignment\_Fault\_Except** flag to have the operating system automatically fix alignment faults.</span></span>

<span data-ttu-id="435c4-165">Modalità di elaborazione di diversi tipi di errori gravi da un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="435c4-165">How an operating system processes several types of serious errors.</span></span> <span data-ttu-id="435c4-166">È possibile specificare che gli errori di elaborazione del sistema operativo o un'applicazione possono ricevere ed elaborare errori.</span><span class="sxs-lookup"><span data-stu-id="435c4-166">You can specify that the operating system process errors, or an application can receive and process errors.</span></span>

<span data-ttu-id="435c4-167">Per impostazione predefinita, il sistema operativo rende visibili gli errori di allineamento a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="435c4-167">The default setting is for the operating system to make alignment faults visible to an application.</span></span> <span data-ttu-id="435c4-168">Poiché la piattaforma x86 non rende visibili gli errori di allineamento a un'applicazione, il flag nessun errore di **\_ allineamento \_ \_ ad eccezione** di non consente al sistema operativo di generare un errore di allineamento, anche se il flag non è impostato.</span><span class="sxs-lookup"><span data-stu-id="435c4-168">Because the x86 platform does not make alignment faults visible to an application, the **No\_Alignment\_Fault\_Except** flag does not make the operating system raise an alignment fault error—even if the flag is not set.</span></span> <span data-ttu-id="435c4-169">Lo stato predefinito per [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) consiste nell'impostare tutti i flag su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="435c4-169">The default state for [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) is to set all of the flags to 0 (zero).</span></span>

<dt>



 <span data-ttu-id="435c4-170">(1)</span><span class="sxs-lookup"><span data-stu-id="435c4-170">(1)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-171">Predefinito</span><span class="sxs-lookup"><span data-stu-id="435c4-171">Default</span></span>

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span data-ttu-id="435c4-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Non riuscita \_ \_Errori critici** (2)</span><span class="sxs-lookup"><span data-stu-id="435c4-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Fail\_Critical\_Errors** (2)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-173">Se questo flag è impostato, il sistema operativo non visualizzerà la finestra di messaggio del gestore errori critico quando si verifica un errore di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="435c4-173">If this flag is set, the operating system does not display the critical error handler message box when such an error occurs.</span></span> <span data-ttu-id="435c4-174">Al contrario, il sistema operativo invia l'errore al processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="435c4-174">Instead, the operating system sends the error to the calling process.</span></span>

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span data-ttu-id="435c4-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No \_ Errore di allineamento \_ \_ eccetto** (4)</span><span class="sxs-lookup"><span data-stu-id="435c4-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No\_Alignment\_Fault\_Except** (4)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-176">Se questo flag è impostato, il sistema operativo corregge automaticamente gli errori di allineamento della memoria e li rende invisibile all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="435c4-176">If this flag is set, the operating system automatically fixes memory alignment faults and makes them invisible to the application.</span></span> <span data-ttu-id="435c4-177">Questa operazione viene eseguita per i processi chiamante e discendente.</span><span class="sxs-lookup"><span data-stu-id="435c4-177">It does this for the calling and descendant processes.</span></span> <span data-ttu-id="435c4-178">Questo flag è valido solo per RISC (Reduced Instruction Set Computing) e non ha alcun effetto sui processori x86.</span><span class="sxs-lookup"><span data-stu-id="435c4-178">This flag applies to reduced instruction set computing (RISC) only, and has no effect on x86 processors.</span></span>

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span data-ttu-id="435c4-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No \_ \_ \_ \_ Casella errore GP** (8)</span><span class="sxs-lookup"><span data-stu-id="435c4-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No\_GP\_Fault\_Error\_Box** (8)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-180">Se questo flag è impostato, nel sistema operativo non viene visualizzata la finestra di messaggio di errore di protezione generale (GP) quando si verifica un errore del GP.</span><span class="sxs-lookup"><span data-stu-id="435c4-180">If this flag is set, the operating system does not display the general protection (GP) fault message box when a GP error occurs.</span></span> <span data-ttu-id="435c4-181">Questo flag deve essere impostato solo tramite il debug di applicazioni che gestiscono gli errori di GP.</span><span class="sxs-lookup"><span data-stu-id="435c4-181">This flag should only be set by debugging applications that handle GP errors.</span></span>

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span data-ttu-id="435c4-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No \_ \_Casella di \_ errore \_ Apri file** (16)</span><span class="sxs-lookup"><span data-stu-id="435c4-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No\_Open\_File\_Error\_Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-183">Se questo flag è impostato, il sistema operativo non visualizza una finestra di messaggio quando non riesce a trovare un file.</span><span class="sxs-lookup"><span data-stu-id="435c4-183">If this flag is set, the operating system does not display a message box when it fails to find a file.</span></span> <span data-ttu-id="435c4-184">Al contrario, l'errore viene restituito al processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="435c4-184">Instead, the error is returned to the calling process.</span></span> <span data-ttu-id="435c4-185">Questo flag è attualmente ignorato.</span><span class="sxs-lookup"><span data-stu-id="435c4-185">This flag is currently ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="435c4-186">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="435c4-186">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-187">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="435c4-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-188">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-189">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute")</span><span class="sxs-lookup"><span data-stu-id="435c4-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwFillAttribute")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-190">Testo e colori di sfondo se viene creata una nuova finestra della console in un'applicazione console.</span><span class="sxs-lookup"><span data-stu-id="435c4-190">The text and background colors if a new console window is created in a console application.</span></span> <span data-ttu-id="435c4-191">Questi valori vengono ignorati nelle applicazioni GUI (Graphical User Interface).</span><span class="sxs-lookup"><span data-stu-id="435c4-191">These values are ignored in graphical user interface (GUI) applications.</span></span> <span data-ttu-id="435c4-192">Per specificare i colori di primo piano e di sfondo, aggiungere insieme i valori.</span><span class="sxs-lookup"><span data-stu-id="435c4-192">To specify both foreground and background colors, add the values together.</span></span> <span data-ttu-id="435c4-193">Ad esempio, per avere un tipo rosso (4) su uno sfondo blu (16), impostare FillAttribute su 20.</span><span class="sxs-lookup"><span data-stu-id="435c4-193">For example, to have red type (4) on a blue background (16), set the FillAttribute to 20.</span></span>

<dt>

<span data-ttu-id="435c4-194">1</span><span class="sxs-lookup"><span data-stu-id="435c4-194">1</span></span>
</dt> <dd>

<span data-ttu-id="435c4-195">Blu in primo piano \_</span><span class="sxs-lookup"><span data-stu-id="435c4-195">Foreground\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="435c4-196">2</span><span class="sxs-lookup"><span data-stu-id="435c4-196">2</span></span>
</dt> <dd>

<span data-ttu-id="435c4-197">Verde primo piano \_</span><span class="sxs-lookup"><span data-stu-id="435c4-197">Foreground\_Green</span></span>

</dd> <dt>

<span data-ttu-id="435c4-198">4</span><span class="sxs-lookup"><span data-stu-id="435c4-198">4</span></span>
</dt> <dd>

<span data-ttu-id="435c4-199">Rosso in primo piano \_</span><span class="sxs-lookup"><span data-stu-id="435c4-199">Foreground\_Red</span></span>

</dd> <dt>

<span data-ttu-id="435c4-200">8</span><span class="sxs-lookup"><span data-stu-id="435c4-200">8</span></span>
</dt> <dd>

<span data-ttu-id="435c4-201">Intensità in primo piano \_</span><span class="sxs-lookup"><span data-stu-id="435c4-201">Foreground\_Intensity</span></span>

</dd> <dt>

<span data-ttu-id="435c4-202">16</span><span class="sxs-lookup"><span data-stu-id="435c4-202">16</span></span>
</dt> <dd>

<span data-ttu-id="435c4-203">\_Blu sfondo</span><span class="sxs-lookup"><span data-stu-id="435c4-203">Background\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="435c4-204">32</span><span class="sxs-lookup"><span data-stu-id="435c4-204">32</span></span>
</dt> <dd>

<span data-ttu-id="435c4-205">\_Verde sfondo</span><span class="sxs-lookup"><span data-stu-id="435c4-205">Background\_Green</span></span>

</dd> <dt>

<span data-ttu-id="435c4-206">64</span><span class="sxs-lookup"><span data-stu-id="435c4-206">64</span></span>
</dt> <dd>

<span data-ttu-id="435c4-207">\_Rosso sfondo</span><span class="sxs-lookup"><span data-stu-id="435c4-207">Background\_Red</span></span>

</dd> <dt>

<span data-ttu-id="435c4-208">128</span><span class="sxs-lookup"><span data-stu-id="435c4-208">128</span></span>
</dt> <dd>

<span data-ttu-id="435c4-209">Intensità di sfondo \_</span><span class="sxs-lookup"><span data-stu-id="435c4-209">Background\_Intensity</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="435c4-210">**PriorityClass**</span><span class="sxs-lookup"><span data-stu-id="435c4-210">**PriorityClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-211">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="435c4-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-212">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-212">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-213">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture di thread \| [**JOBOBJECT \_ Basic \_ limit \_ Information**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass")</span><span class="sxs-lookup"><span data-stu-id="435c4-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information)\|PriorityClass")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-214">Classe di priorità del nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="435c4-214">Priority class of the new process.</span></span> <span data-ttu-id="435c4-215">Utilizzare questa proprietà per determinare le priorità di pianificazione dei thread nel processo.</span><span class="sxs-lookup"><span data-stu-id="435c4-215">Use this property to determine the schedule priorities of the threads in the process.</span></span> <span data-ttu-id="435c4-216">Se la proprietà è null, il valore predefinito della classe priority è Normal, a meno che la classe priority del processo di creazione non sia inattiva o inferiore al \_ normale.</span><span class="sxs-lookup"><span data-stu-id="435c4-216">If the property is left null, the priority class defaults to Normal—unless the priority class of the creating process is Idle or Below\_Normal.</span></span> <span data-ttu-id="435c4-217">In questi casi, il processo figlio riceve la classe di priorità predefinita del processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="435c4-217">In these cases, the child process receives the default priority class of the calling process.</span></span>

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="435c4-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** (32)</span><span class="sxs-lookup"><span data-stu-id="435c4-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-219">Indica un processo normale senza particolari esigenze di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="435c4-219">Indicates a normal process with no special schedule needs.</span></span>

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="435c4-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inattività** (64)</span><span class="sxs-lookup"><span data-stu-id="435c4-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-221">Indica un processo con thread eseguiti solo quando il sistema è inattivo e viene interrotto dai thread di qualsiasi processo in esecuzione in una classe con priorità più elevata.</span><span class="sxs-lookup"><span data-stu-id="435c4-221">Indicates a process with threads that run only when the system is idle and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="435c4-222">Un esempio è un screen saver.</span><span class="sxs-lookup"><span data-stu-id="435c4-222">An example is a screen saver.</span></span> <span data-ttu-id="435c4-223">La classe di priorità inattiva viene ereditata dai processi figlio.</span><span class="sxs-lookup"><span data-stu-id="435c4-223">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="435c4-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (128)</span><span class="sxs-lookup"><span data-stu-id="435c4-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (128)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-225">Indica un processo che esegue attività critiche al tempo che devono essere eseguite immediatamente per l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="435c4-225">Indicates a process that performs time-critical tasks that must be executed immediately to run correctly.</span></span> <span data-ttu-id="435c4-226">I thread di un processo di classe ad alta priorità hanno la precedenza sui thread dei processi di classe di priorità normale o di priorità di inattività.</span><span class="sxs-lookup"><span data-stu-id="435c4-226">The threads of a high-priority class process preempt the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="435c4-227">Un esempio è Windows Elenco attività, che deve rispondere rapidamente quando viene chiamato dall'utente, indipendentemente dal carico sul sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="435c4-227">An example is Windows Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="435c4-228">Prestare particolare attenzione quando si utilizza la classe con priorità alta, perché un'applicazione con associazione alla CPU con priorità alta può utilizzare quasi tutti i cicli disponibili.</span><span class="sxs-lookup"><span data-stu-id="435c4-228">Use extreme care when using the high-priority class, because a high-priority class CPU-bound application can use nearly all of the available cycles.</span></span> <span data-ttu-id="435c4-229">Solo una priorità in tempo reale precede i thread impostati su questo livello.</span><span class="sxs-lookup"><span data-stu-id="435c4-229">Only a real-time priority preempts threads set to this level.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="435c4-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tempo reale** (256)</span><span class="sxs-lookup"><span data-stu-id="435c4-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-231">Indica un processo con la massima priorità possibile.</span><span class="sxs-lookup"><span data-stu-id="435c4-231">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="435c4-232">I thread di un processo della classe di priorità in tempo reale hanno la precedenza sui thread di tutti gli altri processi, inclusi i thread con priorità alta e i processi del sistema operativo che eseguono attività importanti.</span><span class="sxs-lookup"><span data-stu-id="435c4-232">The threads of a real-time priority class process preempt the threads of all other processes—including high-priority threads and operating system processes performing important tasks.</span></span> <span data-ttu-id="435c4-233">Ad esempio, un processo in tempo reale eseguito per più di un intervallo molto breve può causare la mancata scaricamento delle cache del disco o la mancata risposta del mouse.</span><span class="sxs-lookup"><span data-stu-id="435c4-233">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush, or cause a mouse to be unresponsive.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="435c4-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>Di **seguito \_ Normale** (16384)</span><span class="sxs-lookup"><span data-stu-id="435c4-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below\_Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-235">Indica un processo con priorità maggiore di inattività ma inferiore al normale.</span><span class="sxs-lookup"><span data-stu-id="435c4-235">Indicates a process that has a priority higher than Idle but lower than Normal.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="435c4-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Sopra \_ Normale** (32768)</span><span class="sxs-lookup"><span data-stu-id="435c4-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above\_Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="435c4-237">Indica un processo con priorità superiore al normale ma inferiore al valore massimo.</span><span class="sxs-lookup"><span data-stu-id="435c4-237">Indicates a process that has a priority higher than Normal but lower than High.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="435c4-238">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="435c4-238">**ShowWindow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-239">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="435c4-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-240">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-240">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-241">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")</span><span class="sxs-lookup"><span data-stu-id="435c4-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|wShowWindow")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-242">Visualizzazione della finestra all'utente.</span><span class="sxs-lookup"><span data-stu-id="435c4-242">How the window is displayed to the user.</span></span> <span data-ttu-id="435c4-243">Può essere uno qualsiasi dei valori che possono essere specificati nel parametro *nCmdShow* per la funzione [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="435c4-243">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="435c4-244">**Title**</span><span class="sxs-lookup"><span data-stu-id="435c4-244">**Title**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-245">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="435c4-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-246">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-246">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-247">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle")</span><span class="sxs-lookup"><span data-stu-id="435c4-247">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpTitle")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-248">Testo visualizzato nella barra del titolo quando viene creata una nuova finestra della console. usato per i processi della console.</span><span class="sxs-lookup"><span data-stu-id="435c4-248">Text displayed in the title bar when a new console window is created; used for console processes.</span></span> <span data-ttu-id="435c4-249">Se **null**, il nome del file eseguibile viene usato come titolo della finestra.</span><span class="sxs-lookup"><span data-stu-id="435c4-249">If **NULL**, the name of the executable file is used as the window title.</span></span> <span data-ttu-id="435c4-250">Questa proprietà deve essere **null** per i processi GUI o console che non creano una nuova finestra della console.</span><span class="sxs-lookup"><span data-stu-id="435c4-250">This property must be **NULL** for GUI or console processes that do not create a new console window.</span></span>

</dd> <dt>

<span data-ttu-id="435c4-251">**WinstationDesktop**</span><span class="sxs-lookup"><span data-stu-id="435c4-251">**WinstationDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="435c4-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-253">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-253">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-254">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop")</span><span class="sxs-lookup"><span data-stu-id="435c4-254">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpDesktop")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-255">Nome del desktop o nome del desktop e della stazione della finestra per il processo.</span><span class="sxs-lookup"><span data-stu-id="435c4-255">The name of the desktop or the name of both the desktop and window station for the process.</span></span> <span data-ttu-id="435c4-256">Una barra rovesciata nella stringa indica che la stringa include i nomi delle stazioni desktop e di Windows.</span><span class="sxs-lookup"><span data-stu-id="435c4-256">A backslash in the string indicates that the string includes both desktop and window station names.</span></span> <span data-ttu-id="435c4-257">Se **WinstationDesktop** è **null**, il nuovo processo eredita il desktop e la stazione della finestra del processo padre.</span><span class="sxs-lookup"><span data-stu-id="435c4-257">If **WinstationDesktop** is **NULL**, the new process inherits the desktop and window station of its parent process.</span></span> <span data-ttu-id="435c4-258">Se **WinstationDesktop** è una stringa vuota, il processo non eredita il desktop e la stazione della finestra del processo padre.</span><span class="sxs-lookup"><span data-stu-id="435c4-258">If **WinstationDesktop** is an empty string, the process does not inherit the desktop and window station of its parent process.</span></span> <span data-ttu-id="435c4-259">Il sistema determina se è necessario creare un nuovo desktop e una nuova stazione di finestra.</span><span class="sxs-lookup"><span data-stu-id="435c4-259">The system determines if a new desktop and window station must be created.</span></span> <span data-ttu-id="435c4-260">Una finestra è un oggetto protetto che contiene gli appunti, un set di atomi globali e un gruppo di oggetti desktop.</span><span class="sxs-lookup"><span data-stu-id="435c4-260">A window station is a secure object that contains a clipboard, a set of global atoms, and a group of desktop objects.</span></span> <span data-ttu-id="435c4-261">La stazione interattiva della finestra assegnata alla sessione di accesso dell'utente interattivo contiene anche la tastiera, il mouse e il dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="435c4-261">The interactive window station that is assigned to the logon session of the interactive user also contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="435c4-262">Un desktop è un oggetto protetto contenuto all'interno di una finestra.</span><span class="sxs-lookup"><span data-stu-id="435c4-262">A desktop is a secure object contained within a window station.</span></span> <span data-ttu-id="435c4-263">Un desktop ha una superficie di visualizzazione logica e contiene finestre, menu e hook.</span><span class="sxs-lookup"><span data-stu-id="435c4-263">A desktop has a logical display surface and contains windows, menus, and hooks.</span></span> <span data-ttu-id="435c4-264">Una stazione della finestra può avere più desktop.</span><span class="sxs-lookup"><span data-stu-id="435c4-264">A window station can have multiple desktops.</span></span> <span data-ttu-id="435c4-265">Solo i desktop della stazione finestra interattiva possono essere visibili e ricevere l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="435c4-265">Only the desktops of the interactive window station can be visible and receive user input.</span></span>

</dd> <dt>

<span data-ttu-id="435c4-266">**X**</span><span class="sxs-lookup"><span data-stu-id="435c4-266">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-267">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="435c4-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-268">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-268">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-269">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwX")</span><span class="sxs-lookup"><span data-stu-id="435c4-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwX")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-270">Offset X dell'angolo superiore sinistro di una finestra se viene creata una nuova finestra, in pixel.</span><span class="sxs-lookup"><span data-stu-id="435c4-270">The X offset of the upper left corner of a window if a new window is created—in pixels.</span></span> <span data-ttu-id="435c4-271">Gli offset si trovano nell'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="435c4-271">The offsets are from the upper left corner of the screen.</span></span> <span data-ttu-id="435c4-272">Per i processi GUI, la posizione specificata viene usata la prima volta che il nuovo processo chiama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per creare una finestra sovrapposta se il parametro *X* di **CreateWindow** è **CW \_ usedefault (**.</span><span class="sxs-lookup"><span data-stu-id="435c4-272">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *X* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="435c4-273">\[! Nota X\]</span><span class="sxs-lookup"><span data-stu-id="435c4-273">\[!Note  X\]</span></span>  
> <span data-ttu-id="435c4-274">e **Y** non possono essere specificati in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="435c4-274">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="435c4-275">**XCountChars**</span><span class="sxs-lookup"><span data-stu-id="435c4-275">**XCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-276">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="435c4-276">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-277">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-277">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-278">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars")</span><span class="sxs-lookup"><span data-stu-id="435c4-278">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|XCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-279">Larghezza del buffer dello schermo nelle colonne di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="435c4-279">Screen buffer width in character columns.</span></span> <span data-ttu-id="435c4-280">Questa proprietà viene usata per i processi che creano una finestra della console e viene ignorata nei processi GUI.</span><span class="sxs-lookup"><span data-stu-id="435c4-280">This property is used for processes that create a console window, and is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="435c4-281">Non è possibile specificare **XCountChars** e **YCountChars** in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="435c4-281">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="435c4-282">**XSize**</span><span class="sxs-lookup"><span data-stu-id="435c4-282">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-283">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="435c4-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-284">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-284">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-285">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize")</span><span class="sxs-lookup"><span data-stu-id="435c4-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwXSize")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-286">Larghezza in pixel di una finestra se viene creata una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="435c4-286">Pixel width of a window if a new window is created.</span></span> <span data-ttu-id="435c4-287">Per i processi GUI, viene usato solo la prima volta che il nuovo processo chiama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per creare una finestra sovrapposta se il parametro NWidth di **CreateWindow** è **CW \_ usedefault (**.</span><span class="sxs-lookup"><span data-stu-id="435c4-287">For GUI processes, this is only used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the nWidth parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="435c4-288">Non è possibile specificare **XSize** e **ysize** in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="435c4-288">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="435c4-289">**S**</span><span class="sxs-lookup"><span data-stu-id="435c4-289">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-290">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="435c4-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-291">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-291">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-292">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| Dwy")</span><span class="sxs-lookup"><span data-stu-id="435c4-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwY")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-293">Offset in pixel dell'angolo superiore sinistro di una finestra se viene creata una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="435c4-293">Pixel offset of the upper-left corner of a window if a new window is created.</span></span> <span data-ttu-id="435c4-294">Gli offset sono dall'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="435c4-294">The offsets are from the upper-left corner of the screen.</span></span> <span data-ttu-id="435c4-295">Per i processi GUI, la posizione specificata viene usata la prima volta che il nuovo processo chiama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per creare una finestra sovrapposta se il parametro *y* di **CreateWindow** è **CW \_ usedefault (**.</span><span class="sxs-lookup"><span data-stu-id="435c4-295">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *y* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="435c4-296">\[! Nota X\]</span><span class="sxs-lookup"><span data-stu-id="435c4-296">\[!Note  X\]</span></span>  
> <span data-ttu-id="435c4-297">e **Y** non possono essere specificati in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="435c4-297">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="435c4-298">**YCountChars**</span><span class="sxs-lookup"><span data-stu-id="435c4-298">**YCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-299">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="435c4-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-300">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-301">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars")</span><span class="sxs-lookup"><span data-stu-id="435c4-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|YCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-302">Altezza buffer dello schermo in righe di caratteri.</span><span class="sxs-lookup"><span data-stu-id="435c4-302">Screen buffer height in character rows.</span></span> <span data-ttu-id="435c4-303">Questa proprietà viene usata per i processi che creano una finestra della console, ma viene ignorata nei processi GUI.</span><span class="sxs-lookup"><span data-stu-id="435c4-303">This property is used for processes that create a console window, but is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="435c4-304">Non è possibile specificare **XCountChars** e **YCountChars** in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="435c4-304">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="435c4-305">**YSize**</span><span class="sxs-lookup"><span data-stu-id="435c4-305">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="435c4-306">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="435c4-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="435c4-307">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="435c4-307">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="435c4-308">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize")</span><span class="sxs-lookup"><span data-stu-id="435c4-308">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwYSize")</span></span>
</dt> </dl>

<span data-ttu-id="435c4-309">Altezza in pixel di una finestra se viene creata una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="435c4-309">Pixel height of a window if a new window is created.</span></span> <span data-ttu-id="435c4-310">Per i processi GUI, viene usato solo la prima volta che il nuovo processo chiama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per creare una finestra sovrapposta se il parametro *nWidth* di **CreateWindow** è **CW \_ usedefault (**.</span><span class="sxs-lookup"><span data-stu-id="435c4-310">For GUI processes, this is used only the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *nWidth* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="435c4-311">Non è possibile specificare **XSize** e **ysize** in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="435c4-311">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="435c4-312">Commenti</span><span class="sxs-lookup"><span data-stu-id="435c4-312">Remarks</span></span>

<span data-ttu-id="435c4-313">Questa classe è derivata da [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md).</span><span class="sxs-lookup"><span data-stu-id="435c4-313">This class is derived from [**Win32\_MethodParameterClass**](win32-methodparameterclass.md).</span></span>

<span data-ttu-id="435c4-314">Panoramica</span><span class="sxs-lookup"><span data-stu-id="435c4-314">Overview</span></span>

<span data-ttu-id="435c4-315">Il metodo di [**creazione**](create-method-in-class-win32-process.md) [**\_ processo Win32**](win32-process.md) consente di configurare le opzioni di avvio per qualsiasi nuovo processo in esecuzione in un computer.</span><span class="sxs-lookup"><span data-stu-id="435c4-315">The [**Win32\_Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md) method enables you to configure startup options for any new process running on a computer.</span></span> <span data-ttu-id="435c4-316">Ad esempio, è possibile configurare un processo in modo che venga avviato in una finestra "nascosta", che impedisce a un utente di visualizzare e possibilmente interromperlo.</span><span class="sxs-lookup"><span data-stu-id="435c4-316">For example, you can configure a process so that it starts in a "hidden" window, which prevents a user from seeing, and possibly interrupting, it.</span></span> <span data-ttu-id="435c4-317">Se il processo viene eseguito in una finestra di comando, è possibile configurare le dimensioni, il titolo e i colori di primo piano e di sfondo della finestra.</span><span class="sxs-lookup"><span data-stu-id="435c4-317">If the process runs in a command window, you can configure the size, title, and foreground and background colors of the window.</span></span>

<span data-ttu-id="435c4-318">Le opzioni di avvio vengono configurate utilizzando la classe **Win32 \_ ProcessStartup** .</span><span class="sxs-lookup"><span data-stu-id="435c4-318">Startup options are configured using the **Win32\_ProcessStartup** class.</span></span> <span data-ttu-id="435c4-319">**Win32 \_ ProcessStartup** è una classe del tipo di metodo. la classe del tipo di metodo esiste esclusivamente per passare informazioni a un metodo.</span><span class="sxs-lookup"><span data-stu-id="435c4-319">**Win32\_ProcessStartup** is a Method Type class; the Method Type class exists solely to pass information to a method.</span></span> <span data-ttu-id="435c4-320">In questo caso, tutte le proprietà di un'istanza di **Win32 \_ ProcessStartup** vengono passate a un'istanza del [**\_ processo Win32**](win32-process.md).</span><span class="sxs-lookup"><span data-stu-id="435c4-320">In this case, all the properties of an instance of **Win32\_ProcessStartup** are passed to an instance of [**Win32\_Process**](win32-process.md).</span></span>

<span data-ttu-id="435c4-321">**Uso di Win32 \_ ProcessStartup**</span><span class="sxs-lookup"><span data-stu-id="435c4-321">**Using Win32\_ProcessStartup**</span></span>

1.  <span data-ttu-id="435c4-322">Creare un'istanza di **Win32 \_ ProcessStartup**.</span><span class="sxs-lookup"><span data-stu-id="435c4-322">Create an instance of **Win32\_ProcessStartup**.</span></span>
2.  <span data-ttu-id="435c4-323">Configurare le proprietà della nuova istanza di.</span><span class="sxs-lookup"><span data-stu-id="435c4-323">Configure the properties of the new instance.</span></span>
3.  <span data-ttu-id="435c4-324">Includere l'istanza di come parte del metodo di creazione del [**\_ processo Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="435c4-324">Include the instance as part of the [**Win32\_Process**](win32-process.md) Create method.</span></span>

<span data-ttu-id="435c4-325">Se, ad esempio, è stata creata un'istanza **Win32 \_ ProcessStartup** denominata objConfig, il nome dell'oggetto verrà passato nel metodo create come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="435c4-325">For example, if you have created a **Win32\_ProcessStartup** instance named objConfig, you would pass the object name in the Create method as follows:</span></span>

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a><span data-ttu-id="435c4-326">Esempio</span><span class="sxs-lookup"><span data-stu-id="435c4-326">Examples</span></span>

<span data-ttu-id="435c4-327">Per configurare varie opzioni di avvio per un processo, è possibile usare la classe **Win32 \_ ProcessStartup** .</span><span class="sxs-lookup"><span data-stu-id="435c4-327">You can use the **Win32\_ProcessStartup** class to configure various startup options for a process.</span></span> <span data-ttu-id="435c4-328">Queste opzioni comprendono, ma non sono limitate, ad esempio la creazione di un processo in una finestra nascosta e la creazione di un processo con priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="435c4-328">These options include, but are not limited to, such things as creating a process in a hidden window and creating a higher-priority process.</span></span> <span data-ttu-id="435c4-329">Il codice VBScript seguente consente di creare un processo in una finestra nascosta.</span><span class="sxs-lookup"><span data-stu-id="435c4-329">The following VBScript creates a process in a hidden window.</span></span>


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



<span data-ttu-id="435c4-330">Il codice VBScript seguente consente di creare un processo con priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="435c4-330">The following VBScript creates a higher-priority process.</span></span>


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



<span data-ttu-id="435c4-331">Nell'esempio di codice VBScript seguente viene creato un processo blocco note nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="435c4-331">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="435c4-332">**Win32 \_ ProcessStartup** viene usato per configurare le impostazioni del processo.</span><span class="sxs-lookup"><span data-stu-id="435c4-332">**Win32\_ProcessStartup** is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="435c4-333">Requisiti</span><span class="sxs-lookup"><span data-stu-id="435c4-333">Requirements</span></span>



| <span data-ttu-id="435c4-334">Requisito</span><span class="sxs-lookup"><span data-stu-id="435c4-334">Requirement</span></span> | <span data-ttu-id="435c4-335">Valore</span><span class="sxs-lookup"><span data-stu-id="435c4-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="435c4-336">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="435c4-336">Minimum supported client</span></span><br/> | <span data-ttu-id="435c4-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="435c4-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="435c4-338">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="435c4-338">Minimum supported server</span></span><br/> | <span data-ttu-id="435c4-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="435c4-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="435c4-340">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="435c4-340">Namespace</span></span><br/>                | <span data-ttu-id="435c4-341">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="435c4-341">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="435c4-342">MOF</span><span class="sxs-lookup"><span data-stu-id="435c4-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="435c4-343"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="435c4-343"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="435c4-344">DLL</span><span class="sxs-lookup"><span data-stu-id="435c4-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="435c4-345"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="435c4-345"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="435c4-346">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="435c4-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="435c4-347">**\_MethodParameterClass Win32**</span><span class="sxs-lookup"><span data-stu-id="435c4-347">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md)
</dt> <dt>

[<span data-ttu-id="435c4-348">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="435c4-348">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="435c4-349">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="435c4-349">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="435c4-350">**\_\_ProviderHostQuotaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="435c4-350">**\_\_ProviderHostQuotaConfiguration**</span></span>](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[<span data-ttu-id="435c4-351">Attività WMI: processi</span><span class="sxs-lookup"><span data-stu-id="435c4-351">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
