---
title: Schtasks.exe
description: Consente a un amministratore di creare, eliminare, eseguire query, modificare, eseguire e terminare attività pianificate in un computer locale o remoto.
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe Utilità di pianificazione
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 2a57ee4edae1cd1604f10a88f3fc8cf2ea0971fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326484"
---
# <a name="schtasksexe"></a><span data-ttu-id="29550-104">Schtasks.exe</span><span class="sxs-lookup"><span data-stu-id="29550-104">Schtasks.exe</span></span>

<span data-ttu-id="29550-105">Consente a un amministratore di creare, eliminare, eseguire query, modificare, eseguire e terminare attività pianificate in un computer locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="29550-105">Enables an administrator to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> <span data-ttu-id="29550-106">L'esecuzione di Schtasks.exe senza argomenti consente di visualizzare lo stato e la fase di esecuzione successiva per ogni attività registrata.</span><span class="sxs-lookup"><span data-stu-id="29550-106">Running Schtasks.exe without arguments displays the status and next run time for each registered task.</span></span> 

<span data-ttu-id="29550-107">Per ulteriori informazioni su Utilità di pianificazione, vedere questa introduzione: [utilità di pianificazione per sviluppatori](task-scheduler-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="29550-107">For more information on Task Scheduler, see this introduction: [Task Scheduler for developers](task-scheduler-start-page.md).</span></span>

## <a name="creating-a-task"></a><span data-ttu-id="29550-108">Creazione di un'attività</span><span class="sxs-lookup"><span data-stu-id="29550-108">Creating a Task</span></span>

<span data-ttu-id="29550-109">La sintassi seguente consente di creare un'attività nel computer locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="29550-109">The following syntax is used to create a task on the local or remote computer.</span></span>

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

## <a name="parameters"></a><span data-ttu-id="29550-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="29550-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29550-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="29550-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="29550-112">Valore che specifica il computer remoto a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="29550-112">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="29550-113">Se omesso, il valore predefinito del parametro di sistema è il computer locale.</span><span class="sxs-lookup"><span data-stu-id="29550-113">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="29550-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**</span><span class="sxs-lookup"><span data-stu-id="29550-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="29550-115">Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-115">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="29550-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**</span><span class="sxs-lookup"><span data-stu-id="29550-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="29550-117">Valore che specifica la password per un contesto utente specificato.</span><span class="sxs-lookup"><span data-stu-id="29550-117">A value that specifies the password for a given user context.</span></span> <span data-ttu-id="29550-118">Se omesso, Schtasks.exe richiede l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="29550-118">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="29550-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span> **Nome utente** /ru</span><span class="sxs-lookup"><span data-stu-id="29550-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/RU** **username**</span></span>
</dt> <dd>

<span data-ttu-id="29550-120">Valore che specifica il contesto utente in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-120">A value that specifies the user context under which the task runs.</span></span> <span data-ttu-id="29550-121">Per l'account di sistema, i valori validi sono "", "NT AUTHORITY \\ System" o "System".</span><span class="sxs-lookup"><span data-stu-id="29550-121">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="29550-122">Per le attività Utilità di pianificazione 2,0, anche "NT AUTHORITY \\ LocalService" e "NT Authority \\ NetworkService" sono valori validi.</span><span class="sxs-lookup"><span data-stu-id="29550-122">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE", and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="29550-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span> **\[ Password \]** /RP</span><span class="sxs-lookup"><span data-stu-id="29550-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="29550-124">Valore che specifica la password per l'utente specificato con il parametro/RU.</span><span class="sxs-lookup"><span data-stu-id="29550-124">A value that specifies the password for the user specified with the /RU parameter.</span></span> <span data-ttu-id="29550-125">Per richiedere la password, il valore deve essere " \* " o nessun valore.</span><span class="sxs-lookup"><span data-stu-id="29550-125">To prompt for the password, the value must be either "\*" or no value.</span></span> <span data-ttu-id="29550-126">Questa password viene ignorata per l'account di sistema.</span><span class="sxs-lookup"><span data-stu-id="29550-126">This password is ignored for the system account.</span></span> <span data-ttu-id="29550-127">Questo parametro deve essere combinato con l'opzione/RU o/XML.</span><span class="sxs-lookup"><span data-stu-id="29550-127">This parameter must be combined with either /RU or the /XML switch.</span></span>

</dd> <dt>

<span data-ttu-id="29550-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span> **Pianificazione** di/SC</span><span class="sxs-lookup"><span data-stu-id="29550-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **schedule**</span></span>
</dt> <dd>

<span data-ttu-id="29550-129">Valore che specifica la frequenza di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="29550-129">A value that specifies the schedule frequency.</span></span> <span data-ttu-id="29550-130">I valori validi sono: minuti, orari, giornalieri, SETTIMANAli, MENSILi, una volta, in base al LOGO, OnIdle e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="29550-130">Valid values are: MINUTE, HOURLY, DAILY, WEEKLY, MONTHLY, ONCE, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="29550-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span> **Modificatore** /mo</span><span class="sxs-lookup"><span data-stu-id="29550-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/MO** **modifier**</span></span>
</dt> <dd>

<span data-ttu-id="29550-132">Valore che perfeziona il tipo di pianificazione per consentire un controllo più preciso sulla ricorrenza della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="29550-132">A value that refines the schedule type to allow for finer control over the schedule recurrence.</span></span> <span data-ttu-id="29550-133">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="29550-133">Valid values are:</span></span>

-   <span data-ttu-id="29550-134">MINUTO: 1-1439 minuti.</span><span class="sxs-lookup"><span data-stu-id="29550-134">MINUTE: 1 - 1439 minutes.</span></span>
-   <span data-ttu-id="29550-135">OGNI ora: 1-23 ore.</span><span class="sxs-lookup"><span data-stu-id="29550-135">HOURLY: 1 - 23 hours.</span></span>
-   <span data-ttu-id="29550-136">OGNI giorno: 1-365 giorni.</span><span class="sxs-lookup"><span data-stu-id="29550-136">DAILY: 1 - 365 days.</span></span>
-   <span data-ttu-id="29550-137">SETTIMANALE: settimane 1-52.</span><span class="sxs-lookup"><span data-stu-id="29550-137">WEEKLY: weeks 1 - 52.</span></span>
-   <span data-ttu-id="29550-138">ONCE: nessun modificatore.</span><span class="sxs-lookup"><span data-stu-id="29550-138">ONCE: No modifiers.</span></span>
-   <span data-ttu-id="29550-139">OnStart: nessun modificatore.</span><span class="sxs-lookup"><span data-stu-id="29550-139">ONSTART: No modifiers.</span></span>
-   <span data-ttu-id="29550-140">ONLOGON: nessun modificatore.</span><span class="sxs-lookup"><span data-stu-id="29550-140">ONLOGON: No modifiers.</span></span>
-   <span data-ttu-id="29550-141">OnIdle: nessun modificatore.</span><span class="sxs-lookup"><span data-stu-id="29550-141">ONIDLE: No modifiers.</span></span>
-   <span data-ttu-id="29550-142">MENSILE: 1-12, o prima, seconda, terza, quarta, ultima e LASTDAY.</span><span class="sxs-lookup"><span data-stu-id="29550-142">MONTHLY: 1 - 12, or FIRST, SECOND, THIRD, FOURTH, LAST, and LASTDAY.</span></span>
-   <span data-ttu-id="29550-143">OnEvent: stringa di query dell'evento XPath.</span><span class="sxs-lookup"><span data-stu-id="29550-143">ONEVENT: XPath event query string.</span></span>

</dd> <dt>

<span data-ttu-id="29550-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **giorni**</span><span class="sxs-lookup"><span data-stu-id="29550-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **days**</span></span>
</dt> <dd>

<span data-ttu-id="29550-145">Valore che specifica il giorno della settimana in cui eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-145">A value that specifies the day of the week to run the task.</span></span> <span data-ttu-id="29550-146">I valori validi sono: MON, Mar, Mer, Gio, ven, SAT, SUN e per le pianificazioni MENSILi 1-31 (giorni del mese).</span><span class="sxs-lookup"><span data-stu-id="29550-146">Valid values are: MON, TUE, WED, THU, FRI, SAT, SUN and for MONTHLY schedules 1 - 31 (days of the month).</span></span> <span data-ttu-id="29550-147">Il carattere jolly ( \* ) specifica tutti i giorni.</span><span class="sxs-lookup"><span data-stu-id="29550-147">The wildcard character (\*) specifies all days.</span></span>

</dd> <dt>

<span data-ttu-id="29550-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **mesi**</span><span class="sxs-lookup"><span data-stu-id="29550-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **months**</span></span>
</dt> <dd>

<span data-ttu-id="29550-149">Valore che specifica i mesi dell'anno.</span><span class="sxs-lookup"><span data-stu-id="29550-149">A value that specifies months of the year.</span></span> <span data-ttu-id="29550-150">Il valore predefinito è il primo giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="29550-150">Defaults to the first day of the month.</span></span> <span data-ttu-id="29550-151">I valori validi sono: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV e DEC.</span><span class="sxs-lookup"><span data-stu-id="29550-151">Valid values are: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV, and DEC.</span></span> <span data-ttu-id="29550-152">Il carattere jolly ( \* ) specifica tutti i mesi.</span><span class="sxs-lookup"><span data-stu-id="29550-152">The wildcard character (\*) specifies all months.</span></span>

</dd> <dt>

<span data-ttu-id="29550-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **tempoinattività**</span><span class="sxs-lookup"><span data-stu-id="29550-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**</span></span>
</dt> <dd>

<span data-ttu-id="29550-154">Valore che specifica la quantità di tempo di inattività di attesa prima dell'esecuzione di un'attività OnIdle pianificata.</span><span class="sxs-lookup"><span data-stu-id="29550-154">A value that specifies the amount of idle time to wait before running a scheduled ONIDLE task.</span></span> <span data-ttu-id="29550-155">L'intervallo valido è 1-999 minuti.</span><span class="sxs-lookup"><span data-stu-id="29550-155">The valid range is 1 - 999 minutes.</span></span>

</dd> <dt>

<span data-ttu-id="29550-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**</span><span class="sxs-lookup"><span data-stu-id="29550-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="29550-157">Valore che specifica un nome che identifica in modo univoco l'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="29550-157">A value that specifies a name which uniquely identifies the scheduled task.</span></span>

</dd> <dt>

<span data-ttu-id="29550-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span> **Esecuzioneattività** /TR</span><span class="sxs-lookup"><span data-stu-id="29550-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="29550-159">Valore che specifica il percorso e il nome file dell'attività da eseguire all'ora pianificata.</span><span class="sxs-lookup"><span data-stu-id="29550-159">A value that specifies the path and file name of the task to be run at the scheduled time.</span></span> <span data-ttu-id="29550-160">Ad esempio: C: \\ Windows \\ system32 \\calc.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-160">For example: C:\\Windows\\System32\\calc.exe.</span></span>

</dd> <dt>

<span data-ttu-id="29550-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**</span><span class="sxs-lookup"><span data-stu-id="29550-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="29550-162">Valore che specifica l'ora di inizio per l'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-162">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="29550-163">Il formato dell'ora è HH: mm (ora di 24 ore).</span><span class="sxs-lookup"><span data-stu-id="29550-163">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="29550-164">14:30, ad esempio, specifica 2: pm.</span><span class="sxs-lookup"><span data-stu-id="29550-164">For example, 14:30 specifies 2:30PM.</span></span> <span data-ttu-id="29550-165">Il valore predefinito è l'ora corrente in cui non è specificato/ST.</span><span class="sxs-lookup"><span data-stu-id="29550-165">The default is the current time is /ST is not specified.</span></span> <span data-ttu-id="29550-166">Questa opzione è obbligatoria per Wit l'argomento/SC ONCE.</span><span class="sxs-lookup"><span data-stu-id="29550-166">This option is required wit the /SC ONCE argument.</span></span>

</dd> <dt>

<span data-ttu-id="29550-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span> **Intervallo** /ri</span><span class="sxs-lookup"><span data-stu-id="29550-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="29550-168">Valore che specifica l'intervallo di ripetizione in minuti.</span><span class="sxs-lookup"><span data-stu-id="29550-168">A value that specifies the repetition interval in minutes.</span></span> <span data-ttu-id="29550-169">Questa operazione non è applicabile per i tipi di pianificazione seguenti: MINUTE, HOURly, OnStart, on LOGOn, OnIdle e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="29550-169">This is not applicable for the following schedule types: MINUTE, HOURLY, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="29550-170">L'intervallo valido è 1-599940 minuti.</span><span class="sxs-lookup"><span data-stu-id="29550-170">The valid range is 1 - 599940 minutes.</span></span> <span data-ttu-id="29550-171">Se vengono specificati i parametri/ET o/DU, il valore predefinito è 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="29550-171">If either the /ET or /DU parameters are specified, the default is 10 minutes.</span></span>

<span data-ttu-id="29550-172">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-172">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span> **EndTime** /et</span><span class="sxs-lookup"><span data-stu-id="29550-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="29550-174">Valore che specifica l'ora di fine per l'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-174">A value that specifies the end time to run the task.</span></span> <span data-ttu-id="29550-175">Il formato dell'ora è HH: mm (ora di 24 ore).</span><span class="sxs-lookup"><span data-stu-id="29550-175">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="29550-176">14:50, ad esempio, specifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="29550-176">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="29550-177">Questa operazione non è applicabile per i tipi di pianificazione seguenti: OnStart, ONLOGON, OnIdle e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="29550-177">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

<span data-ttu-id="29550-178">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-178">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span> **Durata** /du</span><span class="sxs-lookup"><span data-stu-id="29550-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="29550-180">Valore che specifica la durata di esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-180">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="29550-181">Il formato dell'ora è HH: mm (ora di 24 ore).</span><span class="sxs-lookup"><span data-stu-id="29550-181">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="29550-182">14:50, ad esempio, specifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="29550-182">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="29550-183">Questa operazione non è applicabile a/ET e per i tipi di pianificazione seguenti: OnStart, inidle e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="29550-183">This is not applicable with /ET and for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="29550-184">Per le attività/V1 (Utilità di pianificazione 1,0 attività), se si specifica/RI, il valore predefinito della durata è di un'ora.</span><span class="sxs-lookup"><span data-stu-id="29550-184">For /V1 tasks (Task Scheduler 1.0 tasks), if /RI is specified, then the duration default is one hour.</span></span>

<span data-ttu-id="29550-185">**Windows XP:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-185">**Windows XP:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="29550-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-187">Valore che termina l'attività all'ora di fine o alla durata.</span><span class="sxs-lookup"><span data-stu-id="29550-187">A value that terminates the task at the end time or duration time.</span></span> <span data-ttu-id="29550-188">Questa operazione non è applicabile per i tipi di pianificazione seguenti: OnStart, ONLOGON, OnIdle e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="29550-188">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="29550-189">È necessario specificare/ET o/DU.</span><span class="sxs-lookup"><span data-stu-id="29550-189">Either /ET or /DU must be specified.</span></span>

<span data-ttu-id="29550-190">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-190">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **StartDate**</span><span class="sxs-lookup"><span data-stu-id="29550-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="29550-192">Valore che specifica la prima data in cui eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-192">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="29550-193">Il formato è mm/gg/aaaa.</span><span class="sxs-lookup"><span data-stu-id="29550-193">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="29550-194">Per impostazione predefinita, questo valore viene impostato sulla data corrente.</span><span class="sxs-lookup"><span data-stu-id="29550-194">This value defaults to the current date.</span></span> <span data-ttu-id="29550-195">Questa operazione non è applicabile per i tipi di pianificazione seguenti: una volta, OnStart, un oggetto OnIdle e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="29550-195">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="29550-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**</span><span class="sxs-lookup"><span data-stu-id="29550-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="29550-197">Valore che specifica l'ultima data in cui l'attività viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="29550-197">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="29550-198">Il formato è mm/gg/aaaa.</span><span class="sxs-lookup"><span data-stu-id="29550-198">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="29550-199">Questa operazione non è applicabile per i tipi di pianificazione seguenti: una volta, OnStart, un oggetto OnIdle e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="29550-199">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="29550-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span> **Canalename** /CE</span><span class="sxs-lookup"><span data-stu-id="29550-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**</span></span>
</dt> <dd>

<span data-ttu-id="29550-201">Valore che specifica il canale dell'evento per i trigger OnEvent.</span><span class="sxs-lookup"><span data-stu-id="29550-201">A value that specifies the event channel for ONEVENT triggers.</span></span>

<span data-ttu-id="29550-202">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-202">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="29550-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-204">Valore che consente l'esecuzione interattiva dell'attività solo se l'utente/RU è attualmente connesso al momento dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-204">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="29550-205">L'attività viene eseguita solo se l'utente è connesso.</span><span class="sxs-lookup"><span data-stu-id="29550-205">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="29550-206">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-206">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span><span class="sxs-lookup"><span data-stu-id="29550-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-208">Valore che indica che non viene archiviata alcuna password.</span><span class="sxs-lookup"><span data-stu-id="29550-208">A value that indicates that no password is stored.</span></span> <span data-ttu-id="29550-209">L'attività non viene eseguita in modo interattivo come l'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="29550-209">The task does not run interactively as the given user.</span></span> <span data-ttu-id="29550-210">Sono disponibili solo le risorse locali.</span><span class="sxs-lookup"><span data-stu-id="29550-210">Only local resources are available.</span></span>

<span data-ttu-id="29550-211">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-211">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span><span class="sxs-lookup"><span data-stu-id="29550-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-213">Valore che contrassegna l'attività da eliminare dopo l'esecuzione finale.</span><span class="sxs-lookup"><span data-stu-id="29550-213">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="29550-214">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-214">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>XMLFile **/XML** </span><span class="sxs-lookup"><span data-stu-id="29550-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**</span></span>
</dt> <dd>

<span data-ttu-id="29550-216">Valore che crea un'attività da un file XML.</span><span class="sxs-lookup"><span data-stu-id="29550-216">A value that creates a task from an XML file.</span></span> <span data-ttu-id="29550-217">Questo parametro può essere combinato con le opzioni/RU e/RP oppure con l'opzione/RP da sola quando il codice XML dell'attività contiene già il database principale.</span><span class="sxs-lookup"><span data-stu-id="29550-217">This parameter can be combined with /RU and /RP switches, or with the /RP switch alone when the task XML already contains the principal.</span></span>

<span data-ttu-id="29550-218">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-218">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span><span class="sxs-lookup"><span data-stu-id="29550-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-220">Valore che crea un'attività visibile alle piattaforme Windows 2000, Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29550-220">A value that creates a task visible to Windows 2000, Windows Server 2003, and Windows XP platforms.</span></span>

<span data-ttu-id="29550-221">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-221">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="29550-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-223">Valore che crea l'attività in modo forzato ed evita gli avvisi se l'attività specificata esiste già.</span><span class="sxs-lookup"><span data-stu-id="29550-223">A value that forcefully creates the task and suppresses warnings if the specified task already exists.</span></span>

<span data-ttu-id="29550-224">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-224">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Livello** /RL</span><span class="sxs-lookup"><span data-stu-id="29550-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="29550-226">Valore che imposta il livello di esecuzione per l'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-226">A value that sets the run level for the task.</span></span> <span data-ttu-id="29550-227">I valori validi sono limitati e MASSIMi.</span><span class="sxs-lookup"><span data-stu-id="29550-227">Valid values are LIMITED and HIGHEST.</span></span> <span data-ttu-id="29550-228">Il valore predefinito è LIMITED.</span><span class="sxs-lookup"><span data-stu-id="29550-228">The default is LIMITED.</span></span>

<span data-ttu-id="29550-229">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-229">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span> **DelayTime** /Delay</span><span class="sxs-lookup"><span data-stu-id="29550-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="29550-231">Valore che specifica il tempo di attesa per ritardare l'attività dopo che il trigger è stato attivato.</span><span class="sxs-lookup"><span data-stu-id="29550-231">A value that specifies the wait time to delay the task after the trigger is fired.</span></span> <span data-ttu-id="29550-232">Il formato dell'ora è mmmm: SS.</span><span class="sxs-lookup"><span data-stu-id="29550-232">The time format is mmmm:ss.</span></span> <span data-ttu-id="29550-233">Questa opzione è valida solo per i tipi di pianificazione OnStart, ONLOGON e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="29550-233">This option is only valid for schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="29550-234">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-234">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-235"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="29550-235"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-236">Valore che Visualizza il messaggio della Guida per Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-236">A value that displays the help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29550-237">Commenti</span><span class="sxs-lookup"><span data-stu-id="29550-237">Remarks</span></span>

<span data-ttu-id="29550-238">Quando si crea un'attività in un computer remoto che esegue il sistema operativo Windows XP, Windows Server 2003 o Windows 2000, usare l'opzione/V1.</span><span class="sxs-lookup"><span data-stu-id="29550-238">When creating a task on a remote computer running on the Windows XP, Windows Server 2003, or Windows 2000 operating system, use the /V1 switch.</span></span>

<span data-ttu-id="29550-239">Non è possibile creare un'attività remota non interattiva Utilità di pianificazione 1,0 (creare un'attività senza usare l'opzione/IT e con l'opzione/V1) se nel computer remoto è abilitata l'eccezione del firewall per la condivisione di file e stampanti e l'eccezione del firewall di gestione delle attività pianificate Remote è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="29550-239">You cannot create a non-interactive remote Task Scheduler 1.0 task (create a task by not using the /IT switch and using the /V1 switch) if the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled.</span></span>

## <a name="deleting-a-task"></a><span data-ttu-id="29550-240">Eliminazione di un'attività</span><span class="sxs-lookup"><span data-stu-id="29550-240">Deleting a Task</span></span>

<span data-ttu-id="29550-241">Per eliminare una o più attività pianificate, viene utilizzata la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="29550-241">The following syntax is used to delete one or more scheduled tasks.</span></span>

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

## <a name="parameters"></a><span data-ttu-id="29550-242">Parametri</span><span class="sxs-lookup"><span data-stu-id="29550-242">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29550-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="29550-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="29550-244">Valore che specifica il computer remoto a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="29550-244">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="29550-245">Se omesso, il valore predefinito del parametro di sistema è il computer locale.</span><span class="sxs-lookup"><span data-stu-id="29550-245">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="29550-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**</span><span class="sxs-lookup"><span data-stu-id="29550-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="29550-247">Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-247">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="29550-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**</span><span class="sxs-lookup"><span data-stu-id="29550-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="29550-249">Valore che specifica la password per il contesto utente specificato.</span><span class="sxs-lookup"><span data-stu-id="29550-249">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="29550-250">Se omesso, Schtasks.exe richiede l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="29550-250">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="29550-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**</span><span class="sxs-lookup"><span data-stu-id="29550-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="29550-252">Valore che specifica il nome dell'attività pianificata da eliminare.</span><span class="sxs-lookup"><span data-stu-id="29550-252">A value that specifies the name of the scheduled task to delete.</span></span> <span data-ttu-id="29550-253">Il carattere jolly ( \* ) può essere utilizzato per eliminare tutte le attività.</span><span class="sxs-lookup"><span data-stu-id="29550-253">The wildcard character (\*) can be used to delete all tasks.</span></span>

</dd> <dt>

<span data-ttu-id="29550-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="29550-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-255">Valore che elimina l'attività in modo forzato ed Elimina gli avvisi se l'attività specificata è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="29550-255">A value that forcefully deletes the task and suppresses warnings if the specified task is running.</span></span>

</dd> <dt>

<span data-ttu-id="29550-256"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="29550-256"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="29550-257">Valore che visualizza la guida per Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-257">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="running-a-task"></a><span data-ttu-id="29550-258">Esecuzione di un'attività</span><span class="sxs-lookup"><span data-stu-id="29550-258">Running a Task</span></span>

<span data-ttu-id="29550-259">La sintassi seguente viene utilizzata per eseguire immediatamente un'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="29550-259">The following syntax is used to immediately run a scheduled task.</span></span>

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

## <a name="parameters"></a><span data-ttu-id="29550-260">Parametri</span><span class="sxs-lookup"><span data-stu-id="29550-260">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29550-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="29550-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="29550-262">Valore che specifica il computer remoto a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="29550-262">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="29550-263">Se omesso, il valore predefinito del parametro di sistema è il computer locale.</span><span class="sxs-lookup"><span data-stu-id="29550-263">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="29550-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**</span><span class="sxs-lookup"><span data-stu-id="29550-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="29550-265">Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-265">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="29550-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**</span><span class="sxs-lookup"><span data-stu-id="29550-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="29550-267">Valore che specifica la password per il contesto utente specificato.</span><span class="sxs-lookup"><span data-stu-id="29550-267">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="29550-268">Se omesso, Schtasks.exe richiede l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="29550-268">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="29550-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**</span><span class="sxs-lookup"><span data-stu-id="29550-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="29550-270">Valore che specifica il nome dell'attività pianificata da eseguire.</span><span class="sxs-lookup"><span data-stu-id="29550-270">A value that specifies the name of the scheduled task to run.</span></span>

</dd> <dt>

<span data-ttu-id="29550-271"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="29550-271"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="29550-272">Valore che visualizza la guida per Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-272">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="ending-a-running-task"></a><span data-ttu-id="29550-273">Terminazione di un'attività in esecuzione</span><span class="sxs-lookup"><span data-stu-id="29550-273">Ending a Running Task</span></span>

<span data-ttu-id="29550-274">La sintassi seguente viene utilizzata per arrestare un'attività pianificata in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="29550-274">The following syntax is used to stop a running scheduled task.</span></span>

> [!Note]  
> <span data-ttu-id="29550-275">Per arrestare l'esecuzione di un'attività remota, verificare che nel computer remoto siano abilitate le eccezioni del firewall per la condivisione di file e stampanti e le attività pianificate remote.</span><span class="sxs-lookup"><span data-stu-id="29550-275">To stop a remote task from running, ensure that the remote computer has the File and Printer Sharing and Remote Scheduled Tasks Management firewall exceptions enabled.</span></span>

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

## <a name="parameters"></a><span data-ttu-id="29550-276">Parametri</span><span class="sxs-lookup"><span data-stu-id="29550-276">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29550-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="29550-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="29550-278">Valore che specifica il computer remoto a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="29550-278">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="29550-279">Se omesso, il valore predefinito del parametro di sistema è il computer locale.</span><span class="sxs-lookup"><span data-stu-id="29550-279">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="29550-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**</span><span class="sxs-lookup"><span data-stu-id="29550-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="29550-281">Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-281">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="29550-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**</span><span class="sxs-lookup"><span data-stu-id="29550-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="29550-283">Valore che specifica la password per il contesto utente specificato.</span><span class="sxs-lookup"><span data-stu-id="29550-283">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="29550-284">Se omesso, Schtasks.exe richiede l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="29550-284">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="29550-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**</span><span class="sxs-lookup"><span data-stu-id="29550-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="29550-286">Valore che specifica il nome dell'attività pianificata da arrestare.</span><span class="sxs-lookup"><span data-stu-id="29550-286">A value that specifies the name of the scheduled task to stop.</span></span>

</dd> <dt>

<span data-ttu-id="29550-287"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="29550-287"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="29550-288">Valore che visualizza la guida per Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-288">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="querying-for-task-information"></a><span data-ttu-id="29550-289">Esecuzione di query per informazioni sulle attività</span><span class="sxs-lookup"><span data-stu-id="29550-289">Querying for Task Information</span></span>

<span data-ttu-id="29550-290">La sintassi seguente consente di visualizzare le attività pianificate dal computer locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="29550-290">The following syntax is used to display the scheduled tasks from the local or remote computer.</span></span>

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

## <a name="parameters"></a><span data-ttu-id="29550-291">Parametri</span><span class="sxs-lookup"><span data-stu-id="29550-291">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29550-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="29550-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="29550-293">Valore che specifica il computer remoto a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="29550-293">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="29550-294">Se omesso, il valore predefinito del parametro di sistema è il computer locale.</span><span class="sxs-lookup"><span data-stu-id="29550-294">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="29550-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**</span><span class="sxs-lookup"><span data-stu-id="29550-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="29550-296">Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-296">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="29550-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**</span><span class="sxs-lookup"><span data-stu-id="29550-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="29550-298">Valore che specifica la password per il contesto utente specificato.</span><span class="sxs-lookup"><span data-stu-id="29550-298">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="29550-299">Se omesso, Schtasks.exe richiede l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="29550-299">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="29550-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span> **Formato** /fo</span><span class="sxs-lookup"><span data-stu-id="29550-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** **format**</span></span>
</dt> <dd>

<span data-ttu-id="29550-301">Valore che specifica il formato di output.</span><span class="sxs-lookup"><span data-stu-id="29550-301">A value that specifies the output format.</span></span> <span data-ttu-id="29550-302">I valori validi sono TABLE, LIST e CSV.</span><span class="sxs-lookup"><span data-stu-id="29550-302">The valid values are TABLE, LIST, and CSV.</span></span>

</dd> <dt>

<span data-ttu-id="29550-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span><span class="sxs-lookup"><span data-stu-id="29550-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-304">Valore che specifica che l'intestazione di colonna non deve essere visualizzata nell'output.</span><span class="sxs-lookup"><span data-stu-id="29550-304">A value that specifies that the column header should not be displayed in the output.</span></span> <span data-ttu-id="29550-305">Questa operazione è valida solo per i formati di tabella e CSV.</span><span class="sxs-lookup"><span data-stu-id="29550-305">This is valid only for TABLE and CSV formats.</span></span>

</dd> <dt>

<span data-ttu-id="29550-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="29550-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-307">Valore che Visualizza l'output dettagliato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-307">A value that displays verbose task output.</span></span>

> [!Note]  
> <span data-ttu-id="29550-308">Se un'attività è stata pianificata per essere eseguita una sola volta, le informazioni di pianificazione visualizzate sono "la pianificazione dei dati non è disponibile in questo formato".</span><span class="sxs-lookup"><span data-stu-id="29550-308">If a task was scheduled to run only one time, then the displayed schedule information is "Scheduling data is not available in this format."</span></span>

 

</dd> <dt>

<span data-ttu-id="29550-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**</span><span class="sxs-lookup"><span data-stu-id="29550-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="29550-310">Valore che specifica il nome dell'attività per il quale recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="29550-310">A value that specifies the task name for which to retrieve the information.</span></span> <span data-ttu-id="29550-311">Se non viene specificato alcun nome di attività, verranno visualizzate le informazioni relative a tutte le attività.</span><span class="sxs-lookup"><span data-stu-id="29550-311">If no task name is specified, then information for all the tasks will be displayed.</span></span>

<span data-ttu-id="29550-312">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-312">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span><span class="sxs-lookup"><span data-stu-id="29550-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-314">Valore utilizzato per visualizzare le definizioni di attività in formato XML.</span><span class="sxs-lookup"><span data-stu-id="29550-314">A value that is used to display the task definitions in XML format.</span></span>

<span data-ttu-id="29550-315">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-315">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-316"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="29550-316"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="29550-317">Valore utilizzato per visualizzare la guida per Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-317">A value that is used to display the Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="changing-a-task"></a><span data-ttu-id="29550-318">Modifica di un'attività</span><span class="sxs-lookup"><span data-stu-id="29550-318">Changing a Task</span></span>

<span data-ttu-id="29550-319">La sintassi seguente consente di modificare la modalità di esecuzione del programma o di modificare l'account utente e la password utilizzati da un'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="29550-319">The following syntax is used to change how the program runs, or change the user account and password used by a scheduled task.</span></span>

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

## <a name="parameters"></a><span data-ttu-id="29550-320">Parametri</span><span class="sxs-lookup"><span data-stu-id="29550-320">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29550-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="29550-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="29550-322">Valore che specifica il computer remoto a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="29550-322">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="29550-323">Se omesso, il valore predefinito del parametro di sistema è il computer locale.</span><span class="sxs-lookup"><span data-stu-id="29550-323">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="29550-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**</span><span class="sxs-lookup"><span data-stu-id="29550-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="29550-325">Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-325">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="29550-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**</span><span class="sxs-lookup"><span data-stu-id="29550-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="29550-327">Valore che specifica la password per il contesto utente specificato.</span><span class="sxs-lookup"><span data-stu-id="29550-327">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="29550-328">Se omesso, Schtasks.exe richiede l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="29550-328">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="29550-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**</span><span class="sxs-lookup"><span data-stu-id="29550-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="29550-330">Valore che specifica l'attività pianificata da modificare.</span><span class="sxs-lookup"><span data-stu-id="29550-330">A value that specifies which scheduled task to change.</span></span>

</dd> <dt>

<span data-ttu-id="29550-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span> **RunAsUser** /ru</span><span class="sxs-lookup"><span data-stu-id="29550-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/RU** **runasuser**</span></span>
</dt> <dd>

<span data-ttu-id="29550-332">Valore che modifica il nome utente (contesto utente) in cui viene eseguita l'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="29550-332">A value that changes the user name (user context) under which the scheduled task will run.</span></span> <span data-ttu-id="29550-333">Per l'account di sistema, i valori validi sono "", "NT AUTHORITY \\ System" o "System".</span><span class="sxs-lookup"><span data-stu-id="29550-333">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="29550-334">Per le attività Utilità di pianificazione 2,0, anche "NT AUTHORITY \\ LocalService" e "NT Authority \\ NetworkService" sono valori validi.</span><span class="sxs-lookup"><span data-stu-id="29550-334">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE" and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="29550-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span> **RunAsPassword** /RP</span><span class="sxs-lookup"><span data-stu-id="29550-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**</span></span>
</dt> <dd>

<span data-ttu-id="29550-336">Valore che specifica una nuova password per il contesto utente esistente o la password per un nuovo account utente.</span><span class="sxs-lookup"><span data-stu-id="29550-336">A value that specifies a new password for the existing user context or the password for a new user account.</span></span> <span data-ttu-id="29550-337">Questa password viene ignorata per l'account di sistema.</span><span class="sxs-lookup"><span data-stu-id="29550-337">This password is ignored for the system account.</span></span>

</dd> <dt>

<span data-ttu-id="29550-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span> **Esecuzioneattività** /TR</span><span class="sxs-lookup"><span data-stu-id="29550-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="29550-339">Valore che specifica un nuovo programma che l'attività eseguirà.</span><span class="sxs-lookup"><span data-stu-id="29550-339">A value that specifies a new program that the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="29550-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**</span><span class="sxs-lookup"><span data-stu-id="29550-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="29550-341">Valore che specifica l'ora di inizio per l'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-341">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="29550-342">Il formato dell'ora è HH: mm (ora di 24 ore).</span><span class="sxs-lookup"><span data-stu-id="29550-342">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="29550-343">14:30, ad esempio, specifica 2: pm.</span><span class="sxs-lookup"><span data-stu-id="29550-343">For example, 14:30 specifies 2:30PM.</span></span>

<span data-ttu-id="29550-344">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-344">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span> **Intervallo** /ri</span><span class="sxs-lookup"><span data-stu-id="29550-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="29550-346">Valore che specifica l'intervallo di ripetizione, in minuti.</span><span class="sxs-lookup"><span data-stu-id="29550-346">A value that specifies the repetition interval, in minutes.</span></span> <span data-ttu-id="29550-347">L'intervallo valido è 1-599940 minuti.</span><span class="sxs-lookup"><span data-stu-id="29550-347">The valid range is 1 - 599940 minutes.</span></span>

<span data-ttu-id="29550-348">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-348">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span> **EndTime** /et</span><span class="sxs-lookup"><span data-stu-id="29550-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="29550-350">Valore che specifica l'ora di fine dell'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-350">A value that specifies the end time for the task.</span></span> <span data-ttu-id="29550-351">Il formato dell'ora è HH: mm (ora di 24 ore).</span><span class="sxs-lookup"><span data-stu-id="29550-351">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="29550-352">14:50, ad esempio, specifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="29550-352">For example, 14:50 specifies 2:50PM.</span></span>

<span data-ttu-id="29550-353">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-353">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span> **Durata** /du</span><span class="sxs-lookup"><span data-stu-id="29550-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="29550-355">Valore che specifica la durata di esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-355">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="29550-356">Il formato dell'ora è HH: mm (ora di 24 ore).</span><span class="sxs-lookup"><span data-stu-id="29550-356">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="29550-357">14:50, ad esempio, specifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="29550-357">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="29550-358">Questa operazione non è applicabile al parametro/ET.</span><span class="sxs-lookup"><span data-stu-id="29550-358">This is not applicable with the /ET parameter.</span></span>

<span data-ttu-id="29550-359">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-359">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="29550-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-361">Valore che termina l'attività all'ora di fine o alla durata.</span><span class="sxs-lookup"><span data-stu-id="29550-361">A value that terminates the task at the end time or duration time.</span></span>

<span data-ttu-id="29550-362">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-362">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **StartDate**</span><span class="sxs-lookup"><span data-stu-id="29550-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="29550-364">Valore che specifica la prima data in cui eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-364">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="29550-365">Il formato è mm/gg/aaaa.</span><span class="sxs-lookup"><span data-stu-id="29550-365">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="29550-366">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-366">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**</span><span class="sxs-lookup"><span data-stu-id="29550-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="29550-368">Valore che specifica l'ultima data in cui l'attività viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="29550-368">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="29550-369">Il formato è mm/gg/aaaa.</span><span class="sxs-lookup"><span data-stu-id="29550-369">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="29550-370">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-370">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="29550-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-372">Valore che consente l'esecuzione interattiva dell'attività solo se l'utente/RU è attualmente connesso al momento dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-372">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="29550-373">L'attività viene eseguita solo se l'utente è connesso.</span><span class="sxs-lookup"><span data-stu-id="29550-373">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="29550-374">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-374">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Livello** /RL</span><span class="sxs-lookup"><span data-stu-id="29550-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="29550-376">Valore che imposta il livello di esecuzione per l'attività.</span><span class="sxs-lookup"><span data-stu-id="29550-376">A value that sets the run level for the task.</span></span> <span data-ttu-id="29550-377">I valori validi sono limitati e MASSIMi.</span><span class="sxs-lookup"><span data-stu-id="29550-377">Valid values are LIMITED and HIGHEST.</span></span>

<span data-ttu-id="29550-378">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-378">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span><span class="sxs-lookup"><span data-stu-id="29550-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-380">Valore che Abilita l'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="29550-380">A value that enables the scheduled task.</span></span> <span data-ttu-id="29550-381">È possibile eseguire un'attività abilitata e non è possibile eseguire un'attività disabilitata.</span><span class="sxs-lookup"><span data-stu-id="29550-381">An enabled task can run, and a disabled task cannot run.</span></span>

<span data-ttu-id="29550-382">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-382">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span><span class="sxs-lookup"><span data-stu-id="29550-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-384">Valore che disabilita l'esecuzione dell'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="29550-384">A value that disables the scheduled task from running.</span></span>

> [!Note]  
> <span data-ttu-id="29550-385">Se un'attività Utilità di pianificazione 1,0 remota viene disabilitata da Schtasks.exe e nel computer remoto è abilitata l'eccezione del firewall per la condivisione di file e stampanti e l'eccezione del firewall di gestione delle attività pianificate Remote è disabilitata, l'attività non verrà disabilitata quando viene letta da un'API Utilità di pianificazione 2,0.</span><span class="sxs-lookup"><span data-stu-id="29550-385">If a remote Task Scheduler 1.0 task is disabled by Schtasks.exe and the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled, then the task will not be disabled when read from a Task Scheduler 2.0 API.</span></span>

 

<span data-ttu-id="29550-386">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-386">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span><span class="sxs-lookup"><span data-stu-id="29550-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-388">Valore che contrassegna l'attività da eliminare dopo l'esecuzione finale.</span><span class="sxs-lookup"><span data-stu-id="29550-388">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="29550-389">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-389">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span> **DelayTime** /Delay</span><span class="sxs-lookup"><span data-stu-id="29550-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="29550-391">Valore che specifica il tempo di attesa per ritardare l'esecuzione dell'attività dopo che il trigger è stato attivato.</span><span class="sxs-lookup"><span data-stu-id="29550-391">A value that specifies the wait time to delay the running of the task after the trigger is fired.</span></span> <span data-ttu-id="29550-392">Il formato dell'ora è mmmm: SS.</span><span class="sxs-lookup"><span data-stu-id="29550-392">The time format is mmmm:ss.</span></span> <span data-ttu-id="29550-393">Questa opzione è valida solo per le attività con i tipi di pianificazione OnStart, ONLOGON e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="29550-393">This option is only valid for tasks with the schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="29550-394">**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="29550-394">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="29550-395"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="29550-395"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="29550-396">Valore che Visualizza il messaggio della Guida per Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="29550-396">A value that displays the Help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29550-397">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29550-397">Requirements</span></span>



| <span data-ttu-id="29550-398">Requisito</span><span class="sxs-lookup"><span data-stu-id="29550-398">Requirement</span></span> | <span data-ttu-id="29550-399">Valore</span><span class="sxs-lookup"><span data-stu-id="29550-399">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="29550-400">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29550-400">Minimum supported client</span></span><br/> | <span data-ttu-id="29550-401">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="29550-401">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="29550-402">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29550-402">Minimum supported server</span></span><br/> | <span data-ttu-id="29550-403">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="29550-403">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 





