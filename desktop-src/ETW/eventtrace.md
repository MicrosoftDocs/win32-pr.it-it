---
description: Classe astratta da cui vengono derivate tutte le classi di traccia eventi.
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: Classe EventTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: 37124a1c5ef23782261cbe94462c737d137dc6965363d9c907ea895e289237d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130611"
---
# <a name="eventtrace-class"></a>Classe EventTrace

Classe astratta da cui vengono derivate tutte le classi di traccia eventi.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a>Members

La **classe EventTrace** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe EventTrace** ha queste proprietà.

<dl> <dt>

**EventGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (8), **Max** (16)
</dt> </dl>

GUID della classe di traccia eventi di questo evento.

</dd> <dt>

**EventSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (1)
</dt> </dl>

Numero totale di byte dell'evento.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (3)
</dt> </dl>

Tipo di evento definito dal provider. Indica la classe del tipo di evento da usare per decifrare i dati degli eventi definiti dal provider (i dati a cui **punta MofData**).

</dd> <dt>

**InstanceId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (11)
</dt> </dl>

Identificatore di questa istanza dell'evento.

</dd> <dt>

**KernelTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (9)
</dt> </dl>

Tempo di esecuzione trascorso per le istruzioni in modalità kernel, in tick CPU.

</dd> <dt>

**MofData**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (14), **Puntatore**
</dt> </dl>

Puntatore ai dati dell'evento specifici del provider.

</dd> <dt>

**MofLength**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (15)
</dt> </dl>

Lunghezza dei dati dell'evento specifici del provider.

</dd> <dt>

**ParentGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (12), **Max** (16)
</dt> </dl>

GUID della classe di traccia eventi dell'istanza padre.

</dd> <dt>

**ParentInstanceId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (13)
</dt> </dl>

Identificatore dei dati dell'istanza padre.

</dd> <dt>

**ReservedHeaderField**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (2)
</dt> </dl>

Riservato.

</dd> <dt>

**ThreadId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (6), **Puntatore**
</dt> </dl>

Identifica il thread che ha generato l'evento.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (7)
</dt> </dl>

Contiene la data e l'ora in cui si è verificato l'evento.

</dd> <dt>

**TraceLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (4)
</dt> </dl>

Valore definito dal provider che definisce il livello di gravità usato per generare l'evento.

</dd> <dt>

**TraceVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (5)
</dt> </dl>

Numero di versione definito dal provider della classe di traccia eventi utilizzata per generare l'evento.

</dd> <dt>

**Tempi**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (10)
</dt> </dl>

Tempo di esecuzione trascorso per le istruzioni in modalità utente, in tick CPU.

</dd> </dl>

## <a name="remarks"></a>Commenti

Non usare queste proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| MOF<br/>                      | <dl> <dt>Wmi.mof</dt> </dl> |



 

 




