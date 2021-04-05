---
description: 'Altre informazioni su: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: fe3a8ccd813ececcb42388c7d577f78e9055d5b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751375"
---
# <a name="jet_dbid"></a>JET_DBID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_dbid"></a>JET_DBID

Il tipo di dati **JET_DBID** contiene l'handle per il database. Per gestire lo schema di un database viene utilizzato un handle di database. Può inoltre essere utilizzato per gestire le tabelle all'interno di tale database.

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>Tipi di dati

JET_DBID

Handle per il database.

Il valore JET_dbidNil indica che l'handle non è valido.

### <a name="remarks"></a>Commenti

Un handle di database viene creato tramite una chiamata a [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetOpenDatabase](./jetopendatabase-function.md).

Un handle di database può essere chiuso in modo esplicito da [JetCloseDatabase](./jetclosedatabase-function.md) o chiuso in modo implicito da [JetEndSession](./jetendsession-function.md) o [JetTerm](./jetterm-function.md).

Un handle di database può essere utilizzato solo all'interno della sessione in cui è stato creato. L'esistenza di un handle di database corrisponde all'apertura logica di un database. Una apertura logica è diversa dall'apertura fisica di un database, che si verifica quando un database viene collegato al sistema.

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

[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetEndSession](./jetendsession-function.md)
