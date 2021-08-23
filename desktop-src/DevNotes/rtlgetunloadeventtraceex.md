---
description: Recupera le dimensioni e la posizione dell'elenco di moduli scaricati dinamicamente per il processo corrente.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: Funzione RtlGetUnloadEventTraceEx
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
ms.openlocfilehash: 35c4001851cc12701152f983c51a800d8f1846e015f5cf4d967c6371d9807578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571361"
---
# <a name="rtlgetunloadeventtraceex-function"></a>Funzione RtlGetUnloadEventTraceEx

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

*ElementSize* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che contiene le dimensioni di un elemento nell'elenco.

</dd> <dt>

*ElementCount* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che contiene il numero di elementi nell'elenco.

</dd> <dt>

*EventTrace* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di **strutture \_ RTL UNLOAD \_ EVENT \_ TRACE.** Per altre informazioni, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Il caricatore archivia le informazioni sugli eventi non caricati in posizioni che possono essere lette tra i processi sfruttando il fatto che Ntdll.dll viene caricato allo stesso indirizzo di base in tutti i processi. Quando un debugger deve eseguire query sulle informazioni sui moduli scaricati, chiama questa funzione per determinare l'indirizzo in cui si trovano le variabili, quindi esegue una query sulla memoria virtuale nel processo di destinazione in tali indirizzi per leggere i valori effettivi.

Ogni elemento nell'elenco viene definito come segue.

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

A questa funzione non è associato alcun file di intestazione. La libreria di importazione associata, Ntdll.lib, è disponibile in Windows Driver Kit (WDK). È anche possibile chiamare questa funzione usando [**le funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
