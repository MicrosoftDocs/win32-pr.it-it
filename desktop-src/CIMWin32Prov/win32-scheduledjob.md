---
description: Rappresenta un processo creato con il comando AT.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049117"
---
# <a name="win32_scheduledjob-class"></a><span data-ttu-id="fc609-103">Win32 \_ ScheduledJob (classe)</span><span class="sxs-lookup"><span data-stu-id="fc609-103">Win32\_ScheduledJob class</span></span>

<span data-ttu-id="fc609-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ScheduledJob Win32**   rappresenta un processo creato con il comando **at** .</span><span class="sxs-lookup"><span data-stu-id="fc609-104">The **Win32\_ScheduledJob** [WMI class](../wmisdk/retrieving-a-class.md) represents a job created with the **AT** command.</span></span>

> [!Note]  
> <span data-ttu-id="fc609-105">La classe **Win32 \_ ScheduledJob** non rappresenta un processo creato con la creazione guidata attività pianificata dal pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="fc609-105">The **Win32\_ScheduledJob** class does not represent a job created with the Scheduled Task Wizard from the Control Panel.</span></span> <span data-ttu-id="fc609-106">Non è possibile modificare un'attività creata da WMI nell'interfaccia utente delle attività pianificate.</span><span class="sxs-lookup"><span data-stu-id="fc609-106">You cannot change a task created by WMI in the Scheduled Tasks UI.</span></span> <span data-ttu-id="fc609-107">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="fc609-107">For more information, see the Remarks section.</span></span>

 

<span data-ttu-id="fc609-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fc609-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fc609-109">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="fc609-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc609-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc609-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="fc609-111">Members</span><span class="sxs-lookup"><span data-stu-id="fc609-111">Members</span></span>

<span data-ttu-id="fc609-112">La classe **Win32 \_ ScheduledJob** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fc609-112">The **Win32\_ScheduledJob** class has these types of members:</span></span>

-   [<span data-ttu-id="fc609-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="fc609-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="fc609-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fc609-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fc609-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="fc609-115">Methods</span></span>

<span data-ttu-id="fc609-116">La classe **Win32 \_ ScheduledJob** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="fc609-116">The **Win32\_ScheduledJob** class has these methods.</span></span>



| <span data-ttu-id="fc609-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="fc609-117">Method</span></span>                                                      | <span data-ttu-id="fc609-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc609-118">Description</span></span>                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc609-119">**Creare**</span><span class="sxs-lookup"><span data-stu-id="fc609-119">**Create**</span></span>](create-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="fc609-120">Metodo della classe che invia un processo al sistema operativo per l'esecuzione in una data e ora future specificate.</span><span class="sxs-lookup"><span data-stu-id="fc609-120">Class method that submits a job to the operating system for execution at a specified future time and date.</span></span><br/> |
| [<span data-ttu-id="fc609-121">**Delete**</span><span class="sxs-lookup"><span data-stu-id="fc609-121">**Delete**</span></span>](delete-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="fc609-122">Metodo della classe che elimina un processo pianificato.</span><span class="sxs-lookup"><span data-stu-id="fc609-122">Class method that deletes a scheduled job.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="fc609-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fc609-123">Properties</span></span>

<span data-ttu-id="fc609-124">La classe **Win32 \_ ScheduledJob** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fc609-124">The **Win32\_ScheduledJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc609-125">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="fc609-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc609-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-128">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="fc609-128">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-129">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fc609-129">A short textual description of the object.</span></span>

<span data-ttu-id="fc609-130">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc609-131">**Comando**</span><span class="sxs-lookup"><span data-stu-id="fc609-131">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc609-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-134">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Command**")</span><span class="sxs-lookup"><span data-stu-id="fc609-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Command**")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-135">Nome del comando, del programma batch o del file binario (e degli argomenti della riga di comando) usati dal servizio Schedule per richiamare il processo.</span><span class="sxs-lookup"><span data-stu-id="fc609-135">Name of the command, batch program, or binary file (and command-line arguments) that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="fc609-136">Esempio: "**Defrag** **/q/f**"</span><span class="sxs-lookup"><span data-stu-id="fc609-136">Example: "**defrag** **/q/f**"</span></span>

</dd> <dt>

<span data-ttu-id="fc609-137">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="fc609-137">**DaysOfMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-138">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc609-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-140">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**")</span><span class="sxs-lookup"><span data-stu-id="fc609-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfMonth**")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-141">Giorni del mese in cui è pianificata l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="fc609-141">Days of the month when the job is scheduled to run.</span></span> <span data-ttu-id="fc609-142">Se un processo è pianificato per essere eseguito in più giorni del mese, questi valori possono essere Uniti in un OR logico.</span><span class="sxs-lookup"><span data-stu-id="fc609-142">If a job is scheduled to run on multiple days of the month, these values can be joined in a logical OR.</span></span> <span data-ttu-id="fc609-143">Se, ad esempio, un processo deve essere eseguito il 1 ° e il sedicesimo di ogni mese, il valore della proprietà **DaysOfMonth** sarà 1 o 32768.</span><span class="sxs-lookup"><span data-stu-id="fc609-143">For example, if a job is to run on the 1st and 16th of each month, the value of the **DaysOfMonth** property would be 1 OR 32768.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="fc609-144"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="fc609-144"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-145">1 °</span><span class="sxs-lookup"><span data-stu-id="fc609-145">1st</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="fc609-146"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="fc609-146"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-147">secondo</span><span class="sxs-lookup"><span data-stu-id="fc609-147">2nd</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="fc609-148"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="fc609-148"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-149">3°</span><span class="sxs-lookup"><span data-stu-id="fc609-149">3rd</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="fc609-150"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="fc609-150"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-151">4°</span><span class="sxs-lookup"><span data-stu-id="fc609-151">4th</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="fc609-152"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="fc609-152"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-153">5°</span><span class="sxs-lookup"><span data-stu-id="fc609-153">5th</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="fc609-154"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="fc609-154"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-155">6°</span><span class="sxs-lookup"><span data-stu-id="fc609-155">6th</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="fc609-156"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="fc609-156"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-157">7°</span><span class="sxs-lookup"><span data-stu-id="fc609-157">7th</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="fc609-158"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="fc609-158"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-159">8°</span><span class="sxs-lookup"><span data-stu-id="fc609-159">8th</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="fc609-160"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="fc609-160"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-161">9°</span><span class="sxs-lookup"><span data-stu-id="fc609-161">9th</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="fc609-162"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="fc609-162"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-163">10</span><span class="sxs-lookup"><span data-stu-id="fc609-163">10th</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="fc609-164"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="fc609-164"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-165">11°</span><span class="sxs-lookup"><span data-stu-id="fc609-165">11th</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="fc609-166"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="fc609-166"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-167">12°</span><span class="sxs-lookup"><span data-stu-id="fc609-167">12th</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="fc609-168"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="fc609-168"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-169">13°</span><span class="sxs-lookup"><span data-stu-id="fc609-169">13th</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="fc609-170"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="fc609-170"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-171">14</span><span class="sxs-lookup"><span data-stu-id="fc609-171">14th</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="fc609-172"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="fc609-172"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-173">15</span><span class="sxs-lookup"><span data-stu-id="fc609-173">15th</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="fc609-174"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="fc609-174"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-175">16</span><span class="sxs-lookup"><span data-stu-id="fc609-175">16th</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="fc609-176"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="fc609-176"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-177">17</span><span class="sxs-lookup"><span data-stu-id="fc609-177">17th</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="fc609-178"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="fc609-178"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-179">18</span><span class="sxs-lookup"><span data-stu-id="fc609-179">18th</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="fc609-180"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="fc609-180"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-181">19</span><span class="sxs-lookup"><span data-stu-id="fc609-181">19th</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="fc609-182"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="fc609-182"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-183">20</span><span class="sxs-lookup"><span data-stu-id="fc609-183">20th</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="fc609-184"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="fc609-184"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-185">21°</span><span class="sxs-lookup"><span data-stu-id="fc609-185">21st</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="fc609-186"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="fc609-186"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-187">22°</span><span class="sxs-lookup"><span data-stu-id="fc609-187">22nd</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="fc609-188"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="fc609-188"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-189">23°</span><span class="sxs-lookup"><span data-stu-id="fc609-189">23rd</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="fc609-190"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="fc609-190"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-191">24</span><span class="sxs-lookup"><span data-stu-id="fc609-191">24th</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="fc609-192"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="fc609-192"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-193">25</span><span class="sxs-lookup"><span data-stu-id="fc609-193">25th</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="fc609-194"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="fc609-194"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-195">26</span><span class="sxs-lookup"><span data-stu-id="fc609-195">26th</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="fc609-196"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="fc609-196"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-197">27</span><span class="sxs-lookup"><span data-stu-id="fc609-197">27th</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="fc609-198"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="fc609-198"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-199">28</span><span class="sxs-lookup"><span data-stu-id="fc609-199">28th</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="fc609-200"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="fc609-200"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-201">29</span><span class="sxs-lookup"><span data-stu-id="fc609-201">29th</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="fc609-202"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="fc609-202"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-203">30</span><span class="sxs-lookup"><span data-stu-id="fc609-203">30th</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="fc609-204"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="fc609-204"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="fc609-205">31</span><span class="sxs-lookup"><span data-stu-id="fc609-205">31st</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc609-206">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="fc609-206">**DaysOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-207">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc609-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-209">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")</span><span class="sxs-lookup"><span data-stu-id="fc609-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfWeek**")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-210">Giorni della settimana in cui è pianificata l'esecuzione di un processo.</span><span class="sxs-lookup"><span data-stu-id="fc609-210">Days of the week when a job is scheduled to run.</span></span> <span data-ttu-id="fc609-211">Se un processo è pianificato per essere eseguito in più giorni della settimana, i valori possono essere Uniti in un OR logico.</span><span class="sxs-lookup"><span data-stu-id="fc609-211">If a job is scheduled to run on multiple days of the week, the values can be joined in a logical OR.</span></span> <span data-ttu-id="fc609-212">Se, ad esempio, si pianifica l'esecuzione di un processo lunedì, mercoledì e venerdì, il valore della proprietà **DaysOfWeek** sarà 1 o 4 o 16.</span><span class="sxs-lookup"><span data-stu-id="fc609-212">For example, if a job is scheduled to run on Mondays, Wednesdays, and Fridays the value of the **DaysOfWeek** property would be 1 OR 4 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="fc609-213">**Lunedì** (1)</span><span class="sxs-lookup"><span data-stu-id="fc609-213">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="fc609-214">**Martedì** (2)</span><span class="sxs-lookup"><span data-stu-id="fc609-214">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="fc609-215">**Mercoledì** (4)</span><span class="sxs-lookup"><span data-stu-id="fc609-215">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="fc609-216">**Giovedi** (8)</span><span class="sxs-lookup"><span data-stu-id="fc609-216">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="fc609-217">**Venerdì** (16)</span><span class="sxs-lookup"><span data-stu-id="fc609-217">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="fc609-218">**Sabato** (32)</span><span class="sxs-lookup"><span data-stu-id="fc609-218">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="fc609-219">**Domenica** (64)</span><span class="sxs-lookup"><span data-stu-id="fc609-219">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc609-220">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="fc609-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc609-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-223">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="fc609-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-224">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fc609-224">A textual description of the object.</span></span>

<span data-ttu-id="fc609-225">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc609-226">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="fc609-226">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-227">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fc609-227">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc609-229">Periodo di tempo durante il quale il processo è stato eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc609-229">Length of time the job has been executing.</span></span>

<span data-ttu-id="fc609-230">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-230">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc609-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fc609-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-232">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fc609-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-234">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="fc609-234">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-235">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="fc609-235">Indicates when the object was installed.</span></span> <span data-ttu-id="fc609-236">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="fc609-236">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="fc609-237">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc609-238">**InteractWithDesktop**</span><span class="sxs-lookup"><span data-stu-id="fc609-238">**InteractWithDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-239">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fc609-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-241">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **Job \_ Interactive**")</span><span class="sxs-lookup"><span data-stu-id="fc609-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_NONINTERACTIVE**")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-242">Il processo specificato è interattivo, il che significa che un utente può fornire l'input a un processo pianificato mentre è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fc609-242">Specified job is interactive, which means that a user can give input to a scheduled job while it is executing.</span></span>

</dd> <dt>

<span data-ttu-id="fc609-243">**JobId**</span><span class="sxs-lookup"><span data-stu-id="fc609-243">**JobId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-244">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc609-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-246">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobID**")</span><span class="sxs-lookup"><span data-stu-id="fc609-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobId**")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-247">Numero di identificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="fc609-247">Identifying number of the job.</span></span> <span data-ttu-id="fc609-248">Viene usato dai metodi come handle per un processo pianificato in questo computer.</span><span class="sxs-lookup"><span data-stu-id="fc609-248">It is used by methods as a handle to one job being scheduled on this computer.</span></span>

</dd> <dt>

<span data-ttu-id="fc609-249">**Stato processo**</span><span class="sxs-lookup"><span data-stu-id="fc609-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-250">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc609-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-252">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **Flags** \| **Job \_ Exec \_ Error**")</span><span class="sxs-lookup"><span data-stu-id="fc609-252">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**Flags**\|**JOB\_EXEC\_ERROR**")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-253">Stato di esecuzione dell'ultima volta in cui è stato pianificato l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="fc609-253">Status of execution the last time this job was scheduled to run.</span></span>

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

<span data-ttu-id="fc609-254">**Esito positivo** ("operazione riuscita")</span><span class="sxs-lookup"><span data-stu-id="fc609-254">**Success** ("Success")</span></span>


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

<span data-ttu-id="fc609-255">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="fc609-255">**Failure** ("Failure")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc609-256">**Nome**</span><span class="sxs-lookup"><span data-stu-id="fc609-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc609-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-259">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="fc609-259">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-260">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="fc609-260">Label by which the object is known.</span></span> <span data-ttu-id="fc609-261">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="fc609-261">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="fc609-262">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc609-263">**Notificare**</span><span class="sxs-lookup"><span data-stu-id="fc609-263">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc609-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc609-266">L'utente riceve una notifica al completamento o all'esito negativo del processo.</span><span class="sxs-lookup"><span data-stu-id="fc609-266">User is notified upon job completion or failure.</span></span>

<span data-ttu-id="fc609-267">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-267">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc609-268">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="fc609-268">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-269">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc609-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc609-271">Utente che ha inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="fc609-271">User who submitted the job.</span></span>

<span data-ttu-id="fc609-272">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-272">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc609-273">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="fc609-273">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-274">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc609-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc609-276">Importanza dell'esecuzione di un processo.</span><span class="sxs-lookup"><span data-stu-id="fc609-276">Importance of a job's execution.</span></span>

<span data-ttu-id="fc609-277">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-277">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc609-278">**RunRepeatedly**</span><span class="sxs-lookup"><span data-stu-id="fc609-278">**RunRepeatedly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-279">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fc609-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-281">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API le \| strutture \| [**di gestione di rete nel processo di flag \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \|  \| **\_ vengono eseguite \_ periodicamente**")</span><span class="sxs-lookup"><span data-stu-id="fc609-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_RUN\_PERIODICALLY**")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-282">Il processo pianificato viene eseguito ripetutamente nei giorni in cui il processo è pianificato.</span><span class="sxs-lookup"><span data-stu-id="fc609-282">Scheduled job runs repeatedly on the days that the job is scheduled.</span></span> <span data-ttu-id="fc609-283">Se **false**, il processo viene eseguito una sola volta.</span><span class="sxs-lookup"><span data-stu-id="fc609-283">If **False**, then the job is run one time.</span></span>

</dd> <dt>

<span data-ttu-id="fc609-284">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="fc609-284">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-285">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fc609-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-287">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobTime**")</span><span class="sxs-lookup"><span data-stu-id="fc609-287">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobTime**")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-288">Ora UTC in cui eseguire il processo, nel formato "ad aaaammgghhmmss. MMMMMM (+-) OOO ", dove" AAAAMMGG "deve essere sostituito da" \* \* \* \* \* \* \* \* ".</span><span class="sxs-lookup"><span data-stu-id="fc609-288">UTC time to run the job, in the form of "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="fc609-289">La sostituzione è necessaria perché il servizio di pianificazione consente solo la configurazione dei processi per l'esecuzione una sola volta o l'esecuzione in un giorno del mese o settimana.</span><span class="sxs-lookup"><span data-stu-id="fc609-289">The replacement is necessary because the scheduling service only allows jobs to be configured to run one time, or run on a day of the month or week.</span></span> <span data-ttu-id="fc609-290">Un processo non può essere eseguito in una data specifica.</span><span class="sxs-lookup"><span data-stu-id="fc609-290">A job cannot be run on a specific date.</span></span>

<span data-ttu-id="fc609-291">La sezione "(+-) OOO" del valore della proprietà **StartTime** è la distorsione corrente per la conversione dell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="fc609-291">The "(+-)OOO" section of the **StartTime** property value is the current bias for local time translation.</span></span> <span data-ttu-id="fc609-292">La distorsione è la differenza tra l'ora UTC e l'ora locale.</span><span class="sxs-lookup"><span data-stu-id="fc609-292">The bias is the difference between the UTC time and local time.</span></span> <span data-ttu-id="fc609-293">Per calcolare la distorsione per il fuso orario, moltiplicare il numero di ore per cui il fuso orario è in anticipo o dietro la ora di Greenwich (GMT) di 60 (usare un numero positivo per il numero di ore se il fuso orario è preceduto da GMT e un numero negativo se il fuso orario è dietro GMT).</span><span class="sxs-lookup"><span data-stu-id="fc609-293">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="fc609-294">Aggiungere un ulteriore 60 al calcolo se il fuso orario USA l'ora legale.</span><span class="sxs-lookup"><span data-stu-id="fc609-294">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="fc609-295">Ad esempio, il fuso orario Pacifico standard è di otto ore dietro GMT, quindi la distorsione è uguale a-420 (-8 \* 60 + 60) quando l'ora legale è in uso e-480 (-8 \* 60) quando l'ora legale non è in uso.</span><span class="sxs-lookup"><span data-stu-id="fc609-295">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="fc609-296">È anche possibile determinare il valore della distorsione eseguendo una query sulla proprietà bias della classe [**del \_ fuso orario Win32**](win32-timezone.md) .</span><span class="sxs-lookup"><span data-stu-id="fc609-296">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

<span data-ttu-id="fc609-297">Ad esempio: " \* \* \* \* \* \* \* \* 123000.000000-420" specifica 14,30 (2:30) PST con ora legale in vigore.</span><span class="sxs-lookup"><span data-stu-id="fc609-297">For example: "\*\*\*\*\*\*\*\*123000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

</dd> <dt>

<span data-ttu-id="fc609-298">**Status**</span><span class="sxs-lookup"><span data-stu-id="fc609-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-299">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc609-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc609-301">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="fc609-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fc609-302">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fc609-302">String that indicates the current status of the object.</span></span> <span data-ttu-id="fc609-303">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="fc609-303">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="fc609-304">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="fc609-304">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="fc609-305">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="fc609-305">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="fc609-306">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="fc609-306">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fc609-307">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="fc609-307">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fc609-308">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="fc609-308">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fc609-309">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-309">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fc609-310">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc609-310">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fc609-311">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="fc609-311">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fc609-312">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="fc609-312">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fc609-313">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="fc609-313">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc609-314">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="fc609-314">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fc609-315">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="fc609-315">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fc609-316">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="fc609-316">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fc609-317">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="fc609-317">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fc609-318">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="fc609-318">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fc609-319">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="fc609-319">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fc609-320">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="fc609-320">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fc609-321">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="fc609-321">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fc609-322">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="fc609-322">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc609-323">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="fc609-323">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-324">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fc609-324">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc609-326">Ora di invio del processo.</span><span class="sxs-lookup"><span data-stu-id="fc609-326">Time that the job was submitted.</span></span>

<span data-ttu-id="fc609-327">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-327">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc609-328">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="fc609-328">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc609-329">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fc609-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc609-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc609-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc609-331">Ora in cui il processo non è valido o deve essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="fc609-331">Time at which the job is invalid or should be stopped.</span></span>

<span data-ttu-id="fc609-332">Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-332">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc609-333">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc609-333">Remarks</span></span>

<span data-ttu-id="fc609-334">Ogni processo pianificato per il servizio Schedule viene archiviato in modo permanente (l'utilità di pianificazione può avviare un processo dopo un riavvio) e viene eseguito all'ora e al giorno della settimana o del mese specificati.</span><span class="sxs-lookup"><span data-stu-id="fc609-334">Each job scheduled against the schedule service is stored persistently (the scheduler can start a job after a reboot), and is executed at the specified time and day of the week or month.</span></span> <span data-ttu-id="fc609-335">Se il computer non è attivo o se il servizio pianificato non è in esecuzione all'ora del processo specificata, il servizio Schedule esegue il processo specificato il giorno successivo all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="fc609-335">If the computer is not active, or if the scheduled service is not running at the specified job time, the schedule service runs the specified job on the next day at the specified time.</span></span>

<span data-ttu-id="fc609-336">I processi sono pianificati in base all'ora UTC (Coordinated Universal Time) con offset di distorsione rispetto all'ora di Greenwich (GMT), il che significa che è possibile specificare un processo usando qualsiasi fuso orario.</span><span class="sxs-lookup"><span data-stu-id="fc609-336">Jobs are scheduled according to Coordinated Universal Time (UTC) with bias offset from Greenwich Mean Time (GMT), which means that a job can be specified using any time zone.</span></span> <span data-ttu-id="fc609-337">La classe **Win32 \_ ScheduledJob** restituisce l'ora locale con offset UTC durante l'enumerazione di un oggetto e viene convertita nell'ora locale durante la creazione di nuovi processi.</span><span class="sxs-lookup"><span data-stu-id="fc609-337">The **Win32\_ScheduledJob** class returns the local time with UTC offset when enumerating an object, and converts to local time when creating new jobs.</span></span> <span data-ttu-id="fc609-338">Ad esempio, un processo specificato per l'esecuzione in un computer a Boston alle ore 10:30.</span><span class="sxs-lookup"><span data-stu-id="fc609-338">For example, a job specified to run on a computer in Boston at 10:30 P.M.</span></span> <span data-ttu-id="fc609-339">Il tempo di lunedì PST verrà pianificato per essere eseguito localmente alle ore 1:30.</span><span class="sxs-lookup"><span data-stu-id="fc609-339">Monday PST time will be scheduled to run locally at 1:30 A.M.</span></span> <span data-ttu-id="fc609-340">Martedì EST.</span><span class="sxs-lookup"><span data-stu-id="fc609-340">Tuesday EST.</span></span>

> [!Note]  
> <span data-ttu-id="fc609-341">Un client deve prendere in considerazione se l'ora legale è in esecuzione nel computer locale e, in tal caso, sottrarre un bias di 60 minuti dall'offset UTC.</span><span class="sxs-lookup"><span data-stu-id="fc609-341">A client must take into account whether or not daylight savings time is in operation on the local computer, and if it is, then subtract a bias of 60 minutes from the UTC offset.</span></span>

 

<span data-ttu-id="fc609-342">La classe **Win32 \_ ScheduledJob** è derivata dal [**\_ processo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-342">The **Win32\_ScheduledJob** class is derived from [**CIM\_Job**](cim-job.md).</span></span> <span data-ttu-id="fc609-343">Per creare un processo pianificato utilizzando questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="fc609-343">You must be a member of the administrators group to create a scheduled job using this class.</span></span>

<span data-ttu-id="fc609-344">La classe **Win32 \_ ScheduledJob** utilizza internamente il protocollo at, che è associato a deprecazione a partire da Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="fc609-344">The **Win32\_ScheduledJob** class is internally using the AT protocol, which is bound to deprecation starting with Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="fc609-345">Come primo passaggio, il protocollo AT è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="fc609-345">As a first step the AT protocol is disabled by default.</span></span> <span data-ttu-id="fc609-346">Se il protocollo è disabilitato, ad esempio la chiamata al metodo [**create**](create-method-in-class-win32-scheduledjob.md) su un oggetto **Win32 \_ ScheduledJob** avrà esito negativo con errore 0x8.</span><span class="sxs-lookup"><span data-stu-id="fc609-346">If the protocol is disabled, for example calling the [**Create**](create-method-in-class-win32-scheduledjob.md) method on a **Win32\_ScheduledJob** object will fail with error 0x8.</span></span> <span data-ttu-id="fc609-347">È possibile attivare di nuovo il protocollo AT aggiungendo la seguente voce del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="fc609-347">You can turn the AT protocol back on by adding the following registry entry:</span></span>

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

<span data-ttu-id="fc609-348">Potrebbe essere necessario riavviare il computer per rendere effettiva l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="fc609-348">You may need to restart the machine to make the setting effective.</span></span>

<span data-ttu-id="fc609-349">Poiché **Win32 \_ ScheduledJob** è basato sull'API Win32 [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) , non è possibile usare questa classe insieme al utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="fc609-349">Because **Win32\_ScheduledJob** is based on the [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) Win32 API, you cannot use this class in conjunction with the Task Scheduler.</span></span> <span data-ttu-id="fc609-350">Se si desidera utilizzare Utilità di pianificazione, utilizzare l'API Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="fc609-350">If you wish to use Task Scheduler, use the Task Scheduler API.</span></span> <span data-ttu-id="fc609-351">Per ulteriori informazioni, vedere il [riferimento utilità di pianificazione](../taskschd/task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="fc609-351">For more information, see the [Task Scheduler Reference](../taskschd/task-scheduler-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fc609-352">Esempio</span><span class="sxs-lookup"><span data-stu-id="fc609-352">Examples</span></span>

<span data-ttu-id="fc609-353">Nell'esempio di codice VBScript seguente viene pianificato Notepad.exe per l'esecuzione interattiva a 1:25 dall'ora del computer locale ogni mercoledì.</span><span class="sxs-lookup"><span data-stu-id="fc609-353">The following VBScript code example schedules Notepad.exe to run interactively at 1:25 by the local computer time every Wednesday.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



## <a name="requirements"></a><span data-ttu-id="fc609-354">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc609-354">Requirements</span></span>



| <span data-ttu-id="fc609-355">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc609-355">Requirement</span></span> | <span data-ttu-id="fc609-356">Valore</span><span class="sxs-lookup"><span data-stu-id="fc609-356">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc609-357">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc609-357">Minimum supported client</span></span><br/> | <span data-ttu-id="fc609-358">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc609-358">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc609-359">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc609-359">Minimum supported server</span></span><br/> | <span data-ttu-id="fc609-360">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc609-360">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc609-361">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fc609-361">Namespace</span></span><br/>                | <span data-ttu-id="fc609-362">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fc609-362">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fc609-363">MOF</span><span class="sxs-lookup"><span data-stu-id="fc609-363">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc609-364"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc609-364"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc609-365">DLL</span><span class="sxs-lookup"><span data-stu-id="fc609-365">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc609-366"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc609-366"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc609-367">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc609-367">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc609-368">**\_Processo CIM**</span><span class="sxs-lookup"><span data-stu-id="fc609-368">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dt>

[<span data-ttu-id="fc609-369">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="fc609-369">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="fc609-370">Attività WMI: attività pianificate</span><span class="sxs-lookup"><span data-stu-id="fc609-370">WMI Tasks: Scheduled Tasks</span></span>](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
