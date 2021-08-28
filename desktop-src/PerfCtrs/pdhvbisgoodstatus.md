---
description: La funzione PdhVbIsGoodStatus verifica un valore di stato per determinare se si tratta di un codice di esito positivo o negativo. Se il valore dello stato ha esito positivo, il valore restituito sarà diverso da zero. Se si tratta di un codice di stato di errore, il valore restituito sarà zero.
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: Funzione PdhVbIsGoodStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: e0b142da988143d7304a6b9b01bc5163e741fdaff77d7e0d796882607fc73044
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683771"
---
# <a name="pdhvbisgoodstatus-function"></a>Funzione PdhVbIsGoodStatus

La **funzione PdhVbIsGoodStatus** verifica un valore di stato per determinare se si tratta di un codice di esito positivo o negativo. Se il valore dello stato ha esito positivo, il valore restituito sarà diverso da zero. Se si tratta di un codice di stato di errore, il valore restituito sarà zero.

> [!IMPORTANT]
> La funzione descritta in questo argomento potrebbe essere modificata o non disponibile in futuro. Microsoft consiglia invece di usare le funzioni descritte in [Funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbIsGoodStatus( \_ ByVal StatusValue As Long \_ ) As Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*StatusValue* 
</dt> <dd>

Valore di stato restituito da un'altra funzione PDH da testare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce zero se il codice di stato è un codice di stato di errore. Restituisce un valore diverso da zero se il codice di stato è un codice di stato di esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




