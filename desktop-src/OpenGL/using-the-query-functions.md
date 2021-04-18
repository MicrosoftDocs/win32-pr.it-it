---
title: Uso delle funzioni di query
description: Uso delle funzioni di query
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, funzioni di query
- funzioni di query OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298300"
---
# <a name="using-the-query-functions"></a>Uso delle funzioni di query

Sono disponibili quattro funzioni di query per ottenere semplici variabili di stato e una per determinare se un determinato stato è abilitato o disabilitato:

-   [**glGetBooleanv**](glgetbooleanv.md)
-   [**glGetIntegerv**](glgetintegerv.md)
-   [**glGetFloatv**](glgetfloatv.md)
-   [**glGetDoublev**](glgetdoublev.md)
-   [**glIsEnabled**](glisenabled.md)

I prototipi per le funzioni di query sono:

**void** **glGetBooleanv**(**GLEnum** *pname* , **GLboolean \*** *params* );

**void** **glGetIntegerv**(**GLEnum** *pname* , **riflesso \*** *params* );

**void** **glGetFloatv**(**GLEnum** *pname* , **GLfloat \*** *params* );

**void** **glGetDoublev**(**GLEnum** *pname* , **GLdouble \*** *params* );

Le funzioni di query ottengono rispettivamente variabili di stato booleane, Integer, a virgola mobile o a precisione doppia. Il parametro *pname* è una costante simbolica che indica la variabile di stato da restituire e *params* è un puntatore a una matrice del tipo indicato in cui inserire i dati restituiti. I valori possibili per *pname* sono elencati in [variabili di stato OpenGL](opengl-state-variables.md). Se necessario, viene eseguita una conversione di tipi per restituire la variabile desiderata come tipo di dati richiesto.

Il prototipo per [**glIsEnabled**](glisenabled.md) è:

**GLboolean** **glIsEnabled**(GLEnum *Cap* );

Se la modalità specificata da *Cap* è abilitata, **glIsEnabled** restituisce GL \_ true. Se la modalità specificata da *Cap* è disabilitata, **glIsEnabled** restituisce GL \_ false. I valori possibili per *Cap* sono elencati in [variabili di stato OpenGL](opengl-state-variables.md).

Altre funzioni specializzate restituiscono variabili di stato specifiche. Per informazioni sull'uso di queste funzioni, vedere le variabili di stato OpenGL e il *Manuale di riferimento di OpenGL*. Per ulteriori informazioni sulla funzionalità di gestione degli errori di OpenGL e sulla funzione **glGetError** , vedere [gestione degli errori](error-handling.md).

Le funzioni che restituiscono variabili di stato specifiche sono:

-   [**glGetClipPlane**](glgetclipplane.md)
-   [**glGetError**](glgeterror.md)
-   [**glGetLight**](glgetlight.md)
-   [**glGetMap**](glgetmap.md)
-   [**glGetMaterial**](glgetmaterial.md)
-   [**glGetPixelMap**](glgetpixelmap.md)
-   [**glGetPolygonStipple**](glgetpolygonstipple.md)
-   [**glGetString**](glgetstring.md)
-   [**glGetTexEnv**](glgettexenv.md)
-   [**glGetTexGen**](glgettexgen.md)
-   [**glGetTexImage**](glgetteximage.md)
-   [**glGetTexLevelParameter**](glgettexlevelparameter.md)
-   [**glGetTexParameter**](glgettexparameter.md)

 

 




