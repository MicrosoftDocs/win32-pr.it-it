---
title: Acquisizione delle informazioni sullo stato
description: Acquisizione delle informazioni sullo stato
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, informazioni sullo stato
- OpenGL, variabili di stato
- informazioni sullo stato OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709718"
---
# <a name="obtaining-state-information"></a>Acquisizione delle informazioni sullo stato

OpenGL gestisce molte variabili di stato che influiscono sul comportamento di molte funzioni. Alcune di queste variabili hanno funzioni di query specializzate.



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [**glGetClipPlane**](glgetclipplane.md) | [**glGetPixelMap**](glgetpixelmap.md)             | [**glGetTexImage**](glgetteximage.md)                   |
| [**glGetLight**](glgetlight.md)         | [**glGetPolygonStipple**](glgetpolygonstipple.md) | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |
| [**glGetMap**](glgetmap.md)             | [**glGetTexEnv**](glgettexenv.md)                 | [**glGetTexParameter**](glgettexparameter.md)           |
| [**glGetMaterial**](glgetmaterial.md)   | [**glGetTexGen**](glgettexgen.md)                 |                                                          |



 

Per ottenere il valore di altre variabili di stato, usare [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetIntegerv**](glgetintegerv.md), a seconda dei casi. Per informazioni sull'uso di queste funzioni, vedere [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) . Altre funzioni di query che è possibile usare sono [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)e [**glIsEnabled**](glisenabled.md). Per ulteriori informazioni sulle funzioni correlate alla gestione degli errori, vedere [gestione degli errori](handling-errors.md) . Per salvare e ripristinare set di variabili di stato, usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).

-   [Uso delle funzioni di query](using-the-query-functions.md)
-   [Gestione degli errori](error-handling.md)
-   [Codici di errore OpenGL](opengl-error-codes.md)
-   [Salvataggio e ripristino di set di variabili di stato](saving-and-restoring-sets-of-state-variables.md)
-   [Variabili di stato OpenGL](opengl-state-variables.md)
-   [Riferimento alle informazioni sullo stato](state-information-reference.md)

 

 




