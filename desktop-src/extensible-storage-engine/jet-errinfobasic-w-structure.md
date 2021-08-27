---
description: 'Altre informazioni su: JET_ERRINFOBASIC_W struttura'
title: JET_ERRINFOBASIC_W struttura
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: c02d9f8081040293bd154137163e13cc9d313a32
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984034"
---
# <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W struttura

La **JET_ERRINFOBASIC_W** definisce i dati restituiti dal metodo [JetGetErrorInfo()](./jetgeterrorinfow-function.md) quando viene passato JET_ErrorInfoSpecificErr InfoLevel.

Nota: questa documentazione si basa su una versione preliminare di Extensible Archiviazione Engine. Queste informazioni sono soggette a modifiche.

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni della struttura, in byte. Deve essere impostato su sizeof( JET_ERRINFOBASIC ).

**errValue**

Valore di errore valutato, come passato per *l'argomento pvResult* [a JetGetErrorInfo().](./jetgeterrorinfow-function.md)

**errcatMostSpecific**

Costante di livello [più JET_ERRCAT](./jet-errcat.md) associata all'errore. ciò significa che la categoria a livello foglia nella gerarchia di categorie documentata in [JET_ERRCAT](./jet-errcat.md).

**rgCategoricalHierarchy \[ 8\]**

Gerarchia delle categorie di errore associata all'errore. La posizione 0 è il livello più alto nella gerarchia di [JET_ERRCAT](./jet-errcat.md)e le altre sono sottocategorie fino a quando non viene impostata la categoria più specifica, dopo la quale tutte le categorie vengono JET_errcatUnknown.

**lSourceLine**

Riservato.

**rgszSourceFile \[ 64\]**

Riservato.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows 8 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 

