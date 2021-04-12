---
title: Contenimento/delega
description: Il meccanismo più comune per il riutilizzo degli oggetti in COM è il contenimento/delega.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d26e0c1d1e48596cb9acef740405c797f6f0f46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332356"
---
# <a name="containmentdelegation"></a>Contenimento/delega

Il meccanismo più comune per il riutilizzo degli oggetti in COM è il *contenimento/delega*. Questo tipo di riutilizzo è un concetto familiare presente nella maggior parte dei sistemi e dei linguaggi orientati agli oggetti. L'oggetto esterno, che deve usare l'oggetto interno, funge da client oggetto per l'oggetto interno. L'oggetto esterno "contiene" l'oggetto interno e quando l'oggetto esterno richiede i servizi dell'oggetto interno, l'oggetto esterno delega in modo esplicito l'implementazione ai metodi dell'oggetto interno. Ciò significa che l'oggetto esterno usa i servizi dell'oggetto interno per implementare se stesso.

Non è necessario che gli oggetti esterni e interni supportino le stesse interfacce, sebbene sia certamente ragionevole contenere un oggetto che implementi un'interfaccia non eseguita dall'oggetto esterno e implementi i metodi dell'oggetto esterno semplicemente come le chiamate ai metodi corrispondenti nell'oggetto interno. Quando la complessità degli oggetti esterni e interni è notevolmente diversa, tuttavia, l'oggetto esterno può implementare alcuni dei metodi delle relative interfacce delegando le chiamate ai metodi di interfaccia implementati nell'oggetto interno.

È semplice implementare il contenimento per un oggetto esterno. L'oggetto esterno crea gli oggetti interni che devono usare come qualsiasi altro client. Non si tratta di una novità: il processo è simile a un oggetto C++ che a sua volta contiene un oggetto stringa C++ che usa per eseguire determinate funzioni stringa, anche se l'oggetto esterno non è considerato un oggetto stringa in un proprio diritto. Quindi, usando il relativo puntatore all'oggetto interno, una chiamata a un metodo nell'oggetto esterno genera una chiamata a un metodo dell'oggetto interno.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggregazione](aggregation.md)
</dt> </dl>

 

 




