---
description: Consente al codice di dump di ottenere le informazioni sul modulo scaricato Ntdll.dll per l'archiviazione nel minidump.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: Funzione RtlGetUnloadEventTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d8575610ab34b62c9228f87fa64fbd6a40fa0201b7fe1a70ab95c7daae706854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058591"
---
# <a name="rtlgetunloadeventtrace-function"></a>Funzione RtlGetUnloadEventTrace

\[Questa funzione può essere modificata o rimossa da Windows senza preavviso.\]

Consente al codice di dump di ottenere le informazioni sul modulo scaricato Ntdll.dll per l'archiviazione nel minidump.

## <a name="syntax"></a>Sintassi


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce un puntatore a una matrice. Per altre informazioni, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

La matrice RtlpUnloadEventTrace è definita come segue:

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

A questa funzione non è associato alcun file di intestazione. La libreria di importazione associata, Ntdll.lib, è disponibile in Windows Driver Kit (WDK). È anche possibile chiamare questa funzione usando [**le funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
