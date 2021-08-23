---
description: 'Altre informazioni su: Extensible Archiviazione Engine Errors'
title: Errori del motore Archiviazione estendibile
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 0c0ee0a4423d5b37913bd7922af07a7b2196a30176b2a1adca37240e03a28594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721461"
---
# <a name="extensible-storage-engine-errors"></a>Errori del motore Archiviazione estendibile


_**Si applica a:** Windows | Windows Server_

## <a name="extensible-storage-engine-errors"></a>Errori del motore Archiviazione estendibile

Tutti i possibili errori restituiti dall'API Extensible Archiviazione Engine (ESE) sono definiti dal [tipo JET_ERR](./jet-err.md) dati. Per un elenco dei flag di errore definiti per questa API, vedere [Extensible Archiviazione Engine Error Codes](./extensible-storage-engine-error-codes.md).

Nella documentazione dell'API ESE sono documentati solo gli errori più importanti. Questi errori rappresentano in genere errori di utilizzo dell'API o condizioni di errore molto importanti. Tenere presente che una qualsiasi di queste API ESE può restituire anche altri errori non documentati per ogni API. In questi casi, il chiamante deve semplicemente gestire l'errore come qualsiasi altro errore restituito dall'API. Il valore di errore specifico può quindi essere usato per scopi diagnostici, ad esempio la traccia.

In generale, un valore maggiore di zero deve essere interpretato come un avviso, il valore zero deve essere interpretato come esito positivo e un valore minore di zero deve essere interpretato come un errore. Nessun altro modello in questi valori (ad esempio, intervalli di valori) deve essere basato su un'applicazione.

Quando ESE rileva alcuni degli errori più gravi, crea una voce del registro eventi che contiene i dettagli sugli errori. Il livello di registrazione può essere controllato dai [parametri del registro eventi](./event-log-parameters.md).

Alcune applicazioni richiedono la possibilità di [restituire JET_ERR](./jet-err.md)come HRESULT. L'esempio C++ seguente mostra come eseguire la conversione:

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

Per informazioni sulla configurazione dei parametri di sistema per la gestione degli errori, vedere [Parametri di gestione degli errori.](./error-handling-parameters.md)

### <a name="see-also"></a>Vedere anche

[Parametri di gestione degli errori](./error-handling-parameters.md)

[Codici di errore del Archiviazione estendibile](./extensible-storage-engine-error-codes.md)

[JET_ERR](./jet-err.md)
