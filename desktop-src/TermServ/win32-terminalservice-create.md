---
title: Metodo Create della classe Win32_Service (Servizi Desktop remoto)
description: Create method of the Win32_Service class (Servizi Desktop remoto) - Crea un nuovo servizio di sistema.
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- Creare il metodo Servizi Desktop remoto
- Creare il metodo Servizi Desktop remoto , Win32_Service classe
- Win32_Service classe Servizi Desktop remoto metodo , Create
topic_type:
- apiref
api_name:
- Win32_Service.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b776d3e451d84c63be5bb61b98ed22081e1a29
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387120"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="d2a4c-106">Metodo Create della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-106">Create method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="d2a4c-107">Il **metodo Crea** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuovo servizio di sistema.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-107">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="d2a4c-108">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d2a4c-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d2a4c-109">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d2a4c-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a4c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2a4c-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d2a4c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2a4c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a4c-112">*Nome* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-113">Nome del servizio da installare nel **metodo Create.**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="d2a4c-114">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="d2a4c-115">Il database di Gestione controllo servizi mantiene la distinzione tra maiuscole e minuscole dei caratteri, ma i confronti tra i nomi dei servizi non esentengono sempre la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="d2a4c-116">Le barre (/) e le doppie barre rovesciata ( \\ \\ ) sono caratteri del nome di servizio non validi.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-116">Forward-slashes (/) and double back-slashes (\\\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-117">*DisplayName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-118">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-118">Display name of the service.</span></span> <span data-ttu-id="d2a4c-119">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="d2a4c-120">Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="d2a4c-121">*Per i confronti displayName* non viene sempre fatto distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="d2a4c-122">Vincoli: accetta lo stesso valore del *parametro Name.*</span><span class="sxs-lookup"><span data-stu-id="d2a4c-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="d2a4c-123">Esempio: "Atdisk".</span><span class="sxs-lookup"><span data-stu-id="d2a4c-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-124">*PathName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-125">Percorso completo del file eseguibile che implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="d2a4c-126">Esempio: \\ "SystemRoot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="d2a4c-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-127">*ServiceType* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-128">Tipo di servizi forniti ai processi che li chiamano.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-128">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="d2a4c-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-130">Kernel Driver</span><span class="sxs-lookup"><span data-stu-id="d2a4c-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-131">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-132">File System Driver</span><span class="sxs-lookup"><span data-stu-id="d2a4c-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-134">Adattatore</span><span class="sxs-lookup"><span data-stu-id="d2a4c-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-136">Driver di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="d2a4c-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-138">Processo personalizzato</span><span class="sxs-lookup"><span data-stu-id="d2a4c-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-140">Processo di condivisione</span><span class="sxs-lookup"><span data-stu-id="d2a4c-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-142">Processo interattivo</span><span class="sxs-lookup"><span data-stu-id="d2a4c-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d2a4c-143">*ErrorControl* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-144">Gravità dell'errore se non **è possibile avviare** il metodo Create.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="d2a4c-145">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-145">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="d2a4c-146">Tutti gli errori vengono registrati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="d2a4c-147">0</span><span class="sxs-lookup"><span data-stu-id="d2a4c-147">0</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-148">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-148">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-149">1</span><span class="sxs-lookup"><span data-stu-id="d2a4c-149">1</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-150">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-150">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-151">2</span><span class="sxs-lookup"><span data-stu-id="d2a4c-151">2</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-152">Il sistema viene riavviato con l'ultima configurazione valida nota.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-152">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-153">3</span><span class="sxs-lookup"><span data-stu-id="d2a4c-153">3</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-154">Il sistema tenta di iniziare con una configurazione valida.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-154">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d2a4c-155">*StartMode* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-155">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-156">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-156">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="d2a4c-157">Avvio</span><span class="sxs-lookup"><span data-stu-id="d2a4c-157">Boot</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-158">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-158">Device driver started by the operating system loader.</span></span> <span data-ttu-id="d2a4c-159">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-160">Sistema</span><span class="sxs-lookup"><span data-stu-id="d2a4c-160">System</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-161">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-161">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="d2a4c-162">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-162">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-163">Automatico</span><span class="sxs-lookup"><span data-stu-id="d2a4c-163">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-164">Servizio che deve essere avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-164">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-165">Manuale</span><span class="sxs-lookup"><span data-stu-id="d2a4c-165">Manual</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-166">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il [**metodo StartService.**](win32-terminalservice-startservice.md)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-166">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-167">Disabled</span><span class="sxs-lookup"><span data-stu-id="d2a4c-167">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-168">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-168">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d2a4c-169">*DesktopInteract* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-169">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-170">Se **true,** il servizio può creare o comunicare con le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-170">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-171">*StartName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-171">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-172">Nome dell'account con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-172">Account name under which the service runs.</span></span> <span data-ttu-id="d2a4c-173">A seconda del tipo di servizio, il nome dell'account può essere nel formato NomeDominioNomeUtente o Nome entità \\ utente (UPN) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="d2a4c-173">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="d2a4c-174">Il processo del servizio viene registrato usando uno di questi due formati durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-174">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="d2a4c-175">Se l'account appartiene al dominio predefinito, . \\ È possibile specificare il nome utente.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-175">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="d2a4c-176">Se viene specificato **NULL,** il servizio viene connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-176">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="d2a4c-177">Per un kernel o driver a livello di sistema, *StartName* contiene il nome dell'oggetto driver (ovvero FileSystem Rdr o Driver Xns) che il sistema di input e \\ output \\ \\ (I/O) usa per caricare il driver di \\ dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-177">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="d2a4c-178">Se **viene specificato NULL,** il driver viene eseguito con un nome di oggetto predefinito creato dal sistema di I/O in base al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-178">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="d2a4c-179">Esempio: Amministratore \\ DWDOM.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-179">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-180">*StartPassword* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-180">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-181">Password per il nome dell'account specificato dal *parametro StartName.*</span><span class="sxs-lookup"><span data-stu-id="d2a4c-181">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="d2a4c-182">Specificare **NULL** se la password non viene cambiata.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-182">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="d2a4c-183">Specificare una stringa vuota se il servizio non dispone di password.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-183">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-184">*LoadOrderGroup* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-184">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-185">Nome del gruppo associato al nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-185">Group name associated with the new service.</span></span> <span data-ttu-id="d2a4c-186">I gruppi degli ordini di carico sono contenuti nel Registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-186">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="d2a4c-187">Se il puntatore **è NULL** o punta a una stringa vuota, il servizio non appartiene a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-187">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="d2a4c-188">Le dipendenze tra gruppi devono essere elencate nel *parametro LoadOrderGroupDependencies.*</span><span class="sxs-lookup"><span data-stu-id="d2a4c-188">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="d2a4c-189">I servizi nell'elenco dei gruppi di ordinamento del carico vengono avviati per primi, seguiti dai servizi in gruppi non presenti nell'elenco di gruppi di ordinamento del carico, seguiti dai servizi che non appartengono a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-189">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="d2a4c-190">Il Registro di sistema include un elenco di gruppi di ordinamento del carico disponibili in:</span><span class="sxs-lookup"><span data-stu-id="d2a4c-190">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="d2a4c-191">**HKEY \_ Local \_ MACHINE System** \\  \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-191">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-192">*Dipendenze di LoadOrderGroupDependencies* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-192">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-193">Matrice di gruppi di ordinamento del carico che devono essere avviati prima di questo servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-193">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="d2a4c-194">Ogni elemento nella matrice è delimitato da **NULL** e l'elenco termina con due **valori NULL.**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-194">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="d2a4c-195">In Visual Basic o script è possibile passare un oggetto vbArray.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-195">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="d2a4c-196">Se il puntatore **è NULL** o punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-196">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="d2a4c-197">I nomi dei gruppi devono essere preceduti dal carattere **SC \_ GROUP \_ IDENTIFIER** (definito nel file Winsvc.h) per distinguerlo da un nome di servizio, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-197">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="d2a4c-198">La dipendenza da un gruppo significa che il servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-198">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-199">*Dipendenze dei servizi* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d2a4c-199">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-200">Matrice contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-200">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="d2a4c-201">Ogni elemento nella matrice è delimitato da **NULL** e l'elenco termina con due **valori NULL.**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-201">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="d2a4c-202">In Visual Basic o script è possibile passare un oggetto vbArray.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-202">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="d2a4c-203">Se il puntatore **è NULL** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="d2a4c-204">La dipendenza da un servizio significa che il servizio può essere eseguito solo se il servizio da cui dipende è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-204">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a4c-205">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2a4c-205">Return value</span></span>

<span data-ttu-id="d2a4c-206">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-206">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="d2a4c-207">Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-207">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d2a4c-208">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-208">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d2a4c-209">**0**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-209">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-210">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-210">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-211">**1**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-211">**1**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-212">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-212">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-213">**2**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-213">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-214">L'utente non aveva l'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-214">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-215">**3**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-215">**3**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-216">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-216">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-217">**4**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-217">**4**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-218">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-218">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-219">**5**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-219">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-220">Il codice di controllo richiesto non può essere inviato al servizio perché lo stato del servizio (proprietà **State** della [**classe \_ Win32 BaseService)**](/windows/desktop/CIMWin32Prov/win32-baseservice) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-220">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-221">**6**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-221">**6**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-222">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-223">**7**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-223">**7**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-224">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-224">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-225">**8**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-225">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-226">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-226">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-227">**9**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-227">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-228">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-228">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-229">**10**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-229">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-230">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-230">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-231">**11**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-231">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-232">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-232">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-233">**12**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-233">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-234">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-234">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-235">**13**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-235">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-236">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-236">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-237">**14**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-237">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-238">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-238">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-239">**15**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-239">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-240">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-240">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-241">**16**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-241">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-242">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-242">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-243">**17**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-243">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-244">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-244">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-245">**18**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-245">**18**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-246">Il servizio presenta dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-246">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-247">**19**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-247">**19**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-248">Un servizio viene eseguito con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-248">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-249">**20**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-249">**20**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-250">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-250">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-251">**21**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-251">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-252">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-252">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-253">**22**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-253">**22**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-254">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-254">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-255">**23**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-255">**23**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-256">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-256">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d2a4c-257">**24**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-257">**24**</span></span>
</dt> <dd>

<span data-ttu-id="d2a4c-258">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-258">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2a4c-259">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2a4c-259">Remarks</span></span>

<span data-ttu-id="d2a4c-260">I servizi vengono in genere installati in uno dei due modi seguenti: come parte dell'installazione del sistema operativo o tramite un programma di installazione fornito dallo sviluppatore del servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-260">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="d2a4c-261">Tuttavia, alcuni servizi, in particolare quelli creati all'interno di , potrebbero non avere un programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-261">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="d2a4c-262">In questi casi, è possibile usare il **metodo Create per** installare i servizi a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-262">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="d2a4c-263">Nonostante il nome, il metodo Create non crea effettivamente un servizio. si limita a installare un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-263">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="d2a4c-264">Per usare questo comando, è necessario copiare il file eseguibile del servizio in un computer e quindi usare **Crea** per installare il servizio.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-264">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="d2a4c-265">Il **metodo Create** è simile al metodo [**Change.**](win32-terminalservice-change.md)</span><span class="sxs-lookup"><span data-stu-id="d2a4c-265">The **Create** method is similar to the [**Change**](win32-terminalservice-change.md) method.</span></span> <span data-ttu-id="d2a4c-266">In entrambi i casi, le proprietà del servizio vengono passate come parametri al metodo .</span><span class="sxs-lookup"><span data-stu-id="d2a4c-266">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="d2a4c-267">Come per i parametri usati con il **metodo Change,** l'ordine in cui questi parametri vengono passati è molto importante.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-267">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="d2a4c-268">Il *parametro LoadOrderGroup* rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-268">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="d2a4c-269">I servizi devono essere avviati nell'ordine specificato dal gruppo di ordini di carico, in quanto i servizi dipendono l'uno dall'altro.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-269">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="d2a4c-270">Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi antecenti.</span><span class="sxs-lookup"><span data-stu-id="d2a4c-270">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a4c-271">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2a4c-271">Requirements</span></span>



| <span data-ttu-id="d2a4c-272">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a4c-272">Requirement</span></span> | <span data-ttu-id="d2a4c-273">Valore</span><span class="sxs-lookup"><span data-stu-id="d2a4c-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a4c-274">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2a4c-274">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a4c-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2a4c-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2a4c-276">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2a4c-276">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a4c-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2a4c-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2a4c-278">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2a4c-278">Namespace</span></span><br/>                | <span data-ttu-id="d2a4c-279">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d2a4c-279">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d2a4c-280">MOF</span><span class="sxs-lookup"><span data-stu-id="d2a4c-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2a4c-281"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2a4c-281"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2a4c-282">DLL</span><span class="sxs-lookup"><span data-stu-id="d2a4c-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2a4c-283"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2a4c-283"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2a4c-284">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2a4c-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a4c-285">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-285">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="d2a4c-286">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d2a4c-286">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="d2a4c-287">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="d2a4c-287">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="d2a4c-288">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="d2a4c-288">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

