---
title: Uso degli esempi di codice Windows Media Format SDK
description: Uso degli esempi di codice Windows Media Format SDK
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows Media Format SDK, esempi di codice
- Windows Media Format SDK, codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6a5b6718bf7665d04fedb5d5a0bad473a632cbeeabdfd756a52877ccdc84ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963940"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a>Uso degli esempi di codice Windows Media Format SDK

Molte delle sezioni esplicative di questo SDK includono esempi di codice. Gli esempi sono scritti per essere il più chiari e concisi possibile. Quando si leggono gli esempi, è necessario tenere presenti le convenzioni seguenti.

-   Si presuppone che tutti gli esempi includano windows.h e wmsdk.h. Eventuali altri file di intestazione necessari sono indicati nel testo esplicativo.
-   Il controllo degli errori è stato limitato all'interruzione della funzione se si verifica un errore. In un'applicazione è necessario verificare la presenza di codici di errore specifici e fornire un tipo di segnalazione degli errori.

    Quando si controllano i valori restituiti da metodi o funzioni che restituiscono un valore **HRESULT,** è necessario usare la macro **FAILED** per individuare se il valore restituito indica un errore.

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    Molti esempi di questa documentazione usano una macro denominata GOTO \_ EXIT \_ IF \_ FAILED, definita nel codice seguente.

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    Ognuna di queste funzioni di esempio ha un tag denominato "Exit:", dopo il quale vengono rilasciate tutte le interfacce e la memoria allocata nella funzione e viene restituito il codice di errore, se presente.

-   Le interfacce e la memoria vengono rilasciate negli esempi di codice usando macro denominate SAFE \_ RELEASE e SAFE ARRAY \_ \_ DELETE. Queste macro sono definite nel codice seguente:
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

-   Spesso è necessario includere la logica di un esempio in un altro esempio perché l'esempio sia significativo. In questi casi è incluso un commento TODO, con un riferimento all'esempio di codice appropriato.
-   Per semplificare la lettura del codice, nessuna delle funzioni di esempio in questa documentazione convalida i parametri di input. Se si copia una di queste funzioni nel codice, è necessario convalidare tutti i parametri di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività iniziali**](getting-started.md)
</dt> </dl>

 

 




