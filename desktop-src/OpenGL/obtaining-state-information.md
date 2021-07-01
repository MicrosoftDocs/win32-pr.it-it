---
title: Recupero di informazioni sullo stato
description: Recupero di informazioni sullo stato
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, informazioni sullo stato
- OpenGL, variabili di stato
- informazioni sullo stato OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8329fd34fc68122be8d63e4dc28756f88faf7797
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120686"
---
# <a name="obtaining-state-information"></a>Recupero di informazioni sullo stato

OpenGL gestisce molte variabili di stato che influiscono sul comportamento di molte funzioni. Alcune di queste variabili hanno funzioni di query specializzate.

:::row:::
    :::column:::
        [**glGetClipPlane**](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [**glGetPixelMap**](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexImage**](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetLight**](glgetlight.md)
    :::column-end:::
    :::column:::
        [**glGetPolygonStipple**](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [**glGetTexLevelParameter**](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMap**](glgetmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexEnv**](glgettexenv.md)
    :::column-end:::
    :::column:::
        [**glGetTexParameter**](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMaterial**](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [**glGetTexGen**](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

Per ottenere il valore di altre variabili di stato, usare [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetIntegerv**](glgetintegerv.md), in base alle esigenze. Per informazioni su come usare queste funzioni, vedere [**glGet.**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Altre funzioni di query che è possibile usare sono [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)e [**glIsEnabled**](glisenabled.md). Per altre [informazioni sulle funzioni correlate alla gestione degli](handling-errors.md) errori, vedere Gestione degli errori. Per salvare e ripristinare set di variabili di stato, usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).

-   [Uso delle funzioni di query](using-the-query-functions.md)
-   [Gestione degli errori](error-handling.md)
-   [Codici di errore OpenGL](opengl-error-codes.md)
-   [Salvataggio e ripristino di set di variabili di stato](saving-and-restoring-sets-of-state-variables.md)
-   [Variabili di stato OpenGL](opengl-state-variables.md)
-   [Informazioni di riferimento sullo stato](state-information-reference.md)

 

 




