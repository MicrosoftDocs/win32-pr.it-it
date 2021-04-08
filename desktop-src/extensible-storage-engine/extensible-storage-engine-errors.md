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
# <a name="extensible-storage-engine-errors"></a><span data-ttu-id="1e394-103">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="1e394-103">Extensible Storage Engine Errors</span></span>


<span data-ttu-id="1e394-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1e394-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-errors"></a><span data-ttu-id="1e394-105">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="1e394-105">Extensible Storage Engine Errors</span></span>

<span data-ttu-id="1e394-106">Tutti i possibili errori restituiti dall'API Extensible Storage Engine (ESE) sono definiti dal tipo di dati [JET_ERR](./jet-err.md) .</span><span class="sxs-lookup"><span data-stu-id="1e394-106">All possible errors returned by the Extensible Storage Engine (ESE) API are defined by the [JET_ERR](./jet-err.md) data type.</span></span> <span data-ttu-id="1e394-107">Per un elenco dei flag di errore definiti per questa API, vedere codici di [errore del motore di archiviazione estendibile](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1e394-107">For a list of the error flags that are defined for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="1e394-108">In tutta la documentazione dell'API ESE vengono documentati solo gli errori più importanti.</span><span class="sxs-lookup"><span data-stu-id="1e394-108">Throughout the ESE API documentation, only the most important errors are documented.</span></span> <span data-ttu-id="1e394-109">Questi errori rappresentano in genere errori di utilizzo dell'API o condizioni di errore molto importanti.</span><span class="sxs-lookup"><span data-stu-id="1e394-109">These errors typically represent API usage errors or very important error conditions.</span></span> <span data-ttu-id="1e394-110">Tenere presente che qualsiasi API ESE può restituire anche altri errori non documentati per ogni API.</span><span class="sxs-lookup"><span data-stu-id="1e394-110">Be aware that any of these ESE APIs can also return other errors that are not documented for each API.</span></span> <span data-ttu-id="1e394-111">In questi casi, il chiamante deve semplicemente gestire l'errore come per qualsiasi altro errore restituito dall'API.</span><span class="sxs-lookup"><span data-stu-id="1e394-111">In these cases, the caller should simply handle the error as they would any other error that is returned by the API.</span></span> <span data-ttu-id="1e394-112">Il valore di errore specifico può quindi essere utilizzato per scopi diagnostici, ad esempio la traccia.</span><span class="sxs-lookup"><span data-stu-id="1e394-112">The specific error value may then be used for diagnostic purposes such as tracing.</span></span>

<span data-ttu-id="1e394-113">In generale, un valore maggiore di zero deve essere interpretato come un avviso, un valore pari a zero deve essere interpretato come esito positivo e un valore minore di zero deve essere interpretato come un errore.</span><span class="sxs-lookup"><span data-stu-id="1e394-113">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="1e394-114">Nessun altro criterio in questi valori (ad esempio, intervalli di valori) deve essere considerato attendibile da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e394-114">No other patterns in these values (for example, ranges of values) should be relied upon by an application.</span></span>

<span data-ttu-id="1e394-115">Quando ESE rileva alcuni degli errori più gravi, viene creata una voce del registro eventi che contiene i dettagli sugli errori.</span><span class="sxs-lookup"><span data-stu-id="1e394-115">When ESE encounters some of the more serious errors, it creates an event log entry that contains details about the errors.</span></span> <span data-ttu-id="1e394-116">Il livello di registrazione può essere controllato dai [parametri del registro eventi](./event-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1e394-116">The level of logging can be controlled by [Event Log Parameters](./event-log-parameters.md).</span></span>

<span data-ttu-id="1e394-117">Alcune applicazioni richiedono la possibilità di restituire [JET_ERR](./jet-err.md)s come HRESULT.</span><span class="sxs-lookup"><span data-stu-id="1e394-117">Some applications require the ability to return [JET_ERR](./jet-err.md)s as HRESULTs.</span></span> <span data-ttu-id="1e394-118">Nell'esempio C++ riportato di seguito viene illustrato come eseguire la conversione:</span><span class="sxs-lookup"><span data-stu-id="1e394-118">The following C++ example shows how to make that conversion:</span></span>

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

<span data-ttu-id="1e394-119">Per informazioni sulla configurazione dei parametri di sistema per la gestione degli errori, vedere [parametri di gestione degli errori](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1e394-119">For information about configuring system parameters for error handling, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="see-also"></a><span data-ttu-id="1e394-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1e394-120">See Also</span></span>

[<span data-ttu-id="1e394-121">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="1e394-121">Error Handling Parameters</span></span>](./error-handling-parameters.md)

[<span data-ttu-id="1e394-122">Codici di errore di Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="1e394-122">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)

[<span data-ttu-id="1e394-123">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1e394-123">JET_ERR</span></span>](./jet-err.md)
