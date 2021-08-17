---
title: Uso degli esempi di codice del client DRM di Microsoft Windows Media
description: Uso degli esempi di codice del client DRM di Microsoft Windows Media
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows Media Format SDK, esempi di codice
- Windows Media Format SDK, codice di esempio
- Windows Sdk di formato multimediale, esempi di codice DRM
- digital rights management (DRM), esempi di codice
- DRM (digital rights management),esempi di codice
- digital rights management (DRM), codice di esempio
- DRM (digital rights management),codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e14ef7e1d003dec8270bb4cfb63d5b4ead7f11751eb94dd09cd771ebd34b3ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704214"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>Uso degli esempi di codice del client DRM di Microsoft Windows Media

In questa documentazione sono inclusi esempi di codice per illustrare l'uso dei componenti. Gli esempi sono scritti per essere il più chiari e concisi possibile. Quando si leggono gli esempi, è necessario tenere presenti le convenzioni seguenti.

-   Si presuppone che tutti gli esempi includano windows.h e wmdrmsdk.h. L'esempio includerà una nota se sono necessarie altre intestazioni per la compilazione.
-   Il controllo degli errori è stato limitato all'interruzione della funzione se si verifica un errore. In un'applicazione è necessario verificare la presenza di codici di errore specifici e fornire un tipo di segnalazione degli errori.
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

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività iniziali**](drm-getting-started.md)
</dt> </dl>

 

 




