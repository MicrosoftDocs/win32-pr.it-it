---
description: La struttura QUERYTABLE fornisce un elenco dei computer che attualmente usano Network Monitor per acquisire i dati di rete.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: Struttura QUERYTABLE (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 9b8f291f055bfba159309b6c75a54d95514ed9c7614eb0456a4870e657f04209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555371"
---
# <a name="querytable-structure"></a>Struttura QUERYTABLE

La **struttura QUERYTABLE** fornisce un elenco dei computer che attualmente usano Network Monitor per acquisire i dati di rete.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**nStationQueries**
</dt> <dd>

In input, il numero massimo di computer che si Network Monitor restituire.

Nell'output, il numero di [strutture STATIONQUERY](stationquery.md) restituite da Network Monitor. Ogni **struttura STATIONQUERY** rappresenta un computer che sta attualmente acquisendo dati.

</dd> <dt>

**StationQuery**
</dt> <dd>

Nell'input, matrice di [strutture STATIONQUERY](stationquery.md) vuote che contiene il numero di elementi specificati in **nStationQueries**.

Nell'output, una struttura [STATIONQUERY](stationquery.md) compilata per ogni computer che acquisisce dati. Il numero di elementi riempiti viene restituito da **nStationQueries**.

</dd> </dl>

## <a name="remarks"></a>Commenti

La memoria per questa struttura e la matrice [STATIONQUERY](stationquery.md) deve essere allocata dall'applicazione chiamante e liberata dopo che le informazioni non sono più necessarie.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC::QueryStations](idelaydc-querystations.md)
</dt> <dt>

[IESP::QueryStations](iesp-querystations.md)
</dt> <dt>

[IRTC::QueryStations](irtc-querystations.md)
</dt> <dt>

[IStats::QueryStations](istats-querystations.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




