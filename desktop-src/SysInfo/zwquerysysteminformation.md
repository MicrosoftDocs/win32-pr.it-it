---
description: Recupera le informazioni di sistema specificate.
ms.assetid: c91b9a35-ca2b-4d81-973d-fe709144df90
title: ZwQuerySystemInformation (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQuerySystemInformation
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 2e516b12e5109470c1ddb86ea6a665ca29f138b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329100"
---
# <a name="zwquerysysteminformation-function"></a><span data-ttu-id="b4203-103">ZwQuerySystemInformation (funzione)</span><span class="sxs-lookup"><span data-stu-id="b4203-103">ZwQuerySystemInformation function</span></span>

<span data-ttu-id="b4203-104">\[**ZwQuerySystemInformation** non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b4203-104">\[**ZwQuerySystemInformation** is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b4203-105">Usare invece le funzioni alternative elencate in questo argomento.\]</span><span class="sxs-lookup"><span data-stu-id="b4203-105">Instead, use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="b4203-106">Recupera le informazioni di sistema specificate.</span><span class="sxs-lookup"><span data-stu-id="b4203-106">Retrieves the specified system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4203-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4203-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="b4203-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4203-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4203-109">*SystemInformationClass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4203-109">*SystemInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4203-110">Tipo di informazioni di sistema da recuperare.</span><span class="sxs-lookup"><span data-stu-id="b4203-110">The type of system information to be retrieved.</span></span> <span data-ttu-id="b4203-111">Questo parametro può essere uno dei valori seguenti del tipo di **enumerazione \_ \_ classe informazioni di sistema** .</span><span class="sxs-lookup"><span data-stu-id="b4203-111">This parameter can be one of the following values from the **SYSTEM\_INFORMATION\_CLASS** enumeration type.</span></span>

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span data-ttu-id="b4203-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span><span class="sxs-lookup"><span data-stu-id="b4203-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-113">Il numero di processori nel sistema in una struttura **di \_ \_ informazioni di base del sistema** .</span><span class="sxs-lookup"><span data-stu-id="b4203-113">The number of processors in the system in a **SYSTEM\_BASIC\_INFORMATION** structure.</span></span> <span data-ttu-id="b4203-114">Usare invece la funzione [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .</span><span class="sxs-lookup"><span data-stu-id="b4203-114">Use the [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function instead.</span></span>

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span data-ttu-id="b4203-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span><span class="sxs-lookup"><span data-stu-id="b4203-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-116">Struttura di **\_ \_ informazioni sulle prestazioni di sistema** opaca che può essere utilizzata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali.</span><span class="sxs-lookup"><span data-stu-id="b4203-116">An opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="b4203-117">Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="b4203-117">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span data-ttu-id="b4203-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span><span class="sxs-lookup"><span data-stu-id="b4203-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-119">Struttura di **\_ \_ informazioni TimeOfDay di sistema** opaca che può essere usata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali.</span><span class="sxs-lookup"><span data-stu-id="b4203-119">An opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="b4203-120">Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="b4203-120">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span data-ttu-id="b4203-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span><span class="sxs-lookup"><span data-stu-id="b4203-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-122">Matrice di strutture **di \_ \_ informazioni del processo di sistema** , una per ogni processo in esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b4203-122">An array of **SYSTEM\_PROCESS\_INFORMATION** structures, one for each process running in the system.</span></span>

<span data-ttu-id="b4203-123">Queste strutture contengono informazioni sull'utilizzo delle risorse di ogni processo, tra cui il numero di handle utilizzati dal processo, il picco di utilizzo del file di paging e il numero di pagine di memoria allocate dal processo.</span><span class="sxs-lookup"><span data-stu-id="b4203-123">These structures contain information about the resource usage of each process, including the number of handles used by the process, the peak page-file usage, and the number of memory pages that the process has allocated.</span></span>

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span data-ttu-id="b4203-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span><span class="sxs-lookup"><span data-stu-id="b4203-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-125">Una matrice di strutture di **\_ \_ \_ informazioni sulle prestazioni del processore di sistema** , una per ogni processore installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b4203-125">An array of **SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION** structures, one for each processor installed in the system.</span></span>

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span data-ttu-id="b4203-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span><span class="sxs-lookup"><span data-stu-id="b4203-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-127">Struttura di **\_ \_ informazioni di interrupt del sistema** opaco che può essere utilizzata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali.</span><span class="sxs-lookup"><span data-stu-id="b4203-127">An opaque **SYSTEM\_INTERRUPT\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="b4203-128">Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="b4203-128">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span data-ttu-id="b4203-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="b4203-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-130">Struttura di **\_ \_ informazioni sulle eccezioni di sistema** opaca che può essere utilizzata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali.</span><span class="sxs-lookup"><span data-stu-id="b4203-130">An opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="b4203-131">Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="b4203-131">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span data-ttu-id="b4203-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span><span class="sxs-lookup"><span data-stu-id="b4203-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-133">Struttura **\_ \_ \_ delle informazioni sulle quote del registro di sistema** .</span><span class="sxs-lookup"><span data-stu-id="b4203-133">A **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure.</span></span>

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span data-ttu-id="b4203-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span><span class="sxs-lookup"><span data-stu-id="b4203-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-135">Struttura di **\_ \_ informazioni LOOKASIDE di sistema** opaca che può essere usata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali.</span><span class="sxs-lookup"><span data-stu-id="b4203-135">An opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="b4203-136">Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="b4203-136">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b4203-137">*Proprietà SystemInformation* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b4203-137">*SystemInformation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4203-138">Puntatore a un buffer che riceve le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="b4203-138">A pointer to a buffer that receives the requested information.</span></span> <span data-ttu-id="b4203-139">Le dimensioni e la struttura di queste informazioni variano a seconda del valore del parametro *SystemInformationClass* , come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b4203-139">The size and structure of this information varies depending on the value of the *SystemInformationClass* parameter, as indicated in the following table.</span></span>

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span data-ttu-id="b4203-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_informazioni di base \_ sul sistema**</span><span class="sxs-lookup"><span data-stu-id="b4203-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**SYSTEM\_BASIC\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-141">Quando il parametro *SystemInformationClass* è **SystemBasicInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una singola struttura di **\_ \_ informazioni di base del sistema** con il layout seguente:</span><span class="sxs-lookup"><span data-stu-id="b4203-141">When the *SystemInformationClass* parameter is **SystemBasicInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

<span data-ttu-id="b4203-142">Il membro **NumberOfProcessors** contiene il numero di processori presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b4203-142">The **NumberOfProcessors** member contains the number of processors present in the system.</span></span> <span data-ttu-id="b4203-143">Usare invece [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) per recuperare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="b4203-143">Use [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) instead to retrieve this information.</span></span>

<span data-ttu-id="b4203-144">Gli altri membri della struttura sono riservati per uso interno da parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4203-144">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span data-ttu-id="b4203-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**\_informazioni sulle prestazioni del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="b4203-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**SYSTEM\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-146">Quando il parametro *SystemInformationClass* è **SystemPerformanceInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una struttura di **\_ \_ informazioni sulle prestazioni del sistema** opaco da usare per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali.</span><span class="sxs-lookup"><span data-stu-id="b4203-146">When the *SystemInformationClass* parameter is **SystemPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="b4203-147">A questo scopo, la struttura presenta il layout seguente:</span><span class="sxs-lookup"><span data-stu-id="b4203-147">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="b4203-148">I singoli membri della struttura sono riservati per uso interno da parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4203-148">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="b4203-149">Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) per generare dati casuali crittograficamente.</span><span class="sxs-lookup"><span data-stu-id="b4203-149">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span data-ttu-id="b4203-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_informazioni sul TimeOfDay di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="b4203-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**SYSTEM\_TIMEOFDAY\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-151">Quando il parametro *SystemInformationClass* è **SystemTimeOfDayInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una struttura **di \_ \_ informazioni TimeOfDay di sistema** opaca da utilizzare per la generazione di un valore di inizializzazione imprevedibile per un generatore di numeri casuali.</span><span class="sxs-lookup"><span data-stu-id="b4203-151">When the *SystemInformationClass* parameter is **SystemTimeOfDayInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="b4203-152">A questo scopo, la struttura presenta il layout seguente:</span><span class="sxs-lookup"><span data-stu-id="b4203-152">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

<span data-ttu-id="b4203-153">I singoli membri della struttura sono riservati per uso interno da parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4203-153">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="b4203-154">Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) per generare dati casuali crittograficamente.</span><span class="sxs-lookup"><span data-stu-id="b4203-154">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span data-ttu-id="b4203-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**\_informazioni sul processo di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="b4203-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**SYSTEM\_PROCESS\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-156">Quando il parametro *SystemInformationClass* è **SystemProcessInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una matrice che contiene tutte le strutture di **\_ \_ informazioni del processo di sistema** quanti sono i processi in esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b4203-156">When the *SystemInformationClass* parameter is **SystemProcessInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processes running in the system.</span></span> <span data-ttu-id="b4203-157">Ogni struttura presenta il layout seguente:</span><span class="sxs-lookup"><span data-stu-id="b4203-157">Each structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PROCESS_INFORMATION {
    ULONG NextEntryOffset;
    ULONG NumberOfThreads;
    BYTE Reserved1[48];
    PVOID Reserved2[3];
    HANDLE UniqueProcessId;
    PVOID Reserved3;
    ULONG HandleCount;
    BYTE Reserved4[4];
    PVOID Reserved5[11];
    SIZE_T PeakPagefileUsage;
    SIZE_T PrivatePageCount;
    LARGE_INTEGER Reserved6[6];
} SYSTEM_PROCESS_INFORMATION;
```

<span data-ttu-id="b4203-158">Il membro **NumberOfThreads** contiene il numero totale di thread attualmente in esecuzione nel processo.</span><span class="sxs-lookup"><span data-stu-id="b4203-158">The **NumberOfThreads** member contains the total number of currently running threads in the process.</span></span>

<span data-ttu-id="b4203-159">Il membro **HandleCount** contiene il numero totale di handle utilizzati dal processo in questione. usare [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) per recuperare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="b4203-159">The **HandleCount** member contains the total number of handles being used by the process in question; use [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) to retrieve this information instead.</span></span>

<span data-ttu-id="b4203-160">Il membro **PeakPagefileUsage** contiene il numero massimo di byte di archiviazione di file di paging utilizzato dal processo e il membro **PrivatePageCount** contiene il numero di pagine di memoria allocate per l'utilizzo di questo processo.</span><span class="sxs-lookup"><span data-stu-id="b4203-160">The **PeakPagefileUsage** member contains the maximum number of bytes of page-file storage used by the process, and the **PrivatePageCount** member contains the number of memory pages allocated for the use of this process.</span></span>

<span data-ttu-id="b4203-161">È anche possibile recuperare queste informazioni usando la funzione [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) o la classe [**del \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="b4203-161">You can also retrieve this information using either the [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) function or the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span>

<span data-ttu-id="b4203-162">Gli altri membri della struttura sono riservati per uso interno da parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4203-162">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span data-ttu-id="b4203-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**\_ \_ informazioni sulle prestazioni del processore di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="b4203-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-164">Quando il parametro *SystemInformationClass* è **SystemProcessorPerformanceInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una matrice che contiene tutte le strutture di **\_ \_ informazioni del processo di sistema** in cui sono installati i processori (CPU) nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b4203-164">When the *SystemInformationClass* parameter is **SystemProcessorPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processors (CPUs) installed in the system.</span></span> <span data-ttu-id="b4203-165">Ogni struttura presenta il layout seguente:</span><span class="sxs-lookup"><span data-stu-id="b4203-165">Each structure has the following layout:</span></span>

``` syntax
typedef struct
_SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION {
    LARGE_INTEGER IdleTime;
    LARGE_INTEGER KernelTime;
    LARGE_INTEGER UserTime;
    LARGE_INTEGER Reserved1[2];
    ULONG Reserved2;
} SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="b4203-166">Il membro **tempoinattività** contiene la quantità di tempo in cui il sistema è rimasto inattivo, in 1/100 di un nanosecondo.</span><span class="sxs-lookup"><span data-stu-id="b4203-166">The **IdleTime** member contains the amount of time that the system has been idle, in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="b4203-167">Il membro **KernelTime** contiene la quantità di tempo impiegato dal sistema per l'esecuzione in modalità kernel, inclusi tutti i thread in tutti i processi, in tutti i processori, in 1/100 di un nanosecondo.</span><span class="sxs-lookup"><span data-stu-id="b4203-167">The **KernelTime** member contains the amount of time that the system has spent executing in Kernel mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="b4203-168">Il membro **UserTime** contiene la quantità di tempo impiegato dal sistema in modalità utente (inclusi tutti i thread in tutti i processi, su tutti i processori), in 1/100 di un nanosecondo.</span><span class="sxs-lookup"><span data-stu-id="b4203-168">The **UserTime** member contains the amount of time that the system has spent executing in User mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="b4203-169">Usare invece [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) per recuperare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="b4203-169">Use [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) instead to retrieve this information.</span></span>

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span data-ttu-id="b4203-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_informazioni di interrupt di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="b4203-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**SYSTEM\_INTERRUPT\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-171">Quando il parametro *SystemInformationClass* è **SystemInterruptInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una matrice che contiene il numero di strutture di **\_ \_ informazioni di interrupt del sistema** opaco in quanto sono presenti processori (CPU) installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b4203-171">When the *SystemInformationClass* parameter is **SystemInterruptInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many opaque **SYSTEM\_INTERRUPT\_INFORMATION** structures as there are processors (CPUs) installed on the system.</span></span> <span data-ttu-id="b4203-172">Ogni struttura o la matrice nel suo complesso può essere usata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali.</span><span class="sxs-lookup"><span data-stu-id="b4203-172">Each structure, or the array as a whole, can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="b4203-173">A questo scopo, la struttura presenta il layout seguente:</span><span class="sxs-lookup"><span data-stu-id="b4203-173">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

<span data-ttu-id="b4203-174">I singoli membri della struttura sono riservati per uso interno da parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4203-174">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="b4203-175">Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) per generare dati casuali crittograficamente.</span><span class="sxs-lookup"><span data-stu-id="b4203-175">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span data-ttu-id="b4203-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**\_informazioni sulle eccezioni di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="b4203-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**SYSTEM\_EXCEPTION\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-177">Quando il parametro *SystemInformationClass* è **SystemExceptionInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una struttura **di \_ \_ informazioni sulle eccezioni di sistema** opaca da utilizzare per la generazione di un valore di inizializzazione imprevedibile per un generatore di numeri casuali.</span><span class="sxs-lookup"><span data-stu-id="b4203-177">When the *SystemInformationClass* parameter is **SystemExceptionInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="b4203-178">A questo scopo, la struttura presenta il layout seguente:</span><span class="sxs-lookup"><span data-stu-id="b4203-178">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

<span data-ttu-id="b4203-179">I singoli membri della struttura sono riservati per uso interno da parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4203-179">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="b4203-180">Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) per generare dati casuali crittograficamente.</span><span class="sxs-lookup"><span data-stu-id="b4203-180">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span data-ttu-id="b4203-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**\_ \_ informazioni quota registro di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="b4203-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**SYSTEM\_REGISTRY\_QUOTA\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-182">Quando il parametro *SystemInformationClass* è **SystemRegistryQuotaInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una singola struttura di **\_ \_ \_ informazioni sulle quote del registro di sistema** con il seguente layout:</span><span class="sxs-lookup"><span data-stu-id="b4203-182">When the *SystemInformationClass* parameter is **SystemRegistryQuotaInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

<span data-ttu-id="b4203-183">Il membro **RegistryQuotaAllowed** contiene le dimensioni massime, in byte, che il registro di sistema può raggiungere nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b4203-183">The **RegistryQuotaAllowed** member contains the maximum size, in bytes, that the Registry can attain on this system.</span></span>

<span data-ttu-id="b4203-184">Il membro **RegistryQuotaUsed** contiene le dimensioni correnti, in byte, del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b4203-184">The **RegistryQuotaUsed** member contains the current size of the Registry, in bytes.</span></span>

<span data-ttu-id="b4203-185">Usare invece [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) per recuperare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="b4203-185">Use [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) instead to retrieve this information.</span></span>

<span data-ttu-id="b4203-186">L'altro membro della struttura è riservato per uso interno da parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4203-186">The other member of the structure is reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span data-ttu-id="b4203-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**\_informazioni sul LOOKASIDE di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="b4203-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**SYSTEM\_LOOKASIDE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="b4203-188">Quando il parametro *SystemInformationClass* è **SystemLookasideInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una struttura **di \_ \_ informazioni LOOKASIDE di sistema** opaca da utilizzare per la generazione di un valore di inizializzazione imprevedibile per un generatore di numeri casuali.</span><span class="sxs-lookup"><span data-stu-id="b4203-188">When the *SystemInformationClass* parameter is **SystemLookasideInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="b4203-189">A questo scopo, la struttura presenta il layout seguente:</span><span class="sxs-lookup"><span data-stu-id="b4203-189">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

<span data-ttu-id="b4203-190">I singoli membri della struttura sono riservati per uso interno da parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4203-190">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="b4203-191">Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) per generare dati casuali crittograficamente.</span><span class="sxs-lookup"><span data-stu-id="b4203-191">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b4203-192">*SystemInformationLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4203-192">*SystemInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4203-193">Dimensioni in byte del buffer a cui punta il parametro *SystemInformation* .</span><span class="sxs-lookup"><span data-stu-id="b4203-193">The size of the buffer pointed to by the *SystemInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b4203-194">*ReturnLength* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b4203-194">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4203-195">Puntatore facoltativo a una posizione in cui la funzione scrive le dimensioni effettive delle informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="b4203-195">An optional pointer to a location where the function writes the actual size of the information requested.</span></span> <span data-ttu-id="b4203-196">Se tali dimensioni sono minori o uguali al parametro *SystemInformationLength* , la funzione copia le informazioni nel buffer *SystemInformation* ; in caso contrario, restituisce un codice di errore NTSTATUS e restituisce in *ReturnLength* la dimensione del buffer necessaria per ricevere le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="b4203-196">If that size is less than or equal to the *SystemInformationLength* parameter, the function copies the information into the *SystemInformation* buffer; otherwise, it returns an NTSTATUS error code and returns in *ReturnLength* the size of buffer required to receive the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4203-197">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4203-197">Return value</span></span>

<span data-ttu-id="b4203-198">Restituisce un codice di errore o di esito positivo NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="b4203-198">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="b4203-199">I moduli e il significato dei codici di errore NTSTATUS sono elencati nel file di intestazione Ntstatus. h disponibile in DDK e sono descritti nella documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="b4203-199">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4203-200">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4203-200">Remarks</span></span>

<span data-ttu-id="b4203-201">La funzione **ZwQuerySystemInformation** e le strutture restituite sono interne al sistema operativo e sono soggette a modifiche da una versione di Windows a un'altra.</span><span class="sxs-lookup"><span data-stu-id="b4203-201">The **ZwQuerySystemInformation** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="b4203-202">Per mantenere la compatibilità dell'applicazione, è preferibile usare invece le funzioni alternative citate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b4203-202">To maintain the compatibility of your application, it is better to use the alternate functions previously mentioned instead.</span></span>

<span data-ttu-id="b4203-203">Se si utilizza **ZwQuerySystemInformation**, accedere alla funzione tramite il [collegamento dinamico in fase di esecuzione](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span><span class="sxs-lookup"><span data-stu-id="b4203-203">If you do use **ZwQuerySystemInformation**, access the function through [run-time dynamic linking](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span></span> <span data-ttu-id="b4203-204">In questo modo il codice può rispondere normalmente se la funzione è stata modificata o rimossa dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4203-204">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="b4203-205">Le modifiche alla firma, tuttavia, potrebbero non essere rilevabili.</span><span class="sxs-lookup"><span data-stu-id="b4203-205">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="b4203-206">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="b4203-206">This function has no associated import library.</span></span> <span data-ttu-id="b4203-207">È necessario utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="b4203-207">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4203-208">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4203-208">Requirements</span></span>



| <span data-ttu-id="b4203-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4203-209">Requirement</span></span> | <span data-ttu-id="b4203-210">Valore</span><span class="sxs-lookup"><span data-stu-id="b4203-210">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b4203-211">DLL</span><span class="sxs-lookup"><span data-stu-id="b4203-211">DLL</span></span><br/> | <dl> <span data-ttu-id="b4203-212"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4203-212"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4203-213">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4203-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4203-214">**GetSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="b4203-214">**GetSystemInfo**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[<span data-ttu-id="b4203-215">**GetProcessHandleCount**</span><span class="sxs-lookup"><span data-stu-id="b4203-215">**GetProcessHandleCount**</span></span>](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[<span data-ttu-id="b4203-216">**GetProcessMemoryInfo**</span><span class="sxs-lookup"><span data-stu-id="b4203-216">**GetProcessMemoryInfo**</span></span>](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[<span data-ttu-id="b4203-217">**GetSystemTimes**</span><span class="sxs-lookup"><span data-stu-id="b4203-217">**GetSystemTimes**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[<span data-ttu-id="b4203-218">**GetSystemRegistryQuota**</span><span class="sxs-lookup"><span data-stu-id="b4203-218">**GetSystemRegistryQuota**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

