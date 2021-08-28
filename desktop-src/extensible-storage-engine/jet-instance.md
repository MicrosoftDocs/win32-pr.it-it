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
ms.openlocfilehash: 1fc288c17c90070d48669c7ad6f1554d52c83278
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481767"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_instance"></a>JET_INSTANCE

Il **JET_INSTANCE** dati contiene un handle per l'istanza del database da utilizzare per una chiamata all'API JET.

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>Tipi di dati

JET_INSTANCE

È **possibile usare NULL** o [JET_instanceNil](./invalid-handle-constants.md) per indicare un handle di istanza non valido.

### <a name="remarks"></a>Commenti

Questo handle viene ottenuto quando si crea un'istanza del database chiamando le funzioni [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)o [JetInit2.](./jetinit2-function.md)

**Windows XP:**  L'uso esplicito delle istanze è supportato solo in Windows XP e versioni successive.

**Windows 2000:**  È supportata una sola istanza globale per processo.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)
