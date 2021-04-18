---
title: Uso degli esempi di codice client DRM di Microsoft Windows Media
description: Uso degli esempi di codice client DRM di Microsoft Windows Media
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows Media Format SDK, esempi di codice
- Windows Media Format SDK, esempio di codice
- Windows Media Format SDK, esempi di codice DRM
- Digital Rights Management (DRM), esempi di codice
- DRM (Digital Rights Management), esempi di codice
- Digital Rights Management (DRM), codice di esempio
- DRM (Digital Rights Management), codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 054d1ed804873c8aca104203ee1f235ecb3856f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400067"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>Uso degli esempi di codice client DRM di Microsoft Windows Media

Gli esempi di codice sono inclusi in questa documentazione per illustrare l'utilizzo dei componenti di. Gli esempi sono scritti nel modo più chiaro e conciso possibile. Quando si leggono gli esempi, è necessario tenere presente le convenzioni seguenti.

-   Si presuppone che tutti gli esempi includano Windows. h e wmdrmsdk. h. Nell'esempio sarà inclusa una nota se sono necessarie altre intestazioni per la compilazione.
-   Se si verifica un errore, il controllo degli errori è stato limitato alla suddivisione della funzione. In un'applicazione, è necessario verificare la presenza di codici di errore specifici e fornire un tipo di segnalazione degli errori.
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

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Introduzione**](drm-getting-started.md)
</dt> </dl>

 

 




