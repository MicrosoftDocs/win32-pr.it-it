---
description: 'Altre informazioni su: funzione JET_PFNREALLOC callback'
title: JET_PFNREALLOC di callback
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: f7427a28752384f6c30e050458e5844dcaedd1a7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989144"
---
# <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC di callback


_**Si applica a:** Windows | Windows Server_

## <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC di callback

La JET_PFNREALLOC è un callback compatibile con [riallocare](/cpp/c-runtime-library/reference/realloc?view=vs-2019) usato [da JetEnumerateColumns](./jetenumeratecolumns-function.md) per allocare memoria per i buffer di output.

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>Parametri

*pvContext*

Puntatore di contesto assegnato [a JetEnumerateColumns.](./jetenumeratecolumns-function.md) Questo puntatore di contesto può essere usato per trasmettere lo stato dal [chiamante di JetEnumerateColumns](./jetenumeratecolumns-function.md) all'implementazione di questo callback.

*Pv*

Se diverso da NULL, specifica un puntatore a un blocco di memoria allocato in precedenza da questo callback. Se NULL, verrà allocato un nuovo blocco di memoria delle dimensioni richieste.

*Cb*

Nuova dimensione in byte del blocco di memoria. Se questo parametro è 0 (zero) e viene specificato un blocco di memoria, tale blocco di memoria verrà liberato.

### <a name="return-value"></a>Valore restituito

Il sistema può generare codici di esito positivo o negativo in seguito a una chiamata a questa funzione. Per informazioni su come restituire questi codici come HRESULT, vedere Errori del motore Archiviazione [estendibile](./extensible-storage-engine-errors.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>Operazione completata</p> | <p>Se è stato specificato un blocco di memoria allocato in precedenza ed è stata specificata una nuova dimensione pari a zero, tale blocco viene liberato e verrà restituito NULL. Se è stato specificato un blocco di memoria allocato in precedenza ed è stata specificata una nuova dimensione diverso da zero, viene restituito il blocco di memoria riallocato. Se non è stato specificato alcun blocco di memoria, viene restituito un blocco di memoria appena allocato delle dimensioni specificate.</p> | 
| <p>Operazioni non riuscite</p> | <p>Verrà restituito NULL. Se è stato fornito un blocco di memoria allocato in precedenza, tale blocco rimarrà allocato.</p> | 



### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetEnumerateColumns](./jetenumeratecolumns-function.md)
