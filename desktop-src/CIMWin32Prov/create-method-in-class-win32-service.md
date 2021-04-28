---
description: Creare il metodo della Win32_Service (provider WMI CIMWin32) - Crea un nuovo servizio di sistema.
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71bc0f4edb879fc4a51a012bc53db67031056f47
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089690"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="4a56f-103">Metodo Create della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="4a56f-103">Create method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4a56f-104">Il **metodo Crea** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuovo servizio di sistema.</span><span class="sxs-lookup"><span data-stu-id="4a56f-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="4a56f-105">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4a56f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4a56f-106">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4a56f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a56f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a56f-107">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="4a56f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a56f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a56f-109">*Nome* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-110">Nome del servizio da installare nel **metodo Create.**</span><span class="sxs-lookup"><span data-stu-id="4a56f-110">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="4a56f-111">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="4a56f-111">The maximum string length is 256 characters.</span></span> <span data-ttu-id="4a56f-112">Il database di Gestione controllo servizi mantiene la distinzione tra maiuscole e minuscole dei caratteri, ma i confronti tra i nomi dei servizi non esentengono sempre la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4a56f-112">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="4a56f-113">Le barre (/) e le doppie barre rovesciata ( \\ ) sono caratteri del nome di servizio non validi.</span><span class="sxs-lookup"><span data-stu-id="4a56f-113">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-114">*DisplayName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-114">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-115">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-115">Display name of the service.</span></span> <span data-ttu-id="4a56f-116">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="4a56f-116">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="4a56f-117">Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="4a56f-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="4a56f-118">*Per i confronti displayName* non viene sempre fatto distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4a56f-118">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="4a56f-119">Vincoli: accetta lo stesso valore del *parametro Name.*</span><span class="sxs-lookup"><span data-stu-id="4a56f-119">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="4a56f-120">Esempio: "Atdisk".</span><span class="sxs-lookup"><span data-stu-id="4a56f-120">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-121">*PathName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-121">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-122">Percorso completo del file eseguibile che implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-122">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="4a56f-123">Esempio: \\ "SystemRoot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="4a56f-123">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-124">*ServiceType* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-124">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-125">Tipo di servizi forniti ai processi che li chiamano.</span><span class="sxs-lookup"><span data-stu-id="4a56f-125">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="4a56f-126">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4a56f-126">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-127">Kernel Driver</span><span class="sxs-lookup"><span data-stu-id="4a56f-127">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-128">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="4a56f-128">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-129">File System Driver</span><span class="sxs-lookup"><span data-stu-id="4a56f-129">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-130">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="4a56f-130">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-131">Adattatore</span><span class="sxs-lookup"><span data-stu-id="4a56f-131">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-132">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="4a56f-132">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-133">Driver di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="4a56f-133">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-134">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="4a56f-134">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-135">Processo personalizzato</span><span class="sxs-lookup"><span data-stu-id="4a56f-135">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-136">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="4a56f-136">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-137">Processo di condivisione</span><span class="sxs-lookup"><span data-stu-id="4a56f-137">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-138">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="4a56f-138">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-139">Processo interattivo</span><span class="sxs-lookup"><span data-stu-id="4a56f-139">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4a56f-140">*ErrorControl* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-140">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-141">Gravità dell'errore se **l'avvio del metodo Create** non riesce.</span><span class="sxs-lookup"><span data-stu-id="4a56f-141">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="4a56f-142">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="4a56f-142">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="4a56f-143">Tutti gli errori vengono registrati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4a56f-143">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="4a56f-144">0</span><span class="sxs-lookup"><span data-stu-id="4a56f-144">0</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-145">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="4a56f-145">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-146">1</span><span class="sxs-lookup"><span data-stu-id="4a56f-146">1</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-147">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="4a56f-147">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-148">2</span><span class="sxs-lookup"><span data-stu-id="4a56f-148">2</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-149">Il sistema viene riavviato con l'ultima configurazione valida nota.</span><span class="sxs-lookup"><span data-stu-id="4a56f-149">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-150">3</span><span class="sxs-lookup"><span data-stu-id="4a56f-150">3</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-151">Il sistema tenta di iniziare con una buona configurazione.</span><span class="sxs-lookup"><span data-stu-id="4a56f-151">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4a56f-152">*StartMode* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-152">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-153">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="4a56f-153">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="4a56f-154">Avvio</span><span class="sxs-lookup"><span data-stu-id="4a56f-154">Boot</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-155">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4a56f-155">Device driver started by the operating system loader.</span></span> <span data-ttu-id="4a56f-156">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="4a56f-156">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-157">Sistema</span><span class="sxs-lookup"><span data-stu-id="4a56f-157">System</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-158">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4a56f-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="4a56f-159">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="4a56f-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-160">Automatico</span><span class="sxs-lookup"><span data-stu-id="4a56f-160">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-161">Servizio che deve essere avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="4a56f-161">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-162">Manuale</span><span class="sxs-lookup"><span data-stu-id="4a56f-162">Manual</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-163">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il [**metodo StartService.**](startservice-method-in-class-win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="4a56f-163">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-164">Disabled</span><span class="sxs-lookup"><span data-stu-id="4a56f-164">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-165">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="4a56f-165">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4a56f-166">*DesktopInteract* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-167">Se **true,** il servizio può creare o comunicare con le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="4a56f-167">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-168">*StartName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-169">Nome dell'account con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-169">Account name under which the service runs.</span></span> <span data-ttu-id="4a56f-170">A seconda del tipo di servizio, il nome dell'account può essere nel formato NomeDominioNomeUtente o Nome entità \\ utente (UPN) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="4a56f-170">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="4a56f-171">Il processo del servizio viene registrato usando uno di questi due formati durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4a56f-171">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="4a56f-172">Se l'account appartiene al dominio predefinito, . \\ È possibile specificare il nome utente.</span><span class="sxs-lookup"><span data-stu-id="4a56f-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="4a56f-173">Se viene specificato **NULL,** il servizio viene connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="4a56f-173">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="4a56f-174">Per un kernel o driver a livello di sistema, *StartName* contiene il nome dell'oggetto driver (ovvero FileSystem Rdr o Driver Xns) che il sistema di input e \\ output \\ \\ (I/O) usa per caricare il driver di \\ dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a56f-174">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="4a56f-175">Se **viene specificato NULL,** il driver viene eseguito con un nome di oggetto predefinito creato dal sistema di I/O in base al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-175">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="4a56f-176">Esempio: Amministratore \\ DWDOM.</span><span class="sxs-lookup"><span data-stu-id="4a56f-176">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-177">*StartPassword* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-178">Password per il nome dell'account specificato dal *parametro StartName.*</span><span class="sxs-lookup"><span data-stu-id="4a56f-178">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="4a56f-179">Specificare **NULL** se la password non viene cambiata.</span><span class="sxs-lookup"><span data-stu-id="4a56f-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="4a56f-180">Specificare una stringa vuota se il servizio non dispone di password.</span><span class="sxs-lookup"><span data-stu-id="4a56f-180">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-181">*LoadOrderGroup* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-181">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-182">Nome del gruppo associato al nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-182">Group name associated with the new service.</span></span> <span data-ttu-id="4a56f-183">I gruppi degli ordini di caricamento sono contenuti nel Registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4a56f-183">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="4a56f-184">Se il puntatore **è NULL** o punta a una stringa vuota, il servizio non appartiene a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="4a56f-184">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="4a56f-185">Le dipendenze tra gruppi devono essere elencate nel *parametro LoadOrderGroupDependencies.*</span><span class="sxs-lookup"><span data-stu-id="4a56f-185">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="4a56f-186">I servizi nell'elenco dei gruppi di ordinamento del carico vengono avviati per primi, seguiti dai servizi in gruppi non presenti nell'elenco dei gruppi di ordinamento del carico, seguiti dai servizi che non appartengono a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="4a56f-186">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="4a56f-187">Il Registro di sistema include un elenco di gruppi di ordinamento del carico disponibili in:</span><span class="sxs-lookup"><span data-stu-id="4a56f-187">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="4a56f-188">**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="4a56f-188">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-189">*LoadOrderGroupDependencies* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-189">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-190">Matrice di gruppi di ordinamento del carico che devono essere avviati prima di questo servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-190">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="4a56f-191">Ogni elemento della matrice è delimitato da **NULL** e l'elenco viene terminato da due **valori NULL.**</span><span class="sxs-lookup"><span data-stu-id="4a56f-191">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="4a56f-192">In Visual Basic script è possibile passare un vbArray.</span><span class="sxs-lookup"><span data-stu-id="4a56f-192">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="4a56f-193">Se il puntatore **è NULL** o punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="4a56f-193">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="4a56f-194">I nomi dei gruppi devono essere preceduti dal carattere **SC \_ GROUP \_ IDENTIFIER** (definito nel file Winsvc.h) per differenziarlo da un nome di servizio, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4a56f-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="4a56f-195">La dipendenza da un gruppo indica che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="4a56f-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-196">*Dipendenze dei servizi* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a56f-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-197">Matrice contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-197">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="4a56f-198">Ogni elemento della matrice è delimitato da **NULL** e l'elenco viene terminato da due **valori NULL.**</span><span class="sxs-lookup"><span data-stu-id="4a56f-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="4a56f-199">In Visual Basic script è possibile passare un oggetto vbArray.</span><span class="sxs-lookup"><span data-stu-id="4a56f-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="4a56f-200">Se il puntatore **è NULL** o punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="4a56f-200">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="4a56f-201">La dipendenza da un servizio significa che il servizio può essere eseguito solo se il servizio da cui dipende è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4a56f-201">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a56f-202">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a56f-202">Return value</span></span>

<span data-ttu-id="4a56f-203">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="4a56f-203">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="4a56f-204">Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="4a56f-204">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4a56f-205">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="4a56f-205">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4a56f-206">**0**</span><span class="sxs-lookup"><span data-stu-id="4a56f-206">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-207">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="4a56f-207">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-208">**1**</span><span class="sxs-lookup"><span data-stu-id="4a56f-208">**1**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-209">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="4a56f-209">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-210">**2**</span><span class="sxs-lookup"><span data-stu-id="4a56f-210">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-211">L'utente non aveva l'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="4a56f-211">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-212">**3**</span><span class="sxs-lookup"><span data-stu-id="4a56f-212">**3**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-213">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-214">**4**</span><span class="sxs-lookup"><span data-stu-id="4a56f-214">**4**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-215">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-215">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-216">**5**</span><span class="sxs-lookup"><span data-stu-id="4a56f-216">**5**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-217">Il codice di controllo richiesto non può essere inviato al servizio perché lo stato del servizio (proprietà **State** della [**classe \_ Win32 BaseService)**](win32-baseservice.md) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="4a56f-217">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](win32-baseservice.md) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-218">**6**</span><span class="sxs-lookup"><span data-stu-id="4a56f-218">**6**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-219">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="4a56f-219">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-220">**7**</span><span class="sxs-lookup"><span data-stu-id="4a56f-220">**7**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-221">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-221">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-222">**8**</span><span class="sxs-lookup"><span data-stu-id="4a56f-222">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-223">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-223">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-224">**9**</span><span class="sxs-lookup"><span data-stu-id="4a56f-224">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-225">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-225">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-226">**10**</span><span class="sxs-lookup"><span data-stu-id="4a56f-226">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-227">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4a56f-227">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-228">**11**</span><span class="sxs-lookup"><span data-stu-id="4a56f-228">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-229">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="4a56f-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-230">**12**</span><span class="sxs-lookup"><span data-stu-id="4a56f-230">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-231">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4a56f-231">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-232">**13**</span><span class="sxs-lookup"><span data-stu-id="4a56f-232">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-233">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="4a56f-233">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-234">**14**</span><span class="sxs-lookup"><span data-stu-id="4a56f-234">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-235">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4a56f-235">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-236">**15**</span><span class="sxs-lookup"><span data-stu-id="4a56f-236">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-237">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4a56f-237">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-238">**16**</span><span class="sxs-lookup"><span data-stu-id="4a56f-238">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-239">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4a56f-239">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-240">**17**</span><span class="sxs-lookup"><span data-stu-id="4a56f-240">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-241">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4a56f-241">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-242">**18**</span><span class="sxs-lookup"><span data-stu-id="4a56f-242">**18**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-243">Il servizio presenta dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-243">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-244">**19**</span><span class="sxs-lookup"><span data-stu-id="4a56f-244">**19**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-245">Un servizio viene eseguito con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="4a56f-245">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-246">**20**</span><span class="sxs-lookup"><span data-stu-id="4a56f-246">**20**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-247">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="4a56f-247">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-248">**21**</span><span class="sxs-lookup"><span data-stu-id="4a56f-248">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-249">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="4a56f-249">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-250">**22**</span><span class="sxs-lookup"><span data-stu-id="4a56f-250">**22**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-251">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-251">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-252">**23**</span><span class="sxs-lookup"><span data-stu-id="4a56f-252">**23**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-253">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4a56f-253">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4a56f-254">**24**</span><span class="sxs-lookup"><span data-stu-id="4a56f-254">**24**</span></span>
</dt> <dd>

<span data-ttu-id="4a56f-255">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4a56f-255">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a56f-256">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a56f-256">Remarks</span></span>

<span data-ttu-id="4a56f-257">I servizi vengono in genere installati in uno dei due modi seguenti: come parte dell'installazione del sistema operativo o tramite un programma di installazione fornito dallo sviluppatore del servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-257">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="4a56f-258">Tuttavia, alcuni servizi, in particolare quelli creati all'interno, potrebbero non avere un programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="4a56f-258">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="4a56f-259">In questi casi, è possibile usare il **metodo Create per** installare i servizi a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="4a56f-259">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="4a56f-260">Nonostante il nome, il metodo Create non crea effettivamente un servizio. installa semplicemente un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="4a56f-260">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="4a56f-261">Per usare questo comando, è necessario copiare il file eseguibile del servizio in un computer e quindi usare **Crea** per installare il servizio.</span><span class="sxs-lookup"><span data-stu-id="4a56f-261">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="4a56f-262">Il **metodo Create** è simile al metodo [**Change.**](change-method-in-class-win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="4a56f-262">The **Create** method is similar to the [**Change**](change-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="4a56f-263">In entrambi i casi, le proprietà del servizio vengono passate come parametri al metodo .</span><span class="sxs-lookup"><span data-stu-id="4a56f-263">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="4a56f-264">Come per i parametri usati con il **metodo Change,** l'ordine in cui questi parametri vengono passati è molto importante.</span><span class="sxs-lookup"><span data-stu-id="4a56f-264">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="4a56f-265">Il *parametro LoadOrderGroup* rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4a56f-265">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="4a56f-266">I servizi devono essere avviati nell'ordine specificato dal gruppo di ordini di caricamento, in quanto i servizi dipendono l'uno dall'altro.</span><span class="sxs-lookup"><span data-stu-id="4a56f-266">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="4a56f-267">Questi servizi dipendenti richiedono la presenza dei servizi di riferimento per il corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="4a56f-267">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="4a56f-268">Esempio</span><span class="sxs-lookup"><span data-stu-id="4a56f-268">Examples</span></span>

<span data-ttu-id="4a56f-269">Il codice VBScript seguente installa un servizio denominato DbService</span><span class="sxs-lookup"><span data-stu-id="4a56f-269">The following VBScript installs a service named DbService</span></span>


```VB
Const OWN_PROCESS = 16
Const NOT_INTERACTIVE = True
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objService = objWMIService.Get("Win32_BaseService")
errReturn = objService.Create ("DbService", "Personnel Database", _
"c:\windows\system32\db.exe", OWN_PROCESS ,2 ,"Automatic" , _
 NOT_INTERACTIVE ,".\LocalSystem" ,"")
```



## <a name="requirements"></a><span data-ttu-id="4a56f-270">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a56f-270">Requirements</span></span>



| <span data-ttu-id="4a56f-271">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a56f-271">Requirement</span></span> | <span data-ttu-id="4a56f-272">Valore</span><span class="sxs-lookup"><span data-stu-id="4a56f-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a56f-273">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a56f-273">Minimum supported client</span></span><br/> | <span data-ttu-id="4a56f-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a56f-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a56f-275">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a56f-275">Minimum supported server</span></span><br/> | <span data-ttu-id="4a56f-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a56f-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a56f-277">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4a56f-277">Namespace</span></span><br/>                | <span data-ttu-id="4a56f-278">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4a56f-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4a56f-279">MOF</span><span class="sxs-lookup"><span data-stu-id="4a56f-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a56f-280"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a56f-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a56f-281">DLL</span><span class="sxs-lookup"><span data-stu-id="4a56f-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a56f-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a56f-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a56f-283">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a56f-283">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a56f-284">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4a56f-284">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4a56f-285">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="4a56f-285">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="4a56f-286">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="4a56f-286">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

