---
description: La funzione PdhVbIsGoodStatus verifica un valore di stato per determinare se si tratta di un codice di esito positivo o negativo. Se il valore di stato è quello corretto, il valore restituito sarà diverso da zero. Se si tratta di un codice di stato di errore, il valore restituito sarà zero.
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: PdhVbIsGoodStatus (funzione)
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
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312146"
---
# <a name="pdhvbisgoodstatus-function"></a>PdhVbIsGoodStatus (funzione)

La funzione **PdhVbIsGoodStatus** verifica un valore di stato per determinare se si tratta di un codice di esito positivo o negativo. Se il valore di stato è quello corretto, il valore restituito sarà diverso da zero. Se si tratta di un codice di stato di errore, il valore restituito sarà zero.

> [!IMPORTANT]
> La funzione descritta in questo argomento può essere modificata o non disponibile in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbIsGoodStatus ( \_ ByVal StatusValue Long \_ ) Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*StatusValue* 
</dt> <dd>

Valore di stato restituito da un'altra funzione PDH che deve essere testata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce zero se il codice di stato è un codice di stato di errore. Restituisce un valore diverso da zero se il codice di stato è un codice di stato di esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




