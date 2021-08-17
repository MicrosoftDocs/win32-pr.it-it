---
description: Recupera informazioni sul processo specificato.
ms.assetid: c36c023f-7f9a-4ba5-a41f-f2f755a24eb6
title: Funzione ZwQueryInformationProcess
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
ms.openlocfilehash: 7972d3d2e6b98f56829680dd77c4c0a97b51679ffb2d9cfef928d4a279f6b7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792915"
---
# <a name="zwqueryinformationprocess-function"></a>Funzione ZwQueryInformationProcess

\[**ZwQueryInformationProcess** potrebbe essere modificato o non disponibile nelle versioni future Windows. Le applicazioni devono usare le funzioni alternative elencate in questo argomento.\]

Recupera informazioni sul processo specificato.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProcessHandle* \[ Pollici\]
</dt> <dd>

Handle per il processo per il quale devono essere recuperate le informazioni.

</dd> <dt>

*Classe ProcessInformationClass* \[ Pollici\]
</dt> <dd>

Tipo di informazioni sul processo da recuperare. Questo parametro può essere uno dei valori seguenti **dell'enumerazione PROCESSINFOCLASS.**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </dl></td>
<td>Recupera un puntatore a una struttura PEB che può essere utilizzato per determinare se è in corso il debug del processo specificato e un valore univoco utilizzato dal sistema per identificare il processo specificato. <br/> È meglio usare le funzioni <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> e <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> per ottenere queste informazioni.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </dl></td>
<td>Recupera un <strong>DWORD_PTR</strong> valore che rappresenta il numero di porta del debugger per il processo. Un valore diverso da zero indica che il processo viene eseguito sotto il controllo di un debugger ring 3.<br/> È meglio usare la <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>funzione CheckRemoteDebuggerPresent</strong></a> <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>o IsDebuggerPresent.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </dl></td>
<td>Determina se il processo è in esecuzione nell'ambiente WOW64 (WOW64 è l'emulatore x86 che consente l'esecuzione di applicazioni basate su Win32 in un Windows a 64 bit).<br/> È meglio usare la <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>funzione IsWow64Process</strong></a> per ottenere queste informazioni.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </dl></td>
<td>Recupera un valore <strong>UNICODE_STRING</strong> contenente il nome del file di immagine per il processo.<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </dl></td>
<td>Recupera un valore <strong>ULONG</strong> che indica se il processo è considerato critico.<br/>
<blockquote>
[!Note]<br />
Questo valore può essere usato a partire da Windows XP con SP3. A partire Windows 8.1, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>è invece consigliabile usare IsProcessCritical.</strong></a>
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </dl></td>
<td>Recupera un valore BYTE che indica il tipo di processo protetto e il firmatario del processo protetto.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*Informazioni sul processo* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer fornito dall'applicazione chiamante in cui la funzione scrive le informazioni richieste. Le dimensioni delle informazioni scritte variano a seconda del valore del *parametro ProcessInformationClass:*

<dl> <dt>

<span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>ELABORARE \_ LE INFORMAZIONI DI \_ BASE
</dt> <dd>

Quando il *parametro ProcessInformationClass* è **ProcessBasicInformation,** il buffer a cui punta il *parametro ProcessInformation* deve essere sufficientemente grande da contenere una singola struttura **PROCESS BASIC \_ \_ INFORMATION** con il layout seguente:

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

Il **membro UniqueProcessId** punta all'identificatore univoco del sistema per questo processo. È meglio usare la [**funzione GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) per recuperare queste informazioni.

Il **membro PebBaseAddress** punta a una [**struttura PEB.**](/windows/desktop/api/Winternl/ns-winternl-peb)

Gli altri membri di questa struttura sono riservati per l'uso interno da parte del sistema operativo.

</dd> <dt>

<span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG \_ PTR
</dt> <dd>

Quando il *parametro ProcessInformationClass* è **ProcessWow64Information,** il buffer a cui punta il parametro *ProcessInformation* deve essere sufficientemente grande da contenere un **\_ PTR ULONG.** Se questo valore è diverso da zero, il processo viene eseguito in un ambiente WOW64. In caso contrario, se il valore è uguale a zero, il processo non è in esecuzione in un ambiente WOW64.

È meglio usare la funzione [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) per determinare se un processo è in esecuzione nell'ambiente WOW64.

</dd> <dt>

<span id="UNICODE_STRING"></span><span id="unicode_string"></span>STRINGA \_ UNICODE
</dt> <dd>

Quando il *parametro ProcessInformationClass* è **ProcessImageFileName,** il buffer a cui punta il parametro *ProcessInformation* deve essere sufficientemente grande da contenere una struttura **\_ STRING UNICODE** e la stringa stessa. La stringa archiviata nel **membro Buffer** è il nome del file di immagine.

Se il buffer è troppo piccolo, la funzione ha esito negativo con il codice di errore STATUS \_ INFO \_ LENGTH MISMATCH e il parametro ReturnLength è impostato \_ sulle dimensioni del buffer richieste. 

</dd> <dt>

<span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION
</dt> <dd>

Quando il *parametro ProcessInformationClass* è **ProcessProtectionInformation,** il buffer a cui punta il parametro *ProcessInformation* deve essere sufficientemente grande da contenere una singola struttura **PS_PROTECTION** con il layout seguente:

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

I primi 3 bit contengono il tipo di processo protetto:

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

I primi 4 bit contengono il firmatario del processo protetto:

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

*ProcessInformationLength* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer a cui punta il *parametro ProcessInformation,* in byte.

</dd> <dt>

*ReturnLength* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile in cui la funzione restituisce le dimensioni delle informazioni richieste. Se la funzione ha esito positivo, si tratta della dimensione delle informazioni scritte nel buffer a cui punta il parametro *ProcessInformation,* ma se il buffer è troppo piccolo, si tratta della dimensione minima del buffer necessaria per ricevere correttamente le informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un codice di errore o di esito positivo NTSTATUS.

I formati e il significato dei codici di errore NTSTATUS sono elencati nel file di intestazione Ntstatus.h disponibile nel DDK e sono descritti nella documentazione di DDK in architettura del driver Kernel-Mode/Guida alla progettazione/Tecniche di programmazione del driver/Errori di registrazione.

## <a name="remarks"></a>Commenti

La **funzione ZwQueryInformationProcess** e le strutture restituite sono interne al sistema operativo e soggette a modifiche da una versione di Windows a un'altra. Per mantenere la compatibilità dell'applicazione, è meglio usare le funzioni pubbliche citate nella descrizione del *parametro ProcessInformationClass.*

Se si usa **ZwQueryInformationProcess,** accedere alla funzione tramite il [collegamento dinamico in fase di esecuzione.](../dlls/using-run-time-dynamic-linking.md) In questo modo il codice può rispondere normalmente se la funzione è stata modificata o rimossa dal sistema operativo. Le modifiche della firma, tuttavia, potrebbero non essere rilevabili.

A questa funzione non è associata alcuna libreria di importazione. È necessario usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
