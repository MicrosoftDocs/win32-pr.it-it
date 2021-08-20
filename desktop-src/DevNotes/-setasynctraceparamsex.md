---
description: 'Funzione SetAsyncTraceParamsEx: completa la configurazione di un buffer di traccia con campi facoltativi per le tracce in stile sprintf.'
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: Funzione SetAsyncTraceParamsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 6c41369e8a0d73a56dc5d9d831d0028e87a7ecec300f2e43a625f17bd25bede1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538867"
---
# <a name="setasynctraceparamsex-function"></a>Funzione SetAsyncTraceParamsEx

Completa la configurazione di un buffer di traccia con campi facoltativi per le tracce in stile **sprintf.**

## <a name="syntax"></a>Sintassi


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszModule* 
</dt> <dd>

Nome del modulo associato alla traccia.

</dd> <dt>

*pszFile* 
</dt> <dd>

Nome del file di origine che contiene l'eccezione.

</dd> <dt>

*lLine* 
</dt> <dd>

Numero di riga dell'eccezione nel file di origine.

</dd> <dt>

*pszFunction* 
</dt> <dd>

Nome della funzione dell'eccezione.

</dd> <dt>

*dwTraceMask* 
</dt> <dd>

Costante del flag di traccia che rappresenta uno dei tipi di traccia disponibili. Questo parametro può essere uno dei valori seguenti.

<dl> <dt>

<span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**ERRORE IRREVERSIBILE \_ TRACE \_ MASK** (0x00000001)
</dt> <dt>

<span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERRORE \_ TRACE \_ MASK** (0x00000002)
</dt> <dt>

<span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG \_ TRACE \_ MASK** (0x00000004)
</dt> <dt>

<span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE \_ TRACE \_ MASK** (0x00000008)
</dt> <dt>

<span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT \_ TRACE \_ MASK** (0x00000010)
</dt> <dt>

<span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE \_ TRACE \_ MASK** (0x00000020)
</dt> <dt>

<span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL \_ TRACE \_ MASK** (0xFFFFFFFF)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce 1 se la funzione ha esito positivo; In caso contrario, restituisce 0.

## <a name="remarks"></a>Commenti

Exstrace.dll è un componente facoltativo che viene installato con il Simple Mail Transfer Protocol (SMTP) e il protocollo NNTP (Network News Transfer Protocol).

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
