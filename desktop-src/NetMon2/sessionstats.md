---
description: La struttura SESSIONSTATS fornisce statistiche su una sessione.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: Struttura SESSIONSTATS (Netmon. h)
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
ms.openlocfilehash: 4eddfa6b0a45627c59e61fd083eb11b8d5f26caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226963"
---
# <a name="sessionstats-structure"></a>Struttura SESSIONSTATS

La struttura **SESSIONSTATS** fornisce statistiche su una [*sessione*](s.md).

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

Indice di una stazione proprietaria all'interno della matrice di strutture [STATIONSTATS](stationstats.md) associata. La stazione del proprietario è la stazione che ha avviato la sessione, ovvero la stazione che ha inviato i pacchetti della sessione.

</dd> <dt>

**StationPartner**
</dt> <dd>

Indice dell'altra stazione all'interno della matrice di strutture [STATIONSTATS](stationstats.md) associata. La stazione partner è la stazione che ha ricevuto i pacchetti della sessione.

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

Network Monitor archivia le informazioni sulla sessione e sulla stazione in due matrici associate, i cui elementi sono rispettivamente **SESSIONSTATS** e [STATIONSTATS](stationstats.md) . I membri di queste strutture possono essere utilizzati per spostarsi tra di essi. Ad esempio, per passare alla sessione successiva per un proprietario di stazione specifico, usare **NextSession**. Per passare al proprietario e alla stazione partner della sessione nell'array STATIONSTATS, usare l'indice fornito in **StationOwner** e **StationPartner**.

> [!Note]  
> La matrice SESSIONSTATS contiene un elemento per ogni sessione nell'acquisizione corrente. L'algoritmo Network Monitor USA per aggiungere elementi alla matrice SESSIONSTATS si basa sulla registrazione efficiente delle informazioni mentre è in corso l'acquisizione. Di conseguenza, la sessione successiva per una stazione proprietaria specifica non è sempre l'elemento successivo nella matrice.

 

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

 

 




