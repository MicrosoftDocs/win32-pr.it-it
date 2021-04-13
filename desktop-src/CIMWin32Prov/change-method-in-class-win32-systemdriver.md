---
description: Modifica un \_ servizio Win32 SystemDriver.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Metodo Change della classe Win32_SystemDriver (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da814c8321e35189594bc350bd1e278a219bac59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483564"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="96e39-103">Metodo Change della classe Win32 \_ SystemDriver</span><span class="sxs-lookup"><span data-stu-id="96e39-103">Change method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="96e39-104">Il metodo **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) modifica un [**servizio \_ Win32 SystemDriver**](win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="96e39-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span> <span data-ttu-id="96e39-105">Il parametro [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md) rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="96e39-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="96e39-106">I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento poiché i servizi dipendono tra loro.</span><span class="sxs-lookup"><span data-stu-id="96e39-106">The services must be initiated in the order specified by the Load Order Group as the services are dependent on each other.</span></span> <span data-ttu-id="96e39-107">Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi precedenti.</span><span class="sxs-lookup"><span data-stu-id="96e39-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="96e39-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="96e39-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="96e39-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="96e39-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="96e39-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96e39-110">Syntax</span></span>


```mof
uint32 Change(
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



## <a name="parameters"></a><span data-ttu-id="96e39-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="96e39-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96e39-112">*DisplayName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e39-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e39-113">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="96e39-113">The display name of the service.</span></span> <span data-ttu-id="96e39-114">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="96e39-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="96e39-115">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="96e39-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="96e39-116">I confronti *DisplayName* sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="96e39-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="96e39-117">Constraints: accetta lo stesso valore del parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="96e39-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="96e39-118">Esempio: "ATDISK"</span><span class="sxs-lookup"><span data-stu-id="96e39-118">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="96e39-119">*Nome percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e39-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e39-120">Percorso completo del file eseguibile che implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="96e39-120">The fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="96e39-121">Esempio: *\\ systemroot \\ System32 \\ drivers \\afd.sys*</span><span class="sxs-lookup"><span data-stu-id="96e39-121">Example: *\\SystemRoot\\System32\\drivers\\afd.sys*</span></span>

</dd> <dt>

<span data-ttu-id="96e39-122">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e39-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e39-123">Tipo di servizi forniti ai processi che li chiamano.</span><span class="sxs-lookup"><span data-stu-id="96e39-123">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="96e39-124">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="96e39-124">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="96e39-125">Driver del kernel</span><span class="sxs-lookup"><span data-stu-id="96e39-125">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="96e39-126">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="96e39-126">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="96e39-127">Driver del file System</span><span class="sxs-lookup"><span data-stu-id="96e39-127">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="96e39-128">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="96e39-128">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="96e39-129">Adattatore</span><span class="sxs-lookup"><span data-stu-id="96e39-129">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="96e39-130">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="96e39-130">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="96e39-131">Driver di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="96e39-131">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="96e39-132">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="96e39-132">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="96e39-133">Processo personale</span><span class="sxs-lookup"><span data-stu-id="96e39-133">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="96e39-134">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="96e39-134">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="96e39-135">Condividi processo</span><span class="sxs-lookup"><span data-stu-id="96e39-135">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="96e39-136">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="96e39-136">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="96e39-137">Processo interattivo</span><span class="sxs-lookup"><span data-stu-id="96e39-137">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="96e39-138">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e39-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e39-139">Gravità dell'errore se il servizio non viene avviato durante l'avvio.</span><span class="sxs-lookup"><span data-stu-id="96e39-139">The severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="96e39-140">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="96e39-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="96e39-141">Tutti gli errori vengono registrati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="96e39-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="96e39-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** (0)</span><span class="sxs-lookup"><span data-stu-id="96e39-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="96e39-143">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="96e39-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="96e39-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** (1)</span><span class="sxs-lookup"><span data-stu-id="96e39-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="96e39-145">Normale.</span><span class="sxs-lookup"><span data-stu-id="96e39-145">Normal.</span></span> <span data-ttu-id="96e39-146">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="96e39-146">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="96e39-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)</span><span class="sxs-lookup"><span data-stu-id="96e39-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="96e39-148">Il sistema viene riavviato con l'ultima configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="96e39-148">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="96e39-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (3)</span><span class="sxs-lookup"><span data-stu-id="96e39-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="96e39-150">Il sistema tenta un riavvio con una configurazione valida.</span><span class="sxs-lookup"><span data-stu-id="96e39-150">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="96e39-151">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e39-151">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e39-152">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="96e39-152">The start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="96e39-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Avvio avvio**</span><span class="sxs-lookup"><span data-stu-id="96e39-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="96e39-154">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="96e39-154">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="96e39-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Avvio avvio**</span><span class="sxs-lookup"><span data-stu-id="96e39-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="96e39-156">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="96e39-156">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="96e39-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Avvio del sistema**</span><span class="sxs-lookup"><span data-stu-id="96e39-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start**</span></span>


</dt> <dd>

<span data-ttu-id="96e39-158">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="96e39-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="96e39-159">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="96e39-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="96e39-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Avvio automatico**</span><span class="sxs-lookup"><span data-stu-id="96e39-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start**</span></span>


</dt> <dd>

<span data-ttu-id="96e39-161">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="96e39-161">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="96e39-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inizio richiesta**</span><span class="sxs-lookup"><span data-stu-id="96e39-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start**</span></span>


</dt> <dd>

<span data-ttu-id="96e39-163">Servizio per avviare il gestore di controllo del servizio quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="96e39-163">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="96e39-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato**</span><span class="sxs-lookup"><span data-stu-id="96e39-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="96e39-165">Servizio che non può essere avviato.</span><span class="sxs-lookup"><span data-stu-id="96e39-165">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="96e39-166">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e39-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e39-167">Valore che, se impostato su **true**, il servizio può creare o comunicare con le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="96e39-167">A value that, if **True**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="96e39-168">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e39-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e39-169">Nome dell'account con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="96e39-169">The account name the service runs under.</span></span> <span data-ttu-id="96e39-170">A seconda del tipo di servizio, il nome dell'account può essere nel formato DomainName \\ username o. \\ Nome utente.</span><span class="sxs-lookup"><span data-stu-id="96e39-170">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="96e39-171">Quando viene eseguito, il processo del servizio viene registrato utilizzando uno di questi due formati.</span><span class="sxs-lookup"><span data-stu-id="96e39-171">When it runs, the service process is logged using one of these two forms.</span></span> <span data-ttu-id="96e39-172">Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente.</span><span class="sxs-lookup"><span data-stu-id="96e39-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="96e39-173">Se viene specificata una stringa vuota, il servizio viene connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="96e39-173">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="96e39-174">Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto driver, ad esempio \\ filesystem \\ RDR o \\ driver \\ XNS, che il sistema di input e output (i/O) USA per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96e39-174">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns), which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="96e39-175">Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio, ad esempio DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="96e39-175">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="96e39-176">È anche possibile usare il formato del nome dell'entità utente (UPN) per specificare il nome **iniziale**, ad esempio *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="96e39-176">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="96e39-177">*StartPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e39-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e39-178">Password per il nome dell'account specificato dal parametro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="96e39-178">The password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="96e39-179">Specificare **null** se non si sta modificando la password.</span><span class="sxs-lookup"><span data-stu-id="96e39-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="96e39-180">Specificare una stringa vuota se il servizio non dispone di password.</span><span class="sxs-lookup"><span data-stu-id="96e39-180">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="96e39-181">Quando si modifica un servizio da un sistema locale a una rete o da una rete a un sistema locale, *StartPassword* deve essere una stringa vuota ("") e non **null**.</span><span class="sxs-lookup"><span data-stu-id="96e39-181">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="96e39-182">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e39-182">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e39-183">Nome del gruppo a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="96e39-183">The group name that it is associated with.</span></span> <span data-ttu-id="96e39-184">I gruppi dell'ordine di caricamento sono contenuti nel registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="96e39-184">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="96e39-185">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non appartiene a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="96e39-185">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="96e39-186">Le dipendenze tra i gruppi devono essere elencate nel parametro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="96e39-186">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="96e39-187">I servizi nell'elenco di gruppi per l'ordine di caricamento vengono avviati per primi, seguiti da servizi nei gruppi non inclusi nell'elenco del gruppo di ordini di carico, seguiti da servizi che non appartengono a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="96e39-187">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="96e39-188">Nel registro di sistema è presente un elenco di gruppi di ordini di carico disponibili in:</span><span class="sxs-lookup"><span data-stu-id="96e39-188">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="96e39-189">**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="96e39-189">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="96e39-190">*LoadOrderGroupDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e39-190">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e39-191">Elenco di gruppi di ordini di caricamento che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="96e39-191">The list of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="96e39-192">La matrice è con doppia terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="96e39-192">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="96e39-193">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="96e39-193">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="96e39-194">I nomi dei gruppi devono essere preceduti **dall' \_ \_ identificatore del gruppo SC** (definito nel file WinSvc. h) per distinguerli dai nomi dei servizi, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="96e39-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the WinSvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="96e39-195">La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="96e39-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="96e39-196">*ServiceDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96e39-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e39-197">Elenco contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="96e39-197">The list that contains the names of the services that must start before this service starts.</span></span> <span data-ttu-id="96e39-198">La matrice è con doppia terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="96e39-198">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="96e39-199">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="96e39-199">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="96e39-200">La dipendenza da un servizio significa che questo servizio può essere eseguito solo se è in esecuzione il servizio da cui dipende.</span><span class="sxs-lookup"><span data-stu-id="96e39-200">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96e39-201">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96e39-201">Return value</span></span>

<span data-ttu-id="96e39-202">Restituisce un valore pari a zero (0) se il servizio è stato modificato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="96e39-202">Returns a value of zero (0) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="96e39-203">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="96e39-203">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-204">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="96e39-204">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-205">**Accesso negato** (2)</span><span class="sxs-lookup"><span data-stu-id="96e39-205">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-206">**Servizi dipendenti in esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="96e39-206">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-207">**Controllo del servizio non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="96e39-207">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-208">Il **servizio non può accettare il controllo** (5)</span><span class="sxs-lookup"><span data-stu-id="96e39-208">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-209">**Servizio non attivo** (6)</span><span class="sxs-lookup"><span data-stu-id="96e39-209">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-210">**Timeout richiesta di servizio** (7)</span><span class="sxs-lookup"><span data-stu-id="96e39-210">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-211">**Errore sconosciuto** (8)</span><span class="sxs-lookup"><span data-stu-id="96e39-211">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-212">**Percorso non trovato** (9)</span><span class="sxs-lookup"><span data-stu-id="96e39-212">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-213">**Servizio già in esecuzione** (10)</span><span class="sxs-lookup"><span data-stu-id="96e39-213">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-214">**Database del servizio bloccato** (11)</span><span class="sxs-lookup"><span data-stu-id="96e39-214">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-215">**Dipendenza servizio eliminata** (12)</span><span class="sxs-lookup"><span data-stu-id="96e39-215">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-216">**Errore di dipendenza del servizio** (13)</span><span class="sxs-lookup"><span data-stu-id="96e39-216">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-217">**Servizio disabilitato** (14)</span><span class="sxs-lookup"><span data-stu-id="96e39-217">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-218">**Accesso al servizio non riuscito** (15)</span><span class="sxs-lookup"><span data-stu-id="96e39-218">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-219">**Servizio contrassegnato per l'eliminazione** (16)</span><span class="sxs-lookup"><span data-stu-id="96e39-219">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-220">**Servizio senza thread** (17)</span><span class="sxs-lookup"><span data-stu-id="96e39-220">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-221">**Stato dipendenza circolare** (18)</span><span class="sxs-lookup"><span data-stu-id="96e39-221">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-222">**Stato nome duplicato** (19)</span><span class="sxs-lookup"><span data-stu-id="96e39-222">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-223">**Stato nome non valido** (20)</span><span class="sxs-lookup"><span data-stu-id="96e39-223">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-224">**Stato parametro non valido** (21)</span><span class="sxs-lookup"><span data-stu-id="96e39-224">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-225">**Stato account del servizio non valido** (22)</span><span class="sxs-lookup"><span data-stu-id="96e39-225">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-226">Il **servizio di stato esiste** (23)</span><span class="sxs-lookup"><span data-stu-id="96e39-226">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-227">**Servizio già sospeso** (24)</span><span class="sxs-lookup"><span data-stu-id="96e39-227">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="96e39-228">**Altro** (25 4294967295)</span><span class="sxs-lookup"><span data-stu-id="96e39-228">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="96e39-229">Commenti</span><span class="sxs-lookup"><span data-stu-id="96e39-229">Remarks</span></span>

<span data-ttu-id="96e39-230">Per modificare un servizio da un servizio di rete al sistema locale, usare i valori seguenti per i parametri *StartName* e *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="96e39-230">To change a service from a network service to the local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="96e39-231">Per modificare un servizio da un servizio di sistema locale al servizio di rete, usare i valori seguenti per i parametri *StartName* e *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="96e39-231">To change a service from a local system service to network service, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="96e39-232">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96e39-232">Requirements</span></span>



| <span data-ttu-id="96e39-233">Requisito</span><span class="sxs-lookup"><span data-stu-id="96e39-233">Requirement</span></span> | <span data-ttu-id="96e39-234">Valore</span><span class="sxs-lookup"><span data-stu-id="96e39-234">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96e39-235">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96e39-235">Minimum supported client</span></span><br/> | <span data-ttu-id="96e39-236">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96e39-236">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96e39-237">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96e39-237">Minimum supported server</span></span><br/> | <span data-ttu-id="96e39-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96e39-238">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96e39-239">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="96e39-239">Namespace</span></span><br/>                | <span data-ttu-id="96e39-240">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="96e39-240">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="96e39-241">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96e39-241">Header</span></span><br/>                   | <dl> <span data-ttu-id="96e39-242"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="96e39-242"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="96e39-243">MOF</span><span class="sxs-lookup"><span data-stu-id="96e39-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96e39-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96e39-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="96e39-245">DLL</span><span class="sxs-lookup"><span data-stu-id="96e39-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96e39-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96e39-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96e39-247">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96e39-247">See also</span></span>

<dl> <dt>

<span data-ttu-id="96e39-248">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="96e39-248">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="96e39-249">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="96e39-249">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

