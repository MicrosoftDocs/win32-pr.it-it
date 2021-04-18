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
# <a name="loading-a-win32-pe-resource-module"></a><span data-ttu-id="adc6e-104">Caricamento di un modulo di risorse PE Win32</span><span class="sxs-lookup"><span data-stu-id="adc6e-104">Loading a Win32 PE Resource Module</span></span>

<span data-ttu-id="adc6e-105">Questo argomento descrive il modo in cui l'applicazione carica un modulo di risorse PE Win32 in Windows Vista e versioni successive o in un sistema operativo precedente.</span><span class="sxs-lookup"><span data-stu-id="adc6e-105">This topic describes how the application loads a Win32 PE resource module on either Windows Vista and later or on an earlier operating system.</span></span> <span data-ttu-id="adc6e-106">Sono incluse chiamate per il rilascio del modulo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="adc6e-106">Calls are included for releasing the resource module.</span></span>

## <a name="load-the-resource-module-on-windows-vista-and-later"></a><span data-ttu-id="adc6e-107">Caricare il modulo Resource in Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="adc6e-107">Load the Resource Module on Windows Vista and Later</span></span>

<span data-ttu-id="adc6e-108">In Windows Vista e versioni successive, l'applicazione carica il modulo Resource usando una chiamata a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span><span class="sxs-lookup"><span data-stu-id="adc6e-108">On Windows Vista and later, the application loads the resource module using a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span> <span data-ttu-id="adc6e-109">L'operazione consigliata consiste nel chiamare questa funzione con entrambi i flag specificati.</span><span class="sxs-lookup"><span data-stu-id="adc6e-109">The recommended operation is to call this function with both flags specified.</span></span> <span data-ttu-id="adc6e-110">Di seguito è riportato un esempio di codice dell'applicazione che carica un modulo in base alle impostazioni della lingua del sistema.</span><span class="sxs-lookup"><span data-stu-id="adc6e-110">The following is an example of application code that loads a module based on system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="adc6e-111">Caricare il modulo Resource nei sistemi operativi precedenti a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="adc6e-111">Load the Resource Module on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="adc6e-112">Nei sistemi operativi precedenti a Windows Vista, l'applicazione carica un modulo di risorse in base a un'impostazione della lingua compatibile con il sistema operativo di destinazione, nonché Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="adc6e-112">On pre-Windows Vista operating systems, the application loads a resource module based on a language setting that is compatible with the target operating system, as well as Windows Vista and later.</span></span> <span data-ttu-id="adc6e-113">Per questo tipo di caricamento del modulo, l'applicazione deve chiamare le funzioni MUI [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span><span class="sxs-lookup"><span data-stu-id="adc6e-113">For this type of module loading, the application must call the MUI functions [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span></span>


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="adc6e-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="adc6e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adc6e-115">Individuazione delle risorse PE Win32</span><span class="sxs-lookup"><span data-stu-id="adc6e-115">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> <dt>

[<span data-ttu-id="adc6e-116">Esempio di impostazioni di MUI: Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="adc6e-116">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[<span data-ttu-id="adc6e-117">Esempio di impostazioni di MUI: Application-Specific (precedente a Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="adc6e-117">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
