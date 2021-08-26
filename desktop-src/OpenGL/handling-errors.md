---
title: Gestione degli errori (OpenGL)
description: La funzione gluErrorString recupera le stringhe di errore che corrispondono ai codici di errore OpenGL o GLU.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- Utilità OpenGL (GLU), codici di errore
- GLU (Utilità OpenGL),codici di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ac3fd9010862dd9c567cb7688f7f96286cae06f7e3b0e4ffe73d3b41ca9b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035191"
---
# <a name="handling-errors-opengl"></a>Gestione degli errori (OpenGL)

La **funzione gluErrorString** recupera le stringhe di errore che corrispondono ai codici di errore OpenGL o GLU. I codici di errore OpenGL attualmente definiti sono descritti in [**glGetError**](glgeterror.md). I codici di errore GLU sono elencati in [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md)e [*gluNurbsCallback*](glunurbs.md).

Il valore restituito per **gluErrorString** è un puntatore a una stringa descrittiva che corrisponde al numero di errore OpenGL, GLU o GLX passato nel *parametro errorCode.* I codici di errore definiti sono descritti nel manuale *di riferimento di OpenGL* insieme alla funzione o alla funzione che può generarli.

 

 




