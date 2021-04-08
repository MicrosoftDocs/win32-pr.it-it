---
description: 'Altre informazioni su: errori del motore di archiviazione estendibile'
title: Errori del motore di archiviazione estendibile
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 55c86d51f44414688897d6450adf214a0478f7d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885610"
---
# <a name="extensible-storage-engine-errors"></a>Errori del motore di archiviazione estendibile


_**Si applica a:** Windows | Windows Server_

## <a name="extensible-storage-engine-errors"></a>Errori del motore di archiviazione estendibile

Tutti i possibili errori restituiti dall'API Extensible Storage Engine (ESE) sono definiti dal tipo di dati [JET_ERR](./jet-err.md) . Per un elenco dei flag di errore definiti per questa API, vedere codici di [errore del motore di archiviazione estendibile](./extensible-storage-engine-error-codes.md).

In tutta la documentazione dell'API ESE vengono documentati solo gli errori più importanti. Questi errori rappresentano in genere errori di utilizzo dell'API o condizioni di errore molto importanti. Tenere presente che qualsiasi API ESE può restituire anche altri errori non documentati per ogni API. In questi casi, il chiamante deve semplicemente gestire l'errore come per qualsiasi altro errore restituito dall'API. Il valore di errore specifico può quindi essere utilizzato per scopi diagnostici, ad esempio la traccia.

In generale, un valore maggiore di zero deve essere interpretato come un avviso, un valore pari a zero deve essere interpretato come esito positivo e un valore minore di zero deve essere interpretato come un errore. Nessun altro criterio in questi valori (ad esempio, intervalli di valori) deve essere considerato attendibile da un'applicazione.

Quando ESE rileva alcuni degli errori più gravi, viene creata una voce del registro eventi che contiene i dettagli sugli errori. Il livello di registrazione può essere controllato dai [parametri del registro eventi](./event-log-parameters.md).

Alcune applicazioni richiedono la possibilità di restituire [JET_ERR](./jet-err.md)s come HRESULT. Nell'esempio C++ riportato di seguito viene illustrato come eseguire la conversione:

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

Per informazioni sulla configurazione dei parametri di sistema per la gestione degli errori, vedere [parametri di gestione degli errori](./error-handling-parameters.md).

### <a name="see-also"></a>Vedere anche

[Parametri di gestione degli errori](./error-handling-parameters.md)

[Codici di errore di Extensible Storage Engine](./extensible-storage-engine-error-codes.md)

[JET_ERR](./jet-err.md)
