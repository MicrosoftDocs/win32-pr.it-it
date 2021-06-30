---
description: La sessione di traccia eventi autologger registra gli eventi che si verificano nelle prime fasi del processo di avvio del sistema operativo.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Configurazione e avvio di una sessione di autologger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6560aece87506b1d064981ee5f49a56bbf0da19e
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102040"
---
# <a name="configuring-and-starting-an-autologger-session"></a><span data-ttu-id="55a21-103">Configurazione e avvio di una sessione di autologger</span><span class="sxs-lookup"><span data-stu-id="55a21-103">Configuring and Starting an AutoLogger Session</span></span>

<span data-ttu-id="55a21-104">La sessione di traccia eventi autologger registra gli eventi che si verificano nelle prime fasi del processo di avvio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="55a21-104">The AutoLogger event tracing session records events that occur early in the operating system boot process.</span></span> <span data-ttu-id="55a21-105">Le applicazioni e i driver di dispositivo possono usare la sessione AutoLogger per acquisire le tracce prima che l'utente esezioni l'accesso.</span><span class="sxs-lookup"><span data-stu-id="55a21-105">Applications and device drivers can use the AutoLogger session to capture traces before the user logs in.</span></span> <span data-ttu-id="55a21-106">Si noti che alcuni driver di dispositivo, ad esempio i driver di dispositivo del disco, non vengono caricati all'inizio della sessione di AutoLogger.</span><span class="sxs-lookup"><span data-stu-id="55a21-106">Note that some device drivers, such as disk device drivers, are not loaded at the time the AutoLogger session begins.</span></span>

<span data-ttu-id="55a21-107">AutoLogger differisce dal logger globale nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="55a21-107">The AutoLogger differs from the Global Logger in the following ways:</span></span>

-   <span data-ttu-id="55a21-108">È possibile specificare una o più sessioni autologger (il logger globale è una singola sessione in cui tutti gli utenti hanno registrato gli eventi).</span><span class="sxs-lookup"><span data-stu-id="55a21-108">You can specify one or more AutoLogger sessions (the Global Logger was a single session to which everyone logged events).</span></span>
-   <span data-ttu-id="55a21-109">AutoLogger invia una notifica di abilitazione ai provider all'avvio della sessione (il logger globale non ha inviato una notifica di abilitazione ai provider, quindi i provider dovevano basarsi su altri mezzi per sapere se la sessione del logger globale è stata avviata per iniziare a registrare gli eventi).</span><span class="sxs-lookup"><span data-stu-id="55a21-109">The AutoLogger sends an enable notification to the providers when the session starts (the Global Logger did not send an enable notification to the providers, so the providers had to rely on other means to know if the Global Logger session was started in order to begin logging events).</span></span>
-   <span data-ttu-id="55a21-110">AutoLogger non supporta la registrazione degli eventi del logger del kernel NT (vedere il **membro EnableFlags** di [**EVENT TRACE \_ \_ PROPERTIES).**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)</span><span class="sxs-lookup"><span data-stu-id="55a21-110">The AutoLogger does not support logging NT Kernel Logger events (see the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span></span> <span data-ttu-id="55a21-111">Per registrare gli eventi del logger del kernel NT, è necessario usare [il logger globale](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="55a21-111">To log NT Kernel Logger events, you must use the [Global Logger](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="55a21-112">Per altre informazioni sulla seesion del logger globale, vedere [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="55a21-112">For more information on the Global Logger seesion, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

> [!Note]  
> <span data-ttu-id="55a21-113">ETW supporta autologger in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="55a21-113">ETW supports the AutoLogger on Windows Vista and later.</span></span> <span data-ttu-id="55a21-114">Usare il [logger globale](configuring-and-starting-the-global-logger-session.md) nei sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="55a21-114">Use the [Global Logger](configuring-and-starting-the-global-logger-session.md) on earlier operating systems.</span></span>

 

<span data-ttu-id="55a21-115">Usare il Registro di sistema per configurare la sessione autologger.</span><span class="sxs-lookup"><span data-stu-id="55a21-115">You use the registry to configure the AutoLogger session.</span></span> <span data-ttu-id="55a21-116">Aggiungere la chiave del Registro di sistema seguente, se non è già presente:</span><span class="sxs-lookup"><span data-stu-id="55a21-116">Add the following registry key, if it is not already present:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

<span data-ttu-id="55a21-117">Nella chiave **Autologger** creare una chiave per ogni sessione di AutoLogger che si vuole configurare, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="55a21-117">Under the **Autologger** key create a key for each AutoLogger session that you want to configure as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="55a21-118">Per ogni sessione, creare una chiave per ogni provider che si desidera abilitare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="55a21-118">For each session, create a key for each provider that you want to enable to the session.</span></span> <span data-ttu-id="55a21-119">Usare il GUID del provider come chiave.</span><span class="sxs-lookup"><span data-stu-id="55a21-119">Use the provider's GUID as the key.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="55a21-120">Nella tabella seguente vengono descritti i valori che è possibile definire per ogni sessione di AutoLogger.</span><span class="sxs-lookup"><span data-stu-id="55a21-120">The following table describes the values that you can define for each AutoLogger session.</span></span> <span data-ttu-id="55a21-121">Per specificare questi valori del Registro di sistema, è necessario disporre dei privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="55a21-121">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="55a21-122">I **valori Start** e **Guid** sono gli unici valori necessari per avviare la sessione di AutoLogger. Tutti gli altri valori hanno impostazioni predefinite che vengono usate se il valore non è presente nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="55a21-122">The **Start** and **Guid** value are the only values required to start the AutoLogger session; all other values have default settings that are used if the value is not present in the registry.</span></span> <span data-ttu-id="55a21-123">In genere, è consigliabile usare i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="55a21-123">Typically, you should use the default values.</span></span> <span data-ttu-id="55a21-124">Se si specifica un valore che ETW non può supportare, ETW eseguirà l'override del valore.</span><span class="sxs-lookup"><span data-stu-id="55a21-124">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55a21-125">Valore</span><span class="sxs-lookup"><span data-stu-id="55a21-125">Value</span></span></th>
<th><span data-ttu-id="55a21-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="55a21-126">Type</span></span></th>
<th><span data-ttu-id="55a21-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55a21-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55a21-128"><strong>BufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-128"><strong>BufferSize</strong></span></span></td>
<td><span data-ttu-id="55a21-129"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-129"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-130">Dimensioni di ogni buffer, in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="55a21-130">The size of each buffer, in kilobytes.</span></span> <span data-ttu-id="55a21-131">Deve essere minore di un megabyte.</span><span class="sxs-lookup"><span data-stu-id="55a21-131">Should be less than one megabyte.</span></span> <span data-ttu-id="55a21-132">ETW usa le dimensioni della memoria fisica per calcolare questo valore.</span><span class="sxs-lookup"><span data-stu-id="55a21-132">ETW uses the size of physical memory to calculate this value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a21-133"><strong>Tipo di orologio</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-133"><strong>ClockType</strong></span></span></td>
<td><span data-ttu-id="55a21-134"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-134"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-135">Timer da usare per la registrazione del timestamp per ogni evento.</span><span class="sxs-lookup"><span data-stu-id="55a21-135">The timer to use when logging the time stamp for each event.</span></span>
<ul>
<li><span data-ttu-id="55a21-136">1 = Valore del contatore delle prestazioni (risoluzione elevata)</span><span class="sxs-lookup"><span data-stu-id="55a21-136">1 = Performance counter value (high resolution)</span></span></li>
<li><span data-ttu-id="55a21-137">2 = Timer di sistema</span><span class="sxs-lookup"><span data-stu-id="55a21-137">2 = System timer</span></span></li>
<li><span data-ttu-id="55a21-138">3 = Contatore ciclo CPU</span><span class="sxs-lookup"><span data-stu-id="55a21-138">3 = CPU cycle counter</span></span></li>
</ul>
<span data-ttu-id="55a21-139">Per una descrizione di ogni tipo di orologio, vedere il <strong>membro ClientContext</strong> <a href="wnode-header.md"><strong>di WNODE_HEADER</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="55a21-139">For a description of each clock type, see the <strong>ClientContext</strong> member of <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span></span><br/> <span data-ttu-id="55a21-140">Il valore predefinito è 1 (valore del contatore delle prestazioni) in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="55a21-140">The default value is 1 (performance counter value) on Windows Vista and later.</span></span> <span data-ttu-id="55a21-141">Prima di Windows Vista, il valore predefinito è 2 (timer di sistema).</span><span class="sxs-lookup"><span data-stu-id="55a21-141">Prior to Windows Vista, the default value is 2 (system timer).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a21-142"><strong>DisableRealtimePersistence</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-142"><strong>DisableRealtimePersistence</strong></span></span></td>
<td><span data-ttu-id="55a21-143"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-143"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-144">Per disabilitare la persistenza in tempo reale, impostare questo valore su 1.</span><span class="sxs-lookup"><span data-stu-id="55a21-144">To disable real time persistence, set this value to 1.</span></span> <span data-ttu-id="55a21-145">Il valore predefinito è 0 (abilitato) per le sessioni in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="55a21-145">The default is 0 (enabled) for real time sessions.</span></span><br/> <span data-ttu-id="55a21-146">Se è abilitata la persistenza in tempo reale, gli eventi in tempo reale che non sono stati recapitati al momento dell'arresto del computer verranno resi persistenti.</span><span class="sxs-lookup"><span data-stu-id="55a21-146">If real time persistence is enabled, real-time events that were not delivered by the time the computer was shutdown will be persisted.</span></span> <span data-ttu-id="55a21-147">Gli eventi verranno quindi recapitati al consumer alla successiva connessione del consumer alla sessione.</span><span class="sxs-lookup"><span data-stu-id="55a21-147">The events will then be delivered to the consumer the next time the consumer connects to the session.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a21-148"><strong>FileCounter</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-148"><strong>FileCounter</strong></span></span></td>
<td><span data-ttu-id="55a21-149"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-149"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-150">Non impostare o modificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="55a21-150">Do not set or modify this value.</span></span> <span data-ttu-id="55a21-151">Questo valore è il numero di serie usato per incrementare il nome del file di log se <strong>è specificato FileMax.</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-151">This value is the serial number used to increment the log file name if <strong>FileMax</strong> is specified.</span></span> <span data-ttu-id="55a21-152">Se il valore non è valido, verrà utilizzato 1.</span><span class="sxs-lookup"><span data-stu-id="55a21-152">If the value is not valid, 1 will be assumed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a21-153"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-153"><strong>FileName</strong></span></span></td>
<td><span data-ttu-id="55a21-154"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-154"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="55a21-155">Percorso completo del file di log.</span><span class="sxs-lookup"><span data-stu-id="55a21-155">The fully qualified path of the log file.</span></span> <span data-ttu-id="55a21-156">Il percorso di questo file deve esistere.</span><span class="sxs-lookup"><span data-stu-id="55a21-156">The path to this file must exist.</span></span> <span data-ttu-id="55a21-157">Il file di log è un file di log sequenziale.</span><span class="sxs-lookup"><span data-stu-id="55a21-157">The log file is a sequential log file.</span></span> <span data-ttu-id="55a21-158">Il percorso è limitato a 1024 caratteri.</span><span class="sxs-lookup"><span data-stu-id="55a21-158">The path is limited to 1024 characters.</span></span><br/> <span data-ttu-id="55a21-159">Se <strong>FileName</strong> non viene specificato, gli eventi vengono scritti in %SystemRoot%\System32\LogFiles\WMI \& lt;sessionname &gt; .etl.</span><span class="sxs-lookup"><span data-stu-id="55a21-159">If <strong>FileName</strong> is not specified, events are written to %SystemRoot%\System32\LogFiles\WMI\&lt;sessionname&gt;.etl.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a21-160"><strong>FileMax</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-160"><strong>FileMax</strong></span></span></td>
<td><span data-ttu-id="55a21-161"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-161"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-162">Numero massimo di istanze del file di log create da ETW.</span><span class="sxs-lookup"><span data-stu-id="55a21-162">The maximum number of instances of the log file that ETW creates.</span></span> <span data-ttu-id="55a21-163">Se il file di log specificato in <strong>FileName</strong> esiste, ETW aggiunge il <strong>valore FileCounter</strong> al nome del file.</span><span class="sxs-lookup"><span data-stu-id="55a21-163">If the log file specified in <strong>FileName</strong> exists, ETW appends the <strong>FileCounter</strong> value to the file name.</span></span> <span data-ttu-id="55a21-164">Ad esempio, se si usa il nome del file di log predefinito, il formato sarà %SystemRoot%\System32\LogFiles\WMI \& lt;nome sessione &gt; .etl. Nnnn.</span><span class="sxs-lookup"><span data-stu-id="55a21-164">For example, if the default log file name is used, the form is %SystemRoot%\System32\LogFiles\WMI\&lt;sessionname&gt;.etl.NNNN.</span></span> <br/> <span data-ttu-id="55a21-165">La prima volta che il computer viene avviato, il nome del file è sessionname .etl.0001, la seconda volta il nome del file è &lt; &gt; &lt; sessionname &gt; .etl.0002 e così via.</span><span class="sxs-lookup"><span data-stu-id="55a21-165">The first time the computer is started, the file name is &lt;sessionname&gt;.etl.0001, the second time the file name is &lt;sessionname&gt;.etl.0002, and so on.</span></span> <span data-ttu-id="55a21-166">Se <strong>FileMax</strong> è 3, al quarto riavvio del computer ETW reimposta il contatore su 1 e sovrascrive il nome sessione &lt; &gt; .etl.0001, se esistente.</span><span class="sxs-lookup"><span data-stu-id="55a21-166">If <strong>FileMax</strong> is 3, on the fourth restart of the computer, ETW resets the counter to 1 and overwrites &lt;sessionname&gt;.etl.0001, if it exists.</span></span><br/> <span data-ttu-id="55a21-167">Il numero massimo di istanze del file di log supportate è 16.</span><span class="sxs-lookup"><span data-stu-id="55a21-167">The maximum number of instances of the log file that are supported is 16.</span></span><br/> <span data-ttu-id="55a21-168">Non utilizzare questa funzionalità con la modalità <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> file di log.</span><span class="sxs-lookup"><span data-stu-id="55a21-168">Do not use this feature with the <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> log file mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a21-169"><strong>FlushTimer</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-169"><strong>FlushTimer</strong></span></span></td>
<td><span data-ttu-id="55a21-170"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-170"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-171">Frequenza, in secondi, con cui i buffer di traccia vengono scaricati forzatamente.</span><span class="sxs-lookup"><span data-stu-id="55a21-171">How often, in seconds, the trace buffers are forcibly flushed.</span></span> <span data-ttu-id="55a21-172">Il tempo di scaricamento minimo è di 1 secondo.</span><span class="sxs-lookup"><span data-stu-id="55a21-172">The minimum flush time is 1 second.</span></span> <span data-ttu-id="55a21-173">Questo scaricamento forzato si aggiunge allo scaricamento automatico che si verifica quando un buffer è pieno e quando la sessione di traccia si arresta.</span><span class="sxs-lookup"><span data-stu-id="55a21-173">This forced flush is in addition to the automatic flush that occurs when a buffer is full and when the trace session stops.</span></span> <br/> <span data-ttu-id="55a21-174">Nel caso di un logger in tempo reale, un valore pari a zero (valore predefinito) indica che l'ora di scaricamento verrà impostata su 1 secondo.</span><span class="sxs-lookup"><span data-stu-id="55a21-174">For the case of a real-time logger, a value of zero (the default value) means that the flush time will be set to 1 second.</span></span> <span data-ttu-id="55a21-175">Un logger in tempo reale è quando <strong>LogFileMode è</strong> impostato <strong>su EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="55a21-175">A real-time logger is when <strong>LogFileMode</strong> is set to <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="55a21-176">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="55a21-176">The default value is 0.</span></span> <span data-ttu-id="55a21-177">Per impostazione predefinita, i buffer vengono scaricati solo quando sono pieni.</span><span class="sxs-lookup"><span data-stu-id="55a21-177">By default, buffers are flushed only when they are full.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a21-178"><strong>Guid</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-178"><strong>Guid</strong></span></span></td>
<td><span data-ttu-id="55a21-179"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-179"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="55a21-180">Stringa contenente un GUID che identifica in modo univoco la sessione.</span><span class="sxs-lookup"><span data-stu-id="55a21-180">A string that contains a GUID that uniquely identifies the session.</span></span> <span data-ttu-id="55a21-181">Questo valore è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="55a21-181">This value is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a21-182"><strong>LogFileMode</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-182"><strong>LogFileMode</strong></span></span></td>
<td><span data-ttu-id="55a21-183"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-183"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-184">Specificare una o più modalità di log.</span><span class="sxs-lookup"><span data-stu-id="55a21-184">Specify one or more log modes.</span></span> <span data-ttu-id="55a21-185">Per i valori possibili, vedere <a href="logging-mode-constants.md">Costanti della modalità di registrazione.</a></span><span class="sxs-lookup"><span data-stu-id="55a21-185">For possible values, see <a href="logging-mode-constants.md">Logging Mode Constants</a>.</span></span> <span data-ttu-id="55a21-186">Il valore predefinito <strong>è EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="55a21-186">The default is <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span></span> <span data-ttu-id="55a21-187">Anziché scrivere in un file di log, è possibile specificare EVENT_TRACE_BUFFERING_MODE <strong>o</strong> <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="55a21-187">Instead of writing to a log file, you can specify either <strong>EVENT_TRACE_BUFFERING_MODE</strong> or <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="55a21-188">Specificando <strong>EVENT_TRACE_BUFFERING_MODE</strong> si evita il costo dello scaricamento del contenuto della sessione su disco quando il file system diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="55a21-188">Specifying <strong>EVENT_TRACE_BUFFERING_MODE</strong> avoids the cost of flushing the contents of the session to disk when the file system becomes available.</span></span> <br/> <span data-ttu-id="55a21-189">Si noti che <strong>EVENT_TRACE_BUFFERING_MODE</strong> il sistema ignorerà il valore <strong>MaximumBuffers,</strong> perché le dimensioni del buffer sono invece il prodotto di <strong>MinimumBuffers</strong> e <strong>BufferSize.</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-189">Note that using <strong>EVENT_TRACE_BUFFERING_MODE</strong> will cause the system to ignore the <strong>MaximumBuffers</strong> value, as the buffer size is instead the product of <strong>MinimumBuffers</strong> and <strong>BufferSize</strong>.</span></span><br/> <span data-ttu-id="55a21-190">Le sessioni autologger non supportano la <strong>modalità EVENT_TRACE_FILE_MODE_NEWFILE</strong> registrazione automatica.</span><span class="sxs-lookup"><span data-stu-id="55a21-190">AutoLogger sessions do not support the <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> logging mode.</span></span><br/> <span data-ttu-id="55a21-191">Se <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> specificato, <strong>BufferSize</strong> deve essere specificato in modo esplicito e deve essere lo stesso sia nel logger che nel file da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="55a21-191">If <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> is specified, <strong>BufferSize</strong> must be explicitly provided and must be the same in both the logger and the file being appended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a21-192"><strong>Maxfilesize</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-192"><strong>MaxFileSize</strong></span></span></td>
<td><span data-ttu-id="55a21-193"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-193"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-194">Dimensioni massime del file di log, in megabyte.</span><span class="sxs-lookup"><span data-stu-id="55a21-194">The maximum file size of the log file, in megabytes.</span></span> <span data-ttu-id="55a21-195">La sessione viene chiusa quando viene raggiunta la dimensione massima, a meno che non si sia in modalità file di log circolare.</span><span class="sxs-lookup"><span data-stu-id="55a21-195">The session is closed when the maximum size is reached, unless you are in circular log file mode.</span></span> <span data-ttu-id="55a21-196">Per non specificare alcun limite, impostare il valore su 0.</span><span class="sxs-lookup"><span data-stu-id="55a21-196">To specify no limit, set value to 0.</span></span> <span data-ttu-id="55a21-197">Il valore predefinito è 100 MB, se non impostato.</span><span class="sxs-lookup"><span data-stu-id="55a21-197">The default is 100 MB, if not set.</span></span> <span data-ttu-id="55a21-198">Il comportamento che si verifica quando viene raggiunta la dimensione massima del file dipende dal valore di <strong>LogFileMode</strong>.</span><span class="sxs-lookup"><span data-stu-id="55a21-198">The behavior that occurs when the maximum file size is reached depends on the value of <strong>LogFileMode</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a21-199"><strong>MaximumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-199"><strong>MaximumBuffers</strong></span></span></td>
<td><span data-ttu-id="55a21-200"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-200"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-201">Numero massimo di buffer da allocare.</span><span class="sxs-lookup"><span data-stu-id="55a21-201">The maximum number of buffers to allocate.</span></span> <span data-ttu-id="55a21-202">In genere, questo valore è il numero minimo di buffer più venti.</span><span class="sxs-lookup"><span data-stu-id="55a21-202">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="55a21-203">ETW usa le dimensioni del buffer e la dimensione della memoria fisica per calcolare questo valore.</span><span class="sxs-lookup"><span data-stu-id="55a21-203">ETW uses the buffer size and the size of physical memory to calculate this value.</span></span> <span data-ttu-id="55a21-204">Questo valore deve essere maggiore o uguale al valore per <strong>MinimumBuffers.</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-204">This value must be greater than or equal to the value for <strong>MinimumBuffers</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a21-205"><strong>MinimumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-205"><strong>MinimumBuffers</strong></span></span></td>
<td><span data-ttu-id="55a21-206"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-206"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-207">Numero minimo di buffer da allocare all'avvio.</span><span class="sxs-lookup"><span data-stu-id="55a21-207">The minimum number of buffers to allocate at startup.</span></span> <span data-ttu-id="55a21-208">Il numero minimo di buffer che è possibile specificare è due buffer per processore.</span><span class="sxs-lookup"><span data-stu-id="55a21-208">The minimum number of buffers that you can specify is two buffers per processor.</span></span> <span data-ttu-id="55a21-209">In un computer a processore singolo, ad esempio, il numero minimo di buffer è due.</span><span class="sxs-lookup"><span data-stu-id="55a21-209">For example, on a single processor computer, the minimum number of buffers is two.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a21-210"><strong>Inizia</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-210"><strong>Start</strong></span></span></td>
<td><span data-ttu-id="55a21-211"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-211"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-212">Per fare in modo che la sessione autologger venga avviata al successivo riavvio del computer, impostare questo valore su 1. In caso contrario, impostare questo valore su 0.</span><span class="sxs-lookup"><span data-stu-id="55a21-212">To have the AutoLogger session start the next time the computer is restarted, set this value to 1; otherwise, set this value to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a21-213"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-213"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="55a21-214"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-214"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-215">Stato di avvio di AutoLogger.</span><span class="sxs-lookup"><span data-stu-id="55a21-215">The startup status of the AutoLogger.</span></span> <span data-ttu-id="55a21-216">Se l'avvio di AutoLogger non è riuscito, il valore di questa chiave è il codice di errore Win32 appropriato.</span><span class="sxs-lookup"><span data-stu-id="55a21-216">If the AutoLogger failed to start, the value of this key is the appropriate Win32 error code.</span></span> <span data-ttu-id="55a21-217">Se AutoLogger è stato avviato correttamente, <strong></strong> il valore di questa chiave ERROR_SUCCESS (0).</span><span class="sxs-lookup"><span data-stu-id="55a21-217">If the AutoLogger successfully started, the value of this key is <strong>ERROR_SUCCESS</strong> (0).</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="55a21-218">Nella tabella seguente vengono descritti i valori che è possibile definire per ogni provider che si desidera abilitare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="55a21-218">The following table describes the values that you can define for each provider that you want to enable to your session.</span></span> <span data-ttu-id="55a21-219">Per specificare questi valori del Registro di sistema, è necessario disporre dei privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="55a21-219">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="55a21-220">Se si specifica un valore che ETW non può supportare, ETW eseguirà l'override del valore.</span><span class="sxs-lookup"><span data-stu-id="55a21-220">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55a21-221">Valore</span><span class="sxs-lookup"><span data-stu-id="55a21-221">Value</span></span></th>
<th><span data-ttu-id="55a21-222">Tipo</span><span class="sxs-lookup"><span data-stu-id="55a21-222">Type</span></span></th>
<th><span data-ttu-id="55a21-223">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55a21-223">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55a21-224"><strong>Enabled</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-224"><strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="55a21-225"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-225"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-226">Determina se il provider è abilitato.</span><span class="sxs-lookup"><span data-stu-id="55a21-226">Determines if the provider is enabled.</span></span> <span data-ttu-id="55a21-227">Per abilitare il provider, impostare questo valore su 1.</span><span class="sxs-lookup"><span data-stu-id="55a21-227">To enable the provider, set this value to 1.</span></span> <span data-ttu-id="55a21-228">Per disabilitare il provider, impostare questo valore su 0.</span><span class="sxs-lookup"><span data-stu-id="55a21-228">To disable the provider, set this value to 0.</span></span> <span data-ttu-id="55a21-229">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="55a21-229">The default is 0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a21-230"><strong>EnableFlags</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-230"><strong>EnableFlags</strong></span></span></td>
<td><span data-ttu-id="55a21-231"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-231"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-232">Valore definito dal provider che specifica la classe di eventi per cui il provider genera eventi.</span><span class="sxs-lookup"><span data-stu-id="55a21-232">Provider-defined value that specifies the class of events for which the provider generates events.</span></span> <span data-ttu-id="55a21-233">Per informazioni dettagliate, <em>vedere il parametro EnableFlags</em> della <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>funzione EnableTrace.</strong></a></span><span class="sxs-lookup"><span data-stu-id="55a21-233">For details, see the <em>EnableFlags</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> function.</span></span> <span data-ttu-id="55a21-234">Specificare questo nome di valore se il provider non supporta <strong>MatchAnyKeyword</strong> <strong>o MatchAllKeyword</strong>.</span><span class="sxs-lookup"><span data-stu-id="55a21-234">Specify this value name if the provider does not support <strong>MatchAnyKeyword</strong> or <strong>MatchAllKeyword</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a21-235"><strong>EnableLevel</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-235"><strong>EnableLevel</strong></span></span></td>
<td><span data-ttu-id="55a21-236"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-236"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-237">Valore definito dal provider che specifica il livello di dettaglio incluso nell'evento.</span><span class="sxs-lookup"><span data-stu-id="55a21-237">Provider-defined value that specifies the level of detail included in the event.</span></span> <span data-ttu-id="55a21-238">Ad esempio, è possibile utilizzare questo valore per indicare il livello di gravità degli eventi (informativo, di avviso, di errore) generati dal provider.</span><span class="sxs-lookup"><span data-stu-id="55a21-238">For example, you can use this value to indicate the severity level of the events (informational, warning, error) that the provider generates.</span></span> <span data-ttu-id="55a21-239">Per un elenco dei livelli predefiniti, vedere il <em>parametro level</em> della <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>funzione EnableTraceEx.</strong></a></span><span class="sxs-lookup"><span data-stu-id="55a21-239">For a list of predefined levels, see the <em>level</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a21-240"><strong>EnableProperty</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-240"><strong>EnableProperty</strong></span></span></td>
<td><span data-ttu-id="55a21-241"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-241"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-242">Usare questo valore per includere uno o più degli elementi seguenti nel file di log:</span><span class="sxs-lookup"><span data-stu-id="55a21-242">Use this value to include one or more of the following items in the log file:</span></span>
<ul>
<li><span data-ttu-id="55a21-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Includere nei dati estesi l'ID di sicurezza (SID) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="55a21-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Include in the extended data the security identifier (SID) of the user.</span></span></li>
<li><span data-ttu-id="55a21-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Include nei dati estesi l'identificatore di sessione del terminale.</span><span class="sxs-lookup"><span data-stu-id="55a21-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Include in the extended data the terminal session identifier.</span></span></li>
<li><span data-ttu-id="55a21-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Include nei dati estesi un'analisi dello stack di chiamate per gli eventi scritti usando <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite.</strong></a></span><span class="sxs-lookup"><span data-stu-id="55a21-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Include in the extended data a call stack trace for events written using <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span></span></li>
<li><span data-ttu-id="55a21-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filtra tutti gli eventi per cui non è specificata una parola chiave diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="55a21-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filters out all events that do not have a non-zero keyword specified.</span></span></li>
<li><span data-ttu-id="55a21-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = indica che questa chiamata <a href="provider-traits.md">a</a> <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> deve abilitare un gruppo di provider anziché un singolo provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="55a21-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Indicates that this call to <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> should enable a <a href="provider-traits.md">Provider Group</a> rather than an individual Event Provider.</span></span></li>
<li><span data-ttu-id="55a21-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Includere la chiave di avvio del processo nei dati estesi.</span><span class="sxs-lookup"><span data-stu-id="55a21-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Include the Process Start Key in the extended data.</span></span></li>
<li><span data-ttu-id="55a21-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Includere la chiave evento nei dati estesi.</span><span class="sxs-lookup"><span data-stu-id="55a21-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Include the Event Key in the extended data.</span></span></li>
<li><span data-ttu-id="55a21-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filtra tutti gli eventi contrassegnati come evento InPrivate o provenienti da un processo contrassegnato come InPrivate.</span><span class="sxs-lookup"><span data-stu-id="55a21-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filters out all events that are either marked as an InPrivate event or come from a process that is marked as InPrivate.</span></span></li>
</ul>
<span data-ttu-id="55a21-251">Per altre informazioni su questi elementi, vedere <strong>EnableProperty</strong> della <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> struttura .</span><span class="sxs-lookup"><span data-stu-id="55a21-251">For more information about these items, see the <strong>EnableProperty</strong> of the <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a21-252"><strong>MatchAnyKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-252"><strong>MatchAnyKeyword</strong></span></span></td>
<td><span data-ttu-id="55a21-253"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-253"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-254">Maschera di bit di parole chiave che determinano la categoria di eventi che il provider deve scrivere.</span><span class="sxs-lookup"><span data-stu-id="55a21-254">Bitmask of keywords that determine the category of events that you want the provider to write.</span></span> <span data-ttu-id="55a21-255">Il provider scrive l'evento se uno dei bit della parola chiave dell'evento corrisponde a uno dei bit impostati in questa maschera.</span><span class="sxs-lookup"><span data-stu-id="55a21-255">The provider writes the event if any of the event's keyword bits match any of the bits set in this mask.</span></span> <span data-ttu-id="55a21-256">Per specificare che il provider deve scrivere tutti gli eventi, impostare questo valore su zero.</span><span class="sxs-lookup"><span data-stu-id="55a21-256">To specify that the provider write all events, set this value to zero.</span></span> <span data-ttu-id="55a21-257">Per un esempio, vedere la sezione Osservazioni della <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>funzione EnableTraceEx.</strong></a></span><span class="sxs-lookup"><span data-stu-id="55a21-257">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a21-258"><strong>MatchAllKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-258"><strong>MatchAllKeyword</strong></span></span></td>
<td><span data-ttu-id="55a21-259"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="55a21-259"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="55a21-260">Questa maschera di bit è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="55a21-260">This bitmask is optional.</span></span> <span data-ttu-id="55a21-261">Questa maschera limita ulteriormente la categoria di eventi che il provider deve scrivere.</span><span class="sxs-lookup"><span data-stu-id="55a21-261">This mask further restricts the category of events that you want the provider to write.</span></span> <span data-ttu-id="55a21-262">Se la parola chiave dell'evento soddisfa la condizione <em>MatchAnyKeyword,</em> il provider scriverà l'evento solo se tutti i bit in questa maschera sono presenti nella parola chiave dell'evento.</span><span class="sxs-lookup"><span data-stu-id="55a21-262">If the event's keyword meets the <em>MatchAnyKeyword</em> condition, the provider will write the event only if all of the bits in this mask exist in the event's keyword.</span></span> <span data-ttu-id="55a21-263">Questa maschera non viene usata se <em>MatchAnyKeyword</em> è zero.</span><span class="sxs-lookup"><span data-stu-id="55a21-263">This mask is not used if <em>MatchAnyKeyword</em> is zero.</span></span> <span data-ttu-id="55a21-264">Per un esempio, vedere la sezione Osservazioni della <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>funzione EnableTraceEx.</strong></a></span><span class="sxs-lookup"><span data-stu-id="55a21-264">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="55a21-265">Dopo la modifica del Registro di sistema, la sessione autologger viene avviata al successivo riavvio del computer.</span><span class="sxs-lookup"><span data-stu-id="55a21-265">After the registry has been modified, the AutoLogger session is started the next time the computer is restarted.</span></span> <span data-ttu-id="55a21-266">La sessione AutoLogger chiama la [**funzione EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) per abilitare i provider.</span><span class="sxs-lookup"><span data-stu-id="55a21-266">The AutoLogger session calls the [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) function to enable the providers.</span></span>

<span data-ttu-id="55a21-267">Le sessioni autologger aumentano il tempo di avvio del sistema e devono essere usate con moderamento.</span><span class="sxs-lookup"><span data-stu-id="55a21-267">The AutoLogger sessions increase the system boot time and should be used sparingly.</span></span> <span data-ttu-id="55a21-268">I servizi che vogliono acquisire informazioni durante il processo di avvio devono prendere in considerazione l'aggiunta della logica del controller a se stessa anziché usare la sessione autologger.</span><span class="sxs-lookup"><span data-stu-id="55a21-268">Services that want to capture information during the boot process should consider adding controller logic to itself instead of using the AutoLogger session.</span></span>

<span data-ttu-id="55a21-269">Per arrestare una sessione di AutoLogger, chiamare la [**funzione ControlTrace.**](/windows/win32/api/evntrace/nf-evntrace-controltracea)</span><span class="sxs-lookup"><span data-stu-id="55a21-269">To stop an AutoLogger session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function.</span></span> <span data-ttu-id="55a21-270">Il nome della sessione passato alla funzione è il nome della chiave del Registro di sistema usata per definire la sessione nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="55a21-270">The session name that you pass to the function is the name of the registry key that you used to define the session in the registry.</span></span>

<span data-ttu-id="55a21-271">In Windows 8.1, Windows Server 2012 R2 e versioni successive, il payload dell'evento, l'ambito e i filtri di percorso dello stack possono essere usati dalla funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e dalle strutture [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) per filtrare in base a condizioni specifiche in una sessione del logger.</span><span class="sxs-lookup"><span data-stu-id="55a21-271">On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="55a21-272">Per altre informazioni sui filtri di payload degli eventi, vedere le funzioni [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e le strutture **ENABLE TRACE \_ \_ PARAMETERS**, **EVENT FILTER \_ \_ DESCRIPTOR** e [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)</span><span class="sxs-lookup"><span data-stu-id="55a21-272">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="55a21-273">Per informazioni dettagliate sull'avvio di una sessione di traccia eventi, vedere [Configurazione e avvio di una sessione di traccia eventi.](configuring-and-starting-an-event-tracing-session.md)</span><span class="sxs-lookup"><span data-stu-id="55a21-273">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="55a21-274">Per informazioni dettagliate sull'avvio di una sessione di logger privata, vedere [Configurazione e avvio di una sessione privata del logger.](configuring-and-starting-a-private-logger-session.md)</span><span class="sxs-lookup"><span data-stu-id="55a21-274">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="55a21-275">Per informazioni dettagliate sull'avvio di una sessione di logger del kernel NT, vedere [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="55a21-275">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="55a21-276">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55a21-276">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55a21-277">Configurazione e avvio di una sessione privata del logger</span><span class="sxs-lookup"><span data-stu-id="55a21-277">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="55a21-278">Configurazione e avvio di una sessione SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="55a21-278">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="55a21-279">Configurazione e avvio di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="55a21-279">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="55a21-280">Configurazione e avvio della sessione del logger del kernel NT</span><span class="sxs-lookup"><span data-stu-id="55a21-280">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="55a21-281">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="55a21-281">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="55a21-282">**ABILITARE \_ I PARAMETRI DI \_ TRACCIA**</span><span class="sxs-lookup"><span data-stu-id="55a21-282">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="55a21-283">**DESCRITTORE \_ DEL \_ FILTRO EVENTI**</span><span class="sxs-lookup"><span data-stu-id="55a21-283">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="55a21-284">**PREDICATO \_ DEL \_ FILTRO DI PAYLOAD**</span><span class="sxs-lookup"><span data-stu-id="55a21-284">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="55a21-285">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="55a21-285">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="55a21-286">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="55a21-286">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="55a21-287">Aggiornamento di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="55a21-287">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>
