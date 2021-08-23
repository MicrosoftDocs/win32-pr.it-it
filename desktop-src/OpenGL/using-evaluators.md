---
title: Uso degli analizzatori
description: Uso degli analizzatori
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, analizzatori
- Analizzatori OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4bb6808ad1898b0c98906a543291c700ee61257a35befa8886789f3f8b7e31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553491"
---
# <a name="using-evaluators"></a>Uso degli analizzatori

Le funzioni dell'analizzatore OpenGL consentono di usare un mapping polinomiale per produrre vertici, normali, coordinate di trama e colori. Questi valori calcolati vengono quindi passati alla pipeline di elaborazione come se fossero stati specificati direttamente. Le funzioni dell'analizzatore sono anche alla base delle funzioni NURBS (Non-Uniform Rational B-Spline), che consentono di definire curve e superfici, come descritto in Libreria dell'utilità [OpenGL](opengl-utility-library.md).

Il primo passaggio nell'uso degli analizzatori consiste nel definire il mapping polinomiale bidimensionale appropriato usando [**glMap \***](glmap1.md). È quindi possibile specificare e valutare i valori di dominio per questa mappa in uno dei due modi seguenti:

-   Definire una serie di valori di dominio di cui eseguire il mapping in modo uniforme usando [**glMapGrid**](glmapgrid-functions.md) e quindi valutare un subset rettangolare di tale griglia con [**glEvalMesh**](glevalmesh-functions.md). È possibile valutare un singolo punto della griglia usando [**glEvalPoint**](glevalpoint.md).
-   Specificare in modo esplicito un valore di dominio desiderato come argomento, che valuta le mappe in corrispondenza di tale valore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento per gli analizzatori](evaluators-reference.md)
</dt> </dl>

 

 




