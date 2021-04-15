---
title: Metodo Create della classe Win32_Service (Servizi Desktop remoto)
description: Crea un nuovo servizio di sistema.
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto crea metodo
- Create Method Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo create
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
ms.openlocfilehash: be44d6c67e0d5bd6333f57c44cc44c25dc64e04a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477710"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="dfd52-106">Metodo Create della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="dfd52-106">Create method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="dfd52-107">Il metodo **create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuovo servizio di sistema.</span><span class="sxs-lookup"><span data-stu-id="dfd52-107">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="dfd52-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="dfd52-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dfd52-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dfd52-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd52-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfd52-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="dfd52-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="dfd52-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfd52-112">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-113">Nome del servizio da installare nel metodo **create** .</span><span class="sxs-lookup"><span data-stu-id="dfd52-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="dfd52-114">La lunghezza massima della stringa è 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="dfd52-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="dfd52-115">Il database di gestione controllo servizi conserva la distinzione tra maiuscole e minuscole dei caratteri, ma i confronti tra nomi di servizio non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="dfd52-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="dfd52-116">Barre (/) e barre rovesciate doppie ( \) sono caratteri del nome del servizio non validi.</span><span class="sxs-lookup"><span data-stu-id="dfd52-116">Forward-slashes (/) and double back-slashes (\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-117">*DisplayName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-118">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-118">Display name of the service.</span></span> <span data-ttu-id="dfd52-119">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="dfd52-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="dfd52-120">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="dfd52-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="dfd52-121">I confronti *DisplayName* sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="dfd52-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="dfd52-122">Constraints: accetta lo stesso valore del parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="dfd52-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="dfd52-123">Esempio: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="dfd52-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-124">*Nome percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-125">Percorso completo del file eseguibile che implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="dfd52-126">Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="dfd52-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-127">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-128">Tipo di servizi forniti ai processi che li chiamano.</span><span class="sxs-lookup"><span data-stu-id="dfd52-128">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="dfd52-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="dfd52-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-130">Driver del kernel</span><span class="sxs-lookup"><span data-stu-id="dfd52-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-131">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="dfd52-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-132">Driver del file System</span><span class="sxs-lookup"><span data-stu-id="dfd52-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="dfd52-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-134">Adattatore</span><span class="sxs-lookup"><span data-stu-id="dfd52-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="dfd52-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-136">Driver di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="dfd52-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="dfd52-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-138">Processo personale</span><span class="sxs-lookup"><span data-stu-id="dfd52-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="dfd52-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-140">Condividi processo</span><span class="sxs-lookup"><span data-stu-id="dfd52-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="dfd52-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-142">Processo interattivo</span><span class="sxs-lookup"><span data-stu-id="dfd52-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dfd52-143">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-144">Gravità dell'errore se non è possibile avviare il metodo **create** .</span><span class="sxs-lookup"><span data-stu-id="dfd52-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="dfd52-145">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="dfd52-145">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="dfd52-146">Tutti gli errori vengono registrati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="dfd52-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="dfd52-147">0</span><span class="sxs-lookup"><span data-stu-id="dfd52-147">0</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-148">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="dfd52-148">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-149">1</span><span class="sxs-lookup"><span data-stu-id="dfd52-149">1</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-150">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="dfd52-150">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-151">2</span><span class="sxs-lookup"><span data-stu-id="dfd52-151">2</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-152">Il sistema viene riavviato con l'ultima configurazione valida nota.</span><span class="sxs-lookup"><span data-stu-id="dfd52-152">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-153">3</span><span class="sxs-lookup"><span data-stu-id="dfd52-153">3</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-154">Il sistema tenta di iniziare con una configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="dfd52-154">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dfd52-155">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-155">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-156">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="dfd52-156">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="dfd52-157">Avvio</span><span class="sxs-lookup"><span data-stu-id="dfd52-157">Boot</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-158">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dfd52-158">Device driver started by the operating system loader.</span></span> <span data-ttu-id="dfd52-159">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="dfd52-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-160">Sistema</span><span class="sxs-lookup"><span data-stu-id="dfd52-160">System</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-161">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dfd52-161">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="dfd52-162">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="dfd52-162">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-163">Automatico</span><span class="sxs-lookup"><span data-stu-id="dfd52-163">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-164">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="dfd52-164">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-165">Manuale</span><span class="sxs-lookup"><span data-stu-id="dfd52-165">Manual</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-166">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="dfd52-166">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-167">Disabled</span><span class="sxs-lookup"><span data-stu-id="dfd52-167">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-168">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="dfd52-168">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dfd52-169">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-169">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-170">Se **true**, il servizio può creare o comunicare con Windows sul desktop.</span><span class="sxs-lookup"><span data-stu-id="dfd52-170">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-171">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-171">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-172">Nome dell'account con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-172">Account name under which the service runs.</span></span> <span data-ttu-id="dfd52-173">A seconda del tipo di servizio, il nome dell'account può essere nel formato DomainName \\ username o nome dell'entità utente (UPN) Username@DomainName .</span><span class="sxs-lookup"><span data-stu-id="dfd52-173">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="dfd52-174">Il processo del servizio viene registrato utilizzando una di queste due forme durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dfd52-174">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="dfd52-175">Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente.</span><span class="sxs-lookup"><span data-stu-id="dfd52-175">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="dfd52-176">Se viene specificato **null** , il servizio viene connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="dfd52-176">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="dfd52-177">Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto driver (ovvero \\ filesystem \\ RDR o \\ driver \\ XNS) utilizzato dal sistema di input e output (i/O) per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dfd52-177">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="dfd52-178">Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-178">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="dfd52-179">Esempio: amministratore di DWDOM \\ .</span><span class="sxs-lookup"><span data-stu-id="dfd52-179">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-180">*StartPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-180">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-181">Password per il nome dell'account specificato dal parametro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="dfd52-181">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="dfd52-182">Specificare **null** se non si sta modificando la password.</span><span class="sxs-lookup"><span data-stu-id="dfd52-182">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="dfd52-183">Specificare una stringa vuota se il servizio non dispone di password.</span><span class="sxs-lookup"><span data-stu-id="dfd52-183">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-184">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-184">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-185">Nome del gruppo associato al nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-185">Group name associated with the new service.</span></span> <span data-ttu-id="dfd52-186">I gruppi dell'ordine di caricamento sono contenuti nel registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dfd52-186">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="dfd52-187">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non appartiene a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="dfd52-187">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="dfd52-188">Le dipendenze tra i gruppi devono essere elencate nel parametro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="dfd52-188">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="dfd52-189">I servizi nell'elenco di gruppi per l'ordine di caricamento vengono avviati per primi, seguiti da servizi nei gruppi non inclusi nell'elenco del gruppo di ordini di carico, seguiti da servizi che non appartengono a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="dfd52-189">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="dfd52-190">Nel registro di sistema è presente un elenco di gruppi di ordini di carico disponibili in:</span><span class="sxs-lookup"><span data-stu-id="dfd52-190">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="dfd52-191">**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="dfd52-191">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-192">*LoadOrderGroupDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-192">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-193">Matrice di gruppi di ordini di caricamento che devono iniziare prima del servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-193">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="dfd52-194">Ogni elemento nella matrice è delimitato da **null** e l'elenco viene terminato da due valori **null** .</span><span class="sxs-lookup"><span data-stu-id="dfd52-194">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="dfd52-195">In Visual Basic o script è possibile passare un vbArray.</span><span class="sxs-lookup"><span data-stu-id="dfd52-195">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="dfd52-196">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="dfd52-196">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="dfd52-197">I nomi dei gruppi devono essere preceduti **dall' \_ \_ identificatore del gruppo SC** (definito nel file winsvc. h) per distinguerlo dal nome del servizio, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="dfd52-197">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="dfd52-198">La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="dfd52-198">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-199">*ServiceDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd52-199">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-200">Matrice che contiene i nomi dei servizi che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-200">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="dfd52-201">Ogni elemento nella matrice è delimitato da **null** e l'elenco viene terminato da due valori **null** .</span><span class="sxs-lookup"><span data-stu-id="dfd52-201">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="dfd52-202">In Visual Basic o script è possibile passare un vbArray.</span><span class="sxs-lookup"><span data-stu-id="dfd52-202">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="dfd52-203">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="dfd52-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="dfd52-204">La dipendenza da un servizio significa che questo servizio può essere eseguito solo se è in esecuzione il servizio da cui dipende.</span><span class="sxs-lookup"><span data-stu-id="dfd52-204">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfd52-205">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dfd52-205">Return value</span></span>

<span data-ttu-id="dfd52-206">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="dfd52-206">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="dfd52-207">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="dfd52-207">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="dfd52-208">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="dfd52-208">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="dfd52-209">**0**</span><span class="sxs-lookup"><span data-stu-id="dfd52-209">**0**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-210">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="dfd52-210">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-211">**1**</span><span class="sxs-lookup"><span data-stu-id="dfd52-211">**1**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-212">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="dfd52-212">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-213">**2**</span><span class="sxs-lookup"><span data-stu-id="dfd52-213">**2**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-214">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="dfd52-214">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-215">**3**</span><span class="sxs-lookup"><span data-stu-id="dfd52-215">**3**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-216">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-216">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-217">**4**</span><span class="sxs-lookup"><span data-stu-id="dfd52-217">**4**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-218">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-218">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-219">**5**</span><span class="sxs-lookup"><span data-stu-id="dfd52-219">**5**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-220">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio (proprietà di **stato** della classe [**\_ BaseService Win32**](/windows/desktop/CIMWin32Prov/win32-baseservice) ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="dfd52-220">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-221">**6**</span><span class="sxs-lookup"><span data-stu-id="dfd52-221">**6**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-222">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="dfd52-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-223">**7**</span><span class="sxs-lookup"><span data-stu-id="dfd52-223">**7**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-224">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-224">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-225">**8**</span><span class="sxs-lookup"><span data-stu-id="dfd52-225">**8**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-226">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-226">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-227">**9**</span><span class="sxs-lookup"><span data-stu-id="dfd52-227">**9**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-228">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-228">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-229">**10**</span><span class="sxs-lookup"><span data-stu-id="dfd52-229">**10**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-230">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dfd52-230">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-231">**11**</span><span class="sxs-lookup"><span data-stu-id="dfd52-231">**11**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-232">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="dfd52-232">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-233">**12**</span><span class="sxs-lookup"><span data-stu-id="dfd52-233">**12**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-234">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="dfd52-234">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-235">**13**</span><span class="sxs-lookup"><span data-stu-id="dfd52-235">**13**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-236">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="dfd52-236">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-237">**14**</span><span class="sxs-lookup"><span data-stu-id="dfd52-237">**14**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-238">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="dfd52-238">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-239">**15**</span><span class="sxs-lookup"><span data-stu-id="dfd52-239">**15**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-240">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="dfd52-240">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-241">**16**</span><span class="sxs-lookup"><span data-stu-id="dfd52-241">**16**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-242">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="dfd52-242">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-243">**17**</span><span class="sxs-lookup"><span data-stu-id="dfd52-243">**17**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-244">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dfd52-244">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-245">**18**</span><span class="sxs-lookup"><span data-stu-id="dfd52-245">**18**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-246">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-246">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-247">**19**</span><span class="sxs-lookup"><span data-stu-id="dfd52-247">**19**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-248">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="dfd52-248">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-249">**20**</span><span class="sxs-lookup"><span data-stu-id="dfd52-249">**20**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-250">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="dfd52-250">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-251">**21**</span><span class="sxs-lookup"><span data-stu-id="dfd52-251">**21**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-252">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-252">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-253">**22**</span><span class="sxs-lookup"><span data-stu-id="dfd52-253">**22**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-254">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-254">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-255">**23**</span><span class="sxs-lookup"><span data-stu-id="dfd52-255">**23**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-256">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="dfd52-256">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dfd52-257">**24**</span><span class="sxs-lookup"><span data-stu-id="dfd52-257">**24**</span></span>
</dt> <dd>

<span data-ttu-id="dfd52-258">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="dfd52-258">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfd52-259">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfd52-259">Remarks</span></span>

<span data-ttu-id="dfd52-260">I servizi vengono in genere installati in uno dei due modi seguenti: come parte dell'installazione del sistema operativo o mediante un programma di installazione fornito dallo sviluppatore del servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-260">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="dfd52-261">Tuttavia, alcuni servizi, in particolare quelli creati internamente, potrebbero non avere un programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="dfd52-261">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="dfd52-262">In questi casi, è possibile usare il metodo **create** per installare i servizi a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="dfd52-262">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="dfd52-263">Nonostante il nome, il metodo create non crea effettivamente un servizio. viene semplicemente installato un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="dfd52-263">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="dfd52-264">Per usare questo comando, è necessario copiare il file eseguibile del servizio in un computer e quindi usare **Crea** per installare il servizio.</span><span class="sxs-lookup"><span data-stu-id="dfd52-264">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="dfd52-265">Il metodo **create** è simile al metodo [**Change**](win32-terminalservice-change.md) .</span><span class="sxs-lookup"><span data-stu-id="dfd52-265">The **Create** method is similar to the [**Change**](win32-terminalservice-change.md) method.</span></span> <span data-ttu-id="dfd52-266">In entrambi i casi, le proprietà del servizio vengono passate come parametri al metodo.</span><span class="sxs-lookup"><span data-stu-id="dfd52-266">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="dfd52-267">Come per i parametri usati con il metodo **Change** , l'ordine in cui vengono passati questi parametri è molto importante.</span><span class="sxs-lookup"><span data-stu-id="dfd52-267">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="dfd52-268">Il parametro *LoadOrderGroup* rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dfd52-268">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="dfd52-269">I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento, in quanto i servizi sono dipendenti tra loro.</span><span class="sxs-lookup"><span data-stu-id="dfd52-269">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="dfd52-270">Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi precedenti.</span><span class="sxs-lookup"><span data-stu-id="dfd52-270">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd52-271">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfd52-271">Requirements</span></span>



| <span data-ttu-id="dfd52-272">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfd52-272">Requirement</span></span> | <span data-ttu-id="dfd52-273">Valore</span><span class="sxs-lookup"><span data-stu-id="dfd52-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd52-274">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfd52-274">Minimum supported client</span></span><br/> | <span data-ttu-id="dfd52-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfd52-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dfd52-276">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfd52-276">Minimum supported server</span></span><br/> | <span data-ttu-id="dfd52-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfd52-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dfd52-278">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dfd52-278">Namespace</span></span><br/>                | <span data-ttu-id="dfd52-279">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="dfd52-279">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="dfd52-280">MOF</span><span class="sxs-lookup"><span data-stu-id="dfd52-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfd52-281"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfd52-281"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfd52-282">DLL</span><span class="sxs-lookup"><span data-stu-id="dfd52-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfd52-283"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfd52-283"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfd52-284">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfd52-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd52-285">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="dfd52-285">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="dfd52-286">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="dfd52-286">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="dfd52-287">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="dfd52-287">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="dfd52-288">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="dfd52-288">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

