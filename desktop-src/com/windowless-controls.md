---
title: Controlli senza finestra
description: Controlli senza finestra
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396919"
---
# <a name="windowless-controls"></a><span data-ttu-id="8c80c-103">Controlli senza finestra</span><span class="sxs-lookup"><span data-stu-id="8c80c-103">Windowless Controls</span></span>

<span data-ttu-id="8c80c-104">La specifica ActiveX Controls 96 include una definizione per i controlli privi di finestra.</span><span class="sxs-lookup"><span data-stu-id="8c80c-104">The ActiveX Controls 96 specification includes a definition for windowless controls.</span></span> <span data-ttu-id="8c80c-105">Questi controlli non funzionano nella propria finestra e richiedono che un contenitore offra una finestra condivisa in cui il controllo può essere disegnato, vedere ActiveX SDK.</span><span class="sxs-lookup"><span data-stu-id="8c80c-105">Such controls do not operate in their own window and require a container to offer a shared window into which the control may draw, see the ActiveX SDK.</span></span> <span data-ttu-id="8c80c-106">I controlli privi di finestra sono progettati per essere compatibili con i contenitori di controllo meno recenti creando una propria finestra in questa situazione, i contenitori di controllo senza finestra devono ospitare controlli con finestra in modo tradizionale senza problemi.</span><span class="sxs-lookup"><span data-stu-id="8c80c-106">Windowless controls are designed to be compatible with older control containers by creating their own window in that situation, windowless control containers should host windowed controls in the traditional way with no problem.</span></span> <span data-ttu-id="8c80c-107">Può tuttavia essere utile per un contenitore distinguere i controlli che possono funzionare in modalità senza finestra, quindi viene definita una categoria di componenti appropriata.</span><span class="sxs-lookup"><span data-stu-id="8c80c-107">It may however be useful for a container to distinguish those controls that can operate in a windowless mode, so an appropriate component category is defined.</span></span>

<span data-ttu-id="8c80c-108">CATId-{1D06B600-3AE3-11cf-87B9-00AA006C8166} CATId \_ WindowlessObject</span><span class="sxs-lookup"><span data-stu-id="8c80c-108">CATID - {1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID\_WindowlessObject</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c80c-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c80c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c80c-110">Categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="8c80c-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




