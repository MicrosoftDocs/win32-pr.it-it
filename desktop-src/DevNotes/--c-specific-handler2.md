---
description: Chiamato dal compilatore per implementare estensioni di gestione delle eccezioni strutturate.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: Funzione __C_specific_handler (WDM. h)
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
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326686"
---
# <a name="__c_specific_handler-function"></a>\_\_\_Funzione del gestore specifico di C \_

Chiamato dal compilatore per implementare estensioni di gestione delle eccezioni strutturate.

L'indirizzo relativo del gestore specifico del linguaggio è presente nelle informazioni di rimozione \_ ogni volta che Flags Unw \_ flag \_ EHANDLER o Unw \_ flag \_ UHANDLER sono impostati. Il gestore specifico del linguaggio viene chiamato come parte della ricerca di un gestore di eccezioni o come parte di una rimozione. Per ulteriori informazioni, vedere [gestore specifico del linguaggio](/cpp/build/language-specific-handler).

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

*ExceptionRecord* \[ in\]
</dt> <dd>

Fornisce un puntatore a un record di eccezione, che ha la definizione Win64 standard.

</dd> <dt>

*EstablisherFrame* \[ in\]
</dt> <dd>

Indirizzo della base dell'allocazione dello stack fisso per questa funzione.

</dd> <dt>

*ContextRecord* \[ in uscita\]
</dt> <dd>

Punta al contesto dell'eccezione nel momento in cui è stata generata l'eccezione (nel caso del gestore di eccezioni) o nel contesto di rimozione corrente (nel caso del gestore di terminazione).

</dd> <dt>

*DispatcherContext* \[ in uscita\]
</dt> <dd>

Punta al contesto del dispatcher per questa funzione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WDM. h</dt> </dl>        |
| Libreria<br/> | <dl> <dt>NtosKrnl. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntoskrnl.exe</dt> </dl> |



 

