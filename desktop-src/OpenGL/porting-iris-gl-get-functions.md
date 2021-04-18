---
title: Porting delle funzioni Get di IRIS GL
description: IRIS GL \ 0034; Get \ 0034; le funzioni hanno il formato seguente
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- Porting di IRIS GL, funzioni Get
- porting da IRIS GL, Get Functions
- porting in OpenGL da IRIS GL, funzioni Get
- Porting OpenGL da IRIS GL, funzioni Get
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298544"
---
# <a name="porting-iris-gl-get-functions"></a>Porting delle funzioni Get di IRIS GL

Le funzioni "Get" di IRIS GL hanno il formato seguente:

``` syntax
int getthing();
```

e

``` syntax
int getthings( int *a, int *b);
```

Il codice di IRIS GL include probabilmente le chiamate di funzione Get che hanno un aspetto simile al seguente:

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

In OpenGL si usa uno dei quattro tipi seguenti di funzioni [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) al posto delle funzioni Get di Iris GL equivalenti:

-   **glGetBooleanv**
-   **glGetIntegerv**
-   **glGetFloatv**
-   **glGetDoublev**

Le funzioni presentano la sintassi seguente:

``` syntax
glGet<Datatype>v( value, *data );
```

dove *value* è di tipo **GLEnum** e i dati sono di tipo **GLdatatype**. Quando si chiama **glGet** e viene restituito un tipo diverso dal tipo previsto, il tipo viene convertito in modo appropriato. Per un elenco completo dei parametri **glGet** , vedere [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).

 

 




