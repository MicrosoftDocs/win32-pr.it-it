---
description: Controllo dei grafici di filtro tramite C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Controllo dei grafici di filtro tramite C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e234413f7642d7349c2bf378d1aded97b399e252117b0793f90335de8643912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073755"
---
# <a name="controlling-filter-graphs-using-c"></a>Controllo dei grafici di filtro tramite C

Se si scrive un'applicazione DirectShow in C (anziché in C++), è necessario usare un puntatore vtable per chiamare i metodi. L'esempio seguente illustra come chiamare il **metodo IUnknown::QueryInterface** da un'applicazione scritta in C:


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



Di seguito viene illustrata la chiamata equivalente in C++:


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



In C le interfacce COM sono definite come strutture. Il **membro lpVtbl** è un puntatore a una tabella di metodi di interfaccia (vtable). Tutti i metodi accettano un parametro aggiuntivo, ovvero un puntatore all'interfaccia .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Appendici](appendixes.md)
</dt> </dl>

 

 



