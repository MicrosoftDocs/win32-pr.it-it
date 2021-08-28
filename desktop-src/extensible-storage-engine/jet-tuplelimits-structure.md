---
description: 'Altre informazioni su: JET_TUPLELIMITS Structure'
title: JET_TUPLELIMITS struttura
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
ms.openlocfilehash: 7155763f68a74333fc71db1054fb0ecffcca862e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983764"
---
# <a name="jet_tuplelimits-structure"></a>JET_TUPLELIMITS struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_tuplelimits-structure"></a>JET_TUPLELIMITS struttura

La **JET_TUPLELIMITS** consente la personalizzazione delle caratteristiche dell'indice di tupla in base all'indice, anziché in base all'istanza, usando [JetSetSystemParameter](./jetsetsystemparameter-function.md).

**Windows Server 2003:** La **JET_TUPLELIMITS** è stata introdotta in Windows Server 2003.

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

Lunghezza massima di una stringa da indicizzare. Ad esempio, se una colonna ha una lunghezza di 100 caratteri e **chToIndexMax** è impostato su 60, verranno indicizzati solo i primi 60 caratteri della colonna. Il valore predefinito è 32767.

**cchIncrement**

Ciò consente di configurare lo stride in base all'indice.

**Windows Vista:** Il **membro cchIncrement** è stato introdotto in Windows Vista. Prima di Windows Vista, la quantità di spostamento della finestra (lo "stride") era sempre 1, come illustrato nell'esempio nella sezione osservazioni.

**ichStart**

Offset nel valore per iniziare a recuperare le tuple dal valore.

**Windows Vista:** Il **membro ichStart** è stato introdotto in Windows Vista.

### <a name="remarks"></a>Commenti

Un indice di tupla illustra una stringa e indicizza tutte le possibili sottostringhe di **chLengthMax.** Alla fine della stringa (o nella posizione **chToIndexMax,** a seconda di quale si verifica per prima), le sottostringhe di **almeno chLengthMin** verranno indicizzate.

Un indice di tupla può essere usato per la ricerca di stringhe con caratteri jolly iniziali e finali.

Supponendo che una riga con un campo di testo "RAIN IN SPAIN" venga creata con i parametri \! **chLengthMin**=2 e **chLengthMax**=3, nell'indice vengono create le voci seguenti:

"RAI"  
"AIN"  
"IN "  
"N I"  
"IN"  
"IN "  
"N S"  
"SP"  
"SPA"  
"PAI"  
"AIN"  
"IN \! "  
"N \! "

Si noti che "IN" si verifica due volte e che l'ultima voce ("N ") è minore di \! 3 (**chLengthMax**). Si noti anche che l'algoritmo di suddivisione non è a conoscenza di spazi o parole e considera tutti i caratteri in modo identico.

**Windows XP:** Windows XP supporta gli indici di tupla, ma non **dispone di JET_TUPLELIMITS**. Il motore di database usa i valori predefiniti (**chLengthMin**=3, **chLengthMax**=10, **chToIndexMax**=32767). È comunque possibile modificare questi valori, ma vengono impostati per ogni istanza usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)e [JET_paramIndexTuplesToIndexMax](./index-parameters.md).

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
