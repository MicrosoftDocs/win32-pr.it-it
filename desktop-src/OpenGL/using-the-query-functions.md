---
title: Uso delle funzioni di query
description: Uso delle funzioni di query
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, funzioni di query
- Funzioni di query OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e3e883bdf8730dac7b1a8e07448b771109bef0ac5ec2246411703e8f841a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776481"
---
# <a name="using-the-query-functions"></a>Uso delle funzioni di query

Sono disponibili quattro funzioni di query per ottenere variabili di stato semplici e una per determinare se un determinato stato è abilitato o disabilitato:

-   [**glGetBooleanv**](glgetbooleanv.md)
-   [**glGetIntegerv**](glgetintegerv.md)
-   [**glGetFloatv**](glgetfloatv.md)
-   [**glGetDoublev**](glgetdoublev.md)
-   [**glIsEnabled**](glisenabled.md)

I prototipi per le funzioni di query sono:

**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \** _ _params* );

**void** **glGetIntegerv**(**GLenum** *pname* , **GLint \** _ _params* );

**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \** _ _params* );

**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \** _ _params* );

Le funzioni di query ottengono rispettivamente variabili di stato booleane, intere, a virgola mobile o a precisione doppia. Il *parametro pname* è una costante simbolica che indica la variabile di stato da restituire e *params* è un puntatore a una matrice del tipo indicato in cui inserire i dati restituiti. I valori possibili per *pname* sono elencati in [OpenGL State Variables](opengl-state-variables.md). Se necessario, viene eseguita una conversione del tipo per restituire la variabile desiderata come tipo di dati richiesto.

Il prototipo [**per glIsEnabled**](glisenabled.md) è:

**GLboolean** **glIsEnabled**(GLenum *cap* );

Se la modalità specificata da *cap* è abilitata, **glIsEnabled** restituisce GL \_ TRUE. Se la modalità specificata da *cap è* disabilitata, **glIsEnabled** restituisce GL \_ FALSE. I valori possibili per *cap sono* elencati in [OpenGL State Variables](opengl-state-variables.md).

Altre funzioni specializzate restituiscono variabili di stato specifiche. Per sapere quando usare queste funzioni, vedere OpenGL State Variables (Variabili di stato OpenGL) e *openGL Reference Manual (Manuale di riferimento di OpenGL).* Per altre informazioni sulla funzionalità di gestione degli errori di OpenGL e sulla **funzione glGetError,** vedere [Gestione degli errori.](error-handling.md)

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

 

 




