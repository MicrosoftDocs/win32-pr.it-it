---
description: Caricamento delle risorse della lingua
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Caricamento delle risorse della lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eebf027476658872fe392fe60699da1a586f9297f39a191898b1e132439962c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106931"
---
# <a name="loading-language-resources"></a>Caricamento delle risorse della lingua

L'applicazione carica tutte le risorse della lingua dell'interfaccia utente, diverse da determinate stringhe del Registro di sistema reindirizzate, usando chiamate alle funzioni di caricamento delle risorse standard, ad esempio [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)e [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea). Molte funzioni di caricamento delle risorse sono state modificate per caricare automaticamente le risorse dai file di risorse specifici della lingua, trattando le risorse come se fossero contenute nel file LN. L'esempio seguente illustra l'uso di **LoadString per caricare** stringhe di lingua per un'applicazione che segue le impostazioni della lingua di sistema.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Individuazione delle risorse PE Win32](locating-win32-pe-resources.md)
</dt> </dl>

 

 
