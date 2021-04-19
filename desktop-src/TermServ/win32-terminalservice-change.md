---
title: Metodo Change della classe Win32_Service (Mbnapi. h) (TerminalService)
description: Modifica un \_ TerminalService Win32.
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- Modificare il metodo Servizi Desktop remoto
- Modificare il metodo Servizi Desktop remoto, Win32_Service classe
- Classe Win32_Service Servizi Desktop remoto, metodo Change
topic_type:
- apiref
api_name:
- Win32_Service.Change
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa34ea0c9c38cd0b11f97a0bbf651f1aebf37a46
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389205"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a><span data-ttu-id="4e419-106">Metodo Change della classe Win32_Service (Mbnapi. h)-TerminalService</span><span class="sxs-lookup"><span data-stu-id="4e419-106">Change method of the Win32_Service class (Mbnapi.h) - TerminalService</span></span>

<span data-ttu-id="4e419-107">Il metodo **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) modifica un [**\_ TerminalService Win32**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="4e419-107">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="4e419-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4e419-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4e419-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4e419-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e419-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e419-110">Syntax</span></span>


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
  [in] string  LoadOrderGroupDependencies,
  [in] string  ServiceDependencies
);
```



## <a name="parameters"></a><span data-ttu-id="4e419-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e419-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e419-112">*DisplayName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e419-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e419-113">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-113">The display name of the service.</span></span> <span data-ttu-id="4e419-114">La lunghezza massima della stringa è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="4e419-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="4e419-115">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="4e419-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="4e419-116">I confronti *DisplayName* sono sempre senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4e419-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="4e419-117">Constraints: accetta lo stesso valore della proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="4e419-117">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="4e419-118">Esempio, "ATDISK".</span><span class="sxs-lookup"><span data-stu-id="4e419-118">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="4e419-119">*Nome percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e419-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e419-120">Percorso completo del file eseguibile che implementa il servizio, ad esempio " \\ systemroot \\ system32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="4e419-120">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="4e419-121">*ServiceType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e419-121">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e419-122">Tipo di servizi forniti ai processi che li chiamano.</span><span class="sxs-lookup"><span data-stu-id="4e419-122">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="4e419-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4e419-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4e419-124">Driver del kernel</span><span class="sxs-lookup"><span data-stu-id="4e419-124">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="4e419-125">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="4e419-125">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="4e419-126">Driver del file System</span><span class="sxs-lookup"><span data-stu-id="4e419-126">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="4e419-127">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="4e419-127">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="4e419-128">Adattatore</span><span class="sxs-lookup"><span data-stu-id="4e419-128">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="4e419-129">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="4e419-129">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="4e419-130">Driver di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="4e419-130">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="4e419-131">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="4e419-131">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="4e419-132">Processo personale</span><span class="sxs-lookup"><span data-stu-id="4e419-132">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="4e419-133">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="4e419-133">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="4e419-134">Condividi processo</span><span class="sxs-lookup"><span data-stu-id="4e419-134">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="4e419-135">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="4e419-135">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="4e419-136">Processo interattivo</span><span class="sxs-lookup"><span data-stu-id="4e419-136">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4e419-137">*ErrorControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e419-137">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e419-138">Gravità dell'errore se il servizio non viene avviato durante l'avvio.</span><span class="sxs-lookup"><span data-stu-id="4e419-138">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="4e419-139">Il valore indica l'azione eseguita dal programma di avvio in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="4e419-139">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="4e419-140">Tutti gli errori vengono registrati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4e419-140">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="4e419-141">0</span><span class="sxs-lookup"><span data-stu-id="4e419-141">0</span></span>
</dt> <dd>

<span data-ttu-id="4e419-142">**Ignore**.</span><span class="sxs-lookup"><span data-stu-id="4e419-142">**Ignore**.</span></span> <span data-ttu-id="4e419-143">L'avvio continua.</span><span class="sxs-lookup"><span data-stu-id="4e419-143">Startup continues.</span></span> <span data-ttu-id="4e419-144">Non viene fornita alcuna notifica all'utente che il servizio non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="4e419-144">No notification is given to the user that the service failed.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-145">1</span><span class="sxs-lookup"><span data-stu-id="4e419-145">1</span></span>
</dt> <dd>

<span data-ttu-id="4e419-146">**Normale.**</span><span class="sxs-lookup"><span data-stu-id="4e419-146">**Normal.**</span></span> <span data-ttu-id="4e419-147">L'avvio continua.</span><span class="sxs-lookup"><span data-stu-id="4e419-147">Startup continues.</span></span> <span data-ttu-id="4e419-148">Prima che l'utente acceda, l'utente riceve la notifica "almeno un servizio o un dispositivo ha avuto esito negativo durante l'avvio".</span><span class="sxs-lookup"><span data-stu-id="4e419-148">Before the user logs on, the user receives the notification, "At least one service or device failed during startup."</span></span>

</dd> <dt>

<span data-ttu-id="4e419-149">2</span><span class="sxs-lookup"><span data-stu-id="4e419-149">2</span></span>
</dt> <dd>

<span data-ttu-id="4e419-150">**Grave.**</span><span class="sxs-lookup"><span data-stu-id="4e419-150">**Severe.**</span></span> <span data-ttu-id="4e419-151">Il computer tenta di riavviare con l'ultima configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="4e419-151">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="4e419-152">Se il servizio ha di nuovo esito negativo, l'avvio continua e viene fornita una notifica all'utente.</span><span class="sxs-lookup"><span data-stu-id="4e419-152">If the service fails again, startup continues and notification is given to the user.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-153">3</span><span class="sxs-lookup"><span data-stu-id="4e419-153">3</span></span>
</dt> <dd>

<span data-ttu-id="4e419-154">**Critico.**</span><span class="sxs-lookup"><span data-stu-id="4e419-154">**Critical.**</span></span> <span data-ttu-id="4e419-155">Il computer tenta di riavviare con l'ultima configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="4e419-155">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="4e419-156">Se il servizio ha di nuovo esito negativo, l'avvio viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="4e419-156">If the service fails again, startup stops.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4e419-157">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e419-157">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e419-158">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="4e419-158">Start mode of the Windows base service.</span></span> <span data-ttu-id="4e419-159">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4e419-159">For more information, see the Remarks section.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="4e419-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span><span class="sxs-lookup"><span data-stu-id="4e419-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="4e419-161">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e419-161">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="4e419-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema**</span><span class="sxs-lookup"><span data-stu-id="4e419-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="4e419-163">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e419-163">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="4e419-164">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="4e419-164">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="4e419-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatico**</span><span class="sxs-lookup"><span data-stu-id="4e419-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="4e419-166">Il servizio viene avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="4e419-166">Service is started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="4e419-167">I servizi di avvio automatico vengono avviati prima che un utente acceda al computer ed eseguito anche se nessun utente accede al computer.</span><span class="sxs-lookup"><span data-stu-id="4e419-167">Autostart services start before a user logs on to the computer and run even if no user logs on to the computer.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="4e419-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale**</span><span class="sxs-lookup"><span data-stu-id="4e419-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="4e419-169">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4e419-169">Service to be started by the service control manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span> <span data-ttu-id="4e419-170">Sebbene i servizi manuali debbano essere avviati in modo specifico da un utente (o da uno script), continuano a essere eseguiti anche se l'utente si disconnette.</span><span class="sxs-lookup"><span data-stu-id="4e419-170">Although manual services must be specifically started by a user (or by a script), they continue to run even if the user logs off.</span></span> <span data-ttu-id="4e419-171">I servizi manuali sono spesso denominati servizi su richiesta.</span><span class="sxs-lookup"><span data-stu-id="4e419-171">Manual services are often referred to as on-demand services.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4e419-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato**</span><span class="sxs-lookup"><span data-stu-id="4e419-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="4e419-173">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="4e419-173">Service that can no longer be started.</span></span> <span data-ttu-id="4e419-174">Per avviare un servizio disabilitato, è innanzitutto necessario modificare l'opzione di avvio su automatico o manuale.</span><span class="sxs-lookup"><span data-stu-id="4e419-174">To start a disabled service, you must first change the startup option to either Auto or Manual.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4e419-175">*DesktopInteract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e419-175">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e419-176">Se **true**, il servizio può creare o comunicare con una finestra sul desktop.</span><span class="sxs-lookup"><span data-stu-id="4e419-176">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-177">*StartName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e419-177">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e419-178">Nome dell'account con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-178">Account name the service runs under.</span></span> <span data-ttu-id="4e419-179">A seconda del tipo di servizio, il nome dell'account può essere nel formato DomainName \\ username o. \\ Nome utente.</span><span class="sxs-lookup"><span data-stu-id="4e419-179">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="4e419-180">Il processo del servizio verrà registrato utilizzando una di queste due forme durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4e419-180">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="4e419-181">Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente.</span><span class="sxs-lookup"><span data-stu-id="4e419-181">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="4e419-182">Se viene specificato **null** , il servizio verrà connesso come account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="4e419-182">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="4e419-183">Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto del driver (ovvero, \\ filesystem \\ RDR o \\ driver \\ XNS) usato dal sistema di input e output (i/O) per caricare il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e419-183">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="4e419-184">Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio, ad esempio "DWDOM \\ admin".</span><span class="sxs-lookup"><span data-stu-id="4e419-184">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="4e419-185">È anche possibile usare il formato del nome dell'entità utente (UPN) per specificare il nome **iniziale**, ad esempio *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="4e419-185">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-186">*StartPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e419-186">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e419-187">Password per il nome dell'account specificato dal parametro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="4e419-187">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="4e419-188">Specificare **null** se non si sta modificando la password.</span><span class="sxs-lookup"><span data-stu-id="4e419-188">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="4e419-189">Specificare una stringa vuota se il servizio non dispone di password.</span><span class="sxs-lookup"><span data-stu-id="4e419-189">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="4e419-190">Quando si modifica un servizio da un sistema locale a una rete o da una rete a un sistema locale, *StartPassword* deve essere una stringa vuota ("") e non **null**.</span><span class="sxs-lookup"><span data-stu-id="4e419-190">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="4e419-191">*LoadOrderGroup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e419-191">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e419-192">Nome del gruppo a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="4e419-192">Group name that it is associated with.</span></span> <span data-ttu-id="4e419-193">I gruppi dell'ordine di caricamento sono contenuti nel registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e419-193">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="4e419-194">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non appartiene a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="4e419-194">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="4e419-195">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4e419-195">For more information, see the Remarks section.</span></span>

<span data-ttu-id="4e419-196">Le dipendenze tra i gruppi devono essere elencate nel parametro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="4e419-196">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="4e419-197">I servizi nell'elenco di gruppi per l'ordine di caricamento vengono avviati per primi, seguiti da servizi nei gruppi non inclusi nell'elenco del gruppo di ordini di carico, seguiti da servizi che non appartengono a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="4e419-197">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="4e419-198">Nel registro di sistema è presente un elenco di gruppi di ordini di carico disponibili in:</span><span class="sxs-lookup"><span data-stu-id="4e419-198">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="4e419-199">**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="4e419-199">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="4e419-200">*LoadOrderGroupDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e419-200">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e419-201">Elenco di gruppi di ordini di caricamento che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-201">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="4e419-202">La matrice è con doppia terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="4e419-202">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="4e419-203">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="4e419-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="4e419-204">I nomi dei gruppi devono essere preceduti **dall' \_ \_ identificatore del gruppo SC** (definito nel file winsvc. h) per distinguerli dai nomi dei servizi, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4e419-204">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="4e419-205">La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="4e419-205">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-206">*ServiceDependencies* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e419-206">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e419-207">Elenco contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-207">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="4e419-208">La matrice è con doppia terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="4e419-208">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="4e419-209">Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze.</span><span class="sxs-lookup"><span data-stu-id="4e419-209">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="4e419-210">La dipendenza da un servizio indica che il servizio può essere eseguito solo se è in esecuzione il servizio da cui dipende.</span><span class="sxs-lookup"><span data-stu-id="4e419-210">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e419-211">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e419-211">Return value</span></span>

<span data-ttu-id="4e419-212">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="4e419-212">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="4e419-213">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="4e419-213">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4e419-214">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4e419-214">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4e419-215">**0**</span><span class="sxs-lookup"><span data-stu-id="4e419-215">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-216">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="4e419-216">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-217">**1**</span><span class="sxs-lookup"><span data-stu-id="4e419-217">**1**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-218">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="4e419-218">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-219">**2**</span><span class="sxs-lookup"><span data-stu-id="4e419-219">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-220">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="4e419-220">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-221">**3**</span><span class="sxs-lookup"><span data-stu-id="4e419-221">**3**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-222">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-222">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-223">**4**</span><span class="sxs-lookup"><span data-stu-id="4e419-223">**4**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-224">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-224">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-225">**5**</span><span class="sxs-lookup"><span data-stu-id="4e419-225">**5**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-226">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="4e419-226">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-227">**6**</span><span class="sxs-lookup"><span data-stu-id="4e419-227">**6**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-228">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="4e419-228">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-229">**7**</span><span class="sxs-lookup"><span data-stu-id="4e419-229">**7**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-230">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="4e419-230">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-231">**8**</span><span class="sxs-lookup"><span data-stu-id="4e419-231">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-232">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-232">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-233">**9**</span><span class="sxs-lookup"><span data-stu-id="4e419-233">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-234">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-234">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-235">**10**</span><span class="sxs-lookup"><span data-stu-id="4e419-235">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-236">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4e419-236">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-237">**11**</span><span class="sxs-lookup"><span data-stu-id="4e419-237">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-238">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="4e419-238">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-239">**12**</span><span class="sxs-lookup"><span data-stu-id="4e419-239">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-240">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4e419-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-241">**13**</span><span class="sxs-lookup"><span data-stu-id="4e419-241">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-242">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="4e419-242">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-243">**14**</span><span class="sxs-lookup"><span data-stu-id="4e419-243">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-244">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4e419-244">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-245">**15**</span><span class="sxs-lookup"><span data-stu-id="4e419-245">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-246">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4e419-246">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-247">**16**</span><span class="sxs-lookup"><span data-stu-id="4e419-247">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-248">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4e419-248">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-249">**17**</span><span class="sxs-lookup"><span data-stu-id="4e419-249">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-250">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4e419-250">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-251">**18**</span><span class="sxs-lookup"><span data-stu-id="4e419-251">**18**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-252">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="4e419-252">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-253">**19**</span><span class="sxs-lookup"><span data-stu-id="4e419-253">**19**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-254">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="4e419-254">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-255">**20**</span><span class="sxs-lookup"><span data-stu-id="4e419-255">**20**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-256">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="4e419-256">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-257">**21**</span><span class="sxs-lookup"><span data-stu-id="4e419-257">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-258">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-258">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-259">**22**</span><span class="sxs-lookup"><span data-stu-id="4e419-259">**22**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-260">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-260">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-261">**23**</span><span class="sxs-lookup"><span data-stu-id="4e419-261">**23**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-262">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4e419-262">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4e419-263">**24**</span><span class="sxs-lookup"><span data-stu-id="4e419-263">**24**</span></span>
</dt> <dd>

<span data-ttu-id="4e419-264">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4e419-264">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e419-265">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e419-265">Remarks</span></span>

<span data-ttu-id="4e419-266">All'avvio di un computer, vengono avviati anche tutti i servizi di avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="4e419-266">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="4e419-267">In alcuni casi, uno di questi servizi potrebbe non riuscire a avviarsi insieme al computer.</span><span class="sxs-lookup"><span data-stu-id="4e419-267">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="4e419-268">Quando un servizio ha esito negativo durante l'avvio del sistema, il computer esegue un'azione in base al valore del codice di controllo degli errori del servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-268">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="4e419-269">la maggior parte dei servizi viene installata usando il normale codice di controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="4e419-269">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="4e419-270">Alcune eccezioni, installate con il codice di errore ignore, includono:</span><span class="sxs-lookup"><span data-stu-id="4e419-270">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="4e419-271">Servizio Replica file</span><span class="sxs-lookup"><span data-stu-id="4e419-271">File Replication Service</span></span>
-   <span data-ttu-id="4e419-272">Smart card</span><span class="sxs-lookup"><span data-stu-id="4e419-272">Smart Card</span></span>
-   <span data-ttu-id="4e419-273">Accesso secondario</span><span class="sxs-lookup"><span data-stu-id="4e419-273">Secondary Logon</span></span>
-   <span data-ttu-id="4e419-274">WMI</span><span class="sxs-lookup"><span data-stu-id="4e419-274">WMI</span></span>

<span data-ttu-id="4e419-275">Per i servizi installati con il codice di errore ignore, non viene fornita alcuna notifica all'utente che indica che il servizio non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="4e419-275">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="4e419-276">Se si preferisce una notifica sullo schermo che non è stato possibile avviare un servizio, è possibile utilizzare WMI per modificare il codice di controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="4e419-276">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="4e419-277">I codici di controllo degli errori si applicano solo all'avvio del computer; i codici di controllo degli errori non vengono utilizzati se si arresta e si tenta di riavviare un servizio dopo che il computer è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4e419-277">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="4e419-278">In alcuni casi potrebbe essere necessario modificare l'account con cui viene eseguito un determinato servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-278">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="4e419-279">Ad esempio, è possibile eseguire un servizio con un account amministrativo.</span><span class="sxs-lookup"><span data-stu-id="4e419-279">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="4e419-280">Poiché questo può creare una vulnerabilità di sicurezza, è possibile passare il servizio a un account con meno privilegi.</span><span class="sxs-lookup"><span data-stu-id="4e419-280">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="4e419-281">In alternativa, è possibile che i servizi vengano eseguiti con un account che sta per essere eliminato oppure che sia necessario assicurarsi che, in tutti i server, determinati servizi vengano eseguiti con determinati account.</span><span class="sxs-lookup"><span data-stu-id="4e419-281">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="4e419-282">È possibile utilizzare il metodo **Change** della classe [**Win32 \_ TerminalService**](win32-terminalservice.md) per configurare i servizi per l'esecuzione con un account utente specificato.</span><span class="sxs-lookup"><span data-stu-id="4e419-282">You can use the **Change** method of the [**Win32\_TerminalService**](win32-terminalservice.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="4e419-283">Quando si seleziona un account, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="4e419-283">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="4e419-284">L'account usato come account del servizio deve avere il diritto di accedere come servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-284">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="4e419-285">Questo diritto può essere concesso usando Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="4e419-285">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="4e419-286">L'account utilizzato come account del servizio non deve essere un membro di un gruppo Administrators locale, di dominio o Enterprise.</span><span class="sxs-lookup"><span data-stu-id="4e419-286">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="4e419-287">Ogni istanza di un servizio deve essere eseguita con un account utente univoco.</span><span class="sxs-lookup"><span data-stu-id="4e419-287">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="4e419-288">In questo modo viene fornita una sicurezza aggiuntiva e viene abilitato il controllo delle singole istanze del servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-288">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="4e419-289">Se il servizio è interattivo, il servizio deve essere eseguito con l'account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="4e419-289">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="4e419-290">LocalSystem è necessario perché una sola finestra (WinSta0) può essere visibile e interattiva alla volta.</span><span class="sxs-lookup"><span data-stu-id="4e419-290">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="4e419-291">Se un servizio viene eseguito con un account diverso da LocalSystem, viene eseguito nel servizio-0x03E7 $ \\ Default Window Station, che è una finestra invisibile.</span><span class="sxs-lookup"><span data-stu-id="4e419-291">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="4e419-292">I servizi in esecuzione in questa finestra non possono ricevere output di input o di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4e419-292">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="4e419-293">Quando si assegna un account a un servizio, SCM richiede la password corretta per l'account prima di eseguire l'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="4e419-293">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="4e419-294">Se si fornisce una password non corretta, SCM rifiuta l'account.</span><span class="sxs-lookup"><span data-stu-id="4e419-294">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="4e419-295">Se si configura un account del servizio utilizzando l'account LocalSystem, LocalService o NetworkService, non è necessario specificare una password dell'account perché questi account non dispongono di password.</span><span class="sxs-lookup"><span data-stu-id="4e419-295">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="4e419-296">SCM archivia la password dell'account nel database dei servizi.</span><span class="sxs-lookup"><span data-stu-id="4e419-296">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="4e419-297">Dopo che la password è stata assegnata, tuttavia, SCM non garantisce che la password archiviata nel database dei servizi e la password assegnata all'account utente in Active Directory continuino a corrispondere.</span><span class="sxs-lookup"><span data-stu-id="4e419-297">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="4e419-298">Di conseguenza, potrebbe verificarsi una situazione simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="4e419-298">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="4e419-299">. Configurare un servizio per l'esecuzione con un account utente specifico.</span><span class="sxs-lookup"><span data-stu-id="4e419-299">.You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="4e419-300">Il servizio viene avviato con tale account utilizzando la password dell'account corrente.</span><span class="sxs-lookup"><span data-stu-id="4e419-300">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="4e419-301">Modificare la password per l'account utente.</span><span class="sxs-lookup"><span data-stu-id="4e419-301">You change the password for the user account.</span></span>
-   <span data-ttu-id="4e419-302">Il servizio continua a essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e419-302">The service continues to run.</span></span> <span data-ttu-id="4e419-303">Tuttavia, se il servizio viene arrestato, non è possibile riavviarlo perché SCM continua a usare la vecchia password non valida.</span><span class="sxs-lookup"><span data-stu-id="4e419-303">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="4e419-304">La modifica della password in Active Directory non comporta la modifica della password archiviata nel database dei servizi.</span><span class="sxs-lookup"><span data-stu-id="4e419-304">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="4e419-305">Se si eseguono servizi con account utente regolari, è necessario aggiornare le password del servizio ogni volta che viene modificata la password dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="4e419-305">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="4e419-306">Questa operazione può richiedere molto tempo se non si è certi di quali servizi sono in esecuzione con tale account o in quali computer sono in esecuzione i servizi con tale account.</span><span class="sxs-lookup"><span data-stu-id="4e419-306">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="4e419-307">Fortunatamente, è possibile utilizzare WMI per verificare gli account del servizio in tutti i computer e, se necessario, modificare la password dell'account del servizio.</span><span class="sxs-lookup"><span data-stu-id="4e419-307">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="4e419-308">Il [**parametro \_ LoadOrderGroup di Win32**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) rappresenta un gruppo di servizi di sistema che definiscono le dipendenze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4e419-308">The [**Win32\_LoadOrderGroup**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="4e419-309">I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento perché i servizi dipendono tra loro.</span><span class="sxs-lookup"><span data-stu-id="4e419-309">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="4e419-310">Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi precedenti.</span><span class="sxs-lookup"><span data-stu-id="4e419-310">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="4e419-311">Per modificare un servizio da un servizio di rete a un sistema locale, i parametri *StartName* e *StartPassword* devono avere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e419-311">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="4e419-312">Per modificare un servizio da un servizio di sistema locale a una rete, i parametri *StartName* e *StartPassword* devono avere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e419-312">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="4e419-313">Esempio</span><span class="sxs-lookup"><span data-stu-id="4e419-313">Examples</span></span>

<span data-ttu-id="4e419-314">Il codice VBScript seguente consente di modificare l'account del servizio per i servizi in esecuzione con un account utente specificato in LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="4e419-314">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change _
 ( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="4e419-315">Il codice VBScript seguente modifica la password dell'account del servizio per tutti gli script in esecuzione in netsvc</span><span class="sxs-lookup"><span data-stu-id="4e419-315">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="4e419-316">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e419-316">Requirements</span></span>



| <span data-ttu-id="4e419-317">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e419-317">Requirement</span></span> | <span data-ttu-id="4e419-318">Valore</span><span class="sxs-lookup"><span data-stu-id="4e419-318">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e419-319">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e419-319">Minimum supported client</span></span><br/> | <span data-ttu-id="4e419-320">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e419-320">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e419-321">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e419-321">Minimum supported server</span></span><br/> | <span data-ttu-id="4e419-322">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e419-322">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e419-323">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e419-323">Namespace</span></span><br/>                | <span data-ttu-id="4e419-324">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4e419-324">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4e419-325">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e419-325">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e419-326"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e419-326"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="4e419-327">MOF</span><span class="sxs-lookup"><span data-stu-id="4e419-327">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e419-328"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e419-328"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e419-329">DLL</span><span class="sxs-lookup"><span data-stu-id="4e419-329">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e419-330"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e419-330"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e419-331">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e419-331">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e419-332">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="4e419-332">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="4e419-333">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="4e419-333">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="4e419-334">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="4e419-334">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="4e419-335">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="4e419-335">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

