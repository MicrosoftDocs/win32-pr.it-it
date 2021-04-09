---
description: 'Altre informazioni su: JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: 6e1fde3e01c8328d2fdaf6609c6772fda9cd1428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968051"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_instance"></a>JET_INSTANCE

Il tipo di dati **JET_INSTANCE** contiene un handle per l'istanza del database da usare per una chiamata all'API Jet.

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>Tipi di dati

JET_INSTANCE

È possibile utilizzare **null** o [JET_instanceNil](./invalid-handle-constants.md) per indicare un handle di istanza non valido.

### <a name="remarks"></a>Commenti

Questo handle viene ottenuto quando si crea un'istanza del database chiamando le funzioni [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)o [JetInit2](./jetinit2-function.md) .

**Windows XP:**  L'utilizzo esplicito di istanze è supportato solo in Windows XP e versioni successive.

**Windows 2000:**  Per ogni processo è supportata una sola istanza globale.

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

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)
