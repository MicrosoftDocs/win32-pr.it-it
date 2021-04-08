---
description: 'Altre informazioni su: struttura JET_TUPLELIMITS'
title: Struttura JET_TUPLELIMITS
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
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
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968615"
---
# <a name="jet_tuplelimits-structure"></a>Struttura JET_TUPLELIMITS


_**Si applica a:** Windows | Windows Server_

## <a name="jet_tuplelimits-structure"></a>Struttura JET_TUPLELIMITS

La struttura **JET_TUPLELIMITS** consente la personalizzazione delle caratteristiche degli indici di tupla in base all'indice, anziché per ogni singola istanza, usando [JetSetSystemParameter](./jetsetsystemparameter-function.md).

**Windows Server 2003:** La struttura **JET_TUPLELIMITS** è stata introdotta in Windows Server 2003.

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a>Membri

**chLengthMin**

Lunghezza minima di una tupla. Il valore predefinito è 3.

**chLengthMax**

Lunghezza massima di una tupla. Il valore predefinito è 10.

**chToIndexMax**

Lunghezza massima di una stringa da indicizzare. Se ad esempio una colonna ha una lunghezza di 100 caratteri e **chToIndexMax** è impostato su 60, verranno indicizzati solo i primi 60 caratteri della colonna. Il valore predefinito è 32767.

**cchIncrement**

Questo consente di configurare lo stride in base all'indice.

**Windows Vista:** Il membro **cchIncrement** è stato introdotto in Windows Vista. Prima di Windows Vista, la quantità di spostamento della finestra ("stride") era sempre 1, come illustrato nell'esempio nella sezione Osservazioni.

**ichStart**

Offset nel valore per iniziare a recuperare le tuple dal valore.

**Windows Vista:** Il membro **ichStart** è stato introdotto in Windows Vista.

### <a name="remarks"></a>Commenti

Un indice tupla percorre una stringa e indicizza tutte le sottostringhe possibili di **chLengthMax**. Alla fine della stringa (o nella posizione **chToIndexMax**, a seconda di quale si verifichi per primo), le sottostringhe di almeno **chLengthMin** verranno indicizzate.

Un indice tupla può essere utilizzato per la ricerca di stringhe con caratteri jolly iniziali e finali.

Supponendo una riga con un campo di testo "RAIN IN SPAIN \! ", se viene creato un indice di tupla con i parametri **chLengthMin**= 2 e **chLengthMax**= 3, nell'indice vengono create le voci seguenti:

Rai  
Ain  
IN  
"N I"  
IN  
IN  
"N S"  
SP  
Spa  
Pai  
Ain  
"IN \! "  
"N \! "

Si noti che "IN" si verifica due volte e che l'ultima voce ("N \! ") è più corta di 3 (**chLengthMax**). Si noti inoltre che l'algoritmo di suddivisione non è in grado di riconoscere spazi o parole e considera tutti i caratteri in modo identico.

**Windows XP:** Windows XP supporta gli indici di tupla, ma non **JET_TUPLELIMITS**. Il motore di database utilizzerà i valori predefiniti (**chLengthMin**= 3, **chLengthMax**= 10, **chToIndexMax**= 32767). È comunque possibile modificare questi valori, ma vengono impostati per ogni singola istanza usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)e [JET_paramIndexTuplesToIndexMax](./index-parameters.md).

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
