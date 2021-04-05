---
description: 'Altre informazioni su: struttura JET_ERRINFOBASIC_W'
title: Struttura JET_ERRINFOBASIC_W
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103969534"
---
# <a name="jet_errinfobasic_w-structure"></a>Struttura JET_ERRINFOBASIC_W


_**Si applica a:** Windows | Windows Server_

## <a name="jet_errinfobasic_w-structure"></a>Struttura JET_ERRINFOBASIC_W

La struttura **JET_ERRINFOBASIC_W** definisce i dati restituiti dal metodo [JetGetErrorInfo ()](./jetgeterrorinfow-function.md) quando il JET_ErrorInfoSpecificErr InfoLevel viene passato.

Nota: questa documentazione si basa su una versione preliminare del motore di archiviazione estendibile. Queste informazioni sono soggette a modifiche.

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

Dimensioni, in byte, della struttura. Deve essere impostato su sizeof (JET_ERRINFOBASIC).

**errValue**

Valore di errore valutato, come passato per l'argomento *pvResult* a [JetGetErrorInfo ()](./jetgeterrorinfow-function.md).

**errcatMostSpecific**

Costante [JET_ERRCAT](./jet-errcat.md) di livello più basso associata all'errore. ovvero la categoria a livello foglia nella gerarchia delle categorie documentata in [JET_ERRCAT](./jet-errcat.md).

**rgCategoricalHierarchy \[ 8\]**

Gerarchia delle categorie di errore associata all'errore. La posizione 0 è il livello più alto nella gerarchia di [JET_ERRCAT](./jet-errcat.md)e le altre sono sottocategorie fino a quando non viene impostata la categoria più specifica, dopo le quali vengono JET_errcatUnknown tutte le categorie.

**lSourceLine**

Riservato.

**rgszSourceFile \[ 64\]**

Riservato.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>
