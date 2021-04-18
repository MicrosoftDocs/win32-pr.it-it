---
description: Copia il contenuto di un blocco di memoria di origine in un blocco di memoria di destinazione e supporta i blocchi di memoria di origine e di destinazione sovrapposti.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Funzione RtlMoveMemory (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304655"
---
# <a name="rtlmovememory-function"></a>RtlMoveMemory (funzione)

Copia il contenuto di un blocco di memoria di origine in un blocco di memoria di destinazione e supporta i blocchi di memoria di origine e di destinazione sovrapposti.

## <a name="syntax"></a>Sintassi


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Destinazione* \[ out\]
</dt> <dd>

Puntatore al blocco di memoria di destinazione in cui copiare i byte.

</dd> <dt>

*Origine* \[ dati in\]
</dt> <dd>

Puntatore al blocco di memoria di origine da cui copiare i byte.

</dd> <dt>

*Lunghezza* \[ in\]
</dt> <dd>

Numero di byte da copiare dall'origine alla destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="remarks"></a>Osservazioni

Il blocco di memoria di origine, definito dall' *origine* e dalla *lunghezza*, può sovrapporsi al blocco di memoria di destinazione, definito in base a *destinazione* e *lunghezza*.

La routine [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) viene eseguita più velocemente di **RtlMoveMemory**, ma **RtlCopyMemory** richiede che i blocchi di memoria di origine e di destinazione non si sovrappongano.

I chiamanti di **RtlMoveMemory** possono essere in esecuzione in qualsiasi livello IRQL se i blocchi di memoria di origine e di destinazione si trovano in memoria di sistema non di paging. In caso contrario, il chiamante deve essere in esecuzione a livello IRQL <= \_ livello APC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                    |
| Piattaforma di destinazione<br/>          | <dl> <dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Intestazione<br/>                   | <dl> <dt>WDM. h (include WDM. h, ntddk. h o Ntifs. h)</dt> </dl>                   |
| Libreria<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
