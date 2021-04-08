---
description: Accesso alle superfici di DirectDraw
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Accesso alle superfici di DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1acdd122fa7d21fd49868c45f065f59b06ad8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876973"
---
# <a name="access-to-directdraw-surfaces"></a><span data-ttu-id="c2e0f-103">Accesso alle superfici di DirectDraw</span><span class="sxs-lookup"><span data-stu-id="c2e0f-103">Access to DirectDraw Surfaces</span></span>

<span data-ttu-id="c2e0f-104">Gli oggetti multimediali di esempio forniti da VMR ai filtri upstream supportano l'interfaccia [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) .</span><span class="sxs-lookup"><span data-stu-id="c2e0f-104">The Media Sample objects provided by the VMR to upstream filters support the [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) interface.</span></span> <span data-ttu-id="c2e0f-105">Per ottenere l'interfaccia, chiamare QueryInterface sull'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) e specificare IID \_ IVMRSurface.</span><span class="sxs-lookup"><span data-stu-id="c2e0f-105">To obtain the interface, call QueryInterface on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface and specify IID\_IVMRSurface.</span></span> <span data-ttu-id="c2e0f-106">I filtri upstream possono quindi usare i metodi IVMRSurface per accedere e modificare la superficie creata da VMR.</span><span class="sxs-lookup"><span data-stu-id="c2e0f-106">Upstream filters can then use the IVMRSurface methods to access and manipulate the surface that has been created by the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2e0f-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2e0f-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2e0f-108">Uso di VMR per gli sviluppatori di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="c2e0f-108">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



