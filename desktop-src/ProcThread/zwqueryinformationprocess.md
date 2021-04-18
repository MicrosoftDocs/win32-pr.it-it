---
description: Recupera le informazioni sul processo specificato.
ms.assetid: c36c023f-7f9a-4ba5-a41f-f2f755a24eb6
title: ZwQueryInformationProcess (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQueryInformationProcess
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 30207c8d3d54c54f77194b542e10e9fee94e055a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311944"
---
# <a name="zwqueryinformationprocess-function"></a><span data-ttu-id="e8389-103">ZwQueryInformationProcess (funzione)</span><span class="sxs-lookup"><span data-stu-id="e8389-103">ZwQueryInformationProcess function</span></span>

<span data-ttu-id="e8389-104">\[**ZwQueryInformationProcess** può essere modificato o non disponibile nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="e8389-104">\[**ZwQueryInformationProcess** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="e8389-105">Le applicazioni devono utilizzare le funzioni alternative elencate in questo argomento.\]</span><span class="sxs-lookup"><span data-stu-id="e8389-105">Applications should use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="e8389-106">Recupera le informazioni sul processo specificato.</span><span class="sxs-lookup"><span data-stu-id="e8389-106">Retrieves information about the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8389-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8389-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="e8389-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8389-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8389-109">*ProcessHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8389-109">*ProcessHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8389-110">Handle per il processo per il quale devono essere recuperate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="e8389-110">A handle to the process for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="e8389-111">*ProcessInformationClass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8389-111">*ProcessInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8389-112">Tipo di informazioni del processo da recuperare.</span><span class="sxs-lookup"><span data-stu-id="e8389-112">The type of process information to be retrieved.</span></span> <span data-ttu-id="e8389-113">Questo parametro può essere uno dei valori seguenti dell'enumerazione **PROCESSINFOCLASS** .</span><span class="sxs-lookup"><span data-stu-id="e8389-113">This parameter can be one of the following values from the **PROCESSINFOCLASS** enumeration.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8389-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e8389-114">Value</span></span></th>
<th><span data-ttu-id="e8389-115">Significato</span><span class="sxs-lookup"><span data-stu-id="e8389-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <span data-ttu-id="e8389-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="e8389-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="e8389-117">Recupera un puntatore a una struttura PEB che può essere utilizzata per determinare se è in corso il debug del processo specificato e un valore univoco utilizzato dal sistema per identificare il processo specificato.</span><span class="sxs-lookup"><span data-stu-id="e8389-117">Retrieves a pointer to a PEB structure that can be used to determine whether the specified process is being debugged, and a unique value used by the system to identify the specified process.</span></span> <br/> <span data-ttu-id="e8389-118">Per ottenere queste informazioni, è preferibile usare le funzioni <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> e <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e8389-118">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> functions to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <span data-ttu-id="e8389-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="e8389-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="e8389-120">Recupera un valore <strong>DWORD_PTR</strong> che rappresenta il numero di porta del debugger per il processo.</span><span class="sxs-lookup"><span data-stu-id="e8389-120">Retrieves a <strong>DWORD_PTR</strong> value that is the port number of the debugger for the process.</span></span> <span data-ttu-id="e8389-121">Un valore diverso da zero indica che il processo viene eseguito sotto il controllo di un debugger Ring 3.</span><span class="sxs-lookup"><span data-stu-id="e8389-121">A nonzero value indicates that the process is being run under the control of a ring 3 debugger.</span></span><br/> <span data-ttu-id="e8389-122">È preferibile usare la funzione <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> o <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e8389-122">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> or <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <span data-ttu-id="e8389-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span><span class="sxs-lookup"><span data-stu-id="e8389-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span></span></dl></td>
<td><span data-ttu-id="e8389-124">Determina se il processo è in esecuzione nell'ambiente WOW64 (WOW64 è l'emulatore x86 che consente l'esecuzione delle applicazioni basate su Win32 in Windows a 64 bit).</span><span class="sxs-lookup"><span data-stu-id="e8389-124">Determines whether the process is running in the WOW64 environment (WOW64 is the x86 emulator that allows Win32-based applications to run on 64-bit Windows).</span></span><br/> <span data-ttu-id="e8389-125">Per ottenere queste informazioni, è preferibile usare la funzione <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e8389-125">It is best to use the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> function to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <span data-ttu-id="e8389-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span><span class="sxs-lookup"><span data-stu-id="e8389-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span></span></dl></td>
<td><span data-ttu-id="e8389-127">Recupera un valore <strong>UNICODE_STRING</strong> contenente il nome del file di immagine per il processo.</span><span class="sxs-lookup"><span data-stu-id="e8389-127">Retrieves a <strong>UNICODE_STRING</strong> value containing the name of the image file for the process.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <span data-ttu-id="e8389-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span><span class="sxs-lookup"><span data-stu-id="e8389-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span></span></dl></td>
<td><span data-ttu-id="e8389-129">Recupera un valore <strong>ULONG</strong> che indica se il processo è considerato critico.</span><span class="sxs-lookup"><span data-stu-id="e8389-129">Retrieves a <strong>ULONG</strong> value indicating whether the process is considered critical.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e8389-130">Questo valore può essere utilizzato a partire da Windows XP con SP3.</span><span class="sxs-lookup"><span data-stu-id="e8389-130">This value can be used starting in Windows XP with SP3.</span></span> <span data-ttu-id="e8389-131">A partire da Windows 8.1, usare invece <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e8389-131">Starting in Windows 8.1, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> should be used instead.</span></span>
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <span data-ttu-id="e8389-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span><span class="sxs-lookup"><span data-stu-id="e8389-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span></span></dl></td>
<td><span data-ttu-id="e8389-133">Recupera un valore BYTE che indica il tipo di processo protetto e il firmatario del processo protetto.</span><span class="sxs-lookup"><span data-stu-id="e8389-133">Retrieves a BYTE value indicating the type of protected process and the protected process signer.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="e8389-134">*ProcessInformation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e8389-134">*ProcessInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8389-135">Puntatore a un buffer fornito dall'applicazione chiamante in cui la funzione scrive le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="e8389-135">A pointer to a buffer supplied by the calling application into which the function writes the requested information.</span></span> <span data-ttu-id="e8389-136">Le dimensioni delle informazioni scritte variano a seconda del valore del parametro *ProcessInformationClass* :</span><span class="sxs-lookup"><span data-stu-id="e8389-136">The size of the information written varies depending on the value of the *ProcessInformationClass* parameter:</span></span>

<dl> <dt>

<span data-ttu-id="e8389-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>ELABORA \_ informazioni di base \_</span><span class="sxs-lookup"><span data-stu-id="e8389-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>PROCESS\_BASIC\_INFORMATION</span></span>
</dt> <dd>

<span data-ttu-id="e8389-138">Quando il parametro *ProcessInformationClass* è **ProcessBasicInformation**, il buffer a cui punta il parametro *ProcessInformation* deve essere sufficientemente grande da contenere una singola struttura di **\_ \_ informazioni di base del processo** con il layout seguente:</span><span class="sxs-lookup"><span data-stu-id="e8389-138">When the *ProcessInformationClass* parameter is **ProcessBasicInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PROCESS\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

<span data-ttu-id="e8389-139">Il membro **UniqueProcessId** punta all'identificatore univoco del sistema per questo processo.</span><span class="sxs-lookup"><span data-stu-id="e8389-139">The **UniqueProcessId** member points to the system's unique identifier for this process.</span></span> <span data-ttu-id="e8389-140">Per recuperare queste informazioni, è preferibile usare la funzione [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) .</span><span class="sxs-lookup"><span data-stu-id="e8389-140">It is best to use the [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) function to retrieve this information.</span></span>

<span data-ttu-id="e8389-141">Il membro **PebBaseAddress** punta a una struttura [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) .</span><span class="sxs-lookup"><span data-stu-id="e8389-141">The **PebBaseAddress** member points to a [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) structure.</span></span>

<span data-ttu-id="e8389-142">Gli altri membri di questa struttura sono riservati per uso interno da parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e8389-142">The other members of this structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="e8389-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>\_ptr ULONG</span><span class="sxs-lookup"><span data-stu-id="e8389-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG\_PTR</span></span>
</dt> <dd>

<span data-ttu-id="e8389-144">Quando il parametro *ProcessInformationClass* è **ProcessWow64Information**, il buffer a cui punta il parametro *ProcessInformation* deve essere sufficientemente grande da contenere un **\_ ptr ULONG**.</span><span class="sxs-lookup"><span data-stu-id="e8389-144">When the *ProcessInformationClass* parameter is **ProcessWow64Information**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **ULONG\_PTR**.</span></span> <span data-ttu-id="e8389-145">Se questo valore è diverso da zero, il processo viene eseguito in un ambiente WOW64. in caso contrario, se il valore è uguale a zero, il processo non è in esecuzione in un ambiente WOW64.</span><span class="sxs-lookup"><span data-stu-id="e8389-145">If this value is nonzero, the process is running in a WOW64 environment; otherwise, if the value is equal to zero, the process is not running in a WOW64 environment.</span></span>

<span data-ttu-id="e8389-146">È consigliabile usare la funzione [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) per determinare se un processo è in esecuzione nell'ambiente WOW64.</span><span class="sxs-lookup"><span data-stu-id="e8389-146">It is best to use the [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) function to determine whether a process is running in the WOW64 environment.</span></span>

</dd> <dt>

<span data-ttu-id="e8389-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>\_stringa Unicode</span><span class="sxs-lookup"><span data-stu-id="e8389-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>UNICODE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="e8389-148">Quando il parametro *ProcessInformationClass* è **ProcessImageFileName**, il buffer a cui punta il parametro *ProcessInformation* deve essere sufficientemente grande da contenere una struttura di **\_ stringhe Unicode** e la stessa stringa.</span><span class="sxs-lookup"><span data-stu-id="e8389-148">When the *ProcessInformationClass* parameter is **ProcessImageFileName**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **UNICODE\_STRING** structure as well as the string itself.</span></span> <span data-ttu-id="e8389-149">La stringa archiviata nel membro **buffer** è il nome del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="e8389-149">The string stored in the **Buffer** member is the name of the image file.</span></span>

<span data-ttu-id="e8389-150">Se il buffer è troppo piccolo, la funzione ha esito negativo \_ e il codice di errore indica la mancata corrispondenza della lunghezza delle informazioni sullo stato \_ \_ e il parametro *ReturnLength* è impostato sulle dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="e8389-150">If the buffer is too small, the function fails with the STATUS\_INFO\_LENGTH\_MISMATCH error code and the *ReturnLength* parameter is set to the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="e8389-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span><span class="sxs-lookup"><span data-stu-id="e8389-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span></span>
</dt> <dd>

<span data-ttu-id="e8389-152">Quando il parametro *ProcessInformationClass* è **ProcessProtectionInformation**, il buffer a cui punta il parametro *ProcessInformation* deve essere sufficientemente grande da contenere una singola struttura di **PS_PROTECTION** con il layout seguente:</span><span class="sxs-lookup"><span data-stu-id="e8389-152">When the *ProcessInformationClass* parameter is **ProcessProtectionInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PS_PROTECTION** structure having the following layout:</span></span>

``` syntax
typedef struct _PS_PROTECTION {
    union {
        UCHAR Level;
        struct {
            UCHAR Type   : 3;
            UCHAR Audit  : 1;                  // Reserved
            UCHAR Signer : 4;
        };
    };
} PS_PROTECTION, *PPS_PROTECTION;
```

<span data-ttu-id="e8389-153">I primi 3 bit contengono il tipo di processo protetto:</span><span class="sxs-lookup"><span data-stu-id="e8389-153">The first 3 bits contain the type of protected process:</span></span>

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

<span data-ttu-id="e8389-154">I primi 4 bit contengono il firmatario del processo protetto:</span><span class="sxs-lookup"><span data-stu-id="e8389-154">The top 4 bits contain the protected process signer:</span></span>

``` syntax
typedef enum _PS_PROTECTED_SIGNER {
    PsProtectedSignerNone = 0,
    PsProtectedSignerAuthenticode,
    PsProtectedSignerCodeGen,
    PsProtectedSignerAntimalware,
    PsProtectedSignerLsa,
    PsProtectedSignerWindows,
    PsProtectedSignerWinTcb,
    PsProtectedSignerWinSystem,
    PsProtectedSignerApp,
    PsProtectedSignerMax
} PS_PROTECTED_SIGNER, *PPS_PROTECTED_SIGNER;
```

</dd> </dl> </dd> <dt>

<span data-ttu-id="e8389-155">*ProcessInformationLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8389-155">*ProcessInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8389-156">Dimensioni in byte del buffer a cui punta il parametro *ProcessInformation* .</span><span class="sxs-lookup"><span data-stu-id="e8389-156">The size of the buffer pointed to by the *ProcessInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e8389-157">*ReturnLength* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e8389-157">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e8389-158">Puntatore a una variabile in cui la funzione restituisce la dimensione delle informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="e8389-158">A pointer to a variable in which the function returns the size of the requested information.</span></span> <span data-ttu-id="e8389-159">Se la funzione ha esito positivo, si tratta della dimensione delle informazioni scritte nel buffer a cui punta il parametro *ProcessInformation* , ma se il buffer era troppo piccolo, si tratta della dimensione minima del buffer necessaria per ricevere correttamente le informazioni.</span><span class="sxs-lookup"><span data-stu-id="e8389-159">If the function was successful, this is the size of the information written to the buffer pointed to by the *ProcessInformation* parameter, but if the buffer was too small, this is the minimum size of buffer needed to receive the information successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8389-160">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8389-160">Return value</span></span>

<span data-ttu-id="e8389-161">Restituisce un codice di errore o di esito positivo NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="e8389-161">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="e8389-162">I moduli e il significato dei codici di errore di NTSTATUS sono elencati nel file di intestazione Ntstatus. h disponibile nel DDK e sono descritti nella documentazione di DDK in Kernel-Mode architettura del driver/Guida alla progettazione/Guida alla programmazione dei driver/errori di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e8389-162">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation under Kernel-Mode Driver Architecture / Design Guide / Driver Programming Techniques / Logging Errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8389-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8389-163">Remarks</span></span>

<span data-ttu-id="e8389-164">La funzione **ZwQueryInformationProcess** e le strutture restituite sono interne al sistema operativo e sono soggette a modifiche da una versione di Windows a un'altra.</span><span class="sxs-lookup"><span data-stu-id="e8389-164">The **ZwQueryInformationProcess** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="e8389-165">Per mantenere la compatibilità dell'applicazione, è preferibile usare le funzioni pubbliche indicate nella descrizione del parametro *ProcessInformationClass* .</span><span class="sxs-lookup"><span data-stu-id="e8389-165">To maintain the compatibility of your application, it is better to use public functions mentioned in the description of the *ProcessInformationClass* parameter instead.</span></span>

<span data-ttu-id="e8389-166">Se si utilizza **ZwQueryInformationProcess**, accedere alla funzione tramite il [collegamento dinamico in fase di esecuzione](../dlls/using-run-time-dynamic-linking.md).</span><span class="sxs-lookup"><span data-stu-id="e8389-166">If you do use **ZwQueryInformationProcess**, access the function through [run-time dynamic linking](../dlls/using-run-time-dynamic-linking.md).</span></span> <span data-ttu-id="e8389-167">In questo modo il codice può rispondere normalmente se la funzione è stata modificata o rimossa dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e8389-167">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="e8389-168">Le modifiche alla firma, tuttavia, potrebbero non essere rilevabili.</span><span class="sxs-lookup"><span data-stu-id="e8389-168">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="e8389-169">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="e8389-169">This function has no associated import library.</span></span> <span data-ttu-id="e8389-170">È necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="e8389-170">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8389-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8389-171">Requirements</span></span>



| <span data-ttu-id="e8389-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8389-172">Requirement</span></span> | <span data-ttu-id="e8389-173">Valore</span><span class="sxs-lookup"><span data-stu-id="e8389-173">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8389-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8389-174">Minimum supported client</span></span><br/> | <span data-ttu-id="e8389-175">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e8389-175">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e8389-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8389-176">Minimum supported server</span></span><br/> | <span data-ttu-id="e8389-177">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8389-177">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e8389-178">DLL</span><span class="sxs-lookup"><span data-stu-id="e8389-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8389-179"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8389-179"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8389-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8389-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8389-181">**CheckRemoteDebuggerPresent**</span><span class="sxs-lookup"><span data-stu-id="e8389-181">**CheckRemoteDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[<span data-ttu-id="e8389-182">**GetProcessId**</span><span class="sxs-lookup"><span data-stu-id="e8389-182">**GetProcessId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[<span data-ttu-id="e8389-183">**IsDebuggerPresent**</span><span class="sxs-lookup"><span data-stu-id="e8389-183">**IsDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[<span data-ttu-id="e8389-184">**IsWow64Process**</span><span class="sxs-lookup"><span data-stu-id="e8389-184">**IsWow64Process**</span></span>](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
