---
description: Crea un nuovo servizio di sistema.
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
ms.openlocfilehash: 6f23bc2a5c49a85a20765172d4c5d361a8d18316
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749039"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="5b620-103">Metodo Create della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="5b620-103">Create method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="5b620-104">Il metodo **create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuovo servizio di sistema.</span><span class="sxs-lookup"><span data-stu-id="5b620-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="5b620-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5b620-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5b620-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5b620-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b620-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b620-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5b620-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b620-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b620-109">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-110">Nome del servizio da installare nel metodo **create** .</span><span class="sxs-lookup"><span data-stu-id="5b620-110">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="5b620-111">La lunghezza massima della stringa è 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5b620-111">The maximum string length is 256 characters.</span></span> <span data-ttu-id="5b620-112">Il database di gestione controllo servizi conserva la distinzione tra maiuscole e minuscole dei caratteri, ma i confronti tra nomi di servizio non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5b620-112">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="5b620-113">Le barre (/) e le barre rovesciate doppie ( \\ ) non sono caratteri validi per il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-113">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-114">*DisplayName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-114">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-115">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-115">Display name of the service.</span></span> <span data-ttu-id="5b620-116">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5b620-116">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="5b620-117">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="5b620-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="5b620-118">I confronti *DisplayName* sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5b620-118">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="5b620-119">Constraints: accetta lo stesso valore del parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="5b620-119">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="5b620-120">Esempio: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="5b620-120">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="5b620-121">*Nome percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-121">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-122">Percorso completo del file eseguibile che implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-122">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="5b620-123">Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="5b620-123">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="5b620-124">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-124">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-125">Tipo di servizi forniti ai processi che li chiamano.</span><span class="sxs-lookup"><span data-stu-id="5b620-125">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="5b620-126">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="5b620-126">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="5b620-127">Driver del kernel</span><span class="sxs-lookup"><span data-stu-id="5b620-127">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="5b620-128">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="5b620-128">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="5b620-129">Driver del file System</span><span class="sxs-lookup"><span data-stu-id="5b620-129">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="5b620-130">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="5b620-130">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="5b620-131">Adattatore</span><span class="sxs-lookup"><span data-stu-id="5b620-131">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="5b620-132">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="5b620-132">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="5b620-133">Driver di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="5b620-133">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="5b620-134">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="5b620-134">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="5b620-135">Processo personale</span><span class="sxs-lookup"><span data-stu-id="5b620-135">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="5b620-136">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="5b620-136">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="5b620-137">Condividi processo</span><span class="sxs-lookup"><span data-stu-id="5b620-137">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="5b620-138">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="5b620-138">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="5b620-139">Processo interattivo</span><span class="sxs-lookup"><span data-stu-id="5b620-139">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5b620-140">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-140">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-141">Gravità dell'errore se non è possibile avviare il metodo **create** .</span><span class="sxs-lookup"><span data-stu-id="5b620-141">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="5b620-142">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="5b620-142">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="5b620-143">Tutti gli errori vengono registrati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="5b620-143">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="5b620-144">0</span><span class="sxs-lookup"><span data-stu-id="5b620-144">0</span></span>
</dt> <dd>

<span data-ttu-id="5b620-145">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="5b620-145">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-146">1</span><span class="sxs-lookup"><span data-stu-id="5b620-146">1</span></span>
</dt> <dd>

<span data-ttu-id="5b620-147">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="5b620-147">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-148">2</span><span class="sxs-lookup"><span data-stu-id="5b620-148">2</span></span>
</dt> <dd>

<span data-ttu-id="5b620-149">Il sistema viene riavviato con l'ultima configurazione valida nota.</span><span class="sxs-lookup"><span data-stu-id="5b620-149">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-150">3</span><span class="sxs-lookup"><span data-stu-id="5b620-150">3</span></span>
</dt> <dd>

<span data-ttu-id="5b620-151">Il sistema tenta di iniziare con una configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="5b620-151">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5b620-152">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-152">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-153">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="5b620-153">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="5b620-154">Avvio</span><span class="sxs-lookup"><span data-stu-id="5b620-154">Boot</span></span>
</dt> <dd>

<span data-ttu-id="5b620-155">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5b620-155">Device driver started by the operating system loader.</span></span> <span data-ttu-id="5b620-156">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="5b620-156">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-157">Sistema</span><span class="sxs-lookup"><span data-stu-id="5b620-157">System</span></span>
</dt> <dd>

<span data-ttu-id="5b620-158">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5b620-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="5b620-159">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="5b620-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-160">Automatico</span><span class="sxs-lookup"><span data-stu-id="5b620-160">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="5b620-161">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="5b620-161">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-162">Manuale</span><span class="sxs-lookup"><span data-stu-id="5b620-162">Manual</span></span>
</dt> <dd>

<span data-ttu-id="5b620-163">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="5b620-163">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-164">Disabled</span><span class="sxs-lookup"><span data-stu-id="5b620-164">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="5b620-165">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="5b620-165">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5b620-166">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-167">Se **true**, il servizio può creare o comunicare con Windows sul desktop.</span><span class="sxs-lookup"><span data-stu-id="5b620-167">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-168">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-169">Nome dell'account con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-169">Account name under which the service runs.</span></span> <span data-ttu-id="5b620-170">A seconda del tipo di servizio, il nome dell'account può essere nel formato DomainName \\ username o nome dell'entità utente (UPN) Username@DomainName .</span><span class="sxs-lookup"><span data-stu-id="5b620-170">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="5b620-171">Il processo del servizio viene registrato utilizzando una di queste due forme durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5b620-171">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="5b620-172">Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente.</span><span class="sxs-lookup"><span data-stu-id="5b620-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="5b620-173">Se viene specificato **null** , il servizio viene connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="5b620-173">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="5b620-174">Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto driver (ovvero \\ filesystem \\ RDR o \\ driver \\ XNS) utilizzato dal sistema di input e output (i/O) per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b620-174">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="5b620-175">Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-175">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="5b620-176">Esempio: amministratore di DWDOM \\ .</span><span class="sxs-lookup"><span data-stu-id="5b620-176">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-177">*StartPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-178">Password per il nome dell'account specificato dal parametro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="5b620-178">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="5b620-179">Specificare **null** se non si sta modificando la password.</span><span class="sxs-lookup"><span data-stu-id="5b620-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="5b620-180">Specificare una stringa vuota se il servizio non dispone di password.</span><span class="sxs-lookup"><span data-stu-id="5b620-180">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-181">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-181">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-182">Nome del gruppo associato al nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-182">Group name associated with the new service.</span></span> <span data-ttu-id="5b620-183">I gruppi dell'ordine di caricamento sono contenuti nel registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5b620-183">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="5b620-184">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non appartiene a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b620-184">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="5b620-185">Le dipendenze tra i gruppi devono essere elencate nel parametro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="5b620-185">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="5b620-186">I servizi nell'elenco di gruppi per l'ordine di caricamento vengono avviati per primi, seguiti da servizi nei gruppi non inclusi nell'elenco del gruppo di ordini di carico, seguiti da servizi che non appartengono a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b620-186">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="5b620-187">Nel registro di sistema è presente un elenco di gruppi di ordini di carico disponibili in:</span><span class="sxs-lookup"><span data-stu-id="5b620-187">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="5b620-188">**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="5b620-188">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="5b620-189">*LoadOrderGroupDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-189">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-190">Matrice di gruppi di ordini di caricamento che devono iniziare prima del servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-190">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="5b620-191">Ogni elemento nella matrice è delimitato da **null** e l'elenco viene terminato da due valori **null** .</span><span class="sxs-lookup"><span data-stu-id="5b620-191">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="5b620-192">In Visual Basic o script è possibile passare un vbArray.</span><span class="sxs-lookup"><span data-stu-id="5b620-192">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="5b620-193">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="5b620-193">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="5b620-194">I nomi dei gruppi devono essere preceduti **dall' \_ \_ identificatore del gruppo SC** (definito nel file winsvc. h) per distinguerlo dal nome del servizio, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5b620-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="5b620-195">La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b620-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-196">*ServiceDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b620-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b620-197">Matrice che contiene i nomi dei servizi che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-197">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="5b620-198">Ogni elemento nella matrice è delimitato da **null** e l'elenco viene terminato da due valori **null** .</span><span class="sxs-lookup"><span data-stu-id="5b620-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="5b620-199">In Visual Basic o script è possibile passare un vbArray.</span><span class="sxs-lookup"><span data-stu-id="5b620-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="5b620-200">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="5b620-200">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="5b620-201">La dipendenza da un servizio significa che questo servizio può essere eseguito solo se è in esecuzione il servizio da cui dipende.</span><span class="sxs-lookup"><span data-stu-id="5b620-201">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b620-202">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b620-202">Return value</span></span>

<span data-ttu-id="5b620-203">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="5b620-203">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="5b620-204">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5b620-204">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5b620-205">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5b620-205">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5b620-206">**0**</span><span class="sxs-lookup"><span data-stu-id="5b620-206">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-207">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="5b620-207">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-208">**1**</span><span class="sxs-lookup"><span data-stu-id="5b620-208">**1**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-209">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="5b620-209">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-210">**2**</span><span class="sxs-lookup"><span data-stu-id="5b620-210">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-211">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="5b620-211">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-212">**3**</span><span class="sxs-lookup"><span data-stu-id="5b620-212">**3**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-213">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-214">**4**</span><span class="sxs-lookup"><span data-stu-id="5b620-214">**4**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-215">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-215">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-216">**5**</span><span class="sxs-lookup"><span data-stu-id="5b620-216">**5**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-217">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio (proprietà di **stato** della classe [**\_ BaseService Win32**](win32-baseservice.md) ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="5b620-217">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](win32-baseservice.md) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-218">**6**</span><span class="sxs-lookup"><span data-stu-id="5b620-218">**6**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-219">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="5b620-219">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-220">**7**</span><span class="sxs-lookup"><span data-stu-id="5b620-220">**7**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-221">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="5b620-221">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-222">**8**</span><span class="sxs-lookup"><span data-stu-id="5b620-222">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-223">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-223">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-224">**9**</span><span class="sxs-lookup"><span data-stu-id="5b620-224">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-225">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-225">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-226">**10**</span><span class="sxs-lookup"><span data-stu-id="5b620-226">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-227">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5b620-227">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-228">**11**</span><span class="sxs-lookup"><span data-stu-id="5b620-228">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-229">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="5b620-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-230">**12**</span><span class="sxs-lookup"><span data-stu-id="5b620-230">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-231">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="5b620-231">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-232">**13**</span><span class="sxs-lookup"><span data-stu-id="5b620-232">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-233">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="5b620-233">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-234">**14**</span><span class="sxs-lookup"><span data-stu-id="5b620-234">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-235">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="5b620-235">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-236">**15**</span><span class="sxs-lookup"><span data-stu-id="5b620-236">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-237">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5b620-237">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-238">**16**</span><span class="sxs-lookup"><span data-stu-id="5b620-238">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-239">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="5b620-239">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-240">**17**</span><span class="sxs-lookup"><span data-stu-id="5b620-240">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-241">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5b620-241">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-242">**18**</span><span class="sxs-lookup"><span data-stu-id="5b620-242">**18**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-243">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="5b620-243">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-244">**19**</span><span class="sxs-lookup"><span data-stu-id="5b620-244">**19**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-245">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="5b620-245">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-246">**20**</span><span class="sxs-lookup"><span data-stu-id="5b620-246">**20**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-247">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="5b620-247">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-248">**21**</span><span class="sxs-lookup"><span data-stu-id="5b620-248">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-249">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-249">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-250">**22**</span><span class="sxs-lookup"><span data-stu-id="5b620-250">**22**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-251">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-251">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-252">**23**</span><span class="sxs-lookup"><span data-stu-id="5b620-252">**23**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-253">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="5b620-253">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5b620-254">**24**</span><span class="sxs-lookup"><span data-stu-id="5b620-254">**24**</span></span>
</dt> <dd>

<span data-ttu-id="5b620-255">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5b620-255">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b620-256">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b620-256">Remarks</span></span>

<span data-ttu-id="5b620-257">I servizi vengono in genere installati in uno dei due modi seguenti: come parte dell'installazione del sistema operativo o mediante un programma di installazione fornito dallo sviluppatore del servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-257">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="5b620-258">Tuttavia, alcuni servizi, in particolare quelli creati internamente, potrebbero non avere un programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="5b620-258">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="5b620-259">In questi casi, è possibile usare il metodo **create** per installare i servizi a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="5b620-259">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="5b620-260">Nonostante il nome, il metodo create non crea effettivamente un servizio. viene semplicemente installato un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="5b620-260">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="5b620-261">Per usare questo comando, è necessario copiare il file eseguibile del servizio in un computer e quindi usare **Crea** per installare il servizio.</span><span class="sxs-lookup"><span data-stu-id="5b620-261">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="5b620-262">Il metodo **create** è simile al metodo [**Change**](change-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="5b620-262">The **Create** method is similar to the [**Change**](change-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="5b620-263">In entrambi i casi, le proprietà del servizio vengono passate come parametri al metodo.</span><span class="sxs-lookup"><span data-stu-id="5b620-263">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="5b620-264">Come per i parametri usati con il metodo **Change** , l'ordine in cui vengono passati questi parametri è molto importante.</span><span class="sxs-lookup"><span data-stu-id="5b620-264">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="5b620-265">Il parametro *LoadOrderGroup* rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5b620-265">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="5b620-266">I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento, in quanto i servizi sono dipendenti tra loro.</span><span class="sxs-lookup"><span data-stu-id="5b620-266">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="5b620-267">Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi precedenti.</span><span class="sxs-lookup"><span data-stu-id="5b620-267">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="5b620-268">Esempio</span><span class="sxs-lookup"><span data-stu-id="5b620-268">Examples</span></span>

<span data-ttu-id="5b620-269">Il codice VBScript seguente consente di installare un servizio denominato DbService</span><span class="sxs-lookup"><span data-stu-id="5b620-269">The following VBScript installs a service named DbService</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5b620-270">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b620-270">Requirements</span></span>



| <span data-ttu-id="5b620-271">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b620-271">Requirement</span></span> | <span data-ttu-id="5b620-272">Valore</span><span class="sxs-lookup"><span data-stu-id="5b620-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b620-273">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b620-273">Minimum supported client</span></span><br/> | <span data-ttu-id="5b620-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b620-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b620-275">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b620-275">Minimum supported server</span></span><br/> | <span data-ttu-id="5b620-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b620-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b620-277">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5b620-277">Namespace</span></span><br/>                | <span data-ttu-id="5b620-278">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5b620-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5b620-279">MOF</span><span class="sxs-lookup"><span data-stu-id="5b620-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b620-280"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b620-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b620-281">DLL</span><span class="sxs-lookup"><span data-stu-id="5b620-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b620-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b620-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b620-283">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b620-283">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b620-284">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5b620-284">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5b620-285">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="5b620-285">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="5b620-286">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="5b620-286">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

