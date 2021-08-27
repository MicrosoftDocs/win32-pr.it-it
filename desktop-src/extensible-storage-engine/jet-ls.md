---
description: 'Altre informazioni su: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 82a0df37215122e943955f32aeed4d39dd70b268
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983154"
---
# <a name="jet_ls"></a>JET_LS


_**Si applica a:** Windows | Windows Server_

## <a name="jet_ls"></a>JET_LS

Il **JET_LS** dati contiene un handle di contesto per l'archiviazione locale (LS). Questo handle può essere associato a un cursore o a una tabella e può fare riferimento a risorse allocate dinamicamente.

**Windows XP: JET_LS** è stato introdotto in Windows XP.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Tipi di dati

JET_LS

Il valore JET_LSNil indica un handle di contesto non valido.

### <a name="remarks"></a>Commenti

Un handle di contesto viene inizialmente associato al **tipo JET_LS** dati, usando [JetSetLS](./jetsetls-function.md). L'handle di contesto può essere recuperato dal **tipo JET_LS** dati, usando [JetGetLS](./jetgetls-function.md).

L'handle di contesto può essere dissociato in modo esplicito dal tipo di dati JET_LS [tramite JetGetLS](./jetgetls-function.md) con JET_bitLSReset.  In alternativa, l'handle di contesto può essere dissociato in modo implicito dal tipo di dati JET_LS quando l'oggetto sottostante viene rilasciato dal motore di database **come** risultato di un'azione diretta o indiretta da parte dell'applicazione. Nel caso implicito, viene eseguito un callback di runtime per l'applicazione in modo che possa pulire l'handle di contesto. Per altre informazioni sulla dissociazione implicita dal tipo JET_LS dati, vedere [JetSetLS](./jetsetls-function.md). 

I flag seguenti sono associati al tipo JET_LS dati.


| <p>Termine</p> | <p>Descrizione</p> | 
|-------------|--------------------|
| <p>JET_bitLSReset</p> | <p>L'handle di contesto viene dissociato dall'oggetto .</p> | 
| <p>JET_bitLSCursor</p> | <p>Impostare o recuperare l'archiviazione locale associata a un cursore di tabella.</p> | 
| <p>JET_bitLSTable</p> | <p>Impostare o recuperare l'archiviazione locale associata a una tabella.</p> | 
| <p>JET_LSNil</p> | <p>L'handle di contesto non è valido.</p> | 



### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)
