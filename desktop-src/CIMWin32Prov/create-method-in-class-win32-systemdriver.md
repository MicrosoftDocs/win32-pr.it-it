---
description: Crea un nuovo servizio gestito dal driver di sistema.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4ae14243582ea1239e8cc68c1e1d5464339a45b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127763"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="76acc-103">Metodo Create della classe Win32 \_ SystemDriver</span><span class="sxs-lookup"><span data-stu-id="76acc-103">Create method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="76acc-104">Il metodo **create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuovo servizio gestito dal driver di sistema.</span><span class="sxs-lookup"><span data-stu-id="76acc-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service managed by the system driver.</span></span> <span data-ttu-id="76acc-105">Il parametro *Win32 \_ LoadOrderGroup* rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="76acc-105">The *Win32\_LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="76acc-106">I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento, in quanto i servizi sono dipendenti tra loro.</span><span class="sxs-lookup"><span data-stu-id="76acc-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="76acc-107">Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi precedenti.</span><span class="sxs-lookup"><span data-stu-id="76acc-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="76acc-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="76acc-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="76acc-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="76acc-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="76acc-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76acc-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="76acc-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="76acc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76acc-112">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-113">Nome del servizio da installare nel metodo **create** .</span><span class="sxs-lookup"><span data-stu-id="76acc-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="76acc-114">La lunghezza massima della stringa è 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="76acc-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="76acc-115">Il database di gestione controllo servizi conserva la distinzione tra maiuscole e minuscole dei caratteri, ma i confronti tra nomi di servizio non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="76acc-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="76acc-116">Le barre (/) e le barre rovesciate doppie ( \\ ) non sono caratteri validi per il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="76acc-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="76acc-117">*DisplayName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-118">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="76acc-118">Display name of the service.</span></span> <span data-ttu-id="76acc-119">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="76acc-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="76acc-120">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="76acc-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="76acc-121">I confronti *DisplayName* sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="76acc-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="76acc-122">Constraints: accetta lo stesso valore del parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="76acc-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="76acc-123">Esempio: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="76acc-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="76acc-124">*Nome percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-125">Percorso completo del file eseguibile che implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="76acc-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="76acc-126">Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="76acc-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="76acc-127">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-128">Tipo di servizi forniti ai processi che li chiamano.</span><span class="sxs-lookup"><span data-stu-id="76acc-128">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="76acc-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="76acc-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="76acc-130">Driver del kernel</span><span class="sxs-lookup"><span data-stu-id="76acc-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="76acc-131">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="76acc-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="76acc-132">Driver del file System</span><span class="sxs-lookup"><span data-stu-id="76acc-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="76acc-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="76acc-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="76acc-134">Adattatore</span><span class="sxs-lookup"><span data-stu-id="76acc-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="76acc-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="76acc-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="76acc-136">Driver di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="76acc-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="76acc-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="76acc-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="76acc-138">Processo personale</span><span class="sxs-lookup"><span data-stu-id="76acc-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="76acc-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="76acc-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="76acc-140">Condividi processo</span><span class="sxs-lookup"><span data-stu-id="76acc-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="76acc-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="76acc-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="76acc-142">Processo interattivo</span><span class="sxs-lookup"><span data-stu-id="76acc-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="76acc-143">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-144">Gravità dell'errore se non è possibile avviare il metodo **create** .</span><span class="sxs-lookup"><span data-stu-id="76acc-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="76acc-145">Questo valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="76acc-145">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="76acc-146">Tutti gli errori vengono registrati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="76acc-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="76acc-147">0</span><span class="sxs-lookup"><span data-stu-id="76acc-147">0</span></span>
</dt> <dd>

<span data-ttu-id="76acc-148">Ignorare</span><span class="sxs-lookup"><span data-stu-id="76acc-148">"Ignore"</span></span>

<span data-ttu-id="76acc-149">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="76acc-149">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="76acc-150">1</span><span class="sxs-lookup"><span data-stu-id="76acc-150">1</span></span>
</dt> <dd>

<span data-ttu-id="76acc-151">"Normal"</span><span class="sxs-lookup"><span data-stu-id="76acc-151">"Normal"</span></span>

<span data-ttu-id="76acc-152">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="76acc-152">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="76acc-153">2</span><span class="sxs-lookup"><span data-stu-id="76acc-153">2</span></span>
</dt> <dd>

<span data-ttu-id="76acc-154">Grave</span><span class="sxs-lookup"><span data-stu-id="76acc-154">"Severe"</span></span>

<span data-ttu-id="76acc-155">Il sistema viene riavviato con l'ultima configurazione valida nota.</span><span class="sxs-lookup"><span data-stu-id="76acc-155">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="76acc-156">3</span><span class="sxs-lookup"><span data-stu-id="76acc-156">3</span></span>
</dt> <dd>

<span data-ttu-id="76acc-157">Critico</span><span class="sxs-lookup"><span data-stu-id="76acc-157">"Critical"</span></span>

<span data-ttu-id="76acc-158">Il sistema tenta di iniziare con una configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="76acc-158">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="76acc-159">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-159">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-160">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="76acc-160">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="76acc-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span><span class="sxs-lookup"><span data-stu-id="76acc-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="76acc-162">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="76acc-162">Device driver started by the operating system loader.</span></span> <span data-ttu-id="76acc-163">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="76acc-163">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="76acc-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema**</span><span class="sxs-lookup"><span data-stu-id="76acc-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="76acc-165">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="76acc-165">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="76acc-166">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="76acc-166">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="76acc-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatico**</span><span class="sxs-lookup"><span data-stu-id="76acc-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="76acc-168">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="76acc-168">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="76acc-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale**</span><span class="sxs-lookup"><span data-stu-id="76acc-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="76acc-170">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="76acc-170">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="76acc-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato**</span><span class="sxs-lookup"><span data-stu-id="76acc-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="76acc-172">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="76acc-172">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="76acc-173">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-173">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-174">Se **true**, il servizio può creare o comunicare con le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="76acc-174">If **true**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="76acc-175">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-175">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-176">Nome dell'account con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="76acc-176">Account name under which the service runs.</span></span> <span data-ttu-id="76acc-177">A seconda del tipo di servizio, il nome dell'account può essere nel formato DomainName \\ username o nome dell'entità utente (UPN) Username@DomainName .</span><span class="sxs-lookup"><span data-stu-id="76acc-177">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="76acc-178">Il processo del servizio viene registrato utilizzando una di queste due forme durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="76acc-178">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="76acc-179">Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente.</span><span class="sxs-lookup"><span data-stu-id="76acc-179">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="76acc-180">Se viene specificato **null** , il servizio viene connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="76acc-180">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="76acc-181">Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto driver, ovvero \\ filesystem \\ RDR o \\ driver XNS, \\ usato dal sistema di input e output (i/O) per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76acc-181">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="76acc-182">Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="76acc-182">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="76acc-183">Esempio: amministratore di DWDOM \\</span><span class="sxs-lookup"><span data-stu-id="76acc-183">Example: DWDOM\\Admin</span></span>

</dd> <dt>

<span data-ttu-id="76acc-184">*StartPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-184">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-185">Password per il nome dell'account specificato dal parametro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="76acc-185">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="76acc-186">Specificare **null** se non si sta modificando la password.</span><span class="sxs-lookup"><span data-stu-id="76acc-186">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="76acc-187">Specificare una stringa vuota se il servizio non dispone di password.</span><span class="sxs-lookup"><span data-stu-id="76acc-187">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="76acc-188">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-188">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-189">Nome del gruppo associato al nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="76acc-189">Group name associated with the new service.</span></span> <span data-ttu-id="76acc-190">I gruppi dell'ordine di caricamento sono contenuti nel registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="76acc-190">Load order groups are contained in the registry and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="76acc-191">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non appartiene a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="76acc-191">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="76acc-192">Le dipendenze tra i gruppi devono essere elencate nel parametro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="76acc-192">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="76acc-193">I servizi nell'elenco di gruppi per l'ordine di caricamento vengono avviati per primi, seguiti da servizi nei gruppi non inclusi nell'elenco del gruppo di ordini di carico, seguiti da servizi che non appartengono a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="76acc-193">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="76acc-194">Nel registro di sistema è presente un elenco di gruppi di ordini di carico disponibili in:</span><span class="sxs-lookup"><span data-stu-id="76acc-194">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="76acc-195">**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="76acc-195">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="76acc-196">*LoadOrderGroupDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-196">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-197">Matrice di gruppi di ordini di caricamento che devono iniziare prima del servizio.</span><span class="sxs-lookup"><span data-stu-id="76acc-197">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="76acc-198">Ogni elemento nella matrice è delimitato da **null** e l'elenco viene terminato da due valori **null** .</span><span class="sxs-lookup"><span data-stu-id="76acc-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="76acc-199">In Visual Basic o script è possibile passare un vbArray.</span><span class="sxs-lookup"><span data-stu-id="76acc-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="76acc-200">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="76acc-200">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="76acc-201">I nomi dei gruppi devono essere preceduti **dall' \_ \_ identificatore del gruppo SC** (definito nel file winsvc. h) per distinguerlo dal nome del servizio, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="76acc-201">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="76acc-202">La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="76acc-202">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="76acc-203">*ServiceDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76acc-203">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76acc-204">Matrice che contiene i nomi dei servizi che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="76acc-204">An array that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="76acc-205">Ogni elemento nella matrice è delimitato da **null** e l'elenco viene terminato da due valori **null** .</span><span class="sxs-lookup"><span data-stu-id="76acc-205">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="76acc-206">In Visual Basic o script è possibile passare un vbArray.</span><span class="sxs-lookup"><span data-stu-id="76acc-206">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="76acc-207">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="76acc-207">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="76acc-208">La dipendenza da un servizio significa che questo servizio può essere eseguito solo se è in esecuzione il servizio da cui dipende.</span><span class="sxs-lookup"><span data-stu-id="76acc-208">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76acc-209">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76acc-209">Return value</span></span>

<span data-ttu-id="76acc-210">Restituisce un valore pari a 0 (zero) se il servizio è stato creato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="76acc-210">Returns a value of 0 (zero) if the service was successfully created, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="76acc-211">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76acc-211">Requirements</span></span>



| <span data-ttu-id="76acc-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="76acc-212">Requirement</span></span> | <span data-ttu-id="76acc-213">Valore</span><span class="sxs-lookup"><span data-stu-id="76acc-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76acc-214">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76acc-214">Minimum supported client</span></span><br/> | <span data-ttu-id="76acc-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76acc-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="76acc-216">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76acc-216">Minimum supported server</span></span><br/> | <span data-ttu-id="76acc-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76acc-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="76acc-218">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="76acc-218">Namespace</span></span><br/>                | <span data-ttu-id="76acc-219">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="76acc-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="76acc-220">MOF</span><span class="sxs-lookup"><span data-stu-id="76acc-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76acc-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76acc-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="76acc-222">DLL</span><span class="sxs-lookup"><span data-stu-id="76acc-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76acc-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76acc-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76acc-224">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76acc-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="76acc-225">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76acc-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="76acc-226">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="76acc-226">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

