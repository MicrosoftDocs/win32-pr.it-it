---
description: La funzione PdhVbGetDoubleCounterValue restituisce il valore corrente del contatore specificato come valore a virgola mobile a precisione doppia.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: PdhVbGetDoubleCounterValue (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345511"
---
# <a name="pdhvbgetdoublecountervalue-function"></a>PdhVbGetDoubleCounterValue (funzione)

La funzione **PdhVbGetDoubleCounterValue** restituisce il valore corrente del contatore specificato come valore a virgola mobile a precisione doppia. È necessario controllare *CounterStatus* prima di utilizzare il numero restituito, perché il contatore potrebbe non essere valido durante la lettura. Per controllare lo stato del contatore, chiamare la funzione [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) .

> [!IMPORTANT]
> La funzione descritta in questo argomento può essere modificata o non disponibile in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbGetDoubleCounterValue ( \_ ByVal CounterHandle Long, \_ ByVal CounterStatus Long \_ ) As Double

## <a name="parameters"></a>Parametri

<dl> <dt>

*CounterHandle* 
</dt> <dd>

ID del contatore il cui valore corrente deve essere letto.

</dd> <dt>

*CounterStatus* 
</dt> <dd>

Variabile in cui lo stato corrente del valore del contatore viene restituito al chiamante. Il valore dei dati restituiti è valido solo se il valore restituito in CounterStatus è PDH \_ CSTATUS \_ dati validi \_ o PDH \_ CSTATUS \_ nuovi \_ dati (vedere codici di errore PDH). Se il valore restituito in CounterStatus è qualsiasi altro valore, non usare i dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il valore in virgola mobile e precisione doppia del contatore corrente, calcolato e formattato in base a quanto definito dal tipo di contatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




