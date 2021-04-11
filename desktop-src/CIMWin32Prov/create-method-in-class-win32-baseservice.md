---
description: Crea un nuovo servizio.
ms.assetid: e000b896-3b49-4650-b706-548592cfe721
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c8115ed3d9795720796b5f944c11a519ff366983
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126651"
---
# <a name="create-method-of-the-win32_baseservice-class"></a><span data-ttu-id="e4723-103">Metodo Create della classe Win32 \_ BaseService</span><span class="sxs-lookup"><span data-stu-id="e4723-103">Create method of the Win32\_BaseService class</span></span>

<span data-ttu-id="e4723-104">Il metodo **create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service.</span></span> <span data-ttu-id="e4723-105">Il parametro *LoadOrderGroup* rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e4723-105">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="e4723-106">I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento, in quanto i servizi sono dipendenti tra loro.</span><span class="sxs-lookup"><span data-stu-id="e4723-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="e4723-107">Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi precedenti.</span><span class="sxs-lookup"><span data-stu-id="e4723-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="e4723-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e4723-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e4723-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e4723-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4723-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4723-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="e4723-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4723-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4723-112">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-113">Nome del servizio da installare nel metodo **create** .</span><span class="sxs-lookup"><span data-stu-id="e4723-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="e4723-114">La lunghezza massima della stringa è 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e4723-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="e4723-115">Il database di gestione controllo servizi conserva la distinzione tra maiuscole e minuscole dei caratteri, ma i confronti tra nomi di servizio non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e4723-115">The service control manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="e4723-116">Le barre (/) e le barre rovesciate doppie ( \\ ) non sono caratteri validi per il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-117">*DisplayName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-118">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-118">Display name of the service.</span></span> <span data-ttu-id="e4723-119">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e4723-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="e4723-120">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="e4723-120">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="e4723-121">I confronti *DisplayName* sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e4723-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="e4723-122">Constraints: accetta lo stesso valore del parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="e4723-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="e4723-123">Esempio: "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="e4723-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="e4723-124">*Nome percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-125">Percorso completo del file eseguibile che implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="e4723-126">Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="e4723-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="e4723-127">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-128">Tipo di servizi forniti ai processi che li chiamano.</span><span class="sxs-lookup"><span data-stu-id="e4723-128">Type of services provided to processes that call them.</span></span> <span data-ttu-id="e4723-129">Il valore è una bitmap.</span><span class="sxs-lookup"><span data-stu-id="e4723-129">The value is a bitmap.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="e4723-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Driver kernel** (1)</span><span class="sxs-lookup"><span data-stu-id="e4723-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="e4723-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Driver del file System** (2)</span><span class="sxs-lookup"><span data-stu-id="e4723-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="e4723-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span><span class="sxs-lookup"><span data-stu-id="e4723-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="e4723-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Driver di riconoscimento** (8)</span><span class="sxs-lookup"><span data-stu-id="e4723-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="e4723-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Processo personalizzato** (16)</span><span class="sxs-lookup"><span data-stu-id="e4723-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="e4723-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Processo di condivisione** (32)</span><span class="sxs-lookup"><span data-stu-id="e4723-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="e4723-136">256</span><span class="sxs-lookup"><span data-stu-id="e4723-136">256</span></span>
</dt> <dd>

<span data-ttu-id="e4723-137">Processo interattivo</span><span class="sxs-lookup"><span data-stu-id="e4723-137">Interactive Process</span></span>

</dd> <dt>




</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e4723-138">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-139">Gravità dell'errore se non è possibile avviare il metodo **create** .</span><span class="sxs-lookup"><span data-stu-id="e4723-139">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="e4723-140">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="e4723-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="e4723-141">Tutti gli errori vengono registrati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e4723-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="e4723-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** (0)</span><span class="sxs-lookup"><span data-stu-id="e4723-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e4723-143">L'utente non viene notificato.</span><span class="sxs-lookup"><span data-stu-id="e4723-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="e4723-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** (1)</span><span class="sxs-lookup"><span data-stu-id="e4723-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e4723-145">L'utente viene notificato.</span><span class="sxs-lookup"><span data-stu-id="e4723-145">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="e4723-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)</span><span class="sxs-lookup"><span data-stu-id="e4723-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e4723-147">Il sistema viene riavviato con l'ultima configurazione valida nota.</span><span class="sxs-lookup"><span data-stu-id="e4723-147">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="e4723-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (3)</span><span class="sxs-lookup"><span data-stu-id="e4723-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e4723-149">Il sistema tenta di iniziare con una configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="e4723-149">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e4723-150">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-150">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-151">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="e4723-151">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="e4723-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Avvio **avvio** ("avvio")</span><span class="sxs-lookup"><span data-stu-id="e4723-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="e4723-153">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e4723-153">Device driver started by the operating system loader.</span></span> <span data-ttu-id="e4723-154">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="e4723-154">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="e4723-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Avvio del sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="e4723-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="e4723-156">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e4723-156">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="e4723-157">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="e4723-157">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="e4723-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Avvio automatico** ("automatico")</span><span class="sxs-lookup"><span data-stu-id="e4723-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="e4723-159">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="e4723-159">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="e4723-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Avvio della richiesta** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="e4723-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="e4723-161">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="e4723-161">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e4723-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")</span><span class="sxs-lookup"><span data-stu-id="e4723-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="e4723-163">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="e4723-163">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e4723-164">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-164">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-165">Se **true**, il servizio può creare o comunicare con Windows sul desktop.</span><span class="sxs-lookup"><span data-stu-id="e4723-165">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-166">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-166">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-167">Nome dell'account con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-167">Account name under which the service runs.</span></span> <span data-ttu-id="e4723-168">A seconda del tipo di servizio, il nome dell'account può essere nel formato "NomeDominio \\ nomeutente".</span><span class="sxs-lookup"><span data-stu-id="e4723-168">Depending on the service type, the account name may be in the form of "DomainName\\Username".</span></span> <span data-ttu-id="e4723-169">Il processo del servizio viene registrato utilizzando una di queste due forme durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e4723-169">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="e4723-170">Se l'account appartiene al dominio predefinito, ". \\ Nome utente "può essere specificato.</span><span class="sxs-lookup"><span data-stu-id="e4723-170">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="e4723-171">Se viene specificato **null** , il servizio viene connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="e4723-171">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="e4723-172">Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto driver, ovvero \\ filesystem \\ RDR o \\ driver XNS, \\ usato dal sistema di input e output (i/O) per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4723-172">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="e4723-173">Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-173">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="e4723-174">Esempio: amministratore di DWDOM \\ .</span><span class="sxs-lookup"><span data-stu-id="e4723-174">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-175">*StartPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-175">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-176">Password per il nome dell'account specificato dal parametro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="e4723-176">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="e4723-177">Specificare **null** se non si sta modificando la password.</span><span class="sxs-lookup"><span data-stu-id="e4723-177">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="e4723-178">Specificare una stringa vuota se il servizio non dispone di password.</span><span class="sxs-lookup"><span data-stu-id="e4723-178">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-179">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-179">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-180">Nome del gruppo associato al nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-180">Group name associated with the new service.</span></span> <span data-ttu-id="e4723-181">I gruppi dell'ordine di caricamento sono contenuti nel registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e4723-181">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="e4723-182">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non appartiene a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="e4723-182">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="e4723-183">Le dipendenze tra i gruppi devono essere elencate nel parametro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="e4723-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="e4723-184">I servizi nell'elenco di gruppi per l'ordine di caricamento vengono avviati per primi, seguiti da servizi nei gruppi non inclusi nell'elenco del gruppo di ordini di carico, seguiti da servizi che non appartengono a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="e4723-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="e4723-185">Nel registro di sistema è presente un elenco di gruppi di ordini di carico disponibili in:</span><span class="sxs-lookup"><span data-stu-id="e4723-185">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="e4723-186">**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="e4723-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="e4723-187">*LoadOrderGroupDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-188">Matrice di gruppi di ordini di caricamento che devono iniziare prima del servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-188">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="e4723-189">Ogni elemento nella matrice è delimitato da **null** e l'elenco viene terminato da due valori **null** .</span><span class="sxs-lookup"><span data-stu-id="e4723-189">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="e4723-190">In Visual Basic o script è possibile passare un vbArray.</span><span class="sxs-lookup"><span data-stu-id="e4723-190">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="e4723-191">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="e4723-191">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="e4723-192">I nomi dei gruppi devono essere preceduti dall' \_ identificatore del gruppo SC \_ (definito nel file winsvc. h) per distinguerlo dal nome del servizio, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e4723-192">Group names must be prefixed by the SC\_GROUP\_IDENTIFIER (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="e4723-193">La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="e4723-193">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-194">*ServiceDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4723-194">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4723-195">Matrice che contiene i nomi dei servizi che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-195">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="e4723-196">Ogni elemento nella matrice è delimitato da **null** e l'elenco viene terminato da due valori **null** .</span><span class="sxs-lookup"><span data-stu-id="e4723-196">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="e4723-197">In Visual Basic o script è possibile passare un vbArray.</span><span class="sxs-lookup"><span data-stu-id="e4723-197">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="e4723-198">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="e4723-198">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="e4723-199">La dipendenza da un servizio significa che questo servizio può essere eseguito solo se è in esecuzione il servizio da cui dipende.</span><span class="sxs-lookup"><span data-stu-id="e4723-199">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4723-200">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4723-200">Return value</span></span>

<span data-ttu-id="e4723-201">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="e4723-201">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e4723-202">**Success**</span><span class="sxs-lookup"><span data-stu-id="e4723-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-203">0</span><span class="sxs-lookup"><span data-stu-id="e4723-203">0</span></span>

<span data-ttu-id="e4723-204">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="e4723-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-205">**Non supportato**</span><span class="sxs-lookup"><span data-stu-id="e4723-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-206">1</span><span class="sxs-lookup"><span data-stu-id="e4723-206">1</span></span>

<span data-ttu-id="e4723-207">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e4723-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-208">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="e4723-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-209">2</span><span class="sxs-lookup"><span data-stu-id="e4723-209">2</span></span>

<span data-ttu-id="e4723-210">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="e4723-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-211">**Servizi dipendenti in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="e4723-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-212">3</span><span class="sxs-lookup"><span data-stu-id="e4723-212">3</span></span>

<span data-ttu-id="e4723-213">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-214">**Controllo del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="e4723-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-215">4</span><span class="sxs-lookup"><span data-stu-id="e4723-215">4</span></span>

<span data-ttu-id="e4723-216">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-217">**Il servizio non può accettare il controllo**</span><span class="sxs-lookup"><span data-stu-id="e4723-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-218">5</span><span class="sxs-lookup"><span data-stu-id="e4723-218">5</span></span>

<span data-ttu-id="e4723-219">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="e4723-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-220">**Servizio non attivo**</span><span class="sxs-lookup"><span data-stu-id="e4723-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-221">6</span><span class="sxs-lookup"><span data-stu-id="e4723-221">6</span></span>

<span data-ttu-id="e4723-222">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="e4723-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-223">**Timeout richiesta servizio**</span><span class="sxs-lookup"><span data-stu-id="e4723-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-224">7</span><span class="sxs-lookup"><span data-stu-id="e4723-224">7</span></span>

<span data-ttu-id="e4723-225">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="e4723-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-226">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="e4723-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-227">8</span><span class="sxs-lookup"><span data-stu-id="e4723-227">8</span></span>

<span data-ttu-id="e4723-228">Processo interattivo.</span><span class="sxs-lookup"><span data-stu-id="e4723-228">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-229">**Percorso non trovato**</span><span class="sxs-lookup"><span data-stu-id="e4723-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-230">9</span><span class="sxs-lookup"><span data-stu-id="e4723-230">9</span></span>

<span data-ttu-id="e4723-231">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-232">**Servizio già in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="e4723-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-233">10</span><span class="sxs-lookup"><span data-stu-id="e4723-233">10</span></span>

<span data-ttu-id="e4723-234">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e4723-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-235">**Database del servizio bloccato**</span><span class="sxs-lookup"><span data-stu-id="e4723-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-236">11</span><span class="sxs-lookup"><span data-stu-id="e4723-236">11</span></span>

<span data-ttu-id="e4723-237">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="e4723-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-238">**Dipendenza servizio eliminata**</span><span class="sxs-lookup"><span data-stu-id="e4723-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-239">12</span><span class="sxs-lookup"><span data-stu-id="e4723-239">12</span></span>

<span data-ttu-id="e4723-240">Il servizio si basa su una dipendenza che è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e4723-240">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-241">**Errore di dipendenza del servizio**</span><span class="sxs-lookup"><span data-stu-id="e4723-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-242">13</span><span class="sxs-lookup"><span data-stu-id="e4723-242">13</span></span>

<span data-ttu-id="e4723-243">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="e4723-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-244">**Servizio disabilitato**</span><span class="sxs-lookup"><span data-stu-id="e4723-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-245">14</span><span class="sxs-lookup"><span data-stu-id="e4723-245">14</span></span>

<span data-ttu-id="e4723-246">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e4723-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-247">**Accesso al servizio non riuscito**</span><span class="sxs-lookup"><span data-stu-id="e4723-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-248">15</span><span class="sxs-lookup"><span data-stu-id="e4723-248">15</span></span>

<span data-ttu-id="e4723-249">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e4723-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-250">**Servizio contrassegnato per l'eliminazione**</span><span class="sxs-lookup"><span data-stu-id="e4723-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-251">16</span><span class="sxs-lookup"><span data-stu-id="e4723-251">16</span></span>

<span data-ttu-id="e4723-252">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e4723-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-253">**Servizio senza thread**</span><span class="sxs-lookup"><span data-stu-id="e4723-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-254">17</span><span class="sxs-lookup"><span data-stu-id="e4723-254">17</span></span>

<span data-ttu-id="e4723-255">Nessun thread di esecuzione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-255">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-256">**Stato dipendenza circolare**</span><span class="sxs-lookup"><span data-stu-id="e4723-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-257">18</span><span class="sxs-lookup"><span data-stu-id="e4723-257">18</span></span>

<span data-ttu-id="e4723-258">All'avvio del servizio sono state rilevate dipendenze circolari.</span><span class="sxs-lookup"><span data-stu-id="e4723-258">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-259">**Stato nome duplicato**</span><span class="sxs-lookup"><span data-stu-id="e4723-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-260">19</span><span class="sxs-lookup"><span data-stu-id="e4723-260">19</span></span>

<span data-ttu-id="e4723-261">È presente un servizio in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="e4723-261">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-262">**Stato nome non valido**</span><span class="sxs-lookup"><span data-stu-id="e4723-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-263">20</span><span class="sxs-lookup"><span data-stu-id="e4723-263">20</span></span>

<span data-ttu-id="e4723-264">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="e4723-264">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-265">**Stato parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="e4723-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-266">21</span><span class="sxs-lookup"><span data-stu-id="e4723-266">21</span></span>

<span data-ttu-id="e4723-267">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-268">**Stato account del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="e4723-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-269">22</span><span class="sxs-lookup"><span data-stu-id="e4723-269">22</span></span>

<span data-ttu-id="e4723-270">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="e4723-270">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-271">**Il servizio stato esiste**</span><span class="sxs-lookup"><span data-stu-id="e4723-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-272">23</span><span class="sxs-lookup"><span data-stu-id="e4723-272">23</span></span>

<span data-ttu-id="e4723-273">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e4723-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-274">**Servizio già sospeso**</span><span class="sxs-lookup"><span data-stu-id="e4723-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-275">24</span><span class="sxs-lookup"><span data-stu-id="e4723-275">24</span></span>

<span data-ttu-id="e4723-276">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e4723-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="e4723-277">**Altri**</span><span class="sxs-lookup"><span data-stu-id="e4723-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="e4723-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="e4723-278">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4723-279">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4723-279">Requirements</span></span>



| <span data-ttu-id="e4723-280">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4723-280">Requirement</span></span> | <span data-ttu-id="e4723-281">Valore</span><span class="sxs-lookup"><span data-stu-id="e4723-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4723-282">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4723-282">Minimum supported client</span></span><br/> | <span data-ttu-id="e4723-283">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4723-283">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e4723-284">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4723-284">Minimum supported server</span></span><br/> | <span data-ttu-id="e4723-285">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4723-285">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e4723-286">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e4723-286">Namespace</span></span><br/>                | <span data-ttu-id="e4723-287">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e4723-287">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e4723-288">MOF</span><span class="sxs-lookup"><span data-stu-id="e4723-288">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4723-289"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4723-289"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4723-290">DLL</span><span class="sxs-lookup"><span data-stu-id="e4723-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4723-291"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4723-291"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4723-292">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4723-292">See also</span></span>

<dl> <dt>

<span data-ttu-id="e4723-293">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e4723-293">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e4723-294">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="e4723-294">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

