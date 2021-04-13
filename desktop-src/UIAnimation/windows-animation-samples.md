---
title: Esempi di animazioni Windows
description: Negli argomenti contenuti in questa sezione vengono fornite informazioni dettagliate sugli esempi di codice che supportano la documentazione di Windows Animation Manager.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Animazione Windows Animation Windows, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331644"
---
# <a name="windows-animation-samples"></a><span data-ttu-id="1ce40-104">Esempi di animazioni Windows</span><span class="sxs-lookup"><span data-stu-id="1ce40-104">Windows Animation Samples</span></span>

<span data-ttu-id="1ce40-105">Negli argomenti contenuti in questa sezione vengono fornite informazioni dettagliate sugli esempi di codice che supportano la documentazione di Windows Animation Manager.</span><span class="sxs-lookup"><span data-stu-id="1ce40-105">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1ce40-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="1ce40-106">In this section</span></span>



| <span data-ttu-id="1ce40-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="1ce40-107">Topic</span></span>                                                                                     | <span data-ttu-id="1ce40-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ce40-108">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ce40-109">Esempio di animazione basata su applicazioni</span><span class="sxs-lookup"><span data-stu-id="1ce40-109">Application-Driven Animation Sample</span></span>](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [<span data-ttu-id="1ce40-110">Esempio di animazione basata su timer</span><span class="sxs-lookup"><span data-stu-id="1ce40-110">Timer-Driven Animation Sample</span></span>](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [<span data-ttu-id="1ce40-111">Esempio di interpolazione personalizzata</span><span class="sxs-lookup"><span data-stu-id="1ce40-111">Custom Interpolator Sample</span></span>](custom-interpolator-sample.md)<br/>                   | <span data-ttu-id="1ce40-112">Viene illustrato come utilizzare l'animazione Windows con un interpolatore personalizzato, con Direct2D utilizzato per il rendering.</span><span class="sxs-lookup"><span data-stu-id="1ce40-112">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <br/> |
| [<span data-ttu-id="1ce40-113">Esempio di layout di griglia</span><span class="sxs-lookup"><span data-stu-id="1ce40-113">Grid Layout Sample</span></span>](grid-layout-sample.md)<br/>                                   | <span data-ttu-id="1ce40-114">Viene illustrato come utilizzare l'animazione Windows utilizzando Direct2D per animare una griglia di immagini.</span><span class="sxs-lookup"><span data-stu-id="1ce40-114">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span> <br/>                         |
| [<span data-ttu-id="1ce40-115">Esempio di confronto prioritario</span><span class="sxs-lookup"><span data-stu-id="1ce40-115">Priority Comparison Sample</span></span>](priority-comparison-sample.md)<br/>                   | <span data-ttu-id="1ce40-116">Viene illustrato come utilizzare l'animazione Windows con un confronto prioritario tramite Direct2D per il rendering.</span><span class="sxs-lookup"><span data-stu-id="1ce40-116">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span><br/>      |



 

## <a name="sample-files"></a><span data-ttu-id="1ce40-117">File di esempio</span><span class="sxs-lookup"><span data-stu-id="1ce40-117">Sample Files</span></span>

<span data-ttu-id="1ce40-118">Ogni esempio contiene molti dei file di chiave seguenti:</span><span class="sxs-lookup"><span data-stu-id="1ce40-118">Each sample contains many of the following key files:</span></span>

<dl> <dt>

<span data-ttu-id="1ce40-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application. cpp</span><span class="sxs-lookup"><span data-stu-id="1ce40-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application.cpp</span></span>
</dt> <dd>

<span data-ttu-id="1ce40-120">Definisce il punto di ingresso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1ce40-120">Defines the application entry point.</span></span>

</dd> <dt>

<span data-ttu-id="1ce40-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow. h</span><span class="sxs-lookup"><span data-stu-id="1ce40-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow.h</span></span>
</dt> <dd>

<span data-ttu-id="1ce40-122">Dichiara la classe CMainWindow.</span><span class="sxs-lookup"><span data-stu-id="1ce40-122">Declares the CMainWindow class.</span></span>

</dd> <dt>

<span data-ttu-id="1ce40-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow. cpp</span><span class="sxs-lookup"><span data-stu-id="1ce40-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow.cpp</span></span>
</dt> <dd>

<span data-ttu-id="1ce40-124">Inizializza i componenti di animazione e la piattaforma grafica, carica le immagini ed esegue il rendering dell'area client.</span><span class="sxs-lookup"><span data-stu-id="1ce40-124">Initializes the animation components and the graphics platform, loads images, and renders the client area.</span></span>

</dd> <dt>

<span data-ttu-id="1ce40-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager. h</span><span class="sxs-lookup"><span data-stu-id="1ce40-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager.h</span></span>
</dt> <dd>

<span data-ttu-id="1ce40-126">Dichiara la classe CLayoutManager.</span><span class="sxs-lookup"><span data-stu-id="1ce40-126">Declares the CLayoutManager class.</span></span>

</dd> <dt>

<span data-ttu-id="1ce40-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager. cpp</span><span class="sxs-lookup"><span data-stu-id="1ce40-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager.cpp</span></span>
</dt> <dd>

<span data-ttu-id="1ce40-128">Calcola il layout delle immagini nella finestra principale, crea gli storyboard, aggiunge le transizioni allo storyboard e pianifica lo storyboard.</span><span class="sxs-lookup"><span data-stu-id="1ce40-128">Calculates the layout of images in the main window, creates storyboards, adds transitions to the storyboard, and schedules the storyboard.</span></span>

</dd> <dt>

<span data-ttu-id="1ce40-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Anteprima. h</span><span class="sxs-lookup"><span data-stu-id="1ce40-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail.h</span></span>
</dt> <dd>

<span data-ttu-id="1ce40-130">Dichiara la classe CThumbNail.</span><span class="sxs-lookup"><span data-stu-id="1ce40-130">Declares the CThumbNail class.</span></span>

</dd> <dt>

<span data-ttu-id="1ce40-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Anteprima. cpp</span><span class="sxs-lookup"><span data-stu-id="1ce40-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail.cpp</span></span>
</dt> <dd>

<span data-ttu-id="1ce40-132">Crea variabili di animazione ed esegue il rendering delle anteprime.</span><span class="sxs-lookup"><span data-stu-id="1ce40-132">Creates animation variables and renders thumbnails.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="1ce40-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ce40-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ce40-134">Guida allo sviluppo di animazioni Windows</span><span class="sxs-lookup"><span data-stu-id="1ce40-134">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)
</dt> <dt>

[<span data-ttu-id="1ce40-135">Informazioni di riferimento sull'animazione Windows</span><span class="sxs-lookup"><span data-stu-id="1ce40-135">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

 





