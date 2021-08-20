---
description: Copia il contenuto di un blocco di memoria di origine in un blocco di memoria di destinazione e supporta blocchi di memoria di origine e di destinazione sovrapposti.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Funzione RtlMoveMemory (Wdm.h)
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
ms.openlocfilehash: bf4366633de321e27f6d3cdc0396fcdce81b0dac30b0d09a4c2c4675706d939e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161663"
---
# <a name="rtlmovememory-function"></a>Funzione RtlMoveMemory

Copia il contenuto di un blocco di memoria di origine in un blocco di memoria di destinazione e supporta blocchi di memoria di origine e di destinazione sovrapposti.

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

*Destinazione* \[ Cambio\]
</dt> <dd>

Puntatore al blocco di memoria di destinazione in cui copiare i byte.

</dd> <dt>

*Origine* \[ Pollici\]
</dt> <dd>

Puntatore al blocco di memoria di origine da cui copiare i byte.

</dd> <dt>

*Lunghezza* \[ Pollici\]
</dt> <dd>

Numero di byte da copiare dall'origine alla destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="remarks"></a>Osservazioni

Il blocco di memoria di origine, definito da *Source* e *Length,* può sovrapporsi al blocco di memoria di destinazione, definito da *Destination* e *Length.*

La routine [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) viene eseguita più velocemente rispetto a **RtlMoveMemory,** ma **RtlCopyMemory** richiede che i blocchi di memoria di origine e di destinazione non si sovrappongano.

I chiamanti **di RtlMoveMemory** possono essere in esecuzione in qualsiasi IRQL se i blocchi di memoria di origine e di destinazione sono nella memoria di sistema non di pagina. In caso contrario, il chiamante deve essere in esecuzione in IRQL <= APC \_ LEVEL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                    |
| Piattaforma di destinazione<br/>          | <dl> <dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Intestazione<br/>                   | <dl> <dt>Wdm.h (includere Wdm.h, Ntddk.h o Ntifs.h)</dt> </dl>                   |
| Libreria<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
