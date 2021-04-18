---
description: 'Altre informazioni su: struttura JET_RECPOS'
title: Struttura JET_RECPOS
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315096"
---
# <a name="jet_recpos-structure"></a>Struttura JET_RECPOS


_**Si applica a:** Windows | Windows Server_

## <a name="jet_recpos-structure"></a>Struttura JET_RECPOS

La struttura **JET_RECPOS** contiene una raccolta di numeri interi che rappresentano una posizione frazionaria all'interno di un indice. **centriesLT** è il numero di voci di indice minori della chiave di indice corrente. **centriesInRange** è il numero di voci di indice uguali alla chiave corrente. **centriesInRange** non è supportato e viene sempre restituito come 1. **centriesTotal** è il numero di voci di indice nell'indice. Tutti i valori sono approssimazioni senza alcuna garanzia di accuratezza.

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

Dimensioni in byte della struttura [JET_RETINFO](./jet-retinfo-structure.md) . Questo valore conferma la presenza dei campi seguenti.

**centriesLT**

Numero approssimativo di voci di indice minori della chiave corrente.

**centriesInRange**

Numero approssimativo di voci di indice uguali alla chiave corrente. Questo campo è sempre impostato su 1, indipendentemente dal numero di voci di indice effettivamente uguali alla chiave corrente.

**centriesTotal**

Numero approssimativo di voci nell'indice.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)
