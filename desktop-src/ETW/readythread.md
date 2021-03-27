---
description: Questa classe è la classe del tipo di evento per gli eventi di thread pronti. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: Classe ReadyThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879521"
---
# <a name="readythread-class"></a>Classe ReadyThread

Questa classe è la classe del tipo di evento per gli eventi di thread pronti.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a>Members

La classe **ReadyThread** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **ReadyThread** dispone di queste proprietà.

<dl> <dt>

AdjustIncrement
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Valore in base al quale viene regolata la priorità.

</dd> <dt>

AdjustReason
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2)
</dt> </dl>

Motivo del priority boost.



| Valore                                                                        | Significato                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Ignorare l'incremento.<br/>                                                                                        |
| <dl> <dt>1</dt> </dl> | Applicare l'incremento, che decade in modo incrementale alla fine di ogni quantum.<br/>                              |
| <dl> <dt>2</dt> </dl> | Applicare l'incremento come Boost che dedurrà interamente il suo intero in quantum (in genere per la donazione di priorità).<br/> |



 

</dd> <dt>

Contrassegno
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4)
</dt> </dl>

Di seguito sono riportati i flag di stato possibili:



| Valore                                                                          | Significato                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0x1</dt> </dl> | Il thread è stato preparato da DPC (chiamata di procedura posticipata).<br/> |
| <dl> <dt>0x2</dt> </dl> | Lo stack del kernel è attualmente stato scambiato.<br/>                      |
| <dl> <dt>0x4</dt> </dl> | Lo spazio degli indirizzi del processo viene scambiato.<br/>                       |



 

Si noti che quando lo stack del kernel o lo spazio degli indirizzi del processo viene sostituito, sarà presente un evento ReadyThread aggiuntivo dopo lo scambio dello stack del kernel o dello spazio degli indirizzi del processo e il thread sarà pronto per l'invio.

</dd> <dt>

Riservato
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5)
</dt> </dl>

Riservato.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), Format ("x")
</dt> </dl>

Identificatore del thread di cui è in corso la preparazione per l'esecuzione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Thread \_ v2**](thread-v2.md)
</dt> </dl>

 

 




