---
title: Caricamento e registrazione di una libreria dei tipi
description: La libreria di collegamento dinamico di Automazione, Oleaut32.dll, fornisce diverse funzioni che è possibile chiamare per caricare e registrare una libreria dei tipi. La chiamata a LoadTypeLibEx, come illustrato nell'esempio seguente, carica la libreria e crea le voci del Registro di sistema.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98ea3a28f3884cbd6a377e45f1b537d169f510fdc4ce9a433dff6e976d9c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854231"
---
# <a name="loading-and-registering-a-type-library"></a>Caricamento e registrazione di una libreria dei tipi

La libreria di collegamento dinamico di Automazione, Oleaut32.dll, fornisce diverse funzioni che è possibile chiamare per caricare e registrare una libreria dei tipi. Chiamando [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), come illustrato nell'esempio seguente, viene caricata la libreria e vengono create le voci del Registro di sistema.

## <a name="example"></a>Esempio

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

 

 