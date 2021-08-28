---
description: 'Altre informazioni su: Funzione JetGetInstanceMiscInfo'
title: Funzione JetGetInstanceMiscInfo
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07167dc0f2cad5192dc30e9897541b6619086bfc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481347"
---
# <a name="jetgetinstancemiscinfo-function"></a>Funzione JetGetInstanceMiscInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetinstancemiscinfo-function"></a>Funzione JetGetInstanceMiscInfo

La **funzione JetGetInstanceMiscInfo** recupera informazioni sull'istanza, mentre l'istanza è online.

**Windows Vista: JetGetInstanceMiscInfo** è stato introdotto in Windows Vista.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Identifica l'istanza di database che verrà usata per la chiamata API.

*pvResult*

Puntatore a un buffer che riceverà le informazioni. Il tipo del buffer dipende da *InfoLevel.* Il chiamante è responsabile dell'allineamento appropriato del buffer.

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult.*

*InfoLevel*

Determina il tipo di informazioni che verranno recuperate per l'istanza specificata *dall'istanza di*. Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel.*

Le opzioni seguenti sono disponibili per l'uso con questo parametro.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_InstanceMiscInfoLogSignature</p> | <p><em>pvResult viene</em> interpretato come una <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> della sequenza del log delle transazioni associata a questa istanza.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Buffer troppo piccolo.</p> | 
| <p>JET_errInvalidParameter</p> | <p>È stato specificato <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> valore <em>InfoLevel</em> non valido.</p> | 



#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
