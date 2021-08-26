---
description: 'Altre informazioni su: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f341f88a192fee6de55e0077778abde83493e35e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482277"
---
# <a name="jet_err"></a>JET_ERR


_**Si applica a:** Windows | Windows Server_

## <a name="jet_err"></a>JET_ERR

Il **JET_ERR** di dati contiene un codice di [errore extensible Archiviazione Engine](./extensible-storage-engine-error-codes.md).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Tipi di dati

JET_ERR

Un valore zero (corrispondente a JET_errSuccess) indica che la chiamata ha avuto esito positivo. Un valore positivo avvisa di una condizione non irreversibile che si è verificata durante una chiamata altrimenti riuscita. Un valore negativo indica che la chiamata non è riuscita.

### <a name="remarks"></a>Commenti

Per informazioni sulla restituzione di errori come HRESULT, vedere Errori del motore di [Archiviazione estendibile](./extensible-storage-engine-errors.md). Per informazioni sui flag per la configurazione del database per la gestione degli errori, vedere [Parametri di gestione degli errori](./error-handling-parameters.md).

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[Errori del motore Archiviazione estendibile](./extensible-storage-engine-errors.md)  
[Codici di errore del motore Archiviazione estendibile](./extensible-storage-engine-error-codes.md)  
[Parametri di gestione degli errori](./error-handling-parameters.md)
