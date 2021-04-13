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
# <a name="handling-errors-opengl"></a><span data-ttu-id="26341-105">Gestione degli errori (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="26341-105">Handling Errors (OpenGL)</span></span>

<span data-ttu-id="26341-106">La funzione **gluErrorString** recupera le stringhe di errore che corrispondono ai codici di errore OpenGL o Glu.</span><span class="sxs-lookup"><span data-stu-id="26341-106">The **gluErrorString** function retrieves error strings that correspond to OpenGL or GLU error codes.</span></span> <span data-ttu-id="26341-107">I codici di errore OpenGL attualmente definiti sono descritti in [**glGetError**](glgeterror.md).</span><span class="sxs-lookup"><span data-stu-id="26341-107">The currently defined OpenGL error codes are described in [**glGetError**](glgeterror.md).</span></span> <span data-ttu-id="26341-108">I codici di errore GLU sono elencati in [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md)e [*gluNurbsCallback*](glunurbs.md).</span><span class="sxs-lookup"><span data-stu-id="26341-108">The GLU error codes are listed in [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md), and [*gluNurbsCallback*](glunurbs.md).</span></span>

<span data-ttu-id="26341-109">Il valore restituito per **gluErrorString** è un puntatore a una stringa descrittiva che corrisponde al numero di errore OpenGL, Glu o GLX passato nel parametro *ErrorCode* .</span><span class="sxs-lookup"><span data-stu-id="26341-109">The return value for **gluErrorString** is a pointer to a descriptive string that corresponds to the OpenGL, GLU, or GLX error number passed in the *errorCode* parameter.</span></span> <span data-ttu-id="26341-110">I codici di errore definiti sono descritti nel *Manuale di riferimento OpenGL* insieme alla funzione o alla funzione che è in grado di generarli.</span><span class="sxs-lookup"><span data-stu-id="26341-110">The defined error codes are described in the *OpenGL Reference Manual* along with the function or function that can generate them.</span></span>

 

 




