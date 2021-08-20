---
description: Questo argomento descrive come l'applicazione carica un modulo di risorse PE Win32 in Windows Vista e versioni successive o in un sistema operativo precedente. Sono incluse chiamate per rilasciare il modulo della risorsa.
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: Caricamento di un modulo di risorse PE Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: affcd1cf582d81aafd70f208531e03723ea44b314f92848f35dfd391f950b0ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145843"
---
# <a name="loading-a-win32-pe-resource-module"></a>Caricamento di un modulo di risorse PE Win32

Questo argomento descrive come l'applicazione carica un modulo di risorse PE Win32 in Windows Vista e versioni successive o in un sistema operativo precedente. Sono incluse chiamate per rilasciare il modulo della risorsa.

## <a name="load-the-resource-module-on-windows-vista-and-later"></a>Caricare il modulo risorse in Windows Vista e versioni successive

In Windows Vista e versioni successive, l'applicazione carica il modulo delle risorse usando una chiamata a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa) L'operazione consigliata è chiamare questa funzione con entrambi i flag specificati. Di seguito è riportato un esempio di codice dell'applicazione che carica un modulo in base alle impostazioni della lingua di sistema.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a>Caricare il modulo delle risorse nei sistemi operativi Windows Vista pre-installato

Nei sistemi operativi Windows Vista pre-installato, l'applicazione carica un modulo di risorse in base a un'impostazione della lingua compatibile con il sistema operativo di destinazione, nonché Windows Vista e versioni successive. Per questo tipo di caricamento del modulo, l'applicazione deve chiamare le funzioni [**MUI LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) [**e FreeMUILibrary.**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Individuazione delle risorse PE Win32](locating-win32-pe-resources.md)
</dt> <dt>

[MUI: Application-Specific Impostazioni esempio (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI: Application-Specific Impostazioni esempio (pre-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
