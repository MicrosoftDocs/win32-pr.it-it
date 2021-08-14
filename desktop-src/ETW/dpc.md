---
description: Questa classe è la classe del tipo di evento per gli eventi DPC (Device Deferred Procedure Call). La sintassi seguente è semplificata dal codice MOF.
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
ms.openlocfilehash: ef1f0c43d8b91aec1de266176aaef254360c73c99db163280b7bb2d1cbde4832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395165"
---
# <a name="dpc-class"></a>Classe DPC

Questa classe è la classe del tipo di evento per gli eventi DPC (Device Deferred Procedure Call).

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

La **classe DPC** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe DPC** ha queste proprietà.

<dl> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Extension("WmiTime")
</dt> </dl>

Tempo di ingresso DPC.

</dd> <dt>

**Routine**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Pointer
</dt> </dl>

Indirizzo della routine DPC. Usare l'indirizzo con gli eventi Image per trovare l'immagine avviata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi eventi vengono registrati quando viene immesso un DPC. Questi eventi vengono utilizzati per monitorare e verificare il comportamento dei driver e dei componenti in modalità kernel. Ad esempio, è possibile usare gli eventi DPC, ISR e Image per determinare i componenti che impiegano troppo tempo a livelli di interrupt elevati. Gli eventi DPC e ISR hanno un timestamp di ingresso che viene usato per calcolare la durata delle routine. Gli eventi immagine vengono letti per costruire le aree di memoria mappate a determinati moduli. È possibile utilizzare il mapping per individuare il modulo che contiene la routine di interrupt.

L'evento TimerDPC registra quando un DPC viene generato in seguito alla scadenza di un timer e l'evento ThreadDPC registra quando viene eseguito un DPC a thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 




