---
description: Invia un processo a un sistema operativo per l'esecuzione a una data e ora specificate in futuro.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342351"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="aaec6-103">Metodo Create della classe Win32 \_ ScheduledJob</span><span class="sxs-lookup"><span data-stu-id="aaec6-103">Create method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="aaec6-104">Il metodo **Crea** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) Invia un processo a un sistema operativo per l'esecuzione a una data e ora specificate in futuro.</span><span class="sxs-lookup"><span data-stu-id="aaec6-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method submits a job to an operating system for execution at a specified time and date in the future.</span></span> <span data-ttu-id="aaec6-105">Questo metodo richiede che il servizio Schedule venga avviato nel computer a cui viene inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="aaec6-105">This method requires that the schedule service be started on the computer to which the job is submitted.</span></span>

<span data-ttu-id="aaec6-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="aaec6-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="aaec6-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="aaec6-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="aaec6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aaec6-108">Syntax</span></span>


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a><span data-ttu-id="aaec6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="aaec6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaec6-110">*Comando* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aaec6-110">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-111">Nome del comando, del programma batch o dei parametri del file binario e della riga di comando utilizzati dal servizio Schedule per richiamare il processo.</span><span class="sxs-lookup"><span data-stu-id="aaec6-111">Name of the command, batch program, or binary file and command-line parameters that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="aaec6-112">Esempio: "Defrag/q/f".</span><span class="sxs-lookup"><span data-stu-id="aaec6-112">Example: "defrag /q /f".</span></span>

</dd> <dt>

<span data-ttu-id="aaec6-113">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aaec6-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-114">Ora UTC (Coordinated Universal Time) per l'esecuzione di un processo.</span><span class="sxs-lookup"><span data-stu-id="aaec6-114">Coordinated Universal Time (UTC) time to run a job.</span></span> <span data-ttu-id="aaec6-115">Il formato deve essere: "ad aaaammgghhmmss. MMMMMM (+-) OOO ", dove" AAAAMMGG "deve essere sostituito da" \* \* \* \* \* \* \* \* ".</span><span class="sxs-lookup"><span data-stu-id="aaec6-115">The form must be: "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="aaec6-116">Ad esempio: " \* \* \* \* \* \* \* \* 143000.000000-420" specifica 14,30 (2:30) PST con ora legale in vigore.</span><span class="sxs-lookup"><span data-stu-id="aaec6-116">For example: "\*\*\*\*\*\*\*\*143000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

<span data-ttu-id="aaec6-117">La sezione "(+-) OOO" del valore della proprietà StartTime è la distorsione corrente per la conversione dell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="aaec6-117">The "(+-)OOO" section of the StartTime property value is the current bias for local time translation.</span></span> <span data-ttu-id="aaec6-118">La distorsione è la differenza tra l'ora UTC e l'ora locale.</span><span class="sxs-lookup"><span data-stu-id="aaec6-118">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="aaec6-119">Per calcolare la distorsione per il fuso orario, moltiplicare il numero di ore per cui il fuso orario è in anticipo o dietro la ora di Greenwich (GMT) di 60 (usare un numero positivo per il numero di ore se il fuso orario è preceduto da GMT e un numero negativo se il fuso orario è dietro GMT).</span><span class="sxs-lookup"><span data-stu-id="aaec6-119">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="aaec6-120">Aggiungere un ulteriore 60 al calcolo se il fuso orario USA l'ora legale.</span><span class="sxs-lookup"><span data-stu-id="aaec6-120">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="aaec6-121">Ad esempio, il fuso orario Pacifico standard è di otto ore dietro GMT, quindi la distorsione è uguale a-420 (-8 \* 60 + 60) quando l'ora legale è in uso e-480 (-8 \* 60) quando l'ora legale non è in uso.</span><span class="sxs-lookup"><span data-stu-id="aaec6-121">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="aaec6-122">È anche possibile determinare il valore della distorsione eseguendo una query sulla proprietà bias della classe [**del \_ fuso orario Win32**](win32-timezone.md) .</span><span class="sxs-lookup"><span data-stu-id="aaec6-122">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="aaec6-123">*RunRepeatedly* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="aaec6-123">*RunRepeatedly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-124">Se **true**, un processo pianificato viene eseguito ripetutamente in giorni specifici.</span><span class="sxs-lookup"><span data-stu-id="aaec6-124">If **True**, a scheduled job runs repeatedly on specific days.</span></span> <span data-ttu-id="aaec6-125">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="aaec6-125">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="aaec6-126">*DaysOfWeek* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="aaec6-126">*DaysOfWeek* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-127">Giorni della settimana in cui è pianificata l'esecuzione di un processo; utilizzato solo quando il parametro *RunRepeatedly* è **true**.</span><span class="sxs-lookup"><span data-stu-id="aaec6-127">Days of the week when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span> <span data-ttu-id="aaec6-128">Per pianificare un processo per più di un giorno della settimana, unire i valori appropriati in un operatore OR logico.</span><span class="sxs-lookup"><span data-stu-id="aaec6-128">To schedule a job for more than one day of the week, join the appropriate values in a logical OR.</span></span> <span data-ttu-id="aaec6-129">Per pianificare un processo per martedì e venerdì, ad esempio, il valore di *DaysOfWeek* è 2 o 16.</span><span class="sxs-lookup"><span data-stu-id="aaec6-129">For example, to schedule a job for Tuesdays and Fridays, the value of *DaysOfWeek* are 2 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="aaec6-130">**Lunedì** (1)</span><span class="sxs-lookup"><span data-stu-id="aaec6-130">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="aaec6-131">**Martedì** (2)</span><span class="sxs-lookup"><span data-stu-id="aaec6-131">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="aaec6-132">**Mercoledì** (4)</span><span class="sxs-lookup"><span data-stu-id="aaec6-132">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="aaec6-133">**Giovedi** (8)</span><span class="sxs-lookup"><span data-stu-id="aaec6-133">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="aaec6-134">**Venerdì** (16)</span><span class="sxs-lookup"><span data-stu-id="aaec6-134">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="aaec6-135">**Sabato** (32)</span><span class="sxs-lookup"><span data-stu-id="aaec6-135">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="aaec6-136">**Domenica** (64)</span><span class="sxs-lookup"><span data-stu-id="aaec6-136">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="aaec6-137">*DaysOfMonth* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="aaec6-137">*DaysOfMonth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-138">Giorni del mese in cui è pianificata l'esecuzione di un processo; utilizzato solo quando il parametro *RunRepeatedly* è **true**.</span><span class="sxs-lookup"><span data-stu-id="aaec6-138">Days of the month when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="aaec6-139"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="aaec6-139"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-140">Primo giorno del mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-140">Day 1 of a month</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="aaec6-141"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="aaec6-141"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-142">Giorno 2 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-142">Day 2 of a month</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="aaec6-143"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="aaec6-143"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-144">Giorno 3 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-144">Day 3 of a month</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="aaec6-145"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="aaec6-145"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-146">Giorno 4 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-146">Day 4 of a month</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="aaec6-147"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="aaec6-147"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-148">Giorno 5 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-148">Day 5 of a month</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="aaec6-149"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="aaec6-149"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-150">Giorno 6 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-150">Day 6 of a month</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="aaec6-151"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="aaec6-151"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-152">Giorno 7 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-152">Day 7 of a month</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="aaec6-153"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="aaec6-153"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-154">Giorno 8 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-154">Day 8 of a month</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="aaec6-155"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="aaec6-155"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-156">Giorno 9 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-156">Day 9 of a month</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="aaec6-157"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="aaec6-157"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-158">Giorno 10 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-158">Day 10 of a month</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="aaec6-159"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="aaec6-159"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-160">Giorno 11 del mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-160">Day 11 of a month</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="aaec6-161"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="aaec6-161"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-162">Giorno 12 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-162">Day 12 of a month</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="aaec6-163"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="aaec6-163"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-164">Giorno 13 del mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-164">Day 13 of a month</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="aaec6-165"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="aaec6-165"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-166">Giorno 14 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-166">Day 14 of a month</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="aaec6-167"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="aaec6-167"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-168">Giorno 15 del mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-168">Day 15 of a month</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="aaec6-169"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="aaec6-169"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-170">Giorno 16 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-170">Day 16 of a month</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="aaec6-171"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="aaec6-171"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-172">Giorno 17 del mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-172">Day 17 of a month</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="aaec6-173"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="aaec6-173"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-174">Giorno 18 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-174">Day 18 of a month</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="aaec6-175"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="aaec6-175"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-176">Giorno 19 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-176">Day 19 of a month</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="aaec6-177"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="aaec6-177"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-178">Giorno 20 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-178">Day 20 of a month</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="aaec6-179"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="aaec6-179"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-180">Giorno 21 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-180">Day 21 of a month</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="aaec6-181"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="aaec6-181"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-182">Giorno 22 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-182">Day 22 of a month</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="aaec6-183"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="aaec6-183"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-184">Giorno 23 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-184">Day 23 of a month</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="aaec6-185"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="aaec6-185"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-186">Giorno 24 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-186">Day 24 of a month</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="aaec6-187"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="aaec6-187"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-188">Giorno 25 del mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-188">Day 25 of a month</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="aaec6-189"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="aaec6-189"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-190">Giorno 26 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-190">Day 26 of a month</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="aaec6-191"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="aaec6-191"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-192">Giorno 27 del mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-192">Day 27 of a month</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="aaec6-193"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="aaec6-193"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-194">Giorno 28 del mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-194">Day 28 of a month</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="aaec6-195"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="aaec6-195"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-196">29 giorni di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-196">Day 29 of a month</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="aaec6-197"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="aaec6-197"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-198">Giorno 30 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-198">Day 30 of a month</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="aaec6-199"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="aaec6-199"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="aaec6-200">Giorno 31 di un mese</span><span class="sxs-lookup"><span data-stu-id="aaec6-200">Day 31 of a month</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="aaec6-201">*InteractWithDesktop* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="aaec6-201">*InteractWithDesktop* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-202">Se **true**, il processo specificato deve essere interattivo, il che significa che un utente può fornire l'input a un processo pianificato mentre il processo è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="aaec6-202">If **True**, the specified job should be interactive, which means that a user can give input to a scheduled job while the job is executing.</span></span> <span data-ttu-id="aaec6-203">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="aaec6-203">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="aaec6-204">*JobID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aaec6-204">*JobId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-205">Identificatore del numero di un processo.</span><span class="sxs-lookup"><span data-stu-id="aaec6-205">Identifier number of a job.</span></span> <span data-ttu-id="aaec6-206">Questo parametro è un handle per un processo pianificato in un computer.</span><span class="sxs-lookup"><span data-stu-id="aaec6-206">This parameter is a handle to a job being scheduled on a computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaec6-207">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aaec6-207">Return value</span></span>

<span data-ttu-id="aaec6-208">Restituisce un valore pari a 0 (zero) quando ha esito positivo e un numero diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="aaec6-208">Returns a value of 0 (zero) when successful, and a different number to indicate an error.</span></span> <span data-ttu-id="aaec6-209">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="aaec6-209">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="aaec6-210">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="aaec6-210">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="aaec6-211">**Operazione completata**</span><span class="sxs-lookup"><span data-stu-id="aaec6-211">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-212">0</span><span class="sxs-lookup"><span data-stu-id="aaec6-212">0</span></span>

<span data-ttu-id="aaec6-213">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="aaec6-213">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="aaec6-214">**Non supportato**</span><span class="sxs-lookup"><span data-stu-id="aaec6-214">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-215">1</span><span class="sxs-lookup"><span data-stu-id="aaec6-215">1</span></span>

<span data-ttu-id="aaec6-216">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="aaec6-216">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="aaec6-217">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="aaec6-217">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-218">2</span><span class="sxs-lookup"><span data-stu-id="aaec6-218">2</span></span>

<span data-ttu-id="aaec6-219">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="aaec6-219">The user does not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="aaec6-220">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="aaec6-220">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-221">8</span><span class="sxs-lookup"><span data-stu-id="aaec6-221">8</span></span>

<span data-ttu-id="aaec6-222">Processo interattivo.</span><span class="sxs-lookup"><span data-stu-id="aaec6-222">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="aaec6-223">**Impossibile trovare il percorso**</span><span class="sxs-lookup"><span data-stu-id="aaec6-223">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-224">9</span><span class="sxs-lookup"><span data-stu-id="aaec6-224">9</span></span>

<span data-ttu-id="aaec6-225">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="aaec6-225">The directory path to the service executable file cannot be found.</span></span>

</dd> <dt>

<span data-ttu-id="aaec6-226">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="aaec6-226">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-227">21</span><span class="sxs-lookup"><span data-stu-id="aaec6-227">21</span></span>

<span data-ttu-id="aaec6-228">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="aaec6-228">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="aaec6-229">**Servizio non avviato**</span><span class="sxs-lookup"><span data-stu-id="aaec6-229">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-230">22</span><span class="sxs-lookup"><span data-stu-id="aaec6-230">22</span></span>

<span data-ttu-id="aaec6-231">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="aaec6-231">The account that this service runs under is invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="aaec6-232">**Altri**</span><span class="sxs-lookup"><span data-stu-id="aaec6-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="aaec6-233">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="aaec6-233">23 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aaec6-234">Commenti</span><span class="sxs-lookup"><span data-stu-id="aaec6-234">Remarks</span></span>

<span data-ttu-id="aaec6-235">Se il processo pianificato avvia un programma interattivo, ad esempio Blocco note, la proprietà **InteractWithDeskto** deve essere impostata su **true** o la schermata del programma non è visibile.</span><span class="sxs-lookup"><span data-stu-id="aaec6-235">If your scheduled job starts an interactive program such as Notepad, then the **InteractWithDeskto** property must be set to **True** or the program's screen is not visible.</span></span> <span data-ttu-id="aaec6-236">Il processo viene comunque visualizzato in **Gestione attività** anche se non viene visualizzato sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="aaec6-236">The process still appears in the **Task Manager** even if it does not appear on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaec6-237">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aaec6-237">Requirements</span></span>



| <span data-ttu-id="aaec6-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaec6-238">Requirement</span></span> | <span data-ttu-id="aaec6-239">Valore</span><span class="sxs-lookup"><span data-stu-id="aaec6-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaec6-240">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaec6-240">Minimum supported client</span></span><br/> | <span data-ttu-id="aaec6-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aaec6-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aaec6-242">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaec6-242">Minimum supported server</span></span><br/> | <span data-ttu-id="aaec6-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aaec6-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aaec6-244">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aaec6-244">Namespace</span></span><br/>                | <span data-ttu-id="aaec6-245">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="aaec6-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aaec6-246">MOF</span><span class="sxs-lookup"><span data-stu-id="aaec6-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aaec6-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aaec6-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aaec6-248">DLL</span><span class="sxs-lookup"><span data-stu-id="aaec6-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaec6-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaec6-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaec6-250">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aaec6-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="aaec6-251">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aaec6-251">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="aaec6-252">**\_ScheduledJob Win32**</span><span class="sxs-lookup"><span data-stu-id="aaec6-252">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

