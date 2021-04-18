---
description: I thread sono pianificati per l'esecuzione in base alla relativa priorità di pianificazione.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Priorità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311964"
---
# <a name="scheduling-priorities"></a><span data-ttu-id="c07db-103">Priorità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c07db-103">Scheduling Priorities</span></span>

<span data-ttu-id="c07db-104">I thread sono pianificati per l'esecuzione in base alla relativa *priorità di pianificazione*.</span><span class="sxs-lookup"><span data-stu-id="c07db-104">Threads are scheduled to run based on their *scheduling priority*.</span></span> <span data-ttu-id="c07db-105">A ogni thread viene assegnata una priorità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c07db-105">Each thread is assigned a scheduling priority.</span></span> <span data-ttu-id="c07db-106">I livelli di priorità variano da zero (priorità più bassa) a 31 (priorità più alta).</span><span class="sxs-lookup"><span data-stu-id="c07db-106">The priority levels range from zero (lowest priority) to 31 (highest priority).</span></span> <span data-ttu-id="c07db-107">Solo il thread di pagina zero può avere una priorità pari a zero.</span><span class="sxs-lookup"><span data-stu-id="c07db-107">Only the zero-page thread can have a priority of zero.</span></span> <span data-ttu-id="c07db-108">(Il thread di pagina zero è un thread di sistema responsabile dell'azzeramento di tutte le pagine libere quando non è necessario eseguire altri thread).</span><span class="sxs-lookup"><span data-stu-id="c07db-108">(The zero-page thread is a system thread responsible for zeroing any free pages when there are no other threads that need to run.)</span></span>

<span data-ttu-id="c07db-109">Il sistema considera tutti i thread con la stessa priorità uguale a.</span><span class="sxs-lookup"><span data-stu-id="c07db-109">The system treats all threads with the same priority as equal.</span></span> <span data-ttu-id="c07db-110">Il sistema assegna intervalli temporali in modo round robin a tutti i thread con la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="c07db-110">The system assigns time slices in a round-robin fashion to all threads with the highest priority.</span></span> <span data-ttu-id="c07db-111">Se nessuno di questi thread è pronto per l'esecuzione, il sistema assegna intervalli temporali in modo round robin a tutti i thread con la priorità più alta successiva.</span><span class="sxs-lookup"><span data-stu-id="c07db-111">If none of these threads are ready to run, the system assigns time slices in a round-robin fashion to all threads with the next highest priority.</span></span> <span data-ttu-id="c07db-112">Se un thread con priorità più alta diventa disponibile per l'esecuzione, il sistema smette di eseguire il thread con priorità inferiore (senza consentirne il completamento utilizzando il relativo intervallo di tempo) e assegna un intervallo di tempo completo al thread con priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="c07db-112">If a higher-priority thread becomes available to run, the system ceases to execute the lower-priority thread (without allowing it to finish using its time slice) and assigns a full time slice to the higher-priority thread.</span></span> <span data-ttu-id="c07db-113">Per altre informazioni, vedere [commutazioni di contesto](context-switches.md).</span><span class="sxs-lookup"><span data-stu-id="c07db-113">For more information, see [Context Switches](context-switches.md).</span></span>

<span data-ttu-id="c07db-114">La priorità di ogni thread è determinata dai criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="c07db-114">The priority of each thread is determined by the following criteria:</span></span>

-   <span data-ttu-id="c07db-115">Classe di priorità del processo</span><span class="sxs-lookup"><span data-stu-id="c07db-115">The priority class of its process</span></span>
-   <span data-ttu-id="c07db-116">Livello di priorità del thread all'interno della classe di priorità del processo</span><span class="sxs-lookup"><span data-stu-id="c07db-116">The priority level of the thread within the priority class of its process</span></span>

<span data-ttu-id="c07db-117">La classe di priorità e il livello di priorità vengono combinati per formare la *priorità di base* di un thread.</span><span class="sxs-lookup"><span data-stu-id="c07db-117">The priority class and priority level are combined to form the *base priority* of a thread.</span></span> <span data-ttu-id="c07db-118">Per informazioni sulla priorità dinamica di un thread, vedere [priorità Boost](priority-boosts.md).</span><span class="sxs-lookup"><span data-stu-id="c07db-118">For information on the dynamic priority of a thread, see [Priority Boosts](priority-boosts.md).</span></span>

## <a name="priority-class"></a><span data-ttu-id="c07db-119">Classe Priority</span><span class="sxs-lookup"><span data-stu-id="c07db-119">Priority Class</span></span>

<span data-ttu-id="c07db-120">Ogni processo appartiene a una delle seguenti classi di priorità:</span><span class="sxs-lookup"><span data-stu-id="c07db-120">Each process belongs to one of the following priority classes:</span></span><dl> <span data-ttu-id="c07db-121">\_classe priorità INattiva \_</span><span class="sxs-lookup"><span data-stu-id="c07db-121">IDLE\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="c07db-122">classe di priorità inferiore al \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="c07db-122">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="c07db-123">\_classe di priorità normale \_</span><span class="sxs-lookup"><span data-stu-id="c07db-123">NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="c07db-124">\_classe di \_ priorità \_ normale sopra</span><span class="sxs-lookup"><span data-stu-id="c07db-124">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="c07db-125">\_classe con priorità alta \_</span><span class="sxs-lookup"><span data-stu-id="c07db-125">HIGH\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="c07db-126">\_classe priorità in tempo reale \_</span><span class="sxs-lookup"><span data-stu-id="c07db-126">REALTIME\_PRIORITY\_CLASS</span></span>  
</dl>

<span data-ttu-id="c07db-127">Per impostazione predefinita, la classe di priorità di un processo è la \_ classe di priorità normale \_ .</span><span class="sxs-lookup"><span data-stu-id="c07db-127">By default, the priority class of a process is NORMAL\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="c07db-128">Utilizzare la funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) per specificare la classe di priorità di un processo figlio quando viene creata.</span><span class="sxs-lookup"><span data-stu-id="c07db-128">Use the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function to specify the priority class of a child process when you create it.</span></span> <span data-ttu-id="c07db-129">Se il processo chiamante è una \_ classe di priorità inattiva \_ o una classe di \_ \_ priorità normale \_ , il nuovo processo erediterà questa classe.</span><span class="sxs-lookup"><span data-stu-id="c07db-129">If the calling process is IDLE\_PRIORITY\_CLASS or BELOW\_NORMAL\_PRIORITY\_CLASS, the new process will inherit this class.</span></span> <span data-ttu-id="c07db-130">Utilizzare la funzione [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) per determinare la classe di priorità corrente di un processo e la funzione [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) per modificare la classe di priorità di un processo.</span><span class="sxs-lookup"><span data-stu-id="c07db-130">Use the [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) function to determine the current priority class of a process and the [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) function to change the priority class of a process.</span></span>

<span data-ttu-id="c07db-131">I processi che monitorano il sistema, ad esempio screen saver o applicazioni che aggiornano periodicamente una visualizzazione, devono usare la classe di priorità di inattività \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c07db-131">Processes that monitor the system, such as screen savers or applications that periodically update a display, should use IDLE\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="c07db-132">In questo modo si impedisce che i thread di questo processo, che non hanno priorità elevata, interferiscano con i thread con priorità più elevata.</span><span class="sxs-lookup"><span data-stu-id="c07db-132">This prevents the threads of this process, which do not have high priority, from interfering with higher priority threads.</span></span>

<span data-ttu-id="c07db-133">Usare \_ \_ la classe con priorità alta con cautela.</span><span class="sxs-lookup"><span data-stu-id="c07db-133">Use HIGH\_PRIORITY\_CLASS with care.</span></span> <span data-ttu-id="c07db-134">Se un thread viene eseguito con il livello di priorità più alto per i periodi prolungati, gli altri thread del sistema non otterranno il tempo del processore.</span><span class="sxs-lookup"><span data-stu-id="c07db-134">If a thread runs at the highest priority level for extended periods, other threads in the system will not get processor time.</span></span> <span data-ttu-id="c07db-135">Se più thread vengono impostati con priorità alta allo stesso tempo, i thread perdono la loro efficacia.</span><span class="sxs-lookup"><span data-stu-id="c07db-135">If several threads are set at high priority at the same time, the threads lose their effectiveness.</span></span> <span data-ttu-id="c07db-136">La classe con priorità alta deve essere riservata ai thread che devono rispondere a eventi critici per il tempo.</span><span class="sxs-lookup"><span data-stu-id="c07db-136">The high-priority class should be reserved for threads that must respond to time-critical events.</span></span> <span data-ttu-id="c07db-137">Se l'applicazione esegue un'attività che richiede la classe con priorità alta mentre le altre attività sono la priorità normale, usare [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) per generare temporaneamente la classe di priorità dell'applicazione; quindi ridurlo dopo aver completato l'attività critica.</span><span class="sxs-lookup"><span data-stu-id="c07db-137">If your application performs one task that requires the high-priority class while the rest of its tasks are normal priority, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) to raise the priority class of the application temporarily; then reduce it after the time-critical task has been completed.</span></span> <span data-ttu-id="c07db-138">Un'altra strategia consiste nel creare un processo con priorità alta con tutti i thread bloccati nella maggior parte dei casi, riattivando i thread solo quando sono necessarie attività critiche.</span><span class="sxs-lookup"><span data-stu-id="c07db-138">Another strategy is to create a high-priority process that has all of its threads blocked most of the time, awakening threads only when critical tasks are needed.</span></span> <span data-ttu-id="c07db-139">Il punto importante è che un thread ad alta priorità deve essere eseguito per un breve periodo di tempo e solo quando è necessario eseguire un lavoro critico nel tempo.</span><span class="sxs-lookup"><span data-stu-id="c07db-139">The important point is that a high-priority thread should execute for a brief time, and only when it has time-critical work to perform.</span></span>

<span data-ttu-id="c07db-140">Non usare quasi mai la classe di priorità in tempo reale \_ \_ , perché questo interrompe i thread di sistema che gestiscono l'input del mouse, l'input da tastiera e lo scaricamento del disco in background.</span><span class="sxs-lookup"><span data-stu-id="c07db-140">You should almost never use REALTIME\_PRIORITY\_CLASS, because this interrupts system threads that manage mouse input, keyboard input, and background disk flushing.</span></span> <span data-ttu-id="c07db-141">Questa classe può essere appropriata per le applicazioni che "comunicano" direttamente con l'hardware o che eseguono brevi attività che devono avere interruzioni limitate.</span><span class="sxs-lookup"><span data-stu-id="c07db-141">This class can be appropriate for applications that "talk" directly to hardware or that perform brief tasks that should have limited interruptions.</span></span>

## <a name="priority-level"></a><span data-ttu-id="c07db-142">Livello di priorità</span><span class="sxs-lookup"><span data-stu-id="c07db-142">Priority Level</span></span>

<span data-ttu-id="c07db-143">Di seguito sono riportati i livelli di priorità all'interno di ogni classe di priorità:</span><span class="sxs-lookup"><span data-stu-id="c07db-143">The following are priority levels within each priority class:</span></span><dl> <span data-ttu-id="c07db-144">\_priorità thread \_ inattiva</span><span class="sxs-lookup"><span data-stu-id="c07db-144">THREAD\_PRIORITY\_IDLE</span></span>  
<span data-ttu-id="c07db-145">\_priorità thread \_ più bassa</span><span class="sxs-lookup"><span data-stu-id="c07db-145">THREAD\_PRIORITY\_LOWEST</span></span>  
<span data-ttu-id="c07db-146">priorità THREAD al di \_ \_ sotto del \_ normale</span><span class="sxs-lookup"><span data-stu-id="c07db-146">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  
<span data-ttu-id="c07db-147">priorità THREAD- \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="c07db-147">THREAD\_PRIORITY\_NORMAL</span></span>  
<span data-ttu-id="c07db-148">\_priorità thread \_ superiore al \_ normale</span><span class="sxs-lookup"><span data-stu-id="c07db-148">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  
<span data-ttu-id="c07db-149">\_priorità thread \_ più elevata</span><span class="sxs-lookup"><span data-stu-id="c07db-149">THREAD\_PRIORITY\_HIGHEST</span></span>  
<span data-ttu-id="c07db-150">\_tempo di priorità thread \_ \_ critico</span><span class="sxs-lookup"><span data-stu-id="c07db-150">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span>  
</dl>

<span data-ttu-id="c07db-151">Tutti i thread vengono creati utilizzando la priorità di THREAD \_ \_ normale.</span><span class="sxs-lookup"><span data-stu-id="c07db-151">All threads are created using THREAD\_PRIORITY\_NORMAL.</span></span> <span data-ttu-id="c07db-152">Ciò significa che la priorità del thread corrisponde alla classe di priorità del processo.</span><span class="sxs-lookup"><span data-stu-id="c07db-152">This means that the thread priority is the same as the process priority class.</span></span> <span data-ttu-id="c07db-153">Dopo aver creato un thread, usare la funzione [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) per regolarne la priorità rispetto agli altri thread nel processo.</span><span class="sxs-lookup"><span data-stu-id="c07db-153">After you create a thread, use the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function to adjust its priority relative to other threads in the process.</span></span>

<span data-ttu-id="c07db-154">Una strategia tipica consiste nell'usare la \_ priorità \_ dei thread sopra la \_ priorità normale o thread \_ \_ più elevata per il thread di input del processo, per garantire che l'applicazione sia reattiva all'utente.</span><span class="sxs-lookup"><span data-stu-id="c07db-154">A typical strategy is to use THREAD\_PRIORITY\_ABOVE\_NORMAL or THREAD\_PRIORITY\_HIGHEST for the process's input thread, to ensure that the application is responsive to the user.</span></span> <span data-ttu-id="c07db-155">I thread in background, in particolare quelli che richiedono un utilizzo intensivo del processore, possono essere impostati sulla priorità del THREAD al di \_ \_ sotto della \_ priorità normale o della priorità del thread \_ \_ più bassa, per assicurarsi che possano essere interrotti quando necessario.</span><span class="sxs-lookup"><span data-stu-id="c07db-155">Background threads, particularly those that are processor intensive, can be set to THREAD\_PRIORITY\_BELOW\_NORMAL or THREAD\_PRIORITY\_LOWEST, to ensure that they can be preempted when necessary.</span></span> <span data-ttu-id="c07db-156">Tuttavia, se si dispone di un thread in attesa di un altro thread con una priorità più bassa per completare un'attività, assicurarsi di bloccare l'esecuzione del thread con priorità alta in attesa.</span><span class="sxs-lookup"><span data-stu-id="c07db-156">However, if you have a thread waiting for another thread with a lower priority to complete some task, be sure to block the execution of the waiting high-priority thread.</span></span> <span data-ttu-id="c07db-157">A tale scopo, usare una [funzione wait](../sync/wait-functions.md), una [sezione critica](../sync/critical-section-objects.md)o la funzione [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) , [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)o [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) .</span><span class="sxs-lookup"><span data-stu-id="c07db-157">To do this, use a [wait function](../sync/wait-functions.md), [critical section](../sync/critical-section-objects.md), or the [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function, [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function.</span></span> <span data-ttu-id="c07db-158">Questa operazione è preferibile quando il thread esegue un ciclo.</span><span class="sxs-lookup"><span data-stu-id="c07db-158">This is preferable to having the thread execute a loop.</span></span> <span data-ttu-id="c07db-159">In caso contrario, il processo potrebbe diventare un deadlock, perché il thread con priorità inferiore non viene mai pianificato.</span><span class="sxs-lookup"><span data-stu-id="c07db-159">Otherwise, the process may become deadlocked, because the thread with lower priority is never scheduled.</span></span>

<span data-ttu-id="c07db-160">Per determinare il livello di priorità corrente di un thread, usare la funzione [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) .</span><span class="sxs-lookup"><span data-stu-id="c07db-160">To determine the current priority level of a thread, use the [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) function.</span></span>

## <a name="base-priority"></a><span data-ttu-id="c07db-161">Priorità di base</span><span class="sxs-lookup"><span data-stu-id="c07db-161">Base Priority</span></span>

<span data-ttu-id="c07db-162">La classe di priorità del processo e il livello di priorità del thread vengono combinati per formare la priorità di base di ogni thread.</span><span class="sxs-lookup"><span data-stu-id="c07db-162">The process priority class and thread priority level are combined to form the base priority of each thread.</span></span>

<span data-ttu-id="c07db-163">Nella tabella seguente viene illustrata la priorità di base per le combinazioni di classe priorità processo e valore Priorità thread.</span><span class="sxs-lookup"><span data-stu-id="c07db-163">The following table shows the base priority for combinations of process priority class and thread priority value.</span></span>


<table>
<tr>
<th colspan="2"><span data-ttu-id="c07db-164">Classe di priorità del processo</span><span class="sxs-lookup"><span data-stu-id="c07db-164">Process priority class</span></span></th>
<th><span data-ttu-id="c07db-165">Livello di priorità thread</span><span class="sxs-lookup"><span data-stu-id="c07db-165">Thread priority level</span></span></th>
<th><span data-ttu-id="c07db-166">Priorità di base</span><span class="sxs-lookup"><span data-stu-id="c07db-166">Base priority</span></span></th>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c07db-167">IDLE_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c07db-167">IDLE_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c07db-168">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c07db-168">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c07db-169">1</span><span class="sxs-lookup"><span data-stu-id="c07db-169">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-170">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c07db-170">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c07db-171">2</span><span class="sxs-lookup"><span data-stu-id="c07db-171">2</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-172">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-172">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-173">3</span><span class="sxs-lookup"><span data-stu-id="c07db-173">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-174">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-174">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-175">4</span><span class="sxs-lookup"><span data-stu-id="c07db-175">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-176">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-176">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-177">5</span><span class="sxs-lookup"><span data-stu-id="c07db-177">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-178">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c07db-178">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c07db-179">6</span><span class="sxs-lookup"><span data-stu-id="c07db-179">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-180">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c07db-180">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c07db-181">15</span><span class="sxs-lookup"><span data-stu-id="c07db-181">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c07db-182">BELOW_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c07db-182">BELOW_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c07db-183">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c07db-183">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c07db-184">1</span><span class="sxs-lookup"><span data-stu-id="c07db-184">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-185">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c07db-185">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c07db-186">4</span><span class="sxs-lookup"><span data-stu-id="c07db-186">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-187">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-187">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-188">5</span><span class="sxs-lookup"><span data-stu-id="c07db-188">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-189">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-189">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-190">6</span><span class="sxs-lookup"><span data-stu-id="c07db-190">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-191">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-191">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-192">7</span><span class="sxs-lookup"><span data-stu-id="c07db-192">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-193">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c07db-193">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c07db-194">8</span><span class="sxs-lookup"><span data-stu-id="c07db-194">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-195">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c07db-195">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c07db-196">15</span><span class="sxs-lookup"><span data-stu-id="c07db-196">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c07db-197">NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c07db-197">NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c07db-198">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c07db-198">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c07db-199">1</span><span class="sxs-lookup"><span data-stu-id="c07db-199">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-200">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c07db-200">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c07db-201">6</span><span class="sxs-lookup"><span data-stu-id="c07db-201">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-202">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-202">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-203">7</span><span class="sxs-lookup"><span data-stu-id="c07db-203">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-204">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-204">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-205">8</span><span class="sxs-lookup"><span data-stu-id="c07db-205">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-206">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-206">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-207">9</span><span class="sxs-lookup"><span data-stu-id="c07db-207">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-208">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c07db-208">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c07db-209">10</span><span class="sxs-lookup"><span data-stu-id="c07db-209">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-210">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c07db-210">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c07db-211">15</span><span class="sxs-lookup"><span data-stu-id="c07db-211">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c07db-212">ABOVE_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c07db-212">ABOVE_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c07db-213">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c07db-213">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c07db-214">1</span><span class="sxs-lookup"><span data-stu-id="c07db-214">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-215">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c07db-215">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c07db-216">8</span><span class="sxs-lookup"><span data-stu-id="c07db-216">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-217">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-217">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-218">9</span><span class="sxs-lookup"><span data-stu-id="c07db-218">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-219">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-219">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-220">10</span><span class="sxs-lookup"><span data-stu-id="c07db-220">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-221">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-221">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-222">11</span><span class="sxs-lookup"><span data-stu-id="c07db-222">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-223">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c07db-223">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c07db-224">12</span><span class="sxs-lookup"><span data-stu-id="c07db-224">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-225">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c07db-225">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c07db-226">15</span><span class="sxs-lookup"><span data-stu-id="c07db-226">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c07db-227">HIGH_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c07db-227">HIGH_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c07db-228">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c07db-228">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c07db-229">1</span><span class="sxs-lookup"><span data-stu-id="c07db-229">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-230">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c07db-230">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c07db-231">11</span><span class="sxs-lookup"><span data-stu-id="c07db-231">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-232">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-232">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-233">12</span><span class="sxs-lookup"><span data-stu-id="c07db-233">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-234">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-234">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-235">13</span><span class="sxs-lookup"><span data-stu-id="c07db-235">13</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-236">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-236">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-237">14</span><span class="sxs-lookup"><span data-stu-id="c07db-237">14</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-238">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c07db-238">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c07db-239">15</span><span class="sxs-lookup"><span data-stu-id="c07db-239">15</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-240">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c07db-240">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c07db-241">15</span><span class="sxs-lookup"><span data-stu-id="c07db-241">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c07db-242">REALTIME_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c07db-242">REALTIME_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c07db-243">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c07db-243">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c07db-244">16</span><span class="sxs-lookup"><span data-stu-id="c07db-244">16</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-245">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c07db-245">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c07db-246">22</span><span class="sxs-lookup"><span data-stu-id="c07db-246">22</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-247">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-247">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-248">23</span><span class="sxs-lookup"><span data-stu-id="c07db-248">23</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-249">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-249">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-250">24</span><span class="sxs-lookup"><span data-stu-id="c07db-250">24</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-251">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c07db-251">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c07db-252">25</span><span class="sxs-lookup"><span data-stu-id="c07db-252">25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-253">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c07db-253">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c07db-254">26</span><span class="sxs-lookup"><span data-stu-id="c07db-254">26</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c07db-255">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c07db-255">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c07db-256">31</span><span class="sxs-lookup"><span data-stu-id="c07db-256">31</span></span></td>
</tr>
</table>

 

 

 
