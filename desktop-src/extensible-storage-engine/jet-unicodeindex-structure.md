---
description: 'Altre informazioni su: JET_UNICODEINDEX struttura'
title: JET_UNICODEINDEX struttura
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb2779c75d525e45e9140d8f70665a09fe202b21
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988114"
---
# <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX struttura

La **JET_UNICODEINDEX** struttura consente di personalizzare la normalizzazione dei dati Unicode quando viene creato un indice su una colonna Unicode.

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a>Membri

**lcid**

ID delle impostazioni locali da usare per la normalizzazione dei dati. È possibile usare qualsiasi impostazione locale, purché language pack sia stato installato nel computer. L'unica eccezione è che le impostazioni locali indipendenti dalla lingua (LCID pari a zero) non sono valide.

**dwMapFlags**

Questi flag vengono passati a [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) quando i dati Unicode vengono normalizzati in una chiave, che consente ai flag definiti dall'utente di eseguire l'override del valore predefinito.

**Windows 2000:** gli unici due valori validi per **dwFlags** sono:

  - ( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE )

<!-- end list -->

  - ( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH )

**dwMapFlags** presenta le restrizioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>LCMAP_SORTKEY</p> | <p>Mandatory.</p> | 
| <p>LCMAP_BYTEREV</p> | <p>facoltativo.</p> | 
| <p>NORM_IGNORECASE</p> | <p>facoltativo.</p> | 
| <p>NORM_IGNORENONSPACE</p> | <p>facoltativo.</p> | 
| <p>NORM_IGNORESYMBOLS</p> | <p>facoltativo.</p> | 
| <p>NORM_IGNOREKANATYPE</p> | <p>facoltativo.</p> | 
| <p>NORM_IGNOREWIDTH</p> | <p>facoltativo.</p> | 
| <p>SORT_STRINGSORT</p> | <p>facoltativo.</p> | 



### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)
