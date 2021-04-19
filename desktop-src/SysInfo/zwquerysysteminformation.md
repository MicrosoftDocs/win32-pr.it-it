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
# <a name="zwquerysysteminformation-function"></a>ZwQuerySystemInformation (funzione)

\[**ZwQuerySystemInformation** non è più disponibile per l'uso a partire da Windows 8. Usare invece le funzioni alternative elencate in questo argomento.\]

Recupera le informazioni di sistema specificate.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SystemInformationClass* \[ in\]
</dt> <dd>

Tipo di informazioni di sistema da recuperare. Questo parametro può essere uno dei valori seguenti del tipo di **enumerazione \_ \_ classe informazioni di sistema** .

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**


</dt> <dd>

Il numero di processori nel sistema in una struttura **di \_ \_ informazioni di base del sistema** . Usare invece la funzione [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**


</dt> <dd>

Struttura di **\_ \_ informazioni sulle prestazioni di sistema** opaca che può essere utilizzata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali. Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**


</dt> <dd>

Struttura di **\_ \_ informazioni TimeOfDay di sistema** opaca che può essere usata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali. Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**


</dt> <dd>

Matrice di strutture **di \_ \_ informazioni del processo di sistema** , una per ogni processo in esecuzione nel sistema.

Queste strutture contengono informazioni sull'utilizzo delle risorse di ogni processo, tra cui il numero di handle utilizzati dal processo, il picco di utilizzo del file di paging e il numero di pagine di memoria allocate dal processo.

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**


</dt> <dd>

Una matrice di strutture di **\_ \_ \_ informazioni sulle prestazioni del processore di sistema** , una per ogni processore installato nel sistema.

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**


</dt> <dd>

Struttura di **\_ \_ informazioni di interrupt del sistema** opaco che può essere utilizzata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali. Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**


</dt> <dd>

Struttura di **\_ \_ informazioni sulle eccezioni di sistema** opaca che può essere utilizzata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali. Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**


</dt> <dd>

Struttura **\_ \_ \_ delle informazioni sulle quote del registro di sistema** .

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**


</dt> <dd>

Struttura di **\_ \_ informazioni LOOKASIDE di sistema** opaca che può essere usata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali. Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> </dl> </dd> <dt>

*Proprietà SystemInformation* \[ in uscita\]
</dt> <dd>

Puntatore a un buffer che riceve le informazioni richieste. Le dimensioni e la struttura di queste informazioni variano a seconda del valore del parametro *SystemInformationClass* , come indicato nella tabella seguente.

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_informazioni di base \_ sul sistema**


</dt> <dd>

Quando il parametro *SystemInformationClass* è **SystemBasicInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una singola struttura di **\_ \_ informazioni di base del sistema** con il layout seguente:

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

Il membro **NumberOfProcessors** contiene il numero di processori presenti nel sistema. Usare invece [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) per recuperare queste informazioni.

Gli altri membri della struttura sono riservati per uso interno da parte del sistema operativo.

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**\_informazioni sulle prestazioni del sistema \_**


</dt> <dd>

Quando il parametro *SystemInformationClass* è **SystemPerformanceInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una struttura di **\_ \_ informazioni sulle prestazioni del sistema** opaco da usare per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali. A questo scopo, la struttura presenta il layout seguente:

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

I singoli membri della struttura sono riservati per uso interno da parte del sistema operativo.

Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) per generare dati casuali crittograficamente.

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_informazioni sul TimeOfDay di sistema \_**


</dt> <dd>

Quando il parametro *SystemInformationClass* è **SystemTimeOfDayInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una struttura **di \_ \_ informazioni TimeOfDay di sistema** opaca da utilizzare per la generazione di un valore di inizializzazione imprevedibile per un generatore di numeri casuali. A questo scopo, la struttura presenta il layout seguente:

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

I singoli membri della struttura sono riservati per uso interno da parte del sistema operativo.

Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) per generare dati casuali crittograficamente.

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**\_informazioni sul processo di sistema \_**


</dt> <dd>

Quando il parametro *SystemInformationClass* è **SystemProcessInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una matrice che contiene tutte le strutture di **\_ \_ informazioni del processo di sistema** quanti sono i processi in esecuzione nel sistema. Ogni struttura presenta il layout seguente:

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

Il membro **NumberOfThreads** contiene il numero totale di thread attualmente in esecuzione nel processo.

Il membro **HandleCount** contiene il numero totale di handle utilizzati dal processo in questione. usare [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) per recuperare queste informazioni.

Il membro **PeakPagefileUsage** contiene il numero massimo di byte di archiviazione di file di paging utilizzato dal processo e il membro **PrivatePageCount** contiene il numero di pagine di memoria allocate per l'utilizzo di questo processo.

È anche possibile recuperare queste informazioni usando la funzione [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) o la classe [**del \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) .

Gli altri membri della struttura sono riservati per uso interno da parte del sistema operativo.

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**\_ \_ informazioni sulle prestazioni del processore di sistema \_**


</dt> <dd>

Quando il parametro *SystemInformationClass* è **SystemProcessorPerformanceInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una matrice che contiene tutte le strutture di **\_ \_ informazioni del processo di sistema** in cui sono installati i processori (CPU) nel sistema. Ogni struttura presenta il layout seguente:

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

Il membro **tempoinattività** contiene la quantità di tempo in cui il sistema è rimasto inattivo, in 1/100 di un nanosecondo.

Il membro **KernelTime** contiene la quantità di tempo impiegato dal sistema per l'esecuzione in modalità kernel, inclusi tutti i thread in tutti i processi, in tutti i processori, in 1/100 di un nanosecondo.

Il membro **UserTime** contiene la quantità di tempo impiegato dal sistema in modalità utente (inclusi tutti i thread in tutti i processi, su tutti i processori), in 1/100 di un nanosecondo.

Usare invece [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) per recuperare queste informazioni.

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_informazioni di interrupt di sistema \_**


</dt> <dd>

Quando il parametro *SystemInformationClass* è **SystemInterruptInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una matrice che contiene il numero di strutture di **\_ \_ informazioni di interrupt del sistema** opaco in quanto sono presenti processori (CPU) installati nel sistema. Ogni struttura o la matrice nel suo complesso può essere usata per generare un valore di inizializzazione imprevedibile per un generatore di numeri casuali. A questo scopo, la struttura presenta il layout seguente:

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

I singoli membri della struttura sono riservati per uso interno da parte del sistema operativo.

Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) per generare dati casuali crittograficamente.

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**\_informazioni sulle eccezioni di sistema \_**


</dt> <dd>

Quando il parametro *SystemInformationClass* è **SystemExceptionInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una struttura **di \_ \_ informazioni sulle eccezioni di sistema** opaca da utilizzare per la generazione di un valore di inizializzazione imprevedibile per un generatore di numeri casuali. A questo scopo, la struttura presenta il layout seguente:

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

I singoli membri della struttura sono riservati per uso interno da parte del sistema operativo.

Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) per generare dati casuali crittograficamente.

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**\_ \_ informazioni quota registro di sistema \_**


</dt> <dd>

Quando il parametro *SystemInformationClass* è **SystemRegistryQuotaInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una singola struttura di **\_ \_ \_ informazioni sulle quote del registro di sistema** con il seguente layout:

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

Il membro **RegistryQuotaAllowed** contiene le dimensioni massime, in byte, che il registro di sistema può raggiungere nel sistema.

Il membro **RegistryQuotaUsed** contiene le dimensioni correnti, in byte, del registro di sistema.

Usare invece [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) per recuperare queste informazioni.

L'altro membro della struttura è riservato per uso interno da parte del sistema operativo.

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**\_informazioni sul LOOKASIDE di sistema \_**


</dt> <dd>

Quando il parametro *SystemInformationClass* è **SystemLookasideInformation**, il buffer a cui punta il parametro *SystemInformation* deve essere sufficientemente grande da contenere una struttura **di \_ \_ informazioni LOOKASIDE di sistema** opaca da utilizzare per la generazione di un valore di inizializzazione imprevedibile per un generatore di numeri casuali. A questo scopo, la struttura presenta il layout seguente:

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

I singoli membri della struttura sono riservati per uso interno da parte del sistema operativo.

Usare invece la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) per generare dati casuali crittograficamente.

</dd> </dl> </dd> <dt>

*SystemInformationLength* \[ in\]
</dt> <dd>

Dimensioni in byte del buffer a cui punta il parametro *SystemInformation* .

</dd> <dt>

*ReturnLength* \[ out, facoltativo\]
</dt> <dd>

Puntatore facoltativo a una posizione in cui la funzione scrive le dimensioni effettive delle informazioni richieste. Se tali dimensioni sono minori o uguali al parametro *SystemInformationLength* , la funzione copia le informazioni nel buffer *SystemInformation* ; in caso contrario, restituisce un codice di errore NTSTATUS e restituisce in *ReturnLength* la dimensione del buffer necessaria per ricevere le informazioni richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un codice di errore o di esito positivo NTSTATUS.

I moduli e il significato dei codici di errore NTSTATUS sono elencati nel file di intestazione Ntstatus. h disponibile in DDK e sono descritti nella documentazione di DDK.

## <a name="remarks"></a>Commenti

La funzione **ZwQuerySystemInformation** e le strutture restituite sono interne al sistema operativo e sono soggette a modifiche da una versione di Windows a un'altra. Per mantenere la compatibilità dell'applicazione, è preferibile usare invece le funzioni alternative citate in precedenza.

Se si utilizza **ZwQuerySystemInformation**, accedere alla funzione tramite il [collegamento dinamico in fase di esecuzione](/windows/desktop/Dlls/using-run-time-dynamic-linking). In questo modo il codice può rispondere normalmente se la funzione è stata modificata o rimossa dal sistema operativo. Le modifiche alla firma, tuttavia, potrebbero non essere rilevabili.

A questa funzione non è associata alcuna libreria di importazione. È necessario utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

