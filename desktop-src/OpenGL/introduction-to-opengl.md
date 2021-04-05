---
title: Introduzione a OpenGL
description: Introduzione a OpenGL
ms.assetid: 8fe214a9-f071-470b-ac72-182a7bd54fbd
keywords:
- OpenGL, introduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cece636e51348288e587116bf13f95696b93ab9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955337"
---
# <a name="introduction-to-opengl"></a><span data-ttu-id="f2e4b-104">Introduzione a OpenGL</span><span class="sxs-lookup"><span data-stu-id="f2e4b-104">Introduction to OpenGL</span></span>

<span data-ttu-id="f2e4b-105">Come interfaccia software per l'hardware grafico, lo scopo principale di OpenGL è eseguire il rendering di oggetti bidimensionali e tridimensionali in un framebuffer.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-105">As a software interface for graphics hardware, the main purpose of OpenGL is to render two- and three-dimensional objects into a framebuffer.</span></span> <span data-ttu-id="f2e4b-106">Questi oggetti sono descritti come sequenze di vertici (che definiscono oggetti geometrici) o pixel (che definiscono le immagini).</span><span class="sxs-lookup"><span data-stu-id="f2e4b-106">These objects are described as sequences of vertices (that define geometric objects) or pixels (that define images).</span></span> <span data-ttu-id="f2e4b-107">OpenGL esegue diversi processi su questi dati per convertirli in pixel per formare l'immagine finale desiderata nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-107">OpenGL performs several processes on this data to convert it to pixels to form the final desired image in the framebuffer.</span></span>

<span data-ttu-id="f2e4b-108">Negli argomenti seguenti viene illustrata una visualizzazione globale del funzionamento di OpenGL:</span><span class="sxs-lookup"><span data-stu-id="f2e4b-108">The following topics present a global view of how OpenGL works:</span></span>

-   <span data-ttu-id="f2e4b-109">[Primitive e comandi](primitives-and-commands.md) illustrano punti, segmenti di linea e poligoni come unità di base del disegno; e l'elaborazione dei comandi.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-109">[Primitives and Commands](primitives-and-commands.md) discusses points, line segments, and polygons as the basic units of drawing; and the processing of commands.</span></span>
-   <span data-ttu-id="f2e4b-110">Il [controllo grafico OpenGL](opengl-graphic-control.md) descrive quali operazioni grafiche i controlli OpenGL e quali non controllano.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-110">[OpenGL Graphic Control](opengl-graphic-control.md) describes which graphic operations OpenGL controls and which it does not control.</span></span>
-   <span data-ttu-id="f2e4b-111">[Modello di esecuzione](execution-model.md) viene illustrato il modello client/server per l'interpretazione dei comandi OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-111">[Execution Model](execution-model.md) discusses the client/server model for interpreting OpenGL commands.</span></span>
-   <span data-ttu-id="f2e4b-112">L' [operazione OpenGL di base](basic-opengl-operation.md) offre una descrizione di alto livello del modo in cui OpenGL elabora i dati per produrre un'immagine corrispondente nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-112">[Basic OpenGL Operation](basic-opengl-operation.md) gives a high-level description of how OpenGL processes data to produce a corresponding image in the framebuffer.</span></span>
-   <span data-ttu-id="f2e4b-113">I [nomi delle funzioni OpenGL](opengl-function-names.md) descrivono le convenzioni di denominazione usate in OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-113">[OpenGL Function Names](opengl-function-names.md) describes the naming conventions used in OpenGL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2e4b-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2e4b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2e4b-115">Pipeline di elaborazione OpenGL</span><span class="sxs-lookup"><span data-stu-id="f2e4b-115">OpenGL Processing Pipeline</span></span>](opengl-processing-pipeline.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-116">Utilizzo degli analizzatori</span><span class="sxs-lookup"><span data-stu-id="f2e4b-116">Using Evaluators</span></span>](using-evaluators.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-117">Esecuzione di selezioni e commenti</span><span class="sxs-lookup"><span data-stu-id="f2e4b-117">Performing Selection and Feedback</span></span>](performing-selection-and-feedback.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-118">Uso degli elenchi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="f2e4b-118">Using Display Lists</span></span>](using-display-lists.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-119">Gestione di modalità ed esecuzione</span><span class="sxs-lookup"><span data-stu-id="f2e4b-119">Managing Modes and Execution</span></span>](managing-modes-and-execution.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-120">Acquisizione delle informazioni sullo stato</span><span class="sxs-lookup"><span data-stu-id="f2e4b-120">Obtaining State Information</span></span>](obtaining-state-information.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-121">Libreria di utilità OpenGL</span><span class="sxs-lookup"><span data-stu-id="f2e4b-121">OpenGL Utility Library</span></span>](opengl-utility-library.md)
</dt> </dl>

 

 




