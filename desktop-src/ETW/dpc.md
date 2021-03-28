---
description: Questa classe è la classe del tipo di evento per gli eventi DPC (Device rinviated procedure call). La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: Classe DPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878733"
---
# <a name="dpc-class"></a>Classe DPC

Questa classe è la classe del tipo di evento per gli eventi DPC (Device rinviated procedure call).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a>Members

La classe **DPC** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **DPC** dispone di queste proprietà.

<dl> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), Extension ("WmiTime")
</dt> </dl>

Tempo di immissione DPC.

</dd> <dt>

**Routine**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), puntatore
</dt> </dl>

Indirizzo della routine DPC. Usare l'indirizzo con gli eventi di immagine per individuare l'immagine avviata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi eventi vengono registrati quando viene immesso un DPC. Questi eventi vengono utilizzati per monitorare e verificare il comportamento dei driver e dei componenti in modalità kernel. Ad esempio, è possibile usare gli eventi DPC, ISR ed image per determinare i componenti che impiegano troppo tempo a livelli di interrupt elevati. Gli eventi DPC e ISR hanno un timestamp di ingresso che viene usato per calcolare la durata delle routine. Gli eventi di immagine vengono letti per costruire le aree di memoria che eseguono il mapping a determinati moduli. È possibile usare il mapping per individuare il modulo che contiene la routine di interrupt.

L'evento TimerDPC registra quando un DPC viene attivato in seguito a una scadenza del timer e ai record di evento ThreadDPC quando viene eseguito un DPC a thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




