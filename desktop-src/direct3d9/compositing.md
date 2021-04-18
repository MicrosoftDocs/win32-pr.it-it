---
description: L'applicazione può usare il buffer dello stencil per le immagini 2D o 3D composite su una scena 3D.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Composizione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305306"
---
# <a name="compositing-direct3d-9"></a><span data-ttu-id="c8ef4-103">Composizione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c8ef4-103">Compositing (Direct3D 9)</span></span>

<span data-ttu-id="c8ef4-104">L'applicazione può usare il buffer dello stencil per le immagini 2D o 3D composite su una scena 3D.</span><span class="sxs-lookup"><span data-stu-id="c8ef4-104">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="c8ef4-105">Una maschera nel buffer dello stencil viene utilizzata per occludere un'area della superficie di destinazione del rendering.</span><span class="sxs-lookup"><span data-stu-id="c8ef4-105">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="c8ef4-106">Le informazioni 2D archiviate, ad esempio testo o bitmap, possono quindi essere scritte nell'area.</span><span class="sxs-lookup"><span data-stu-id="c8ef4-106">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="c8ef4-107">In alternativa, l'applicazione è in grado di eseguire il rendering di primitive 3D nell'area mascherata dallo stencil della superficie di destinazione per il rendering.</span><span class="sxs-lookup"><span data-stu-id="c8ef4-107">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="c8ef4-108">È anche possibile eseguire il rendering di un'intera scena.</span><span class="sxs-lookup"><span data-stu-id="c8ef4-108">It can even render an entire scene.</span></span>

<span data-ttu-id="c8ef4-109">I giochi spesso compostano contemporaneamente più scene 3D.</span><span class="sxs-lookup"><span data-stu-id="c8ef4-109">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="c8ef4-110">Ad esempio, per la guida dei giochi viene in genere visualizzato un mirror di visualizzazione posteriore.</span><span class="sxs-lookup"><span data-stu-id="c8ef4-110">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="c8ef4-111">Il mirror contiene la visualizzazione della scena 3D dietro il driver.</span><span class="sxs-lookup"><span data-stu-id="c8ef4-111">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="c8ef4-112">Si tratta essenzialmente di una seconda scena 3D composita con la visualizzazione in diretta del driver.</span><span class="sxs-lookup"><span data-stu-id="c8ef4-112">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8ef4-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8ef4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8ef4-114">Tecniche del buffer dello stencil</span><span class="sxs-lookup"><span data-stu-id="c8ef4-114">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



