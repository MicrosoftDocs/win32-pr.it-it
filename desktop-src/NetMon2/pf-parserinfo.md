---
description: La struttura PARSERINFO di PF \_ definisce un parser alla volta. Nella struttura PF PARSERINFO un parser viene definito dalle informazioni sul protocollo rilevato \_ dal parser.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: PF_PARSERINFO struttura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 533e8dae6a009488998acd3232b062b423553b9df10f14ec97ef9ae2f8c55bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889941"
---
# <a name="pf_parserinfo-structure"></a>Struttura PARSERINFO di PF \_

La **struttura \_ PARSERINFO** di PF definisce un parser alla volta. Nella **struttura PF \_ PARSERINFO** un parser viene definito dalle informazioni sul protocollo rilevato dal parser.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**szProtocolName**
</dt> <dd>

Nome del protocollo rilevato dal parser.

</dd> <dt>

**szComment**
</dt> <dd>

Breve descrizione del protocollo.

</dd> <dt>

**szHelpFile**
</dt> <dd>

Nome del file della Guida del protocollo, se presente.

</dd> <dt>

**pWhoCanPrecedeMe**
</dt> <dd>

Puntatore a [una struttura PF \_ FOLLOWSET](pf-followset.md) che elenca i protocolli che possono precedere il protocollo descritto **dalla struttura PF \_ PARSERINFO.** Network Monitor aggiunge il protocollo del parser al [*set seguente*](f.md) di tutti i protocolli nel set.

</dd> <dt>

**pWhoCanFollowMe**
</dt> <dd>

Puntatore a [una struttura PF \_ FOLLOWSET](pf-followset.md) che elenca il protocollo che può seguire il protocollo descritto **dalla struttura PF \_ PARSERINFO.** Network Monitor aggiunge i protocolli del set al [*set seguente*](f.md) del protocollo del parser.

</dd> <dt>

**pWhoHandsOffToMe**
</dt> <dd>

Puntatore a [una struttura PF \_ HANDOFFSET](pf-handoffset.md) che si sposta sul protocollo descritto **dalla struttura PF \_ PARSERINFO.** Network Monitor aggiunge il protocollo del parser ai [*set di handoff*](h.md) di tutti i protocolli nel set.

</dd> <dt>

**pWhoDoIHandOffTo**
</dt> <dd>

Puntatore a [una struttura PF \_ HANDOFFSET](pf-handoffset.md) che elenca i protocolli a cui il protocollo del parser consegna. Network Monitor aggiunge i protocolli di questo set al [*set di handoff*](h.md) del protocollo del parser.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura PF \_ PARSERINFO** viene usata nella struttura **PF \_ PARSERDLLINFO** per fornire una descrizione di un parser. Network Monitor usa la descrizione del parser per aggiornare il file [*Parser.ini*](p.md) e i file INI dei parser che precedono e seguono il protocollo descritto nella struttura **PF \_ PARSERINFO.**

Un set di follow specifica i protocolli che seguono un protocollo. Network Monitor usa un set di follow quando il parser non è in grado di identificare il protocollo successivo dai dati in un'istanza del protocollo. Un set di follow viene archiviato nel file [*Parser.ini.*](p.md) Quando il parser viene installato per la prima volta, Network Monitor aggiorna il set seguente dei protocolli del parser elencati in **pWhoCanPrecedeMe** e **pWhoCanFollowMe**.

Un set di consegna specifica i protocolli che seguono un protocollo. Il parser usa un set di handoff solo quando il parser è in grado di identificare il protocollo successivo dai dati in un'istanza del protocollo. Un set di handoff viene archiviato nei file INI di ogni parser. Quando il parser viene installato per la prima volta, Network Monitor aggiorna il set di handoff dei protocolli del parser elencati in **pWhoHandsOffToMe** e **pWhoDoIHandOffTo**.



| Per informazioni su                                               | Vedere                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Che cosa sono i parser e come funzionano con Network Monitor.        | [Parser](parsers.md)                                                       |
| Contenuto dei set seguenti.                                        | [Specifica di un set di follow](specifying-a-follow-set.md)                       |
| Quali set di handoff contengono.                                       | [Specifica di un set handoff](specifying-a-handoff-set.md)                     |
| Punti di ingresso inclusi nella DLL del parser.                | [Architettura della DLL del parser](parser-dll-architecture.md)                       |
| Come implementare **ParserAutoInstallInfo include**  un esempio. | [Implementazione di ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> <dt>

[PF \_ FOLLOWSET](pf-followset.md)
</dt> <dt>

[PF \_ HANDOFFSET](pf-handoffset.md)
</dt> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




