---
description: La struttura SESSIONSTATS fornisce statistiche su una sessione.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: Struttura SESSIONSTATS (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 231c94d2abda40974249f6c3cc82c8efc7518cb21d5881f44e63f647bcb21de2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128831"
---
# <a name="sessionstats-structure"></a>Struttura SESSIONSTATS

La **struttura SESSIONSTATS** fornisce statistiche su una [*sessione.*](s.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a>Members

<dl> <dt>

**NextSession**
</dt> <dd>

Indice della sessione successiva del proprietario della stazione.

</dd> <dt>

**StationOwner**
</dt> <dd>

Indice di una stazione proprietaria all'interno della matrice di [strutture STATIONSTATS](stationstats.md) associata. La stazione proprietaria è la stazione che ha avviato la sessione, la stazione che ha inviato i pacchetti della sessione.

</dd> <dt>

**StationPartner**
</dt> <dd>

Indice dell'altra stazione all'interno della matrice di [strutture STATIONSTATS](stationstats.md) associata. La stazione partner è la stazione che ha ricevuto i pacchetti della sessione.

</dd> <dt>

**Flag**
</dt> <dd>

Questo membro è obsoleto.

</dd> <dt>

**TotalPacketsSent**
</dt> <dd>

Numero di pacchetti inviati nella sessione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Network Monitor le informazioni di sessione e stazione in due matrici associate, i cui elementi sono **rispettivamente strutture SESSIONSTATS** e [STATIONSTATS.](stationstats.md) I membri di queste strutture possono essere usati per spostarsi tra di essi. Ad esempio, per passare alla sessione successiva per un proprietario di stazione specifico, usare **NextSession**. Per passare al proprietario e alla stazione partner della sessione nella matrice STATIONSTATS, usare l'indice fornito in **StationOwner** e **StationPartner**.

> [!Note]  
> La matrice SESSIONSTATS contiene un elemento per ogni sessione nell'acquisizione corrente. L'algoritmo Network Monitor per aggiungere elementi alla matrice SESSIONSTATS si basa sulla registrazione efficiente delle informazioni mentre è in corso l'acquisizione. Di conseguenza, la sessione successiva per una stazione proprietaria specifica non è sempre l'elemento successivo nella matrice.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> </dl>

 

 




