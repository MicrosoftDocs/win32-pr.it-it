---
description: CSourcePosition è una classe astratta per l'implementazione dell'interfaccia IMediaPosition in un filtro di origine.
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: Classe CSourcePosition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourcePosition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0b88289381641edcef5922557862729acbb81f54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303774"
---
# <a name="csourceposition-class"></a><span data-ttu-id="d6853-103">Classe CSourcePosition</span><span class="sxs-lookup"><span data-stu-id="d6853-103">CSourcePosition class</span></span>

<span data-ttu-id="d6853-104">`CSourcePosition` è una classe astratta per l'implementazione dell'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) in un filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="d6853-104">`CSourcePosition` is an abstract class for implementing the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface on a source filter.</span></span>

<span data-ttu-id="d6853-105">Questa classe è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d6853-105">This class is obsolete.</span></span> <span data-ttu-id="d6853-106">Se il filtro di origine è ricercabile, deve esporre l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) anziché **IMediaPosition**.</span><span class="sxs-lookup"><span data-stu-id="d6853-106">If your source filter is seekable, it should expose the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface instead of **IMediaPosition**.</span></span> <span data-ttu-id="d6853-107">A questo scopo, è possibile usare la classe di base [**CSourceSeeking**](csourceseeking.md) .</span><span class="sxs-lookup"><span data-stu-id="d6853-107">You can use the [**CSourceSeeking**](csourceseeking.md) base class for this purpose.</span></span>

 

 



