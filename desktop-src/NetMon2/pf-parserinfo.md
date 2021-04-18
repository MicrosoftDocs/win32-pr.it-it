---
description: La \_ struttura PF PARSERINFO definisce un parser alla volta. Nella struttura PF \_ PARSERINFO un parser viene definito dalle informazioni sul protocollo rilevato dal parser.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: Struttura PF_PARSERINFO (Netmon. h)
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
ms.openlocfilehash: 28ebeaad31e6f40ceb961d8c303a22590966947f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314750"
---
# <a name="pf_parserinfo-structure"></a>\_Struttura PF PARSERINFO

La struttura **PF \_ PARSERINFO** definisce un parser alla volta. Nella struttura **PF \_ PARSERINFO** un parser viene definito dalle informazioni sul protocollo rilevato dal parser.

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

Nome del file della guida del protocollo, se disponibile.

</dd> <dt>

**pWhoCanPrecedeMe**
</dt> <dd>

Puntatore a una struttura [PF \_ follower](pf-followset.md) che elenca i protocolli che possono precedere il protocollo descritto dalla struttura **PF \_ PARSERINFO** . Network Monitor aggiunge il protocollo del parser al [*set seguente*](f.md) di tutti i protocolli nel set.

</dd> <dt>

**pWhoCanFollowMe**
</dt> <dd>

Puntatore a una struttura [PF \_ follower](pf-followset.md) che elenca il protocollo che può seguire il protocollo descritto dalla struttura **PF \_ PARSERINFO** . Network Monitor aggiunge i protocolli del set al [*seguente set*](f.md) del protocollo del parser.

</dd> <dt>

**pWhoHandsOffToMe**
</dt> <dd>

Puntatore a una struttura [PF \_ HANDOFFSET](pf-handoffset.md) che passa al protocollo descritto dalla struttura **PF \_ PARSERINFO** . Network Monitor aggiunge il protocollo del parser ai [*set*](h.md) di tutti i protocolli nel set.

</dd> <dt>

**pWhoDoIHandOffTo**
</dt> <dd>

Puntatore a una struttura [PF \_ HANDOFFSET](pf-handoffset.md) che elenca i protocolli a cui il protocollo del parser passa. Network Monitor aggiunge i protocolli di questo set al [*set di continuità*](h.md) del protocollo del parser.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **PF \_ PARSERINFO** viene usata nella struttura **PF \_ PARSERDLLINFO** per fornire una descrizione di un parser. Network Monitor usa la descrizione del parser per aggiornare il file di [*Parser.ini*](p.md) e i file ini dei parser che precedono e seguono il protocollo descritto nella struttura **PF \_ PARSERINFO** .

Un set di seguito specifica i protocolli che seguono un protocollo. Network Monitor utilizza un set di seguito quando il parser non è in grado di identificare il protocollo successivo tra i dati in un'istanza del protocollo. Un set di seguito viene archiviato nel file di [*Parser.ini*](p.md) . Quando il parser viene installato per la prima volta, Network Monitor aggiorna il set seguente di protocolli del parser elencati in **pWhoCanPrecedeMe** e **pWhoCanFollowMe**.

Un set di continuità specifica i protocolli che seguono un protocollo. Il parser utilizza un set di continuità solo quando il parser è in grado di identificare il protocollo successivo tra i dati in un'istanza del protocollo. Un set di continuità viene archiviato nei file INI di ogni parser. Quando il parser viene installato per la prima volta, Network Monitor aggiorna il set di protocolli di parser elencati in **pWhoHandsOffToMe** e **pWhoDoIHandOffTo**.



| Per informazioni su                                               | Vedere                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor.        | [Parser](parsers.md)                                                       |
| Elementi che seguono i set.                                        | [Specifica di un set di seguito](specifying-a-follow-set.md)                       |
| Elementi inclusi nei set di continuità.                                       | [Specifica di un set di continuità](specifying-a-handoff-set.md)                     |
| Punti di ingresso inclusi nella DLL del parser.                | [Architettura DLL parser](parser-dll-architecture.md)                       |
| L'implementazione di **ParserAutoInstallInfo**  include un esempio. | [Implementazione di ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> <dt>

[PF \_](pf-followset.md)
</dt> <dt>

[PF \_ HANDOFFSET](pf-handoffset.md)
</dt> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




