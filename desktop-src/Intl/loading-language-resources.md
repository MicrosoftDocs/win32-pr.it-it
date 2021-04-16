---
description: Caricamento delle risorse di lingua
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Caricamento delle risorse di lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6917f03e773a470288fb4c9577812e0b38868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350306"
---
# <a name="loading-language-resources"></a><span data-ttu-id="acf31-103">Caricamento delle risorse di lingua</span><span class="sxs-lookup"><span data-stu-id="acf31-103">Loading Language Resources</span></span>

<span data-ttu-id="acf31-104">L'applicazione carica tutte le risorse di lingua dell'interfaccia utente, oltre a determinate stringhe del registro di sistema reindirizzate, usando le chiamate alle funzioni di caricamento delle risorse standard, ad esempio [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)e [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span><span class="sxs-lookup"><span data-stu-id="acf31-104">Your application loads all user interface language resources, other than certain redirected registry strings, using calls to standard resource loading functions, for example, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), and [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span></span> <span data-ttu-id="acf31-105">Molte funzioni di caricamento delle risorse sono state modificate per caricare automaticamente le risorse dai file di risorse specifici della lingua, considerando le risorse come se fossero contenute nel file LN.</span><span class="sxs-lookup"><span data-stu-id="acf31-105">Many resource loading functions have been modified to load resources from language-specific resource files automatically, treating resources as if they are contained in the LN file.</span></span> <span data-ttu-id="acf31-106">Nell'esempio seguente viene illustrato l'utilizzo di **LoadString** per caricare le stringhe di lingua per un'applicazione che segue le impostazioni della lingua di sistema.</span><span class="sxs-lookup"><span data-stu-id="acf31-106">The following example illustrates the use of **LoadString** to load language strings for an application that follows system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="acf31-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acf31-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acf31-108">Individuazione delle risorse PE Win32</span><span class="sxs-lookup"><span data-stu-id="acf31-108">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> </dl>

 

 
