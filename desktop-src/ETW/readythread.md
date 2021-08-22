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
ms.openlocfilehash: 1b4b3d63b63e4deb9c48f9e117122f021e9d63791292e60da3cc919a6e4535e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069811"
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

La **classe ReadyThread** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe ReadyThread** ha queste proprietà.

<dl> <dt>

AdjustIncrement
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3)
</dt> </dl>

Valore in base al quale viene modificata la priorità.

</dd> <dt>

AdjustReason
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2)
</dt> </dl>

Motivo della priority boost.



| Valore                                                                        | Significato                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Ignorare l'incremento.<br/>                                                                                        |
| <dl> <dt>1</dt> </dl> | Applicare l'incremento, che decadrà in modo incrementale alla fine di ogni quantum.<br/>                              |
| <dl> <dt>2</dt> </dl> | Applicare l'incremento come boost che decadrà nella sua interezza in modalità quantistica (in genere per la donazione della priorità).<br/> |



 

</dd> <dt>

Contrassegno
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4)
</dt> </dl>

Di seguito sono riportati i possibili flag di stato:



| Valore                                                                          | Significato                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0x1</dt> </dl> | Il thread è stato letto da DPC (chiamata di procedura posticipata).<br/> |
| <dl> <dt>0x2</dt> </dl> | Lo stack del kernel è attualmente scambiato.<br/>                      |
| <dl> <dt>0x4</dt> </dl> | Lo spazio indirizzi del processo viene scambiato.<br/>                       |



 

Si noti che quando lo stack del kernel o lo spazio degli indirizzi del processo viene scambiato, verrà generato un evento ReadyThread aggiuntivo dopo che lo stack del kernel o lo spazio indirizzi del processo è stato scambiato nuovamente in e il thread è pronto per l'invio.

</dd> <dt>

Riservato
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(5)
</dt> </dl>

Riservato.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Format("x")
</dt> </dl>

Identificatore di thread del thread da leggere per l'esecuzione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Thread \_ V2**](thread-v2.md)
</dt> </dl>

 

 




