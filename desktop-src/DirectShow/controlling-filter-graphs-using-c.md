---
description: Controllo di grafici filtro con C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Controllo di grafici filtro con C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce6d78875c6b0d5f028ea89dfbd2b061285f1c1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401259"
---
# <a name="controlling-filter-graphs-using-c"></a>Controllo di grafici filtro con C

Se si sta scrivendo un'applicazione DirectShow in C (anziché in C++), è necessario usare un puntatore vtable per chiamare i metodi. Nell'esempio seguente viene illustrato come chiamare il metodo **IUnknown:: QueryInterface** da un'applicazione scritta in C:


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



Di seguito viene illustrata la chiamata equivalente in C++:


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



In C, le interfacce COM sono definite come strutture. Il membro **lpVtbl** è un puntatore a una tabella di metodi di interfaccia (vtable). Tutti i metodi accettano un parametro aggiuntivo, ovvero un puntatore all'interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Appendici](appendixes.md)
</dt> </dl>

 

 



