---
description: 'Altre informazioni su: JET_RECPOS struttura'
title: JET_RECPOS struttura
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: 6eb136ef309bad4ffd5c02768a3ca5b8e0d52f3c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470516"
---
# <a name="jet_recpos-structure"></a>JET_RECPOS struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_recpos-structure"></a>JET_RECPOS struttura

La **JET_RECPOS** contiene una raccolta di interi che rappresentano una posizione frazionaria all'interno di un indice. **centriesLT** è il numero di voci di indice inferiori alla chiave di indice corrente. **centriesInRange è** il numero di voci di indice uguali alla chiave corrente. **centriesInRange** non è supportato e viene sempre restituito come 1. **centriesTotal** è il numero di voci di indice nell'indice. Tutti i valori sono approssimazioni senza alcuna garanzia di accuratezza.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni della struttura [JET_RETINFO,](./jet-retinfo-structure.md) in byte. Questo valore conferma la presenza dei campi seguenti.

**centriesLT**

Numero approssimativo di voci di indice inferiori alla chiave corrente.

**centriesInRange**

Numero approssimativo di voci di indice uguali alla chiave corrente. Questo campo è sempre impostato su 1, indipendentemente dal numero di voci di indice effettivamente uguali alla chiave corrente.

**centriesTotal**

Numero approssimativo di voci nell'indice.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)
