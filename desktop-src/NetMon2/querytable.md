---
description: La struttura QUERYTABLE fornisce un elenco dei computer che attualmente utilizzano Network Monitor per acquisire i dati di rete.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: Struttura QUERYTABLE (Netmon. h)
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
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310960"
---
# <a name="querytable-structure"></a>Struttura QUERYTABLE

La struttura **QUERYTABLE** fornisce un elenco dei computer che attualmente utilizzano Network Monitor per acquisire i dati di rete.

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

In input, il numero massimo di computer che si desidera Network Monitor restituire.

Nell'output, numero di strutture [STATIONQUERY](stationquery.md) restituite da Network Monitor. Ogni struttura **STATIONQUERY** rappresenta un computer che attualmente sta acquisendo dati.

</dd> <dt>

**StationQuery**
</dt> <dd>

In input, matrice di strutture [STATIONQUERY](stationquery.md) vuote che contiene il numero di elementi specificato in **nStationQueries**.

Nell'output, una struttura [STATIONQUERY](stationquery.md) piena per ogni computer che sta acquisendo dati. Il numero di elementi riempiti viene restituito da **nStationQueries**.

</dd> </dl>

## <a name="remarks"></a>Commenti

La memoria per questa struttura e la matrice [STATIONQUERY](stationquery.md) deve essere allocata dall'applicazione chiamante e liberata dopo che le informazioni non sono più necessarie.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC::QueryStations](idelaydc-querystations.md)
</dt> <dt>

[IESP::QueryStations](iesp-querystations.md)
</dt> <dt>

[IRTC:: QueryStations](irtc-querystations.md)
</dt> <dt>

[IStats:: QueryStations](istats-querystations.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




