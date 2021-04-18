---
description: Completa la configurazione di un buffer di traccia con campi facoltativi per le tracce di tipo sprintf.
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: SetAsyncTraceParamsEx (funzione)
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
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326837"
---
# <a name="setasynctraceparamsex-function"></a>SetAsyncTraceParamsEx (funzione)

Completa la configurazione di un buffer di traccia con campi facoltativi per le tracce di tipo **sprintf**.

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

Costante di un flag di traccia che rappresenta uno dei tipi di traccia disponibili. Questo parametro può essere uno dei valori seguenti.

<dl> <dt>

<span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**Errore irreversibile \_ \_Maschera di traccia** (0x00000001)
</dt> <dt>

<span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Errore \_ \_Maschera di traccia** (0x00000002)
</dt> <dt>

<span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Esegui debug \_ \_Maschera di traccia** (0x00000004)
</dt> <dt>

<span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**Stato \_ di \_Maschera di traccia** (0x00000008)
</dt> <dt>

<span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>Funzione **\_ \_Maschera di traccia** (0x00000010)
</dt> <dt>

<span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Messaggio \_ di \_Maschera di traccia** (0x00000020)
</dt> <dt>

<span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Tutto \_ \_Maschera di traccia** (0xFFFFFFFF)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce 1 se la funzione ha esito positivo; in caso contrario, restituisce 0.

## <a name="remarks"></a>Commenti

Exstrace.dll è un componente facoltativo che viene installato con il Simple Mail Transfer Protocol (SMTP) e il protocollo NNTP (Network News Transfer Protocol).

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
