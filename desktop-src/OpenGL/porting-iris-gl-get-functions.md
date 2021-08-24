---
title: Porting IRIS GL Get Functions
description: IRIS GL \ 0034;get \ 0034; Le funzioni hanno il formato seguente
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- Porting IRIS GL,funzioni get
- porting da IRIS GL,funzioni get
- porting a OpenGL da IRIS GL,funzioni get
- Porting OpenGL da IRIS GL,funzioni get
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfe9159e0207198fa94959729bd0c95439bb91b5dd55a8a1f9adf3b048d7bb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485561"
---
# <a name="porting-iris-gl-get-functions"></a>Porting IRIS GL Get Functions

Le funzioni "get" di IRIS GL hanno il formato seguente:

``` syntax
int getthing();
```

e

``` syntax
int getthings( int *a, int *b);
```

Il codice IRIS GL include probabilmente chiamate di funzione get simili a:

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

In OpenGL si usa uno dei quattro tipi di funzioni [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) seguenti al posto delle funzioni get IRIS GL equivalenti:

-   **glGetBooleanv**
-   **glGetIntegerv**
-   **glGetFloatv**
-   **glGetDoublev**

Le funzioni hanno la sintassi seguente:

``` syntax
glGet<Datatype>v( value, *data );
```

dove *value* è di tipo **GLenum** e i dati sono di tipo **GLdatatype**. Quando si chiama **glGet** e viene restituito un tipo diverso dal tipo previsto, il tipo viene convertito in modo appropriato. Per un elenco completo dei **parametri glGet,** vedere [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).

 

 




