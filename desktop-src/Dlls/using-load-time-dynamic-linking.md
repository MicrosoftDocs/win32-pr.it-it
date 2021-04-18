---
description: Dopo aver creato una DLL, è possibile usare le funzioni definite in un'applicazione. Di seguito è riportata una semplice applicazione console che usa la funzione put esportata da Myputs.dll (vedere Creazione di una libreria di Dynamic-Link semplice).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Uso di Load-Time collegamento dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e5d14ba2190528c44d892b957d22b273fd4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310041"
---
# <a name="using-load-time-dynamic-linking"></a>Uso di Load-Time collegamento dinamico

Dopo aver creato una DLL, è possibile usare le funzioni definite in un'applicazione. Di seguito è riportata una semplice applicazione console che usa la funzione put esportata da Myputs.dll (vedere [creazione di una libreria di Dynamic-Link semplice](creating-a-simple-dynamic-link-library.md)).

Poiché in questo esempio la funzione DLL viene chiamata in modo esplicito, il modulo per l'applicazione deve essere collegato con la libreria di importazione My put. lib. Per ulteriori informazioni sulla creazione di dll, vedere la documentazione inclusa con gli strumenti di sviluppo.


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Collegamento dinamico in fase di caricamento](load-time-dynamic-linking.md)
</dt> </dl>

 

 



