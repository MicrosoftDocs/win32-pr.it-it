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
# <a name="loading-language-resources"></a>Caricamento delle risorse di lingua

L'applicazione carica tutte le risorse di lingua dell'interfaccia utente, oltre a determinate stringhe del registro di sistema reindirizzate, usando le chiamate alle funzioni di caricamento delle risorse standard, ad esempio [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)e [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea). Molte funzioni di caricamento delle risorse sono state modificate per caricare automaticamente le risorse dai file di risorse specifici della lingua, considerando le risorse come se fossero contenute nel file LN. Nell'esempio seguente viene illustrato l'utilizzo di **LoadString** per caricare le stringhe di lingua per un'applicazione che segue le impostazioni della lingua di sistema.


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

 

 
