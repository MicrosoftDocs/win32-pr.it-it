---
description: Win32 \_ StartupCommand&\# 8194; La classe WMI rappresenta un comando che viene eseguito automaticamente quando un utente accede al computer.
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Classe Win32_StartupCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878225"
---
# <a name="win32_startupcommand-class"></a><span data-ttu-id="62bd3-103">Win32 \_ StartupCommand (classe)</span><span class="sxs-lookup"><span data-stu-id="62bd3-103">Win32\_StartupCommand class</span></span>

<span data-ttu-id="62bd3-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ StartupCommand Win32** rappresenta un comando che viene eseguito automaticamente quando un utente accede al computer.</span><span class="sxs-lookup"><span data-stu-id="62bd3-104">The **Win32\_StartupCommand** [WMI class](../wmisdk/retrieving-a-class.md) represents a command that runs automatically when a user logs onto the computer system.</span></span>

<span data-ttu-id="62bd3-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="62bd3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="62bd3-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="62bd3-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="62bd3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62bd3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a><span data-ttu-id="62bd3-108">Members</span><span class="sxs-lookup"><span data-stu-id="62bd3-108">Members</span></span>

<span data-ttu-id="62bd3-109">La classe **Win32 \_ StartupCommand** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="62bd3-109">The **Win32\_StartupCommand** class has these types of members:</span></span>

-   [<span data-ttu-id="62bd3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="62bd3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62bd3-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="62bd3-111">Properties</span></span>

<span data-ttu-id="62bd3-112">La classe **Win32 \_ StartupCommand** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="62bd3-112">The **Win32\_StartupCommand** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62bd3-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="62bd3-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bd3-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="62bd3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="62bd3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-116">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="62bd3-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="62bd3-117">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="62bd3-117">Short textual description of the current object.</span></span>

<span data-ttu-id="62bd3-118">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="62bd3-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bd3-119">**Comando**</span><span class="sxs-lookup"><span data-stu-id="62bd3-119">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bd3-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="62bd3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="62bd3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-122">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")</span><span class="sxs-lookup"><span data-stu-id="62bd3-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>
</dt> </dl>

<span data-ttu-id="62bd3-123">Comando eseguito dal comando di avvio.</span><span class="sxs-lookup"><span data-stu-id="62bd3-123">Command run by the startup command.</span></span>

<span data-ttu-id="62bd3-124">WMI ottiene questi dati dalla chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="62bd3-124">WMI obtains this data from the registry key</span></span>

<span data-ttu-id="62bd3-125">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Run**</span><span class="sxs-lookup"><span data-stu-id="62bd3-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Run**</span></span>

<span data-ttu-id="62bd3-126">Esempio: "C: \\ Windows \\notepad.exe myfile.txt"</span><span class="sxs-lookup"><span data-stu-id="62bd3-126">Example: "C:\\Windows\\notepad.exe myfile.txt"</span></span>

</dd> <dt>

<span data-ttu-id="62bd3-127">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="62bd3-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bd3-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="62bd3-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="62bd3-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62bd3-130">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="62bd3-130">Textual description of the current object.</span></span>

<span data-ttu-id="62bd3-131">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="62bd3-131">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bd3-132">**Posizione**</span><span class="sxs-lookup"><span data-stu-id="62bd3-132">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bd3-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="62bd3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="62bd3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-135">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Windows")</span><span class="sxs-lookup"><span data-stu-id="62bd3-135">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|\\\\SOFTWARE\\\\MICROSOFT\\\\WINDOWS\\\\CURRENTVERSION\\\\Windows")</span></span>
</dt> </dl>

<span data-ttu-id="62bd3-136">Percorso in cui si trova il comando di avvio sul disco file system.</span><span class="sxs-lookup"><span data-stu-id="62bd3-136">Path where the startup command resides on the disk file system.</span></span>

<span data-ttu-id="62bd3-137">Ad esempio: HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="62bd3-137">For example: HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

<span data-ttu-id="62bd3-138">**Startup** ("Startup")</span><span class="sxs-lookup"><span data-stu-id="62bd3-138">**Startup** ("Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

<span data-ttu-id="62bd3-139">**Avvio comune** ("avvio comune")</span><span class="sxs-lookup"><span data-stu-id="62bd3-139">**Common Startup** ("Common Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

<span data-ttu-id="62bd3-140">**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")</span><span class="sxs-lookup"><span data-stu-id="62bd3-140">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

<span data-ttu-id="62bd3-141">**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices")</span><span class="sxs-lookup"><span data-stu-id="62bd3-141">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="62bd3-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="62bd3-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bd3-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="62bd3-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="62bd3-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-145">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| file Structures \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| cFileName")</span><span class="sxs-lookup"><span data-stu-id="62bd3-145">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Structures\|[**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa)\|cFileName")</span></span>
</dt> </dl>

<span data-ttu-id="62bd3-146">Nome file del comando di avvio.</span><span class="sxs-lookup"><span data-stu-id="62bd3-146">File name of the startup command.</span></span>

<span data-ttu-id="62bd3-147">Esempio: "FindFast"</span><span class="sxs-lookup"><span data-stu-id="62bd3-147">Example: "FindFast"</span></span>

</dd> <dt>

<span data-ttu-id="62bd3-148">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="62bd3-148">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bd3-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="62bd3-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="62bd3-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-151">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="62bd3-151">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="62bd3-152">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="62bd3-152">Identifier by which the current object is known.</span></span>

<span data-ttu-id="62bd3-153">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="62bd3-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bd3-154">**Utente**</span><span class="sxs-lookup"><span data-stu-id="62bd3-154">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bd3-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="62bd3-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="62bd3-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-157">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="62bd3-157">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="62bd3-158">Nome utente per il quale verrà eseguito il comando di avvio.</span><span class="sxs-lookup"><span data-stu-id="62bd3-158">User name for whom this startup command will run.</span></span>

<span data-ttu-id="62bd3-159">Esempio: "nome dominio \\ "</span><span class="sxs-lookup"><span data-stu-id="62bd3-159">Example: "mydomain\\myname"</span></span>

</dd> <dt>

<span data-ttu-id="62bd3-160">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="62bd3-160">**UserSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bd3-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="62bd3-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="62bd3-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bd3-163">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="62bd3-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="62bd3-164">La proprietà UserSID indica il SID dell'utente per il quale verrà eseguito il comando di avvio.</span><span class="sxs-lookup"><span data-stu-id="62bd3-164">The UserSID property indicates the SID of the user for whom this startup command will run.</span></span> <span data-ttu-id="62bd3-165">Tale proprietà utente può essere vuota, ma UserSID ancora un valore se non è possibile risolvere il nome utente (ad esempio, nel caso di un utente eliminato).</span><span class="sxs-lookup"><span data-stu-id="62bd3-165">That User property may be empty but UserSID still has a value if the user name can't be resolved (like in the case of a deleted user).</span></span> <span data-ttu-id="62bd3-166">La proprietà è utile per distinguere tra i comandi associati a due utenti diversi con nomi non risolti.</span><span class="sxs-lookup"><span data-stu-id="62bd3-166">The property is helpful to distinguish between commands associated w/ two different users with unresolved names.</span></span> <span data-ttu-id="62bd3-167">Può essere NULL se il comando è associato a elementi che non identificano effettivamente un utente come tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="62bd3-167">It may be NULL when the command is associated with items not actually identifying a user like All Users.</span></span>

<span data-ttu-id="62bd3-168">Esempio: S-1-5-21-1579938362-1064596589-3161144252-1006</span><span class="sxs-lookup"><span data-stu-id="62bd3-168">Example:S-1-5-21-1579938362-1064596589-3161144252-1006</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62bd3-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="62bd3-169">Remarks</span></span>

<span data-ttu-id="62bd3-170">La classe **Win32 \_ StartupCommand** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="62bd3-170">The **Win32\_StartupCommand** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="62bd3-171">L'avvio del computer non termina dopo il caricamento del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="62bd3-171">Computer startup does not end after the operating system has been loaded.</span></span> <span data-ttu-id="62bd3-172">Al contrario, è possibile configurare il sistema operativo Windows in modo che i comandi di avvio vengano eseguiti ogni volta che viene avviato Windows.</span><span class="sxs-lookup"><span data-stu-id="62bd3-172">Instead, the Windows operating system can be configured so that startup commands are run each time Windows starts.</span></span> <span data-ttu-id="62bd3-173">I comandi di avvio vengono archiviati nel registro di sistema o come parte del profilo utente e vengono usati per avviare automaticamente gli script o le applicazioni specificati ogni volta che viene caricato Windows.</span><span class="sxs-lookup"><span data-stu-id="62bd3-173">Startup commands are stored in the registry or as part of the user profile and are used to automatically start specified scripts or applications each time Windows is loaded.</span></span>

<span data-ttu-id="62bd3-174">Nella maggior parte dei casi, i programmi di avvio automatico sono utili. assicurano che alcune applicazioni, ad esempio gli strumenti antivirus, vengano avviate automaticamente ed eseguite ogni volta che viene caricato Windows.</span><span class="sxs-lookup"><span data-stu-id="62bd3-174">In most cases, autostart programs are useful; they ensure that certain applications, such as antivirus tools, are automatically started and run each time Windows is loaded.</span></span> <span data-ttu-id="62bd3-175">Tuttavia, i programmi di avvio automatico possono anche essere responsabili di problemi quali:</span><span class="sxs-lookup"><span data-stu-id="62bd3-175">However, autostart programs also can be responsible for problems such as:</span></span>

-   <span data-ttu-id="62bd3-176">Computer che importano un tempo eccezionalmente lungo per l'avvio.</span><span class="sxs-lookup"><span data-stu-id="62bd3-176">Computers that take an exceptionally long time to start.</span></span> <span data-ttu-id="62bd3-177">Questo potrebbe essere il risultato di un numero elevato di applicazioni che devono essere avviate ogni volta che viene avviato Windows.</span><span class="sxs-lookup"><span data-stu-id="62bd3-177">This might be the result of a large number of applications that must be started each time Windows starts.</span></span>
-   <span data-ttu-id="62bd3-178">Applicazioni rappresentate nella barra delle applicazioni o in Gestione attività, anche se non sono state avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="62bd3-178">Applications that are represented in the Taskbar or in Task Manager, even though the user did not start them.</span></span> <span data-ttu-id="62bd3-179">Anche se queste applicazioni non causano necessariamente problemi, possono comportare chiamate di help desk da parte di utenti confusi da dove provengono questi programmi e perché sono in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="62bd3-179">Although these applications do not necessarily cause problems, they can result in help desk calls from users who are confused as to where these programs came from and why they are running.</span></span>
-   <span data-ttu-id="62bd3-180">Computer che riscontrano problemi anche quando sembrano inattivi.</span><span class="sxs-lookup"><span data-stu-id="62bd3-180">Computers experiencing problems even when they seem idle.</span></span> <span data-ttu-id="62bd3-181">Questi problemi vengono spesso tracciati per i comandi di avvio che sono in esecuzione quando nessuno è consapevole che sono in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="62bd3-181">These problems are often traced to startup commands that are running when no one is aware that they are running.</span></span>

<span data-ttu-id="62bd3-182">Identificare le applicazioni e gli script che vengono eseguiti automaticamente all'avvio è un'attività amministrativa importante, ma complessa, perché i comandi di avvio possono essere archiviati in molte posizioni diverse:</span><span class="sxs-lookup"><span data-stu-id="62bd3-182">Identifying the applications and scripts that automatically run at startup is an important but difficult administrative task, because startup commands can be stored in many different locations:</span></span>

-   <span data-ttu-id="62bd3-183">HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="62bd3-183">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="62bd3-184">HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="62bd3-184">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="62bd3-185">HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="62bd3-185">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="62bd3-186">HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="62bd3-186">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="62bd3-187">HKU \\ ProgID \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="62bd3-187">HKU\\ProgID\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="62bd3-188">SystemDrive \\ Documents and Settings \\ tutti gli utenti \\ Start menu \\ programs \\ Startup</span><span class="sxs-lookup"><span data-stu-id="62bd3-188">systemdrive\\Documents and Settings\\All Users\\Start Menu\\Programs\\Startup</span></span>
-   <span data-ttu-id="62bd3-189">\\documenti SystemDrive e impostazioni \\ nome utente avvio \\ \\ programmi \\ menu Start</span><span class="sxs-lookup"><span data-stu-id="62bd3-189">systemdrive\\Documents and Settings\\username\\Start Menu\\Programs\\Startup</span></span>

<span data-ttu-id="62bd3-190">È possibile utilizzare la classe WMI Win32 \_ StartupCommand per enumerare i programmi di avvio automatico indipendentemente dalla posizione in cui sono archiviate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="62bd3-190">You can use the WMI Win32\_StartupCommand class to enumerate autostart programs regardless of where the information is stored.</span></span>

<span data-ttu-id="62bd3-191">Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="62bd3-191">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="62bd3-192">Se ad esempio si enumera questa classe nel computer locale, l'account con cui viene eseguita l'applicazione deve disporre di questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="62bd3-192">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="62bd3-193">Per altre informazioni, vedere [esecuzione di operazioni con privilegi](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="62bd3-193">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="62bd3-194">È possibile modificare i valori del registro di sistema in cui **Win32 \_ StartupCommand** ottiene i dati chiamando i metodi del [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) WMI nello script o in C++.</span><span class="sxs-lookup"><span data-stu-id="62bd3-194">You can change the registry values where **Win32\_StartupCommand** obtains data by calling the WMI [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) methods in script or in C++.</span></span> <span data-ttu-id="62bd3-195">Per ulteriori informazioni, vedere [modifica del registro di sistema](../wmisdk/modifying-the-system-registry.md).</span><span class="sxs-lookup"><span data-stu-id="62bd3-195">For more information, see [Modifying the System Registry](../wmisdk/modifying-the-system-registry.md).</span></span>

## <a name="examples"></a><span data-ttu-id="62bd3-196">Esempio</span><span class="sxs-lookup"><span data-stu-id="62bd3-196">Examples</span></span>

<span data-ttu-id="62bd3-197">Il codice VBScript seguente enumera i comandi di avvio in un computer.</span><span class="sxs-lookup"><span data-stu-id="62bd3-197">The following VBScript enumerates the startup commands on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
Next
```



## <a name="requirements"></a><span data-ttu-id="62bd3-198">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62bd3-198">Requirements</span></span>



| <span data-ttu-id="62bd3-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="62bd3-199">Requirement</span></span> | <span data-ttu-id="62bd3-200">Valore</span><span class="sxs-lookup"><span data-stu-id="62bd3-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62bd3-201">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62bd3-201">Minimum supported client</span></span><br/> | <span data-ttu-id="62bd3-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62bd3-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62bd3-203">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62bd3-203">Minimum supported server</span></span><br/> | <span data-ttu-id="62bd3-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62bd3-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62bd3-205">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="62bd3-205">Namespace</span></span><br/>                | <span data-ttu-id="62bd3-206">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="62bd3-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62bd3-207">MOF</span><span class="sxs-lookup"><span data-stu-id="62bd3-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62bd3-208"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62bd3-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62bd3-209">DLL</span><span class="sxs-lookup"><span data-stu-id="62bd3-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62bd3-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62bd3-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62bd3-211">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62bd3-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62bd3-212">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="62bd3-212">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="62bd3-213">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="62bd3-213">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
