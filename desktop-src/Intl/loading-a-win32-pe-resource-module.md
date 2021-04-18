---
description: Questo argomento descrive il modo in cui l'applicazione carica un modulo di risorse PE Win32 in Windows Vista e versioni successive o in un sistema operativo precedente. Sono incluse chiamate per il rilascio del modulo della risorsa.
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: Caricamento di un modulo di risorse PE Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c4c1906a4fc09dc39b805e8ad5a875d96fae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319493"
---
# <a name="loading-a-win32-pe-resource-module"></a>Caricamento di un modulo di risorse PE Win32

Questo argomento descrive il modo in cui l'applicazione carica un modulo di risorse PE Win32 in Windows Vista e versioni successive o in un sistema operativo precedente. Sono incluse chiamate per il rilascio del modulo della risorsa.

## <a name="load-the-resource-module-on-windows-vista-and-later"></a>Caricare il modulo Resource in Windows Vista e versioni successive

In Windows Vista e versioni successive, l'applicazione carica il modulo Resource usando una chiamata a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa). L'operazione consigliata consiste nel chiamare questa funzione con entrambi i flag specificati. Di seguito è riportato un esempio di codice dell'applicazione che carica un modulo in base alle impostazioni della lingua del sistema.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a>Caricare il modulo Resource nei sistemi operativi precedenti a Windows Vista

Nei sistemi operativi precedenti a Windows Vista, l'applicazione carica un modulo di risorse in base a un'impostazione della lingua compatibile con il sistema operativo di destinazione, nonché Windows Vista e versioni successive. Per questo tipo di caricamento del modulo, l'applicazione deve chiamare le funzioni MUI [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).


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

[Esempio di impostazioni di MUI: Application-Specific (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[Esempio di impostazioni di MUI: Application-Specific (precedente a Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
