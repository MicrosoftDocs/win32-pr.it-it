---
description: Recupera le dimensioni e la posizione dell'elenco di moduli scaricati dinamicamente per il processo corrente.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: RtlGetUnloadEventTraceEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330957"
---
# <a name="rtlgetunloadeventtraceex-function"></a>RtlGetUnloadEventTraceEx (funzione)

Recupera le dimensioni e la posizione dell'elenco di moduli scaricati dinamicamente per il processo corrente.

## <a name="syntax"></a>Sintassi


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ElementSize* \[ out\]
</dt> <dd>

Puntatore a una variabile che contiene la dimensione di un elemento nell'elenco.

</dd> <dt>

*Valore elementCount* \[ out\]
</dt> <dd>

Puntatore a una variabile che contiene il numero di elementi nell'elenco.

</dd> <dt>

*EventTrace* \[ out\]
</dt> <dd>

Puntatore a una matrice di strutture **di \_ \_ \_ traccia degli eventi di scaricamento RTL** . Per altre informazioni, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Il caricatore archivia le informazioni sugli eventi scaricati in posizioni che possono essere lette nei processi sfruttando il fatto che Ntdll.dll viene caricato allo stesso indirizzo di base in tutti i processi. Quando un debugger deve eseguire una query sulle informazioni sui moduli scaricate, chiama questa funzione per determinare l'indirizzo in cui risiedono le variabili, quindi esegue una query sulla memoria virtuale nel processo di destinazione in corrispondenza di tali indirizzi per leggere i valori effettivi.

Ogni elemento nell'elenco è definito nel modo seguente.

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

A questa funzione non è associato alcun file di intestazione. La libreria di importazione associata, Ntdll. lib, è disponibile in Windows Driver Kit (WDK). È inoltre possibile chiamare questa funzione utilizzando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
