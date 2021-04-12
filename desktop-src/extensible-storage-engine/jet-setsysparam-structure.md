---
description: 'Altre informazioni su: struttura JET_SETSYSPARAM'
title: Struttura JET_SETSYSPARAM
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342991"
---
# <a name="jet_setsysparam-structure"></a>Struttura JET_SETSYSPARAM


_**Si applica a:** Windows | Windows Server_

## <a name="jet_setsysparam-structure"></a>Struttura JET_SETSYSPARAM

Una matrice di strutture di **JET_SETSYSPARAM** indica un set specifico di parametri di sistema globale impostati come argomento quando si utilizza la funzione [JetEnableMultiInstance](./jetenablemultiinstance-function.md) .

**Windows XP:** Questa struttura è stata introdotta in Windows XP.

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a>Membri

**paramid**

ID del parametro di sistema che verrà impostato.

Vedere [parametri di sistema Extensible Storage Engine](./extensible-storage-engine-system-parameters.md) per un elenco completo dei parametri di sistema e delle rispettive proprietà.

**lParam**

Valore facoltativo da impostare per il parametro di sistema selezionato se il parametro di sistema è di tipo Integer.

**SZ**

Valore facoltativo da impostare per il parametro di sistema selezionato se tale parametro di sistema è di tipo String.

**Err**

Errore risultante dalla chiamata a [JetSetSystemParameter](./jetsetsystemparameter-function.md) con i parametri specificati in precedenza.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JET_ SETSYSPARAM_W</strong> (Unicode) e <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[Parametri di sistema Extensible Storage Engine](./extensible-storage-engine-system-parameters.md)  
[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
