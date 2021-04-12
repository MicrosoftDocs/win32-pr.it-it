---
title: Utilizzo degli analizzatori
description: Utilizzo degli analizzatori
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, analizzatori
- analizzatori OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329204"
---
# <a name="using-evaluators"></a>Utilizzo degli analizzatori

Le funzioni dell'analizzatore OpenGL consentono di usare un mapping polinomiale per produrre vertici, normali, coordinate di trama e colori. Questi valori calcolati vengono quindi passati alla pipeline di elaborazione come se fossero stati specificati direttamente. Le funzioni dell'analizzatore rappresentano anche la base per le funzioni NURBS (non-Uniform Rational B-spline), che consentono di definire curve e superfici, come descritto nella [libreria di utilità OpenGL](opengl-utility-library.md).

Il primo passaggio nell'utilizzo degli analizzatori consiste nel definire il mapping polinomiale bidimensionale o bidimensionale appropriato utilizzando [**glMap \***](glmap1.md). È quindi possibile specificare e valutare i valori di dominio per la mappa in uno dei due modi seguenti:

-   Definire una serie di valori di dominio con spazi uniformi da mappare usando [**glMapGrid**](glmapgrid-functions.md) , quindi valutare un subset rettangolare della griglia con [**glEvalMesh**](glevalmesh-functions.md). Un singolo punto della griglia può essere valutato usando [**glEvalPoint**](glevalpoint.md).
-   Specificare in modo esplicito un valore di dominio desiderato come argomento, che valuta le mappe in corrispondenza di tale valore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento per gli analizzatori](evaluators-reference.md)
</dt> </dl>

 

 




