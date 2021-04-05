---
description: 'Altre informazioni su: funzione JetGetInstanceInfo'
title: JetGetInstanceInfo (funzione)
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883469"
---
# <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo (funzione)

La funzione **JetGetInstanceInfo** recupera le informazioni sulle istanze in esecuzione.

**Windows XP: JetGetInstanceInfo** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>Parametri

*pcInstanceInfo*

Puntatore a un buffer che riceverà il numero di elementi archiviati in *paInstanceInfo*.

*paInstanceInfo*

Puntatore a un buffer che riceverà l'indirizzo del primo elemento di una matrice di strutture.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo errore viene restituito da <strong>JetGetInstanceInfo</strong> quando:</p>
<ul>
<li><p><em>pcInstanceInfo</em> o <em>paInstanceInfo</em> sono null.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Memoria insufficiente per elaborare la richiesta.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Tramite il motore di database viene allocata una matrice di strutture di [JET_INSTANCE_INFO](./jet-instance-info-structure.md) . Il chiamante è responsabile della liberazione della memoria con [JetFreeBuffer](./jetfreebuffer-function.md).

Se non sono presenti istanze attive, **JetGetInstanceInfo** restituirà JET_errSuccess e *pcInstanceInfo* riceverà un valore pari a 0.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetGetInstanceInfoW</strong> (Unicode) e <strong>JetGetInstanceInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)
