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
ms.openlocfilehash: c576734a3e2da71f041509e5b7d7d9244427dbb8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986694"
---
# <a name="jet_dbid"></a>JET_DBID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_dbid"></a>JET_DBID

Il **JET_DBID** dati contiene l'handle per il database. Un handle di database viene usato per gestire lo schema di un database. Può essere usato anche per gestire le tabelle all'interno di tale database.

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>Tipi di dati

JET_DBID

Handle per il database.

Il valore JET_dbidNil indica che l'handle non è valido.

### <a name="remarks"></a>Commenti

Un handle di database viene creato tramite una chiamata a [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetOpenDatabase](./jetopendatabase-function.md).

Un handle di database può essere chiuso in modo [esplicito da JetCloseDatabase](./jetclosedatabase-function.md) o in modo implicito da [JetEndSession](./jetendsession-function.md) o [JetTerm.](./jetterm-function.md)

Un handle di database può essere utilizzato solo all'interno della sessione in cui è stato creato. L'esistenza di un handle di database corrisponde all'apertura logica di un database. Un'apertura logica è diversa dall'apertura fisica di un database, che si verifica quando un database è collegato al sistema.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetEndSession](./jetendsession-function.md)
