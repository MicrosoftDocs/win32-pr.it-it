---
description: La struttura STATISTICS fornisce statistiche per l'acquisizione. Alcune di queste statistiche vengono generate da Network Monitor, mentre altre dall'interfaccia di rete a cui è connesso il NPP.
ms.assetid: 5e30ae30-d8ad-4336-9e4d-fa10ceefc966
title: Struttura STATISTICS (Netmon.h)
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
ms.openlocfilehash: 273e6ba9e32337cc65b3dce979d2ff407b904595237b60025e42fc58e57d9823
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778281"
---
# <a name="statistics-structure"></a>Struttura STATISTICS

La **struttura STATISTICS** fornisce statistiche per l'acquisizione. Alcune di queste statistiche vengono generate da Network Monitor, mentre altre dall'interfaccia di rete a cui è connesso il NPP.

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

Numero totale di frame attualmente archiviati. Questo numero è limitato dalle dimensioni del file o del buffer di acquisizione utilizzato per archiviare i frame.

</dd> <dt>

**TotalBytesCaptured**
</dt> <dd>

Numero totale di byte attualmente archiviati. Questo numero è limitato dalle dimensioni del file o del buffer di acquisizione utilizzato per archiviare i frame.

</dd> <dt>

**TotalFramesFiltered**
</dt> <dd>

Numero totale di frame passati attraverso il filtro di acquisizione corrente. Se non viene usato un filtro, questo valore corrisponde a **TotalFramesSeen.**

</dd> <dt>

**TotalBytesFiltered**
</dt> <dd>

Numero totale di frame passati attraverso il filtro di acquisizione corrente. Se non viene usato un filtro, questo valore corrisponde a **TotalBytesSeen.**

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

Numero totale di frame eliminati (frame che hanno superato il filtro ma non sono stati salvati).

</dd> <dt>

**TotalFramesDroppedFromBuffer**
</dt> <dd>

Numero di frame eliminati dal file o dal buffer di acquisizione. Quando il buffer è pieno, i frame meno recenti vengono rimossi per fare spazio a quelli nuovi.

</dd> <dt>

**MacFramesReceived**
</dt> <dd>

Numero di frame che la scheda di interfaccia di rete segnala di aver ricevuto.

</dd> <dt>

**MacCRCErrors**
</dt> <dd>

Numero di errori CRC segnalati dalla scheda di interfaccia di rete.

</dd> <dt>

**MacBytesReceivedEx**
</dt> <dd>

Numero di byte che la scheda di interfaccia di rete segnala di aver ricevuto.

</dd> <dt>

**MacFramesDropped \_ NoBuffers**
</dt> <dd>

Numero di frame segnalati dalla scheda di interfaccia di rete eliminati a causa della mancanza di spazio nel buffer.

</dd> <dt>

**MacMulticastsReceived**
</dt> <dd>

Numero di multicast ricevuti dalla scheda di interfaccia di rete.

</dd> <dt>

**MacBroadcastsReceived**
</dt> <dd>

Numero di trasmissioni ricevute dai report della scheda di interfaccia di rete.

</dd> <dt>

**MacFramesDropped \_ HwError**
</dt> <dd>

Numero di frame che la scheda di interfaccia di rete segnala come eliminati a causa di errori hardware.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata per recuperare le [*statistiche totali*](t.md)e per sospendere o arrestare l'acquisizione corrente.

Non è possibile recuperare le statistiche totali quando si usa l'interfaccia NPP [IESP.](iesp.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IStats::GetTotalStatistics](istats-gettotalstatistics.md)
</dt> <dt>

[IDelaydC::P ause](idelaydc-pause.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> <dt>

[IStatsC::Stop](istats-stop.md)
</dt> </dl>

 

 




