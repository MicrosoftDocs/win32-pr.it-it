---
description: La struttura STATIONSTATS fornisce statistiche su una specifica stazione descritta dall'acquisizione corrente.
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: Struttura STATIONSTATS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049826"
---
# <a name="stationstats-structure"></a>Struttura STATIONSTATS

La struttura **STATIONSTATS** fornisce statistiche su una specifica [*stazione*](s.md) descritta dall'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a>Members

<dl> <dt>

**NextStationStats**
</dt> <dd>

Indice della stazione successiva registrata nella matrice di strutture **STATIONSTATS** .

</dd> <dt>

**SessionPartnerList**
</dt> <dd>

Indice dell'elenco di partner di stazione.

</dd> <dt>

**Flag**
</dt> <dd>

Questo membro è obsoleto.

</dd> <dt>

**StationAddress**
</dt> <dd>

Indirizzo MAC della stazione.

</dd> <dt>

**Pad**
</dt> <dd>

Allineamento **DWORD** .

</dd> <dt>

**TotalPacketsReceived**
</dt> <dd>

Numero totale di pacchetti inviati alla stazione.

</dd> <dt>

**TotalDirectedPacketsSent**
</dt> <dd>

Numero totale di pacchetti diretti inviati dalla stazione.

</dd> <dt>

**TotalBroadcastPacketsSent**
</dt> <dd>

Numero totale di pacchetti diretti da broadcast (indirizzo MAC FF FF FF FF FF) inviati dalla stazione.

</dd> <dt>

**TotalMulticastPacketsSent**
</dt> <dd>

Numero totale di pacchetti multicast (bit del gruppo impostati nell'indirizzo di destinazione) inviati dalla stazione.

</dd> <dt>

**TotalBytesReceived**
</dt> <dd>

Numero totale di byte inviati alla stazione.

</dd> <dt>

**TotalBytesSent**
</dt> <dd>

Numero totale di byte inviati dalla stazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Network Monitor archivia le informazioni sulla sessione e sulla stazione in due matrici associate. i cui elementi sono rispettivamente [SESSIONSTATS](sessionstats.md) e **STATIONSTATS** . I membri di queste strutture possono essere utilizzati per spostarsi tra di essi. Ad esempio, per passare alla stazione successiva, usare **NextStationStats**. Per passare all'elenco partner di sessione nella matrice SESSIONSTATS, usare l'indice fornito in **SessionPartnerList**.

> [!Note]  
> La matrice **STATIONSTATS** contiene un elemento per ogni stazione utilizzata durante l'acquisizione corrente. L'algoritmo Network Monitor USA per aggiungere elementi a questa matrice si basa sul modo più efficiente per registrare le informazioni mentre è in corso l'acquisizione. Di conseguenza, la stazione successiva non è sempre l'elemento successivo nella matrice.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IRTC:: GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IStats:: GetConversationStatistics](istats-getconversationstatistics.md)
</dt> </dl>

 

 




