---
description: Modifica un oggetto servizio derivato da Win32 \_ BaseService.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Metodo Change della classe Win32_BaseService (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a70ee83229a830e22fba4241a6c50eb8d971c5ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127227"
---
# <a name="change-method-of-the-win32_baseservice-class"></a><span data-ttu-id="778a5-103">Metodo Change della classe Win32 \_ BaseService</span><span class="sxs-lookup"><span data-stu-id="778a5-103">Change method of the Win32\_BaseService class</span></span>

<span data-ttu-id="778a5-104">Il metodo **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) modifica un oggetto servizio derivato da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="778a5-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span> <span data-ttu-id="778a5-105">Il [**parametro \_ LoadOrderGroup di Win32**](win32-loadordergroup.md) rappresenta un gruppo di servizi di sistema che definiscono le dipendenze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="778a5-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="778a5-106">I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento, perché i servizi dipendono tra loro.</span><span class="sxs-lookup"><span data-stu-id="778a5-106">The services must be initiated in the order specified by the Load Order Group, because the services depend on each other.</span></span> <span data-ttu-id="778a5-107">Per il corretto funzionamento di questi servizi dipendenti sono necessari servizi precedenti.</span><span class="sxs-lookup"><span data-stu-id="778a5-107">These dependent services require antecedent services to function correctly.</span></span>

<span data-ttu-id="778a5-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="778a5-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="778a5-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="778a5-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="778a5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="778a5-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="778a5-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="778a5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="778a5-112">*DisplayName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778a5-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778a5-113">Nome visualizzato per un servizio.</span><span class="sxs-lookup"><span data-stu-id="778a5-113">The display name for a service.</span></span> <span data-ttu-id="778a5-114">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="778a5-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="778a5-115">Il nome viene mantenuto nella gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="778a5-115">The name is case preserved in the service control manager.</span></span> <span data-ttu-id="778a5-116">I confronti *DisplayName* sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="778a5-116">*DisplayName* comparisons are always case insensitive.</span></span>

<span data-ttu-id="778a5-117">Constraints: accetta lo stesso valore del parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="778a5-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="778a5-118">Esempio: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="778a5-118">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="778a5-119">*Nome percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778a5-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778a5-120">Percorso completo del file eseguibile che implementa un servizio.</span><span class="sxs-lookup"><span data-stu-id="778a5-120">The fully qualified path to the executable file that implements a service.</span></span>

<span data-ttu-id="778a5-121">Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="778a5-121">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="778a5-122">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778a5-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778a5-123">Tipo di servizi forniti ai processi che li chiamano.</span><span class="sxs-lookup"><span data-stu-id="778a5-123">Type of services provided to processes that call them.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="778a5-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Driver kernel** (1)</span><span class="sxs-lookup"><span data-stu-id="778a5-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="778a5-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Driver del file System** (2)</span><span class="sxs-lookup"><span data-stu-id="778a5-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="778a5-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span><span class="sxs-lookup"><span data-stu-id="778a5-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="778a5-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Driver di riconoscimento** (8)</span><span class="sxs-lookup"><span data-stu-id="778a5-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="778a5-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Processo personalizzato** (16)</span><span class="sxs-lookup"><span data-stu-id="778a5-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="778a5-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Processo di condivisione** (32)</span><span class="sxs-lookup"><span data-stu-id="778a5-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="778a5-130">(256)</span><span class="sxs-lookup"><span data-stu-id="778a5-130">(256)</span></span>


</dt> <dd>

<span data-ttu-id="778a5-131">Processo interattivo</span><span class="sxs-lookup"><span data-stu-id="778a5-131">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="778a5-132">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778a5-132">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778a5-133">Gravità di un errore se il servizio non viene avviato durante l'avvio.</span><span class="sxs-lookup"><span data-stu-id="778a5-133">Severity of an error if this service does not start during startup.</span></span> <span data-ttu-id="778a5-134">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="778a5-134">The value indicates the action that the startup program takes if failure occurs.</span></span> <span data-ttu-id="778a5-135">Tutti gli errori vengono registrati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="778a5-135">The system logs all errors.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="778a5-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** (0)</span><span class="sxs-lookup"><span data-stu-id="778a5-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="778a5-137">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="778a5-137">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="778a5-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** (1)</span><span class="sxs-lookup"><span data-stu-id="778a5-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="778a5-139">Normale.</span><span class="sxs-lookup"><span data-stu-id="778a5-139">Normal.</span></span> <span data-ttu-id="778a5-140">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="778a5-140">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="778a5-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)</span><span class="sxs-lookup"><span data-stu-id="778a5-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="778a5-142">Il sistema viene riavviato con l'ultima configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="778a5-142">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="778a5-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (3)</span><span class="sxs-lookup"><span data-stu-id="778a5-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="778a5-144">Il sistema tenta un riavvio con una configurazione valida.</span><span class="sxs-lookup"><span data-stu-id="778a5-144">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="778a5-145">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778a5-145">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778a5-146">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="778a5-146">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="778a5-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Avvio **avvio** ("avvio")</span><span class="sxs-lookup"><span data-stu-id="778a5-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="778a5-148">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="778a5-148">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="778a5-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Avvio del sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="778a5-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="778a5-150">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="778a5-150">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="778a5-151">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="778a5-151">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="778a5-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Avvio automatico** ("automatico")</span><span class="sxs-lookup"><span data-stu-id="778a5-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="778a5-153">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="778a5-153">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="778a5-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Avvio della richiesta** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="778a5-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="778a5-155">Servizio per avviare il gestore di controllo del servizio quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="778a5-155">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="778a5-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")</span><span class="sxs-lookup"><span data-stu-id="778a5-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="778a5-157">Servizio che non può essere avviato.</span><span class="sxs-lookup"><span data-stu-id="778a5-157">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="778a5-158">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778a5-158">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778a5-159">Se **true**, il servizio può creare o comunicare con una finestra sul desktop.</span><span class="sxs-lookup"><span data-stu-id="778a5-159">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-160">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778a5-160">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778a5-161">Nome dell'account con cui viene eseguito il servizio, che dipende dal tipo di servizio.</span><span class="sxs-lookup"><span data-stu-id="778a5-161">Account name that the service runs under, which depends on the service type.</span></span> <span data-ttu-id="778a5-162">Il nome dell'account può essere nel formato DomainName \\ username o. \\ Nome utente.</span><span class="sxs-lookup"><span data-stu-id="778a5-162">The account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="778a5-163">Quando viene eseguito, il processo del servizio viene registrato utilizzando uno dei due formati precedenti.</span><span class="sxs-lookup"><span data-stu-id="778a5-163">When it runs, the service process is logged by using one of the previous two forms.</span></span> <span data-ttu-id="778a5-164">Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente.</span><span class="sxs-lookup"><span data-stu-id="778a5-164">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="778a5-165">Se viene specificata una stringa vuota, il servizio viene connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="778a5-165">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="778a5-166">Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto driver, ad esempio \\ filesystem \\ RDR o \\ driver \\ XNS, usato dal sistema di input e output (i/O) per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="778a5-166">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns, which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="778a5-167">Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio, ad esempio DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="778a5-167">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="778a5-168">È anche possibile usare il formato del nome dell'entità utente (UPN) per specificare il nome **iniziale**, ad esempio *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="778a5-168">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-169">*StartPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778a5-169">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778a5-170">Password per il nome dell'account specificato dal parametro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="778a5-170">Password to the account name that the *StartName* parameter specifies.</span></span> <span data-ttu-id="778a5-171">Specificare **null** se non si modifica la password.</span><span class="sxs-lookup"><span data-stu-id="778a5-171">Specify **NULL** when you do not change the password.</span></span> <span data-ttu-id="778a5-172">Specificare una stringa vuota se il servizio non dispone di una password.</span><span class="sxs-lookup"><span data-stu-id="778a5-172">Specify an empty string if the service does not have a password.</span></span>

> [!Note]  
> <span data-ttu-id="778a5-173">Quando si modifica un servizio da sistema locale a rete o da rete a sistema locale, *StartPassword* deve essere una stringa vuota ("") e non **null**.</span><span class="sxs-lookup"><span data-stu-id="778a5-173">When you change a service from local system to network or from network to local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="778a5-174">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778a5-174">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778a5-175">Nome del gruppo a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="778a5-175">Group name that it is associated with.</span></span> <span data-ttu-id="778a5-176">I gruppi dell'ordine di caricamento sono contenuti nel registro di sistema e determinano la sequenza di caricamento dei servizi in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="778a5-176">Load order groups are contained in the system registry, and determine the sequence that services are loaded into an operating system.</span></span> <span data-ttu-id="778a5-177">Se il puntatore è **null** o punta a una stringa vuota, il servizio non appartiene a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="778a5-177">If the pointer is **NULL**, or points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="778a5-178">Le dipendenze tra i gruppi devono essere elencate nel parametro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="778a5-178">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="778a5-179">I servizi nell'elenco di gruppi per l'ordine di caricamento vengono avviati per primi, seguiti da servizi nei gruppi non inclusi nell'elenco del gruppo di ordini di carico, seguiti da servizi che non appartengono a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="778a5-179">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="778a5-180">Il registro di sistema include un elenco di gruppi di ordini di carico situati in **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.</span><span class="sxs-lookup"><span data-stu-id="778a5-180">The system registry has a list of load ordering groups located at **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-181">*LoadOrderGroupDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778a5-181">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778a5-182">Elenco di gruppi di ordini di caricamento che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="778a5-182">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="778a5-183">La matrice è con doppia terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="778a5-183">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="778a5-184">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="778a5-184">If the pointer is **NULL**, or if it points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="778a5-185">I nomi dei gruppi devono essere preceduti **dall' \_ \_ identificatore del gruppo SC** (definito nel file winsvc. h) per distinguerli dai nomi dei servizi, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="778a5-185">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="778a5-186">La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="778a5-186">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-187">*ServiceDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="778a5-187">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778a5-188">Elenco contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="778a5-188">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="778a5-189">La matrice è con doppia terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="778a5-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="778a5-190">Se il puntatore è **null** o punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="778a5-190">If the pointer is **NULL**, or points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="778a5-191">La dipendenza da un servizio significa che questo servizio può essere eseguito solo se è in esecuzione il servizio da cui dipende.</span><span class="sxs-lookup"><span data-stu-id="778a5-191">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="778a5-192">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="778a5-192">Return value</span></span>

<span data-ttu-id="778a5-193">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="778a5-193">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="778a5-194">**Success**</span><span class="sxs-lookup"><span data-stu-id="778a5-194">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-195">0</span><span class="sxs-lookup"><span data-stu-id="778a5-195">0</span></span>

<span data-ttu-id="778a5-196">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="778a5-196">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-197">**Non supportato**</span><span class="sxs-lookup"><span data-stu-id="778a5-197">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-198">1</span><span class="sxs-lookup"><span data-stu-id="778a5-198">1</span></span>

<span data-ttu-id="778a5-199">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="778a5-199">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-200">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="778a5-200">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-201">2</span><span class="sxs-lookup"><span data-stu-id="778a5-201">2</span></span>

<span data-ttu-id="778a5-202">L'utente non dispone dei privilegi di accesso necessari.</span><span class="sxs-lookup"><span data-stu-id="778a5-202">The user does not have the necessary access privileges.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-203">**Servizi dipendenti in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="778a5-203">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-204">3</span><span class="sxs-lookup"><span data-stu-id="778a5-204">3</span></span>

<span data-ttu-id="778a5-205">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="778a5-205">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-206">**Controllo del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="778a5-206">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-207">4</span><span class="sxs-lookup"><span data-stu-id="778a5-207">4</span></span>

<span data-ttu-id="778a5-208">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="778a5-208">The requested control code is not valid, or is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-209">**Il servizio non può accettare il controllo**</span><span class="sxs-lookup"><span data-stu-id="778a5-209">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-210">5</span><span class="sxs-lookup"><span data-stu-id="778a5-210">5</span></span>

<span data-ttu-id="778a5-211">Impossibile inviare il codice di controllo richiesto al servizio perché la proprietà [**state**](win32-baseservice.md) nell'oggetto [**Win32 \_ BaseService**](win32-baseservice.md) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="778a5-211">The requested control code cannot be sent to the service because the [**State**](win32-baseservice.md) property in the [**Win32\_BaseService**](win32-baseservice.md) object is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-212">**Servizio non attivo**</span><span class="sxs-lookup"><span data-stu-id="778a5-212">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-213">6</span><span class="sxs-lookup"><span data-stu-id="778a5-213">6</span></span>

<span data-ttu-id="778a5-214">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="778a5-214">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-215">**Timeout richiesta servizio**</span><span class="sxs-lookup"><span data-stu-id="778a5-215">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-216">7</span><span class="sxs-lookup"><span data-stu-id="778a5-216">7</span></span>

<span data-ttu-id="778a5-217">Il servizio non risponde alla richiesta di avvio rapidamente.</span><span class="sxs-lookup"><span data-stu-id="778a5-217">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-218">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="778a5-218">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-219">8</span><span class="sxs-lookup"><span data-stu-id="778a5-219">8</span></span>

<span data-ttu-id="778a5-220">Processo interattivo.</span><span class="sxs-lookup"><span data-stu-id="778a5-220">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-221">**Percorso non trovato**</span><span class="sxs-lookup"><span data-stu-id="778a5-221">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-222">9</span><span class="sxs-lookup"><span data-stu-id="778a5-222">9</span></span>

<span data-ttu-id="778a5-223">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="778a5-223">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-224">**Servizio già in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="778a5-224">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-225">10</span><span class="sxs-lookup"><span data-stu-id="778a5-225">10</span></span>

<span data-ttu-id="778a5-226">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="778a5-226">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-227">**Database del servizio bloccato**</span><span class="sxs-lookup"><span data-stu-id="778a5-227">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-228">11</span><span class="sxs-lookup"><span data-stu-id="778a5-228">11</span></span>

<span data-ttu-id="778a5-229">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="778a5-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-230">**Dipendenza servizio eliminata**</span><span class="sxs-lookup"><span data-stu-id="778a5-230">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-231">12</span><span class="sxs-lookup"><span data-stu-id="778a5-231">12</span></span>

<span data-ttu-id="778a5-232">Una dipendenza per cui si basa questo servizio viene rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="778a5-232">A dependency for which this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-233">**Errore di dipendenza del servizio**</span><span class="sxs-lookup"><span data-stu-id="778a5-233">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-234">13</span><span class="sxs-lookup"><span data-stu-id="778a5-234">13</span></span>

<span data-ttu-id="778a5-235">Il servizio non trova il servizio necessario da un servizio dipendente.</span><span class="sxs-lookup"><span data-stu-id="778a5-235">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-236">**Servizio disabilitato**</span><span class="sxs-lookup"><span data-stu-id="778a5-236">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-237">14</span><span class="sxs-lookup"><span data-stu-id="778a5-237">14</span></span>

<span data-ttu-id="778a5-238">Il servizio è disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="778a5-238">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-239">**Accesso al servizio non riuscito**</span><span class="sxs-lookup"><span data-stu-id="778a5-239">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-240">15</span><span class="sxs-lookup"><span data-stu-id="778a5-240">15</span></span>

<span data-ttu-id="778a5-241">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="778a5-241">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-242">**Servizio contrassegnato per l'eliminazione**</span><span class="sxs-lookup"><span data-stu-id="778a5-242">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-243">16</span><span class="sxs-lookup"><span data-stu-id="778a5-243">16</span></span>

<span data-ttu-id="778a5-244">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="778a5-244">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-245">**Servizio senza thread**</span><span class="sxs-lookup"><span data-stu-id="778a5-245">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-246">17</span><span class="sxs-lookup"><span data-stu-id="778a5-246">17</span></span>

<span data-ttu-id="778a5-247">Nessun thread di esecuzione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="778a5-247">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-248">**Stato dipendenza circolare**</span><span class="sxs-lookup"><span data-stu-id="778a5-248">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-249">18</span><span class="sxs-lookup"><span data-stu-id="778a5-249">18</span></span>

<span data-ttu-id="778a5-250">All'avvio del servizio sono state rilevate dipendenze circolari.</span><span class="sxs-lookup"><span data-stu-id="778a5-250">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-251">**Stato nome duplicato**</span><span class="sxs-lookup"><span data-stu-id="778a5-251">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-252">19</span><span class="sxs-lookup"><span data-stu-id="778a5-252">19</span></span>

<span data-ttu-id="778a5-253">È presente un servizio in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="778a5-253">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-254">**Stato nome non valido**</span><span class="sxs-lookup"><span data-stu-id="778a5-254">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-255">20</span><span class="sxs-lookup"><span data-stu-id="778a5-255">20</span></span>

<span data-ttu-id="778a5-256">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="778a5-256">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-257">**Stato parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="778a5-257">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-258">21</span><span class="sxs-lookup"><span data-stu-id="778a5-258">21</span></span>

<span data-ttu-id="778a5-259">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="778a5-259">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-260">**Stato account del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="778a5-260">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-261">22</span><span class="sxs-lookup"><span data-stu-id="778a5-261">22</span></span>

<span data-ttu-id="778a5-262">L'account per il servizio da eseguire non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="778a5-262">The account for this service to run under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-263">**Il servizio stato esiste**</span><span class="sxs-lookup"><span data-stu-id="778a5-263">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-264">23</span><span class="sxs-lookup"><span data-stu-id="778a5-264">23</span></span>

<span data-ttu-id="778a5-265">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="778a5-265">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-266">**Servizio già sospeso**</span><span class="sxs-lookup"><span data-stu-id="778a5-266">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-267">24</span><span class="sxs-lookup"><span data-stu-id="778a5-267">24</span></span>

<span data-ttu-id="778a5-268">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="778a5-268">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="778a5-269">**Altri**</span><span class="sxs-lookup"><span data-stu-id="778a5-269">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="778a5-270">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="778a5-270">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="778a5-271">Commenti</span><span class="sxs-lookup"><span data-stu-id="778a5-271">Remarks</span></span>

<span data-ttu-id="778a5-272">Per modificare un servizio da una rete a un sistema locale, usare i valori seguenti per i parametri *StartName* e *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="778a5-272">To change a service from a network to a local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="778a5-273">Per modificare un servizio da un sistema locale a una rete, usare i valori seguenti per i parametri *StartName* e *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="778a5-273">To change a service from a local system to a network, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="778a5-274">Requisiti</span><span class="sxs-lookup"><span data-stu-id="778a5-274">Requirements</span></span>



| <span data-ttu-id="778a5-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="778a5-275">Requirement</span></span> | <span data-ttu-id="778a5-276">Valore</span><span class="sxs-lookup"><span data-stu-id="778a5-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="778a5-277">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="778a5-277">Minimum supported client</span></span><br/> | <span data-ttu-id="778a5-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="778a5-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="778a5-279">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="778a5-279">Minimum supported server</span></span><br/> | <span data-ttu-id="778a5-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="778a5-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="778a5-281">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="778a5-281">Namespace</span></span><br/>                | <span data-ttu-id="778a5-282">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="778a5-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="778a5-283">Intestazione</span><span class="sxs-lookup"><span data-stu-id="778a5-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="778a5-284"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="778a5-284"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="778a5-285">MOF</span><span class="sxs-lookup"><span data-stu-id="778a5-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="778a5-286"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="778a5-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="778a5-287">DLL</span><span class="sxs-lookup"><span data-stu-id="778a5-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="778a5-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="778a5-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="778a5-289">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="778a5-289">See also</span></span>

<dl> <dt>

<span data-ttu-id="778a5-290">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="778a5-290">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="778a5-291">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="778a5-291">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

