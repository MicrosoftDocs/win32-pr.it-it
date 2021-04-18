---
description: La struttura delle statistiche fornisce le statistiche per l'acquisizione. Alcune di queste statistiche vengono generate da Network Monitor, mentre altre vengono generate dalla scheda di interfaccia di rete a cui è connessa l'oggetto NPP.
ms.assetid: 5e30ae30-d8ad-4336-9e4d-fa10ceefc966
title: Struttura STATISTICs (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATISTICS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a3798f32f7341722432441272eded7d7605cf8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310479"
---
# <a name="statistics-structure"></a>Struttura STATISTICs

La struttura delle **statistiche** fornisce le statistiche per l'acquisizione. Alcune di queste statistiche vengono generate da Network Monitor, mentre altre vengono generate dalla scheda di interfaccia di rete a cui è connessa l'oggetto NPP.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _STATISTICS {
  __int64 TimeElapsed;
  DWORD   TotalFramesCaptured;
  DWORD   TotalBytesCaptured;
  DWORD   TotalFramesFiltered;
  DWORD   TotalBytesFiltered;
  DWORD   TotalMulticastsFiltered;
  DWORD   TotalBroadcastsFiltered;
  DWORD   TotalFramesSeen;
  DWORD   TotalBytesSeen;
  DWORD   TotalMulticastsReceived;
  DWORD   TotalBroadcastsReceived;
  DWORD   TotalFramesDropped;
  DWORD   TotalFramesDroppedFromBuffer;
  DWORD   MacFramesReceived;
  DWORD   MacCRCErrors;
  __int64 MacBytesReceivedEx;
  DWORD   MacFramesDropped_NoBuffers;
  DWORD   MacMulticastsReceived;
  DWORD   MacBroadcastsReceived;
  DWORD   MacFramesDropped_HwError;
} STATISTICS, *LPSTATISTICS;
```



## <a name="members"></a>Members

<dl> <dt>

**TimeElapsed**
</dt> <dd>

Tempo trascorso, in microsecondi.

</dd> <dt>

**TotalFramesCaptured**
</dt> <dd>

Numero totale di frame attualmente archiviati. Questo numero è limitato dalle dimensioni del file di acquisizione o del buffer utilizzato per archiviare i frame.

</dd> <dt>

**TotalBytesCaptured**
</dt> <dd>

Numero totale di byte attualmente archiviati. Questo numero è limitato dalle dimensioni del file di acquisizione o del buffer utilizzato per archiviare i frame.

</dd> <dt>

**TotalFramesFiltered**
</dt> <dd>

Numero totale di frame passati tramite il filtro di acquisizione corrente. Se non si utilizza un filtro, questo valore corrisponde a **TotalFramesSeen**.

</dd> <dt>

**TotalBytesFiltered**
</dt> <dd>

Numero totale di frame passati tramite il filtro di acquisizione corrente. Se non si utilizza un filtro, questo valore corrisponde a **TotalBytesSeen**.

</dd> <dt>

**TotalMulticastsFiltered**
</dt> <dd>

Questo membro è obsoleto.

</dd> <dt>

**TotalBroadcastsFiltered**
</dt> <dd>

Questo membro è obsoleto.

</dd> <dt>

**TotalFramesSeen**
</dt> <dd>

Numero totale di frame gestiti dalla scheda di interfaccia di rete.

</dd> <dt>

**TotalBytesSeen**
</dt> <dd>

Numero totale di byte gestiti dalla scheda di interfaccia di rete.

</dd> <dt>

**TotalMulticastsReceived**
</dt> <dd>

Questo membro è obsoleto.

</dd> <dt>

**TotalBroadcastsReceived**
</dt> <dd>

Questo membro è obsoleto.

</dd> <dt>

**TotalFramesDropped**
</dt> <dd>

Numero totale di frame eliminati (frame che hanno superato il filtro ma non salvati).

</dd> <dt>

**TotalFramesDroppedFromBuffer**
</dt> <dd>

Numero di frame eliminati dal file o dal buffer di acquisizione. Quando il buffer è pieno, i frame meno recenti vengono rimossi per fare spazio a quelli nuovi.

</dd> <dt>

**MacFramesReceived**
</dt> <dd>

Numero di frame ricevuti dalla scheda di interfaccia di rete.

</dd> <dt>

**MacCRCErrors**
</dt> <dd>

Numero di errori CRC segnalati dalla scheda di interfaccia di rete.

</dd> <dt>

**MacBytesReceivedEx**
</dt> <dd>

Numero di byte ricevuti dalla scheda di interfaccia di rete.

</dd> <dt>

**MacFramesDropped \_ Nobuffers**
</dt> <dd>

Numero di frame rilasciati dalla scheda di interfaccia di rete a causa della mancanza di spazio del buffer.

</dd> <dt>

**MacMulticastsReceived**
</dt> <dd>

Numero di multicast ricevuti dai report della scheda di interfaccia di rete.

</dd> <dt>

**MacBroadcastsReceived**
</dt> <dd>

Numero di trasmissioni ricevute dai report NIC.

</dd> <dt>

**\_HwError MacFramesDropped**
</dt> <dd>

Numero di fotogrammi segnalati dalla scheda di interfaccia di rete come eliminati a causa di errori hardware.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata per recuperare le [*statistiche totali*](t.md)e per sospendere o arrestare l'acquisizione corrente.

Non è possibile recuperare le statistiche totali quando si usa l'interfaccia [IESP](iesp.md) NPP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IRTC:: GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IStats:: GetTotalStatistics](istats-gettotalstatistics.md)
</dt> <dt>

[IDelaydC::P ause](idelaydc-pause.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IDelaydC:: Stop](idelaydc-stop.md)
</dt> <dt>

[IESP:: Stop](iesp-stop.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> <dt>

[IStatsC:: Stop](istats-stop.md)
</dt> </dl>

 

 




