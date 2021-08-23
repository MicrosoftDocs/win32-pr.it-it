---
description: Chiamato dal compilatore per implementare estensioni di gestione delle eccezioni strutturate.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: __C_specific_handler funzione (Wdm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: c61d14b591f54ea44ba0f33a36a2ca5acecb129ba46b5f45fcc18185f5d9448c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017829"
---
# <a name="__c_specific_handler-function"></a>\_\_Funzione \_ del gestore specifico di C \_

Chiamato dal compilatore per implementare estensioni di gestione delle eccezioni strutturate.

L'indirizzo relativo del gestore specifico del linguaggio è presente in UNWIND INFO ogni volta che vengono impostati i flag \_ UNW \_ FLAG \_ EHANDLER o UNW \_ FLAG \_ UHANDLER. Il gestore specifico del linguaggio viene chiamato come parte della ricerca di un gestore di eccezioni o come parte di una rimozione. Per altre informazioni, vedere [Gestore specifico del linguaggio](/cpp/build/language-specific-handler).

## <a name="syntax"></a>Sintassi


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ExceptionRecord* \[ Pollici\]
</dt> <dd>

Fornisce un puntatore a un record di eccezione, con la definizione Win64 standard.

</dd> <dt>

*EstablisherFrame* \[ Pollici\]
</dt> <dd>

Indirizzo della base dell'allocazione fissa dello stack per questa funzione.

</dd> <dt>

*ContextRecord* \[ in, out\]
</dt> <dd>

Punta al contesto dell'eccezione nel momento in cui è stata generata l'eccezione (nel caso del gestore eccezioni) o al contesto di rimozione corrente (nel caso del gestore di terminazione).

</dd> <dt>

*DispatcherContext* \[ in, out\]
</dt> <dd>

Punta al contesto del dispatcher per questa funzione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wdm.h</dt> </dl>        |
| Libreria<br/> | <dl> <dt>NtosKrnl.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntoskrnl.exe</dt> </dl> |



 

