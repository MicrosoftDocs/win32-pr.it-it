---
title: Componenti
description: Componenti
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL per Windows, componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298599"
---
# <a name="components"></a><span data-ttu-id="9da1c-104">Componenti</span><span class="sxs-lookup"><span data-stu-id="9da1c-104">Components</span></span>

<span data-ttu-id="9da1c-105">L'implementazione Microsoft di OpenGL in Windows include i componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="9da1c-105">Microsoft's implementation of OpenGL in Windows includes the following components:</span></span>

-   <span data-ttu-id="9da1c-106">Set completo di comandi OpenGL correnti</span><span class="sxs-lookup"><span data-stu-id="9da1c-106">The full set of current OpenGL commands</span></span>

    <span data-ttu-id="9da1c-107">OpenGL contiene una libreria di funzioni di base per le operazioni di grafica 3D.</span><span class="sxs-lookup"><span data-stu-id="9da1c-107">OpenGL contains a library of core functions for 3-D graphics operations.</span></span> <span data-ttu-id="9da1c-108">Queste funzioni di base vengono usate per gestire la descrizione della forma dell'oggetto, la trasformazione della matrice, l'illuminazione, la colorazione, la trama, il ritaglio, le bitmap, la nebbia e l'anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="9da1c-108">These basic functions are used to manage object shape description, matrix transformation, lighting, coloring, texture, clipping, bitmaps, fog, and antialiasing.</span></span> <span data-ttu-id="9da1c-109">I nomi per queste funzioni principali hanno un prefisso "GL".</span><span class="sxs-lookup"><span data-stu-id="9da1c-109">The names for these core functions have a "gl" prefix.</span></span>

    <span data-ttu-id="9da1c-110">Molti dei comandi di OpenGL hanno diverse varianti, che differiscono per il numero e il tipo dei parametri.</span><span class="sxs-lookup"><span data-stu-id="9da1c-110">Many of the OpenGL commands have several variants, which differ in the number and type of their parameters.</span></span> <span data-ttu-id="9da1c-111">Il conteggio di tutte le varianti include più di 300 comandi OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9da1c-111">Counting all the variants, there are more than 300 OpenGL commands.</span></span>

-   <span data-ttu-id="9da1c-112">Libreria dell'utilità OpenGL (GLU)</span><span class="sxs-lookup"><span data-stu-id="9da1c-112">The OpenGL Utility (GLU) library</span></span>

    <span data-ttu-id="9da1c-113">Questa libreria di funzioni ausiliarie integra le funzioni di base di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9da1c-113">This library of auxiliary functions complements the core OpenGL functions.</span></span> <span data-ttu-id="9da1c-114">I comandi gestiscono supporto per la trama, trasformazione delle coordinate, suddivisione a mosaico del poligono, sfere di rendering, cilindri e dischi, curve e superfici di base non uniforme, NURBS e gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="9da1c-114">The commands manage texture support, coordinate transformation, polygon tessellation, rendering spheres, cylinders and disks, NURBS (Non-Uniform Rational B-Spline) curves and surfaces, and error handling.</span></span>

-   <span data-ttu-id="9da1c-115">Libreria ausiliaria della Guida per programmatori OpenGL</span><span class="sxs-lookup"><span data-stu-id="9da1c-115">The OpenGL Programming Guide Auxiliary library</span></span>

    <span data-ttu-id="9da1c-116">Si tratta di una semplice libreria indipendente dalla piattaforma di funzioni per la gestione di Windows, la gestione degli eventi di input, il disegno di oggetti 3D classici, la gestione di un processo in background e l'esecuzione di un programma.</span><span class="sxs-lookup"><span data-stu-id="9da1c-116">This is a simple, platform-independent library of functions for managing windows, handling input events, drawing classic 3-D objects, managing a background process, and running a program.</span></span> <span data-ttu-id="9da1c-117">Le routine di gestione e input della finestra forniscono un livello di base di funzionalità con cui è possibile iniziare a programmare rapidamente in OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9da1c-117">The window management and input routines provide a base level of functionality with which you can quickly get started programming in OpenGL.</span></span>

    <span data-ttu-id="9da1c-118">Non utilizzarli, tuttavia, in un'applicazione di produzione.</span><span class="sxs-lookup"><span data-stu-id="9da1c-118">Do not use them, however, in a production application.</span></span> <span data-ttu-id="9da1c-119">Ecco alcuni motivi per questo avviso:</span><span class="sxs-lookup"><span data-stu-id="9da1c-119">Here are some reasons for this warning:</span></span>

    -   <span data-ttu-id="9da1c-120">Il ciclo di messaggi si trova nel codice della libreria.</span><span class="sxs-lookup"><span data-stu-id="9da1c-120">The message loop is in the library code.</span></span>
    -   <span data-ttu-id="9da1c-121">Non è possibile aggiungere gestori per messaggi WM aggiuntivi \* .</span><span class="sxs-lookup"><span data-stu-id="9da1c-121">There is no way to add handlers for additional WM\* messages.</span></span>
    -   <span data-ttu-id="9da1c-122">Il supporto per le tavolozze logiche è minimo.</span><span class="sxs-lookup"><span data-stu-id="9da1c-122">There is very little support for logical palettes.</span></span>

    <span data-ttu-id="9da1c-123">La libreria viene descritta e usata nella *Guida alla programmazione di OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="9da1c-123">The library is described and used in the *OpenGL Programming Guide*.</span></span>

-   <span data-ttu-id="9da1c-124">Funzioni WGL</span><span class="sxs-lookup"><span data-stu-id="9da1c-124">The WGL functions</span></span>

    <span data-ttu-id="9da1c-125">Questo set di funzioni connette OpenGL al sistema Windows windowing.</span><span class="sxs-lookup"><span data-stu-id="9da1c-125">This set of functions connects OpenGL to the Windows windowing system.</span></span> <span data-ttu-id="9da1c-126">Le funzioni gestiscono i contesti di rendering, gli elenchi di visualizzazione, le funzioni di estensione e le bitmap dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="9da1c-126">The functions manage rendering contexts, display lists, extension functions, and font bitmaps.</span></span> <span data-ttu-id="9da1c-127">Le funzioni WGL sono analoghe alle estensioni GLX che connettono OpenGL al sistema X Window.</span><span class="sxs-lookup"><span data-stu-id="9da1c-127">The WGL functions are analogous to the GLX extensions that connect OpenGL to the X Window System.</span></span> <span data-ttu-id="9da1c-128">I nomi di queste funzioni hanno un prefisso "WGL".</span><span class="sxs-lookup"><span data-stu-id="9da1c-128">The names for these functions have a "wgl" prefix.</span></span>

-   <span data-ttu-id="9da1c-129">Nuove funzioni di Windows per formati pixel e doppio buffering</span><span class="sxs-lookup"><span data-stu-id="9da1c-129">New Windows functions for pixel formats and double buffering</span></span>

    <span data-ttu-id="9da1c-130">Queste funzioni supportano i formati pixel per finestra e il doppio buffer (per le modifiche apportate alle immagini) di Windows.</span><span class="sxs-lookup"><span data-stu-id="9da1c-130">These functions support per-window pixel formats and double buffering (for smooth image changes) of windows.</span></span> <span data-ttu-id="9da1c-131">Queste nuove funzioni si applicano solo alle finestre grafiche OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9da1c-131">These new functions apply only to OpenGL graphics windows.</span></span>

 

 




