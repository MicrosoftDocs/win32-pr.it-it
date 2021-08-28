---
description: 'Altre informazioni su: Funzione JetGetInstanceInfo'
title: Funzione JetGetInstanceInfo
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
ms.openlocfilehash: 9dfc8bec0e6cee6e127dc99135d82db3ee3001ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478347"
---
# <a name="jetgetinstanceinfo-function"></a>Funzione JetGetInstanceInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetinstanceinfo-function"></a>Funzione JetGetInstanceInfo

La **funzione JetGetInstanceInfo** recupera informazioni sulle istanze in esecuzione.

**Windows XP: JetGetInstanceInfo** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>Parametri

*pcInstanceInfo*

Puntatore a un buffer che riceverà il numero di elementi archiviati in *paInstanceInfo.*

*paInstanceInfo*

Puntatore a un buffer che riceverà l'indirizzo del primo elemento di una matrice di strutture .

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo errore verrà restituito da <strong>JetGetInstanceInfo</strong> quando:</p><ul><li><p><em>pcInstanceInfo</em> o <em>paInstanceInfo</em> sono NULL.</p></li></ul> | 
| <p>JET_errOutOfMemory</p> | <p>Memoria insufficiente per elaborare la richiesta.</p> | 



#### <a name="remarks"></a>Commenti

Il motore di database alloca una matrice [JET_INSTANCE_INFO](./jet-instance-info-structure.md) strutture. Il chiamante è responsabile del liberare la memoria con [JetFreeBuffer](./jetfreebuffer-function.md).

Se non sono presenti istanze attive, **JetGetInstanceInfo** restituirà JET_errSuccess e *pcInstanceInfo* riceverà il valore 0.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetGetInstanceInfoW</strong> (Unicode) e <strong>JetGetInstanceInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)
