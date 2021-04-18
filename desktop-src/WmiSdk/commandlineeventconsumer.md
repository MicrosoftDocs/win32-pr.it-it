---
description: La classe CommandLineEventConsumer avvia un processo arbitrario nel sistema locale quando viene recapitato un evento.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: Classe CommandLineEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334364"
---
# <a name="commandlineeventconsumer-class"></a><span data-ttu-id="5e4c0-103">Classe CommandLineEventConsumer</span><span class="sxs-lookup"><span data-stu-id="5e4c0-103">CommandLineEventConsumer class</span></span>

<span data-ttu-id="5e4c0-104">La classe **CommandLineEventConsumer** avvia un processo arbitrario nel sistema locale quando viene recapitato un evento.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-104">The **CommandLineEventConsumer** class starts an arbitrary process in the local system when an event is delivered to it.</span></span> <span data-ttu-id="5e4c0-105">Questa classe è uno dei consumer di eventi standard forniti da WMI.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="5e4c0-106">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="5e4c0-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

> [!Note]  
> <span data-ttu-id="5e4c0-107">Quando si usa la classe **CommandLineEventConsumer** , proteggere il file eseguibile che si vuole avviare.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-107">When using the **CommandLineEventConsumer** class, secure the executable that you want to start.</span></span> <span data-ttu-id="5e4c0-108">Se il file eseguibile non si trova in un percorso sicuro o protetto con un elenco di controllo di accesso (ACL) sicuro, un utente non autorizzato può sostituire l'eseguibile con un eseguibile dannoso.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-108">If the executable is not in a secure location, or secured with a strong access control list (ACL), an unauthorized user can replace your executable with a malicious executable.</span></span> <span data-ttu-id="5e4c0-109">Per ulteriori informazioni sugli ACL, visitare la sezione relativa alla sicurezza di Microsoft Windows Software Development Kit (SDK) e vedere [creazione di un descrittore di sicurezza per un nuovo oggetto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="5e4c0-109">For more information about ACLs, visit the Security section of the Microsoft Windows Software Development Kit (SDK), and see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5e4c0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e4c0-110">Syntax</span></span>

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a><span data-ttu-id="5e4c0-111">Members</span><span class="sxs-lookup"><span data-stu-id="5e4c0-111">Members</span></span>

<span data-ttu-id="5e4c0-112">La classe **CommandLineEventConsumer** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5e4c0-112">The **CommandLineEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="5e4c0-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e4c0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e4c0-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e4c0-114">Properties</span></span>

<span data-ttu-id="5e4c0-115">La classe **CommandLineEventConsumer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-115">The **CommandLineEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e4c0-116">**CommandLineTemplate**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-116">**CommandLineTemplate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-119">Modello di stringa standard che specifica il processo da avviare.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-119">Standard string template that specifies the process to be started.</span></span> <span data-ttu-id="5e4c0-120">Questa proprietà può essere **null** e la proprietà **ExecutablePath** viene utilizzata come riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-120">This property can be **NULL**, and the **ExecutablePath** property is used as the command line.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-121">**CreateNewConsole**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-121">**CreateNewConsole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-122">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-124">Not used.</span></span> <span data-ttu-id="5e4c0-125">Se a questa proprietà viene assegnato un valore, viene generato un messaggio di traccia.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-125">If a value is assigned to this property, a tracing message is generated.</span></span> <span data-ttu-id="5e4c0-126">Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="5e4c0-126">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-127">**CreateNewProcessGroup**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-127">**CreateNewProcessGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-130">Se **true**, il nuovo processo è il processo radice di un nuovo gruppo di processi.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-130">If **True**, the new process is the root process of a new process group.</span></span> <span data-ttu-id="5e4c0-131">Il gruppo di processi include tutti i processi discendenti di questo processo radice.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-131">The process group includes all processes that are descendants of this root process.</span></span> <span data-ttu-id="5e4c0-132">L'identificatore di processo del nuovo gruppo di processi è uguale a questo identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-132">The process identifier of the new process group is the same as this process identifier.</span></span> <span data-ttu-id="5e4c0-133">I gruppi di processi vengono usati dal metodo [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) per consentire l'invio di un segnale CTRL + C o Ctrl + Break a un gruppo di processi della console.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-133">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable sending a CTRL+C or CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-134">**CreateSeparateWowVdm**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-134">**CreateSeparateWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-135">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-137">Se **true**, il nuovo processo viene eseguito in una macchina virtuale DOS privata (VDM).</span><span class="sxs-lookup"><span data-stu-id="5e4c0-137">If **True**, the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="5e4c0-138">Questa operazione è valida solo quando si avvia un'applicazione in esecuzione in un sistema operativo Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-138">This is only valid when starting an application running on a 16-bit Windows operating system.</span></span> <span data-ttu-id="5e4c0-139">Se è impostato su **false**, tutte le applicazioni in esecuzione su un sistema operativo Windows a 16 bit vengono eseguite come thread in un'unica VDM condivisa.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-139">If set to **False**, all applications running on a 16-bit Windows operating system run as threads in a single, shared VDM.</span></span> <span data-ttu-id="5e4c0-140">Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-140">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-141">**CreateSharedWowVdm**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-141">**CreateSharedWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-142">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-144">Se **true**, il metodo [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) esegue il nuovo processo nella macchina virtuale DOS condivisa (VDM).</span><span class="sxs-lookup"><span data-stu-id="5e4c0-144">If **True**, the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method runs the new process in the shared Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="5e4c0-145">Questa proprietà può eseguire l'override dell'opzione DefaultSeparateVDM nella sezione Windows di Win.ini se impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-145">This property can override the DefaultSeparateVDM switch in the Windows section of Win.ini if set to **True**.</span></span> <span data-ttu-id="5e4c0-146">Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-146">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-147">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-147">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-148">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-148">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-150">ID di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-150">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="5e4c0-151">WMI archivia il SID dell'utente che crea un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) o il SID Administrator, a seconda del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-151">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="5e4c0-152">Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-152">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="5e4c0-153">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="5e4c0-153">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-154">**Desktopname**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-154">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-157">Non usato.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-157">Not used.</span></span> <span data-ttu-id="5e4c0-158">Se a questa proprietà viene assegnato un valore, viene generato un messaggio di traccia.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-158">If a value is assigned to this property a tracing message is generated.</span></span> <span data-ttu-id="5e4c0-159">Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="5e4c0-159">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-160">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-160">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-163">Modulo da eseguire.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-163">Module to execute.</span></span> <span data-ttu-id="5e4c0-164">La stringa può specificare il percorso completo e il nome file del modulo da eseguire oppure può specificare un nome parziale.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-164">The string can specify the full path and file name of the module to execute, or it can specify a partial name.</span></span> <span data-ttu-id="5e4c0-165">Se viene specificato un nome parziale, si presuppone l'unità corrente e la directory corrente.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-165">If a partial name is specified, the current drive and current directory are assumed.</span></span>

<span data-ttu-id="5e4c0-166">La proprietà **ExecutablePath** può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-166">The **ExecutablePath** property can be **NULL**.</span></span> <span data-ttu-id="5e4c0-167">In tal caso, il nome del modulo deve essere il primo token delimitato da spazi vuoti nel valore della proprietà **CommandLineTemplate** .</span><span class="sxs-lookup"><span data-stu-id="5e4c0-167">In that case, the module name must be the first white space-delimited token in the **CommandLineTemplate** property value.</span></span> <span data-ttu-id="5e4c0-168">Se si utilizza un nome di file lungo che contiene uno spazio, utilizzare stringhe tra virgolette per indicare dove termina il nome file e gli argomenti iniziano a chiarire il nome del file.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-168">If using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin to clarify the file name.</span></span>

> [!Note]  
> <span data-ttu-id="5e4c0-169">Poiché la proprietà **CommandLineTemplate** può essere un modello in cui il modulo da eseguire viene fornito da una variabile, una proprietà **ExecutablePath** **null** consente il modulo specificato nel parametro da eseguire e quindi è fuori dal controllo.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-169">Because the **CommandLineTemplate** property can be a template where the module to execute is supplied by a variable, a **NULL** **ExecutablePath** property permits the module that is specified in the parameter to execute, and then it is out of your control.</span></span> <span data-ttu-id="5e4c0-170">Impostare sempre la proprietà **ExecutablePath** nella registrazione **CommandLineEventConsumer** per includere l'eseguibile richiesto, evitando la sovrascrittura da parte dei parametri degli eventi.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-170">Always set the **ExecutablePath** property in the **CommandLineEventConsumer** registration to include the required executable, which avoids overwriting by events parameters.</span></span> <span data-ttu-id="5e4c0-171">Se è necessario usare un modello e una variabile per specificare il modulo da eseguire, prestare attenzione agli utenti a cui vengono concessi i privilegi di scrittura completi nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-171">If you must use a template and variable to specify the module to execute, be careful about who is granted full write privilege in the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e4c0-172">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-172">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-173">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-175">Specifica il testo iniziale e i colori di sfondo se viene creata una nuova finestra della console in un'applicazione console</span><span class="sxs-lookup"><span data-stu-id="5e4c0-175">Specifies the initial text and background colors if a new console window is created in a console application</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-176">**FillAttributes**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-176">**FillAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-177">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-179">Testo iniziale e colori di sfondo, se viene creata una nuova finestra della console in un'applicazione console.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-179">Initial text and background colors, if a new console window is created in a console application.</span></span> <span data-ttu-id="5e4c0-180">Questa proprietà viene ignorata in un'applicazione GUI.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-180">This property is ignored in a GUI application.</span></span> <span data-ttu-id="5e4c0-181">Il valore può essere una qualsiasi combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-181">The value can be any combination of the following values.</span></span>

<dt>

<span data-ttu-id="5e4c0-182">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-182">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-183">primo piano blu</span><span class="sxs-lookup"><span data-stu-id="5e4c0-183">blue foreground</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-184">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-184">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-185">primo piano verde</span><span class="sxs-lookup"><span data-stu-id="5e4c0-185">green foreground</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-186">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-186">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-187">primo piano rosso</span><span class="sxs-lookup"><span data-stu-id="5e4c0-187">red foreground</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-188">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-188">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-189">intensità in primo piano</span><span class="sxs-lookup"><span data-stu-id="5e4c0-189">foreground intensity</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-190">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-190">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-191">sfondo blu</span><span class="sxs-lookup"><span data-stu-id="5e4c0-191">blue background</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-192">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-192">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-193">sfondo verde</span><span class="sxs-lookup"><span data-stu-id="5e4c0-193">green background</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-194">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-194">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-195">sfondo rosso</span><span class="sxs-lookup"><span data-stu-id="5e4c0-195">red background</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-196">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-196">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-197">intensità di sfondo</span><span class="sxs-lookup"><span data-stu-id="5e4c0-197">background intensity</span></span>

</dd> </dl>

<span data-ttu-id="5e4c0-198">Ad esempio, le combinazioni seguenti producono testo rosso su sfondo bianco:</span><span class="sxs-lookup"><span data-stu-id="5e4c0-198">For example, the following combinations produce red text on a white background:</span></span>


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  <span data-ttu-id="5e4c0-199">oppure</span><span class="sxs-lookup"><span data-stu-id="5e4c0-199">or</span></span>  


```mof
0x74
```



</dd> <dt>

<span data-ttu-id="5e4c0-200">**ForceOffFeedback**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-200">**ForceOffFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-201">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-203">Se **true**, il cursore del feedback viene forzato all'avvio del processo.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-203">If **True**, the feedback cursor is forced off while the process is starting.</span></span> <span data-ttu-id="5e4c0-204">Viene visualizzato il cursore normale.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-204">The normal cursor is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-205">**ForceOnFeedback**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-205">**ForceOnFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-206">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-208">Se **true**, il cursore è in modalità di feedback per due secondi dopo la chiamata a [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="5e4c0-208">If **True**, the cursor is in feedback mode for two seconds after [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) is called.</span></span> <span data-ttu-id="5e4c0-209">Durante questi due secondi, se il processo effettua la prima chiamata a GUI, il sistema fornisce cinque secondi per il processo.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-209">During those two seconds, if the process makes the first GUI call, the system gives five more seconds to the process.</span></span> <span data-ttu-id="5e4c0-210">Durante questi cinque secondi, se il processo Mostra una finestra, il sistema concede altri cinque secondi al processo per completare il disegno della finestra.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-210">During those five seconds, if the process shows a window, the system gives another five seconds to the process to finish drawing the window.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-211">**KillTimeout**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-211">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-212">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-214">Numero, in secondi, di attesa del servizio WMI prima di terminare un processo 0 (zero) indica che non è stato possibile terminare un processo.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-214">Number, in seconds, that the WMI service waits before killing a process 0 (zero) indicates a process is not to be killed.</span></span> <span data-ttu-id="5e4c0-215">L'arresto di un processo impedisce l'esecuzione illimitata di un processo.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-215">Killing a process prevents a process from running indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-216">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-216">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-219">Nome del computer a cui Strumentazione gestione Windows (WMI) Invia gli eventi.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-219">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="5e4c0-220">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="5e4c0-220">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-221">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-221">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-222">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-224">Numero massimo di code per un consumer specifico, in byte.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-224">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="5e4c0-225">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="5e4c0-225">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-226">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-229">Qualificatori: [ **chiave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-229">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-230">Nome univoco di un consumer.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-230">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-231">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-231">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-232">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-232">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-234">Pianificazione del livello di priorità dei thread di processo.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-234">Scheduling priority level of the process threads.</span></span> <span data-ttu-id="5e4c0-235">Nell'elenco seguente sono elencati i livelli di priorità disponibili.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-235">The following list lists the priority levels available.</span></span>

<dt>

<span data-ttu-id="5e4c0-236">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-236">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-237">Indica un processo normale senza necessità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-237">Indicates a normal process without scheduling needs.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-238">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-238">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-239">Indica un processo i cui thread vengono eseguiti solo quando il sistema è inattivo e vengono interrotti dai thread di qualsiasi processo in esecuzione in una classe di priorità superiore.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-239">Indicates a process whose threads run only when the system is idle, and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="5e4c0-240">Un esempio è un screen saver.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-240">An example is a screen saver.</span></span> <span data-ttu-id="5e4c0-241">La classe di priorità inattiva viene ereditata dai processi figlio.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-241">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-242">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-242">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-243">Indica un processo che esegue attività critiche in termini di priorità elevata.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-243">Indicates a process that performs high-priority, time critical tasks.</span></span> <span data-ttu-id="5e4c0-244">I thread di un processo di classe ad alta priorità hanno la precedenza sui thread dei processi di classe di priorità normale o di priorità di inattività.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-244">The threads of a high-priority class process preempts the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="5e4c0-245">Un esempio è il Elenco attività, che deve rispondere rapidamente quando viene chiamato dall'utente indipendentemente dal carico del sistema.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-245">An example is the Task List, which must respond quickly when called by the user regardless of the load on the system.</span></span> <span data-ttu-id="5e4c0-246">Prestare particolare attenzione quando si usa la classe con priorità alta, perché un'applicazione associata alla CPU con una classe con priorità alta può usare quasi tutti i cicli disponibili.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-246">Use extreme care when using the high-priority class, because a CPU-bound application with a high-priority class can use nearly all available cycles.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-247">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="5e4c0-247">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="5e4c0-248">Indica un processo con la massima priorità possibile.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-248">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="5e4c0-249">I thread di un processo della classe di priorità in tempo reale hanno la precedenza sui thread di tutti gli altri processi, inclusi i processi del sistema operativo che eseguono attività importanti.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-249">The threads of a real-time priority class process preempt the threads of all other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="5e4c0-250">Ad esempio, un processo in tempo reale eseguito per più di un breve intervallo può causare la mancata scaricamento delle cache del disco o la mancata risposta del mouse.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-250">For example, a real-time process that executes for more than a brief interval can cause disk caches not to flush, or cause the mouse to be unresponsive.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5e4c0-251">**RunInteractively**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-251">**RunInteractively**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-252">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-254">Se **true**, il processo viene avviato nella winstation interattiva.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-254">If **True**, the process is launched in the interactive WinStation.</span></span> <span data-ttu-id="5e4c0-255">Se **false**, il processo viene avviato nel servizio predefinito WinStation.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-255">If **False**, the process is launched in the default service WinStation.</span></span> <span data-ttu-id="5e4c0-256">Questa proprietà esegue l'override della proprietà **desktopname** .</span><span class="sxs-lookup"><span data-stu-id="5e4c0-256">This property overrides the **DesktopName** property.</span></span> <span data-ttu-id="5e4c0-257">Questa proprietà viene utilizzata solo localmente e solo se l'utente interattivo è lo stesso utente che ha configurato il consumer.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-257">This property is only used locally, and only if the interactive user is the same user who set up the consumer.</span></span>

<span data-ttu-id="5e4c0-258">A partire da Windows Vista, il processo che esegue l'istanza di **CommandLineEventConsumer** viene avviato con l'account **LocalSystem** e si trova nella sessione 0.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-258">Starting with Windows Vista, the process running the **CommandLineEventConsumer** instance is started under the **LocalSystem** account and is in session 0.</span></span> <span data-ttu-id="5e4c0-259">I servizi eseguiti nella sessione 0 non possono interagire con le sessioni utente.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-259">Services which run in session 0 cannot interact with user sessions.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-260">**ShowWindowCommand**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-260">**ShowWindowCommand**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-261">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-263">Mostra stato finestra.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-263">Window show state.</span></span> <span data-ttu-id="5e4c0-264">Può essere uno qualsiasi dei valori che possono essere specificati nel parametro *nCmdShow* per la funzione [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="5e4c0-264">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-265">**UseDefaultErrorMode**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-265">**UseDefaultErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-266">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-268">Se **true**, viene usata la modalità di errore predefinita.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-268">If **True**, the default error mode is used.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-269">**WindowTitle**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-269">**WindowTitle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-270">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-272">Titolo visualizzato sulla barra del titolo del processo.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-272">Title that appears on the title bar of the process.</span></span> <span data-ttu-id="5e4c0-273">Questa proprietà viene ignorata per le applicazioni GUI.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-273">This property is ignored for GUI applications.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-274">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-274">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-275">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-277">Directory di lavoro per questo processo.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-277">Working directory for this process.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-278">**XCoordinate**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-278">**XCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-279">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-281">Offset X, in pixel, dal bordo sinistro dello schermo al bordo sinistro della finestra, se viene creata una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-281">X-offset, in pixels, from the left edge of the screen to the left edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-282">**XNumCharacters**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-282">**XNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-283">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-285">Larghezza del buffer dello schermo, in colonne di tipo carattere, se viene creata una nuova finestra della console.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-285">Screen buffer width, in character columns, if a new console window is created.</span></span> <span data-ttu-id="5e4c0-286">Questa proprietà viene ignorata in un processo GUI.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-286">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-287">**XSize**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-287">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-288">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-290">Larghezza, in pixel, di una nuova finestra, se viene creata una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-290">Width, in pixels, of a new window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-291">**YCoordinate**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-291">**YCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-292">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-294">Offset Y, in pixel, dal bordo superiore dello schermo al bordo superiore della finestra, se viene creata una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-294">Y-offset, in pixels, from the top edge of the screen to the top edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-295">**YNumCharacters**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-295">**YNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-296">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-298">Altezza del buffer dello schermo, in righe di caratteri, se viene creata una nuova finestra della console.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-298">Screen buffer height, in character rows, if a new console window is created.</span></span> <span data-ttu-id="5e4c0-299">Questa proprietà viene ignorata in un processo GUI.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-299">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c0-300">**YSize**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-300">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4c0-301">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4c0-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e4c0-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e4c0-303">Altezza, in pixel, della nuova finestra, se viene creata una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-303">Height, in pixels, of the new window, if a new window is created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e4c0-304">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e4c0-304">Remarks</span></span>

<span data-ttu-id="5e4c0-305">La classe **CommandLineEventConsumer** è derivata dalla classe astratta [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="5e4c0-305">The **CommandLineEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="5e4c0-306">La proprietà **CreateSeparateWowVdm** indica se il nuovo processo viene eseguito in una macchina virtuale DOS privata (VDM).</span><span class="sxs-lookup"><span data-stu-id="5e4c0-306">The **CreateSeparateWowVdm** property indicates whether or not the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="5e4c0-307">Il vantaggio di eseguire separatamente è il fatto che un arresto anomalo termina solo il singolo VDM.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-307">The advantage of running separately is that a crash only terminates the single VDM.</span></span> <span data-ttu-id="5e4c0-308">I programmi in esecuzione in VDMs distinti continuano a funzionare normalmente e le applicazioni basate su Windows a 16 bit eseguite in VDMs separate hanno code di input separate.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-308">Programs running in distinct VDMs continue to function normally, and the 16-bit Windows-based applications running in separate VDMs have separate input queues.</span></span> <span data-ttu-id="5e4c0-309">Ciò significa che se un'applicazione smette di rispondere momentaneamente, le applicazioni in VDMs separate continuano a ricevere input.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-309">This means that if one application stops responding momentarily, the applications in separate VDMs continue to receive input.</span></span> <span data-ttu-id="5e4c0-310">Lo svantaggio dell'esecuzione separata è il fatto che richiede una quantità di memoria significativamente maggiore.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-310">The disadvantage of running separately is that it takes significantly more memory to do so.</span></span> <span data-ttu-id="5e4c0-311">È necessario impostare questa proprietà su **true** solo se l'utente richiede che le applicazioni basate su Windows a 16 bit vengano eseguite nel proprio VDM.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-311">You should set this property to **True** only if the user requests that 16-bit Windows-based applications run in their own VDM.</span></span>

> [!Note]  
> <span data-ttu-id="5e4c0-312">**CommandLineEventConsumer** utilizza internamente il metodo [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) e passa le proprietà **ExecutablePath** e **CommandLineTemplate** come parametri *lpApplicationName* e *lpCommandLine* .</span><span class="sxs-lookup"><span data-stu-id="5e4c0-312">The **CommandLineEventConsumer** uses the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method internally, and passes the **ExecutablePath** and **CommandLineTemplate** properties as the *lpApplicationName* and *lpCommandLine* parameters.</span></span> <span data-ttu-id="5e4c0-313">Nell'esempio di codice seguente Managed Object Format (MOF) non viene utilizzato correttamente **CommandLineEventConsumer** .</span><span class="sxs-lookup"><span data-stu-id="5e4c0-313">The following Managed Object Format (MOF) code example does not use **CommandLineEventConsumer** correctly.</span></span>

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="5e4c0-314">Il metodo [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) passa *lpCommandLine* come `argv[0]` , `argv[1]` e così via.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-314">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method passes *lpCommandLine* as `argv[0]`, `argv[1]`, and so on.</span></span> <span data-ttu-id="5e4c0-315">Poiché `argv[0]` per le applicazioni a 16 bit utilizzate per essere riservate al nome del file eseguibile, il codice MOF precedente comporta la creazione del processo come se il comando seguente venisse immesso al prompt dei comandi: **c: \\ Windows \\ system32 \\cscript.exe param1 param2**.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-315">Because `argv[0]` for 16-bit applications used to be reserved for the executable file name, the previous MOF code results in the process being created as though the following command is entered at the command prompt: **c:\\windows\\system32\\cscript.exe param1 param2**.</span></span>

<span data-ttu-id="5e4c0-316">Il comando precedente non ha esito positivo perché Cscript.exe non è in grado di osservare `argv[0]` , quindi non riconosce che non contiene il proprio nome, ma un altro ("c: \\ \\ Scripts \\ \\MyScript.js").</span><span class="sxs-lookup"><span data-stu-id="5e4c0-316">The previous command does not succeed because Cscript.exe does not look at `argv[0]`, and so it does not recognize that it does not contain its own name, but something else ("c:\\\\scripts\\\\MyScript.js").</span></span> <span data-ttu-id="5e4c0-317">Nell'esempio seguente viene identificato l'utilizzo consigliato di **CommandLineEventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-317">The following example identifies the recommended use of **CommandLineEventConsumer**.</span></span>


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="5e4c0-318">L'uso precedente di **CommandLineEventConsumer** genera il processo creato come se il comando seguente venisse immesso al prompt dei comandi: **c: \\ Windows \\ system32 \\cscript.exe c: \\ Scripts \\MyScript.js param1 param2**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-318">The previous use of **CommandLineEventConsumer** results in the process created as though the following command was entered at the command prompt: **c:\\windows\\system32\\cscript.exe c:\\scripts\\MyScript.js param1 param2**</span></span>

<span data-ttu-id="5e4c0-319">Poiché "c: \\ \\ scripts \\ \\MyScript.js" è ora `argv[1]` visibile da Cscript.exe e il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5e4c0-319">Because "c:\\\\scripts\\\\MyScript.js" is now `argv[1]`, it is seen by Cscript.exe and the command succeeds.</span></span>

<span data-ttu-id="5e4c0-320">Per ulteriori informazioni, vedere la funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="5e4c0-320">For more information, see the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="5e4c0-321">Esempio</span><span class="sxs-lookup"><span data-stu-id="5e4c0-321">Examples</span></span>

<span data-ttu-id="5e4c0-322">Per un esempio dell'uso di **CommandLineEventConsumer** per creare un consumer, vedere [esecuzione di un programma dalla riga di comando in base a un evento](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="5e4c0-322">For an example of using **CommandLineEventConsumer** to create a consumer, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e4c0-323">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e4c0-323">Requirements</span></span>



| <span data-ttu-id="5e4c0-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e4c0-324">Requirement</span></span> | <span data-ttu-id="5e4c0-325">Valore</span><span class="sxs-lookup"><span data-stu-id="5e4c0-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e4c0-326">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e4c0-326">Minimum supported client</span></span><br/> | <span data-ttu-id="5e4c0-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e4c0-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e4c0-328">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e4c0-328">Minimum supported server</span></span><br/> | <span data-ttu-id="5e4c0-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e4c0-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e4c0-330">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5e4c0-330">Namespace</span></span><br/>                | <span data-ttu-id="5e4c0-331">\\Sottoscrizione radice</span><span class="sxs-lookup"><span data-stu-id="5e4c0-331">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="5e4c0-332">MOF</span><span class="sxs-lookup"><span data-stu-id="5e4c0-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e4c0-333"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e4c0-333"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e4c0-334">DLL</span><span class="sxs-lookup"><span data-stu-id="5e4c0-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e4c0-335"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e4c0-335"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e4c0-336">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e4c0-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e4c0-337">Classi consumer standard</span><span class="sxs-lookup"><span data-stu-id="5e4c0-337">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="5e4c0-338">Monitoraggio e risposta agli eventi con consumer standard</span><span class="sxs-lookup"><span data-stu-id="5e4c0-338">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="5e4c0-339">Creazione di un consumer logico</span><span class="sxs-lookup"><span data-stu-id="5e4c0-339">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="5e4c0-340">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="5e4c0-340">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="5e4c0-341">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="5e4c0-341">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

