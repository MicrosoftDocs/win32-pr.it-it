---
title: Gestione degli errori (OpenGL)
description: La funzione gluErrorString recupera le stringhe di errore che corrispondono ai codici di errore OpenGL o GLU.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- Utilità OpenGL (GLU), codici di errore
- GLU (utilità OpenGL), codici di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab319fd978cd5ea901133fc9961caf1c66f3185d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340022"
---
# <a name="handling-errors-opengl"></a>Gestione degli errori (OpenGL)

La funzione **gluErrorString** recupera le stringhe di errore che corrispondono ai codici di errore OpenGL o Glu. I codici di errore OpenGL attualmente definiti sono descritti in [**glGetError**](glgeterror.md). I codici di errore GLU sono elencati in [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md)e [*gluNurbsCallback*](glunurbs.md).

Il valore restituito per **gluErrorString** è un puntatore a una stringa descrittiva che corrisponde al numero di errore OpenGL, Glu o GLX passato nel parametro *ErrorCode* . I codici di errore definiti sono descritti nel *Manuale di riferimento OpenGL* insieme alla funzione o alla funzione che è in grado di generarli.

 

 




