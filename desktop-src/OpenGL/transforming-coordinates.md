---
title: Trasformazione delle coordinate
description: La libreria di utilità OpenGL (GLU) fornisce diverse funzioni di trasformazione della matrice comunemente utilizzate.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- Utilità OpenGL (GLU), funzioni di trasformazione matrice
- GLU (utilità OpenGL), funzioni di trasformazione matrice
- funzioni di trasformazione matrice OpenGL
- Utilità OpenGL (GLU), trasformazione delle coordinate
- GLU (utilità OpenGL), trasformazione delle coordinate
- trasformazione di coordinate OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713936"
---
# <a name="transforming-coordinates"></a><span data-ttu-id="8c029-109">Trasformazione delle coordinate</span><span class="sxs-lookup"><span data-stu-id="8c029-109">Transforming Coordinates</span></span>

<span data-ttu-id="8c029-110">La libreria di utilità OpenGL (GLU) fornisce diverse funzioni di trasformazione della matrice comunemente utilizzate.</span><span class="sxs-lookup"><span data-stu-id="8c029-110">The OpenGL Utility library (GLU) provides several commonly used matrix transformation functions.</span></span> <span data-ttu-id="8c029-111">È possibile configurare un'area di visualizzazione ortogonale bidimensionale con [**gluOrtho2D**](gluortho2d.md), un volume di visualizzazione prospettico standard usando [**gluPerspective**](gluperspective.md)o un volume di visualizzazione centrato su un osservazione specificato con [**gluLookAt**](glulookat.md).</span><span class="sxs-lookup"><span data-stu-id="8c029-111">You can set up a two-dimensional orthographic viewing region with [**gluOrtho2D**](gluortho2d.md), a standard perspective view volume using [**gluPerspective**](gluperspective.md), or a view volume that is centered on a specified eyepoint with [**gluLookAt**](glulookat.md).</span></span> <span data-ttu-id="8c029-112">Ognuna di queste funzioni crea la matrice desiderata e la applica alla matrice corrente usando [**glMultMatrix**](glmultmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="8c029-112">Each of these functions creates the desired matrix and applies it to the current matrix using [**glMultMatrix**](glmultmatrix.md).</span></span>

<span data-ttu-id="8c029-113">La funzione [**gluPickMatrix**](glupickmatrix.md) semplifica la selezione di una matrice di selezione creando una matrice che limita il disegno a una piccola area del viewport.</span><span class="sxs-lookup"><span data-stu-id="8c029-113">The [**gluPickMatrix**](glupickmatrix.md) function simplifies selection of a picking matrix by creating a matrix that restricts drawing to a small region of the viewport.</span></span> <span data-ttu-id="8c029-114">Se si esegue nuovamente il rendering della scena in modalità di selezione dopo che questa matrice è stata applicata, verranno selezionati tutti gli oggetti che verranno disegnati accanto al cursore e le relative informazioni verranno archiviate nel buffer di selezione.</span><span class="sxs-lookup"><span data-stu-id="8c029-114">If you re-render the scene in selection mode after this matrix has been applied, all objects that would be drawn near the cursor will be selected, and information about them will be stored in the selection buffer.</span></span> <span data-ttu-id="8c029-115">Per ulteriori informazioni sulla modalità di selezione, vedere l'argomento relativo all'esecuzione di selezioni e commenti [e suggerimenti](performing-selection-and-feedback.md).</span><span class="sxs-lookup"><span data-stu-id="8c029-115">For more information about selection mode, see "Performing Selection and Feedback" [Performing Selection and Feedback](performing-selection-and-feedback.md).</span></span>

<span data-ttu-id="8c029-116">Per determinare la posizione della finestra in cui viene disegnato un oggetto, usare [**gluProject**](gluproject.md), che converte le coordinate dell'oggetto specificato *objX*, *objy* e *objz* in coordinate della finestra usando *modelMatrix*, *projMatrix* e *viewport*.</span><span class="sxs-lookup"><span data-stu-id="8c029-116">To determine where in the window an object is being drawn, use [**gluProject**](gluproject.md), which converts the specified object coordinates *objx*, *objy*, and *objz* into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="8c029-117">Il risultato viene archiviato in *Winx*, *vinoso* e *Winz*.</span><span class="sxs-lookup"><span data-stu-id="8c029-117">The result is stored in *winx*, *winy*, and *winz*.</span></span> <span data-ttu-id="8c029-118">Se la funzione ha esito positivo, il valore restituito è GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="8c029-118">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="8c029-119">Se la funzione ha esito negativo, il valore restituito è GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="8c029-119">If the function fails, the return value is GL\_FALSE.</span></span>

<span data-ttu-id="8c029-120">La funzione [**gluUnProject**](gluunproject.md) esegue la conversione inversa: trasforma la finestra specificata le coordinate *Winx*, *vinoso* e *Winz* nelle coordinate dell'oggetto usando *modelMatrix*, *projMatrix* e *viewport*.</span><span class="sxs-lookup"><span data-stu-id="8c029-120">The [**gluUnProject**](gluunproject.md) function performs the inverse conversion: it transforms the specified window coordinates *winx*, *winy*, and *winz* into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="8c029-121">Il risultato viene archiviato in *objX*, *objy* e *objz*.</span><span class="sxs-lookup"><span data-stu-id="8c029-121">The result is stored in *objx*, *objy*, and *objz*.</span></span> <span data-ttu-id="8c029-122">Se la funzione ha esito positivo, il valore restituito è GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="8c029-122">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="8c029-123">Se la funzione ha esito negativo, il valore restituito è GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="8c029-123">If the function fails, the return value is GL\_FALSE.</span></span>

 

 




