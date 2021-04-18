---
title: Uso degli esempi di codice di Windows Media Format SDK
description: Uso degli esempi di codice di Windows Media Format SDK
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows Media Format SDK, esempi di codice
- Windows Media Format SDK, esempio di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db438a8cb42bbb45768421cc34c129f19948f1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400187"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a>Uso degli esempi di codice di Windows Media Format SDK

Molte delle sezioni esplicative di questo SDK includono esempi di codice. Gli esempi sono scritti nel modo più chiaro e conciso possibile. Quando si leggono gli esempi, è necessario tenere presente le convenzioni seguenti.

-   Si presuppone che tutti gli esempi includano Windows. h e WMSDK. h. Tutti gli altri file di intestazione obbligatori sono indicati nel testo esplicativo.
-   Se si verifica un errore, il controllo degli errori è stato limitato alla suddivisione della funzione. In un'applicazione, è necessario verificare la presenza di codici di errore specifici e fornire un tipo di segnalazione degli errori.

    Quando si controllano i valori restituiti dai metodi o dalle funzioni che restituiscono un valore **HRESULT** , è necessario usare la macro **failed** per individuare se il valore restituito indica un errore.

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    Molti degli esempi in questa documentazione usano una macro denominata GOTO \_ Exit \_ se \_ failed, definita nel codice seguente.

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    Ognuna di queste funzioni di esempio ha un tag denominato "Exit:", dopo il quale vengono rilasciate tutte le interfacce e la memoria allocata nella funzione e viene restituito il codice di errore, se disponibile.

-   Le interfacce e la memoria vengono rilasciate negli esempi di codice che usano le macro denominate SAFE \_ release e Safe \_ array \_ Delete. Queste macro sono definite nel codice seguente:
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

    

-   Spesso è necessario includere la logica di un esempio in un altro esempio perché l'esempio sia significativo. In tali casi, viene incluso un commento TODO con un riferimento all'esempio di codice appropriato.
-   Per semplificare la lettura del codice, nessuna delle funzioni di esempio in questa documentazione convalida i relativi parametri di input. Se si copia una di queste funzioni nel codice, è necessario convalidare i parametri di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Introduzione**](getting-started.md)
</dt> </dl>

 

 




