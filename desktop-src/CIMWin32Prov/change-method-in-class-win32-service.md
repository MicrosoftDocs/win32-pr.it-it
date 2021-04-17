---
description: Modifica un \_ servizio Win32.
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: Metodo Change della classe Win32_Service (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 321b27239114fc86861c0360d507db6c8c520a9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523922"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a><span data-ttu-id="1b685-103">Metodo Change della classe Win32_Service (Mbnapi. h)</span><span class="sxs-lookup"><span data-stu-id="1b685-103">Change method of the Win32_Service class (Mbnapi.h)</span></span>

<span data-ttu-id="1b685-104">Il metodo **modifica** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifica un [**\_ servizio Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="1b685-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="1b685-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="1b685-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1b685-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1b685-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b685-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b685-107">Syntax</span></span>


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="1b685-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b685-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b685-109">*DisplayName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b685-109">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b685-110">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-110">The display name of the service.</span></span> <span data-ttu-id="1b685-111">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1b685-111">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="1b685-112">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="1b685-112">The name is case- preserved in the service control manager.</span></span> <span data-ttu-id="1b685-113">I confronti *DisplayName* sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1b685-113">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="1b685-114">Constraints: accetta lo stesso valore della proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="1b685-114">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="1b685-115">Esempio, "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="1b685-115">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="1b685-116">*Nome percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b685-116">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b685-117">Percorso completo del file eseguibile che implementa il servizio, ad esempio " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="1b685-117">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="1b685-118">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b685-118">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b685-119">Tipo di servizi forniti ai processi che li chiamano.</span><span class="sxs-lookup"><span data-stu-id="1b685-119">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="1b685-120">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1b685-120">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="1b685-121">Driver del kernel</span><span class="sxs-lookup"><span data-stu-id="1b685-121">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="1b685-122">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="1b685-122">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="1b685-123">Driver del file System</span><span class="sxs-lookup"><span data-stu-id="1b685-123">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="1b685-124">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="1b685-124">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="1b685-125">Adattatore</span><span class="sxs-lookup"><span data-stu-id="1b685-125">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="1b685-126">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="1b685-126">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="1b685-127">Driver di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="1b685-127">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="1b685-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="1b685-128">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="1b685-129">Processo personale</span><span class="sxs-lookup"><span data-stu-id="1b685-129">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="1b685-130">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="1b685-130">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="1b685-131">Condividi processo</span><span class="sxs-lookup"><span data-stu-id="1b685-131">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="1b685-132">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="1b685-132">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="1b685-133">Processo interattivo</span><span class="sxs-lookup"><span data-stu-id="1b685-133">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1b685-134">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b685-134">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b685-135">Gravità dell'errore se il servizio non viene avviato durante l'avvio.</span><span class="sxs-lookup"><span data-stu-id="1b685-135">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="1b685-136">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="1b685-136">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="1b685-137">Tutti gli errori vengono registrati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1b685-137">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="1b685-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** (0)</span><span class="sxs-lookup"><span data-stu-id="1b685-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1b685-139">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="1b685-139">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="1b685-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** (1)</span><span class="sxs-lookup"><span data-stu-id="1b685-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1b685-141">Normale.</span><span class="sxs-lookup"><span data-stu-id="1b685-141">Normal.</span></span> <span data-ttu-id="1b685-142">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="1b685-142">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="1b685-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)</span><span class="sxs-lookup"><span data-stu-id="1b685-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1b685-144">Il sistema viene riavviato con l'ultima configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="1b685-144">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="1b685-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (3)</span><span class="sxs-lookup"><span data-stu-id="1b685-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1b685-146">Il sistema tenta un riavvio con una configurazione valida.</span><span class="sxs-lookup"><span data-stu-id="1b685-146">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1b685-147">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b685-147">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b685-148">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="1b685-148">Start mode of the Windows base service.</span></span> <span data-ttu-id="1b685-149">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1b685-149">For more information, see the Remarks section.</span></span>

<dt>

<span data-ttu-id="1b685-150">Avvio</span><span class="sxs-lookup"><span data-stu-id="1b685-150">Boot</span></span>
</dt> <dd>

<span data-ttu-id="1b685-151">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1b685-151">Device driver started by the operating system loader.</span></span> <span data-ttu-id="1b685-152">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="1b685-152">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-153">Sistema</span><span class="sxs-lookup"><span data-stu-id="1b685-153">System</span></span>
</dt> <dd>

<span data-ttu-id="1b685-154">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1b685-154">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="1b685-155">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="1b685-155">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-156">Automatico</span><span class="sxs-lookup"><span data-stu-id="1b685-156">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="1b685-157">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="1b685-157">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-158">Manuale</span><span class="sxs-lookup"><span data-stu-id="1b685-158">Manual</span></span>
</dt> <dd>

<span data-ttu-id="1b685-159">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="1b685-159">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-160">Disabled</span><span class="sxs-lookup"><span data-stu-id="1b685-160">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="1b685-161">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="1b685-161">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1b685-162">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b685-162">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b685-163">Se **true**, il servizio può creare o comunicare con una finestra sul desktop.</span><span class="sxs-lookup"><span data-stu-id="1b685-163">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-164">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b685-164">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b685-165">Nome dell'account con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-165">Account name the service runs under.</span></span> <span data-ttu-id="1b685-166">A seconda del tipo di servizio, il nome dell'account può essere nel formato DomainName \\ username o. \\ Nome utente.</span><span class="sxs-lookup"><span data-stu-id="1b685-166">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="1b685-167">Il processo del servizio verrà registrato utilizzando una di queste due forme durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1b685-167">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="1b685-168">Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente.</span><span class="sxs-lookup"><span data-stu-id="1b685-168">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="1b685-169">Se viene specificato **null** , il servizio verrà connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="1b685-169">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="1b685-170">Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto del driver (ovvero, \\ filesystem \\ RDR o \\ driver \\ XNS) usato dal sistema di input e output (i/O) per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b685-170">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="1b685-171">Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio, ad esempio "DWDOM \\ admin".</span><span class="sxs-lookup"><span data-stu-id="1b685-171">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="1b685-172">È anche possibile usare il formato del nome dell'entità utente (UPN) per specificare il nome **iniziale**, ad esempio *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="1b685-172">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-173">*StartPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b685-173">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b685-174">Password per il nome dell'account specificato dal parametro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="1b685-174">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="1b685-175">Specificare **null** se non si sta modificando la password.</span><span class="sxs-lookup"><span data-stu-id="1b685-175">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="1b685-176">Specificare una stringa vuota se il servizio non dispone di password.</span><span class="sxs-lookup"><span data-stu-id="1b685-176">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="1b685-177">Quando si modifica un servizio da un sistema locale a una rete o da una rete a un sistema locale, *StartPassword* deve essere una stringa vuota ("") e non **null**.</span><span class="sxs-lookup"><span data-stu-id="1b685-177">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b685-178">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b685-178">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b685-179">Nome del gruppo a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="1b685-179">Group name that it is associated with.</span></span> <span data-ttu-id="1b685-180">I gruppi dell'ordine di caricamento sono contenuti nel registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1b685-180">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="1b685-181">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non appartiene a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="1b685-181">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="1b685-182">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1b685-182">For more information, see the Remarks section.</span></span>

<span data-ttu-id="1b685-183">Le dipendenze tra i gruppi devono essere elencate nel parametro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="1b685-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="1b685-184">I servizi nell'elenco di gruppi per l'ordine di caricamento vengono avviati per primi, seguiti da servizi nei gruppi non inclusi nell'elenco del gruppo di ordini di carico, seguiti da servizi che non appartengono a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="1b685-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="1b685-185">Nel registro di sistema è presente un elenco di gruppi di ordini di carico disponibili in:</span><span class="sxs-lookup"><span data-stu-id="1b685-185">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="1b685-186">**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="1b685-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="1b685-187">*LoadOrderGroupDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b685-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b685-188">Elenco di gruppi di ordini di caricamento che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-188">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="1b685-189">La matrice è con doppia terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="1b685-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="1b685-190">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="1b685-190">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="1b685-191">I nomi dei gruppi devono essere preceduti **dall' \_ \_ identificatore del gruppo SC** (definito nel file winsvc. h) per distinguerli dai nomi dei servizi, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="1b685-191">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="1b685-192">La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="1b685-192">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-193">*ServiceDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b685-193">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b685-194">Elenco contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-194">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="1b685-195">La matrice è con doppia terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="1b685-195">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="1b685-196">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="1b685-196">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="1b685-197">La dipendenza da un servizio indica che il servizio può essere eseguito solo se è in esecuzione il servizio da cui dipende.</span><span class="sxs-lookup"><span data-stu-id="1b685-197">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b685-198">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b685-198">Return value</span></span>

<span data-ttu-id="1b685-199">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="1b685-199">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="1b685-200">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1b685-200">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1b685-201">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1b685-201">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1b685-202">**Success**</span><span class="sxs-lookup"><span data-stu-id="1b685-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-203">0</span><span class="sxs-lookup"><span data-stu-id="1b685-203">0</span></span>

<span data-ttu-id="1b685-204">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="1b685-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-205">**Non supportato**</span><span class="sxs-lookup"><span data-stu-id="1b685-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-206">1</span><span class="sxs-lookup"><span data-stu-id="1b685-206">1</span></span>

<span data-ttu-id="1b685-207">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="1b685-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-208">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="1b685-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-209">2</span><span class="sxs-lookup"><span data-stu-id="1b685-209">2</span></span>

<span data-ttu-id="1b685-210">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="1b685-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-211">**Servizi dipendenti in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="1b685-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-212">3</span><span class="sxs-lookup"><span data-stu-id="1b685-212">3</span></span>

<span data-ttu-id="1b685-213">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-214">**Controllo del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="1b685-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-215">4</span><span class="sxs-lookup"><span data-stu-id="1b685-215">4</span></span>

<span data-ttu-id="1b685-216">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-217">**Il servizio non può accettare il controllo**</span><span class="sxs-lookup"><span data-stu-id="1b685-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-218">5</span><span class="sxs-lookup"><span data-stu-id="1b685-218">5</span></span>

<span data-ttu-id="1b685-219">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="1b685-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-220">**Servizio non attivo**</span><span class="sxs-lookup"><span data-stu-id="1b685-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-221">6</span><span class="sxs-lookup"><span data-stu-id="1b685-221">6</span></span>

<span data-ttu-id="1b685-222">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="1b685-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-223">**Timeout richiesta servizio**</span><span class="sxs-lookup"><span data-stu-id="1b685-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-224">7</span><span class="sxs-lookup"><span data-stu-id="1b685-224">7</span></span>

<span data-ttu-id="1b685-225">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="1b685-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-226">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="1b685-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-227">8</span><span class="sxs-lookup"><span data-stu-id="1b685-227">8</span></span>

<span data-ttu-id="1b685-228">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-228">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-229">**Percorso non trovato**</span><span class="sxs-lookup"><span data-stu-id="1b685-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-230">9</span><span class="sxs-lookup"><span data-stu-id="1b685-230">9</span></span>

<span data-ttu-id="1b685-231">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-232">**Servizio già in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="1b685-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-233">10</span><span class="sxs-lookup"><span data-stu-id="1b685-233">10</span></span>

<span data-ttu-id="1b685-234">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1b685-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-235">**Database del servizio bloccato**</span><span class="sxs-lookup"><span data-stu-id="1b685-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-236">11</span><span class="sxs-lookup"><span data-stu-id="1b685-236">11</span></span>

<span data-ttu-id="1b685-237">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="1b685-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-238">**Dipendenza servizio eliminata**</span><span class="sxs-lookup"><span data-stu-id="1b685-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-239">12</span><span class="sxs-lookup"><span data-stu-id="1b685-239">12</span></span>

<span data-ttu-id="1b685-240">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1b685-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-241">**Errore di dipendenza del servizio**</span><span class="sxs-lookup"><span data-stu-id="1b685-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-242">13</span><span class="sxs-lookup"><span data-stu-id="1b685-242">13</span></span>

<span data-ttu-id="1b685-243">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="1b685-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-244">**Servizio disabilitato**</span><span class="sxs-lookup"><span data-stu-id="1b685-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-245">14</span><span class="sxs-lookup"><span data-stu-id="1b685-245">14</span></span>

<span data-ttu-id="1b685-246">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1b685-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-247">**Accesso al servizio non riuscito**</span><span class="sxs-lookup"><span data-stu-id="1b685-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-248">15</span><span class="sxs-lookup"><span data-stu-id="1b685-248">15</span></span>

<span data-ttu-id="1b685-249">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1b685-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-250">**Servizio contrassegnato per l'eliminazione**</span><span class="sxs-lookup"><span data-stu-id="1b685-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-251">16</span><span class="sxs-lookup"><span data-stu-id="1b685-251">16</span></span>

<span data-ttu-id="1b685-252">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1b685-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-253">**Servizio senza thread**</span><span class="sxs-lookup"><span data-stu-id="1b685-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-254">17</span><span class="sxs-lookup"><span data-stu-id="1b685-254">17</span></span>

<span data-ttu-id="1b685-255">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1b685-255">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-256">**Stato dipendenza circolare**</span><span class="sxs-lookup"><span data-stu-id="1b685-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-257">18</span><span class="sxs-lookup"><span data-stu-id="1b685-257">18</span></span>

<span data-ttu-id="1b685-258">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="1b685-258">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-259">**Stato nome duplicato**</span><span class="sxs-lookup"><span data-stu-id="1b685-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-260">19</span><span class="sxs-lookup"><span data-stu-id="1b685-260">19</span></span>

<span data-ttu-id="1b685-261">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="1b685-261">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-262">**Stato nome non valido**</span><span class="sxs-lookup"><span data-stu-id="1b685-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-263">20</span><span class="sxs-lookup"><span data-stu-id="1b685-263">20</span></span>

<span data-ttu-id="1b685-264">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="1b685-264">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-265">**Stato parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="1b685-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-266">21</span><span class="sxs-lookup"><span data-stu-id="1b685-266">21</span></span>

<span data-ttu-id="1b685-267">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-268">**Stato account del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="1b685-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-269">22</span><span class="sxs-lookup"><span data-stu-id="1b685-269">22</span></span>

<span data-ttu-id="1b685-270">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-270">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-271">**Il servizio stato esiste**</span><span class="sxs-lookup"><span data-stu-id="1b685-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-272">23</span><span class="sxs-lookup"><span data-stu-id="1b685-272">23</span></span>

<span data-ttu-id="1b685-273">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1b685-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-274">**Servizio già sospeso**</span><span class="sxs-lookup"><span data-stu-id="1b685-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-275">24</span><span class="sxs-lookup"><span data-stu-id="1b685-275">24</span></span>

<span data-ttu-id="1b685-276">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1b685-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="1b685-277">**Altri**</span><span class="sxs-lookup"><span data-stu-id="1b685-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1b685-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="1b685-278">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b685-279">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b685-279">Remarks</span></span>

<span data-ttu-id="1b685-280">All'avvio di un computer, vengono avviati anche tutti i servizi di avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="1b685-280">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="1b685-281">In alcuni casi, uno di questi servizi potrebbe non riuscire a avviarsi insieme al computer.</span><span class="sxs-lookup"><span data-stu-id="1b685-281">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="1b685-282">Quando un servizio ha esito negativo durante l'avvio del sistema, il computer esegue un'azione in base al valore del codice di controllo degli errori del servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-282">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="1b685-283">la maggior parte dei servizi viene installata usando il normale codice di controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="1b685-283">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="1b685-284">Alcune eccezioni, installate con il codice di errore ignore, includono:</span><span class="sxs-lookup"><span data-stu-id="1b685-284">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="1b685-285">Servizio Replica file</span><span class="sxs-lookup"><span data-stu-id="1b685-285">File Replication Service</span></span>
-   <span data-ttu-id="1b685-286">Smart card</span><span class="sxs-lookup"><span data-stu-id="1b685-286">Smart Card</span></span>
-   <span data-ttu-id="1b685-287">Accesso secondario</span><span class="sxs-lookup"><span data-stu-id="1b685-287">Secondary Logon</span></span>
-   <span data-ttu-id="1b685-288">WMI</span><span class="sxs-lookup"><span data-stu-id="1b685-288">WMI</span></span>

<span data-ttu-id="1b685-289">Per i servizi installati con il codice di errore ignore, non viene fornita alcuna notifica all'utente che indica che il servizio non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="1b685-289">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="1b685-290">Se si preferisce una notifica sullo schermo che non è stato possibile avviare un servizio, è possibile utilizzare WMI per modificare il codice di controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="1b685-290">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="1b685-291">I codici di controllo degli errori si applicano solo all'avvio del computer; i codici di controllo degli errori non vengono utilizzati se si arresta e si tenta di riavviare un servizio dopo che il computer è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1b685-291">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="1b685-292">In alcuni casi potrebbe essere necessario modificare l'account con cui viene eseguito un determinato servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-292">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="1b685-293">Ad esempio, è possibile eseguire un servizio con un account amministrativo.</span><span class="sxs-lookup"><span data-stu-id="1b685-293">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="1b685-294">Poiché questo può creare una vulnerabilità di sicurezza, è possibile passare il servizio a un account con meno privilegi.</span><span class="sxs-lookup"><span data-stu-id="1b685-294">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="1b685-295">In alternativa, è possibile che i servizi vengano eseguiti con un account che sta per essere eliminato oppure che sia necessario assicurarsi che, in tutti i server, determinati servizi vengano eseguiti con determinati account.</span><span class="sxs-lookup"><span data-stu-id="1b685-295">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="1b685-296">È possibile utilizzare il metodo **Change** della classe [**del \_ servizio Win32**](win32-service.md) per configurare i servizi per l'esecuzione con un account utente specificato.</span><span class="sxs-lookup"><span data-stu-id="1b685-296">You can use the **Change** method of the [**Win32\_Service**](win32-service.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="1b685-297">Quando si seleziona un account, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="1b685-297">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="1b685-298">L'account usato come account del servizio deve avere il diritto di accedere come servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-298">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="1b685-299">Questo diritto può essere concesso usando Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="1b685-299">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="1b685-300">L'account utilizzato come account del servizio non deve essere un membro di un gruppo Administrators locale, di dominio o Enterprise.</span><span class="sxs-lookup"><span data-stu-id="1b685-300">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="1b685-301">Ogni istanza di un servizio deve essere eseguita con un account utente univoco.</span><span class="sxs-lookup"><span data-stu-id="1b685-301">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="1b685-302">In questo modo viene fornita una sicurezza aggiuntiva e viene abilitato il controllo delle singole istanze del servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-302">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="1b685-303">Se il servizio è interattivo, il servizio deve essere eseguito con l'account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="1b685-303">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="1b685-304">LocalSystem è necessario perché una sola finestra (WinSta0) può essere visibile e interattiva alla volta.</span><span class="sxs-lookup"><span data-stu-id="1b685-304">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="1b685-305">Se un servizio viene eseguito con un account diverso da LocalSystem, viene eseguito nel servizio-0x03E7 $ \\ Default Window Station, che è una finestra invisibile.</span><span class="sxs-lookup"><span data-stu-id="1b685-305">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="1b685-306">I servizi in esecuzione in questa finestra non possono ricevere output di input o di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1b685-306">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="1b685-307">Quando si assegna un account a un servizio, SCM richiede la password corretta per l'account prima di eseguire l'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="1b685-307">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="1b685-308">Se si fornisce una password non corretta, SCM rifiuta l'account.</span><span class="sxs-lookup"><span data-stu-id="1b685-308">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="1b685-309">Se si configura un account del servizio utilizzando l'account LocalSystem, LocalService o NetworkService, non è necessario specificare una password dell'account perché questi account non dispongono di password.</span><span class="sxs-lookup"><span data-stu-id="1b685-309">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="1b685-310">SCM archivia la password dell'account nel database dei servizi.</span><span class="sxs-lookup"><span data-stu-id="1b685-310">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="1b685-311">Dopo che la password è stata assegnata, tuttavia, SCM non garantisce che la password archiviata nel database dei servizi e la password assegnata all'account utente in Active Directory continuino a corrispondere.</span><span class="sxs-lookup"><span data-stu-id="1b685-311">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="1b685-312">Di conseguenza, potrebbe verificarsi una situazione simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="1b685-312">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="1b685-313">Configurare un servizio per l'esecuzione con un account utente specifico.</span><span class="sxs-lookup"><span data-stu-id="1b685-313">You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="1b685-314">Il servizio viene avviato con tale account utilizzando la password dell'account corrente.</span><span class="sxs-lookup"><span data-stu-id="1b685-314">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="1b685-315">Modificare la password per l'account utente.</span><span class="sxs-lookup"><span data-stu-id="1b685-315">You change the password for the user account.</span></span>
-   <span data-ttu-id="1b685-316">Il servizio continua a essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b685-316">The service continues to run.</span></span> <span data-ttu-id="1b685-317">Tuttavia, se il servizio viene arrestato, non è possibile riavviarlo perché SCM continua a usare la vecchia password non valida.</span><span class="sxs-lookup"><span data-stu-id="1b685-317">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="1b685-318">La modifica della password in Active Directory non comporta la modifica della password archiviata nel database dei servizi.</span><span class="sxs-lookup"><span data-stu-id="1b685-318">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="1b685-319">Se si eseguono servizi con account utente regolari, è necessario aggiornare le password del servizio ogni volta che viene modificata la password dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="1b685-319">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="1b685-320">Questa operazione può richiedere molto tempo se non si è certi di quali servizi sono in esecuzione con tale account o in quali computer sono in esecuzione i servizi con tale account.</span><span class="sxs-lookup"><span data-stu-id="1b685-320">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="1b685-321">Fortunatamente, è possibile utilizzare WMI per verificare gli account del servizio in tutti i computer e, se necessario, modificare la password dell'account del servizio.</span><span class="sxs-lookup"><span data-stu-id="1b685-321">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="1b685-322">Il [**parametro \_ LoadOrderGroup di Win32**](win32-loadordergroup.md) rappresenta un gruppo di servizi di sistema che definiscono le dipendenze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1b685-322">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="1b685-323">I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento perché i servizi dipendono tra loro.</span><span class="sxs-lookup"><span data-stu-id="1b685-323">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="1b685-324">Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi precedenti.</span><span class="sxs-lookup"><span data-stu-id="1b685-324">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="1b685-325">Per modificare un servizio da un servizio di rete a un sistema locale, i parametri *StartName* e *StartPassword* devono avere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b685-325">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="1b685-326">Per modificare un servizio da un servizio di sistema locale a una rete, i parametri *StartName* e *StartPassword* devono avere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b685-326">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="1b685-327">Esempio</span><span class="sxs-lookup"><span data-stu-id="1b685-327">Examples</span></span>

<span data-ttu-id="1b685-328">Il codice VBScript seguente consente di modificare l'account del servizio per i servizi in esecuzione con un account utente specificato in LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="1b685-328">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="1b685-329">Il codice VBScript seguente modifica la password dell'account del servizio per tutti gli script in esecuzione in netsvc</span><span class="sxs-lookup"><span data-stu-id="1b685-329">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="1b685-330">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b685-330">Requirements</span></span>



| <span data-ttu-id="1b685-331">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b685-331">Requirement</span></span> | <span data-ttu-id="1b685-332">Valore</span><span class="sxs-lookup"><span data-stu-id="1b685-332">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b685-333">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b685-333">Minimum supported client</span></span><br/> | <span data-ttu-id="1b685-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b685-334">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b685-335">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b685-335">Minimum supported server</span></span><br/> | <span data-ttu-id="1b685-336">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b685-336">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b685-337">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1b685-337">Namespace</span></span><br/>                | <span data-ttu-id="1b685-338">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1b685-338">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b685-339">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b685-339">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b685-340"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b685-340"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="1b685-341">MOF</span><span class="sxs-lookup"><span data-stu-id="1b685-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b685-342"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b685-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b685-343">DLL</span><span class="sxs-lookup"><span data-stu-id="1b685-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b685-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b685-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b685-345">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b685-345">See also</span></span>

<dl> <dt>

<span data-ttu-id="1b685-346">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1b685-346">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1b685-347">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="1b685-347">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="1b685-348">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="1b685-348">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

