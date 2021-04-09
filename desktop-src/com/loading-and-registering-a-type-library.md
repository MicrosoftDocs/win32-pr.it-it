---
title: Caricamento e registrazione di una libreria dei tipi
description: La libreria a collegamento dinamico di automazione, Oleaut32.dll, fornisce diverse funzioni che è possibile chiamare per caricare e registrare una libreria dei tipi. La chiamata a LoadTypeLibEx, come illustrato nell'esempio seguente, carica la libreria e crea le voci del registro di sistema.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d533225913d6bcfbb74df3ac42bd00b18b00e4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047476"
---
# <a name="loading-and-registering-a-type-library"></a><span data-ttu-id="59754-104">Caricamento e registrazione di una libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="59754-104">Loading and Registering a Type Library</span></span>

<span data-ttu-id="59754-105">La libreria a collegamento dinamico di automazione, Oleaut32.dll, fornisce diverse funzioni che è possibile chiamare per caricare e registrare una libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="59754-105">The Automation dynamic link library, Oleaut32.dll, provides several functions that you can call to load and register a type library.</span></span> <span data-ttu-id="59754-106">La chiamata a [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), come illustrato nell'esempio seguente, carica la libreria e crea le voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="59754-106">Calling [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), as shown in the following example, both loads the library and creates the registry entries.</span></span>

## <a name="example"></a><span data-ttu-id="59754-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="59754-107">Example</span></span>

``` syntax
ITypeLib *pTypeLib;
HRESULT hr;
hr = LoadTypeLibEx("example.tlb", REGKIND_REGISTER, &pTypeLib);
if(SUCCEEDED(hr))
{
    pTypeLib->Release();
} else {
    exit(0); // Handle errors here.
}
```

 

 