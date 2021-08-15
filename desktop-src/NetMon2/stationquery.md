---
description: La struttura STATIONQUERY fornisce informazioni su un computer specifico usando Network Monitor.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: Struttura STATIONQUERY (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a2e46f4c0d213091a3915b5310d7768a193d33e5ac3391fd3bc3c6781e32cb57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363057"
---
# <a name="stationquery-structure"></a>Struttura STATIONQUERY

La **struttura STATIONQUERY** fornisce informazioni su un computer specifico usando Network Monitor.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a>Members

<dl> <dt>

**Flag**
</dt> <dd>

Flag che identificano lo stato corrente Network Monitor.



| Valore                                                                                                                                                                                                                | Significato                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <dt>**FLAG STATIONQUERY \_ \_ CARICATI**</dt> </dl>                   | Il driver viene caricato, ma il kernel non lo è.<br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <dt>**FLAG STATIONQUERY \_ \_ IN ESECUZIONE**</dt> </dl>                | Il driver viene caricato ma non acquisisce dati.<br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <dt>**ACQUISIZIONE DI FLAG STATIONQUERY \_ \_**</dt> </dl>          | Il driver è attivamente coinvolto in un'acquisizione.<br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <dt>**FLAG STATIONQUERY \_ \_ CHE TRASMETTONO**</dt> </dl> | Questo flag è obsoleto.<br/>                       |



 

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Numero di versione secondaria Network Monitor installato nel computer.

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Numero di versione principale Network Monitor installato nel computer.

</dd> <dt>

**LicenseNumber**
</dt> <dd>

Numero di licenza software.

</dd> <dt>

**MachineName**
</dt> <dd>

Nome del produttore del computer, se presente.

</dd> <dt>

**UserName**
</dt> <dd>

Nome utente o identificatore di sistema.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

**AdapterAddress**
</dt> <dd>

Indirizzo NIC.

</dd> <dt>

**WMachineName**
</dt> <dd>

Nome del computer Unicode. Questo membro si applica Network Monitor 2.0 o versione successiva.

</dd> <dt>

**WUserName**
</dt> <dd>

Nome utente Unicode. Questo membro si applica Network Monitor 2.0 o versione successiva.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una matrice di queste strutture viene usata dalla struttura [QUERYTABLE](querytable.md) per fornire un elenco dei computer che attualmente usano Network Monitor per acquisire i dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Querytable](querytable.md)
</dt> </dl>

 

 




