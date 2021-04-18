---
title: Variabili di stato OpenGL
description: Negli argomenti seguenti vengono elencati i nomi delle variabili di stato su cui è possibile eseguire query
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- Variabili di stato OpenGL
- variabili di stato, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298206"
---
# <a name="opengl-state-variables"></a>Variabili di stato OpenGL

Negli argomenti seguenti vengono elencati i nomi delle variabili di stato su cui è possibile eseguire query:

-   [**Variabili di stato per i valori correnti e i dati associati**](state-variables-for-current-values-and-associated-data.md)
-   [**Variabili di stato della trasformazione**](transformation-state-variables.md)
-   [**Variabili di stato colorazione**](coloring-state-variables.md)
-   [**Variabili di stato di illuminazione**](lighting-state-variables.md)
-   [**Variabili di stato di rasterizzazione**](rasterization-state-variables.md)
-   [**Variabili di stato di texturing**](texturing-state-variables.md)
-   [**Operazioni pixel**](pixel-operations.md)
-   [**Variabili di stato del controllo framebuffer**](framebuffer-control-state-variables.md)
-   [**Variabili di stato pixel**](pixel-state-variables.md)
-   [**Variabili di stato dell'analizzatore**](evaluator-state-variables.md)
-   [**Variabili di stato dell'hint**](hint-state-variables.md)
-   [**Variabili di stato dipendenti dall'implementazione**](implementation-dependent-state-variables.md)
-   [**Variabili di stato del Pixel-Depth dipendente dall'implementazione**](implementation-dependent-pixel-depth-state-variables.md)
-   [**Variabili di stato varie**](miscellaneous-state-variables.md)

Per ogni variabile, l'argomento elenca una descrizione, un gruppo di attributi, un valore iniziale o minimo e la funzione [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) suggerita da usare per ottenerlo.

Le variabili di stato che è possibile ottenere tramite [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetDoublev**](glgetdoublev.md) sono elencate con una sola di queste functionsthe più appropriate per il tipo di dati da restituire. Non è possibile ottenere queste variabili di stato usando [**glIsEnabled**](glisenabled.md). È tuttavia possibile ottenere le variabili di stato per le quali **glIsEnabled** è elencato come funzione di query con **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv** e **glGetDoublev**. È possibile ottenere le variabili di stato per le quali qualsiasi altra funzione è elencata come funzione di query solo usando tale funzione. Se non è elencato alcun gruppo di attributi, la variabile non appartiene ad alcun gruppo. Tutte le variabili di stato su cui è possibile eseguire una query, ad eccezione di quelle che dipendono dall'implementazione, presentano valori iniziali. Per determinare il valore iniziale di una variabile per la quale non è elencato alcun valore iniziale, vedere il riferimento della variabile o il

*Manuale di riferimento OpenGL*.

 

 




