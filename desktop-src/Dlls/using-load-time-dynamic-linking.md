---
description: Dopo aver creato una DLL, è possibile usare le funzioni definite in un'applicazione. Di seguito è riportata una semplice applicazione console che usa la funzione myPuts esportata da Myputs.dll (vedere Creazione di una libreria Dynamic-Link semplice).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Uso Load-Time collegamento dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 106d9d73808b56c664e44d8dcd71b74a65431316fd3daf47dd0736596c5aa5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902371"
---
# <a name="using-load-time-dynamic-linking"></a>Uso Load-Time collegamento dinamico

Dopo aver creato una DLL, è possibile usare le funzioni definite in un'applicazione. Di seguito è riportata una semplice applicazione console che usa la funzione myPuts esportata da Myputs.dll (vedere Creazione di una libreria [Dynamic-Link semplice).](creating-a-simple-dynamic-link-library.md)

Poiché questo esempio chiama la funzione DLL in modo esplicito, il modulo per l'applicazione deve essere collegato alla libreria di importazione Myputs.lib. Per altre informazioni sulla compilazione di DLL, vedere la documentazione inclusa con gli strumenti di sviluppo.


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

 

 



